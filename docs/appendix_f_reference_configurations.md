# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


# Appendix F — Reference Configurations

## Jira Workflow

File: [`jira_workflow_reference.yaml`](templates/jira_workflow_reference.yaml)

Core state model:

```yaml
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
```

## GitHub Ruleset

File: [`github_ruleset_reference.json`](templates/github_ruleset_reference.json)

Purpose:

- protect `main`;
- require pull request;
- prevent force-style history rewriting;
- require status checks;
- support controlled release approvals.

## Agent Manifest

File: [`agent_manifest_example.yaml`](templates/agent_manifest_example.yaml)

Minimum governance fields:

```yaml
identity:
scope:
authorization:
data:
tools:
evidence:
escalation:
lifecycle:
```

## Naming Conventions

Suggested:

```text
GAD-###           Work item
DEC-YYYY-###      Decision
EVID-YYYY-###     Evidence package
VAL-YYYY-###      Validation
REM-YYYY-###      Remediation
REL-YYYY-###      Release
INC-YYYY-###      Incident
EXC-YYYY-###      Exception
```

## Configuration Rule

Reference configurations are illustrative. Operational implementations must be tested against the exact tool version, permissions, workflow scheme, and organizational policy.

## Naming Convention

Documentation Release 1.1 adopts a prospective convention:

- human-readable Markdown documents: `kebab-case.md`;
- new machine-consumed CSV/YAML/JSON artifacts: `UPPER_SNAKE.csv`, `UPPER_SNAKE.yaml`, `UPPER_SNAKE.json`.

Some Documentation Release 1.0 structured reference filenames were already published in lowercase (for example `jira_workflow_reference.yaml`). They remain in place for backward compatibility. New structured artifacts follow the convention above. Renaming legacy files is deferred to a compatibility-managed release.

## Example Traceability Chains

```text
GAD-1234
→ DEC-2026-042
→ EVID-2026-118
→ VAL-2026-118
→ REL-2026-031
```

```text
GAD-1250
→ EXC-2026-009
→ DEC-2026-057
→ REM-2026-017
→ EVID-2026-141
```

## Artifact Metadata

Human-readable templates carry a metadata block. Machine-readable artifacts carry metadata in their schema/top-level object where practical or in [`ARTIFACT_INDEX.csv`](templates/ARTIFACT_INDEX.csv).

`MANIFEST.sha256` remains a standard SHA-256 manifest for compatibility. [`MANIFEST.csv`](MANIFEST.csv) adds documentation release, artifact ID, and schema-version metadata.

[Back to outline](outline.md)
