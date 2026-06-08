---
name: clean-implementation
description: "Guide AI-assisted implementation with readable code, focused modules, existing patterns, minimal abstractions, tests, and verification. Use while coding after a plan or spec exists."
---

# Clean Implementation

Use this skill when implementing a planned change.

## Implementation Contract

- Read the existing code before editing.
- Follow local patterns, naming, and architecture.
- Keep functions and files focused.
- Prefer clear data flow over clever abstractions.
- Avoid unrelated refactors and churn.
- Add tests proportional to risk.
- Run the relevant verification commands.
- Summarize what changed and what was verified.

## Coding Checklist

- Module boundaries are clear.
- New code has descriptive names.
- Logic is easy to scan top-to-bottom.
- Side effects are isolated.
- Error states are handled.
- Public APIs and CLI contracts are stable.
- No secrets, credentials, or local machine paths are committed.
- Dependencies are justified.

## When The Plan Looks Wrong

Pause and revise the plan if:

- the requested design conflicts with existing architecture,
- the implementation requires broad unrelated changes,
- tests reveal a deeper bug,
- a simpler solution becomes obvious after reading the code.

Do not continue blindly. Explain the better path and proceed when the tradeoff is clear.
