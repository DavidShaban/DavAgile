# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 3 — Human–AI Team and Agent Roles
**Estimated reading time:** approximately 5 minutes

## Purpose

GAD structures AI as a governed team of capabilities around a human decision hub. Roles may be implemented as separate agents, services, prompts, workflows, or responsibilities; the governance model is more important than the technology.

## 3.1 Human Project Hub

The Human Project Hub is accountable for consequential decisions that the organization has not delegated.

Core responsibilities:

- set intent and constraints;
- approve A3/A4 actions;
- resolve material conflicts;
- accept or reject residual risk;
- approve authority changes;
- approve methodology changes;
- make final decisions that require human judgment.

The Human Project Hub should receive approval-ready packages rather than unfinished analysis.

## 3.2 Orchestrator Agent

Purpose:

- coordinate work;
- determine which capability should act;
- preserve dependencies and sequence;
- request validations;
- stop when a gate is not satisfied.

The orchestrator does not become an approval authority merely because it coordinates other agents.

## 3.3 Planning Agent

Typical responsibilities:

- decompose outcomes into work;
- identify dependencies;
- build forecast options;
- maintain risk assumptions;
- propose backlog priorities;
- detect milestone threats.

The planning agent proposes; policy and authorization determine what may be changed.

## 3.4 Execution / Worker Agent

Typical responsibilities:

- perform bounded tasks;
- generate artifacts;
- implement changes;
- run approved routines;
- report exact outcome and deviations.

A worker should not validate its own consequential output as the only control.

## 3.5 Validation Agent

Typical responsibilities:

- evaluate acceptance criteria;
- run tests;
- check policy rules;
- validate schema/configuration;
- verify evidence completeness;
- detect inconsistencies.

A validator should be independent enough that the execution agent cannot simply mark its own work valid.

## 3.6 Governance / Risk Agent

Typical responsibilities:

- classify A0–A4;
- identify escalation triggers;
- check authorization validity;
- identify policy conflicts;
- check change scope;
- stop unsupported status promotion.

The governance agent can enforce rules but should not invent new authority.

## 3.7 Evidence Agent

Typical responsibilities:

- capture evidence IDs;
- link issue/change/test/approval/release records;
- maintain evidence package completeness;
- distinguish evidence from inference;
- preserve historical outcomes.

## 3.8 Reporting / Control Agent

Typical responsibilities:

- maintain control dashboards;
- summarize active exceptions;
- surface human decisions;
- report WIP and flow;
- highlight overdue approvals or remediation.

Reporting should not alter underlying truth to make dashboards look healthy.

## 3.9 Specialist Agents

Examples:

- security;
- architecture;
- finance;
- legal-support;
- data privacy;
- QA;
- domain-specific technical agents.

Specialists retain bounded scope. The orchestrator cannot silently merge their authority.

## 3.9.1 Reference Role Cards

The ceilings below are default design guidance, not automatic grants. A local authorization record may be stricter.

| Role | Purpose | Default authorization ceiling | Required evidence outputs | Fail-closed behavior |
|---|---|---|---|---|
| Orchestrator | Coordinate bounded work and dependencies | A1; A2 only for explicitly delegated workflow actions | routing/sequence record, blockers, handoffs | stop on missing dependency/authority |
| Planner | Decompose, forecast, and recommend | A1 | assumptions, dependency/risk analysis, recommendation | escalate baseline-impacting change |
| Worker | Perform bounded execution | A1 by default; A2 under delegation | exact action/result, changed artifacts, deviations | stop on scope/tool mismatch |
| Validator | Test claims and acceptance criteria | A1 | criteria checked, result, limitations, evidence links | never self-promote failed output |
| Governance | Evaluate policy/authorization | A1 | classification, applicable rule, escalation | block unsupported authority/status |
| Evidence | Assemble traceability | A1 | evidence index, completeness/sufficiency status | mark incomplete rather than infer |
| Reporting | Surface control state | A1 | dashboard/report provenance | never rewrite source-of-truth state |
| Specialist | Provide bounded domain expertise | Configured per specialist | domain evidence, assumptions, limitations | escalate outside specialist scope |

## 3.9.2 No AI-to-AI Authorization Handoff

An AI agent may delegate **work** to another authorized AI capability, but it may not transfer or create human authorization. The receiving agent acts only within its own valid authorization.

## 3.9.3 Agent Onboarding and Retirement

Before a new agent touches governed work:

1. identity and human owner are recorded;
2. purpose, inputs, data classes, tools, and prohibited scope are specified;
3. authorization ceiling is defined;
4. implementation is tested;
5. validation evidence is reviewed;
6. deployment/operational transition follows [Chapter 4](chapter_04.md);
7. monitoring and retirement conditions are defined.

Retirement requires revoking active delegations, disabling governed tool/data access, preserving required evidence/history, and recording the retirement decision.

## 3.10 Separation of Duties

Recommended minimum separations:

```text
Execute ≠ Approve
Execute ≠ Sole Validator
Recommend ≠ Decide
Orchestrate ≠ Expand Authority
Report ≠ Rewrite History
```

For low-risk A0/A1 work, roles may be combined for efficiency. Separation becomes stronger as consequence rises.

## 3.11 Agent Manifest

A governed agent should have a manifest describing at least:

- identity;
- owner;
- purpose;
- allowed inputs;
- prohibited inputs;
- allowed actions;
- prohibited actions;
- authorization ceiling;
- tools;
- data boundaries;
- required evidence;
- escalation conditions;
- lifecycle status.

See [`agent_manifest_example.yaml`](templates/agent_manifest_example.yaml).

## 3.12 Agent Lifecycle Ownership

This chapter owns **role design**. [Chapter 4](chapter_04.md) is the authoritative home for the agent lifecycle state machine, transition evidence, status integrity, and retirement controls.

An agent role card must state its current lifecycle status, but it must not define a competing lifecycle.

## 3.13 Safe Failure

An agent should stop or escalate when:

- authority is ambiguous;
- required input is unavailable;
- a tool behaves outside the expected contract;
- validation fails;
- output would cross a prohibited boundary;
- evidence cannot be captured;
- a recovery requirement is unmet.

## 3.14 RACI

The reference RACI is in [`RACI_MATRIX.csv`](templates/RACI_MATRIX.csv).

It is intentionally adaptable. The main invariant is that consequential approval remains assigned to a human role unless an organization has explicitly designed and authorized a different control model that still satisfies applicable policy.

## Cross-References

- Authorization levels: [Chapter 2](chapter_02.md)
- Lifecycle and change control: [Chapter 4](chapter_04.md)
- AI monitoring: [Chapter 7](chapter_07.md)
- Evidence: [Chapter 8](chapter_08.md)

[Back to outline](outline.md)
