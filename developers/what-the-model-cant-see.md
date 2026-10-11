# What the Model Can’t See

Large language models operate within strict boundaries. Some of those boundaries used to be obvious: a chat window could not see your screen or your running processes. Coding agents now work in terminals, read editor state, run tests, and in some setups operate a browser or desktop. The boundary has moved, but it has not disappeared. Other boundaries are more subtle and are often overlooked in practice.

This article describes those boundaries, with a focus on how missing context, state, and signals affect reliability in development and IT workflows.

---

## Only what the tools surface

A model does not see your environment directly. It sees what its tools return: the file an agent opened, the command output it captured, the screenshot it took. It does not see the file it didn’t open, the log it didn’t read, or the output that scrolled by before it looked. This is different from human collaboration, where even a glance can change everything.

If information is not surfaced, it is not available. The model may infer or approximate, but inference is not access. Choosing the tools is choosing what the model can see.

---

## No Memory of What You Didn’t Say

Models do not retain context unless it is supplied or explicitly stored by surrounding systems. Assumptions about continuity across sessions or tasks lead to gaps in behavior.

This matters especially when you're working across multiple sessions or switching between projects. Without explicit carryover, reasoning starts from an incomplete picture.

---

## No Real-Time Awareness

An agent that can run commands can observe a failing test or a stack trace—at the moment it runs them. It still isn’t watching the execution state of your application. It can’t tell which breakpoints are set or what changed between runs unless a tool reports it. Its view is a series of snapshots, not a live connection.

Execution state, breakpoints, and runtime errors are visible only when they are surfaced as input. Integration narrows this gap. It does not close it.

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
- Know which tools the agent has, and what each one can and cannot show it.

---

## Closing

Models do not observe your work. They operate on what is presented—by you, or by the tools you gave them.

Making context explicit is not verbosity. It is how reliability is achieved.