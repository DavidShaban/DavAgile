# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 7 — AI-Assisted Execution, Monitoring, and Predictive Risk
**Estimated reading time:** approximately 4 minutes

## Purpose

This chapter defines how GAD uses AI for speed and insight while keeping execution bounded, observable, and recoverable.

## 7.1 AI Task Automation

Suitable tasks include:

- data preparation;
- documentation;
- test generation;
- evidence indexing;
- backlog hygiene;
- classification;
- duplicate detection;
- summarization;
- report generation;
- static validation;
- policy checks;
- routine internal workflow actions under A2 delegation.

The more consequential the output, the stronger the validation and authorization requirement.

## 7.2 Real-Time Monitoring

AI can monitor:

- blocked work;
- aging approvals;
- failed checks;
- WIP breaches;
- dependency changes;
- service health;
- quality trends;
- unauthorized action attempts;
- evidence gaps.

A monitoring system should distinguish:

```text
Observation → Alert → Recommendation → Decision → Action
```

These are not the same thing.

## 7.3 Feedback Loops

GAD supports three feedback loops.

### Execution Loop
Seconds to days:

```text
Do → Validate → Correct
```

### Delivery Loop
Days to weeks:

```text
Deliver → Review → Reprioritize
```

### Governance Loop
Weeks to quarters:

```text
Observe controls → Analyze outcomes → Amend policy/method → Revalidate
```

## 7.3.1 Model, Agent, Prompt, and Configuration Versioning

Where an AI output or action is material to a governed claim, capture enough identity to reproduce or explain the execution:

- provider/runtime;
- model name and effective version or immutable identifier when available;
- agent version;
- prompt/template version where material;
- tool/configuration version;
- timestamp;
- relevant parameters;
- linked work item and evidence ID.

If a provider does not expose a fully pin-able model version, record the strongest available identity and treat silent provider change as an uncertainty.

Cross-reference: [`MODEL_AGENT_REGISTRY.yaml`](templates/MODEL_AGENT_REGISTRY.yaml).

## 7.4 Predictive Analytics

AI may estimate:

- milestone probability;
- schedule risk;
- capacity bottlenecks;
- defect risk;
- approval aging;
- dependency failure probability;
- likely WIP congestion.

Predictions must be presented as estimates, not facts.

## 7.5 Confidence and Uncertainty

A prediction or classification should, where practical, expose:

- confidence;
- uncertainty drivers;
- missing data;
- assumptions;
- model/version;
- evidence period.

High confidence does not override authorization.

### 7.5.1 Confidence Can Restrict, Not Grant, Authority

Confidence is an input to review and monitoring. It does **not** grant A2, A3, or A4 authority.

A local policy may use confidence thresholds to become more conservative:

```text
confidence below configured threshold
→ require additional validation or human review
```

It must not use high confidence to automatically grant a higher authorization level. Thresholds must be calibrated from observed performance for the relevant agent/work class and periodically revalidated.

Cross-reference: [`AI_CONFIDENCE_DASHBOARD.yaml`](templates/AI_CONFIDENCE_DASHBOARD.yaml).

## 7.6 Safe Optimization

AI may optimize within an explicit envelope.

Example:

```yaml
optimization_boundary:
  may_resequence:
    - A0
    - A1
    - delegated_A2
  must_escalate:
    - milestone_baseline_change
    - budget_commitment_change
    - production_release
    - authority_expansion
```

## 7.7 Risk Signals

Potential predictive risk inputs:

- cycle-time trend;
- blocked duration;
- unresolved dependencies;
- test failure trend;
- change volume;
- rework rate;
- approval queue age;
- defect escape;
- unstable requirements;
- staff/capacity variance.

## 7.8 False Positive and False Negative Management

Control automation should be measured for:

- alert precision;
- alert recall;
- false positives;
- false negatives;
- human override rate;
- missed material events.

A noisy control system trains humans to ignore warnings.

## 7.9 Escalation Rules

Examples:

```text
Evidence missing for A3/A4 → block release
Critical validation failed → remediation required
Authority scope mismatch → block execution
Prediction crosses defined milestone-risk threshold → planning review
Repeated AI output disagreement → human review
Unexpected tool behavior → stop and investigate
```

## 7.9.1 AI Error, Hallucination, and Action Recovery

When AI output is demonstrably wrong, unsupported, or outside the expected contract:

1. stop the affected action;
2. preserve the output and execution identity;
3. classify whether any mutation occurred;
4. reverse the mutation when an authorized recovery path exists;
5. route consequential recovery through the applicable A-level;
6. record remediation and residual limitations.

For an AI-initiated A2 action, the recovery path should be known before delegation is granted.

## 7.9.2 Human Override

A named human with applicable authority may veto or stop an in-flight AI action. Capture the action stopped, actor/agent, time, human authority, reason, current state, required recovery/remediation, and linked decision/incident.

An override does not erase the original AI action or recommendation.

## 7.9.3 Escalation Evidence Summary

When AI triggers escalation, provide: what was attempted/observed; model/agent/version; confidence/uncertainty if applicable; boundary crossed; current side effects; relevant evidence links; and the decision required.

Chapter 7 owns the **trigger**; Chapter 8 owns the **decision procedure**; Chapter 4 owns **organizational escalation responsibility**.

## 7.10 No Silent Self-Modification

An AI system should not:

- raise its own authorization ceiling;
- add new tools;
- widen data access;
- change approval rules;
- disable monitoring;
- change the evidence standard

without the applicable governed change.

## 7.11 Monitoring After Release

Monitoring should continue long enough to prove that the released change behaves as expected.

Capture:

- key outcome;
- health metrics;
- incident signals;
- rollback triggers;
- residual risks;
- monitoring close decision.

## Cross-References

- Agent roles: [Chapter 3](chapter_03.md)
- Decision logic: [Chapter 8](chapter_08.md)
- Metrics: [Chapter 11](chapter_11.md)

[Back to outline](outline.md)
