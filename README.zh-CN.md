<div align="center">
  <img src="assets/hero.svg" alt="First Principles Skill" width="100%">

  <h1>First Principles Skill</h1>

  <p>
    <strong>面向 vibe coding agents 的第一性原理思考工具包。</strong>
    <br>
    让 Claude Code、Codex、Cursor、Windsurf、Aider、Cline、Gemini CLI 和其他 AI 编程工具在写代码前先从底层原则推理。
  </p>

  <p>
    <a href="README.md">English</a>
    ·
    <a href="docs/installation.md">Installation</a>
    ·
    <a href="docs/usage.md">Usage</a>
    ·
    <a href="docs/philosophy.md">Philosophy</a>
  </p>

  <p>
    <img alt="Vibe Coding" src="https://img.shields.io/badge/Vibe%20Coding-ready-8B5CF6?style=for-the-badge">
    <img alt="AI Agents" src="https://img.shields.io/badge/AI%20Agents-compatible-06B6D4?style=for-the-badge">
    <img alt="Markdown Only" src="https://img.shields.io/badge/Markdown-only-10B981?style=for-the-badge">
    <img alt="License MIT" src="https://img.shields.io/badge/License-MIT-111827?style=for-the-badge">
  </p>
</div>

## 一句话

Vibe coding 是新的编程界面，first-principles thinking 是安全护栏。

AI 编程 agent 可以非常快，但没有推理的速度，经常会变成脆弱代码、无意义抽象、跟风架构，以及只遮住症状的补丁。

First Principles Skill 给你的 agent 加上一段轻量推理仪式：

```text
不要只是照着需求写代码。
先找到真正问题。
区分事实和假设。
识别约束和根因。
比较多个选择。
选择最小、可验证的路径。
然后再实现。
```

保留 vibe，也保留工程质量。

## 认识 Prism

<p align="center">
  <img src="assets/prism-mascot.svg" alt="Prism，第一性原理编程伙伴" width="560">
</p>

Prism 是这个项目的原创吉祥物：一个小小的第一性原理工程师，把模糊需求拆成 facts、assumptions、constraints、root causes、options 和 verified code。

它的作用是让这个工具包更有记忆点。当你的 agent 开始急着写实现时，Prism 就是在提醒它：先把光束拆开，再写补丁。

Prism 和仓库内视觉资产都是为这个项目原创绘制的 SVG，没有使用外部图库、品牌标识、名人肖像或已有角色 IP。

## 这是什么

First Principles Skill 是一个轻量级开源 prompt 工具包，面向各类 AI coding agents。

它提供可复用的 prompts、项目指令和集成示例，让 coding agents 在修改文件前先进行推理。

没有框架。没有依赖。没有构建步骤。只有可以复制到现有 AI 编程工具中的 Markdown prompts。

## 为什么需要它

AI 编程工具很擅长执行，这也是风险所在。

如果你提出的是错误问题，很多 agents 会很自信地把错误方案实现出来。这个工具包帮助 agent 先停一下，问清楚：

- 真正的问题是什么？
- 哪些信息是确定事实？
- 哪些只是我们的假设？
- 这是根因，还是表面症状？
- 哪个方案最简单、可逆、可测试？
- 如何验证改动有效？
- 如果出问题，如何回滚？

## 它如何工作

<p align="center">
  <img src="assets/reasoning-loop.svg" alt="第一性原理推理流程" width="100%">
</p>

这个工具包会把“直接实现这个需求”变成一个小型推理闭环：

| 步骤 | Agent 应该问什么 | 为什么重要 |
| --- | --- | --- |
| Problem | 需求背后真正的问题是什么？ | 避免盲目接受表面方案。 |
| Facts | 从代码、日志、测试、文档或用户那里确认了什么？ | 让推理有依据。 |
| Assumptions | 哪些只是猜测？ | 让不确定性显性化。 |
| Root Cause | 为什么会发生？ | 避免只修症状。 |
| Options | 有哪些可行路径？ | 避免一次性拍脑袋实现。 |
| Implementation | 最小可靠步骤是什么？ | 降低改动半径。 |
| Verification | 如何证明它有效？ | 用证据替代自信。 |
| Rollback | 如何撤回？ | 让高风险改动保持可逆。 |

## 快速开始

把下面这段复制到你的 coding agent：

```text
Use first-principles thinking before implementing this.

Identify:
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

Do not default to accepting my proposed implementation.
Do not start by writing code.
Prefer the smallest reversible and verifiable solution.
```

或者使用完整通用 prompt：

```text
prompts/first-principles.md
```

## Prompt 套件

| Prompt | 适合场景 | 核心偏向 |
| --- | --- | --- |
| [`first-principles.md`](prompts/first-principles.md) | 实现前的通用推理 | Reason before code |
| [`first-principles-debugging.md`](prompts/first-principles-debugging.md) | Bug、回归、事故、失败测试 | 先找根因，再打补丁 |
| [`first-principles-architecture.md`](prompts/first-principles-architecture.md) | 系统设计、API、服务、迁移 | 先看约束，再谈架构 |
| [`first-principles-refactoring.md`](prompts/first-principles-refactoring.md) | 清理代码、边界调整、技术债 | 先找复杂度来源，再重构 |
| [`first-principles-product.md`](prompts/first-principles-product.md) | 产品范围、功能需求、路线判断 | 先看用户问题，再堆功能 |

## Agent 集成

| 工具 | 集成文件 | 使用方式 |
| --- | --- | --- |
| Claude Code | [`integrations/claude-code/.claude/skills/first-principles/SKILL.md`](integrations/claude-code/.claude/skills/first-principles/SKILL.md) | 如果你的工作流使用 Claude Code skills，可以复制到 skill 路径；否则复制到项目指令。 |
| Codex | [`integrations/codex/AGENTS.md`](integrations/codex/AGENTS.md) | 合并到仓库的 `AGENTS.md`。 |
| Cursor | [`integrations/cursor/cursor-rules.md`](integrations/cursor/cursor-rules.md) | 复制到 Cursor Rules 或项目指令。 |
| Windsurf | [`integrations/windsurf/windsurf-rules.md`](integrations/windsurf/windsurf-rules.md) | 复制到 Windsurf rules、自定义指令或项目指令。 |
| Aider、Cline、Gemini CLI、其他工具 | [`prompts/first-principles.md`](prompts/first-principles.md) | 粘贴到可复用 prompt、自定义指令或任务开头。 |

这个仓库不会编造平台命令。如果某个工具的配置方式变化，请把相关 prompt 复制到该工具当前支持的项目规则或自定义指令中。

## 它适合解决什么

| 场景 | 常见问题 | 第一性原理动作 |
| --- | --- | --- |
| Debugging | Agent 只修第一个报错。 | 复现、隔离候选原因、证明根因。 |
| Architecture | Agent 直接上流行基础设施。 | 从约束、数据流、失败模式、团队能力出发。 |
| Refactoring | Agent 移动代码但没有降低复杂度。 | 找到真正复杂度来源，保持行为不变。 |
| Technical decisions | Agent 选择热门工具。 | 比较适配度、成本、可逆性、验证方式。 |
| Product thinking | Agent 把每个请求都变成功能。 | 从用户问题、价值链、证据、最小实验出发。 |

## 示例 Prompts

实践示例位于 [`examples/`](examples/)：

- [`debugging.md`](examples/debugging.md)
- [`architecture.md`](examples/architecture.md)
- [`refactoring.md`](examples/refactoring.md)
- [`technical-decision.md`](examples/technical-decision.md)
- [`product-thinking.md`](examples/product-thinking.md)

## 什么时候使用

当任务存在不确定性、风险或多条可能路径时，特别适合使用：

- 根因调试
- 架构设计
- 重构策略
- 技术选型
- 产品与范围决策
- 性能优化
- 可靠性改进
- 安全敏感变更
- 迁移规划

对于非常小且明确的改动，推理可以很短。重点是纪律，不是仪式感。

## 文件结构

```text
README.md
README.zh-CN.md
LICENSE
CHANGELOG.md
CONTRIBUTING.md
.gitignore
assets/
  hero.svg
  reasoning-loop.svg
  foundation.svg
  prism-mascot.svg
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

这个仓库只包含文本 prompts、文档和轻量 SVG 资产。它不需要 API keys、遥测、包安装或运行时网络访问。

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
