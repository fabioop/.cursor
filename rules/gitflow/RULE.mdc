---
description: Gitflow Workflow Rules. These rules should be applied when performing git operations.
---
# Gitflow Workflow Rules

## Main Branches

### master (or main)

- Contains production-ready code
- Never commit directly to master
- Only accepts merges from:
  - hotfix/* branches
  - feature/* branches
  - release/* branches

### develop

- Main development branch
- Contains latest delivered development changes
- Source branch for feature branches
- Never commit directly to develop

## Supporting Branches

### feature/*

- Branch from: develop
- Merge back into: develop
- Naming convention: `feature/cor-[jira-id]-allow-fb-deploy`
- Example: `feature/cor-13727-allow-fb-deploy`
- Must be up-to-date with develop before creating PR
- Delete after merge

### release/*

- Branch from: master
- Merge back into: master
- Naming convention: `release/master/year/currentWeek`
- Example: `release/master/2025/w50`

## Commit Messages

- Format: `type(scope): description`
- Types:
  - feat: New feature
  - fix: Bug fix
  - docs: Documentation changes
  - style: Formatting, missing semicolons, etc.
  - refactor: Code refactoring
  - test: Adding tests
  - chore: Maintenance tasks

## Version Control

### Semantic Versioning

- MAJOR version for incompatible API changes
- MINOR version for backwards-compatible functionality
- PATCH version for backwards-compatible bug fixes

## Pull Request Rules

1. All changes must go through Pull Requests
2. Required approvals: minimum 1
3. CI checks must pass
4. No direct commits to protected branches (master, develop)
5. Branch must be up to date before merging
6. Delete branch after merge

### PR Description Format

All PRs must follow this format:

```markdown
## Description

[Describe what this PR does, the changes made, and any relevant context]

## Issues

[COR-XXXXX](https://swordhealth.atlassian.net/browse/COR-XXXXX)

## Feature Branch

[COR-XXXXX](https://cor-xxxxx-[project-name].staging.swordhealth.com)
```

## Branch Protection Rules

### master & develop

- Require pull request reviews
- Require status checks to pass
- Require branches to be up to date
- Include administrators in restrictions
- No force pushes
- No deletions

## Release Process

1. This is done manually, always.
