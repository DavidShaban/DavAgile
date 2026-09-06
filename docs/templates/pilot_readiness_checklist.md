---
artifact_id: ART-PILOT-003
schema_version: "1.1"
documentation_release: "1.1"
method_version: "1.2"
owner: "GAD Method Owner"
status: "REFERENCE_TEMPLATE"
---

# GAD Pilot Readiness Checklist

## Predefined Pilot Outcome Controls
- [ ] Success criteria documented
- [ ] Failure/hold criteria documented
- [ ] Kill criteria documented
- [ ] KPI/data-collection plan documented
- [ ] Duration/work-volume bound documented
- [ ] Required sign-off roles documented

## P0 — Identity & Scope
- [ ] Pilot name and owner confirmed
- [ ] Human Project Hub confirmed
- [ ] Source-of-truth project/repository confirmed
- [ ] Scope and exclusions documented
- [ ] Required prerequisites resolved

## P1 — Authorization
- [ ] A0–A4 matrix approved
- [ ] A3/A4 transitions tested
- [ ] Expired/missing approval blocks execution
- [ ] Standing A2 delegations documented

## P2 — Workflow
- [ ] Ready criteria enforced
- [ ] Validation state works
- [ ] Human Decision state works
- [ ] Remediation Required state works
- [ ] Historical results are preserved

## P3 — AI Boundary
- [ ] Agent/model identities documented
- [ ] Tool permissions bounded
- [ ] Data boundaries tested
- [ ] Authority ceiling tested
- [ ] Escalation works
- [ ] Self-expansion prohibited

## P4 — Evidence
- [ ] Evidence IDs work
- [ ] Test/validation evidence linked
- [ ] Decision evidence linked
- [ ] Recovery evidence linked
- [ ] Evidence sufficiency rubric applied
- [ ] Evidence completeness can be measured

## P5 — Human Control
- [ ] Dashboard is private/restricted
- [ ] Human Decision queue validated
- [ ] A3/A4 approval queue validated
- [ ] Evidence Missing queue validated
- [ ] Validation Failed queue validated
- [ ] Remediation Required queue validated
- [ ] Dependency Blocked queue validated
- [ ] WIP/Flow Exception queue validated
- [ ] Ready for Release Authorization queue validated
- [ ] Unauthorized/Policy Exception queue validated
- [ ] Completed historical records excluded from active queues

## P6 — Recovery
- [ ] Controlled failure case executed
- [ ] No unauthorized side effect
- [ ] Recovery/rollback demonstrated
- [ ] Remediation evidence captured

## P7 — Final Readiness
- [ ] Every mandatory gate PASS
- [ ] No unresolved blocker
- [ ] No unresolved prerequisite
- [ ] Control-by-control result recorded
- [ ] Final readiness outcome is exactly one:
  - [ ] READY_FOR_PILOT_AUTHORIZATION
  - [ ] REMEDIATION_REQUIRED
