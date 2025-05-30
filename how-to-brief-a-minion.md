# How to Brief a Minion

> **Prompt:**  
> Write a 1200–1400 word article titled **“How to Brief a Minion: Designing Prompts with Structure and Intent.”**  
>
> The article should introduce a four-part structure for serious prompt design:
> 
> 1. **Topic Clarification** — A short, clear explanation of what the prompt is about  
> 2. **Structured Reference Material** — Background data in Markdown, XML, JSON, or tables  
> 3. **Task Prompt** — The action or instruction for the assistant to take  
> 4. **Answering Manner / Tone** — The role, voice, or style the minion should adopt when replying
>
> Emphasize how this structure elevates prompt writing from casual querying to repeatable delegation.  
> Explain how each part reduces guesswork and improves consistency.  
> Include examples, especially for structured inputs like XML or Markdown.  
> 
> Close with a reflection: this method helps users shift from ad hoc prompting to **a mindset of reusable workflows.**

---

## How to Brief a Minion: Designing Prompts with Structure and Intent

When people first use a large language model (LLM), their instinct is to type a question the same way they might into Google. But LLMs aren’t search engines. They’re more like eager junior analysts: capable, fast, but reliant on context and instruction. To get great results, you don’t just ask. You **brief**.

Here’s how to think about it.

### Why Briefing Matters

Every business user knows the difference between a good delegation and a vague request. If you delegate a task without specifying the expectations, resources, or outcome criteria, you’ll likely get back something misaligned. The same is true for LLMs.

The best prompts aren’t improvised queries. They’re clear structures.

This article introduces a four-part method for writing serious, reusable prompts. Whether you’re drafting emails, reviewing contracts, or summarizing meeting notes, this format helps you treat your LLM as a capable collaborator.

---

### 1. **Topic Clarification**  
Start with a one- or two-sentence explanation of what the task is about. Think of it as the subject line of a memo.

**Example:**  
“This prompt is about summarizing customer support calls into internal performance reports.”

Clarity here sets the stage. It tells the LLM what universe it’s operating in.

---

### 2. **Structured Reference Material**  
This is the biggest upgrade from casual prompting. Rather than hoping the LLM already knows, you supply the background. And you format it clearly.

Use:
- Markdown (for lists, headings, comments)
- XML or JSON (if you want precision)
- Tables or bullet points (for facts or attributes)

**Example in Markdown:**

```
## Client Feedback
- “Response time was too slow.”
- “Agent was polite but didn’t resolve issue.”

## Call Metadata
- Agent: Sam R
- Duration: 12m 44s
- Outcome: Escalated to Tier 2
```

This gives the model the structured context a trained assistant would expect before beginning a task.

---

### 3. **Task Prompt**  
Now, give the instruction. Keep it tight, but specific.

**Examples:**
- “Summarize the feedback in a professional internal memo.”  
- “Draft a follow-up email based on the above.”  
- “Rewrite this to be more persuasive but retain factual accuracy.”

If you're combining this with tool use or multi-step flows, break it down step by step. But in most business settings, a well-phrased task is enough.

---

### 4. **Answering Manner / Tone**  
This is your chance to shape the voice and style. It also sets boundaries.

**Examples:**
- “Respond as a calm and professional customer service manager.”  
- “Use plain English, short paragraphs.”  
- “Summarize like a business analyst reporting to the CEO.”

This helps control for the LLM’s tendency to drift into overexplaining or strange tone shifts.

---

### A Real Example

Here’s a full brief using all four parts:

---

**Topic Clarification:**  
Summarizing a legal document about a vendor contract

**Structured Reference Material:**
```markdown
## Contract Title
Exclusive Supply Agreement – Northeast Region

## Key Terms
- Duration: 24 months
- Termination clause: 30-day notice by either party
- Pricing: Tiered, based on volume
- Non-compete: Active for 12 months post-contract
```

**Task Prompt:**  
Summarize the contract for a general manager considering renewal.

**Answering Manner / Tone:**  
Use concise, neutral business language. Avoid legalese. Make the summary skimmable in under 200 words.

---

### Why This Works

- **Reduces Guesswork:** The LLM doesn’t have to guess what kind of answer you want.
- **Creates Repeatability:** You can reuse the same format for dozens of tasks.
- **Improves Trust:** Colleagues begin to see consistent quality from your LLM work.

It’s not about cleverness. It’s about clarity.

---

### From Prompting to Workflow

The real goal here isn’t just to write better prompts — it’s to **think in systems**.

Each time you use this format, you're building a repeatable workflow. One that can be stored, shared, and improved. One that lets someone else (human or minion) follow the same steps.

When documented and reused, this structure becomes a component of your knowledge workflow. It supports consistency across teams and helps futureproof your use of AI as business processes evolve.

This is how minions grow from novelty to necessity.

So next time you open a chat window, approach your prompts as you would any professional instruction—clearly, consistently, and with intent.