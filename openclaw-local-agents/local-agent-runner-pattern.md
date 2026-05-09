# OpenClaw Local Agent Runner Pattern

Use OpenClaw when a task should run locally or in the background without turning it into a full app.

Good fits:

- Weekly content scans.
- Local file audits.
- Draft generation from known folders.
- Background research queues.
- Report generation.
- Repeatable checks that write markdown or JSON outputs.

Bad fits:

- Anything requiring direct customer action with no review.
- Payments or production changes.
- Tasks where the input source is unclear.
- Agents that need broad permission to do "whatever seems useful."

## Pattern

1. Give the agent one folder or one queue.
2. Make it write a reviewable file.
3. Include timestamps and source paths.
4. Never let it silently publish.
5. Review the output before routing it to n8n, GitHub, or the website.

