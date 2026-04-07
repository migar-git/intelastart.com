# Contributing to intelastart.com

## Local Development

```bash
python -m http.server 8080
# or
npx serve .
```

## Site Structure

- `index.html` — main landing page
- `services/` — individual service offering pages
- `blog/` — content marketing articles
- `css/` — stylesheets
- `js/` — client-side scripts
- `pricing.html` — pricing tiers

## Updating Pricing

Edit `pricing.html` directly. Ensure any price references in `index.html` or service pages match.

## Adding a Service Page

1. Create `services/service-name.html` (copy existing service page as template).
2. Link from `index.html` services section and `pricing.html`.
3. Add to `sitemap.xml`.

## Deploying

Push to `master`. GitHub Pages auto-deploys via CNAME record for intelastart.com. See `docs/DEPLOYMENT.md`.

## Standards

- Keep claims (revenue figures, automation counts) accurate and verifiable.
- All external links: `rel="noopener noreferrer"`.
- Do not commit API keys, CRM tokens, or webhook secrets.
