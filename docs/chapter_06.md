# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 6 — Agile Execution and Flow Control
**Estimated reading time:** approximately 4 minutes

## Purpose

GAD uses Agile and flow-based practices for execution inside the approved planning and authorization boundaries.

## 6.1 Backlog Architecture

Recommended layers:

```text
Outcome / Initiative
  └─ Epic / Capability
      └─ Feature / Deliverable
          └─ Story / Work Item
              └─ Task / Subtask
```

Every level should preserve traceability to the outcome and applicable controls.

## 6.2 Definition of Ready

A work item is `READY` when enough is known to start safely.

Typical criteria:

- objective clear;
- acceptance criteria clear;
- dependencies resolved or explicitly manageable;
- authorization level classified;
- required data access approved;
- owner identified;
- validation method known;
- required evidence known.

A2/A3/A4 work should not enter execution if required delegation or approval is missing.

## 6.3 Iterations and Kanban

GAD supports Scrum, Kanban, Scrumban, or another Agile execution model.

The essential controls are:

- transparent priorities;
- WIP discipline;
- short feedback cycles;
- visible blocked work;
- inspect-and-adapt;
- evidence-based completion.

## 6.4 WIP Limits

WIP limits protect throughput and reduce hidden risk.

Example:

```text
IN PROGRESS — WIP 4
VALIDATION — WIP 3
HUMAN DECISION — no numeric limit, but aging alert after agreed threshold
```

If a WIP limit is breached, the default response is to finish or unblock before starting more work.

### 6.4.1 Aging-WIP Policy

A WIP limit controls **quantity**; an aging policy controls **time**. For each active state, define a warning age, escalation age, owner, and expected response.

```text
age < warning threshold → normal
warning threshold reached → surface on dashboard
escalation threshold reached → owner review / unblock / re-plan
```

Aging does not automatically imply failure. It is a trigger for attention and, when material, for the escalation process in Chapters 4, 7, and 8.

## 6.5 Validation as Part of Flow

Validation is not a final phase added after “development is done.”

For each work item define:

- acceptance test;
- policy check;
- evidence requirement;
- reviewer/validator;
- expected failure handling.

## 6.6 Definition of Done

A GAD Definition of Done may require:

- acceptance criteria passed;
- tests passed;
- required review complete;
- evidence linked;
- authorization satisfied;
- documentation updated;
- monitoring or recovery requirement satisfied;
- work item status consistent with actual outcome.

For A3/A4, “implemented” is not equivalent to “authorized for release.”

### 6.6.1 Definition of Done by Work-Item Type

| Work type | Minimum evidence examples |
|---|---|
| Documentation | source/provenance links, review/validation result, publication approval if external |
| Software change | code/commit identity, tests, review, evidence package, release approval if consequential |
| Configuration change | before/after config identity, validation, rollback, approval where required |
| AI/agent change | model/agent/prompt/config version, tests, scope/authority validation, monitoring |
| Governance/policy change | change request, impact assessment, decision record, version/migration note |
| Pilot control change | control test evidence, dashboard/filter result, readiness impact |

Evidence should begin accumulating during execution; the team should not wait until `DONE` to discover it cannot prove completion.

Cross-reference: [`pilot_readiness_checklist.md`](templates/pilot_readiness_checklist.md).

### 6.6.2 Throughput vs. Quality

GAD does not optimize cycle time at the expense of mandatory evidence or quality. Preserve mandatory controls first, then automate/simplify stable controls, reduce unnecessary handoffs, and tune WIP/capacity. Change a control only through governed change.

## 6.7 Reviews

Iteration reviews should inspect:

- outcome progress;
- accepted value;
- quality;
- dependency changes;
- control exceptions;
- AI contribution;
- evidence completeness.

## 6.8 Retrospectives

Retrospectives include both delivery and governance questions:

- Which controls prevented a problem?
- Which controls created delay without value?
- Where did AI reduce manual effort?
- Where did AI create noise or uncertainty?
- Were escalations timely?
- Did any role boundary become ambiguous?
- Which rule should change?

## 6.9 Flow Metrics

Recommended metrics:

- cycle time;
- lead time;
- throughput;
- WIP;
- blocked time;
- validation failure rate;
- remediation rate;
- decision latency;
- evidence completion latency.

See [Chapter 11](chapter_11.md).

## 6.10 AI in Agile Execution

AI may:

- refine work items;
- identify duplicates;
- draft acceptance criteria;
- propose decomposition;
- summarize review evidence;
- flag aging work;
- predict milestone risk.

AI should not silently:

- expand scope;
- accept work;
- approve risk;
- release A3/A4 changes.

## Cross-References

- Authorization: [Chapter 2](chapter_02.md)
- AI execution: [Chapter 7](chapter_07.md)
- Metrics: [Chapter 11](chapter_11.md)

[Back to outline](outline.md)
