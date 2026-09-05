# repository-governance

[English](README.md)

建立或审计仓库 AGENTS 指引，并实施明确获准的治理变更。 具体操作、职责边界和输出规则由 [SKILL.md](SKILL.md) 及其[专属合同](references/agents-contract.md)维护。需显式调用，`policy.allow_implicit_invocation` 保持 `false`。

## 维护源与安装内容

本仓库在 [ai_native_workflow](https://github.com/ailijian/ai_native_workflow) 中的维护位置为 `skills/repository-governance/`，保留独立远端和 Git 历史。

组件安装内容为：

```text
SKILL.md
agents/openai.yaml
references/agents-contract.md
```

README、Git 元数据和本机系统文件不属于 Skill payload；LICENSE 保留为约束本组件的仓库元数据。

## 依赖与安装

本仓只包含一个组件。日常采用前，应从总仓发布记录选择经过核验的完整集合。公共执行合同和 manifest 位于 `<agents-root>/workflow-contracts/`，与 `<agents-root>/skills/` 同级；引用到的其他 Skill 合同也必须来自所选集合，不能随意拼接各仓最新版本。

单独克隆本仓不会取得公共包或完成安装。独立检出时，须从所选集合取得依赖和安装说明，不能假设旁边已有总仓目录。总仓为私有仓库，需要访问权限。必要版本或依赖不可取得时，应报告具体缺口，不重新生成一份合同替代。

按所选集合的实际安装与恢复说明操作：解析目标机器的根路径，保留既有用户配置，核对安装内容与引用，记录真正生效的版本。修改维护源不自动更新已安装 Skill，也不迁移既有 Delivery。完整集合未就绪时，本源只支持明确限定范围的候选检查。

## 维护

在规则 Owner 处修改，按总仓 `docs/maintenance.md` 和所选合同核验受影响组件，包括内容身份、显式调用配置、明确组装布局中的引用，以及必要的受影响行为。验证输出与维护源分开，不为每次迁移检查新增永久测试。

迁移来源和准确组合由总仓记录。父仓 gitlink 只能记录子仓提交；未提交内容应另行绑定候选身份、完成评审，才能形成已提交组合。原有 Git 标签继续保留当时的含义。

## 许可证

见 [LICENSE](LICENSE)。
