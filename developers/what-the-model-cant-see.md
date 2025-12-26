# What the Model Can’t See

Large language models operate within strict boundaries. Some of those boundaries are obvious—such as not having access to your screen or running processes. Others are more subtle and are often overlooked in practice.

This article describes those boundaries, with a focus on how missing context, state, and signals affect reliability in development and IT workflows.

---

## No direct access to your environment

A model can’t read your terminal, your screen, or your editor window. It doesn’t see which file you’re in, which variable is highlighted, or what output just scrolled by. This is different from human collaboration, where even a glance can change everything.

If information is not explicitly provided, it is not available. The model may infer or approximate, but inference is not access.

---

## No Memory of What You Didn’t Say

Models do not retain context unless it is supplied or explicitly stored by surrounding systems. Assumptions about continuity across sessions or tasks lead to gaps in behavior.

This matters especially when you're working across multiple sessions or switching between projects. Without explicit carryover, reasoning starts from an incomplete picture.

---

## No Real-Time Awareness

Unlike your IDE or your debugger, the model isn’t connected to the execution state of your application. It can’t tell which breakpoints are set, what your stack trace says, or what line threw the error. That has to be relayed manually, or through tools that bind model interaction to your environment.

Execution state, breakpoints, and runtime errors are not visible unless they are surfaced as input. Integration can bridge this gap, but the limitation exists by default.

---

## The risk of inferred understanding

Models produce coherent output even when underlying assumptions are wrong. Apparent confidence is a property of fluent generation, not verification.

This is not a flaw to be fixed. It is a constraint to design around.

---

## Practical Advice

- State the task and environment explicitly.
- Provide relevant output, logs, or traces as text.
- Refer to concrete files, functions, or symbols rather than pronouns.
- Treat prompts as environment descriptions, not questions alone.

---

## Closing

Models do not observe your work. They operate on what is presented.

Making context explicit is not verbosity. It is how reliability is achieved.