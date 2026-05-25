# The Missing Layer Between Agents and Codebases

When coding agents work on a non-trivial codebase, the failure mode is familiar. The model reads the right files, references the right functions, and produces changes that look reasonable. Yet the result still drifts from how the system is actually supposed to behave.

This usually does not happen because the model is blind or careless. It happens because the codebase has not exposed its own operating rules clearly enough. The missing layer is the layer that tells the agent what must stay true.

---

## Code Is Not the Whole System

A codebase contains more than syntax and control flow. It also contains architectural boundaries, naming expectations, invariants, review norms, test assumptions, ownership lines, and patterns that are supposed to repeat. Humans often learn these gradually through repetition, correction, and team memory.

An agent does not get that ambient learning. It only gets what is visible in the artifacts you surface. If the system’s rules are implicit, the model will still produce output, but it will do so by reconstructing the architecture from incomplete signals.

---

## Why “Looks Right” Is Not Enough

Generated changes often fail in a specific way: they satisfy the local code request while violating the broader system pattern. A helper gets introduced in the wrong layer. A data shape is reused where a translation boundary should exist. A shortcut bypasses a validation rule. A feature works in isolation but weakens the architecture.

This is why coding-agent failures are often subtle. The code compiles. The tests may even pass. But the change is still wrong in the way that matters to the maintainers.

---

## The Missing Layer Is About Invariants

What the agent needs is not just more code. It needs better visibility into the invariants that govern the code. That includes things like:

- which layers may depend on which others
- which models are internal versus external
- where side effects are allowed
- what every handler or component must preserve
- what kinds of changes require broader review

These are not optional niceties. They are the rules that keep a system coherent as it evolves.

---

## Agents Need More Than Retrieval

Simple file retrieval is not enough here. An agent can retrieve the relevant files and still miss the system pattern that ties them together. That is why repositories with good local code and weak architectural surfaces still produce weak agent behavior.

What helps is a layer of explicit guidance that the agent can actually operate against: architecture notes, invariant lists, scoped working rules, boundary documentation, and examples of acceptable versus unacceptable changes. This does not replace the code. It makes the codebase interpretable.

---

## Turn Architecture Into a Working Surface

The best developer environments for agents do not just expose files. They expose a usable working surface. That surface might include:

- concise architectural rules
- allowed dependency directions
- expected test obligations
- definitions of critical domain boundaries
- known anti-patterns to avoid

Once these are explicit, the agent has a better chance of producing changes that fit the system rather than merely touching the right files.

---

## This Is a Software Design Problem

It is tempting to treat this as a prompt problem. Write better instructions. Add more warnings. Repeat the constraints in a longer preamble. Sometimes that helps a little, but it is usually not enough. If the system cannot state its own rules clearly, the agent will continue guessing.

That is why this is really a software design problem. The codebase needs a better way to project its own structure outward to the tools operating on it.

---

## Final Thought

Coding agents do not drift from intent only because models are imperfect. They drift because many codebases still rely on humans to infer rules that were never made explicit.

If you want agents to make changes that hold together, do not just expose the code. Expose the invariants.

---

More depth: [The Missing Layer Between Agents and Codebases on Substack](https://glcapps.substack.com/p/the-missing-layer-between-agents)
