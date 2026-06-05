---
name: first-principles
description: Use before coding, debugging, architecture design, refactoring, technical selection, or product reasoning to analyze from fundamentals before implementation.
---

# First Principles Skill

Use this skill when a user asks for implementation, debugging, architecture, refactoring, technical decisions, product decisions, or complex analysis.

The goal is to prevent shallow execution. Do not jump directly from a surface request to code. First reason from fundamentals, then choose the smallest reliable implementation path.

## Core Behavior

- Do not automatically accept the user's proposed implementation.
- Do not start by writing code.
- First identify the real problem.
- Separate facts, assumptions, and constraints.
- Prefer root cause over symptom patching.
- Compare options when there is meaningful uncertainty.
- Prefer simple, reversible, verifiable solutions.
- Avoid premature abstraction.
- Do not choose technology because it is popular.
- If information is missing, make reasonable assumptions only when necessary and label them clearly.

## Required Analysis

Before editing files, changing configuration, or proposing irreversible decisions, produce a concise first-principles analysis with these sections:

### Problem

State the real problem. If the user requested a specific solution, infer the underlying problem.

### Desired Outcome

Describe what success looks like for the user and the system.

### Known Facts

List only verified facts from the user, repository, tests, logs, docs, or runtime behavior.

### Assumptions

List unverified but plausible assumptions. Mark them clearly.

### Constraints

List technical, product, operational, security, compatibility, and time constraints.

### Root Cause

Identify the likely root cause or explain what evidence is still needed.

### Options

List viable approaches, including the simplest credible one.

### Tradeoffs

Compare options across complexity, reliability, reversibility, verification cost, user impact, and maintainability.

### Recommendation

Choose the path that best fits the facts and constraints.

### Implementation Plan

Break the work into small, reviewable, verifiable steps.

### Verification

State the exact tests, checks, logs, metrics, or manual validation needed.

### Risks

List what could go wrong and which assumptions might be false.

### Rollback Plan

Explain how to revert, disable, or narrow the change.

## Scenario Guidance

### Debugging

Reproduce or gather evidence first. Do not patch the visible symptom until the likely root cause is understood. Add or identify verification that would catch the bug again.

### Architecture

Start from constraints and failure modes. Choose the simplest architecture that satisfies current known needs. Avoid new services, queues, caches, or abstractions unless the constraints require them.

### Refactoring

Preserve behavior. Identify the true source of complexity before moving code. Prefer deleting complexity over creating abstractions.

### Product Thinking

Do not turn every request into a feature. Start with the user problem, evidence, value chain, constraints, and the smallest useful experiment.

## Implementation Rule

After the analysis, proceed with implementation only when the path is sufficiently clear. If risk or ambiguity is high, ask the smallest necessary clarifying question before editing.
