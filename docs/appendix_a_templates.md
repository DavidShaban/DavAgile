# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

# Appendix A — Templates and Artifacts

## Purpose

This appendix is the single lookup point for reusable implementation artifacts.

## Artifact Index

| Artifact ID | File | Owning chapter | Schema | Purpose |
|---|---|---|---|---|
| `ART-AUTH-001` | [`AUTHORIZATION_MATRIX.csv`](templates/AUTHORIZATION_MATRIX.csv) | Chapter 2 | 1.1 | A0–A4 authorization control matrix |
| `ART-AUTH-002` | [`AUTHORIZATION_GRANT_REGISTER.csv`](templates/AUTHORIZATION_GRANT_REGISTER.csv) | Chapter 2 | 1.0 | Delegation register |
| `ART-RACI-001` | [`RACI_MATRIX.csv`](templates/RACI_MATRIX.csv) | Chapter 3 | 1.0 | Reference accountability matrix |
| `ART-PILOT-001` | [`PILOT_GATE_REGISTER.csv`](templates/PILOT_GATE_REGISTER.csv) | Chapters 5/10 | 1.1 | Gate evidence register |
| `ART-EVID-001` | [`evidence_package_template.md`](templates/evidence_package_template.md) | Chapter 8 | 1.1 | Evidence package template |
| `ART-DEC-001` | [`decision_record_template.md`](templates/decision_record_template.md) | Chapter 8 | 1.1 | Decision record template |
| `ART-JIRA-001` | [`jira_workflow_reference.yaml`](templates/jira_workflow_reference.yaml) | Chapter 9 | 1.1 | Jira workflow reference pattern |
| `ART-GH-001` | [`github_ruleset_reference.json`](templates/github_ruleset_reference.json) | Chapter 9 | 1.1 | GitHub ruleset reference pattern |
| `ART-PILOT-003` | [`pilot_readiness_checklist.md`](templates/pilot_readiness_checklist.md) | Chapter 10 | 1.1 | Pilot readiness checklist |
| `ART-KPI-001` | [`KPI_CATALOG.csv`](templates/KPI_CATALOG.csv) | Chapter 11 | 1.1 | KPI catalog |
| `ART-CHG-001` | [`change_request_template.md`](templates/change_request_template.md) | Chapters 4/13 | 1.1 | Change request |
| `ART-REM-001` | [`incident_and_remediation_template.md`](templates/incident_and_remediation_template.md) | Chapters 4/8 | 1.1 | Incident/remediation |
| `ART-AGENT-001` | [`agent_manifest_example.yaml`](templates/agent_manifest_example.yaml) | Chapter 3 | 1.1 | Agent manifest |
| `ART-CHG-002` | [`change-impact-assessment.md`](templates/change-impact-assessment.md) | Chapter 8 | 1.0 | Blast-radius/reversibility assessment |
| `ART-MODEL-001` | [`MODEL_AGENT_REGISTRY.yaml`](templates/MODEL_AGENT_REGISTRY.yaml) | Chapters 7/12 | 1.0 | Model/agent registry |
| `ART-UA-001` | [`UNAUTHORIZED_ACTION_REGISTER.csv`](templates/UNAUTHORIZED_ACTION_REGISTER.csv) | Chapter 11 | 1.0 | Unauthorized-action log |
| `ART-EXC-001` | [`EXCEPTION_REGISTER.csv`](templates/EXCEPTION_REGISTER.csv) | Chapter 8 | 1.0 | Exception register |
| `ART-RISK-001` | [`RISK_REGISTER.csv`](templates/RISK_REGISTER.csv) | Chapters 5/8 | 1.0 | Risk register |
| `ART-AUDIT-001` | [`AUDIT_SAMPLE_LOG.csv`](templates/AUDIT_SAMPLE_LOG.csv) | Chapter 11 | 1.0 | Audit sample log |
| `ART-MAT-001` | [`maturity-assessment.md`](templates/maturity-assessment.md) | Chapter 12 | 1.0 | Evidence-scored maturity assessment |
| `ART-PILOT-002` | [`PILOT_REPORT_TEMPLATE.md`](templates/PILOT_REPORT_TEMPLATE.md) | Chapter 10 | 1.0 | Pilot report |
| `ART-ESC-001` | [`escalation-protocol.md`](templates/escalation-protocol.md) | Chapter 4 | 1.0 | Escalation protocol |
| `ART-DASH-001` | [`AI_CONFIDENCE_DASHBOARD.yaml`](templates/AI_CONFIDENCE_DASHBOARD.yaml) | Chapters 7/11 | 1.0 | Confidence dashboard reference |
| `ART-DASH-002` | [`KPI_DASHBOARD.yaml`](templates/KPI_DASHBOARD.yaml) | Chapter 11 | 1.0 | KPI dashboard reference |
| `ART-GLOSS-001` | [`GAD_TERMINOLOGY_GLOSSARY.csv`](templates/GAD_TERMINOLOGY_GLOSSARY.csv) | Appendix E | 1.0 | Machine-readable glossary |
| `ART-INDEX-001` | [`ARTIFACT_INDEX.csv`](templates/ARTIFACT_INDEX.csv) | Appendix A | 1.0 | Artifact metadata index |

Machine-readable index: [`ARTIFACT_INDEX.csv`](templates/ARTIFACT_INDEX.csv).

## Usage Rule

Templates are reference starting points. Before operational use:

1. map them to local policy;
2. assign owners;
3. test control behavior;
4. version changes;
5. record the applicable approval.

Human-readable templates include metadata blocks. Structured artifacts carry schema/artifact metadata in the file or artifact index.

[Back to outline](outline.md)
