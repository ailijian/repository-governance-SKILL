# Repository AGENTS Contract

Use this contract to structure repository guidance and the outputs of `repository-governance`. Keep project facts out of this reference.

## Method and handoff

Identify the selected collection from the sibling public [manifest](../../../workflow-contracts/manifest.yaml), checking this entrypoint and dependencies actually used. Apply the public [source and evidence](../../../workflow-contracts/execution-contract.md#source-and-evidence) and [handoff](../../../workflow-contracts/execution-contract.md#handoff) rules to current inputs and upstream findings. Do not load every Skill or historical report.

An explicitly selected partial candidate may be used for isolated calibration with its limits disclosed. Ordinary adoption requires the applicable complete release. For missing or mixed dependencies and old reports, use [version and recovery](../../../workflow-contracts/execution-contract.md#versions-and-recovery): retain the old method/source binding, recover necessary original content and block only dependent conclusions. Do not silently substitute current rules, install a package, migrate a Delivery or reissue another producer's verdict.

Keep method identity, assessed input state, authorization and unresolved upstream obligations in the operation report or existing authorized record. They are not automatically durable repository guidance. Audit and Evaluate Candidate remain read-only; Bootstrap / Normalize and Apply may write only the explicitly authorized instruction target. This Skill never creates a receipt, checkpoint or Delivery record as an incidental handoff.

## 1. Lean Repo AGENTS framework

Use only sections supported by repository reality. Rename or combine sections when that improves clarity. Omit empty sections.

```text
# Repository Agent Guide

1. Scope and Knowledge
2. Authority and Repository Invariants
3. Delivery Workflow
4. Documentation Governance
5. Contract, Data, and Security
6. Testing and Commands
7. Governance and Completion
```

### Scope and Knowledge

State durable repository ownership, explicit non-ownership when it prevents boundary mistakes, and the shortest reliable route into the knowledge map. Prefer broad ownership and map references over a list of entities that will decay.

### Authority and Repository Invariants

Route each kind of material fact to its authoritative owner. Include only a few repository-wide invariants whose violation would create serious error or risk. Link to the full explanation instead of reproducing Architecture, Domain, Contract, or Security documents.

Require the agent to stop affected work and report when current authoritative sources materially conflict. Never tell it to choose authority using filenames, recency, code behavior, or historical artifacts alone.

### Delivery Workflow

Record only repository-level routing and durable Gates. For a repository using the Delivery Protocol, a concise route is enough:

```text
substantial planned development
→ approved BASELINE.md
→ [material UI/UX → design-readiness]
→ implementation-planning
→ PLAN.md
→ one Stage at a time
→ required verification and PLAN-required Gates
→ [PLAN requires Stage Acceptance → acceptance-review]
→ checkpoint
```

Point to `delivery-baseline`, `design-readiness` when applicable, `implementation-planning`, `code-review` when review is requested or required, and `acceptance-review` when the PLAN requires Stage Acceptance. In this AI-native workflow, code-review is the unified review entrypoint and reuses the verified native review method; an ordinary native review outside the workflow does not by itself satisfy a workflow Gate. Do not restate either review algorithm or bind review to a product-specific UI feature, mode, or tool.

Navigate to the applicable public contract and actual release selection only when the repository adopts that protocol. Resolve references from the selected installed roots or existing repository navigation; do not copy a developer's absolute home path, embed temporary candidate directories, fabricate a release or require every small repository to adopt this workflow. Missing dependencies are an explicit obligation, not a reason to write links that pretend they are available.

Preserve the low-risk direct path: ordinary local changes can proceed under existing authorization and risk-proportionate verification without mandatory BASELINE, PLAN, RECORD, matrix or new Gate. Use the public [engineering analysis](../../../workflow-contracts/execution-contract.md#engineering-analysis) for applicable risk escalation; risk, verification scope and required Gates are separate decisions. A small diff does not waive a real security, data, contract or cross-component obligation. Governance navigation does not select today's profile, perform review or advance a Stage.

### Documentation Governance

Use one long-lived owner for each material fact. Prefer update-before-create and references over duplication. Do not create per-Delivery or per-version copies of durable Product, Architecture, Domain, Contract, Security, Testing, or Design knowledge. Let Git retain history.

Treat `BASELINE.md` plus `PLAN.md` as the normal new persistent artifacts for a substantial Delivery. Add another durable document only when its knowledge survives future Deliveries, lacks an existing owner, and cannot be derived reliably from a machine-readable source.

Distinguish durable knowledge from the public contract's conditional [control record](../../../workflow-contracts/execution-contract.md#control). Reuse reliable, retrievable PR, CI or project records first. Only a substantial Delivery lacking an equivalent carrier and needing cross-Stage/session recovery calls for a thin RECORD.md through an authorized controller. Reference its existing location and Owner when relevant; do not create it during governance work, prescribe it for every bug or fill AGENTS with its findings, results and control history. Retain necessary evidence under [material lifecycle](../../../workflow-contracts/execution-contract.md#material-lifecycle); navigation cleanup does not authorize deleting its sole recovery source.

Prefer generated views when Contract, Schema, code, or another machine source owns the truth. Treat archives, reviews, Gate evidence, and completed plans as history or evidence unless the knowledge map explicitly assigns current authority. Do not make documentation-tree reorganization an incidental cleanup.

### Contract, Data, and Security

Include only repository-specific, durable, high-risk boundaries such as Contract ownership, authoritative writes, authorization, migration discipline, sensitive data, Secrets, trust boundaries, or server/client ownership. Omit generic security advice already governed globally.

Keep detailed consumer identities, candidate compatibility, rollout and recovery responsibility with Contract/Release Owners. AGENTS may name those Owners and a few necessary boundaries, but should not duplicate a changing consumer/version matrix. Derive relationships from declared or observed authorized sources, not directory proximity.

### Testing and Commands

State the durable test strategy and only canonical command entry points verified to exist. Do not invent missing commands for a new project.

Use these default semantics when applicable: verify every material Stage; do not equate every Stage with a full suite; prefer targeted or affected checks; choose broader regression from risk, the current plan, an integration checkpoint, or final closure; allow Acceptance to reuse trustworthy evidence attributable to the current repository state.

Navigate to actual targeted, affected and full mechanisms only where they exist and are appropriate. Testing/runner Owners own selection semantics; Testing/Verification Owners own durable protection, test consolidation and retirement, flaky/slow test handling and coverage gaps. A short repository-specific link or invariant can be useful; copying the full maintenance or evidence policy into AGENTS is not.

Evaluate proposed test rules against the current Testing Owner and [verification-architecture](../../verification-architecture/SKILL.md) method. Equivalent tests may be consolidated while preserving their verification intent and distinct boundary protection; one finding does not require one permanent suite. Retries and quarantine are not passing evidence or permission to weaken critical protection. Route a capability/policy gap and its Owner without editing tests, quarantine or CI, inventing a command, or treating a proposed check as implemented. A corrected navigation line may explicitly state that the real capability is still missing.

Keep the supported debug loop discoverable where repository-specific routing is needed: focused diagnosis, affected repair verification, then any originally required final broad check. Do not mandate full regression after every small fix. Cost and test lifecycle details remain with their Owners; no per-test metadata registry is required by this framework.

### Governance and Completion

Prevent routine automatic growth. A useful candidate rule is:

```text
Do not modify this AGENTS.md merely because a task reveals a useful local practice.

Report only material repository-governance candidates that are durable across future Deliveries, repository-specific, likely to prevent repeated error or ambiguity, and not better expressed solely elsewhere.

Filter obvious non-candidates without involving the user. For a material candidate, report the proposed rule, why it is durable, and its preferred destination.

Do not modify repository governance without explicit authorization.
```

Add only repository-specific Stage or Gate completion invariants. Do not repeat global completion or communication rules.

## 2. Destination rules

Use the primary destination that owns the rule:

| Destination | Use for |
| --- | --- |
| `AGENTS` | Durable, repository-specific, agent-facing routing or invariant |
| `DOCS` | Durable project knowledge needing an authoritative human-readable owner |
| `SKILL` | A repeatable workflow or method rather than a repository fact |
| `TEST/CI` | Deterministic enforcement or automated drift prevention |
| `CODE` | An executable or machine fact whose durable owner is the implementation |
| `GLOBAL AGENTS` | A cross-project engineering principle or user preference |
| `PLAN/BASELINE` | A current Delivery target, Stage rule, Gate, or execution detail |
| `NONE` | Redundant, obsolete, unsupported, or too low-value to preserve |
| `NEEDS CLARIFICATION` | Material ambiguity that cannot be resolved from current evidence |

Use `AGENTS` as the primary destination and `TEST/CI` as a companion when agents need the high-level invariant and automation should enforce the deterministic condition. Keep the details of enforcement out of `AGENTS.md`.

## 3. Audit Report contract

Return exactly one status heading:

```text
PASS
```

or:

```text
FINDINGS
```

For `PASS`, briefly state the scope and evidence inspected and confirm that no files were modified.

For `FINDINGS`, list only material findings in descending impact. Give each finding:

- the affected rule or location;
- current evidence;
- why it violates correctness, durability, scope, authority, signal density, or enforceability;
- the preferred destination or disposition; and
- the smallest suggested action.

State unresolved authority conflicts and identify which governance conclusions remain blocked. Confirm that the Audit made no modifications.

When findings came from another Specialist, retain the original ID, report and source association beside this audit's current observation and recommended Owner. State what remains unimplemented or unverified; do not rename the upstream result into a governance PASS or infer approval to apply it.

## 4. Governance Candidate Report contract

Use this format:

```text
Decision: <AGENTS | DOCS | SKILL | TEST/CI | CODE | GLOBAL AGENTS | PLAN/BASELINE | NONE | NEEDS CLARIFICATION>
Companion destination: <optional supporting destination>

Reason:
<durability, repository specificity, repeated-error or risk analysis, and ownership rationale>

Evidence:
<current repository sources supporting or contradicting the candidate>

Suggested action:
<smallest next action; state that no file was modified>
```

Use `NEEDS CLARIFICATION` only after repository evidence cannot resolve a material ambiguity. If current authorities conflict, name them and block the affected recommendation rather than choosing one.

## 5. Bootstrap / Normalize and Apply Report contract

Report:

1. the exact `AGENTS.md` or `AGENTS.override.md` modified;
2. the governance rules added, changed, or removed;
3. the evidence for each material change;
4. unresolved governance issues, or `None`;
5. rules better placed in or additionally enforced by docs, a Skill, tests, CI, code, Global `AGENTS.md`, `BASELINE.md`, or `PLAN.md`; and
6. verification performed, including path and command checks plus final diff inspection.

Identify the selected method, actual input and authorization used. Distinguish a verified path/implementation from a command actually executed; do not run tests, builds, generators or services merely to validate a navigation update. Use direct object/content reads or Git queries prefixed with `git --no-optional-locks -c diff.autoRefreshIndex=false`; optional locks alone do not prevent every diff from refreshing index stat data. Compare the final state with the starting state and report unrelated concurrent changes without reverting them.

Do not claim that a companion destination was updated unless it was separately authorized and actually changed.

## 6. Minimal patch contract

For an approved update:

- patch only the resolved and authorized `AGENTS.md` or `AGENTS.override.md`;
- preserve all unrelated supported rules and useful organization;
- place the rule in the narrowest applicable scope;
- use concise agent-facing language and link to the authoritative owner;
- delete or move only content explicitly covered by the approval;
- avoid whole-file rewrites, stylistic reformatting, and opportunistic cleanup;
- do not create an empty framework section;
- verify every new path and command against repository reality;
- inspect the final diff; and
- stop without modifying any companion destination.
