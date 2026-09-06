# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 10 — Pilot Setup and Governed Execution
**Estimated reading time:** approximately 5 minutes

## Purpose

A GAD pilot proves that the governance model works in practice before broader adoption or autonomous execution is expanded.

## 10.1 Pilot Objective

A pilot should validate:

- work-item flow;
- authorization classification;
- human approval gates;
- evidence traceability;
- agent boundaries;
- fail-closed behavior;
- remediation;
- dashboard visibility;
- release/closure control;
- human usability.

## 10.2 Pilot Scope

Prefer a pilot that is:

- bounded;
- meaningful but not mission-critical;
- measurable;
- representative of real work;
- recoverable;
- safe for controlled failure testing;
- limited in data sensitivity until controls are proven.

## 10.2.1 Pilot Success, Failure, and Kill Criteria

Define these **before execution**.

### Success criteria
- every mandatory pilot-control gate passes;
- unauthorized A3/A4 execution is zero;
- mandatory evidence completeness is 100%;
- human-decision and remediation paths work as designed;
- agreed delivery/quality KPIs are measured;
- no unresolved critical control blocker remains.

### Failure / hold criteria
The pilot remains in remediation/hold when a mandatory control fails, required evidence is insufficient, a prerequisite remains unresolved, or the control design is too noisy/ineffective to trust.

### Kill criteria
Suspend or terminate when an uncontrolled high-impact action occurs, sensitive data is processed outside scope, required recovery cannot be demonstrated, or the governance system cannot reliably block prohibited actions.

## 10.2.2 Pilot Data-Collection Plan

Before start, select Chapter 11 KPIs and record baseline/reference period, owner, source system, collection cadence, success threshold, and pilot end-point comparison.

Cross-reference: [`PILOT_REPORT_TEMPLATE.md`](templates/PILOT_REPORT_TEMPLATE.md).

## 10.2.3 Duration and Formal Sign-Off

Set a maximum planned duration or bounded number of work items/iterations. Extension requires explicit review. The Human Project Hub and any required specialist/sponsor authority formally close the pilot.

## 10.3 Preflight

Before starting:

- scope approved;
- participants identified;
- Human Project Hub identified;
- tools configured;
- private/role-restricted control views validated;
- authorization matrix loaded;
- workflow transitions tested;
- evidence repository available;
- recovery approach defined;
- no unresolved prerequisite marked as mandatory.

## 10.4 Reference Pilot Gates

| Gate | Outcome |
|---|---|
| P0 — Identity & Scope | Pilot identity, owner, boundary, source-of-truth confirmed |
| P1 — Authorization | A0–A4 model implemented and tested |
| P2 — Workflow | States, validators, blocked/remediation paths work |
| P3 — AI Boundary | Agent permissions and escalation behavior validated |
| P4 — Evidence | Required evidence can be captured and traced |
| P5 — Human Control | Dashboard/queues expose all decision and exception states |
| P6 — Recovery | Failure and recovery path demonstrated |
| P7 — Readiness | All mandatory gates pass for pilot authorization |

See [`pilot_readiness_checklist.md`](templates/pilot_readiness_checklist.md).

## 10.4.1 Pilot Gates vs. Delivery Gates

- **Chapter 5 delivery gates** govern the lifecycle of a deliverable or release.
- **Chapter 10 pilot gates** test whether the GAD control system is working well enough to authorize the pilot or wider adoption.

A pilot may contain delivery work that passes Chapter 5 gates while the overall pilot still fails a Chapter 10 control gate.

## 10.5 Human Control Dashboard

A reference dashboard may include nine private filter-result views:

1. **Human Decision Required**
2. **A3/A4 Awaiting Approval**
3. **Evidence Missing**
4. **Validation Failed**
5. **Remediation Required**
6. **Dependency Blocked**
7. **WIP / Flow Exceptions**
8. **Ready for Release Authorization**
9. **Unauthorized / Policy Exception Signals**

The dashboard should not replace the source-of-truth issue records.

## 10.6 Privacy of Control Views

Control filters and dashboards may expose:

- risks;
- pending approvals;
- audit findings;
- internal exceptions;
- operational details.

They should therefore be shared only with authorized roles during a controlled pilot.

## 10.7 Historical Records

A pilot should explicitly test that:

- completed historical records do not remain in active queues;
- historical failure/remediation results remain discoverable;
- remediation does not rewrite original outcomes;
- filters query current state correctly.

This is important because a dashboard can appear unhealthy simply because historical truth was mixed with active operational state.

## 10.8 Synthetic Validation

Before using sensitive or consequential data, test with synthetic cases where possible.

Synthetic cases can validate:

- transition guards;
- A3/A4 approval blocking;
- failed validation path;
- evidence-missing path;
- remediation path;
- recovery;
- dashboard queues.

## 10.9 Pilot Decision Logic

The final readiness review is control-by-control.

Example:

```markdown
| Control | Result | Evidence | Blocking? |
|---|---|---|---|
| Authorization classification | PASS | EVID-001 | No |
| A3 approval bypass test | PASS | EVID-002 | No |
| Dashboard privacy | PASS | EVID-003 | No |
| Historical queue exclusion | FAIL | EVID-004 | Yes |
```

## 10.10 Final Outcomes

If every mandatory gate passes:

```text
READY_FOR_PILOT_AUTHORIZATION
```

If any mandatory gate fails or a prerequisite remains unresolved:

```text
REMEDIATION_REQUIRED
```

The remediation outcome should identify exact blockers and required evidence.

## 10.11 Pilot Authorization Is Not Unlimited Autonomy

Passing a pilot does not automatically authorize:

- wider data access;
- production use beyond scope;
- additional agents;
- new tools;
- A4 autonomy;
- cross-project execution.

Each expansion is a new governed decision.

## 10.12 Pilot Exit

A pilot exit package should include:

- gate register;
- exceptions;
- decisions;
- evidence index;
- metrics;
- usability feedback;
- incidents/remediations;
- lessons learned;
- scale recommendation.

## 10.12 Pilot Outcome Decision

Readiness to start and the decision after the pilot are separate. At pilot end, record one recommendation:

- `SCALE_RECOMMENDED`;
- `HOLD_AND_REMEDIATE`;
- `DO_NOT_SCALE`;
- `PILOT_TERMINATED`.

These outcomes do not silently grant new agent authority.

## Cross-References

- Authorization: [Chapter 2](chapter_02.md)
- Tooling: [Chapter 9](chapter_09.md)
- Metrics: [Chapter 11](chapter_11.md)
- Case study: [Appendix D](appendix_d_case_studies.md)

[Back to outline](outline.md)
