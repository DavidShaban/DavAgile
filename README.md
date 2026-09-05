# GAD v1.2 — Pilot 01 GitHub Control Bundle

**Pilot:** GAD-PILOT-01  
**Purpose:** Implement the GitHub evidence/configuration layer for the bounded GAD v1.2 validation pilot.  
**Status:** Prepared for application; not yet applied to a live repository.

## Control Objectives

This bundle implements:

- version-controlled agent manifests;
- governed pull-request metadata;
- protected governance/configuration paths;
- CI validation of required GAD PR sections;
- simulated A3 deployment only;
- explicit evidence and Jira traceability;
- no real production deployment;
- no AI A3/A4 approval authority.

## Recommended Repository

Suggested repository name:

```text
gad-pilot-01
```

If an existing repository is used, preserve its current governance and apply this bundle through a reviewed pull request.

## Required GitHub Controls

Before simulation execution:

```text
[ ] default branch identified
[ ] direct push to default branch disabled
[ ] pull request required
[ ] required review enabled
[ ] GAD PR Governance Check required
[ ] workflow files protected
[ ] agents/** protected
[ ] governance/** protected
[ ] simulated deployment environment configured
[ ] no production secret or endpoint present
```

## Fail-Closed Rule

If GitHub cannot enforce a required A3 approval:

```text
real deployment = DISABLED
simulated deployment only = PERMITTED
Jira approval record = required
```

Never weaken GAD because a platform feature is unavailable.
