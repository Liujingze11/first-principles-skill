# Philosophy

First-principles thinking means reasoning upward from fundamentals instead of copying patterns, trends, or surface-level requests.

The idea has been popularized by builders and engineers because it is useful in uncertain domains: when the obvious answer may be inherited habit, local convention, or incomplete framing.

## Why This Matters For AI Coding

AI coding agents are good at executing instructions. That strength creates a risk: if the instruction is shallow, the implementation can be shallow too.

A user might say:

```text
Add Redis caching here.
```

But the real problem might be:

- A slow query.
- Missing pagination.
- Repeated work in one request.
- A bad index.
- A product flow that asks for too much data.
- A transient dependency failure.

First-principles reasoning asks the agent to pause before accepting the proposed solution.

## Core Beliefs

### Reason Before Code

Implementation should follow understanding. The agent should know what problem it is solving and why the chosen path fits.

### Facts Before Assumptions

Facts come from user context, source code, tests, logs, docs, and runtime behavior. Assumptions are useful, but they must be labeled.

### Root Cause Before Symptom

A symptom patch can be valid as a temporary mitigation. It should not be confused with a root-cause fix.

### Constraints Before Architecture

Architecture should emerge from constraints such as scale, consistency, latency, security, team size, cost, and operational capacity.

### Simplicity Before Abstraction

Abstractions are useful when they remove real complexity. They are harmful when they predict a future that may never arrive.

### Reversibility Before Commitment

When uncertainty is high, choose paths that can be tested, narrowed, disabled, or reverted.

### Verification Before Confidence

The agent should state how the work will be verified before claiming the work is correct.

## What This Toolkit Is Not

This is not a framework, dependency, or runtime.

It is not tied to one AI coding platform.

It is not a reason to make every tiny edit ceremonial.

It is a practical reasoning layer for moments where the cost of being wrong is higher than the cost of thinking clearly.
