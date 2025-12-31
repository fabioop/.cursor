# Run Tests and Fix Failures

## Steps

1. **Run Test Suite**
   - Execute: `npm test` (or `yarn test` / `pnpm test`)
   - Capture all output
   - Identify failing tests

2. **Analyze Failures**
   - Categorize: flaky, broken, or new failures
   - Check if related to recent changes
   - Prioritize by impact

3. **Fix Systematically**
   - Fix one issue at a time
   - Re-run affected tests after each fix
   - Ensure no regressions

## For Each Failure

1. Show the error message
2. Explain the root cause
3. Provide the fix
4. Verify the fix works

## Common Issues to Check

- Mock not properly configured
- Async operations not awaited
- State not reset between tests
- Component not wrapped with required providers
- Outdated snapshots

Continue until all tests pass.
