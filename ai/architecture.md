# Architecture

## System overview

Single static HTML page with one stylesheet, one local image, and inline SVG
for icons and botanical decorations. No build step, no JavaScript, no backend.
Deployed as static files (Netlify, Cloudflare Pages, GitHub Pages, etc.).

## Repository layout

```text
calico-cat/
├── index.html          # Markup for the whole page
├── styles.css          # All styles (tokens + layout + responsive)
├── images/
│   └── calico.jpg      # Single image asset (the cat)
└── ai/                 # Project context for AI agents
```

## Page sections (top to bottom)

There is **no top nav** and **no footer**. The page is a single centered hero.

`<main class="page">` contains only:

- `.photo-frame` — bordered, shadowed `<figure>` containing:
  - the `<img>` of Mochi,
  - a `::after` gradient scrim (dark at bottom, fading up) for headline legibility,
  - the `<h1>` headline absolutely positioned at the **bottom-left** of the
    image as an overlay, with a small trailing accent heart (`.h1-heart`).

**Decorative SVG botanicals** (`.botanical--left`, `.botanical--right`) are
absolutely-positioned to the left and right of the hero, behind the content,
hidden on mobile.

## Major modules

- `index.html` — semantic structure for the headline + heart + image, plus
  the two botanical SVGs.
- `styles.css` — design tokens, base reset, layout, headline, photo frame,
  botanicals, responsive.
- Inline SVGs for the two botanical branches only.

## Data flow

None. The page is fully static.

## Authentication and authorization

None.

## External services

- **Google Fonts** — loads `Cormorant Garamond` and (optionally) `Inter` for
  body copy via `<link>` tags. Page must render readably with the
  `Georgia, serif` and system-sans fallbacks.

## Background jobs

None.

## Error handling

- Missing image → broken-image fallback; alt text remains for screen readers.
- Missing font → falls back to `Georgia, serif` / system sans.

## Testing architecture

No automated tests. Validation is visual:
- Open `index.html` in a browser at desktop (≥1280px) and mobile (375px).
- Confirm all elements render: headline (with accent heart), framed image,
  and the two botanicals (desktop only).
- Confirm layout adapts at the `max-width: 640px` breakpoint.
- Confirm page works with JavaScript disabled.

## Deployment model

Upload the three files (`index.html`, `styles.css`, `images/calico.jpg`) to
any static host. Subdomain DNS points to the host. No build pipeline required.
