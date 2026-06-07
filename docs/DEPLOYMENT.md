# Deployment — intelastart.com

## Platform

Hosted on **GitHub Pages** with custom domain **intelastart.com**.

## DNS Configuration

| Record Type | Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | migar-git.github.io |

Verify DNS:
```bash
dig intelastart.com A +short
```

## Deploy Process

```bash
git add <changed-files>
git commit -m "feat/fix/content: describe your change"
git push origin main
```

GitHub Pages rebuilds automatically within ~60 seconds.

## Verifying Deployment

1. Open https://intelastart.com in a private browser window
2. Hard-refresh (Ctrl+Shift+R) to bypass cache
3. Confirm changed content appears
4. Verify contact/inquiry forms submit correctly (test with a real submission)

## Rollback

```bash
# Revert last commit
git revert HEAD
git push origin main

# Revert specific commit
git revert <commit-sha>
git push origin main
```

## Environment Variables

None required for the static site.

- Contact form endpoint tokens (Formspree IDs, etc.) are public — safe in HTML
- CRM API keys must never appear in this repository

## Pre-Deploy Checklist

- [ ] All pages render at 375px, 768px, 1280px
- [ ] Pricing page matches pricing referenced in other pages
- [ ] Contact/inquiry form works (test submission)
- [ ] Blog articles load correctly
- [ ] Service pages link correctly from homepage and navigation
- [ ] sitemap.xml updated for any new pages
- [ ] Lighthouse Performance ≥ 90, Accessibility ≥ 90
- [ ] No console errors in browser DevTools

## Post-Deploy Checklist

- [ ] intelastart.com resolves over HTTPS
- [ ] Contact form sends correctly (verify email received)
- [ ] All service and pricing pages accessible
- [ ] Analytics recording sessions (if configured)
