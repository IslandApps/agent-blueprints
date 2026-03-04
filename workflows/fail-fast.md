## Reliability & Error Recovery

### Failed Fix Policy (CRITICAL)
When a proposed solution or code change fails to resolve the issue (via test failure, build error, or user feedback):

1. **REVERT immediately** to the last known working state before attempting a different approach:
   ```bash
   # Revert specific files
   git checkout -- <file1> <file2>

   # Or reset to last commit if multiple files changed
   git reset --hard HEAD
   ```

2. **NEVER layer fixes** - Do NOT add new code on top of failed solutions to "patch" them. This creates:
   - Unmaintainable code bloat
   - Hard-to-debug interactions between partial fixes
   - Regressions in unrelated functionality

3. **VERIFY every fix** - Run relevant build/test commands before considering a task complete:
   ```bash
   npm run build    # Verify production build succeeds
   npm run lint     # Check for linting errors
   npm run dev      # Test in development environment
   ```

4. **Document learnings** - If a fix fails, document why it failed in a comment or commit message to prevent repeating the same mistake.

**Rationale:** Clean reverts preserve codebase health and make debugging easier. A failed fix is valuable data—use it to inform your next approach, but don't let it pollute the codebase.
