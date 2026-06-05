# Usage

First Principles Skill works best when the task is ambiguous, risky, or likely to produce multiple possible implementations.

## Basic Pattern

Use this instruction before asking for code:

```text
Use first-principles thinking before implementing. Separate facts from assumptions, identify constraints and root cause, compare options, recommend the smallest verifiable path, and include verification plus rollback.
```

## When To Use The Universal Prompt

Use [`prompts/first-principles.md`](../prompts/first-principles.md) when the task combines multiple concerns or does not fit a single scenario.

Examples:

- "Improve onboarding performance."
- "Decide whether this should be a service."
- "Fix this flaky behavior."
- "Plan a migration."
- "Evaluate this feature request."

## When To Use Scenario Prompts

Use a focused prompt when the work has a clear frame:

- Debugging: [`first-principles-debugging.md`](../prompts/first-principles-debugging.md)
- Architecture: [`first-principles-architecture.md`](../prompts/first-principles-architecture.md)
- Refactoring: [`first-principles-refactoring.md`](../prompts/first-principles-refactoring.md)
- Product thinking: [`first-principles-product.md`](../prompts/first-principles-product.md)

## How Much Analysis Is Enough?

For tiny edits, the analysis can be short:

```text
Facts: button label is misspelled.
Assumption: no behavior change needed.
Plan: update label and run UI snapshot or manual check.
Rollback: revert the text change.
```

For broad or risky work, require the full structure:

- Problem
- Desired outcome
- Known facts
- Assumptions
- Constraints
- Root cause
- Options
- Tradeoffs
- Recommendation
- Implementation plan
- Verification
- Risks
- Rollback plan

## Combining With Agent Workflows

First-principles thinking does not replace tests, code review, or project conventions. It should sit before those steps:

1. Reason from fundamentals.
2. Pick the smallest reliable path.
3. Implement.
4. Verify.
5. Review.
6. Roll back or iterate if evidence says the path was wrong.

## Common Failure Modes

Avoid these patterns:

- Starting with a library choice before stating constraints.
- Refactoring before identifying the true complexity source.
- Adding architecture because the future might need it.
- Fixing the first error message without reproducing the issue.
- Building the requested feature before understanding the user problem.
