# Security — intelastart.com

## Overview

Intelastart is a B2B consulting marketing site. It is a static HTML site with contact/inquiry forms handled via third-party form services. The following security practices apply.

## Content Security Policy (CSP)

Apply CSP via `<meta http-equiv="Content-Security-Policy">` in all HTML pages.

```html
<meta http-equiv="Content-Security-Policy"
  content="default-src 'self';
           script-src 'self' 'unsafe-inline' https://www.googletagmanager.com;
           style-src 'self' 'unsafe-inline' https://fonts.googleapis.com;
           font-src 'self' https://fonts.gstatic.com;
           img-src 'self' data: https:;
           connect-src 'self' https://www.google-analytics.com https://formspree.io;
           frame-src 'none';
           object-src 'none';">
```

Replace `https://formspree.io` with the actual form endpoint domain in use. Tighten `'unsafe-inline'` by externalizing scripts.

## HTTPS Enforcement

GitHub Pages automatically enforces HTTPS. Verify "Enforce HTTPS" is enabled in repository Settings → Pages. All business inquiries and contact forms must operate over HTTPS.

## Contact Form Security

- Use a reputable third-party form service (Formspree, Netlify Forms, etc.) — never build server-side form handling in a static repo
- The form endpoint token/ID is public (it's in the HTML) — this is expected; protect against spam with reCAPTCHA or honeypot fields
- Never embed CRM API secret keys or authentication tokens client-side

## Secrets Management

Never commit to this repository:
- CRM API keys (HubSpot, Salesforce, etc.)
- Email platform API keys
- Analytics write tokens
- Any `.env` file

Required `.gitignore` entries:
```
.env
.env.*
*.key
secrets/
node_modules/
```

## Client-Facing Data

- Do not promise data security postures in marketing copy that cannot be technically substantiated
- Privacy policy (`privacy.html`) must accurately describe what data is collected via forms and analytics
- Terms (`terms.html`) must reflect the actual consulting engagement terms

## HTTPS and Domain Security

- CNAME file must be present for GitHub Pages to provision the custom domain TLS certificate
- Verify certificate renewal (GitHub Pages renews automatically via Let's Encrypt)
- Enable HSTS by enforcing HTTPS at the DNS/CDN level if using Cloudflare in front of GitHub Pages

## Vulnerability Reporting

Report security issues privately to the repository owner. Do not post vulnerability details in public issues.
