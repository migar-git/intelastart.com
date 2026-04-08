# Runbook — intelastart.com

## Service Overview

- **Site:** https://intelastart.com
- **Type:** Static HTML/CSS/JS B2B consulting marketing site
- **Hosting:** GitHub Pages (branch: main)
- **Custom Domain:** intelastart.com

---

## Routine Operations

### Deploy a Change

```bash
git add <files>
git commit -m "type: description"
git push origin main
```

GitHub Pages publishes within ~60 seconds.

### Verify the Site is Live

```bash
curl -I https://intelastart.com
# Expect: HTTP/2 200
```

---

## Incident Procedures

### Site Not Loading

1. Check https://www.githubstatus.com
2. If GitHub Pages operational: check Settings → Pages, confirm source is `main` / root
3. Check last commit did not break HTML structure

### Domain Not Resolving

1. Verify DNS:
   ```bash
   dig intelastart.com A +short
   # Expected: 185.199.108–111.153
   ```
2. Verify A records at registrar
3. Allow up to 48 hours for propagation
4. Verify CNAME file contains `intelastart.com`

### HTTPS Certificate Issue

1. Repository Settings → Pages → verify "Enforce HTTPS" enabled
2. Toggle off/on to re-trigger certificate provisioning if stuck

### Contact Form Not Receiving Submissions

1. Test form submission manually
2. Check spam/junk folder at the receiving email address
3. Log into the form service (Formspree, etc.) dashboard to check submission log
4. Verify form action URL in HTML is correct and has not changed
5. If form service has a status page, check for outages

### CTA / Booking Link Not Working

1. Check the booking URL (Calendly, etc.) is active
2. Update the link in all relevant HTML files
3. Commit and push the fix

### Rollback a Bad Deployment

```bash
git revert HEAD
git push origin main
# Or for a specific commit:
git revert <bad-commit-sha>
git push origin main
```

---

## Cache Invalidation

Allow 60–120 seconds after push. Test with incognito window or hard-refresh (Ctrl+Shift+R).

---

## Content Operations

### Update Pricing

1. Search for old price across all HTML files:
   ```bash
   grep -r "\$499" .
   ```
2. Update all instances consistently (homepage, pricing.html, service pages)
3. Commit and push

### Add a Blog Article

1. Create article in `blog/` directory
2. Add article card to `blog.html`
3. Add URL to `sitemap.xml`
4. Push to main

### Add a New Service Page

1. Create `services/<service-name>.html`
2. Link from homepage services section and navigation
3. Add to `sitemap.xml`
4. Push to main

---

## Monitoring

- Recommended: UptimeRobot free monitor on https://intelastart.com
- Check Google Search Console monthly for crawl errors
- Test contact form monthly to confirm lead delivery

---

## Contacts

| Role | Contact |
|---|---|
| Site Owner | migar (GitHub) |
| Domain Registrar | Check registrar account for intelastart.com |
| Form Service | Check Formspree or configured form provider dashboard |
