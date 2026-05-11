# Workflows

## Implementing a feature

1. Read the active ticket.
2. Read relevant project context.
3. Inspect the existing code.
4. Identify the smallest safe change.
5. Implement the change.
6. Verify visually in a browser at desktop and mobile widths.
7. Update relevant `ai/` documentation if behavior or structure changed.
8. Summarize what changed and why.

## Fixing a bug

1. Reproduce or understand the bug.
2. Identify expected behavior.
3. Locate the smallest faulty area.
4. Fix the root cause.
5. Verify the fix in a browser.
6. Update docs if behavior or assumptions changed.

## Adding or changing tests

No automated tests yet. Validation is manual:
- Open `index.html` directly in a browser, or run a one-liner static server
  (`python3 -m http.server` from the repo root) and open `http://localhost:8000`.
- Resize the window and use devtools device emulation to check 375px and 640px.
- Toggle "Disable JavaScript" in devtools to confirm the page still works.

## Updating the design

The reference image at the top of this project is the visual target. If the
user later supplies a new reference or revises the spec, update
`ai/project.md` and `ai/architecture.md` first, then refactor the page.

## Updating API contracts

N/A — no API.

## Preparing a pull request

When committing or preparing a PR:
- Title: short, imperative ("Add top nav", "Add hero section").
- Body: what visually changed, plus any docs/tickets touched.
- Screenshots welcome for visual changes.

## Updating project context

When behavior, structure, sections, or design tokens change, update the
relevant `ai/` file in the same change. Move completed tickets from
`ai/tickets/active/` to `ai/tickets/done/` only when the user asks.
