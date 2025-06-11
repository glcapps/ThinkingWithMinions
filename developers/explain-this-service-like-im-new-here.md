# Explain This Service Like I’m New Here

When someone joins your team—whether they’re an engineer, a contractor, or even an LLM—the most disorienting question they face is: *What is this service and why does it exist?*

Let’s fix that.

## Describe the “Why” Before the “How”

Most documentation dives into endpoints, data formats, and config knobs. But newcomers—and assistants—first need context.

Start by answering:

- What problem does this service solve?
- Who uses it and how often?
- What would break if it disappeared?

This orientation makes every other detail more meaningful.

## Create an “Explain Like I’m New” Snapshot

We recommend a top-level section in your README or docs called “Service Overview (ELINH)”—Explain Like I’m New Here.

Include:

- **Purpose:** One-sentence mission
- **Audience:** Internal? External? Which teams rely on it?
- **Inputs:** Where does data come from?
- **Outputs:** What does it affect or emit?
- **Lifecycle:** Is this always on? Event-based? Batch?

## Add a 30-second Prompt Summary

For LLM integrations, include a plaintext prompt like:

> You are a helpful assistant learning about the Email Notification Service. It receives event payloads from the orders system, formats them with templates, and sends them via SES. It’s critical for post-purchase user communication.

Now your assistant can speak about this system in team standups, support chats, or code reviews.

## Bonus: Document the “Gotchas”

Add a short section for footguns, legacy assumptions, or upstream quirks.

> ⚠️ Legacy alert: The system retries failed sends every 6 hours. This can lead to bursts of duplicate emails. There’s a fix planned in Q4.

## Don’t Just Explain the API. Explain the Idea.

Remember: your new team member is trying to *think in system-shaped concepts*, not memorize endpoints.

A great ELINH summary saves time for everyone—and trains both people and minions faster.
