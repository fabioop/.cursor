# Generate Quality Assurance Tests

Generate core QA test cases for the feature being developed.

## Steps

1. **Analyze Changes**
   - Run `git diff develop...HEAD` to review branch changes, OR
   - Run `git diff --staged` if working with staged files only
   - Identify all modified/added components, functions, and APIs

2. **Understand the Feature**
   - Determine the feature's purpose and expected behavior
   - Identify user-facing functionality
   - Map data flow and dependencies

3. **Generate Test Cases**
   - Save the test cases to a file called `qa.md`
   - Focus on the most critical core test scenarios (typically 3-5 scenarios)
   - Use a single table format

## Output Format

```
# QA Test Cases - [Feature Name]

## Feature Overview

[Brief description of the feature and its purpose]

---

## Core Test Cases

| Scenario | Steps | Expected Outcome |
|----------|-------|------------------|
| 1. [Scenario name] | 1. Step one<br>2. Step two<br>3. Step three | Expected result description |
| 2. [Scenario name] | 1. Step one<br>2. Step two | Expected result description |
```

**Requirements:**

- Include only the most essential test cases (happy path, error scenarios, edge cases)
- Steps should be numbered and separated by `<br>` tags
- Keep scenarios concise and focused on core functionality
- Generate test cases based on the actual changes in the branch or staged files
