# GAD v1.2 — Modular Markdown Book
**Documentation Release:** 1.1  
**Method Version:** 1.2  
**Publication Baseline:** 6 September 2026

This package is the corrected documentation release produced after reconciling the formal editorial review against the actual Documentation Release 1.0 files.

## Start Here

Open [`outline.md`](outline.md).

## Editorial Reconciliation

- [`EDITORIAL_REMEDIATION_REGISTER.md`](EDITORIAL_REMEDIATION_REGISTER.md) — 49-item human-readable remediation register.
- [`EDITORIAL_REMEDIATION_REGISTER.csv`](EDITORIAL_REMEDIATION_REGISTER.csv) — machine-readable register.
- [`RELEASE_NOTES.md`](RELEASE_NOTES.md) — release summary and method-version decision.

The underlying GAD method remains **v1.2**. Documentation Release 1.1 clarifies and operationalizes the method without changing the A0–A4 authorization semantics or the existing Level 0–5 maturity model.

## Contents

- `outline.md`
- `introduction.md`
- `chapter_01.md` … `chapter_13.md`
- `appendix_a_templates.md` … `appendix_h_faq.md`
- `EDITORIAL_REMEDIATION_REGISTER.md/.csv`
- `RELEASE_NOTES.md`
- `BOOK_COMBINED.md`
- `templates/`
- `MANIFEST.sha256`
- `MANIFEST.csv`

## Naming

Prospective convention:
- human-readable Markdown: `kebab-case.md`;
- new machine-consumed CSV/YAML/JSON: `UPPER_SNAKE.*`.

Documentation Release 1.0 structured filenames are retained where renaming would break compatibility.

## Style

- Use “AI-assisted” in prose and “AI-Assisted” in titles.
- Use the serial comma.
- Use present tense for method definitions and imperative voice for checklists.
- Preserve historical failures/remediations rather than rewriting them.
- A recommendation, confidence score, tool permission, or AI-to-AI handoff does not create authorization.

## Integrity

`MANIFEST.sha256` is the standard byte-integrity manifest. `MANIFEST.csv` adds artifact/schema metadata.
