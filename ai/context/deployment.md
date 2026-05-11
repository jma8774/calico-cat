# Deployment

## Environments

- **Local** — open `index.html` directly or serve via
  `python3 -m http.server 8000` from the repo root.
- **Production** — any static host (Netlify, Cloudflare Pages, GitHub Pages,
  S3+CloudFront). Subdomain DNS points at the host.

## Build process

None. Files are served as-is.

## Release process

Upload `index.html`, `styles.css`, and the `images/` directory to the host
(or push to the host's connected git branch).

## CI/CD

None configured yet.

## Rollback process

Revert to a previous commit and redeploy. Because the site is three files,
rollback is trivial.

## Environment variables

None.

## Monitoring

None.
