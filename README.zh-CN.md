# First Principles Skill

[English](README.md)

一个面向 vibe coding agents 的第一性原理思考工具包，帮助 Claude Code、Codex、Cursor、Windsurf 和其他 AI 编程工具在写代码前先从底层原则推理。

## 这是什么

First Principles Skill 是一个轻量级开源 prompt 工具包，面向各类 AI coding agents。它提供可复用的 prompts、项目指令和集成示例，帮助 AI 编程工具在修改代码前先从基本事实和约束出发进行推理。

当你希望 agent 先慢下来、澄清真正问题、区分事实和假设、比较多个方案，并选择小而可靠、可逆、可验证的路径时，可以使用它。

没有框架。没有依赖。没有构建步骤。只有可以复制到现有 AI 编程工具里的 prompts 和项目指令。

## 为什么 Vibe Coding 需要 First Principles

Vibe coding 很快，但速度也会放大浅层推理的问题。Agents 经常从表面需求直接跳到实现，而没有先判断这个需求是否描述了真正的问题。

第一性原理思考会加入一个有纪律的停顿：

- 拆解问题。
- 区分已知事实和假设。
- 识别约束和根因。
- 从底层原则推导选项。
- 选择最小、可验证的实现路径。
- 明确风险和回滚方式。

目标不是让 AI 编程变慢，而是让它更少随机发挥、更少过度设计，也更容易被信任。

## 它解决什么问题

- Agents 只修表面症状，而不是根因。
- 架构决策被流行趋势驱动，而不是被约束驱动。
- 重构只是移动代码，并没有降低复杂度。
- 产品需求变成功能堆叠。
- 技术选型在权衡明确之前就被决定。
- 大改动难以测试，也难以回滚。

可以把它理解为日常软件工作的 rocket-engineer thinking：从基本原理搭建，reason before code，verify before confidence。

## 支持哪些工具

这个工具包适用于任何支持自定义指令、项目规则、skills 或 prompt 模板的 vibe coding / AI coding agent，包括：

- Claude Code
- Codex
- Cursor
- Windsurf
- Aider
- Cline
- Gemini CLI
- 其他聊天式或编辑器内的 AI 编程工具

只要你的工具能接受 prompt，就可以使用这个工具包。

## 快速开始

1. 将 [`prompts/first-principles.md`](prompts/first-principles.md) 复制到你的 agent 自定义指令、项目规则或系统 prompt 区域。
2. 如果是特定场景，可以从 [`prompts/`](prompts/) 复制对应的场景 prompt。
3. 要求 agent 在改代码前使用第一性原理推理：

```text
Use first-principles thinking before implementing this. Identify facts, assumptions, constraints, root cause, options, tradeoffs, verification, risks, and rollback.
```

## 通用使用方式

当任务较宽泛或包含多个方面时，使用通用 prompt：

- 调试生产问题。
- 设计新的服务边界。
- 判断是否要引入某个库。
- 规划一次重构。
- 评估一个产品功能。
- 在多个实现路径之间做选择。

当工作有明确场景时，使用场景 prompt：

- [`first-principles-debugging.md`](prompts/first-principles-debugging.md)
- [`first-principles-architecture.md`](prompts/first-principles-architecture.md)
- [`first-principles-refactoring.md`](prompts/first-principles-refactoring.md)
- [`first-principles-product.md`](prompts/first-principles-product.md)

## Claude Code 使用方式

Claude Code 用户可以复制示例 skill：

```text
integrations/claude-code/.claude/skills/first-principles/SKILL.md
```

如果你的项目使用 Claude Code skills，可以放到项目中的 `.claude/skills/first-principles/SKILL.md` 路径。

如果你的 Claude Code 工作流不使用 skills，可以将 prompt 内容复制到项目指令或自定义指令中。

## Codex 使用方式

Codex 用户可以复制或合并：

```text
integrations/codex/AGENTS.md
```

到目标仓库的 `AGENTS.md`。

它可以作为项目级指导，告诉 Codex 在调试、架构设计、重构、技术决策和实现规划中如何先进行第一性原理分析。

## Cursor 使用方式

Cursor 用户可以复制：

```text
integrations/cursor/cursor-rules.md
```

到 Cursor Rules 或项目指令中。把它当作规则集，而不是命令。

## Windsurf 使用方式

Windsurf 用户可以复制：

```text
integrations/windsurf/windsurf-rules.md
```

到 Windsurf rules、自定义指令或项目指令中。

## 示例 Prompts

查看 [`examples/`](examples/) 中的实践示例：

- [`debugging.md`](examples/debugging.md)
- [`architecture.md`](examples/architecture.md)
- [`refactoring.md`](examples/refactoring.md)
- [`technical-decision.md`](examples/technical-decision.md)
- [`product-thinking.md`](examples/product-thinking.md)

## 适用场景

当任务存在不确定性、风险或多条可能路径时，First Principles Skill 特别有用：

- 根因调试
- 架构设计
- 重构策略
- 技术选型
- 产品与范围决策
- 性能优化
- 可靠性改进
- 安全敏感变更
- 迁移规划

对于非常小且明确的改动，分析可以很短。重点是有纪律地推理，而不是形式主义。

## 文件结构

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

## 安全与隐私

这个仓库只包含文本 prompts 和文档。它不需要 API keys、遥测、包安装或网络访问。

贡献时请不要提交：

- API keys、tokens、cookies 或凭据。
- 私有 SSH keys 或本地证书。
- 本地绝对路径或机器相关配置。
- IDE 缓存、日志、临时文件或生成的二进制文件。
- 从私有代码库复制出来的项目细节。

## 贡献指南

欢迎贡献。请保持这个工具包轻量、工具中立、可实践。

提交 pull request 前请确认：

- Prompts 清晰且可复用。
- 不确定的平台行为不要写成确定事实。
- 除非有充分理由，不要添加依赖。
- 添加新工作流时尽量包含示例。
- 快速扫描 secrets 和本地机器信息。

更多信息见 [`CONTRIBUTING.md`](CONTRIBUTING.md)。

## License

MIT License。见 [`LICENSE`](LICENSE)。
