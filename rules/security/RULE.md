---
description: Security-first development practices
alwaysApply: true
---

# Security Guidelines

## Input Validation

- Validate all external input at system boundaries
- Never trust client-side validation alone
- Use schema validation (Zod, Yup) for structured data
- Sanitize user input before processing

## Secrets Management

- Never commit secrets to git
- Use `.env.local` for local secrets (in `.gitignore`)
- Access environment variables via `process.env` only on server
- No sensitive data in client bundles or browser storage

## XSS Prevention

- Avoid `dangerouslySetInnerHTML` unless absolutely necessary
- If required, sanitize HTML with DOMPurify or similar
- Use proper output encoding
- Content Security Policy headers in production

## CSRF Protection

- Use CSRF tokens for state-changing operations
- Validate origin headers on API routes
- SameSite cookie attributes

## Authentication & Authorization

- Verify authentication on every protected route
- Check authorization before sensitive operations
- Use secure session management
- Implement proper logout (invalidate tokens)

## API Security

- Rate limiting on public endpoints
- Input validation on all endpoints
- Proper error messages (no stack traces in production)
- Use HTTPS only
- Validate Content-Type headers

## Data Handling

- Don't log sensitive data (passwords, tokens, PII)
- Encrypt sensitive data at rest
- Use parameterized queries (prevent injection)
- Implement proper access controls

## Dependencies

- Keep dependencies updated
- Run `npm audit` regularly
- Review security advisories
- Avoid abandoned packages
