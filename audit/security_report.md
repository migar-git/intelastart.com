# Security Report — intelastart.com

**Audit Date:** 2026-03-29

## Security Concerns

| Issue | Severity | Detail |
|-------|----------|--------|
| `hello@intelastart.com` in JSON-LD | Low | Public email address is exposed to scrapers; use a contact form instead |
| No contact form | Low | Absence of a form means no server-side validation or spam protection |
| Legal claims ("$2M+ revenue") | Medium | Unsubstantiated business claims carry legal risk; consult legal counsel |
| No CSP | Medium | External font/script loads without Content Security Policy |
| `js/` directory not audited | Medium | Could contain hardcoded API keys in form handlers |
| Pricing page without payment | Low | No PCI risk currently; add payment carefully when implementing |

### Secrets Audit

No secrets found in scanned HTML files. `js/` not fully inspected — audit manually.

## Security Baseline

1. **Audit `js/` directory** for hardcoded API keys.
2. **Review business claims** ("500+ automations, $2M+ revenue") with legal counsel if the site actively solicits consulting clients — FTC substantiation requirements apply.
3. **Add CSP meta tag** once JS is inventoried.
4. **If adding a contact form**, use Formspree or similar — never expose API keys client-side.
5. **If adding payment**, use Stripe Checkout or similar hosted solution — never process payment data in static HTML.
6. **Confirm HTTPS enforcement** in GitHub Pages.
