# TICKET-001: Bootstrap repo with index.html, styles.css, image

## Status

Active

## Goal

Create the skeleton files that every other ticket builds on:
`index.html`, `styles.css`, and a placeholder `images/calico.jpg`.

## Background

The repo is empty except for `.git` and `ai/`. Before any visual work, we
need the three files in place with design tokens defined and the warm cream
background working so subsequent tickets only need to add sections.

## Requirements

- Create `index.html` with:
  - `<!doctype html>`, `lang="en"`, viewport meta, charset.
  - `<title>` and `<meta name="description">` matching the spec.
  - Google Fonts preconnect + Cormorant Garamond stylesheet link.
  - Link to `./styles.css`.
  - Empty `<main class="page">` ready for hero content.
- Create `styles.css` with:
  - `:root` design tokens from the spec.
  - `* { box-sizing: border-box; }` reset.
  - `body` background using the spec's radial gradients + `--bg`.
  - `body::before` subtle grain overlay.
  - `.page` centered grid container.
- Create `images/` directory and place a placeholder `calico.jpg` if no
  real photo exists.

## Acceptance criteria

- Opening `index.html` in a browser shows a warm cream page with the
  subtle grain texture and no content yet.
- No console errors.
- Page passes basic HTML validation (no missing closing tags).

## Files likely involved

- `index.html` (new)
- `styles.css` (new)
- `images/calico.jpg` (new, placeholder OK)

## Out of scope

- Any content inside `.page` — that's TICKET-002 onward.

## Notes for implementation

If no real cat image is available, write a tiny SVG saved as `.jpg`-isn't-
valid, so instead drop a placeholder note: leave the path referenced but
known-missing, or generate a tiny solid-color JPG. The user will replace
the asset later.
