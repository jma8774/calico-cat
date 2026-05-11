# TICKET-003: Build cat info (name, description, two CTAs)

## Status

Active

## Goal

Below the framed photo, render Mochi's name, a short description, and two
call-to-action buttons that match the reference image.

## Requirements

- `.cat-name` element:
  - Text: `Mochi` followed by a small sparkle icon (inline SVG).
  - Cormorant Garamond, `color: var(--accent)`, ~`1.75rem`, centered.
- `.cat-desc` element:
  - Two-line copy: "Professional napper. Expert loaf artisan." /
    "Bringer of calm, cuddles, and quiet judgment."
  - Sans, `color: var(--text-muted)`, centered, narrow max-width.
- `.cta` wrapper with two anchor buttons (`<a class="btn ...">`), both
  `href="#"`:
  - **Primary**: filled accent button. Label "View Full Photo" with an
    external-link SVG icon on the left.
  - **Secondary**: outlined button. Label "About This Cat" with a small
    cat-face SVG icon on the left.
- Buttons share a `.btn` base class for padding, radius, font weight, and
  focus ring. Primary variant uses `background: var(--accent)`; secondary
  uses transparent background with `1px solid var(--border)`.

## Acceptance criteria

- The order under the image is: name → description → buttons.
- Buttons sit side by side on desktop with comfortable gap.
- Focus styles are visible when tabbing through the buttons.
- All icons render inline (no font-icon dependency).

## Files likely involved

- `index.html`
- `styles.css`

## Out of scope

- Real destination pages — buttons stay as `href="#"`.
- Mobile stacking (TICKET-005).
