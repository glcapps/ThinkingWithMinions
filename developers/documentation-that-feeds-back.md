# Documentation That Feeds Back

Most developer documentation is written once and read passively. It explains, but it does not participate.

When LLMs are part of the toolchain, documentation can become an input to ongoing work rather than a static artifact. This is no longer speculative. Coding agents now read repository instruction files—AGENTS.md, CLAUDE.md, and similar—before they start work, and many tools pull in project docs on request.

## Start with structured notes

When writing documentation—inline comments, README files, or usage guides—assume it will be consumed by both people and systems.

- Use consistent headings
- Prefer examples over prose
- Clarify assumptions, inputs, and outcomes

The goal is not verbosity. It is consistency. Predictable structure makes documentation usable beyond human skimming.

## Design for reuse

Documentation becomes more valuable when it can be reused by tools, not just read by people.

This does not require retraining models.

- Prompt inputs: documentation is incorporated into structured instructions
- Retrieval material: architecture and usage notes support lookup and reference
- Agent instructions: conventions and constraints that agents load before they start

Over time, this allows tools to reflect established explanations and conventions without inventing new ones.

## Put intent where the work happens

Agents often meet code through a search hit or a narrow edit, not a full read. Intent that lives only in a distant design doc may never reach them.

Durable comments near the point of change—an invariant, an environmental constraint, a warning against a tempting cleanup—do work a README can’t. Temporary working notes are different. Once the uncertainty they track is resolved, remove them. A stale hypothesis left in the code becomes false authority for the next reader.

## Examples

- A repository instruction file that tells coding agents how to build, test, and stay inside the architecture
- A CI tool that explains test failures using comments from past commits
- A CLI helper that draws usage tips from the most up-to-date README

## Active documentation

When your documentation is written with the assistant in mind—and your assistant is designed to consume it—knowledge doesn’t rot. It cycles. It informs.

Documentation that feeds back does not replace understanding. It reinforces it.

Write documentation that can be used, not just read.