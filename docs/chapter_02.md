# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 2 — Authorization Levels and Human Authority
**Estimated reading time:** approximately 7 minutes

## Purpose

The A0–A4 model classifies the level of authorization control required before an action can occur. It is one of GAD's primary safeguards against accidental authority expansion.

## 2.1 Authorization Levels

| Level | Name | Typical Behavior | Human Requirement |
|---|---|---|---|
| A0 | Observe / Analyze | Read, inspect, classify, calculate, monitor | Pre-authorized access boundary |
| A1 | Draft / Validate | Create internal drafts, tests, evidence summaries, recommendations | Pre-authorized bounded activity |
| A2 | Delegated Low-Risk Execution | Reversible internal action with limited consequence | Explicit task or standing delegation |
| A3 | Consequential Controlled Execution | Production, external, financial, security-sensitive, or materially binding action | Specific human approval before execution |
| A4 | High-Impact / Irreversible / Authority-Changing | Major commitments, destructive actions, legal/regulatory sign-off, authority expansion | Named human approval; additional control if policy requires |

The machine-readable reference is [`AUTHORIZATION_MATRIX.csv`](templates/AUTHORIZATION_MATRIX.csv).

## 2.1.1 Semantic Guardrail: A-Levels Are Authorization Levels

A0–A4 classify the **authorization control required for an action**. They are not a maturity ladder and they are not a measure of how smart or confident an AI system is.

An organization may automate an A0 or A1 action heavily, while an A3 action can still require a specific human decision. Conversely, a human may perform an A4 action if that human has the required authority. The level belongs to the **action in context**, not to the identity of the actor alone.

## 2.2 A0 — Observe / Analyze

Examples:

- read a Jira issue;
- calculate cycle time;
- inspect a Git diff;
- check whether required evidence exists;
- monitor a service;
- classify a work item using established rules.

A0 must not mutate operational state.

## 2.3 A1 — Draft / Validate

Examples:

- draft a project plan;
- generate test cases;
- prepare a pull-request description;
- validate a configuration;
- assemble an evidence package;
- write an internal recommendation.

A1 outputs are not automatically approved deliverables.

## 2.4 A2 — Delegated Low-Risk Execution

A2 permits bounded execution when a human has explicitly delegated the class of action.

Typical A2 controls:

- reversible;
- narrow scope;
- low external consequence;
- observable;
- logged;
- clear stop condition;
- no authority expansion;
- no secret or policy bypass.

Examples may include:

- moving a work item between internal non-approval states;
- applying a pre-approved label;
- generating a routine internal report;
- running approved tests;
- creating a draft branch.

## 2.5 A3 — Consequential Controlled Execution

A3 requires a specific human decision before the action.

Common triggers:

- production deployment;
- external publication;
- client-facing delivery;
- financial commitment above delegated authority;
- material data handling change;
- access-control change;
- approval of a release;
- accepting a material risk.

The decision must be recorded and linked to the action.

## 2.6 A4 — High-Impact or Authority-Changing Action

A4 is reserved for actions where the consequence, irreversibility, legal significance, or authority change warrants the strongest control.

Examples:

- granting a new autonomous execution boundary;
- deleting protected production data;
- signing or changing a material contract;
- final regulatory sign-off;
- disabling a critical security control;
- changing the methodology's human-authority model;
- approving an irreversible migration without a safe recovery path.

A4 should not be satisfied by a vague standing statement such as “the AI may do whatever is necessary.”

## 2.7 Authorization Triggers

A work item may be reclassified upward when conditions change.

Typical triggers include:

- budget or schedule threshold breach;
- new client or personal data;
- production scope introduced;
- external communication;
- security privilege change;
- regulatory impact;
- destructive or irreversible operation;
- deviation from approved architecture;
- unresolved evidence gap;
- cross-project or cross-client impact.

## 2.8 Authorization Is Context-Specific

The same technical action can have different authorization levels.

Example:

```text
Restart local disposable test container → A2
Restart shared staging service → A3
Restart production service during incident under approved runbook → A2 or A3 depending on delegation
Disable production security service → A4
```

## 2.9 Authorization Record

A valid authorization record should state:

- decision ID;
- action or action class;
- scope;
- authorized actor;
- approving human;
- conditions;
- validity period if applicable;
- evidence considered;
- recovery conditions;
- decision outcome.

See [`decision_record_template.md`](templates/decision_record_template.md).

## 2.10 Human Decision State

A Jira or workflow implementation should include a visible control point for unresolved consequential decisions.

Recommended conceptual state:

```text
HUMAN DECISION
```

Entering the state should occur when:

- A3/A4 approval is required;
- risk acceptance is needed;
- an exception requires judgment;
- evidence is sufficient for a decision but the system cannot authorize itself.

## 2.11 Authorization and Risk Are Different

A low-risk action is not automatically authorized.

A high-risk action is not automatically prohibited.

Risk informs the required controls; authorization determines whether execution is permitted.

## 2.12 Authorization and Confidence Are Different

High AI confidence does not grant authority.

A model can be 99% confident and still be unauthorized to:

- deploy;
- spend;
- publish;
- approve;
- sign;
- delete;
- expand its own permissions.

## 2.13 Standing Delegation

Standing delegation may be appropriate for A2 activity if it is:

- documented;
- scoped;
- revocable;
- monitored;
- time-bounded or periodically reviewed;
- explicit about prohibited actions.

Standing delegation should not silently become A3/A4 authority.

## 2.14 Minimum Control Rule

If classification is uncertain and the consequence is material, use the more restrictive level until reviewed.

## 2.14 Granting Rules, Evidence Thresholds, and Oversight

| Level | Who may grant it | Minimum authorization evidence | Exposure boundary | Oversight |
|---|---|---|---|---|
| A0 | Project policy/access owner | Approved read/access scope or work-item context | No operational mutation | Logging/monitoring as appropriate |
| A1 | Project policy or authorized task owner | Bounded task/scope and artifact trace | Internal draft/validation output only | Review when output is used consequentially |
| A2 | Named human acting within delegated authority | Recorded delegation or task authorization | Narrow, reversible, low-consequence scope | Logged execution, exceptions surfaced |
| A3 | Named human with authority over the consequence | Specific decision record plus required validation/evidence | Exact consequential scope approved | Pre-action human approval and post-action evidence |
| A4 | Human Project Hub, executive, board, or specialist authority as required by policy | Formal decision with risk, scope, recovery/contingency, and independent evidence appropriate to impact | Exact high-impact, irreversible, or authority-changing scope | Strongest applicable human control and close monitoring where appropriate |

The machine-readable implementation is [`AUTHORIZATION_MATRIX.csv`](templates/AUTHORIZATION_MATRIX.csv).

## 2.15 Worked Examples by Level

### A0 example — Observe
An AI reporting agent reads Jira issue metadata and calculates cycle time. It cannot change issue state.

### A1 example — Draft
An AI agent drafts a change-impact assessment and identifies missing evidence. The draft does not authorize the change.

### A2 example — Delegated low-risk execution
A worker agent applies a pre-approved internal label and runs a known validation script under a time-boxed delegation. The action is logged and reversible.

### A3 example — Consequential controlled execution
A release agent prepares a production deployment but cannot execute until a named human approves the specific release after validation and recovery evidence are complete.

### A4 example — Authority-changing action
A proposal would expand an agent from internal A1 drafting to independently executing a new class of production actions. The authority change itself is A4 and requires a formal human decision; the agent cannot approve its own expansion.

## 2.16 Delegation Validity, Expiry, and Revocation

A2 or other standing delegation should be assigned to a named human grantor, bounded by action class/project/tool/data/environment, time-boxed when practical, revocable, and treated as invalid after expiry or material boundary change.

Every active standing delegation should be recorded in [`AUTHORIZATION_GRANT_REGISTER.csv`](templates/AUTHORIZATION_GRANT_REGISTER.csv). Revocation changes future authority only; it does not erase prior execution history.

## 2.17 Human Decision State Machine

```text
PENDING_HUMAN_DECISION
    ├─→ APPROVED
    ├─→ REJECTED
    ├─→ MORE_INFORMATION_REQUIRED
    ├─→ WITHDRAWN
    └─→ EXPIRED
```

A later human override creates a **new decision record linked to the prior decision** rather than rewriting the earlier outcome.

A decision is executable only when the outcome is `APPROVED`, scope matches, conditions are satisfied, the decision is not expired/revoked, and the actor is authorized.

## 2.18 Authorization-Grant Register

Minimum fields include grant ID, actor/agent, authorization level and action class, scope, granting human, grant/expiry/revocation timestamps, linked decision/evidence, and current status.

Cross-reference: [`AUTHORIZATION_GRANT_REGISTER.csv`](templates/AUTHORIZATION_GRANT_REGISTER.csv).

## Cross-References

- Human–AI roles: [Chapter 3](chapter_03.md)
- Decision logic: [Chapter 8](chapter_08.md)
- Jira implementation: [Chapter 9](chapter_09.md)
- Pilot authorization: [Chapter 10](chapter_10.md)
- Template: [`AUTHORIZATION_MATRIX.csv`](templates/AUTHORIZATION_MATRIX.csv)

[Back to outline](outline.md)
