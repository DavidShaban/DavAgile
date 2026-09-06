# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

> GAD combines deliberate milestone planning, adaptive Agile execution, AI-assisted delivery, and explicit human authority. The method is designed to gain the speed and analytical leverage of AI without allowing convenience, confidence, or automation to silently become authority.


## How to Use This Book

- Start with [Introduction](introduction.md) for the problem GAD solves and the overall operating model.
- Use Chapters 1–4 to establish governance, authority, roles, and lifecycle controls.
- Use Chapters 5–7 to configure the hybrid Waterfall–Agile–AI delivery engine.
- Use Chapters 8–11 to implement decision logic, tooling, pilots, evidence, metrics, and assurance.
- Use Chapters 12–13 to scale GAD and run continuous improvement.
- Use the appendices as an implementation kit.
- Configuration files under [`templates/`](templates/) are reference implementations, not vendor-mandated requirements.

## Table of Contents

- [Introduction — Why Governed Adaptive Delivery](introduction.md)
   - The delivery problem GAD addresses
   - Hybrid design: Waterfall + Agile + AI
   - Human Project Hub
   - Core operating loop
   - What GAD is and is not

1. [Chapter 1 — Foundations and Core Principles](chapter_01.md)
   - GAD design principles
   - Authority before autonomy
   - Evidence before promotion
   - Fail-closed delivery
   - Historical truth preservation
   - Proportional governance

2. [Chapter 2 — Authorization Levels and Human Authority](chapter_02.md)
   - A0–A4 classification
   - Authorization triggers
   - Delegation boundaries
   - Human Decision state
   - Approval evidence
   - Cross-reference: [`AUTHORIZATION_MATRIX.csv`](templates/AUTHORIZATION_MATRIX.csv)

3. [Chapter 3 — Human–AI Team and Agent Roles](chapter_03.md)
   - Human Project Hub
   - Orchestrator, planner, worker, validator, governance, evidence, reporting, specialist agents
   - Separation of duties
   - Agent lifecycle boundaries
   - Cross-reference: [`agent_manifest_example.yaml`](templates/agent_manifest_example.yaml)
   - Cross-reference: [`RACI_MATRIX.csv`](templates/RACI_MATRIX.csv)

4. [Chapter 4 — Governance Architecture and Lifecycle](chapter_04.md)
   - Governance layers
   - Work-item lifecycle
   - Agent lifecycle
   - Change control
   - Exception and remediation handling
   - Status integrity

5. [Chapter 5 — Waterfall Planning and Stage Gates](chapter_05.md)
   - Charter and outcome baseline
   - Architecture, compliance, budget, and milestone gates
   - Dependency mapping
   - Release planning
   - Re-baselining
   - Cross-reference: [`PILOT_GATE_REGISTER.csv`](templates/PILOT_GATE_REGISTER.csv)

6. [Chapter 6 — Agile Execution and Flow Control](chapter_06.md)
   - Backlog architecture
   - Ready criteria
   - Iteration and Kanban execution
   - WIP limits
   - Reviews and retrospectives
   - Flow metrics
   - Definition of Done with evidence

7. [Chapter 7 — AI-Assisted Execution, Monitoring, and Predictive Risk](chapter_07.md)
   - Task automation
   - Real-time monitoring
   - Feedback loops
   - Predictive analytics
   - Confidence and uncertainty
   - Safe optimization boundaries
   - Escalation triggers

8. [Chapter 8 — Decision Logic, Risk, Evidence, and Exceptions](chapter_08.md)
   - Five-question decision model
   - Risk and reversibility
   - Evidence sufficiency
   - Decision records
   - Exceptions and controlled failure
   - Recovery and rollback
   - Cross-reference: [`decision_record_template.md`](templates/decision_record_template.md)
   - Cross-reference: [`evidence_package_template.md`](templates/evidence_package_template.md)

9. [Chapter 9 — Tooling Implementation: Jira + GitHub](chapter_09.md)
   - Jira work types, states, fields, validators, queues, dashboards
   - GitHub branch protection, pull requests, checks, environments
   - Traceability between issue, change, evidence, approval, and release
   - Private human-control views
   - Reference code blocks
   - Cross-reference: [`jira_workflow_reference.yaml`](templates/jira_workflow_reference.yaml)
   - Cross-reference: [`github_ruleset_reference.json`](templates/github_ruleset_reference.json)

10. [Chapter 10 — Pilot Setup and Governed Execution](chapter_10.md)
    - Pilot scope
    - Preflight
    - Gate model
    - Synthetic and low-risk validation
    - Human Control Dashboard
    - Nine reference control queues
    - Readiness decision
    - `READY_FOR_PILOT_AUTHORIZATION` vs `REMEDIATION_REQUIRED`
    - Cross-reference: [`pilot_readiness_checklist.md`](templates/pilot_readiness_checklist.md)

11. [Chapter 11 — Metrics, Evidence, Assurance, and Audit](chapter_11.md)
    - Control effectiveness
    - Unauthorized action tracking
    - Evidence completeness
    - Flow, quality, and decision metrics
    - Audit sampling
    - Assurance reviews
    - Cross-reference: [`KPI_CATALOG.csv`](templates/KPI_CATALOG.csv)

12. [Chapter 12 — Scaling, Maturity, and Enterprise Adoption](chapter_12.md)
    - GAD maturity model
    - Team and portfolio scaling
    - Federated governance
    - Policy-as-code
    - Model and agent portfolio governance
    - Enterprise control integration

13. [Chapter 13 — Operating Playbook and Continuous Improvement](chapter_13.md)
    - Daily/weekly/monthly cadence
    - Change proposals
    - Method versioning
    - Retrospective-to-policy loop
    - Training and onboarding
    - Continuous control improvement

## Appendices

A. [Appendix A — Templates and Artifacts](appendix_a_templates.md)
   - Authorization matrix
   - Evidence package
   - Decision record
   - Change request
   - Incident/remediation record
   - RACI matrix
   - Pilot gates and readiness checklist

B. [Appendix B — Tools and Implementation Patterns](appendix_b_tools.md)
   - Jira implementation kit
   - GitHub implementation kit
   - Agent manifest pattern
   - Evidence repository pattern
   - Dashboard pattern

C. [Appendix C — Checklists](appendix_c_checklists.md)
   - Project startup
   - Work-item authorization
   - Iteration readiness
   - Release readiness
   - Pilot readiness
   - Incident closure
   - Audit closure

D. [Appendix D — Case Studies](appendix_d_case_studies.md)
   - AI documentation project
   - Governed software release
   - GAD-PILOT-01 human-control dashboard pattern
   - Historical remediation preservation pattern

E. [Appendix E — Glossary](appendix_e_glossary.md)
   - Authorization, autonomy, evidence, gate, Human Project Hub, remediation, etc.

F. [Appendix F — Reference Configurations](appendix_f_reference_configurations.md)
   - Jira workflow YAML
   - GitHub ruleset JSON
   - Agent manifest YAML
   - Naming conventions and traceability IDs

G. [Appendix G — Change Log and Versioning](appendix_g_change_log.md)
   - Documentation release history
   - Method change-log format
   - Compatibility and migration expectations

H. [Appendix H — Frequently Asked Questions](appendix_h_faq.md)
   - Proportional governance
   - Human/AI disagreement
   - Vendor model changes
   - Scaling and authorization questions

## Book Navigation and Packaging

- [Editorial Remediation Register](EDITORIAL_REMEDIATION_REGISTER.md)
- [Documentation Release 1.1 Notes](RELEASE_NOTES.md)
- [Combined single-file edition](BOOK_COMBINED.md)
- [README](README.md)
- [`templates/`](templates/) — reusable implementation artifacts
- `MANIFEST.sha256` — integrity hashes for every packaged file

## Suggested Reading Paths

### Executive / Sponsor
Introduction → Chapter 1 → Chapter 2 → Chapter 3 (roles primer) → Chapter 5 → Chapter 10 → Chapter 11 → Chapter 12

### Delivery Lead / PM / Agile Coach
Introduction → Chapters 1–6 → Chapter 8 → Chapters 10–13

### AI / Automation Lead
Introduction → Chapters 2–4 → Chapter 7 → Chapter 8 → Chapter 9 → Chapter 11

### Governance / Audit / Compliance
Introduction → Chapters 1–4 → Chapter 8 → Chapter 9 → Chapter 10 → Chapter 11 → Appendices A–C and H

### Developer / Team Member
Introduction → Chapter 3 → Chapter 6 → Chapter 7 → Chapter 8 → Chapter 9 → Appendices C and F

### Security / Risk Officer
Introduction → Chapters 1–2 → Chapter 4 → Chapter 7 → Chapter 8 → Chapter 12 → Appendices C, G, and H

### Jira / GitHub Administrator
Chapter 2 → Chapter 4 → Chapter 9 → Chapter 10 → Appendices B and F
