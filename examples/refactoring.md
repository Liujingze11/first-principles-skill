# Refactoring Example

## Situation

A single service file has become hard to maintain. The team wants to split it up.

## Prompt

```text
Use first-principles refactoring before changing files.

Current pain: checkout_service is large and hard to modify.
Goal: make future checkout changes safer without changing behavior.

Identify the real source of complexity first. Is it mixed responsibilities, duplicated policy, implicit state, poor boundaries, or missing tests?
Do not refactor for aesthetics. Recommend the smallest behavior-preserving plan with verification and rollback.
```

## Expected Agent Behavior

The agent should:

- Inspect call sites and tests.
- Identify responsibilities and change hotspots.
- Add or identify characterization tests before risky movement.
- Prefer small extractions around stable concepts.
- Avoid broad rewrites.

## Bad Outcome To Avoid

```text
Split the file into repositories, managers, handlers, helpers, and utils.
```

More files do not automatically reduce complexity.
