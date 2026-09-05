# Apply This Bundle to GitHub

## Step 1 — Repository Selection

Preferred pilot repository:

```text
gad-pilot-01
```

Create a new repository or use an explicitly bounded existing repository.

## Step 2 — Apply Through Pull Request

1. create a configuration branch;
2. copy this bundle into repository root;
3. rename `CODEOWNERS.example` to `.github/CODEOWNERS`;
4. replace owner placeholders;
5. commit;
6. open PR referencing Jira configuration record;
7. run `GAD PR Governance Check`;
8. review;
9. merge only after checks/review.

## Step 3 — Protect Default Branch

Configure ruleset/branch protection:

```text
require pull request
require review
require status check: GAD PR Governance Check
block force push
restrict deletion
```

## Step 4 — Configure Simulated Environment

Environment:

```text
gad-a3-simulated-production
```

Where supported, require Human Project Hub reviewer and prevent self-review.

Do not store production secrets.

## Step 5 — Validate

Test:

```text
[ ] PR without Jira key fails
[ ] PR missing Evidence section fails
[ ] agent manifest modification requires review
[ ] simulated deployment has no production side effect
[ ] A3 remains blocked without required approval where enforceable
```

## Step 6 — Update Jira

Record:

- repository;
- default branch;
- PR;
- merge commit;
- workflow run;
- environment configuration evidence;
- limitations.

Only after this should SIM-08 preflight be reconsidered.
