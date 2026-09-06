# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 5 — Waterfall Planning and Stage Gates
**Estimated reading time:** approximately 4 minutes

## Purpose

GAD retains Waterfall where predictability and explicit commitments matter. The goal is not to specify every task up front; it is to stabilize the boundaries that must not drift casually.

## 5.1 Planning Objects

A GAD baseline typically includes:

- business objective;
- measurable outcomes;
- scope boundaries;
- assumptions;
- constraints;
- architecture baseline;
- compliance/security baseline;
- budget or capacity envelope;
- milestone map;
- dependency map;
- release strategy;
- authorization model;
- pilot/production gate model.

## 5.2 Milestone Planning

Milestones should represent meaningful decision or outcome points.

Good milestone:

```text
Pilot readiness gate passed with complete A3/A4 authorization evidence
```

Weak milestone:

```text
Phase 2 complete
```

unless “Phase 2 complete” has objective exit criteria.

## 5.3 Stage Gates

A generic GAD gate sequence:

| Gate | Question |
|---|---|
| G0 | Is the initiative sufficiently defined to begin governed planning? |
| G1 | Are scope, authority, dependencies, and controls defined? |
| G2 | Is the solution/design ready for implementation? |
| G3 | Is implementation ready for integrated validation? |
| G4 | Is evidence sufficient for release decision? |
| G5 | Is the release authorized? |
| G6 | Is operational evidence sufficient for closure/scale? |

Organizations may rename or combine gates.

### 5.3.1 Delivery-Gate Entry and Exit Criteria

These are **delivery lifecycle gates**. They are different from the pilot-control gates in [Chapter 10](chapter_10.md), which validate whether the GAD control system itself is ready.

| Gate | Entry criteria | Exit criteria | Required evidence | Default owner |
|---|---|---|---|---|
| G0 — Initiative Definition | problem/outcome identified | scope, owner, constraints sufficient for governed planning | charter/intent record | Sponsor / Human Project Hub |
| G1 — Governance Ready | baseline draft exists | authority, data, dependencies, controls defined | authorization model, dependency/risk records | Delivery + Governance |
| G2 — Design Ready | requirements/constraints understood | design/architecture/compliance decisions adequate for implementation | design and control evidence | Technical/Domain authority |
| G3 — Validation Ready | implementation substantially complete | integrated validation can run against frozen criteria | implementation identity, test plan | Delivery/Validation |
| G4 — Release Decision Ready | validation completed | evidence package sufficient for decision | validation, risk, recovery, evidence package | Evidence/Validation owner |
| G5 — Release Authorized | decision-ready package complete | valid release approval exists | decision record | Named release authority |
| G6 — Operational Closure/Scale | release executed | monitoring/operational evidence supports closure or next scale decision | operational evidence, incidents/remediations | Human Project Hub / Operations |

### 5.3.2 Risk-Register Integration

Risks discovered at gates must enter the project risk process rather than remain hidden inside gate notes. Cross-reference: [`RISK_REGISTER.csv`](templates/RISK_REGISTER.csv).

A material unresolved risk becomes an input to the [Chapter 8](chapter_08.md) decision model.

### 5.3.3 Baseline Freeze

A baseline is considered frozen when its governing decision is recorded. After freeze, adaptive execution may continue inside the approved tolerance; changes outside tolerance use change control; material commitment changes require re-baselining.

## 5.4 Gate Record

Each gate should record:

- gate ID;
- date;
- owner;
- required evidence;
- evidence present;
- exceptions;
- decision;
- decision authority;
- next authorized stage.

For a reusable gate-register pattern, see [`PILOT_GATE_REGISTER.csv`](templates/PILOT_GATE_REGISTER.csv); despite its historical filename, Documentation Release 1.1 also uses its schema as a reference pattern for explicit gate evidence and ownership.

## 5.5 Dependencies

Dependencies are treated as governed conditions, not footnotes.

Classify dependencies:

- internal work item;
- external vendor;
- architecture decision;
- legal/compliance decision;
- data availability;
- environment;
- human approval;
- other project/program.

A dependency that blocks authorization should surface in a control queue.

## 5.6 Budget and Capacity

Budget and capacity should have explicit tolerance rules.

Example policy:

```text
Within approved team capacity and no material commitment change → adapt in backlog
Forecast breach above defined tolerance → escalate for re-baseline
New external spend outside delegated authority → A3
Material contractual spend or strategic commitment → A4 where policy requires
```

Thresholds are organization-specific.

## 5.7 Architecture and Compliance

Architecture and compliance decisions belong early enough to shape delivery but should be revisited when assumptions change.

A gate should not become a one-time checkbox that remains “passed” after material scope change.

## 5.8 Release Planning

Release plans should define:

- release objective;
- target window;
- minimum evidence;
- approval authority;
- rollback/recovery requirement;
- monitoring period;
- post-release review.

## 5.9 Re-Baselining Triggers

Common triggers:

- material scope change;
- new regulation;
- new data class;
- cost or schedule variance beyond tolerance;
- architecture constraint failure;
- critical dependency slip;
- unacceptable quality trend;
- risk that exceeds approved appetite.

## 5.10 Waterfall Without Over-Specification

GAD does not require a detailed task plan months in advance.

It requires enough up-front definition to know:

- what must remain stable;
- what may adapt;
- who may authorize a change;
- what evidence is required.

## Cross-References

- Agile adaptation within baselines: [Chapter 6](chapter_06.md)
- Risk prediction: [Chapter 7](chapter_07.md)
- Pilot gates: [Chapter 10](chapter_10.md)
- Gate register: [`templates/PILOT_GATE_REGISTER.csv`](templates/PILOT_GATE_REGISTER.csv)

[Back to outline](outline.md)
