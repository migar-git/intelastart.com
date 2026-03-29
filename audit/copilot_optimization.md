# Copilot Optimization — intelastart.com

**Audit Date:** 2026-03-29

## Current Copilot Usefulness Rating: 4 / 10

Separated CSS/JS structure gives Copilot more surface area than aresmaxs.com. Consulting site structure (services, blog, pricing) is a familiar pattern Copilot can extend well.

## Opportunities for AI Assistance

| Task | Opportunity |
|------|-------------|
| Case study page generation | Agent generates case study HTML from a data template |
| Blog article generation | Agent generates articles from arescore research on AI consulting topics |
| Calendly embed integration | Copilot can insert Calendly widget into pricing.html |
| Schema.org Service markup | Copilot can add Service schema to each services/ page |
| Contact form | Copilot can generate a Formspree-powered contact form |
| Testimonial section | Agent generates testimonial cards from a data JSON |

## What Needs to Be Built for Copilot to Help More

1. **Case study template** — Copilot can fill it in from a structured data file.
2. **`data/case-studies.json`** — anonymized project data; Copilot renders to HTML.
3. **Formspree or similar** integration for the contact form — Copilot can write the form HTML.
4. **`.github/copilot-instructions.md`** — describe Intelastart as an AI consulting brand; tone is professional/enterprise, not startup/hype.
5. **Blog template** — consistent article template enabling agent-driven content expansion.
