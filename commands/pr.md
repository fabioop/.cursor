# Create Pull Request Description

Generate a comprehensive PR description for the current branch.

## Steps

1. Run `git diff develop...HEAD` to analyze changes
2. Review all commits on this branch
3. Extract the Jira ticket ID from the branch name (e.g., `feature/cor-13727-some-feature` → `COR-13727`)
4. Generate PR description following the Markdown format:

```markdown
## Description

[Describe what this PR does, the changes made, and any relevant context]

## Issues

[COR-XXXXX](https://swordhealth.atlassian.net/browse/COR-XXXXX)

## Feature Branch

[COR-XXXXX](https://cor-xxxxx-[project-name].staging.swordhealth.com)
```

---

Generate the PR description based on the actual changes in this branch.
