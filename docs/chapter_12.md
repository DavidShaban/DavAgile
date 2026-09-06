# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 12 — Scaling, Maturity, and Enterprise Adoption
**Estimated reading time:** approximately 4 minutes

## Purpose

GAD should scale by increasing repeatability and policy automation, not by multiplying meetings and manual approvals.

## 12.1 GAD Maturity Model

### Level 0 — Ad Hoc
- AI use is individual and inconsistent.
- Decision rights are unclear.
- Evidence is fragmented.
- Exceptions are informal.

### Level 1 — Controlled
- A0–A4 exists.
- Human authority is explicit.
- basic workflow and audit evidence exist.
- consequential actions are gated.

### Level 2 — Repeatable
- standard templates;
- repeatable Jira/GitHub controls;
- defined agent roles;
- consistent pilot/release gates;
- common metrics.

### Level 3 — Measured
- control effectiveness is measured;
- evidence completeness is tracked;
- flow and governance metrics are integrated;
- predictive risk begins to inform planning.

### Level 4 — Adaptive
- policies are increasingly machine-enforced;
- governance thresholds are tuned using evidence;
- low-risk work receives wider bounded automation;
- assurance is continuous.

### Level 5 — Governed Autonomous
- selected action classes operate autonomously inside formally authorized envelopes;
- controls are continuously monitored;
- human authority remains explicit for boundary changes and consequential decisions not delegated;
- autonomy can be revoked quickly.

## 12.1.1 Evidence-Scored Maturity Dimensions

GAD v1.2 retains its existing **Level 0–5** maturity model. The editorial review proposed M0–M4, but changing the number/meaning of maturity levels would be a method change; Documentation Release 1.1 therefore strengthens the existing model instead.

Assess each level using evidence across:

- **Authority** — from unclear/manual to explicit and tool-enforced.
- **Evidence** — from fragmented to mandatory and automatically validated.
- **Autonomy** — from ad hoc use to bounded, explicitly authorized autonomy.
- **Metrics** — from absent to owned, calibrated, and policy-informing.
- **Audit** — from none to risk-stratified/continuous assurance.

A maturity level is **earned by evidence, not claimed by declaration**.

Cross-reference: [`maturity-assessment.md`](templates/maturity-assessment.md).

## 12.1.2 Regression Rule

Maturity is reversible. If material control evidence degrades—such as rising unauthorized-action rate, failed audit, or loss of authorization traceability—the organization should reassess the affected capability and may regress it to a lower operating level until remediation passes.

## 12.2 Scaling Teams

At multi-team scale, standardize:

- authorization taxonomy;
- evidence identifiers;
- minimum workflow semantics;
- escalation model;
- control metrics;
- agent manifest fields.

Allow teams to adapt:

- sprint cadence;
- board layout;
- implementation tools;
- local task decomposition.

## 12.3 Portfolio Governance

Portfolio GAD adds:

- cross-program dependencies;
- shared AI services;
- capacity allocation;
- investment gates;
- enterprise risk;
- model/tool portfolio;
- common controls;
- reusable evidence.

## 12.4 Federated Governance

A federated model can assign:

- enterprise policy ownership centrally;
- execution governance to programs;
- product decisions to product leadership;
- technical controls to engineering/security;
- final accountability to named humans.

## 12.5 Policy as Code

High-value rules can become machine-enforced:

```text
If authorization = A3 or A4
AND approval decision missing
THEN block transition to APPROVED_FOR_RELEASE
```

Policy-as-code should be version controlled and tested.

## 12.6 Model and Agent Portfolio Governance

Track:

- model/agent ID;
- owner;
- purpose;
- data class;
- tools;
- authorization ceiling;
- version;
- test status;
- validation status;
- deployment status;
- operational status;
- retirement date.

## 12.7 Enterprise Integration

GAD can integrate with:

- PMO/PPM;
- ITSM;
- SDLC;
- DevSecOps;
- risk management;
- internal audit;
- quality management;
- compliance management;
- data governance;
- architecture governance.

GAD should bridge these systems through shared evidence and decisions rather than duplicate them.

## 12.7.1 Center of Excellence / Train-the-Trainer

At enterprise scale, a GAD enablement capability may maintain reference controls/templates, train practitioners, qualify internal trainers under organizational policy, facilitate cross-team learning, support maturity assessments, and maintain implementation patterns.

The COE should not centralize every delivery decision. Federated teams retain local execution responsibility inside enterprise guardrails.

## 12.7.2 Vendor and Licensing Governance

For external AI/agent services, track vendor/service identity, contractual/licensing constraints, data-processing boundary, model/version change behavior, availability/exit risk, audit/export capability, cost/renewal authority, approved use cases, and retirement/migration plan.

Cross-reference: [`MODEL_AGENT_REGISTRY.yaml`](templates/MODEL_AGENT_REGISTRY.yaml).

## 12.8 Scaling Guardrail

Do not increase autonomy merely because the organization has more work.

Increase autonomy only when:

- the action class is understood;
- controls are proven;
- evidence is strong;
- failure is manageable;
- monitoring is effective;
- authority is explicitly granted.

## 12.9 Adoption Roadmap

A practical enterprise sequence:

```text
Define → Pilot → Measure → Harden Controls → Repeat → Federate → Automate Controls → Expand Bounded Autonomy
```

## Cross-References

- Pilot: [Chapter 10](chapter_10.md)
- Metrics: [Chapter 11](chapter_11.md)
- Operating playbook: [Chapter 13](chapter_13.md)

[Back to outline](outline.md)
