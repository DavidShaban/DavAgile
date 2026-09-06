# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 13 — Operating Playbook and Continuous Improvement
**Estimated reading time:** approximately 4 minutes

## Purpose

This chapter turns GAD from a design into a repeatable operating rhythm.

## 13.0 Cadence Alignment

| Cadence | Focus | Inputs | Outputs |
|---|---|---|---|
| Daily | Flow health | WIP/age, blockers, AI-confidence anomalies | unblocking/escalation actions |
| Weekly | Decisions and exceptions | decision queue, exception expiries, unauthorized-action log | decisions, renewals/closures, remediation |
| Monthly | Assurance and learning | KPIs, audit samples, retrospective themes | improvement backlog, control-tuning proposals |
| Quarterly | Method/control health | maturity evidence, KPI validity, change proposals | policy/method decisions, training refresh |
| Annual | Method audit | full-year evidence, control effectiveness, external changes | method audit record and roadmap |

Cadence is adaptable; the important requirement is that flow, decisions, assurance, and method change are not conflated.

## 13.1 Daily Operating Cadence

AI and automation may continuously update:

- WIP;
- blocked work;
- evidence gaps;
- validation failures;
- dependency changes;
- aging decisions.

Human daily review should focus on exceptions and decisions rather than every work item.

## 13.2 Weekly Control Review

Suggested agenda:

1. outcome and milestone health;
2. critical dependencies;
3. human decisions required;
4. A3/A4 queue;
5. validation failures;
6. remediation;
7. unauthorized/policy exception signals;
8. AI quality concerns;
9. actions and owners.

## 13.3 Iteration Review

Review:

- delivered value;
- validation results;
- evidence quality;
- scope changes;
- control delays;
- AI contribution;
- upcoming consequential decisions.

## 13.4 Retrospective-to-Policy Loop

A retrospective finding becomes a methodology or policy change only through controlled change.

```text
Observation
  ↓
Improvement Proposal
  ↓
Impact / Risk Assessment
  ↓
Human Approval if required
  ↓
Method / Control Update
  ↓
Test
  ↓
Version
  ↓
Adopt
```

## 13.4.1 Evidence Threshold for Policy Change

A retrospective observation does not automatically become policy. A change proposal should be triggered by evidence such as a recurring pattern, a single high-severity control failure, changed external obligation, measured control ineffectiveness, or a material improvement opportunity.

The exact numeric trigger is locally configured; GAD does not mandate a universal occurrence count.

Use [`change_request_template.md`](templates/change_request_template.md), [`change-impact-assessment.md`](templates/change-impact-assessment.md), and a decision record.

## 13.4.2 Contribution and Feedback Channel

Maintain a governed channel for proposed improvements—such as an issue tracker, repository discussion, or improvement backlog. Contributions remain proposals until evaluated through the change process.

## 13.5 Monthly Assurance

Monthly review should identify:

- stale delegations;
- stale exceptions;
- unnecessary approvals;
- missing controls;
- repeated remediations;
- dashboard inaccuracies;
- over-broad permissions;
- control automation candidates.

## 13.6 Method Versioning

A GAD method release should include:

- version;
- change summary;
- reason/evidence;
- affected controls;
- compatibility impact;
- migration requirement;
- approval;
- effective date.

See [Appendix G](appendix_g_change_log.md).

## 13.6.1 Annual Method Audit

At least annually during sustained use, review authorization semantics, template/tool alignment, metric usefulness, AI/model changes, external obligations, deprecated artifacts, and training accuracy.

A method audit does not automatically increment the method version; it produces evidence for a change decision.

## 13.7 Training

Roles need different learning paths.

### Human Project Hub
- authority model;
- decision packages;
- risk acceptance;
- escalation;
- evidence sufficiency.

### Delivery Lead
- workflow;
- stage gates;
- backlog/WIP;
- dependencies;
- metrics.

### AI/Automation Lead
- manifests;
- authorization ceilings;
- safe failure;
- monitoring;
- model/version traceability.

### Governance/Audit
- evidence chain;
- historical truth;
- exception management;
- control testing.

## 13.8 Onboarding a New Agent

Checklist:

- identity;
- owner;
- purpose;
- allowed scope;
- prohibited scope;
- data class;
- tools;
- authorization ceiling;
- tests;
- validation;
- monitoring;
- escalation;
- retirement path.

## 13.9 Onboarding a New Project

Minimum steps:

1. define outcome;
2. define Human Project Hub;
3. configure authorization matrix;
4. configure workflow;
5. classify sensitive data;
6. define gates;
7. define evidence;
8. validate tooling controls;
9. run synthetic control tests;
10. authorize pilot.

## 13.10 Continuous Improvement Principle

The goal is not to keep every control forever.

Controls should be:

- added when evidence shows a gap;
- automated when stable;
- simplified when redundant;
- removed when no longer useful;
- strengthened when consequence changes.

## 13.11 Method Health Questions

Periodically ask:

- Are people bypassing controls?
- Are controls blocking harmless work?
- Are dashboards truthful?
- Is AI authority understandable?
- Are decisions traceable?
- Are failures preserved?
- Are remediations closing root causes?
- Is bounded autonomy actually bounded?
- Is delivery getting faster without losing control?

## Final Operating Principle

> **GAD succeeds when the system can move quickly by default, stop precisely when required, explain why it stopped, present the right evidence to the right human, and continue without losing historical truth.**

[Back to outline](outline.md)
