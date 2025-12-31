# Create Pull Request

Generate a comprehensive PR description for the current branch.

> **Related Rule**: `gitflow/RULE.md`

## Steps

1. Run `git diff <base-branch>...HEAD` to analyze changes
2. Review all commits on this branch
3. Extract the Jira ticket ID from the branch name (e.g., `feature/cor-13727-some-feature` → `COR-13727`)
4. Generate PR description following the format defined in `gitflow/RULE.md`

---

Generate the PR description based on the actual changes in this branch.
