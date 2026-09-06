# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Appendix D — Case Studies

## Case Study 1 — AI Documentation Project

### Context

A team uses AI to generate technical documentation from governed source artifacts.

### GAD Design

- A0: read approved source material.
- A1: draft documentation and cross-references.
- A2: create draft branches and run link validation under explicit delegation.
- A3: publish externally only after human approval.
- Evidence: source references, validation result, approval record, release record.

### Learning

AI can automate most production effort without gaining publication authority.

---

## Case Study 2 — Governed Software Release

### Context

An AI worker prepares a release and deployment package.

### Flow

```text
GAD Work Item
→ implementation
→ automated tests
→ independent validation
→ evidence package
→ HUMAN DECISION
→ protected environment approval
→ deployment
→ monitoring
```

### Learning

The worker may prepare and validate extensively while production release remains an explicit A3 decision.

---

## Case Study 3 — GAD-PILOT-01 Human-Control Dashboard Pattern

### Context

A controlled Jira pilot needs to ensure that human decisions, failed controls, and release readiness are visible without exposing the dashboard broadly.

### Pattern

Create a private dashboard with separate saved views for:

1. Human Decision Required
2. A3/A4 Awaiting Approval
3. Evidence Missing
4. Validation Failed
5. Remediation Required
6. Dependency Blocked
7. WIP / Flow Exceptions
8. Ready for Release Authorization
9. Unauthorized / Policy Exception Signals

### Validation

Check:

- each filter returns only the intended active population;
- sharing is private/restricted;
- the dashboard uses the correct saved filter;
- completed historical records do not appear in active queues;
- historical failure/remediation records remain preserved.

### Learning

Operational truth and historical truth are both necessary, but they should not be mixed into the same control population.

---

## Case Study 4 — Historical Remediation Preservation

### Context

A work item initially fails a mandatory control. A later remediation succeeds.

### Incorrect Practice

```text
Original result changed from FAIL to PASS.
```

### GAD Practice

```text
Original validation = FAIL
Remediation validation = PASS
Current readiness = READY
Historical result = preserved
```

### Learning

A good governance system can show improvement without falsifying history.

---

## Case Study 5 — Anti-Pattern: Autonomy Exceeded Evidence

### Applicability
**Recommended for:** Executive/Sponsor, AI/Automation Lead, Governance/Audit, Security/Risk.

### Context

A team allows an AI worker to execute production changes because its recent recommendations have been highly accurate. No new authorization is recorded.

### Failure

The team confuses **confidence and past performance** with **authority**. A production action is executed without the required A3 approval, and the evidence package is assembled only afterward.

### GAD Response

```text
Unauthorized action signal
→ stop further autonomous execution
→ preserve logs/evidence
→ assess impact
→ enter remediation
→ revoke/suspend invalid delegation
→ human decision on recovery
→ revalidate controls before resuming
```

### Learning

High confidence can justify less review only if an explicit governance decision creates that bounded delegation. Confidence cannot create authority by itself.

---

## Case-Study Applicability Index

| Case | Most relevant personas |
|---|---|
| AI Documentation Project | Developer/Team Member, AI Lead |
| Governed Software Release | Delivery Lead, Developer, Governance |
| Human-Control Dashboard | Jira/GitHub Admin, Governance, Delivery Lead |
| Historical Remediation Preservation | Governance/Audit, Delivery Lead |
| Autonomy Exceeded Evidence | Executive, AI Lead, Security/Risk, Governance |

[Back to outline](outline.md)
