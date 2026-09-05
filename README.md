# repository-governance

[简体中文](README.zh-CN.md)

Establish or audit repository AGENTS guidance, and apply explicitly authorized governance changes. Detailed operations, boundaries, and output rules belong to [SKILL.md](SKILL.md) and its [dedicated contract](references/agents-contract.md). Invoke it explicitly; `policy.allow_implicit_invocation` remains `false`.

## Source and payload

This independent repository is maintained at `skills/repository-governance/` within [ai_native_workflow](https://github.com/ailijian/ai_native_workflow). Its origin and Git history remain independent.

The installable component files are:

```text
SKILL.md
agents/openai.yaml
references/agents-contract.md
```

README files, Git metadata, and local operating-system files are not Skill payload. LICENSE remains repository metadata governing this component.

## Dependencies and installation

This checkout contains one component. Select a verified complete collection from the parent project's release records before ordinary adoption. Its public execution contract and manifest belong at `<agents-root>/workflow-contracts/`, alongside `<agents-root>/skills/`; referenced sibling contracts must also come from the selected collection. Do not silently combine separate repositories' latest versions.

Cloning this repository alone does not fetch the public package or install the workflow. A standalone checkout must obtain the required dependencies and installation instructions from the selected collection; it must not assume the parent project's directories exist beside it. The parent repository is private and requires access. If a required version or dependency is unavailable, report that specific gap; do not generate a replacement contract.

Use the selected collection's actual installation and recovery instructions. Resolve target roots for that machine, preserve existing user configuration, verify installed content and references, and record what actually became active. Updating this source does not update installed Skills or migrate existing Deliveries. Without a complete verified collection, this source is only suitable for explicitly scoped candidate inspection.

## Maintenance

Edit the owning source and verify the affected component using the parent project's `docs/maintenance.md` and the selected contracts. Check payload identity, explicit-invocation configuration, references in a declared assembled layout, and affected behavior where needed. Keep validation outputs separate from source; do not add a permanent test for every migration check.

The parent project records migration provenance and exact component combinations. A parent gitlink records a child commit only; pending working-tree changes need their own candidate identity and review before they can form a committed combination. Existing Git tags retain their historical meaning.

## License

See [LICENSE](LICENSE).
