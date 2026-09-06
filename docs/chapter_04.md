# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 4 — Governance Architecture and Lifecycle
**Estimated reading time:** approximately 5 minutes

## Purpose

This chapter defines how GAD keeps intent, execution, authority, validation, evidence, and status aligned over time.

## 4.1 Governance Layers

GAD uses four interacting layers.

### Layer 1 — Intent and Enterprise Constraints

Defines:

- strategy;
- outcomes;
- portfolio priorities;
- budget;
- policy;
- regulatory constraints;
- architecture principles;
- major commitments.

### Layer 2 — Delivery Governance

Defines:

- milestones;
- stage gates;
- backlog and WIP;
- dependencies;
- readiness criteria;
- release governance.

### Layer 3 — AI and Execution Governance

Defines:

- agent roles;
- authorization levels;
- allowed tools;
- data boundaries;
- validation;
- escalation;
- safe-failure behavior.

### Layer 4 — Evidence and Assurance

Defines:

- traceability;
- evidence packages;
- decision records;
- audit history;
- metrics;
- incident/remediation records.

## 4.2 Work-Item Lifecycle

A reference workflow:

```text
INTAKE
  ↓
ASSESSED
  ↓
READY
  ↓
IN PROGRESS
  ↓
VALIDATION
  ├─→ REMEDIATION REQUIRED
  ├─→ HUMAN DECISION
  └─→ APPROVED FOR RELEASE
            ↓
         RELEASED
            ↓
           DONE
```

`BLOCKED` may be used as a side state from any active stage.

## 4.3 Status Semantics

Each status should answer a precise question.

Examples:

- `READY` = dependencies and entry criteria are satisfied.
- `VALIDATION` = execution is complete enough for independent checks.
- `HUMAN DECISION` = evidence is ready but human authority is required.
- `REMEDIATION REQUIRED` = a required condition failed or remains unsatisfied.
- `DONE` = closure criteria and evidence are complete.

Avoid vague statuses like “Almost Done.”

### 4.3.1 Status Integrity Is Defined Here

Chapter 4 is the authoritative source for status semantics and status-integrity rules. Chapter 6 defines completion evidence for work types; Chapter 9 implements those rules in tools.

A transition that makes a governed claim—such as `VALIDATED`, `APPROVED_FOR_RELEASE`, `RELEASED`, `DONE`, `DEPLOYED`, or `OPERATIONAL`—must carry the evidence required for that claim. Routine flow transitions must at minimum remain traceable in the source-of-truth system.

## 4.4 Historical Results

Historical validation and remediation results should be append-only or otherwise preserved.

Example:

```yaml
history:
  - event: validation
    result: FAIL
    id: VAL-104
  - event: remediation
    result: PASS
    id: REM-105
current_state: APPROVED_FOR_RELEASE
```

## 4.5 Change Control

A controlled change should pass through:

```text
Define → Assess → Authorize → Implement → Test → Validate → Approve → Version → Deploy → Monitor
```

Not every low-risk change requires a formal ceremony at each step, but the semantic checks should exist.

## 4.6 Re-Baselining

A baseline may change when new information makes the original baseline invalid or suboptimal.

Re-baselining requires:

- proposed change;
- reason;
- impact;
- affected commitments;
- authority level;
- decision;
- new baseline version.

Backlog reprioritization within an approved boundary is not necessarily re-baselining.

## 4.7 Exception Model

Exceptions should include:

- exception ID;
- control being bypassed or deferred;
- rationale;
- risk;
- scope;
- compensating control;
- owner;
- expiry;
- human approval where required.

An exception is not a hidden shortcut.

## 4.7.1 Escalation Ownership

GAD separates three concerns:

- **Chapter 7** defines technical and AI-related escalation **triggers**.
- **Chapter 8** defines the evidence/risk **decision procedure**.
- **Chapter 4** defines organizational **ownership** of the escalation.

| Escalation type | Primary owner | Required human involvement |
|---|---|---|
| Flow/dependency blockage | Delivery Lead / work owner | As needed for commitment change |
| Evidence or validation insufficiency | Validator / Evidence Owner | Human decision when consequential |
| A3/A4 authorization | Human Project Hub or named authority | Mandatory |
| Security/privacy/compliance concern | Applicable specialist control owner | Mandatory where policy requires |
| Authority/tool/data-scope expansion | Human Project Hub / enterprise authority | Mandatory; usually A4 |
| Repeated or systemic control failure | Governance owner | Human review and change decision |

Turnaround targets are defined by local policy and severity. GAD does not invent a universal SLA.

Cross-reference: [`escalation-protocol.md`](templates/escalation-protocol.md).

## 4.7.2 Retention and Audit-Trail Requirements

Decision, evidence, authorization, exception, incident, and release records must be retained for the period required by applicable law, regulation, contract, enterprise policy, audit need, and data-minimization rules.

The control design should specify record class, owner, retention basis, access/export permissions, deletion/archival authority, and legal-hold or incident exceptions. GAD intentionally does not prescribe a universal duration.

## 4.7.3 Policy as Code

Stable governance rules should be version-controlled and tested when practical.

```text
A3/A4 + no valid approval → block release
mandatory evidence incomplete → block governed status promotion
expired delegation → block A2 execution
```

See [Chapter 12](chapter_12.md) for enterprise policy-as-code scaling.

## 4.8 Remediation Model

`REMEDIATION_REQUIRED` is a control outcome, not an embarrassment.

A remediation record should show:

- original failure;
- root cause;
- corrective action;
- validation of corrective action;
- residual limitations;
- closure authority.

See [`incident_and_remediation_template.md`](templates/incident_and_remediation_template.md).

## 4.9 Agent Lifecycle State Machine — Authoritative

```text
PROPOSED
  ↓
SPECIFIED
  ↓
IMPLEMENTED
  ↓
TESTED
  ↓
VALIDATED
  ↓
DEPLOYED
  ↓
OPERATIONAL
  ↓
RETIRED
```

Each transition must be supported by evidence appropriate to the status claim.

| Transition | Minimum evidence concept |
|---|---|
| PROPOSED → SPECIFIED | accepted specification boundary |
| SPECIFIED → IMPLEMENTED | implementation identity and change evidence |
| IMPLEMENTED → TESTED | test execution and results |
| TESTED → VALIDATED | validation against governed acceptance criteria |
| VALIDATED → DEPLOYED | deployment identity and authorization |
| DEPLOYED → OPERATIONAL | operational-readiness evidence and monitoring |
| Any → RETIRED | retirement decision, access/delegation revocation, evidence preservation |

A lower historical result must not be overwritten merely to simplify reporting.

## 4.10 Authorization Changes Are Changes

Changing an agent's authority ceiling, tool access, client scope, data class, or autonomous execution boundary is itself a governed change—typically A3 or A4.

## 4.11 Policy Hierarchy

A common hierarchy:

```text
Law / Regulation
    ↓
Enterprise Policy
    ↓
Program / Portfolio Governance
    ↓
GAD Method Configuration
    ↓
Project Controls
    ↓
Agent / Tool Configuration
    ↓
Individual Work Item
```

Lower layers may be stricter but should not weaken higher requirements.

## Cross-References

- Foundations: [Chapter 1](chapter_01.md)
- Authorization: [Chapter 2](chapter_02.md)
- Stage gates: [Chapter 5](chapter_05.md)
- Exceptions and evidence: [Chapter 8](chapter_08.md)

[Back to outline](outline.md)
