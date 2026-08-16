# Repository AGENTS Contract

Use this contract to structure repository guidance and the outputs of `repository-governance`. Keep project facts out of this reference.

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

Point to `delivery-baseline`, `design-readiness` when applicable, `implementation-planning`, `acceptance-review` when the PLAN requires Stage Acceptance, and Code Review when the PLAN requires it. Do not restate their algorithms or bind Code Review to a product-specific feature, mode, or tool.

### Documentation Governance

Use one long-lived owner for each material fact. Prefer update-before-create and references over duplication. Do not create per-Delivery or per-version copies of durable Product, Architecture, Domain, Contract, Security, Testing, or Design knowledge. Let Git retain history.

Treat `BASELINE.md` plus `PLAN.md` as the normal new persistent artifacts for a substantial Delivery. Add another durable document only when its knowledge survives future Deliveries, lacks an existing owner, and cannot be derived reliably from a machine-readable source.

Prefer generated views when Contract, Schema, code, or another machine source owns the truth. Treat archives, reviews, Gate evidence, and completed plans as history or evidence unless the knowledge map explicitly assigns current authority. Do not make documentation-tree reorganization an incidental cleanup.

### Contract, Data, and Security

Include only repository-specific, durable, high-risk boundaries such as Contract ownership, authoritative writes, authorization, migration discipline, sensitive data, Secrets, trust boundaries, or server/client ownership. Omit generic security advice already governed globally.

### Testing and Commands

State the durable test strategy and only canonical command entry points verified to exist. Do not invent missing commands for a new project.

Use these default semantics when applicable: verify every material Stage; do not equate every Stage with a full suite; prefer targeted or affected checks; choose broader regression from risk, the current plan, an integration checkpoint, or final closure; allow Acceptance to reuse trustworthy evidence attributable to the current repository state.

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
