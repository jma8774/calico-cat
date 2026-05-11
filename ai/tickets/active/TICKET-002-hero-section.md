# TICKET-002: Build hero (pill, headline, subtitle, framed image)

## Status

Active

## Goal

Render the centered hero: outlined `♥ CALICO CAT` pill, serif headline with
trailing accent heart, muted subtitle, and the framed calico photo.

## Background

This is the top-of-page content. With no nav above it, the pill becomes the
first visible element, so it needs comfortable top padding.

## Requirements

- Add `.pill` element near the top of `.page`:
  - Rounded full pill with `1px solid var(--border)` and `var(--bg-soft)`.
  - Small inline SVG heart in `var(--accent)` + uppercase tracked label
    "CALICO CAT".
- Add `<h1>` with the copy:
  ```
  A tiny corner of the internet
  for one perfect loaf. ♥
  ```
  - `<br />` between the two lines.
  - Trailing accent-colored heart inline at the end of the second line.
  - Spec headline styling: `font-size: clamp(2.4rem, 7vw, 5rem)`,
    `line-height: 0.95`, `font-weight: 600`, `letter-spacing: -0.035em`,
    centered.
- Add `.subtitle` with copy "This is Mochi. She sits. She loafs. She rules."
  - Sans, `color: var(--text-muted)`, smaller size, centered.
- Add `.photo-frame` `<figure>` wrapping `<img src="./images/calico.jpg"
  alt="A calico cat sitting like a loaf of bread" />` using the spec's
  photo-frame styling.

## Acceptance criteria

- Hero renders centered horizontally and vertically on desktop.
- Pill, headline, subtitle, and photo stack with comfortable spacing.
- Headline uses Cormorant Garamond (or Georgia fallback).
- Image is capped at ~820px wide and rounded with a soft shadow.

## Files likely involved

- `index.html`
- `styles.css`

## Out of scope

- Cat name, description, buttons (TICKET-003).
- Botanical decorations (TICKET-004).
- Mobile pass (TICKET-005).
