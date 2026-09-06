# GAD v1.2: Governed Adaptive Delivery
**Subtitle:** A Human-Centered Hybrid Method for AI-Assisted, Governed, Adaptive Delivery  
**Method Version:** 1.2  
**Documentation Release:** 1.1  
**Author:** David Betzold  
**Publication Baseline:** 6 September 2026  
**Status:** Corrected modular book documentation release

# Appendix G — Change Log and Versioning

## Version-Control Log

Only version history supported by the current documentation artifacts is recorded here. Proposed dates/history from the editorial review are **not** converted into historical fact without source evidence.

| Method Version | Documentation Release | Date | Author | Summary | Migration Impact |
|---|---|---|---|---|---|
| 1.2 | 1.0 | 6 September 2026 | David Betzold | Initial modular book documentation baseline | Baseline |
| 1.2 | 1.1 | 6 September 2026 | David Betzold | Editorially reconciled release: stronger authority evidence, lifecycle ownership, escalation, model provenance, KPI coverage, pilot controls, templates, FAQ, and remediation register | Documentation/tooling-reference enhancement; no underlying method-version change |

## Documentation Release 1.1 Decision

The underlying **GAD method remains v1.2**. Release 1.1 clarifies existing authorization semantics rather than replacing them; preserves A0–A4 as action-authorization levels; preserves the existing Level 0–5 maturity model; adds operational detail and reference controls; and does not invent pre-1.0 historical releases.

## Method Change-Log Format

```markdown
## GAD vX.Y
- Effective date:
- Approved by:
- Reason:
- Evidence basis:
- Added:
- Changed:
- Deprecated:
- Removed:
- Control impact:
- Migration actions:
- Backward compatibility:
```

## Semver-Style Method Versioning Guidance

- **Major**: incompatible change to core authority/governance semantics or lifecycle contract.
- **Minor**: compatible new method capability, control family, or normative mechanism.
- **Patch / Documentation Release**: clarification, correction, new examples, templates, reference implementations, or editorial changes that do not alter the underlying method contract.

A documentation release may advance independently while the method version remains unchanged.

## Migration Rule

A new methodology version should not silently invalidate active projects. For each material change define affected projects, required migration, grace period if applicable, evidence, authority, deprecated controls, and effective date.

## Historical Preservation

Prior method/documentation versions and project decisions remain retrievable for audit. Historical decisions are interpreted using the version/schema under which they were made.

## Style Guide

- Use **AI-assisted** in prose; **AI-Assisted** only in titles/headings.
- Use `governance-by-design`, `human-in-the-loop`, `human-on-the-loop`, `fail-closed`, and `authority-before-autonomy` as fixed compounds.
- Use the serial comma.
- Use present tense for method definitions and imperative voice for checklists.
- Use `Chapter N — Title` and `Appendix X — Title`.
- Human-readable Markdown uses `kebab-case.md`; new machine artifacts use `UPPER_SNAKE` filenames.
- Define key terms at first consequential use and link to the glossary when useful.

[Back to outline](outline.md)
