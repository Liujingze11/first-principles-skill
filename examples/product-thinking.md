# Product Thinking Example

## Situation

Users ask for a dashboard with more charts.

## Prompt

```text
Use first-principles product thinking before proposing features.

Request: users want more dashboard charts.
Goal: understand the underlying user problem and identify the smallest useful product change.

Separate user evidence from assumptions. Identify who needs this, what decision they are trying to make, what data they trust, and how success will be measured.
Do not turn this into a chart backlog by default.
```

## Expected Agent Behavior

The agent should ask:

- Which users asked?
- What decision are they trying to make?
- What is missing from the current workflow?
- Would better defaults, alerts, exports, or explanations solve the problem better than more charts?
- What signal would prove the change helped?

## Bad Outcome To Avoid

```text
Add five new chart types and filters.
```

More visualizations can increase cognitive load without solving the user problem.
