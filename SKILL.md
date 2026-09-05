---
name: repository-governance
description: >-
  Establish, audit, evaluate candidates for, and apply explicitly approved minimal updates to repository-level AGENTS.md containing durable repository guidance. Use only when the user explicitly selects or invokes this Skill to bootstrap or normalize a repository AGENTS.md, audit repository governance, decide whether a candidate belongs in AGENTS.md, or apply an approved governance update. Do not use for ordinary coding, product or architecture design, delivery baselines or plans, Stage implementation or acceptance, routine code review, documentation maintenance, CI or test changes, or temporary Delivery rules.
---

# Repository Governance

Govern the repository-level instructions an AI agent should retain across future Deliveries. Treat a Repo `AGENTS.md` as a high-signal map plus durable behavior constraints, never as a repository encyclopedia or a second project knowledge base.

Read [references/agents-contract.md](references/agents-contract.md) completely before performing any operation. Use it for the lean document structure, destination rules, report formats, and minimal-patch contract.

Apply its method and handoff rules to identify the selected workflow and attributable inputs. Governance supplies concise navigation to applicable methods and actual capabilities; it does not copy their contracts or install a workflow.

## Preserve the responsibility layers

Maintain this separation:

```text
Global AGENTS.md = cross-project engineering principles
Repo AGENTS.md   = durable repository rules, routing, and invariants
docs / contracts / schema / code = durable project and machine facts
Skills           = repeatable workflows
public contract  = shared workflow method and handoff rules
BASELINE.md       = current Delivery target
PLAN.md           = current Delivery execution plan
existing record  = attributable evidence and control history, conditionally RECORD.md
tests / CI        = deterministic enforcement and evidence
```

Do not copy a global principle, Skill algorithm, authoritative document, current Delivery state, implementation plan, evidence, review history, or completed-plan detail into Repo `AGENTS.md`. Keep a concise high-level invariant in `AGENTS.md` when agents must know it and recommend test or CI enforcement separately when deterministic enforcement is valuable.

## Enforce invocation and mutation boundaries

- Operate only after the user explicitly selects or invokes this Skill.
- Select exactly one operation from Bootstrap / Normalize, Audit, Evaluate Candidate, or Apply Approved Update.
- Treat Audit and Evaluate Candidate as read-only.
- Modify a Repo `AGENTS.md` during Bootstrap / Normalize only when the user explicitly asks to create, initialize, optimize, or normalize it.
- Modify a Repo `AGENTS.md` during Apply Approved Update only when the user explicitly authorizes applying the identified governance update.
- Never create or modify `BASELINE.md`, `PLAN.md`, business code, tests, CI, contracts, schemas, project documentation, or another Skill while using this Skill.
- Never commit, push, advance a Stage, close a Gate, or perform Acceptance.
- Do not reorganize documentation or move rules between root and closer instruction files without explicit authorization.
- If the request exceeds these boundaries, report the correct destination or workflow and stop that part of the work.

## Resolve the target instruction file

Resolve the target before collecting evidence or writing:

1. Use an `AGENTS.md` or `AGENTS.override.md` path explicitly specified by the user.
2. For any repository-wide operation—including Bootstrap / Normalize, Audit, Evaluate Candidate, or Apply—default to the repository-root `AGENTS.md`, even when the current working directory is inside a nested package or application.
3. Read closer `AGENTS.md` and `AGENTS.override.md` files when present as scoped authorities that inform repository-root analysis. Do not make a closer file the mutation target unless the user explicitly scopes the operation to it.
4. If the repository root cannot be determined reliably, ask before modifying anything. For a read-only operation, state the unresolved scope instead of silently choosing the nearest instruction file or broadening the audit.

## Ground in repository reality

Before making a judgment:

1. Apply the target-resolution rules and record the exact instruction file in scope.
2. Read the active global `AGENTS.md` when present so repository guidance does not duplicate it.
3. Read existing root and applicable closer `AGENTS.md` or `AGENTS.override.md` files when present. Respect the instruction hierarchy.
4. Locate the repository knowledge map when present and read only the long-lived Product, Architecture, Domain, Contract, Schema, Security, Testing, or ownership sources necessary for the operation.
5. Inspect the real source tree, package or workspace scripts, documented command entry points, and CI configuration when they bear on a proposed rule.
6. Use current `BASELINE.md`, `PLAN.md`, reviews, archives, and evidence only to identify content that must remain Delivery-specific or historical. Do not treat them as durable authority by default.
7. Record the evidence for every repository-specific rule retained, added, removed, redirected, or challenged.

Identify relevant current content and working-tree state rather than relying on HEAD or an old audit alone. Use non-mutating inspection; disable optional Git locks and diff index auto-refresh when querying Git, and use direct content/object reads for preserved evidence. Verify a command's implementation and Owner, not just a string naming it; this operation does not require running the suite or creating its missing runner.

Consume upstream Specialist findings with their original IDs, source, result and remaining obligations. Rechecking a missing path can establish current governance evidence; it does not close the upstream finding or reissue Verification, Knowledge, Review or Acceptance judgments. A finding or proposed destination is not approval to write.

Prefer the narrowest authoritative source. Do not select between conflicting current authorities based only on date, filename, existing code, or historical behavior. Report a material conflict and block only the affected governance conclusion or update until the authority is resolved.

For a new repository, proceed once its basic purpose and scope are known. Keep the initial guide small. Omit unknown Architecture, Domain, CI, Testing, and command guidance rather than inventing it.

For a mature repository, compare instructions against the knowledge map, authoritative documents, contracts, schema, code, scripts, and CI. Retain only rules supported by current evidence.

## Qualify durable guidance

Include a repository rule only when it is:

- expected to remain valid across multiple future Deliveries;
- specific to this repository rather than a cross-project preference;
- likely to prevent recurring error, ambiguity, or material risk if an agent misses it; and
- best represented in `AGENTS.md`, alone or together with a more authoritative or deterministic owner.

Prefer broad durable ownership plus a knowledge-map reference over enumerating business entities or implementation details. Keep root guidance repository-wide. Leave domain-local guidance in the applicable closer instructions.

Use the reference's Delivery and Testing rules for short, evidence-backed navigation to the selected public contract, code-review, existing records and actual canonical mechanisms. Keep low-risk direct work available. Route test maintenance policy, selection logic, compatibility and release details to their current Owners; do not turn each finding or useful local practice into another permanent AGENTS rule.

Classify a governance candidate without asking the user to answer the qualification questions. Choose the primary decision from `AGENTS`, `DOCS`, `SKILL`, `TEST/CI`, `CODE`, `GLOBAL AGENTS`, `PLAN/BASELINE`, `NONE`, or `NEEDS CLARIFICATION`. Use `CODE` when the implementation is the proper durable owner. Add a companion destination only when another layer has a distinct supporting role, such as deterministic `TEST/CI` enforcement for a high-level `AGENTS` invariant.

## Run the selected operation

### Bootstrap / Normalize

Use this operation for a new repository, first migration to this governance model, or an explicitly requested cleanup of an overgrown guide.

1. Collect the grounding evidence.
2. Separate durable repository-wide guidance from global rules, workflow algorithms, project facts, Delivery state, history, and locally scoped instructions.
3. Draft the smallest useful guide using only applicable sections from the lean framework.
4. Preserve supported repository-specific invariants and navigation.
5. Remove stale, duplicated, Delivery-specific, historical, or misplaced content only within the authorized target `AGENTS.md`.
6. Verify every path and canonical command that remains in the result.
7. Inspect the final diff and report changes with their evidence.

Do not delay Bootstrap until the repository has mature architecture or tooling. Do not create empty sections to simulate completeness.

### Audit

Keep the operation read-only. Compare the current guide with repository reality and check for:

- stale paths, commands, ownership, or invariants;
- duplication of global principles, Skills, or authoritative docs;
- Delivery-specific, Stage-specific, historical, or evidence content;
- deterministic rules better enforced by code, tests, or CI;
- missing high-risk durable repository invariants;
- low signal density or unnecessary length; and
- root rules that belong in closer instructions.

Return `PASS` when there is no material governance issue. Otherwise return `FINDINGS` and order findings by actual impact. Do not pad the report with style preferences.

### Evaluate Candidate

Keep the operation read-only. Evaluate durability, repository specificity, repeated-error or risk reduction, current evidence, scope, duplication, and the best owner. Return the candidate report defined in the reference contract. Redirect Delivery-specific rules to `PLAN/BASELINE`, cross-project preferences to `GLOBAL AGENTS`, workflow methods to `SKILL`, durable facts to `DOCS` or machine authorities, and deterministic checks to `TEST/CI` as appropriate.

Do not reject an important agent-facing invariant merely because tests or CI can also enforce it. Recommend both layers when they serve different purposes.

### Apply Approved Update

Confirm that the user's authorization identifies the rule or approved audit finding to apply. If the target or intended rule is materially ambiguous, request clarification before writing.

1. Recheck the supporting sources and current target file.
2. Patch only the resolved and authorized `AGENTS.md` or `AGENTS.override.md`.
3. Make the smallest coherent insertion, replacement, move, or deletion.
4. Preserve unrelated supported guidance and the existing organization when it remains sound.
5. Remove only stale or duplicate text included in the approval.
6. Re-read the result and inspect the diff for scope expansion.

Bind the patch to the actual authorized rule or finding and preserved constraints. If changed evidence materially alters the approved meaning or target, resolve that part before writing; otherwise complete the existing authorization without requesting it again. A navigation correction cannot certify that a missing mechanism has been implemented or that an upstream obligation is closed.

Do not rewrite the whole file for consistency, update a companion destination, or modify another fact source unless the user separately authorizes it.

## Complete the operation

Use the exact output contract for the selected operation. For Bootstrap / Normalize and Apply, name the modified target instruction file, summarize added, changed, and removed rules with evidence, identify unresolved governance issues, and report any better companion destinations. For Audit and Evaluate Candidate, explicitly confirm that no files were modified.

Stop when the requested governance operation and its proportional verification are complete. Do not begin repository implementation or another governance operation automatically.
