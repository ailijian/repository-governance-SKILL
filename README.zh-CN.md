# Repository Governance Skill

[English](README.md)

`repository-governance` 是一个面向 Codex 的仓库治理 Skill，用于维护高信号、可长期复用的仓库级 `AGENTS.md`。它要求所有判断都以当前仓库事实为依据，并严格区分仓库治理、全局工程原则、项目文档、工作流 Skill、Delivery 基线与计划，以及测试或 CI 的确定性约束。

## 能做什么

- 在用户明确要求时，创建或规范化仓库根 `AGENTS.md`。
- 只读审计现有治理文件，不修改任何文件。
- 判断候选规则应进入 `AGENTS.md`，还是由其他职责层承载。
- 仅应用用户明确批准的最小治理更新。

它不是通用代码审查、架构设计、文档维护或 Delivery 执行工作流。

## 用一段 Prompt 安装

将下面的 Prompt 直接发送给 Codex，或其他支持原生 Skill 安装的 AI 编程工具。无需执行命令，也无需手工复制文件。

```text
请安装位于 https://github.com/ailijian/repository-governance-SKILL.md 仓库根目录的 AI Agent Skill，并以 repository-governance 作为规范名称安装到我的用户级 Skills 目录。优先使用 $skill-installer 或你原生的 Skill 安装能力；不要安装到当前项目中。完整保留 SKILL.md、agents/openai.yaml 和 references/agents-contract.md。如果同名目标已经存在，先停止并询问我是否替换。安装后验证 Skill，并报告安装路径；如果你是 Codex，同时告诉我该 Skill 将从我的下一轮对话开始可用。
```

## 使用示例

```text
使用 $repository-governance 只读审计仓库根 AGENTS.md。不要修改任何文件；如果不存在实质治理问题，返回 PASS。
```

```text
使用 $repository-governance 判断下面这条候选规则是否应进入仓库 AGENTS.md：<候选规则>
```

## 包含内容

- `SKILL.md` — 触发条件、操作边界与四种治理操作。
- `references/agents-contract.md` — 精炼仓库指南框架与精确输出契约。
- `agents/openai.yaml` — Codex 展示元数据与仅显式调用策略。

## 许可证

Apache License 2.0，详见 [LICENSE](LICENSE)。
