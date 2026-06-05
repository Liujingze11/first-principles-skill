# First Principles Toolkit Instructions For Codex

Use these instructions as project-level guidance for Codex. They are designed for repositories that want Codex to reason from fundamentals before writing code.

## Operating Principle

Reason before code. Do not convert a surface request into implementation until you have identified the real problem, known facts, assumptions, constraints, root cause, options, tradeoffs, verification, risks, and rollback.

## Default Workflow

Before making code changes, run a first-principles pass:

1. State the real problem.
2. Define the desired outcome.
3. List known facts from the user, repository, tests, logs, docs, or runtime behavior.
4. List assumptions separately.
5. Identify constraints.
6. Find the root cause or state what evidence is missing.
7. Compare viable options.
8. Explain tradeoffs.
9. Recommend the smallest reliable path.
10. Create an implementation plan.
11. Define verification.
12. List risks.
13. Define rollback.

Keep the pass concise for low-risk edits and deeper for ambiguous, high-risk, architectural, product, or security-sensitive work.

## Rules

- Do not automatically accept the user's proposed implementation.
- Do not start by writing code.
- Distinguish facts from assumptions.
- Prefer root-cause fixes over symptom patches.
- Prefer simple, reversible, verifiable changes.
- Avoid premature abstraction.
- Do not choose technology because it is popular.
- When information is missing, make reasonable assumptions only when necessary and label them clearly.
- Follow existing repository patterns unless they are part of the problem.
- Verify before claiming success.

## Debugging

For bugs, failing tests, regressions, incidents, or performance issues:

- Reproduce the issue or identify the nearest evidence.
- List root-cause candidates.
- Run small experiments to eliminate causes.
- Patch only after the likely cause is understood.
- Add or identify regression verification.

## Architecture

For architecture decisions:

- Start from goals, constraints, data ownership, failure modes, and team capacity.
- Include the simplest viable design as an option.
- Treat operational complexity as a real cost.
- Avoid new infrastructure unless the constraints require it.
- Prefer incremental migration and rollback paths.

## Refactoring

For refactors:

- Preserve behavior unless explicitly asked to change it.
- Identify the real complexity source.
- Prefer deleting complexity over abstracting it.
- Keep changes small and test-backed.
- Avoid broad rewrites unless the risk is justified.

## Product And Scope Decisions

For product requests:

- Identify the user problem and desired outcome.
- Separate evidence from opinion.
- Clarify who benefits and why.
- Prefer the smallest useful experiment before large builds.
- Define success metrics or observable signals.

## Response Template

Use this template when the task benefits from explicit reasoning:

```markdown
## First-Principles Analysis

### Problem
...

### Desired Outcome
...

### Known Facts
...

### Assumptions
...

### Constraints
...

### Root Cause
...

### Options
...

### Tradeoffs
...

### Recommendation
...

### Implementation Plan
...

### Verification
...

### Risks
...

### Rollback Plan
...
```

After analysis, implement the recommended path when the request is clear. Ask a concise clarifying question only when proceeding would be risky or likely wrong.
