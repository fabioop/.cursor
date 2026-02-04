---
description: Deep code review guidelines for senior engineer review
---

# Code Review Guidelines

Perform deep, high-value reviews. Focus on what matters, skip the trivial.

## Review Focus Areas

### 1. Correctness

- Any potential bugs or logic errors?
- Edge cases handled properly?
- Race conditions possible?
- Null/undefined handled correctly?
- Off-by-one errors?

### 2. Security

- Is anything unsafe, injectable, or leaking data?
- Input validation at system boundaries?
- No sensitive data exposed to client?
- Proper authentication/authorization checks?
- No hardcoded secrets?

### 3. Architecture & Design

- Better abstractions possible?
- Proper separation of concerns?
- Following established patterns in the codebase?
- Appropriate coupling and cohesion?
- Will this scale?

### 4. Performance

- Obvious inefficiencies?
- N+1 queries or unnecessary loops?
- Missing memoization where needed?
- Unnecessary re-renders in React?
- Bundle size impact considered?

### 5. Maintainability

- Would another engineer easily extend this?
- Clear naming and structure?
- Sufficient but not excessive documentation?
- Test coverage for critical paths?

## Issue Classification

For each issue found:

1. **BLOCKING** - Must fix before merge
   - Security vulnerabilities
   - Correctness bugs
   - Breaking changes without migration

2. **ENHANCEMENT** - Should consider, not required
   - Performance improvements
   - Code organization
   - Better patterns

## What NOT to Review

- Spacing and formatting (use linters)
- Minor naming preferences
- Tabs vs spaces
- Subjective style choices

Unless these truly impact readability or maintainability.

## Review Output Format

For each issue:

1. Location (file and line if relevant)
2. Classification (BLOCKING or ENHANCEMENT)
3. Explain WHY it's a problem
4. Suggest a fix
