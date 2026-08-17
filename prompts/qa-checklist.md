# QA Checklist Prompt

Use ProjectPilot to run a pre-ship QA pass.

Inputs:

- Intended change and acceptance criteria
- Changed files or comparison base
- Supported environments and primary user flow
- Available build, test, lint, and type-check commands

Check:

- Tests/build/lint/typecheck
- Primary user flow
- Changed files
- Dependency changes
- Secrets/local artifacts
- Docs accuracy
- Remaining risks

For every check, report the evidence observed. Distinguish a passed check from one that could not be run.

Return:

- Status: Ready or Needs Fixes
- Blocking findings
- Verification commands and results
- Manual QA performed
- Unverified areas and remaining risks
- Recommended next action

Use `Ready` only when no blocking finding remains and the primary workflow has been verified.
