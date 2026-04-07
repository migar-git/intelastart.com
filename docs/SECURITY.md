# Security — intelastart.com

## Content Security Policy

Add CSP via `<meta http-equiv="Content-Security-Policy">` in all HTML files.

Recommended:
- `default-src 'self'`
- `script-src 'self' 'unsafe-inline'`
- `style-src 'self' 'unsafe-inline'`
- `img-src 'self' data: https:`
- `object-src 'none'`
- `frame-src 'none'`

## Contact Form / Lead Capture

If contact forms or lead capture are added:
- Use a third-party form service (Formspree, Netlify Forms) — do not process form data in this static repo.
- Do not store form submissions in the repo.
- Embed only the form endpoint URL, not any service secret keys.

## Secrets

Do not commit:
- CRM API keys (HubSpot, Salesforce, etc.)
- Email marketing API keys
- Calendly or booking widget tokens
- Any webhook signing secrets

## Legal Pages

- `privacy.html` — update when adding new data processors (CRM, analytics, chat widgets).
- `terms.html` — should reflect the consulting services offered.

## Reporting Issues

Contact the repo owner privately for any security concerns.
