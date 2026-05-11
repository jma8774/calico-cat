# ADR-0002: Reference image takes precedence over the original spec

## Status

Accepted

## Context

The user supplied a written spec
(`/Users/jimmy/Downloads/calico_loaf_static_site_spec.md`) describing a
minimal page (headline + heart + image only, no nav/footer/buttons), and
later supplied a reference screenshot showing a fuller landing page with:

- A top navigation bar (paw + "Calico" wordmark + HOME/ABOUT/GALLERY/LOVE NOTES).
- A "♥ CALICO CAT" pill above the headline.
- A revised headline: "...for one perfect loaf." (vs spec's "...for this loaf of bread.")
- A subtitle: "This is Mochi. She sits. She loafs. She rules."
- Cat name "Mochi ✨", description, and two CTA buttons below the photo.
- Footer line with copyright.
- Botanical line-art decorations.

These two sources directly conflict on layout, copy, and what elements exist.

## Decision

The user iteratively stripped the reference image down to a minimal hero. The
final page keeps only:

- The serif headline with a small accent heart.
- The framed calico photo.
- The two atmospheric botanical SVGs (desktop only).

Everything else from the reference image was explicitly removed by the user:

- **No top navigation bar** — no paw, no wordmark, no nav links.
- **No footer** — no love line, no sparkles, no copyright.
- **No "CALICO CAT" pill** above the headline.
- **No "This is Mochi…" subtitle** below the headline.
- **No "Mochi" cat name, description, or CTA buttons** below the photo.

The headline copy is taken from the reference image
("...for one perfect loaf."), not the spec ("...for this loaf of bread.").

The written spec remains the source of truth for things neither the image
nor the user dictated explicitly: color tokens (`--bg`, `--text`, etc.),
typography (Cormorant Garamond), spacing primitives, accessibility.

## Consequences

- The page is the minimal hero plus botanicals — closer to the spec's
  intent than the reference image's layout.
- Future additions of nav, footer, pill, subtitle, name, description, or
  buttons should be treated as a new design decision and recorded here.
- The page remains static, mobile responsive, and JS-free.

## Alternatives considered

- Build the minimal spec-only version — rejected because the user
  explicitly chose "follow the reference image" when asked.
- Build a hybrid — rejected for the same reason; would produce a page
  that matches neither source.
