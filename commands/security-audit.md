# Security Audit

Perform a comprehensive security review of the codebase.

> **Related Rule**: `security/RULE.md`

## Steps

1. **Dependency Check**
   - Run: `npm audit`
   - Check for known CVEs
   - Identify outdated packages with security issues

2. **Code Review**
   - Scan for issues against the security rule checklist
   - Check for hardcoded secrets, injection vulnerabilities, improper auth

3. **Report Findings**

## Output Format

For each issue found:

| Field | Description |
|-------|-------------|
| **Severity** | CRITICAL / HIGH / MEDIUM / LOW |
| **Location** | File and line |
| **Description** | What the vulnerability is |
| **Remediation** | Steps to fix |

### Severity Definitions

- **CRITICAL**: Immediate exploitation possible, data breach risk
- **HIGH**: Significant security risk, should fix before release
- **MEDIUM**: Security concern, fix in next sprint
- **LOW**: Minor issue, fix when convenient
