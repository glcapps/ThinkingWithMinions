# Context Chains, Not Retrieval Hacks

There’s a common impulse to treat context in LLM workflows like raw memory: include as much information as possible and assume the model will sort it out.

One response to this has been retrieval-based approaches, where external material is pulled in to expand what the model can see. That can be useful, but it is not the same thing as reasoning.

## Retrieval and reasoning solve different problems

What a model needs is not maximum information, but appropriately prepared information.

Retrieval gathers material. Reasoning depends on sequencing, framing, and relevance. Confusing these roles leads to prompts that are large but unfocused.

Retrieval surfaces candidate material.

Context construction decides what to keep, what to discard, and how to present it so the next step can succeed.

## Build context incrementally

Instead of assembling a single, comprehensive prompt, context can be built in stages, with each step preparing the next:

1. Provide a concise primer describing the relevant domain or task
2. Follow with **extraction**: Pull out only what’s needed from a larger source.
3. Add **focus**: Narrow down the current task and constrain the style or goal.
4. Deliver the final **action prompt**: Now the model is ready to perform.

This approach builds context *on the fly* and makes each step testable and debuggable.

## Why incremental context helps

- Reduces unnecessary context and cognitive load
- Makes assumptions and misunderstandings visible earlier
- Supports interruption, correction, and redirection
- Produces intermediate artifacts that are readable and testable

## When retrieval helps

To be clear: retrieval isn’t bad. It’s just one tool. Use it to *gather*, not to *explain*. Once relevant material is retrieved, it still needs to be interpreted. Summarization, filtering, and restructuring turn raw material into usable context.

## Method, not shortcut

Incremental context construction is not a workaround for model limitations. It is a general method for aligning information, intent, and action.

Don’t just retrieve. Prepare.
