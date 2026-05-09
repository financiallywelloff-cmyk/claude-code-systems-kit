# Claude Code Systems Kit

Practical systems for running a solo AI business with Claude Code, OpenClaw, and n8n.

This is not a prompt dump. It is a small operating kit for deciding which AI tool should own which part of a workflow:

- Claude Code for repo-aware building, editing, QA, and content systems.
- OpenClaw for local/background agent runs.
- n8n for triggers, routing, credentials, retries, logs, and approval gates.

The simple rule:

> Claude builds. OpenClaw runs locally. n8n routes. Human approves.

## What's Inside

| Folder | Use it for |
| --- | --- |
| `claude-skills-routines/` | Claude Code skills, routines, and keep/kill rules. |
| `openclaw-local-agents/` | Local agent runner patterns and background task ideas. |
| `n8n-human-approval-workflows/` | Human approval patterns for workflows that touch customers, money, publishing, or production. |
| `decision-matrix/` | When to use Claude Code, OpenClaw, n8n, scripts, or normal manual work. |
| `templates/` | Copyable markdown templates for audits, runbooks, and workflow specs. |
| `examples/` | Small examples you can adapt. |

## Start Here

1. Read the [AI workflow decision matrix](decision-matrix/ai-workflow-decision-matrix.md).
2. Pick one recurring task that eats time every week.
3. Write the workflow spec with [workflow-spec.md](templates/workflow-spec.md).
4. Add an approval gate before anything risky.
5. Only automate the boring middle after the edges are clear.

## Related Guides

- [n8n AI agent workflow pattern](https://christopheralarcon.com/workflows/n8n-ai-agent-workflow)
- [Claude Code vs n8n for solo builders](https://christopheralarcon.com/blog/claude-code-vs-n8n-for-solo-builders)
- [n8n AI agent workflow builder](https://christopheralarcon.com/tools/n8n-ai-agent-workflow-builder)

## Who This Is For

Solo builders, creators, and operators who have 5-15 hours a week and want systems that save time without turning their business into a pile of fragile automations.

If you are still manually doing the same task every week, start here.

