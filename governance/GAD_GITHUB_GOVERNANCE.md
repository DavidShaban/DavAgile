# GAD-PILOT-01 GitHub Governance Rules

## Protected Paths

```text
.github/workflows/**
agents/**
governance/**
```

## Merge Rules

- PR required.
- Required review for governed paths.
- GAD PR Governance Check required.
- No direct push to protected default branch.
- Failed checks are not bypassed during pilot validation.
- Agent manifest changes must reference Jira.
- A3/A4 changes require explicit Jira approval evidence.

## Deployment Boundary

```text
real production deployment = NOT AUTHORIZED
simulated deployment environment = ALLOWED after configured human gate
```

## Evidence Rule

PRs, workflow runs, commits, and agent-manifest versions are evidence references, not substitutes for human decisions.
