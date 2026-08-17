# ProjectPilot

**Turn rough AI coding ideas into clean, shippable software.**

ProjectPilot is an open-source assistant workflow pack for **Codex** and **Claude Code**. It helps AI-assisted builders move from rough ideas to clean architecture, implementation plans, readable code, UX polish, QA checklists, and high-quality Claude Code prompts.

The goal is simple: keep the speed of AI-assisted building without letting project quality collapse.

## Why This Exists

AI coding tools are fast, but speed alone can produce messy projects:

- unclear architecture
- random abstractions
- weak UX states
- missing tests
- bloated prompts
- code that works once but is hard to maintain

ProjectPilot gives the agent a senior-engineer workflow before and during the build.

## The Wow Feature

### Project Brief -> Build Blueprint

Give ProjectPilot a rough idea:

```txt
Build me a habit tracker with streaks and reminders.
```

It turns that into:

- product goal
- target user
- core workflows
- must-have features
- non-goals
- architecture
- data model
- UX notes
- implementation order
- acceptance criteria
- QA plan
- Claude Code-ready prompt

That means the coding agent starts with a real blueprint instead of a vague wish.

## Quick Start

Choose the workflow that matches the work in front of you:

| Starting point | Use | Result |
| --- | --- | --- |
| Rough product idea | `idea-to-blueprint` | Product and engineering blueprint |
| Existing feature request | `feature-to-spec` | Implementation-ready specification |
| Approved plan | `clean-implementation` | Focused implementation with verification |
| Working interface | `ux-quality-pass` | Prioritized UX review and polished copy |
| Change ready to publish | `qa-before-ship` | Release-readiness report |
| Handoff to Claude Code | `prompt-for-claude-code` | Copy-paste-ready implementation prompt |

Start with one workflow, review its output, and move to the next only when the current stage is clear.

## What Is Included

### Codex Skills

- `idea-to-blueprint` - rough idea to product/engineering blueprint
- `feature-to-spec` - feature request to implementation-ready spec
- `clean-implementation` - readable code and architecture guardrails while coding
- `ux-quality-pass` - polish pass for apps, CLIs, reports, and docs
- `qa-before-ship` - verification workflow before sharing or publishing
- `prompt-for-claude-code` - copy-paste-ready Claude Code prompts

### Claude Code Support

ProjectPilot also includes Markdown command prompts:

- `claude-code/commands/projectpilot-blueprint.md`
- `claude-code/commands/projectpilot-feature.md`
- `claude-code/commands/projectpilot-build.md`
- `claude-code/commands/projectpilot-qa.md`
- `claude-code/commands/projectpilot-prompt.md`

And a repo-level template:

- `claude-code/CLAUDE.md.template`

Copy the command files into your Claude Code command setup, or paste them directly into Claude Code.

## Example Usage

### In Codex

```txt
Use ProjectPilot to turn this idea into a clean build blueprint:

I want to build a subscription tracker that reminds users before renewals.
```

```txt
Use ProjectPilot clean-implementation for this feature. Inspect the repo first, follow existing patterns, implement, and run verification.
```

```txt
Use ProjectPilot qa-before-ship and tell me if this project is ready to publish.
```

### In Claude Code

Paste:

```txt
Use ProjectPilot to create a build blueprint for this idea:
[your idea]
```

Or use the command files under `claude-code/commands/`.

## Suggested Workflow

1. Start with `idea-to-blueprint`.
2. Convert the next feature with `feature-to-spec`.
3. Build with `clean-implementation`.
4. Polish with `ux-quality-pass`.
5. Verify with `qa-before-ship`.
6. Generate a sharper prompt with `prompt-for-claude-code` when handing off to Claude Code.

## Repository Structure

```txt
projectpilot/
  .codex-plugin/
    plugin.json
  skills/
    idea-to-blueprint/
    feature-to-spec/
    clean-implementation/
    ux-quality-pass/
    qa-before-ship/
    prompt-for-claude-code/
  claude-code/
    commands/
    CLAUDE.md.template
  prompts/
  templates/
  examples/
```

## Installation

For Codex plugin development, place this repo in your local plugins directory or install it through your Codex plugin marketplace setup.

For Claude Code, run the following from the ProjectPilot repository root, replacing the placeholder with your project path:

```sh
PROJECT_DIR=/path/to/your/project
mkdir -p "$PROJECT_DIR/.claude/commands"
cp claude-code/commands/*.md "$PROJECT_DIR/.claude/commands/"
```

If the target project does not already have a `CLAUDE.md`, you can also copy the included template:

```sh
test -e "$PROJECT_DIR/CLAUDE.md" || cp claude-code/CLAUDE.md.template "$PROJECT_DIR/CLAUDE.md"
```

If `CLAUDE.md` already exists, merge the relevant guidance manually instead of overwriting it.

## Contributing

Good contributions include:

- new workflow skills
- better Claude Code commands
- stronger QA checklists
- real before/after examples
- framework-specific blueprint templates

Keep the project focused on one promise: helping AI-assisted builders ship cleaner software.

## License

MIT
