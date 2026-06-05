# Debugging Example

## Situation

An API endpoint started returning intermittent `500` responses after a recent deployment.

## Prompt

```text
Use first-principles debugging before patching this.

Endpoint: POST /checkout
Symptom: intermittent 500 responses
Known signal: failures increased after the latest deployment
Goal: identify the root cause, choose the smallest safe fix, and define verification.

Do not patch the first visible error unless it is clearly the root cause.
Separate facts from assumptions, list root-cause candidates, propose experiments, then recommend a fix.
```

## Expected Agent Behavior

The agent should:

- Inspect logs, tests, recent changes, and relevant code paths.
- Separate verified facts from guesses.
- Identify candidate causes such as input validation, dependency timeout, schema mismatch, race condition, or deployment config.
- Run small checks to eliminate causes.
- Recommend a minimal root-cause fix.
- Define regression verification and rollback.

## Bad Outcome To Avoid

```text
The error mentions null, so I will add a null check everywhere.
```

This may hide the symptom without explaining why the null appeared.
