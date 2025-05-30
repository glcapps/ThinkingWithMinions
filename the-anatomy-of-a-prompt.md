


## The Anatomy of a Prompt

Large Language Models (LLMs) can be valuable assets in business workflows — but their usefulness depends almost entirely on how they’re asked to help. In business, where clarity, repeatability, and reliability matter more than novelty, an imprecise prompt often leads to unclear or unusable results.

To get consistent, valuable results, prompts need to behave more like a **briefing packet** than a one-line question. Here’s a practical structure that any business user can follow — even without technical training.

---

### 1. Clarify the Task

Start by defining what kind of thinking or output you want. Be simple and honest:

- “Summarize this set of notes”
- “Highlight possible risks”
- “Draft a checklist for this process”
- “Ask clarifying questions about this policy”

This is the **framing**. You're not giving an answer or asking a question — you’re stating what the model should be doing, as if briefing a junior analyst for a deliverable.

Avoid pretending the LLM already knows what’s going on. Begin fresh each time.

---

### 2. Provide Structured Reference

This is the **heart of the prompt**. Instead of relying on the LLM’s training or memory, give it what it needs to work from.

The best format? Markdown, XML, or even just well-formatted plain text.

Example:
```markdown
## Expense Reimbursement Policy
- Requests must be submitted within 30 days
- Manager approval required
- Receipts mandatory for all expenses
```

This tells the LLM: *"Here's your source material. Work within it."*

Treat this as supplying the model with authoritative reference material — not just hoping the AI "knows enough."

---

### 3. Give a Direct Instruction

Now that the model has its footing, be specific:

- “Create a summary of the above in bullet form”
- “Identify any ambiguous rules in this policy”
- “Convert this to employee-facing language”

No flourish. No open-ended curiosity. Provide a clear directive using straightforward language.

---

### 4. Set the Tone of the Answer

What professional tone should the response adopt?
- A helpful internal policy advisor
- A small business consultant
- A legal summary writer

Specify this in a final line, for example:

> Respond as if writing a memo to a department manager unfamiliar with this topic.

This final element guides the tone and audience alignment of the response.

---

### Example Prompt (Complete)

Here’s what the full four-part structure might look like:

```
You are assisting with policy onboarding.

## Reference Material
### PTO Policy
- All full-time employees receive 15 PTO days per year
- PTO must be requested via the HR portal
- Blackout periods apply during Q4

## Task
Summarize this policy in plain English.

## Response Format
Write in the voice of a helpful internal advisor writing for a company FAQ page.
```

---

### Final Thought

This structure isn’t just about better answers — it’s about better conversations. When business users approach prompts as structured instructions — and treat LLM task briefing as a business process — they receive dependable, context-aware output.

Think of it less like “prompt engineering” and more like **LLM task briefing**. That’s the new skill. And it’s learnable.
