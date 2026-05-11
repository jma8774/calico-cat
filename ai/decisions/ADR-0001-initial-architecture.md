# ADR-0001: Plain static HTML/CSS, single file, no build step

## Status

Accepted

## Context

The site is a single landing page for one cat. The original spec recommended
plain `index.html` + `styles.css` over Vite/Vue because the page is simple.
The reference image expands the page (nav, footer, CTAs, decorations) but
the content is still static and one-of-a-kind.

## Decision

Build the site as plain static files:
- `index.html` at the root containing the full markup.
- `styles.css` at the root containing all styles.
- `images/calico.jpg` for the single image asset.

No build tooling. No JavaScript dependency. No frameworks.

## Consequences

- Trivial to host on any static provider.
- Zero build step — change a file, refresh the browser.
- No type safety or component reuse, but the page has no reusable parts.
- If the site grows to multiple cats or pages, this decision should be
  revisited (likely with Vite + a tiny templating layer).

## Alternatives considered

- **Vite + Vue** — overkill for one page of static content.
- **Astro / Eleventy** — useful if multi-page, but not needed here.
- **Tailwind** — would add a build step and dependency for a small set of
  custom styles; design tokens in CSS variables are sufficient.
