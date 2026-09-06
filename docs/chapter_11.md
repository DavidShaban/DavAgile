# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 11 — Metrics, Evidence, Assurance, and Audit
**Estimated reading time:** approximately 4 minutes

## Purpose

GAD measures both delivery performance and governance effectiveness. A fast delivery system with weak authority controls is not successful; a perfectly controlled system that cannot deliver value is not successful either.

## 11.1 Metric Families

### Delivery
- lead time;
- cycle time;
- throughput;
- predictability;
- blocked time;
- WIP.

### Quality
- validation pass rate;
- defect escape rate;
- rework;
- remediation rate;
- rollback frequency.

### Governance
- unauthorized A3/A4 attempts;
- approval bypass attempts;
- missing approval evidence;
- evidence completeness;
- exception aging;
- decision latency;
- policy violation rate.

### AI
- automation contribution;
- human override rate;
- false alert rate;
- validation disagreement rate;
- AI-induced rework;
- confidence calibration where measurable.

### Outcome
- business outcome progress;
- customer/user impact;
- time to value;
- budget outcome;
- reliability/adoption.

See [`KPI_CATALOG.csv`](templates/KPI_CATALOG.csv).

## 11.1.1 Four Required Coverage Categories

| Category | Required named metrics |
|---|---|
| Delivery speed | cycle time (median/P85 where useful), throughput |
| AI error | AI rejection/error rate, AI-induced rework |
| Governance compliance | evidence-completeness compliance, unauthorized-action rate, on-time approval |
| Remediation time | mean/median time from detection to contained/closed state |

## 11.1.2 Leading Indicators

1. **AI confidence trend by agent/work class** — early warning only; confidence never grants authority.
2. **Evidence-attachment rate at Ready / early execution** — percentage of active governed items already carrying required evidence links.

## 11.1.3 Lagging Indicators

1. **Change failure rate / release defect density**.
2. **Unauthorized-action rate per 1,000 work items**, with a target of zero for unauthorized consequential execution.

## 11.2 Recommended Control Targets

Some targets should be absolute:

```text
Unauthorized A3/A4 execution = 0
A3/A4 releases without required approval evidence = 0
Silent authority expansion = 0
Historical failure rewriting = 0
```

Other thresholds should be locally calibrated:

- evidence completeness;
- WIP compliance;
- decision latency;
- cycle time;
- remediation aging.

## 11.3 Evidence Completeness

Evidence completeness should be calculated against required evidence, not the number of available attachments.

Example:

```text
Required:
- test result
- approval
- recovery plan
- release record

Present:
- test result
- approval
- release record

Completeness = 3 / 4 = 75%
```

## 11.4 Audit Completeness

An audit sample should be able to trace:

```text
Requirement
→ Work Item
→ Authorization
→ Change
→ Validation
→ Evidence
→ Decision
→ Release
→ Monitoring
```

Broken links are findings.

## 11.4.1 Metric Ownership, Provenance, and Alerting

Every governed KPI should define owner, data source/provenance, calculation, review cadence, threshold/interpretation, alert recipient, and expected action when the threshold is breached.

The KPI catalog itself is version-controlled and reviewed at least quarterly during active use.

Cross-reference: [`KPI_CATALOG.csv`](templates/KPI_CATALOG.csv) and [`KPI_DASHBOARD.yaml`](templates/KPI_DASHBOARD.yaml).

## 11.5 Control Testing

Controls should be tested, not merely documented.

Examples:

- attempt prohibited transition;
- attempt release without approval;
- test dashboard permission;
- test expired delegation;
- test missing evidence;
- test completed historical item exclusion;
- test rollback.

## 11.6 Sampling Strategy

Sampling may be:

- risk-based;
- random;
- milestone-based;
- exception-driven;
- full-population for high-impact A3/A4 actions.

## 11.6.1 Audit-Sampling Method

The audit plan must state population, sampling period, sample size, selection method, A-level stratification, reason for denser sampling of higher-consequence work, findings, and follow-up.

Where an assurance statement makes a statistical population claim, document the chosen confidence level, margin of error, assumptions, and sampling method. Otherwise, describe the sample as **risk-based evidence**, not statistically representative evidence.

Cross-reference: [`AUDIT_SAMPLE_LOG.csv`](templates/AUDIT_SAMPLE_LOG.csv).

## 11.6.2 Anti-Gaming Rule

If a metric becomes a target, check whether behavior can improve the number without improving the underlying control. Examples include narrowing prompts to inflate confidence, hiding failed validations, delaying work-item creation to reduce cycle time, or closing exceptions before remediation.

Pair important metrics with independent evidence and counter-metrics.

## 11.7 Assurance Reviews

Suggested cadence:

### Weekly
- active exceptions;
- aging human decisions;
- unauthorized attempt log;
- remediation queue.

### Monthly
- evidence completeness;
- control effectiveness;
- AI false positives/negatives;
- WIP and flow health;
- recurring failure patterns.

### Quarterly / Stage Boundary
- authorization model;
- policy changes;
- maturity progression;
- agent/tool scope;
- audit sample;
- governance debt.

## 11.8 Governance Debt

Governance debt includes:

- manual controls that should be automated;
- undocumented standing delegation;
- stale dashboards;
- unclear status semantics;
- duplicated evidence;
- obsolete rules;
- unowned exceptions;
- permissions broader than required.

Governance debt should enter the backlog like technical debt.

## 11.9 Metric Gaming

Avoid metrics that create perverse incentives.

Examples:

- minimizing remediation by hiding failures;
- improving approval speed by bypassing review;
- improving cycle time by moving waiting time outside the workflow;
- showing “green” dashboards by excluding exceptions improperly.

## 11.10 Human Decision Latency

Track decision latency separately from execution time.

If humans become the bottleneck, improve:

- evidence packaging;
- decision criteria;
- delegation for repeatable A2 work;
- escalation quality;
- dashboard prioritization.

Do not solve human latency by silently increasing AI authority.

## Cross-References

- Pilot: [Chapter 10](chapter_10.md)
- Scaling: [Chapter 12](chapter_12.md)
- KPI catalog: [`templates/KPI_CATALOG.csv`](templates/KPI_CATALOG.csv)

[Back to outline](outline.md)
