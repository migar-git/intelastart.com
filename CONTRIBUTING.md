# Contributing to intelastart.com

Thank you for contributing to Intelastart, the B2B AI consulting site.

## Local Development

No build step required. Open `index.html` in a browser or serve locally:

```bash
# Python
python -m http.server 8080
# Node.js
npx serve .
```

Open http://localhost:8080 in your browser.

## Repository Structure

```
/
├── index.html          # Homepage
├── css/                # Stylesheets
├── js/                 # JavaScript files
├── blog/               # Blog articles
├── services/           # Service detail pages
├── pricing.html        # Pricing tiers
├── about.html          # About page
├── *.html              # Other pages
├── CNAME               # Custom domain: intelastart.com
├── robots.txt / sitemap.xml
├── .gitignore
└── docs/               # Project documentation
```

## Branch Naming

| Purpose | Pattern | Example |
|---|---|---|
| New service page | `feat/<service-name>` | `feat/market-intel-service` |
| Bug fix | `fix/<description>` | `fix/pricing-table` |
| Content update | `content/<description>` | `content/case-study-update` |
| Documentation | `docs/<description>` | `docs/runbook-update` |

## Pull Request Process

1. Branch from `main`
2. Make focused, atomic changes
3. Test at 375px, 768px, 1280px viewports
4. Verify Lighthouse Performance ≥ 90, Accessibility ≥ 90
5. Confirm pricing is accurate and consistent across all pages
6. Open PR with description; request review before merging

## Content Standards

- Service descriptions must accurately reflect what is delivered
- Pricing tiers must be consistent (index, pricing page, and any service pages)
- Testimonials and case studies must be real or clearly marked as illustrative
- Blog content should be substantive and demonstrate genuine expertise

## Security

- Never commit API keys, CRM tokens, or `.env` files
- Contact form submissions must use a server-side proxy or third-party form service — never expose backend credentials client-side
- See `docs/SECURITY.md` for full policy

## Deployment

Push to `main` triggers automatic GitHub Pages deployment. See `docs/DEPLOYMENT.md` for full procedures.
