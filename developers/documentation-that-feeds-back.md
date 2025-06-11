# Documentation That Feeds Back

Most developer documentation is a one-way mirror. You write it for the next person, but it never speaks again. What if it could?

With LLMs embedded in your tooling, documentation becomes an *active participant* in the development cycle.

## Start with structured notes

When writing documentation—be it inline comments, README files, or usage guides—consider the LLM as part of your audience.

- Use consistent headings
- Prefer examples over prose
- Clarify assumptions, inputs, and outcomes

You're not just helping a human skim. You're building a predictable information surface for your AI tooling to grab hold of.

## Add feedback loops

Where it gets interesting is *when that same documentation becomes training data*. Not for a full retrain—but for prompt scaffolds, embedding sources, or memory anchoring.

- **Prompt scaffolding**: Your doc strings become parts of multi-step instructions.
- **Embedding source**: Your architecture docs support semantic search.
- **Memory cues**: Past explanations are referenced as working memory in tools.

In a well-wired workflow, your assistant can learn *how your team explains things*, not just what your code does.

## Examples

- A GitHub Copilot variant that suggests not just syntax but reasoning steps, based on design docs
- A CI tool that explains test failures using comments from past commits
- A CLI helper that draws usage tips from the most up-to-date README

## Active documentation

When your documentation is written with the assistant in mind—and your assistant is designed to consume it—knowledge doesn’t rot. It cycles. It informs.

Write docs that don’t just sit there.

Write docs that *talk back*.