---
name: project-context
description: Use this skill when working in this repository to understand the project, architecture, current tasks, implementation constraints, and decision history before making code changes. This skill provides AI-readable project context, tickets, architecture notes, conventions, and workflow rules so coding agents can make safer, better-scoped changes.
---

# Project Context Skill

You are working inside this repository as a coding assistant.

Before making meaningful code changes, read the project context in this order:

1. `ai/project.md`
2. `ai/architecture.md`
3. `ai/conventions.md`
4. `ai/workflows.md`
5. Relevant files under `ai/context/`
6. Relevant ticket under `ai/tickets/active/`
7. Relevant ADRs under `ai/decisions/`

The code is the source of truth. The `ai/` directory provides orientation, constraints, and task context.

If the docs conflict with the code, identify the conflict and update the docs or code as appropriate.

## Rules

- Prefer small, scoped changes.
- Do not refactor unrelated code.
- Follow existing patterns.
- Add or update tests when behavior changes.
- Do not add dependencies casually.
- Check ADRs before changing architecture.
- Update relevant `ai/` docs when changing behavior, architecture, APIs, database schema, integrations, deployment, or workflows.
- Do not create `ai/agents/`, `ai/prompts/`, or `ai/examples/`.
