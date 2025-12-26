# Documentation That Feeds Back

Most developer documentation is written once and read passively. It explains, but it does not participate.

When LLMs are part of the toolchain, documentation can become an input to ongoing work rather than a static artifact.

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
- Memory cues: prior explanations are reused to maintain continuity

Over time, this allows tools to reflect established explanations and conventions without inventing new ones.

## Examples

- A GitHub Copilot variant that suggests not just syntax but reasoning steps, based on design docs
- A CI tool that explains test failures using comments from past commits
- A CLI helper that draws usage tips from the most up-to-date README

## Active documentation

When your documentation is written with the assistant in mind—and your assistant is designed to consume it—knowledge doesn’t rot. It cycles. It informs.

Documentation that feeds back does not replace understanding. It reinforces it.

Write documentation that can be used, not just read.