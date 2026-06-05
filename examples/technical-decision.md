# Technical Decision Example

## Situation

A team is deciding whether to add a vector database for semantic search.

## Prompt

```text
Use first-principles technical decision making.

Problem: users need better document search.
Proposed solution: add a vector database.
Known facts: current keyword search misses synonyms; data set is small; team already uses Postgres.
Goal: improve search quality with the least operational burden.

Do not choose a vector database just because it is popular. Compare options from fundamentals, including improving existing search, using Postgres extensions, or adding dedicated infrastructure.
```

## Expected Agent Behavior

The agent should compare:

- Better query normalization or ranking in the existing search.
- Postgres-based full-text or vector extension.
- Dedicated vector database.

It should consider quality, cost, operational complexity, migration, reversibility, and measurable search improvement.

## Bad Outcome To Avoid

```text
Install the newest vector database and migrate all documents.
```

That starts with a tool instead of the search problem.
