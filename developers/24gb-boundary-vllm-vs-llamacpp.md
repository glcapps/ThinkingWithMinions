# Agentic LLM Systems at the 24 GB Boundary: vLLM vs llama.cpp

## Framing the problem (from lived reality, not theory)

This article is written from the perspective of someone *already running serious agentic workloads locally* on a **single 24 GB NVIDIA GPU**. Not benchmarking experiments. Not speculative stacks. Real, long‑lived sessions where the model is expected to function as a persistent cognitive workspace.

The concrete baseline we start from is specific and non‑negotiable:

- A 20–30B‑class dense model (e.g. **Devstral‑Small‑2‑24B**)
- **~65k tokens of active context**
- All layers resident on GPU
- No CPU offload
- Single‑agent, CLI‑driven or service‑driven workflows

That setup already works today with **llama.cpp**, including an **OpenAI‑compatible endpoint**, albeit with some ergonomic and API‑level rough edges.

So the question is not *whether* 24 GB is enough. It demonstrably is.

The real question is sharper:

> **Which inference stack lets you inhabit this exact memory boundary reliably while you are building agentic systems on top of it?**

---

## The memory reality at 24 GB (this is the boundary)

Before comparing stacks philosophically, it helps to ground the discussion in the actual VRAM budget for this workload.

For a single agent running ~65k context on a 24 GB GPU, the memory picture looks like this:

### VRAM usage comparison (~65k context, batch=1)

| Stack | Weights | KV cache | Attention / scratch / misc | Total VRAM | Outcome |
|---|---|---|---|---|---|
| **llama.cpp (Q4_K_M)** | ~13–14 GB | ~6–7 GB | ~3–4 GB | **~23–24 GB** | ✅ Proven, stable |
| **vLLM (4‑bit weights, FP16 KV)** | ~13–14 GB | ~14–16 GB | ~3–4 GB | **~31–34 GB** | ❌ Impossible |
| **vLLM + TurboQuant KV** | ~13–14 GB | ~4–5 GB | ~3–4 GB | **~20–23 GB** | ✅ Plausible |
| **vLLM + TurboQuant KV + nvfp4** | ~11–12 GB | ~4–5 GB | ~3–4 GB | **~18–21 GB** | ✅ Comfortable |

This table is not theoretical. It matches what can be observed in practice when running real workloads.

Two conclusions fall directly out of it:

1. **llama.cpp already occupies the maximum feasible envelope at 24 GB**.
2. **vLLM was historically excluded from this envelope solely due to KV cache behavior**.

Everything else in this article follows from those facts.

---

## llama.cpp at 24 GB: proof, not promise

### Why llama.cpp works at the edge

llama.cpp’s advantage is not conceptual sophistication; it is simply that it spends memory in a way that respects the boundary.

At ~65k context:

- Weights sit compactly in ~14 GB
- KV cache consumes most of the remaining headroom
- There is just enough space left for attention scratch and runtime overhead

The result is **a stable equilibrium**:

> no KV eviction, no CPU spill, no latency cliffs.

From the agent’s point of view, this translates to:

- Long reasoning chains that remain intact
- Multi‑hour workflows without aggressive summarization
- A model that remembers *why* it made earlier decisions

### The OpenAI endpoint (and why it still matters)

llama.cpp can and does serve an OpenAI‑compatible endpoint in this configuration, which is why it is usable today in agentic setups.

However, this endpoint shows its limits when pushed beyond basic usage:

- Tool‑calling semantics can be inconsistent
- Streaming and cancellation support is rough
- Concurrency and lifecycle control are minimal

In short:

> llama.cpp secures the **data‑plane guarantee** (memory and execution), but offers only a thin **control plane**.

That trade‑off is acceptable if memory viability is the overriding concern — and for a long time, it had to be.

---

## vLLM at 24 GB: exclusion, then convergence

### Why vLLM used to fail outright

Prior to KV cache compression, vLLM simply could not meet the same constraints.

The table makes this obvious:

- FP16 KV cache alone exceeds 14 GB at 65k context
- Even with 4‑bit weights, total VRAM demand lands far beyond 24 GB

That failure mode was absolute. No tuning could fix it.

### Why people still wanted vLLM

Despite this, vLLM remained attractive for one reason:

> **It natively solves agent‑building problems that llama.cpp pushes onto the user.**

Specifically:

- Robust OpenAI‑compatible APIs
- First‑class tool calling
- Async scheduling and request management
- Cleaner integration with agent frameworks

This is the *control‑plane gap* that motivated the entire comparison.

---

## The convergence: KV compression changes the equation

The table shows exactly where convergence happens.

With modern KV compression (TurboQuant‑class approaches):

- vLLM’s KV cache drops from ~15 GB to ~4–5 GB
- Total VRAM usage drops below the 24 GB line

This does **not** make vLLM superior to llama.cpp at the edge.

It does something more subtle and more important:

> **It allows vLLM to stand on the exact same narrow ledge that llama.cpp already occupies.**

At that point, the comparison stops being about feasibility and becomes architectural.

---

## Where nvfp4 actually helps

Low‑precision formats like nvfp4 do not move the memory boundary. The table makes that clear.

Their contribution is different:

- They trim ~1–2 GB from the weight budget
- That space absorbs allocator overhead, tool metadata, and logging
- The system moves from *knife‑edge* to *operable with margin*

Put simply:

> nvfp4 does not enable this workload — it makes it survivable in real systems.

For agent builders who add complexity incrementally, this matters.

---

## Making the choice as an agent builder

With the memory gap closed, the decision becomes clearer.

### llama.cpp is the right choice if:

- You want maximum long‑context reliability at 24 GB
- You accept building or patching your own agent control logic
- Single‑agent workflows dominate

### vLLM becomes viable if:

- You want robust tool calling and orchestration
- You rely on clean OpenAI semantics
- You accept operating near the memory edge
- You are willing to trade some efficiency for control‑plane leverage

Put differently:

> llama.cpp defines the **floor of feasibility**. vLLM defines the **space above it**, now that it can finally reach the same floor.

---

## The real shift at 24 GB

The key change is not that 24 GB GPUs became powerful.

It is that:

- The exact memory boundary for serious local agents has been measured
- One stack already lives there comfortably
- Another can now join it, with help

Once that is true, agent design becomes a matter of *preference and architecture*, not survival.

That is the real significance of the current moment.

---

## Closing

At the 24 GB boundary, **llama.cpp proves what is possible**. **vLLM is now approaching parity where it matters most**.

The most interesting work ahead is not squeezing in more tokens, but deciding how much structure, scheduling, and abstraction you want layered onto a system that already just barely fits.

Those are the right problems to be arguing about.
