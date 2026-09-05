# repository-governance

[简体中文](README.zh-CN.md)

Establish or audit repository `AGENTS.md` guidance so durable engineering rules, knowledge entry points, and verification commands reflect repository reality.

## When to use

- Create the necessary agent guidance for a new repository.
- Audit stale rules, invalid commands, or temporary project state in existing AGENTS guidance.
- Evaluate a proposed rule's owner or apply approved governance changes.

## Installation

Give this prompt to Codex. Append a tag or commit to select a version; private repositories require access.

```text
Install or update repository-governance for the current user from this repository:
https://github.com/ailijian/repository-governance-SKILL.git
Use my specified version; otherwise read the remote default branch and record the actual commit.
Read SKILL.md, agents/openai.yaml, and references/ first. Check existing external dependencies and version compatibility.
If dependencies are missing or incompatible, report the gaps and stop installation. Do not install other Skills or rewrite shared files automatically.
When dependencies are ready, install only this Skill's SKILL.md, agents/, and references/ at $HOME/.agents/skills/repository-governance/, preserving structure and content.
Leave identical content unchanged. Back up before updating; show conflicting local customizations and wait for my decision.
Check the Skill name, allow_implicit_invocation: false, reference resolution, and host discovery. Report the installation path, commit, and verification results. Do not invoke this Skill during installation.
```

This version references public contracts and applicable related Skill contracts that are not included in this repository; compatible dependencies must already be available locally. Missing dependencies are reported before installation.

## Usage

Explicitly select this Skill in the target project and use the prompts below. Clients supporting `$` invocation can use the complete examples. Replace `<…>` placeholders; do not repeat inputs already clear in context.

### Audit existing guidance

```text
$repository-governance
Run Audit on this repository's root AGENTS.md.
Check rules against current reality, inspect entry points and commands, and identify temporary Delivery state.
Return findings and recommendations only.
```

### Create guidance for a new repository

```text
$repository-governance
Run Bootstrap / Normalize on <repository path> to create its root AGENTS.md.
Repository purpose: <settled purpose>. Write only evidence-backed durable rules and existing entry points, then stop for my review.
```

Select one operation per request. `Evaluate Candidate` assesses a proposed rule's destination without writing; `Apply Approved Update` applies explicitly approved changes to the identified file. Repository-wide requests target the root AGENTS by default, without automatically editing nested guidance, global configuration, code, or CI.

## Files and rules

- [SKILL.md](SKILL.md): responsibilities and execution method.
- [Dedicated contract](references/agents-contract.md): inputs, dependencies, outputs, and decision rules.
- [agents/openai.yaml](agents/openai.yaml): invocation configuration; implicit invocation is disabled.

See the [official Skill documentation](https://learn.chatgpt.com/docs/build-skills) for Codex installation locations and invocation. License: [LICENSE](LICENSE).
