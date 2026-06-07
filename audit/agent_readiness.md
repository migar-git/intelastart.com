# Agent Readiness — intelastart.com

**Audit Date:** 2026-03-29

## Current Agent Readiness: Low (25 / 100)

Standard static site agent readiness. Separated structure makes agent edits safer than aresmaxs.com, but no automation pipeline exists.

## What's Working

- AGENT.md schema v1.0 present.
- `/services/` and `/blog/` directories provide clean namespaces for agent-generated content.
- sitemap.xml and robots.txt present — agents can maintain these.

## What Needs to Be Built for Agent Automation

| Component | Priority | Description |
|-----------|----------|-------------|
| Blog template | High | Agent generates consulting articles from arescore research |
| Case study template + data JSON | High | Agent populates case studies from project records |
| `generate_sitemap.py` | High | Agent maintains sitemap.xml |
| GitHub Actions workflow | High | CI validates HTML and deploys on agent push |
| Analytics reader | Medium | Agent measures consulting page engagement for arescore KPIs |
| Booking system integration | Medium | Agent could monitor booking calendar and trigger follow-up sequences |

## For Static Site Agents — Recommended Next Steps

1. Intelastart's agent use case differs from coves7 — content here supports lead generation, not affiliate clicks. The pipeline is: arescore research → intelastart blog → consulting inquiries → revenue.
2. Agent should monitor competitor consulting sites for topic gaps and generate articles to fill them.
3. A Calendly integration + analytics would give the agent a feedback loop: content → booking → revenue.
4. Priority is lower than coves7.com for the swarm since coves7 has the clearer affiliate revenue path.
