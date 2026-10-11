# Memory Costs and Context Loops

One of the trickiest parts of working with LLMs is how their memory behaves. These tools can now hold hundreds of pages in “context,” and many products add memory features that carry notes from one conversation to the next. But neither one is the model remembering. Context is re-supplied on every turn, and memory is a system deciding what to re-supply. Sometimes that process loops back on itself in unexpected ways.

Let’s demystify how context windows, memory limits, and looping behavior affect the way we work with minions—and the systems around them.

## What Is Context, Really?

“Context” in LLMs is the rolling window of tokens (words, punctuation, formatting) that the model can see at once. It’s not memory in the traditional sense. It’s closer to a temporary working surface during a conversation.

When a long session nears the limit, many tools now compact it: older content is summarized, and the summary is carried forward in its place. That helps, but it is still a chalkboard. Something decided what got erased and what got rewritten in shorthand, and the model works from what is left.

## Memory Features Are Context Too

Saved memories, project files, and custom instructions feel like the assistant knowing you. Mechanically, they are inputs placed back into context before your request.

That makes them useful for continuity. It also means they can carry stale preferences, outdated facts, or details from unrelated work into a task where they don’t belong. Treat memory like any other input: review what has been saved, scope it to the project where it applies, and clear what no longer matters.

## Looping Costs Time and Money

When you use looping processes to refine outputs, surrounding systems often have to resend or reconstruct context repeatedly. That means:

- **Higher token usage**  
- **Slower interactions**  
- **Possible drift in tone or interpretation**

If not carefully managed, your system can loop in ways that reprocess the same context unnecessarily—burning budget and patience.

Prompt caching can make repeated context cheaper. It does not make it more relevant. Stale material carries forward just as easily when it is discounted.

## Mitigating the Limits

There are ways to design around these constraints:

- **Segmented tasks**: Break down work into smaller, less memory-intensive prompts.
- **State summaries**: Pass forward only essential summaries instead of the full interaction history.
- **Chained reasoning**: Use tools or humans to gather outputs and feed them forward intelligently.
- **External memory**: Store long-term context in structured notes or databases, and pull from them only what’s needed.

Think like a playwright, not a stenographer—a useful metaphor for shaping context deliberately rather than exhaustively. Don’t try to capture the whole play in one act.

## When It’s a Feature

These limits aren’t just a flaw—they create boundaries that encourage clarity. Knowing that context must be reintroduced or refreshed encourages writing with more intention. You scaffold the task step by step, using structure to compensate for limited context.

In the same way that Twitter’s old 140-character limit led to punchier writing, context limits can lead to smarter prompting.

## Summary

Your minion’s “memory” is not a mind. It is whatever the system chooses to put back in front of the model.

Design with that in mind. Keep loops efficient, prompts focused, and history externalized. The more you respect the boundaries of context and design around them, the more effective these tools become in practice.
