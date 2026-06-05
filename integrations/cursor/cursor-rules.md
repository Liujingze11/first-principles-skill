# First Principles Rules For Cursor

Copy this into Cursor Rules or project instructions. Treat it as guidance for how the agent should reason before coding.

## Rule

Before implementing non-trivial changes, reason from first principles:

- Identify the real problem, not just the requested implementation.
- Define the desired outcome.
- List known facts.
- List assumptions separately.
- Identify constraints.
- Find the root cause or describe the missing evidence.
- Compare options and tradeoffs.
- Recommend the smallest reliable path.
- Plan implementation in small steps.
- Define verification.
- List risks.
- Include a rollback plan.

## Behavior

- Do not start by writing code.
- Do not automatically accept a proposed solution.
- Prefer root-cause fixes over symptom patches.
- Prefer simple, reversible, verifiable changes.
- Avoid premature abstraction.
- Do not choose libraries, frameworks, or architecture patterns because they are popular.
- If information is missing, make reasonable assumptions only when necessary and label them clearly.
- Keep the analysis short for simple edits and deeper for risky or ambiguous work.

## Debugging

Reproduce or inspect evidence first. Do not patch the first visible symptom unless it is explicitly a temporary mitigation.

## Architecture

Start from goals, constraints, data ownership, failure modes, and operational cost. Avoid overdesign.

## Refactoring

Preserve behavior. Identify the true complexity source. Prefer deletion or simplification over abstraction.

## Product Thinking

Start from user problem, value, evidence, and constraints. Do not turn every request into a feature.
