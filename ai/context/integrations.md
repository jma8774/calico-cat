# Integrations

## External services

- **Google Fonts** — loads the serif `Cormorant Garamond` (and optionally a
  sans like `Inter`) via `<link>` tags in `index.html`. This is the only
  external request the page makes.

## Credentials and environment variables

None.

## Webhooks

None.

## Failure handling

If Google Fonts is blocked or slow, the page falls back to:

- Headline / wordmark / cat name → `Georgia, serif`.
- Body / nav → system sans stack.

The page must remain readable in this fallback state.

## Retry behavior

N/A.

## Local development notes

Just open `index.html` in a browser, or serve the folder with any static
server (e.g. `python3 -m http.server`).
