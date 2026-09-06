# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 8 — Decision Logic, Risk, Evidence, and Exceptions
**Estimated reading time:** approximately 4 minutes

## Purpose

GAD uses a compact decision model so that every material action can be assessed consistently before execution.

## 8.1 The Five-Question Decision Model

### Q1 — What action is actually being proposed?

Describe the action, not the intention.

Weak:

```text
Improve deployment.
```

Better:

```text
Deploy release 1.8.4 to production environment EU-PROD-1.
```

### Q2 — Who is authorized to perform and approve it?

Determine:

- actor;
- authorization level;
- delegation source;
- approver if required;
- scope and expiry.

### Q3 — What is the consequence and reversibility?

Assess:

- external impact;
- financial impact;
- data sensitivity;
- security impact;
- legal/regulatory significance;
- irreversibility;
- blast radius.

### Q4 — Is the evidence sufficient and are dependencies satisfied?

Check:

- acceptance criteria;
- test result;
- validation;
- linked evidence;
- required approvals;
- unresolved blockers;
- known deviations.

### Q5 — What happens if it fails?

Define:

- stop condition;
- rollback;
- recovery;
- escalation;
- monitoring;
- residual limitation.

If any answer is materially incomplete, the action should not cross the relevant control boundary.

## 8.2 Risk Dimensions

GAD does not require a universal numeric risk score. A qualitative model is often more robust.

Suggested dimensions:

- consequence;
- likelihood;
- reversibility;
- scope;
- sensitivity;
- novelty;
- uncertainty;
- dependency complexity.

## 8.3 Evidence Classes

A practical evidence model:

| Evidence Class | Examples |
|---|---|
| E0 — Source | requirement, policy, design, issue |
| E1 — Execution | command result, change record, commit |
| E2 — Test | automated test, manual test, validation |
| E3 — Approval | human decision, risk acceptance |
| E4 — Release | deployment/release record |
| E5 — Operations | monitoring, health, incident-free observation |
| E6 — Audit | control review, traceability check |

## 8.4 Evidence Sufficiency

Evidence is sufficient when it is adequate to support the claim being made.

For example:

- a screenshot that a button exists may support UI existence;
- it does not prove role permissions for all users;
- a passing unit test supports code behavior under test conditions;
- it does not prove production operational readiness.

### 8.4.1 Evidence-Sufficiency Rubric

| Quality | Question |
|---|---|
| Provenance | Can the source, actor, system, or artifact identity be established? |
| Relevance | Does the evidence directly support the claim being made? |
| Recency | Is it current enough for the decision context? |
| Independence | Is consequential validation sufficiently separated from the executor/claimant? |
| Completeness | Are all mandatory evidence categories present? |
| Reproducibility | Can a qualified reviewer repeat or verify the essential result where practical? |

A package can contain many files and still be insufficient if a mandatory category is missing. Use `SUFFICIENT`, `PARTIAL`, or `INSUFFICIENT` in [`evidence_package_template.md`](templates/evidence_package_template.md).

## 8.5 Evidence Package

A human-readable evidence package should separate:

- technical result;
- evidence sufficiency;
- deviations;
- residual limitations;
- readiness assessment;
- approval decision;
- later promotion or release decision.

See [`evidence_package_template.md`](templates/evidence_package_template.md).

## 8.6 Decision Record

Decision record fields:

- decision ID;
- question;
- options;
- evidence;
- risks;
- recommendation;
- decision;
- approver;
- date/time;
- conditions;
- expiry/review date if applicable.

See [`decision_record_template.md`](templates/decision_record_template.md).

### 8.6.1 Decision-Record Schema and Version

Every decision record should identify its template/schema version so historical approvals can be interpreted against the rules in force at the time.

Cross-reference: [`decision_record_template.md`](templates/decision_record_template.md).

Do not silently migrate old decisions to a new schema in a way that changes their historical meaning.

## 8.7 Controlled Failure

A governed test may intentionally demonstrate safe failure.

A valid controlled-failure case should:

- use bounded non-sensitive input;
- state expected failure;
- prove no unauthorized side effect;
- record actual result;
- verify cleanup/recovery;
- preserve the failure result.

### 8.7.1 Blast Radius and Reversibility Bounds

Before an intentional failure or consequential change, define systems/work items affected, maximum data/financial/security exposure, maximum duration, stop trigger, human checkpoint, and rollback/recovery path.

If the expected blast radius is not bounded tightly enough for the authorization level, reclassify or escalate before execution.

Cross-reference: [`change-impact-assessment.md`](templates/change-impact-assessment.md).

## 8.8 Exception Handling

An exception should answer:

```text
What control is not satisfied?
Why is an exception needed?
What is the risk?
What compensating control exists?
Who approved it?
When does it expire?
How will it be closed?
```

### 8.8.1 Exception Expiry and Post-Exception Review

Every exception must have an owner and an expiry/review point. At expiry, close it, renew it through a new/updated decision, convert it into a governed control change, or escalate unresolved risk.

Expired exceptions do not remain valid by default.

Cross-reference: [`EXCEPTION_REGISTER.csv`](templates/EXCEPTION_REGISTER.csv).

## 8.9 Remediation

When a mandatory control fails:

```text
Current outcome = REMEDIATION_REQUIRED
```

Remediation should target the exact failure, not broaden authority.

After remediation:

```text
Historical failure = preserved
Remediation validation = recorded
Current readiness = reassessed
```

## 8.10 Readiness Outcomes

GAD favors explicit readiness labels.

Examples:

- `READY_FOR_VALIDATION`
- `READY_FOR_HUMAN_DECISION`
- `READY_FOR_RELEASE_AUTHORIZATION`
- `READY_FOR_PILOT_AUTHORIZATION`
- `REMEDIATION_REQUIRED`
- `BLOCKED_BY_DEPENDENCY`
- `EVIDENCE_INSUFFICIENT`

## Cross-References

- Foundations: [Chapter 1](chapter_01.md)
- Authorization: [Chapter 2](chapter_02.md)
- Pilot readiness: [Chapter 10](chapter_10.md)
- Audit: [Chapter 11](chapter_11.md)

[Back to outline](outline.md)
