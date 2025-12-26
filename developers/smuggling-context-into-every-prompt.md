# Carrying Context Explicitly

Not every platform provides long-term memory, tool hooks, or system-level configuration. In constrained environments, context still matters—but it must be supplied deliberately.

This is not about bypassing safeguards or manipulating behavior. It is about making expectations, constraints, and domain assumptions explicit at the point of use.

---

## Establishing shared framing

Even without persistent memory, a consistent framing can be established by repeating the same structural cues. For example, start every prompt with something like:

```
Context: You are a legal assistant for a small claims advisor.

Task: Extract the following details...
```

Doing this consistently trains the model, even session by session, to treat your input a certain way.

---

## Packing With Precision

Avoid bloated context. The goal is not volume, but relevance. You’re not dumping a folder of background at the top of every input—you’re setting the stage.

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

When APIs support structured function or tool definitions, descriptions and schemas can carry contextual constraints alongside signatures. If you're calling something like `generate_meeting_summary`, you can add structured cues in its schema or documentation. Treat these as part of the interface contract.

---

## Prompting as a shared practice

The shift is procedural rather than tactical. Instead of searching for a single optimal prompt, teams benefit from agreeing on shared framing, structure, and vocabulary.

Prompt conventions can be reviewed, versioned, and evolved in the same way as other interface definitions.

---

## What This Enables

- Fewer hallucinations from ambiguity
- Stronger consistency in tone and persona
- Prompt reuse across workflows
- Composable prompt structures across workflows

This approach builds scaffolding that improves reliability by making context explicit, inspectable, and repeatable—regardless of platform capabilities.