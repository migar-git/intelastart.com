# Test Strategy — intelastart.com

## Overview

Intelastart is a static B2B consulting marketing site. Testing focuses on performance, accessibility, content accuracy, lead capture form functionality, and SEO.

## Test Categories

### 1. Lighthouse Audits (Primary Quality Gate)

**Targets:**

| Category | Minimum Score |
|---|---|
| Performance | ≥ 90 |
| Accessibility | ≥ 90 |
| Best Practices | ≥ 90 |
| SEO | ≥ 95 |

```bash
npx lighthouse https://intelastart.com --output html --output-path ./lighthouse-report.html
```

Run on both desktop and mobile presets.

### 2. Accessibility Testing

- Run axe DevTools on homepage, pricing, and contact pages
- All images must have meaningful `alt` attributes
- Forms must have proper `<label>` associations
- Keyboard navigation through all CTAs and form fields
- Color contrast ≥ 4.5:1 for body text

### 3. Contact Form Testing

Before every push that touches forms:
- Submit a test inquiry and verify it arrives at the configured email/CRM
- Verify form validation (required fields, email format)
- Check spam protection (honeypot or reCAPTCHA) is functioning
- Confirm success/error states display correctly

### 4. Link Checking

```bash
npx linkinator https://intelastart.com --recurse --skip "^(?!https://intelastart.com)"
```

Verify:
- All service pages accessible from homepage and navigation
- Pricing page accessible and loads correctly
- Blog articles load from blog listing
- CTA buttons ("Book a Call", "Get Started") link to correct destinations

### 5. Content Accuracy Review

Before publishing pricing or service changes:
- Pricing must be consistent across homepage, pricing.html, and all service pages
- Service deliverables must match what is described in the PRD
- No placeholder content ("Lorem ipsum", "TBD") visible in production

### 6. Cross-Browser Testing

Chrome, Firefox, Safari, Edge — latest versions.

Focus areas: form rendering, button hover states, pricing table layout.

### 7. Mobile/Responsive Testing

| Breakpoint | Device |
|---|---|
| 375px | Small phones |
| 768px | Tablet |
| 1280px | Desktop |
| 1920px | Large desktop |

Priority: pricing table and CTA buttons must be fully functional on mobile.

### 8. SEO Checks

- `<title>` unique per page, includes primary keyword + brand
- `<meta name="description">` compelling and under 160 characters
- Schema.org Organization markup on homepage
- sitemap.xml lists all pages
- robots.txt does not block indexable content

### 9. Visual Regression (Major Redesigns)

```bash
npx playwright screenshot https://intelastart.com --full-page --output before.png
# Make changes
npx playwright screenshot https://intelastart.com --full-page --output after.png
```

## Test Schedule

| Trigger | Tests |
|---|---|
| Before every push | Smoke test in browser, form submission |
| Pricing/content change | Content accuracy review, mobile layout |
| Major redesign | Full Lighthouse, cross-browser, visual regression |
| Monthly | Full Lighthouse audit, link check, form test |
