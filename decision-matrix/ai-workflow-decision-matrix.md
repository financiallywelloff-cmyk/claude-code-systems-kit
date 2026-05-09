# AI Workflow Decision Matrix

Use this when you are deciding where a task should live.

| Job | Best owner | Why |
| --- | --- | --- |
| Edit files in a repo | Claude Code | It can read context, change files, run checks, and inspect diffs. |
| Build or refresh a website page | Claude Code | The work is repo-aware and needs QA. |
| Run a local/background agent task | OpenClaw | Good for repeatable local jobs that do not need a visual workflow canvas. |
| Trigger from forms, schedules, webhooks, or apps | n8n | It owns credentials, triggers, retries, logs, and routing. |
| Move data between apps | n8n | This is workflow plumbing. |
| Call an LLM for one judgment step | n8n or Claude Code | Use n8n inside a running workflow. Use Claude Code when the output needs repo context. |
| Generate workflow JSON | Claude Code | Draft the JSON, then inspect before creating the live workflow. |
| Send customer email, publish, charge, deploy, or update production | Human approval first | The model can draft. It should not quietly execute risky actions. |

## The Rule

If the work needs context and judgment, use Claude Code.

If the work needs to run on a trigger, use n8n.

If the work needs to run locally in the background, use OpenClaw.

If the work can embarrass you, cost money, touch customers, or change production, add approval.

## Common Mistakes

### Mistake 1: Making n8n do builder work

n8n can call models, but it is not the cleanest place to write, edit, test, and review project files.

### Mistake 2: Making Claude Code run the whole business

Claude Code is good at building systems. n8n is better at running durable triggers, credentials, and retries.

### Mistake 3: Turning every step into an agent

Most workflow steps should be boring. Use an agent only where judgment is actually needed.

