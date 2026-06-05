# First Principles Skill

[中文](README.zh-CN.md)

A first-principles thinking toolkit for vibe coding agents — helping Claude Code, Codex, Cursor, Windsurf, and other AI coding tools reason from fundamentals before writing code.

## What This Is

First Principles Skill is a lightweight open-source prompt toolkit for AI coding agents. It gives developers reusable prompts, project instructions, and integration examples that push coding tools to reason from fundamentals before they edit files.

Use it when you want an agent to slow down, clarify the real problem, separate facts from assumptions, compare options, and choose a small, reliable, reversible path.

No framework. No dependency. No build step. Just prompts and project instructions you can copy into the agent you already use.

## Why Vibe Coding Needs First Principles

Vibe coding is fast, but speed can amplify shallow reasoning. Agents often jump from a surface request to an implementation before checking whether the request describes the real problem.

First-principles thinking adds a disciplined pause:

- Break down the problem.
- Separate known facts from assumptions.
- Identify constraints and root causes.
- Derive options from fundamentals.
- Choose the smallest verifiable implementation.
- Keep rollback and risk visible.

The goal is not to make AI coding slower. The goal is to make it less random, less overbuilt, and easier to trust.

## Problems It Helps Solve

- Agents patching symptoms instead of root causes.
- Architecture decisions driven by trends instead of constraints.
- Refactors that move code around without reducing complexity.
- Product requests turning into feature piles.
- Technical choices made before tradeoffs are explicit.
- Large changes that are hard to test or roll back.

Think of it as rocket-engineer thinking for everyday software work: build from fundamentals, reason before code, verify before confidence.

## Supported Tools

This toolkit is designed for any vibe coding or AI coding agent that accepts custom instructions, project rules, skills, or prompt templates, including:

- Claude Code
- Codex
- Cursor
- Windsurf
- Aider
- Cline
- Gemini CLI
- Other chat-based or editor-integrated coding agents

If your tool can accept a prompt, it can use this toolkit.

## Quick Start

1. Copy [`prompts/first-principles.md`](prompts/first-principles.md) into your agent's custom instructions, project rules, or system prompt area.
2. For focused work, copy one of the scenario prompts from [`prompts/`](prompts/).
3. Ask your agent to use first-principles reasoning before changing code:

```text
Use first-principles thinking before implementing this. Identify facts, assumptions, constraints, root cause, options, tradeoffs, verification, risks, and rollback.
```

## Generic Usage

Use the universal prompt when the task is broad or mixed:

- Debugging a production issue.
- Designing a new service boundary.
- Deciding whether to adopt a library.
- Planning a refactor.
- Evaluating a product feature.
- Choosing between multiple implementation paths.

Use a scenario prompt when the work has a clear shape:

- [`first-principles-debugging.md`](prompts/first-principles-debugging.md)
- [`first-principles-architecture.md`](prompts/first-principles-architecture.md)
- [`first-principles-refactoring.md`](prompts/first-principles-refactoring.md)
- [`first-principles-product.md`](prompts/first-principles-product.md)

## Claude Code

Claude Code users can copy the example skill from:

```text
integrations/claude-code/.claude/skills/first-principles/SKILL.md
```

into a project's `.claude/skills/first-principles/SKILL.md` location if they use Claude Code skills.

If your Claude Code setup does not use skills, copy the prompt content into your project instructions or custom instructions instead.

## Codex

Codex users can copy or merge:

```text
integrations/codex/AGENTS.md
```

into the target repository's `AGENTS.md`.

Use it as project-level guidance for how Codex should approach debugging, architecture, refactoring, technical decisions, and implementation planning.

## Cursor

Cursor users can copy:

```text
integrations/cursor/cursor-rules.md
```

into Cursor Rules or project instructions. Treat it as a rule set, not as a command.

## Windsurf

Windsurf users can copy:

```text
integrations/windsurf/windsurf-rules.md
```

into Windsurf rules, custom instructions, or project instructions.

## Example Prompts

See [`examples/`](examples/) for practical examples:

- [`debugging.md`](examples/debugging.md)
- [`architecture.md`](examples/architecture.md)
- [`refactoring.md`](examples/refactoring.md)
- [`technical-decision.md`](examples/technical-decision.md)
- [`product-thinking.md`](examples/product-thinking.md)

## Best-Fit Scenarios

First Principles Skill is useful when the task has ambiguity, risk, or multiple possible paths:

- Root-cause debugging
- Architecture design
- Refactoring strategy
- Technical selection
- Product and scope decisions
- Performance work
- Reliability improvements
- Security-sensitive changes
- Migration planning

For tiny, obvious edits, keep the analysis brief. The point is disciplined reasoning, not ceremony.

## File Structure

```text
README.md
README.zh-CN.md
LICENSE
CHANGELOG.md
CONTRIBUTING.md
.gitignore
prompts/
  first-principles.md
  first-principles-debugging.md
  first-principles-architecture.md
  first-principles-refactoring.md
  first-principles-product.md
integrations/
  claude-code/
    .claude/skills/first-principles/SKILL.md
  codex/
    AGENTS.md
  cursor/
    cursor-rules.md
  windsurf/
    windsurf-rules.md
examples/
  debugging.md
  architecture.md
  refactoring.md
  technical-decision.md
  product-thinking.md
docs/
  installation.md
  usage.md
  philosophy.md
```

## Safety And Privacy

This repository contains only text prompts and documentation. It does not require API keys, telemetry, package installation, or network access.

When contributing, do not commit:

- API keys, tokens, cookies, or credentials.
- Private SSH keys or local certificates.
- Local absolute paths or machine-specific configuration.
- IDE caches, logs, temporary files, or generated binaries.
- Private project details copied from proprietary codebases.

## Contributing

Contributions are welcome. Please keep the toolkit lightweight, vendor-neutral, and practical.

Before opening a pull request:

- Keep prompts clear and reusable.
- Avoid platform-specific claims unless verified.
- Do not add dependencies unless there is a strong reason.
- Include examples when adding a new workflow.
- Run a quick scan for secrets and local machine details.

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for more.

## License

MIT License. See [`LICENSE`](LICENSE).
