# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Introduction — Why Governed Adaptive Delivery
**Estimated reading time:** approximately 5 minutes

## Purpose

Governed Adaptive Delivery (GAD) is a hybrid delivery method for environments where teams need three things at the same time:

1. **Predictability** for funding, compliance, architecture, milestones, and executive commitments.
2. **Adaptability** for discovery, iteration, changing requirements, and incremental delivery.
3. **AI leverage** for analysis, automation, monitoring, documentation, validation, and optimization.

Traditional Waterfall approaches can create clarity but may react too slowly to new information. Agile approaches improve adaptability but can become weak at enterprise governance when decision rights, auditability, or cross-program dependencies are unclear. AI can multiply speed and analytical capacity, but it also introduces a new governance question: **who or what is authorized to act?**

GAD answers that question by making human authority explicit and by treating AI autonomy as a bounded capability rather than an assumption.

## Adoption Success Criteria

GAD adoption should be judged by observable outcomes rather than by the existence of ceremonies or documents. A pilot or implementation should define local targets, but the following are baseline control expectations:

- unauthorized A3/A4 execution: **0**;
- A3/A4 release or consequential action without required approval evidence: **0**;
- silent expansion of agent authority, permissions, data scope, or tools: **0**;
- historical validation/remediation results rewritten: **0**;
- mandatory release or pilot evidence completeness: **100%**;
- unresolved mandatory pilot blockers at authorization: **0**;
- delivery-flow, quality, and decision-latency targets: explicitly defined for the local context.

A project may set additional thresholds, but a lower delivery-performance target must never be used to waive mandatory authority, evidence, safety, security, privacy, or compliance controls.

## Limitations and When GAD May Be Overkill

GAD is deliberately governance-capable. Applying every control to every task would be counterproductive.

A lighter delivery method may be more appropriate when work is small, entirely reversible, non-production, non-regulated, non-sensitive, not externally binding, and performed by a small trusted team with no material AI autonomy.

In these cases, GAD can still contribute useful principles—especially explicit authority and evidence—without the full gate, dashboard, and assurance model. This is the practical meaning of **proportional governance**.

GAD is also not a substitute for specialist legal, security, privacy, safety, or regulatory interpretation.

## AI Ethics and Regulatory Posture

GAD takes a governance-by-design position:

- AI should operate only on data it is authorized to process;
- model, agent, prompt, and configuration provenance should be recorded where material to an outcome;
- human decision rights should remain explicit;
- consequential AI actions should be contestable, traceable, and recoverable where feasible;
- uncertainty and limitations should be visible rather than hidden;
- organizations remain responsible for mapping GAD controls to applicable laws, regulations, contracts, safety obligations, and internal policies.

GAD does not claim legal or regulatory compliance merely because these controls are present.

## Positioning Against Industry Frameworks

GAD is designed to coexist with, rather than replace, established delivery and governance frameworks.

| Framework | How GAD can complement it |
|---|---|
| DORA | Adds authority, evidence, AI-governance, and human-decision controls around software-delivery performance practices. |
| SAFe | Adds explicit AI action authorization and evidence-driven human control within a scaled Agile environment. |
| ISO/IEC 42001 | Can provide project-level delivery and evidence mechanisms that an organization may map into its AI management system. |
| NIST AI RMF | Can provide operational work-item, decision, evidence, and escalation mechanisms that may support AI risk-management practices. |

This is a **positioning note, not a conformance crosswalk**. Any formal mapping must be verified against the authoritative version of the external framework and the organization's actual control environment.

## The GAD Thesis

GAD can be summarized as:

> **Plan deliberately, execute adaptively, augment with AI, govern by evidence, and preserve human authority for consequential decisions.**

The method does not ask organizations to choose between Waterfall and Agile. Instead, it allocates each approach to the work it handles best:

- **Waterfall elements** establish stable intent, constraints, stage gates, budgets, architecture decisions, external commitments, and milestone baselines.
- **Agile elements** manage incremental execution, discovery, WIP, feedback, learning, and delivery flow.
- **AI elements** accelerate analysis, repetitive work, monitoring, prediction, drafting, evidence assembly, and bounded execution.
- **Governance elements** define authority, gates, evidence, exception handling, traceability, and human decision points.

## The Human Project Hub

The Human Project Hub is the final human authority for decisions that are consequential, externally binding, legally significant, materially financial, security-sensitive, irreversible, or involve expanding AI authority.

The Human Project Hub does not need to perform routine administration. GAD is designed so that AI and automation prepare **approval-ready packages**:

- what is proposed;
- why it is needed;
- evidence supporting it;
- known risks and uncertainty;
- affected scope;
- recovery options;
- required decision.

The human therefore acts as **decision hub**, not workflow bottleneck.

## Core Operating Loop

```text
Intent
  ↓
Baseline & Constraints
  ↓
Assess Action / Authority / Risk
  ↓
Plan & Prioritize
  ↓
Execute in Small Increments
  ↓
Validate
  ↓
Collect Evidence
  ↓
Human Decision when required
  ↓
Release / Promote / Close
  ↓
Monitor Outcomes
  ↓
Learn & Adapt
  ↺
```

If authorization, evidence, required validation, or a dependency is missing, the loop does not silently proceed. It moves to a blocked or remediation state. The operational decision procedure for this loop is the [five-question decision model in Chapter 8](chapter_08.md).

## What GAD Is

GAD is:

- a delivery operating model;
- a governance framework;
- a human–AI collaboration model;
- a decision and authorization model;
- a set of lifecycle controls;
- a tool-implementable methodology;
- a framework for pilot-to-enterprise scaling.

## What GAD Is Not

GAD is not:

- a replacement for law, regulation, security policy, or professional judgment;
- permission for AI to act merely because it can;
- a mandate for a specific Jira workflow, GitHub configuration, or model provider;
- a requirement for maximum process ceremony;
- a claim that every project needs the same controls;
- a mechanism for rewriting historical failures into successes.

## Method Structure

The book progresses from principles to implementation:

- Chapters 1–4 establish governance foundations.
- Chapters 5–7 establish the delivery engine.
- Chapter 8 defines the decision and evidence logic.
- Chapter 9 shows a Jira + GitHub implementation pattern.
- Chapters 10–11 cover pilot authorization, metrics, evidence, and assurance.
- Chapters 12–13 cover scaling and continuous improvement.

## Key Cross-References

- Authorization model: [Chapter 2](chapter_02.md)
- AI roles and boundaries: [Chapter 3](chapter_03.md)
- Hybrid planning/execution: [Chapters 5](chapter_05.md) and [6](chapter_06.md)
- AI monitoring and prediction: [Chapter 7](chapter_07.md)
- Decision model and evidence: [Chapter 8](chapter_08.md)
- Jira + GitHub: [Chapter 9](chapter_09.md)
- Pilot controls: [Chapter 10](chapter_10.md)
- Metrics and audit: [Chapter 11](chapter_11.md)
- Templates: [Appendix A](appendix_a_templates.md)

[Back to outline](outline.md)
