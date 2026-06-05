# Architecture Example

## Situation

A product needs background processing for long-running report generation.

## Prompt

```text
Use first-principles architecture thinking before proposing an implementation.

Problem: users need reports that can take 30-90 seconds to generate.
Goal: avoid request timeouts and provide reliable report status.
Constraints: small team, existing relational database, low traffic today, unknown future scale.

Compare at least three options, including the simplest viable design. Do not introduce a queue or new service unless the constraints justify it.
```

## Expected Agent Behavior

The agent should compare options such as:

- Synchronous generation with increased timeout.
- Database-backed job table processed by the existing app.
- External queue and worker service.

It should evaluate reliability, operational cost, reversibility, implementation effort, and verification before recommending a path.

## Bad Outcome To Avoid

```text
Use Kafka, workers, Redis, and a new reporting microservice.
```

That may be valid at high scale, but it is not derived from the stated constraints.
