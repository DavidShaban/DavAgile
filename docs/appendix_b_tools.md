# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Appendix B — Tools and Implementation Patterns

## Jira + GitHub Implementation Kit

### Jira

Recommended capabilities:

- custom fields for authorization, evidence, readiness, decision ID;
- workflow validators;
- restricted transitions;
- issue links for dependencies;
- saved filters;
- private control dashboards;
- automation rules for alerts and evidence gaps.

### GitHub

Recommended capabilities:

- protected branches;
- pull requests;
- required status checks;
- CODEOWNERS or required reviewers where appropriate;
- protected environments for consequential releases;
- release tags;
- issue/decision/evidence links.

## Evidence Repository Pattern

A simple structure:

```text
evidence/
  EVID-2026-001/
    summary.md
    tests/
    approvals/
    release/
    monitoring/
```

The evidence store may be Git, a document repository, an audit system, or a combination.

## Dashboard Pattern

The Human Control Dashboard should prioritize actionable exceptions:

```text
Human Decisions
A3/A4 Awaiting Approval
Evidence Missing
Validation Failed
Remediation Required
Dependencies
WIP Exceptions
Release Authorization
Policy/Unauthorized Signals
```

## Tooling Quick-Start

1. Load the Jira and GitHub **reference** configurations into a non-production/staging environment.
2. Create/bind the governed custom fields.
3. Configure evidence and validation checks.
4. Configure protected branches/paths and human release approval where applicable.
5. Configure the rule: confidence below review threshold → Human Review Required.
6. Create the private Human Control dashboard and its nine reference queues.
7. Bind KPI sources to the dashboard model.
8. Run one synthetic work item end-to-end and verify every mandatory guard fails closed.
9. Execute [`pilot_readiness_checklist.md`](templates/pilot_readiness_checklist.md).
10. Export/snapshot the final configuration, version it, and record hashes in the manifests.

Do not treat these files as one-click vendor import contracts; they are implementation patterns that must be adapted and tested against the actual Jira/GitHub versions and permission schemes.

## Governance Tool Backup / Restore Pattern

```text
tooling-config/
  jira/
    workflow-reference.yaml
    field-map.md
    automation-export/
  github/
    ruleset-reference.json
    CODEOWNERS
    environment-notes.md
  restore-procedure.md
  evidence/
```

Test restoration periodically in a safe environment.

## Tool Independence

Equivalent implementations can use:

- Azure DevOps;
- GitLab;
- ServiceNow;
- Linear;
- Trello for lighter use cases;
- internal workflow engines;
- policy-as-code platforms.

The GAD requirement is semantic control, not vendor identity.

[Back to outline](outline.md)
