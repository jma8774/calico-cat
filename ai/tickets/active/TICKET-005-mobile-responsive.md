# TICKET-005: Mobile responsive pass

## Status

Active

## Goal

At narrow viewports (≤640px), the page should still feel spacious and
elegant. No horizontal scroll, no cramped buttons, no overflowing image.

## Requirements

- `.page` mobile padding `3rem 1rem` and `align-items: start`.
- Headline scales down to ~`clamp(2.25rem, 12vw, 3.5rem)`.
- `.photo-frame` becomes `width: 100%`, smaller border-radius and padding
  per the spec.
- `.cta` stacks vertically, each button full-width with consistent gap.
- `.botanical--left` / `.botanical--right` hidden.
- Subtitle and description wrap naturally; nothing overflows the viewport.

## Acceptance criteria

- At 375px width: no horizontal scroll.
- At 375px width: headline, subtitle, image, name, description, and both
  buttons all visible by scrolling — none cut off horizontally.
- At 640px width and above: layout returns to the desktop arrangement.

## Files likely involved

- `styles.css`

## Out of scope

- Tablet-specific tweaks (between 640 and 1024px) unless something looks
  obviously broken.
