# GAD v1.2 — Documentation Release 1.1 Release Notes

## Release Decision

**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Date:** 6 September 2026

The editorial review was reconciled against the actual Documentation Release 1.0 package.

The underlying method version remains **GAD v1.2** because this release does not replace the A0–A4 authorization semantics, does not replace the existing Level 0–5 maturity model, and primarily adds definitions, traceability, operational detail, templates, reference tooling, and editorial corrections.

## Remediation Summary

- ACCEPTED: 40
- PARTIALLY_ACCEPTED: 6
- ALREADY_SATISFIED: 2
- REJECTED/NOT_APPLICABLE: 1

## Major Improvements

- strengthened A0–A4 granting/evidence/validity rules without changing their meaning;
- explicit delegation revocation and Human Decision state machine;
- authoritative lifecycle ownership in Chapter 4;
- escalation ownership and retention guidance;
- gate entry/exit/evidence/owner definitions and risk register;
- AI model/agent/prompt/config provenance and human override;
- evidence-sufficiency rubric and blast-radius assessment;
- richer Jira/GitHub governance-reference patterns;
- pilot success/kill/data/sign-off controls;
- explicit AI-error, governance-compliance, remediation-time, leading, and lagging KPIs;
- evidence-scored maturity assessment while retaining Level 0–5;
- COE/vendor governance;
- cadence, annual method audit, and retrospective-to-policy loop;
- Appendix H FAQ;
- expanded terminology and machine-readable glossary;
- 49-item editorial remediation register;
- new artifact index and integrity metadata.

## Compatibility

Documentation Release 1.0 structured reference filenames are retained when renaming them would break links.

`MANIFEST.sha256` remains standard. `MANIFEST.csv` adds artifact/schema metadata.

## Source-Review Discrepancy

The review's consolidated register omits H-11 and does not enumerate a substantive M-21 despite claiming 49 total / 21 medium findings. Documentation Release 1.1 preserves this discrepancy transparently in the remediation register.
