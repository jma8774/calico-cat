# Project Overview

## What this project does

Calico Loaf is a single-page static landing site for one calico cat named
**Mochi**. It is a warm, elegant, cozy "shrine" page hosted as a static site
on a subdomain. No backend.

The implementation follows a user-supplied reference screenshot, which expands
the original spec into a richer landing page (nav, footer, CTAs, decorations).

## Primary users

- The site owner — wants a personal corner of the internet for their cat.
- Visitors who follow a link to the site.

## Core user flows

1. Visitor loads the page.
2. Visitor sees: a centered serif headline with a small accent heart, and
   the framed calico photo below it. Subtle botanical line-art flanks the
   photo on desktop.
3. There is nothing else on the page — no nav, no pill, no subtitle, no
   cat name, no description, no buttons, no footer.
4. On mobile, the layout reflows: image scales to width and botanicals
   are hidden.

## Non-goals

- **No top navigation bar.**
- **No footer.**
- **No pill / chip above the headline.**
- **No subtitle below the headline.**
- **No cat name, description, or CTA buttons below the photo.**
- No multi-page site.
- No backend, API, or database.
- No JavaScript-driven behavior (page must work without JS).
- No external image hosting — the calico image is bundled locally.
- No gallery, no carousel, no lightbox.

## Important constraints

- Must be static (HTML/CSS, no build step).
- Mobile responsive — layout must not break at 375px width.
- Page must work with JavaScript disabled.
- Image alt text is required.
- No flashing animation; hover motion only on hover-capable devices.
- Color palette from the spec is the source of truth for design tokens.

## Current project status

Initial implementation. Repo bootstrap and design pass underway.
Original spec: `/Users/jimmy/Downloads/calico_loaf_static_site_spec.md`.
Reference design: user-supplied screenshot showing the full landing-page layout.
The reference image takes precedence over the minimal spec where they conflict
(decision recorded in ADR-0001).
