# TICKET-004: Add botanical SVG decorations on left and right

## Status

Active

## Goal

Add subtle accent-colored botanical line illustrations flanking the photo
to match the reference image's atmospheric feel.

## Requirements

- Two inline SVG `<svg class="botanical botanical--left">` and
  `.botanical--right` elements absolutely positioned inside `.page`.
- Stroke color: `var(--accent-soft)` or `var(--accent)` at low opacity
  (~0.35) so they read as background atmosphere, not content.
- Position roughly at left ~6% and right ~6% horizontally, vertically
  aligned with the photo.
- `pointer-events: none` and `aria-hidden="true"`.
- Hidden via `display: none` at the mobile breakpoint.

## Acceptance criteria

- Decorations are visible but subtle on desktop.
- They do not overlap the photo or the headline at any viewport ≥1024px.
- They are completely hidden below 640px.

## Files likely involved

- `index.html` (inline SVG)
- `styles.css`

## Out of scope

- Animation.
- Replacing with raster images.

## Notes for implementation

A short hand-drawn-style branch with a few leaves is sufficient. Keep the
SVG small (≤30 path commands) — this is decoration, not art.
