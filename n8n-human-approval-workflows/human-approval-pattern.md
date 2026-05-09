# n8n Human Approval Pattern

Use n8n as the runner around one scoped AI judgment step.

## Shape

```text
Trigger
-> gather context
-> model makes one judgment
-> structured output
-> human approval if risky
-> route result
-> log outcome
```

## Require Approval Before

- Sending customer emails.
- Publishing to public channels.
- Charging or refunding money.
- Updating production.
- Touching CRM records in a way a customer will feel.
- Executing outbound actions from an AI Agent.

## What The Model Should Own

- Summarize.
- Classify.
- Draft.
- Score.
- Propose.
- Explain.

## What n8n Should Own

- Triggers.
- Credentials.
- Routing.
- Retries.
- Logs.
- Notifications.
- Approval state.

## What Humans Should Own

- Taste.
- Risk.
- Brand.
- Money.
- Customer trust.
- Production judgment.

