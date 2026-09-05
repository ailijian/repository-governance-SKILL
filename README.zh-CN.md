# repository-governance

[English](README.md)

建立或审计仓库级 `AGENTS.md`，让长期工程规则、知识入口和验证命令符合仓库实际情况。

## 使用场景

- 为新仓库创建必要的 Agent 工作指引。
- 检查现有 AGENTS 中的过期规则、无效命令或临时项目状态。
- 判断拟议规则的归属，或应用已经批准的治理修改。

## 安装

将下面提示词交给 Codex。如需指定版本，在末尾补充 tag 或 commit；私有仓库需要相应访问权限。

```text
请从 https://github.com/ailijian/repository-governance-SKILL.git 为当前用户安装或更新 repository-governance。
使用我指定的版本；未指定时读取远端默认分支，并记录实际 commit。
先读取 SKILL.md、agents/openai.yaml 和 references/，核对已有外部依赖及版本兼容性。
依赖缺失或不兼容时，报告具体缺口并停止安装，不自动安装其他 Skill 或改写共享文件。
依赖就绪后，仅将本 Skill 的 SKILL.md、agents/ 和 references/ 安装到 $HOME/.agents/skills/repository-governance/，保留原有结构与内容。
已有内容一致则不重复写入；更新前备份旧内容，如有本地定制冲突，展示差异后等我决定。
检查 Skill 名称、allow_implicit_invocation: false、引用解析和宿主发现情况，报告安装路径、commit 和验证结果。安装时不调用本 Skill。
```

当前版本引用未随本仓提供的公共合同及适用的关联 Skill 合同，运行前需由本机环境提供兼容依赖。缺失依赖会在安装前列出。

## 使用方法

在目标项目中显式选择本 Skill，再使用以下提示词；支持 `$` 调用的客户端可直接复制整段。替换 `<…>` 中的内容，已在上下文明确的信息无需重复提供。

### 审计已有指引

```text
$repository-governance
对当前仓库根目录的 AGENTS.md 执行 Audit。
检查规则是否符合现状、入口和命令是否有效，是否混入临时 Delivery 状态。
本轮只返回审计结论和建议。
```

### 创建新仓库指引

```text
$repository-governance
对 <仓库路径> 执行 Bootstrap / Normalize，创建仓库根目录的 AGENTS.md。
仓库用途为 <已确定用途>，仅写入有依据的长期规则和现有入口，完成后停下供我评审。
```

每次选择一个操作。`Evaluate Candidate` 只读判断拟议规则应归属哪里；`Apply Approved Update` 根据明确批准的内容修改目标文件。仓库级请求默认针对根 AGENTS，不自动修改更深层文件、全局配置、代码或 CI。

## 文件与规则

- [SKILL.md](SKILL.md)：职责和执行方法。
- [专属合同](references/agents-contract.md)：输入、依赖、输出与判定规则。
- [agents/openai.yaml](agents/openai.yaml)：调用配置，已关闭隐式调用。

Codex 的安装目录和调用方式见 [官方 Skill 文档](https://learn.chatgpt.com/docs/build-skills)。许可证见 [LICENSE](LICENSE)。
