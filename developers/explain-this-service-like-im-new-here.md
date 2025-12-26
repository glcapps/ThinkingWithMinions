# Explain This Service Like I’m New Here

When someone joins a team—whether they’re an engineer, a contractor, or a new collaborator—the most disorienting question they face is: *What is this service and why does it exist?*

Let’s fix that.

## Describe the “Why” Before the “How”

Most documentation dives into endpoints, data formats, and config knobs. But newcomers first need context.

Start by answering:

- What problem does this service solve?
- Who uses it and how often?
- What would break if it disappeared?

This orientation makes every other detail more meaningful.

## Create an “Explain Like I’m New” Snapshot

A useful practice is to include a short, top-level overview section in your README or service documentation—something a new reader can absorb in under a minute.

Include:

- **Purpose:** One-sentence mission
- **Audience:** Internal? External? Which teams rely on it?
- **Inputs:** Where does data come from?
- **Outputs:** What does it affect or emit?
- **Lifecycle:** Is this always on? Event-based? Batch?

## Add a 30-second summary

A short, plain-language summary helps others explain the service accurately without rereading the full documentation.

> The Email Notification Service receives event payloads from the orders system, formats them using templates, and sends messages through SES. It supports post-purchase communication and retry handling for delivery failures.

This makes it easier for others to discuss the service in standups, support conversations, or code reviews without misrepresenting its role.

## Bonus: Document the “Gotchas”

Add a short section for footguns, legacy assumptions, or upstream quirks.

> ⚠️ Legacy alert: The system retries failed sends every 6 hours. This can lead to bursts of duplicate emails. There’s a fix planned in Q4.

## Don’t Just Explain the API. Explain the Idea.

Remember: your new team member is trying to *think in system-shaped concepts*, not memorize endpoints.

A clear “new here” summary saves time for everyone and reduces misunderstandings as systems evolve.
