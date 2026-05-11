# Domain Model

## Core entities

- **Cat** — singular. One specific calico named Mochi.
  - name: "Mochi"
  - tagline: "Professional napper. Expert loaf artisan. Bringer of calm,
    cuddles, and quiet judgment."
  - photo: `images/calico.jpg`

There is only one cat. The page is hard-coded for Mochi; there is no model,
list, or template generalization.

## Entity relationships

None.

## Lifecycle states

None.

## Business rules

- The headline copy is fixed: "A tiny corner of the internet for one perfect loaf."
- The subtitle copy is fixed: "This is Mochi. She sits. She loafs. She rules."
- The cat name "Mochi" appears verbatim below the photo with a sparkle.
- The footer copyright currently reads "© 2024 Calico. All rights reserved."

## Edge cases

- If the image fails to load, the alt text must still describe Mochi clearly
  enough for screen readers.
- If the page is printed, the dark text on cream background should remain legible.
