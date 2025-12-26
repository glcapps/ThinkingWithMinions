# Budgeting for Thinking

When working with LLMs, the question isn’t just *how long will this take* but *how much effort am I asking the system to expend?*

That effort has consequences. Longer prompts, broader context, repeated revisions, and deeper analysis all consume resources. The structure of your request directly shapes both the behavior of the system and the cost of using it.

## Different tasks consume different effort

Not all requests are equal.

A straightforward rewrite or summary consumes relatively little effort. A multi-step analysis that requires maintaining context, synthesizing information, or coordinating tools consumes significantly more.

- Repetition and redundant context increase processing load
- Larger or more capable models require more resources per step
- Structured reasoning often requires multiple passes rather than a single response

Efficiency comes from matching the task to the level of effort required — not from treating all prompts the same.

## Budgeting by phase

Most complex uses of AI can be decomposed into distinct phases of work:

1. **Scouting**: Asking exploratory questions or generating broad ideas
2. **Scaffolding**: Creating outlines, plans, and stepwise instructions
3. **Execution**: Doing the work—writing, rewriting, converting formats
4. **Evaluation**: Reviewing output or proposing revisions

Each phase has a different interaction profile. Exploration is usually light. Evaluation can become heavy if it requires revisiting large amounts of prior context. Designing with these differences in mind keeps systems responsive and predictable.

## Think in terms of workload

Every interaction places load on the system. Broad prompts, long histories, and unfocused goals increase that load without guaranteeing better results.

Breaking work into smaller steps, constraining context, and pausing between phases reduces wasted effort and improves clarity.

## Plan your ask, not just your answer

Before launching a prompt, ask yourself:

- What level of capability does this task actually require?
- Can the work be split into clearer stages?
- Do I want intermediate output before committing to a full response?

A little forethought saves more than tokens. It improves results, too.

Managing effort isn’t stinginess. It’s how you design reliable systems.