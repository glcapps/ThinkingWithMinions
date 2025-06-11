# Smuggling Context Into Every Prompt

Not every platform gives you fine-grained control of long-term memory, custom tool use, or even system prompts. But even in constrained environments, you can sneak in more context than you might think—if you do it deliberately.

This isn’t a workaround for jailbreaking or manipulation. It’s a legitimate practice for framing prompts with helpful, structured, in-domain cues. The trick is to know what context helps the model behave how you need it to—and then bake that in.

---

## A Hidden Outline of Shared Language

Even without memory, you can establish a shared framing. For example, start every prompt with something like:

```
Context: You are a legal assistant for a small claims advisor.

Task: Extract the following details...
```

Doing this consistently trains the model, even session by session, to treat your input a certain way. Some models may even infer latent context across prompts if they’re semantically close and well-structured.

---

## Packing With Precision

Avoid stuffing your context. The goal isn’t to overwhelm the model but to direct it. You’re not dumping a folder of background at the top of every input—you’re setting the stage.

Use formatting like:

```
Context:
- Client type: SMB
- Tool: Airtable
- Tone: Business-casual

Prompt:
Explain what went wrong in this workflow.
```

---

## Context Fragments in Function Descriptions

In tools like OpenAI's function calling, you can encode context in the function descriptions. If you're calling something like `generate_meeting_summary`, you can add structured cues in its schema or documentation. Treat these like micro-prompts in your API shape.

---

## Prompt Engineering Is Now Prompt Habit

The biggest shift is cultural. It’s no longer about one perfect prompt—it’s about disciplined prompt hygiene. Teams can agree on framing norms and templates, just like they agree on code style or API shape.

---

## What This Enables

- Fewer hallucinations from ambiguity
- Stronger consistency in tone and persona
- Prompt reuse across workflows
- A more composable minion approach

This is how you build scaffolding that helps your LLM collaborators perform reliably, even before you unlock memory or advanced APIs.