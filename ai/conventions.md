# Coding Conventions

## File organization

- One HTML file (`index.html`) at repo root.
- One CSS file (`styles.css`) at repo root.
- All images under `images/`.
- All AI context under `ai/`.

## Naming conventions

- Class names: lowercase kebab-case (`.photo-frame`, `.topnav`, `.cat-name`).
- CSS custom properties: `--kebab-case` (`--bg-soft`, `--text-muted`).
- File names: lowercase, hyphenated.

## HTML conventions

- Use semantic elements: `<header>`, `<main>`, `<section>`, `<figure>`,
  `<footer>`, `<h1>`, `<nav>`.
- Decorative icons and shapes use `aria-hidden="true"`.
- Image must have a meaningful `alt` attribute.
- Buttons that are real actions use `<button>`; navigation that goes
  somewhere uses `<a href="...">`. Today everything is `<a href="#">`
  because there are no destination pages yet.

## CSS conventions

- Define design tokens once at `:root` as CSS variables — do not hardcode
  colors or shadows elsewhere.
- Use `clamp()` for fluid type and spacing.
- Mobile breakpoint: `@media (max-width: 640px)`.
- Hover effects only inside `@media (hover: hover)`.
- Use `box-sizing: border-box` globally.
- Order rules in `styles.css` as: tokens → reset → layout primitives
  (`.page`, `.topnav`, `.sitefoot`) → components → decorations → responsive.

## Color and typography

Design tokens (from the spec):

```css
--bg: #fbf4e8;
--bg-soft: #fffaf2;
--text: #3c2a1f;
--text-muted: #8a6f5a;
--accent: #b77745;
--accent-soft: #e6c5a8;
--border: rgba(92, 60, 36, 0.16);
--shadow: rgba(68, 42, 24, 0.18);
```

- Headline / wordmark / cat name font: `"Cormorant Garamond", Georgia, serif`.
- Body / nav / button / subtitle font: a clean sans (system stack OK).
- No other typefaces without an ADR.

## Accessibility

- Image must have descriptive alt text.
- Text contrast must meet WCAG AA on the cream background.
- No flashing animation.
- Layout must not break when text scales.
- Page must work without JavaScript.
- Interactive elements need a visible focus ring.

## Dependency rules

- No JS frameworks.
- No CSS frameworks (Tailwind, Bootstrap, etc.).
- Only external resource allowed: Google Fonts.
- Icons are inline SVG; no icon-font dependencies.
- Adding anything else requires an ADR.

## What not to do

- **Do not add a footer or bottom bar.**
- Keep the topbar minimal — one link to the sibling FileDrop app. Do not
  add a wordmark, logo, or additional nav items without an ADR.
- Do not introduce build tooling (Vite, webpack, etc.) — keep it static.
- Do not load remote images.
- Do not add new pages.
- Do not use bright or neon colors.
- Do not add heavy shadows or dramatic motion.
- Do not require JavaScript for the page to function.
