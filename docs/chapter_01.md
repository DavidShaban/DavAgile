# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 1 — Foundations and Core Principles
**Estimated reading time:** approximately 5 minutes

## Purpose

This chapter defines the non-negotiable ideas that make GAD a governed methodology rather than simply an AI-enabled Agile process.

## 1.1 Deliberate Planning, Adaptive Execution

GAD separates **baseline commitments** from **execution choices**.

Baseline commitments may include:

- business outcome and success measures;
- regulatory and security obligations;
- funding boundaries;
- contractual commitments;
- major architecture constraints;
- milestone windows;
- externally committed release dates;
- policy-required approvals.

Execution choices may adapt through:

- backlog reprioritization;
- iteration scope;
- implementation technique;
- task sequencing;
- experiments;
- automation choices within an approved boundary.

This distinction prevents normal Agile adaptation from being mistaken for permission to change commitments that require governance.

## 1.2 Human Authority Is Explicit

Human authority is not inferred from organizational role names, AI confidence, task urgency, or tool access.

GAD requires the delivery system to answer:

- Who may decide?
- Who may execute?
- Under what conditions?
- For what scope?
- For how long?
- What evidence proves the authorization?

See [Chapter 2](chapter_02.md).

## 1.3 Authority Before Autonomy

A system may be technically capable of acting and still be unauthorized.

GAD therefore treats these concepts separately:

- **Capability** — can the actor perform the action?
- **Permission** — does the actor have access?
- **Authorization** — is the actor allowed to perform this action in this context?
- **Autonomy** — may the actor perform it independently inside the authorized boundary?

Autonomy never creates authority by itself.

## 1.4 Evidence Before Promotion

A work item, agent, release, or control does not become “validated,” “approved,” “deployed,” or “operational” because someone intends it to be.

Status promotion requires evidence appropriate to the claim.

Examples:

- `TESTED` requires test evidence.
- `VALIDATED` requires validation evidence.
- `APPROVED` requires an identifiable decision.
- `RELEASED` requires release evidence.
- `OPERATIONAL` requires operational-readiness evidence.

## 1.5 Fail Closed

When a mandatory condition is missing, GAD blocks or escalates rather than guessing.

Typical fail-closed triggers:

- missing approval;
- missing evidence;
- failed validation;
- unresolved dependency;
- scope mismatch;
- expired authorization;
- WIP limit breach;
- ambiguous ownership;
- unavailable recovery path for a high-impact change.

Fail-closed does not mean “stop the whole project.” It means **do not cross the affected control boundary** until the condition is resolved.

## 1.6 Preserve Historical Truth

Historical execution results remain historical facts.

If a work item failed validation and later a remediation passed:

```text
Original result: FAIL
Remediation result: PASS
Current readiness: ACCEPTED
```

GAD does not rewrite the original `FAIL` into `PASS`.

This enables meaningful audit, learning, and root-cause analysis.

## 1.7 Separate Recommendation from Decision

AI may often recommend:

- priority changes;
- risk responses;
- scope options;
- release timing;
- mitigation actions.

A recommendation does not become approval unless the required authorization model says it does.

## 1.8 Proportional Governance

GAD is not “maximum control everywhere.”

Controls should be proportional to:

- consequence;
- reversibility;
- external impact;
- sensitivity;
- uncertainty;
- novelty;
- dependency complexity;
- legal/regulatory significance.

Low-impact work should remain fast. High-impact work should remain controlled.

## 1.9 Traceability by Design

A consequential outcome should be traceable through:

```text
Need → Work Item → Authorization → Change → Validation → Evidence → Decision → Release → Monitoring
```

Where possible, this trace should be machine-queryable.

## 1.10 Recovery Is Part of Delivery

A plan for success without a plan for failure is incomplete.

For meaningful changes GAD asks:

- Can the change be reversed?
- What would trigger rollback?
- Who may initiate recovery?
- What evidence proves recovery?
- What residual effect remains after recovery?

## 1.11 Human Attention Is a Scarce Resource

Human review should be reserved for decisions where human authority or judgment adds value.

AI should prepare concise, evidence-linked decision packages rather than transferring raw operational noise to the Human Project Hub.

## 1.12 Control Outcomes

A well-configured GAD system should make these outcomes observable:

- unauthorized consequential actions: zero;
- missing approval evidence for A3/A4 actions: zero;
- historical failures preserved;
- active queues exclude completed historical records;
- remediation status visible;
- release decisions traceable;
- exceptions measurable;
- AI authority expansion explicit, never silent.

## 1.13 Principles → Mechanisms Traceability

| Principle | Primary mechanism | Tool/artifact cross-reference |
|---|---|---|
| Deliberate planning, adaptive execution | Baselines, stage gates, Agile flow | [Chapters 5–6](chapter_05.md), [`PILOT_GATE_REGISTER.csv`](templates/PILOT_GATE_REGISTER.csv) |
| Human authority is explicit | A0–A4, Human Decision, decision records | [Chapter 2](chapter_02.md), [`AUTHORIZATION_MATRIX.csv`](templates/AUTHORIZATION_MATRIX.csv), [`AUTHORIZATION_GRANT_REGISTER.csv`](templates/AUTHORIZATION_GRANT_REGISTER.csv) |
| Authority before autonomy | Agent authority ceilings and scope controls | [Chapter 3](chapter_03.md), [`MODEL_AGENT_REGISTRY.yaml`](templates/MODEL_AGENT_REGISTRY.yaml) |
| Evidence before promotion | Evidence gates, validation, status integrity | [Chapters 4 and 8](chapter_04.md), [`evidence_package_template.md`](templates/evidence_package_template.md) |
| Fail-closed delivery | Block/remediate/escalate on missing mandatory conditions | [Chapters 4, 7, and 8](chapter_04.md), [`escalation-protocol.md`](templates/escalation-protocol.md) |
| Preserve historical truth | History-preserving results and remediation | [Chapter 4](chapter_04.md), [`incident_and_remediation_template.md`](templates/incident_and_remediation_template.md) |
| Proportional governance | Risk/reversibility-based controls and federated scaling | [Chapters 8 and 12](chapter_08.md) |
| Traceability by design | Stable IDs and evidence links | [Chapter 9](chapter_09.md), [Appendix F](appendix_f_reference_configurations.md) |

## 1.14 Principle-Conflict Resolution

When principles appear to conflict, apply this precedence:

1. applicable law, regulation, contract, and enterprise policy;
2. explicit human authority and prohibited-action boundaries;
3. safety, security, privacy, and data-scope controls;
4. evidence sufficiency and status integrity;
5. approved project/program commitments;
6. flow efficiency and optimization.

A lower-priority objective must not silently override a higher-priority control. If a conflict remains material, route it to the appropriate human authority using the decision process in [Chapter 8](chapter_08.md).

## 1.15 Operational Meaning of Fail-Closed

**Fail-closed delivery** means that when a mandatory authorization, validation, evidence, dependency, tool-contract, or scope condition is unknown or unsatisfied, the affected action does not cross that boundary.

```text
STOP affected action
→ preserve current state
→ capture reason/evidence
→ classify blocker
→ escalate if needed
→ resume only after the blocking condition is resolved
```

Fail-closed is scoped: it should stop the unsafe or unauthorized action, not automatically freeze unrelated work.

## Cross-References

- Authorization matrix: [`templates/AUTHORIZATION_MATRIX.csv`](templates/AUTHORIZATION_MATRIX.csv)
- Lifecycle and status integrity: [Chapter 4](chapter_04.md)
- Evidence and exceptions: [Chapter 8](chapter_08.md)
- Metrics: [Chapter 11](chapter_11.md)

[Back to outline](outline.md)
