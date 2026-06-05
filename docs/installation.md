# Installation

First Principles Skill does not require package installation. It is a collection of Markdown prompts and agent instruction files.

## Generic Installation

1. Open [`prompts/first-principles.md`](../prompts/first-principles.md).
2. Copy the prompt into your AI coding agent's custom instructions, project rules, or reusable prompt library.
3. Optionally copy one or more scenario prompts from [`prompts/`](../prompts/).
4. Ask the agent to use first-principles reasoning before implementation.

## Claude Code

If your Claude Code workflow uses skills, copy:

```text
integrations/claude-code/.claude/skills/first-principles/SKILL.md
```

into the matching `.claude/skills/first-principles/SKILL.md` path in your project.

If your setup does not use skills, copy the content into project instructions or custom instructions instead.

## Codex

Copy or merge:

```text
integrations/codex/AGENTS.md
```

into your repository's `AGENTS.md`.

If your repository already has an `AGENTS.md`, merge the first-principles sections into the existing file so they do not override important project-specific instructions.

## Cursor

Copy:

```text
integrations/cursor/cursor-rules.md
```

into Cursor Rules or project instructions.

## Windsurf

Copy:

```text
integrations/windsurf/windsurf-rules.md
```

into Windsurf rules, custom instructions, or project instructions.

## Other Agents

For Aider, Cline, Gemini CLI, and other tools, copy the universal prompt into whichever place your tool uses for persistent instructions or reusable prompts.

If the tool has no persistent instruction mechanism, paste the prompt at the start of a task.
