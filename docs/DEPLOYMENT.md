# Deployment — intelastart.com

## Platform

Hosted on **GitHub Pages** (`master` branch → root). Custom domain via `CNAME` file.

## Deploy Process

```bash
git add .
git commit -m "your message"
git push origin master
```

GitHub Pages rebuilds within ~30 seconds. No CI pipeline required.

## Custom Domain

- CNAME file contains `intelastart.com`
- DNS A records: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
- HTTPS enforced by GitHub Pages TLS

## Rollback

```bash
git revert HEAD
git push origin master
```

## Pre-deploy Checklist

- [ ] HTML validates
- [ ] Pricing is consistent across all pages
- [ ] sitemap.xml updated for new/removed pages
- [ ] No hardcoded staging or localhost URLs
- [ ] No credentials or API keys in committed files
