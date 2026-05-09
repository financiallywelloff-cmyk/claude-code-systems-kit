# Example: Content System Decision

Goal: turn one weekly long-form video into distribution assets without manually rebuilding the same process every week.

## Owners

| Step | Owner |
| --- | --- |
| Pull transcript | Local script or OpenClaw |
| Score search fit | Claude Code |
| Refresh existing site page | Claude Code |
| Generate short-form ideas | Claude Code or OpenClaw |
| Route approved assets | n8n |
| Publish | Human approval first |

## Why

Claude Code is better for reading the repo, editing pages, and running checks.

n8n is better for moving approved assets to Notion, Slack, email, or a publishing queue.

OpenClaw is useful when the job can run locally and write a reviewable output file.

