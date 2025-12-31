---
description: Modern JavaScript/ES6+ coding conventions and style guidelines
alwaysApply: true
---

# JavaScript Style Guide

## Modern ES6+ Syntax

- Use `const` by default, `let` when reassignment is needed, never `var`
- Use arrow functions for callbacks and non-method functions
- Use destructuring for objects and arrays
- Use spread operator for copying and merging
- Use template literals for string interpolation
- Use optional chaining (`?.`) and nullish coalescing (`??`)
- Prefer `async/await` over `.then()` chains

## Naming Conventions

- **PascalCase**: Components, classes, type definitions
- **camelCase**: Functions, variables, methods, properties
- **UPPER_SNAKE_CASE**: Constants, environment variables
- Use descriptive names with auxiliary verbs: `isLoading`, `hasError`, `canSubmit`, `shouldUpdate`

## Code Structure

- Early returns for error conditions and guard clauses
- Keep functions small and focused (single responsibility)
- Group related code together
- Order: imports, constants, main logic, helpers, exports

## Documentation

- Use JSDoc comments for functions and modules
- Document complex logic with inline comments
- Keep comments current with code changes

## Best Practices

- Prefer immutability where practical
- Avoid side effects in pure functions
- Use meaningful error messages
- Handle promises with proper error catching
- Prefer `Array.prototype` methods over loops when readable
