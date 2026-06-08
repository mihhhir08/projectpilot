---
name: prompt-for-claude-code
description: "Generate high-quality Claude Code prompts from an idea, blueprint, feature spec, bug report, or repo goal. Use when the user wants to hand off work to Claude Code with clear architecture, implementation, and QA instructions."
---

# Prompt For Claude Code

Use this skill to create prompts that help Claude Code build cleaner software.

## Prompt Requirements

Every generated prompt should include:

- Context: project goal and current state.
- Outcome: what Claude Code must produce.
- Architecture: boundaries, modules, and style constraints.
- Implementation Rules: readable code, existing patterns, minimal churn.
- UX Requirements: states, responsiveness, copy, accessibility when relevant.
- Testing Requirements: exact checks to run or infer.
- Deliverables: files, docs, summaries.
- Stop Conditions: when to ask for clarification.

## Template

```txt
You are working in a fresh/existing repo.

Goal:
...

Build:
...

Architecture constraints:
- ...

Implementation rules:
- Read the existing code first.
- Follow local conventions.
- Keep modules focused and readable.
- Avoid unrelated refactors.

UX requirements:
- ...

Tests and verification:
- ...

Before finishing:
- Run verification.
- Fix errors.
- Summarize changed files, tests run, and remaining risks.
```

Make the final prompt practical enough to paste directly into Claude Code.
