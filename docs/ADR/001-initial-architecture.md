# ADR-001: Initial Architecture — Static HTML/CSS/JS on GitHub Pages

**Date:** 2026-02-14
**Status:** Accepted
**Author:** migar

---

## Context

Intelastart is a B2B consulting and AI automation services site. It markets recurring consulting packages ($499–$custom/month) to founders and operators. The site's primary function is lead generation: presenting services, demonstrating expertise, and capturing inquiries.

Architecture options evaluated:

1. **Static HTML/CSS/JS + third-party form service on GitHub Pages** — zero hosting cost, fast, secure, simple
2. **Next.js on Vercel** — SSR capable, better for dynamic content (blog, personalization), but adds complexity
3. **Webflow** — designer-friendly no-code, but $23+/month and limited code customization
4. **HubSpot CMS Hub** — integrated CRM/marketing, but expensive and opinionated

## Decision

**Static HTML/CSS/JS on GitHub Pages with a third-party form service (Formspree or equivalent) for lead capture.**

All CRM integration (HubSpot, Notion, etc.) is handled via the form service webhooks — no backend code required.

## Rationale

### Why static HTML (not Webflow or HubSpot CMS)?

- **Cost:** GitHub Pages is free. Webflow and HubSpot cost $23–$300+/month for comparable functionality.
- **Control:** Full HTML/CSS control enables the premium, cinematic design that positions Intelastart as a high-end provider vs. generic SaaS landing pages.
- **Performance:** Static HTML achieves better Core Web Vitals than CMS-rendered pages at this content volume.

### Why GitHub Pages (not Vercel/Netlify)?

- GitHub is already the VCS of record — Pages adds zero additional tooling
- Free with custom domain and automatic HTTPS
- Adequate CDN performance for a marketing site with B2B traffic patterns

### Why a third-party form service (not a custom backend)?

- Lead capture (name, email, company, message) does not require a custom backend
- Formspree/Netlify Forms provide spam protection, email delivery, and CRM webhook support out of the box
- Avoids maintaining server infrastructure for what is a commodity function

### Lead Qualification Flow

Leads captured via form → Form service → Email notification + CRM webhook → Manual qualification and outreach. This is appropriate for a high-touch consulting business where each engagement is bespoke.

## Consequences

### Positive
- Zero infrastructure to maintain
- Single `git push` deploys
- Full brand control for premium positioning
- Form service handles spam protection and delivery reliability

### Negative / Trade-offs
- No dynamic personalization or gated content without a backend
- Blog content is manually managed HTML (no CMS)
- Adding a client portal, proposal generation, or contract signing requires third-party tools or a platform migration

## Future Considerations

If Intelastart scales to require automated onboarding, proposal generation, or a client portal, the migration path is to Next.js on Vercel with a lightweight backend (FastAPI or Next.js API routes) and a proper CRM integration. The current static site's HTML/CSS can be migrated incrementally to Next.js React components.
