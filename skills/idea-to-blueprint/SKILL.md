---
name: idea-to-blueprint
description: "Turn a rough product or feature idea into a clean build blueprint with product goal, user flows, architecture, data model, implementation order, acceptance criteria, and QA plan. Use before coding when the user has an idea but no clear spec."
---

# Idea To Blueprint

Use this skill when the user brings a rough app, feature, plugin, CLI, website, or product idea and wants a better plan before implementation.

## Workflow

1. Restate the idea in one sentence.
2. Identify the target user and the job-to-be-done.
3. Ask at most three blocking questions only if the answer cannot be reasonably inferred.
4. Produce a build blueprint.
5. Include a Claude Code-ready implementation prompt when useful.

## Blueprint Format

Return these sections:

- Product Goal: one crisp sentence.
- Target User: who it serves and why they care.
- Core Workflows: the 2-5 flows that matter most.
- Must-Haves: the smallest complete product surface.
- Non-Goals: what should stay out to protect quality.
- Architecture: modules, boundaries, data flow, and storage.
- Data Model: entities, fields, relationships, and validation.
- UI/UX Notes: empty states, loading states, errors, mobile, accessibility.
- Implementation Order: ordered tasks with checkpoints.
- Acceptance Criteria: concrete behaviors that define done.
- QA Plan: tests, build checks, smoke tests, edge cases.
- Claude Code Prompt: a complete prompt the user can paste into Claude Code.

## Quality Rules

- Prefer a small complete product over a bloated partial one.
- Choose boring, durable architecture unless the idea truly needs novelty.
- Name the main tradeoffs clearly.
- Keep implementation tasks scoped and testable.
- Do not invent unnecessary services, databases, or frameworks.
- Optimize for a project another developer can understand quickly.
