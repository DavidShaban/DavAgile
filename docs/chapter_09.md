# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Chapter 9 — Tooling Implementation: Jira + GitHub
**Estimated reading time:** approximately 5 minutes

## Purpose

GAD is tool-agnostic, but Jira and GitHub provide a practical implementation pattern for work governance, evidence, source control, approvals, and release traceability.

## 9.1 Jira Responsibilities

Use Jira for:

- intent and work hierarchy;
- workflow state;
- authorization classification;
- human-decision queues;
- dependencies;
- control exceptions;
- evidence references;
- dashboards;
- remediation tracking.

## 9.2 Recommended Jira Fields

Example fields:

```text
GAD Authorization Level: A0 | A1 | A2 | A3 | A4
GAD Decision Required: Yes | No
GAD Decision ID
GAD Evidence Link(s)
GAD Evidence Status: Missing | Partial | Complete
GAD Gate Approval Status: Open | Pending | Approved | Rejected | Expired | Withdrawn
GAD Validation Result: Not Run | PASS | FAIL | INDETERMINATE
GAD AI Confidence: optional numeric/qualitative field; never an authority grant
GAD Human Review Required: Yes | No + trigger timestamp
GAD Unauthorized Action Flag: Yes | No
GAD Readiness: NOT_READY | READY_FOR_HUMAN_DECISION | READY_FOR_RELEASE_AUTHORIZATION | REMEDIATION_REQUIRED
GAD Recovery Plan: URL / reference
GAD Approval Expires
GAD Historical Result
```

## 9.3.1 Reference Validators and Automation

```text
If target state makes a governed completion/release claim
AND mandatory evidence is incomplete
→ block transition

If A3/A4 AND valid APPROVED decision is absent
→ block release

If delegation expired
→ block delegated A2 execution

If AI confidence falls below a configured review threshold
→ set Human Review Required
→ do not grant authority automatically

If a transition skips a mandatory control
→ flag policy exception / unauthorized-action signal
```

## 9.3.2 Override Permissions

Document who can override a gate or workflow guard. A consequential override requires an authorized human and creates a decision record with rationale, scope, evidence, and expiry if temporary. Tool-admin permission by itself is not business authorization.

## 9.3 Reference Workflow

```yaml
workflow:
  states:
    - INTAKE
    - ASSESSED
    - READY
    - IN_PROGRESS
    - VALIDATION
    - HUMAN_DECISION
    - APPROVED_FOR_RELEASE
    - RELEASED
    - DONE
    - BLOCKED
    - REMEDIATION_REQUIRED

  guards:
    READY:
      require:
        - authorization_level_classified
        - dependencies_satisfied
    APPROVED_FOR_RELEASE:
      require:
        - validation_passed
        - evidence_complete
        - approval_if_A3_or_A4
    DONE:
      require:
        - closure_evidence_complete
```

Full reference: [`jira_workflow_reference.yaml`](templates/jira_workflow_reference.yaml).

## 9.4 Private Human-Control Views

Sensitive operational control views should usually be restricted to appropriate roles.

A reference set of nine saved control queues:

1. Human Decision Required
2. A3/A4 Awaiting Approval
3. Evidence Missing
4. Validation Failed
5. Remediation Required
6. Dependency Blocked
7. WIP / Flow Exceptions
8. Ready for Release Authorization
9. Unauthorized / Policy Exception Signals

A Human Control Dashboard can display these as separate filter-result panels.

The exact queries depend on Jira schema and project configuration.

## 9.5 Active vs Historical Records

A crucial dashboard rule:

> Active control queues should represent current actionable state, not every historical item that ever matched a condition.

For example, a completed historical record that once required remediation should remain discoverable in audit history but should not continue polluting an active “Remediation Required” queue after the current state is closed.

Historical result fields should remain preserved.

## 9.6 GitHub Responsibilities

Use GitHub for:

- version-controlled artifacts;
- pull requests;
- review;
- required checks;
- branch protection;
- environment approvals;
- release tags;
- immutable-ish change history.

## 9.7 Reference GitHub Ruleset

```json
{
  "name": "gad-protected-main",
  "target": "branch",
  "enforcement": "active",
  "conditions": {
    "ref_name": {
      "include": ["refs/heads/main"],
      "exclude": []
    }
  },
  "rules": [
    {"type": "deletion"},
    {"type": "non_fast_forward"},
    {"type": "pull_request"},
    {"type": "required_status_checks"}
  ]
}
```

Full reference: [`github_ruleset_reference.json`](templates/github_ruleset_reference.json).

## 9.7.1 Evidence-Enforcing GitHub Pattern

For governed repositories, consider protected `main`/release branches, pull-request review, `CODEOWNERS` for governance-sensitive paths, status checks such as `tests`, `gad-validation`, and `evidence-validator`, linear/non-fast-forward history protection, signed commits where policy requires them, and protected deployment environments with human review for A3/A4 release actions.

These are reference controls; exact availability and syntax depend on the GitHub plan/API and repository governance.

## 9.7.2 Configuration as Code and Recovery

Version the reference Jira/GitHub configuration in a governed repository. Maintain configuration snapshots, change decisions, hashes/versions, export/restore procedure, and ownership for emergency restoration. A failure of the governance tooling is itself a control risk.

## 9.8 Pull Request Evidence

A consequential PR should link:

- Jira issue;
- decision record if required;
- test evidence;
- validation evidence;
- recovery plan;
- release authorization.

Example PR body:

```markdown
## GAD Traceability
- Work item: GAD-123
- Authorization: A3
- Decision: DEC-2026-042
- Validation: VAL-2026-118 PASS
- Evidence package: EVID-2026-118
- Recovery: REC-2026-031
```

## 9.9 Environments

For A3 production deployment, a GitHub environment can enforce a human approval.

Conceptual mapping:

```text
Pull Request Approved
      ↓
Required Checks PASS
      ↓
Production Environment Approval
      ↓
Deployment
      ↓
Post-Deployment Monitoring
```

## 9.10 Traceability IDs

Recommended patterns:

```text
GAD-123           Work item
DEC-2026-042      Decision
EVID-2026-118     Evidence package
VAL-2026-118      Validation
REM-2026-017      Remediation
REL-2026-031      Release
INC-2026-006      Incident
```

## 9.10.1 Worked Traceability Chain

```text
Jira issue GAD-1234
  → PR #567
  → validation VAL-2026-118
  → evidence package EVID-2026-118
  → human decision DEC-2026-042
  → release REL-2026-031 / tag
  → operational evidence
  → audit sample record
```

A reviewer should be able to traverse the chain in both directions.

## 9.11 Tooling Principle

Tools enforce configured rules. They do not prove the rules are correct.

GAD governance therefore includes periodic control validation:

- can unauthorized transitions occur?
- can an A3 release bypass approval?
- can a historical item contaminate active queues?
- are dashboard permissions correct?
- do GitHub checks match the intended branch/environment?

## Cross-References

- Authorization: [Chapter 2](chapter_02.md)
- Lifecycle: [Chapter 4](chapter_04.md)
- Pilot dashboard: [Chapter 10](chapter_10.md)
- Tool appendix: [Appendix B](appendix_b_tools.md)

[Back to outline](outline.md)
