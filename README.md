# Repository Governance Skill

[中文说明](README.zh-CN.md)

`repository-governance` is a Codex skill for maintaining high-signal, durable repository-level `AGENTS.md` guidance. It grounds every judgment in repository reality and keeps repository governance separate from global engineering principles, project documentation, workflow skills, Delivery baselines and plans, and deterministic test or CI enforcement.

## What it does

- Bootstrap or normalize a repository-root `AGENTS.md` when explicitly requested.
- Audit an existing guide without modifying files.
- Evaluate whether a proposed rule belongs in `AGENTS.md` or another authority layer.
- Apply only an explicitly approved, minimal governance update.

The skill is intentionally not a general code-review, architecture-design, documentation-maintenance, or Delivery-execution workflow.

## Install with a prompt

Copy the prompt below into Codex or another AI coding tool with native skill installation support. No shell commands or manual file copying are required.

```text
Install the AI agent skill located at the repository root of https://github.com/ailijian/repository-governance-SKILL.md under the canonical name repository-governance in my user-level skills directory. Use $skill-installer or your native skill installer if available. Do not install it into the current project. Preserve SKILL.md, agents/openai.yaml, and references/agents-contract.md. If a destination with that name already exists, stop and ask before replacing it. Validate the installed skill and report its path; for Codex, also tell me that it will be available on my next turn.
```

## Example prompts

```text
Use $repository-governance to audit the repository-root AGENTS.md. Do not modify files. Return PASS if there is no material governance issue.
```

```text
Use $repository-governance to evaluate whether this candidate rule belongs in the repository AGENTS.md: <candidate rule>
```

## Package contents

- `SKILL.md` — trigger definition, operating boundaries, and the four governance operations.
- `references/agents-contract.md` — lean repository guide and exact output contracts.
- `agents/openai.yaml` — Codex-facing display metadata and explicit-invocation policy.

## License

Apache License 2.0. See [LICENSE](LICENSE).
