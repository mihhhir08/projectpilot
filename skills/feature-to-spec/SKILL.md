---
name: feature-to-spec
description: "Convert a feature request into an engineering-ready spec with behavior, edge cases, affected files, acceptance criteria, and test plan. Use before implementing a feature in an existing project."
---

# Feature To Spec

Use this skill when the user wants to add or change a feature and needs a precise spec before coding.

## Workflow

1. Inspect the repo if available.
2. Identify existing patterns, relevant modules, and likely ownership boundaries.
3. Convert the request into implementation-ready requirements.
4. Highlight ambiguity and resolve it with reasonable defaults when safe.

## Spec Format

- Feature Summary: what changes for the user.
- Current Behavior: what exists today.
- Desired Behavior: exact new behavior.
- Edge Cases: errors, empty states, permissions, invalid inputs, slow paths.
- Affected Areas: files, modules, APIs, components, data model.
- Architecture Fit: how to keep the change aligned with existing code.
- Acceptance Criteria: checklist of observable outcomes.
- Test Plan: unit, integration, smoke, and manual checks.
- Implementation Notes: sequencing, risks, and rollback considerations.

## Guardrails

- Keep the spec coupled to the codebase that exists.
- Avoid unrelated refactors.
- Prefer small changes that compose.
- Include explicit non-goals.
- Call out missing tests or weak architecture before coding.
