---
name: qa-before-ship
description: "Run a pre-ship quality pass for AI-assisted projects: verify build/tests, smoke-test core flows, inspect risky files, check docs, and produce a release-ready summary."
---

# QA Before Ship

Use this skill before the user shares, publishes, commits, or opens a pull request.

## QA Workflow

1. Inspect changed files.
2. Identify the project type and available verification commands.
3. Run tests, build, lint, typecheck, or smoke checks where appropriate.
4. Check for risky changes:
   - secrets or `.env` files
   - dependency and lockfile changes
   - generated artifacts
   - unrelated files
   - missing docs for user-facing behavior
5. Verify the primary user flow manually when possible.
6. Produce a concise ship summary.

## Ship Summary Format

- Status: Ready / Needs Fixes.
- What Changed: short bullets.
- Verification: commands run and results.
- Manual QA: flows checked.
- Risks: remaining concerns.
- Next Step: publish, commit, PR, or fix list.

Do not call something ready if tests or build fail.
