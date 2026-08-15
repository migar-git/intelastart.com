# intelastart.com Feature Requests

<!-- REGROUND:reground-20260815-python-fleet:BEGIN -->

## Re-Grounding 2026-08-15 — Autonomous Fleet Pass

> **Run:** `reground-20260815-python-fleet` · **Method:** static forensic recon of all 59 git repos under `C:\Users\mcgac\Python`
> (tree + manifests + compose + git metadata + targeted greps via Windows-MCP; **no code executed this pass**).
> **Execution contract:** [`FRSP.md`](FRSP.md) — the resident self-agent system prompt generated alongside this block.

### Verified identity (2026-08-15)

Static B2B marketing/consulting site (GitHub Pages, CNAME): multi-page (about/blog+3 articles/pricing/privacy), 3 doc-lint-family workflows.

### Evidence snapshot

| Field | Value |
|---|---|
| Class | Static/managed website |
| Branch @ recon | `master` |
| Last commit observed | 2026-07-27 |
| Stack | Static HTML/CSS/vanilla JS |
| Ports/services declared | none declared |
| Test posture | 3 workflows exist (not product tests) |
| LLM posture | CI-level |
| MCP posture | n/a |
| Dashboard posture | arescore registration |

### Prior-content status

The body below this block is the prior audit register (last authored ~2026-07-03/04, 454 lines). It is preserved verbatim per the fleet data-retention law. Every claim in it is now classified **STALE-UNVERIFIED** until re-proven by the FRSP execution loop — the repo has moved (last commit 2026-07-27).

### Universal mandate assessment (fleet standard M-01..M-10)

| ID | Mandate | Status | Evidence / note |
|---|---|---|---|
| M-01 | Repo self-agent | PARTIAL | AGENT.md/CLAUDE.md governance present fleet-wide; FRSP.md (this pass) is now the executable self-agent contract |
| M-02 | Local-LLM capability (via canonical provider) | N-A/CI-LEVEL | LLM used in CI/build lanes only — correct for this repo class; runtime consumption not required |
| M-03 | Local-LLM management reachable | N-A | Managed centrally by olaman; this repo consumes nothing at runtime |
| M-04 | MCP surface | N-A | n/a |
| M-05 | 3-click dashboard access | PARTIAL | arescore registration; 3-click rule unproven — audit required |
| M-06 | Dedup/consolidate/reuse | OPEN | 1 directive(s) — see FRSP.md §5 |
| M-07 | 100% coverage, all green/clean | UNPROVEN | 3 workflows exist (not product tests) — no verified 100% run on record |
| M-08 | Live operational validation | UNVERIFIED | This pass was static (no code executed); runtime proof owed by FRSP execution |
| M-09 | Traceability & auditability | MINIMAL | Observability signals vary; correlation-ID + decision-record standard mandated |
| M-10 | Total data retention | POLICY-SET | Retention law encoded in FRSP.md §12; archive-never-destroy from this date |

### Deduplication / consolidation directives (repo-specific)

- **DD-01:** Site-kit extraction

### Re-grounded gap register (adds to, never replaces, the register below)

- **RG-01:** Same as siblings + lead-capture handling decision

### Fleet context this repo must honor

- Canonical local-LLM provider: **olaman (Ollama gateway/control plane, port 8030) fronting host Ollama at 127.0.0.1:11434**
- Canonical fleet dashboard/command center: **arescore (ClawMedia command center, app/server.js :8889; Arescore hub seed http://127.0.0.1:8890/)**
- Canonical skills SSOT: **agency (SSOT skill registry, 708-skill capability manifest)**
- Known fleet port collisions (resolve via the arescore port registry): 8030: olaman vs dev-analytics api; 8741: freeai backend vs myskills; 8000: mia, lab, peni, myprd backends (+fira internal); 8028: fira frontend vs midas (full list in FRSP.md §1)

<!-- REGROUND:reground-20260815-python-fleet:END -->


## Review Metadata

- **Review date:** 2026-07-03 (repo local-clock artifacts reference 2026-07-04 in one file timestamp; treated as immaterial)
- **Repo root path:** `C:\Users\mcgac\Python\intelastart.com`
- **Languages/frameworks detected:** Static HTML5, CSS3 (custom, no framework/preprocessor), vanilla JavaScript (ES6, no framework, no bundler, no `package.json`/`node_modules`). No backend language, no server runtime.
- **App type determination:** **Static B2B marketing/consulting website** hosted on GitHub Pages, with a large parallel layer of **AI-agent-orchestration meta-tooling** (prompts, rules, agent manifests, swarm-governance CI) that governs *how AI coding agents edit this repo* — this meta-layer is NOT a product feature of the intelastart.com website itself and must not be confused with in-product AI/agentic capability. Justification: `docs/ARCHITECTURE.md` explicitly states "Backend Tier: Framework: None," `AGENT.md` declares `type: static-site`, `docs/PRD.md` states "Static HTML site — no backend or CRM," `CONTRIBUTING.md` confirms "No build step required," and the only interactive element (`js/main.js`) is client-side DOM/animation code with a simulated (non-functional) form submit. This determination is code-verified, not doc-assumed.
- **Review mode:** Blitz — single-session, sampled evidence (targeted reads of all HTML/CSS/JS files, all docs/*.md, all audit/*.md, CI workflows, manifests; not every prompt/rule/skill/agent meta-file was read in full given their volume and irrelevance to the shipped product).
- **Commands/tools run:** Glob (directory enumeration, targeted extension searches for images/secrets/env files), Grep (14 targeted keyword sweeps across the full tree), Read (~35 files: all HTML pages sampled, `js/main.js` in full, `css` referenced but not fully read, all `docs/*.md`, all `audit/*.md`, `.github/workflows/*.yml`, `AGENT.md`, `AGENTS.md` referenced, `CONTRIBUTING.md`, `CHANGELOG.md`, `sitemap.xml`, `robots.txt`, `CNAME`, `.vscode/tasks.json`, `docs/.template-meta.yaml`).
- **Git history:** **Bash (`git log`, `git branch`, `git tag`, `git status`) worked successfully** via `mcp__workspace__bash` at path `/sessions/epic-tender-pasteur/mnt/Python/intelastart.com/` — no fallback to raw `.git/` file reads was needed. 20 most recent commits reviewed (spanning 2026-02-14 initial launch through 2026-07-03); single branch `master` tracking `origin/master`; no tags; large uncommitted working-tree diff present at review time (70+ modified files, mostly meta/doc-governance files, not core site pages beyond minor doc drift).
- **Tests/CI discovered:** **Yes, but not for the product itself.** Three GitHub Actions workflows exist: `ai-review.yml` (gates AI-assisted doc review, but references `scripts/ai-review.sh` which **does not exist** in the repo — the step no-ops with an echo if missing), `doc-lint.yml` (markdownlint + frontmatter/link validation for `docs/**/*.md` only), `swarm-gate.yml` (validates presence/schema of `AGENT.md`/`AGENTS.md` governance files only). **No workflow builds, tests, lints, or deploys the actual HTML/CSS/JS site.** No `tests/`, `test/`, `__tests__/`, or `spec/` directory exists. `docs/TEST_STRATEGY.md` and `CONTRIBUTING.md` both *prescribe* Lighthouse/axe/Playwright/linkinator testing, but no config, script, or CI job implementing any of it was found — confirmed via Grep and directory listing. The repo's own `audit/org_audit_2026-03-29.md` independently states "Tests: no... Pre-commit: no."
- **Overall confidence:** **High** for what exists/doesn't exist in the shipped site (directly verified in HTML/JS/CSS and confirmed by the repo's own prior internal audits). **Medium-high** for prioritization/ROI scoring (inherently judgment-based). One item flagged "Needs confirmation" and excluded from the FR count (see Gap Analysis).

---

## Existing Capabilities Found

- Multi-page static site: homepage (`index.html`), `about.html`, `blog.html` + 3 blog articles, `pricing.html`, 3 service detail pages (`services/ai-automation.html`, `services/market-intelligence.html`, `services/saas-comparison.html`), `privacy.html`, `terms.html`.
- Custom-domain hosting via GitHub Pages: `CNAME` file present (`intelastart.com`); DNS/A-record setup documented in `docs/DEPLOYMENT.md`.
- `robots.txt` and `sitemap.xml` present and internally consistent (12 URLs listed, all resolve to real files).
- Schema.org JSON-LD structured data on homepage: `Organization` and `Service` types with `OfferCatalog`, present in `index.html` lines 17–71.
- Open Graph meta tags on homepage (`og:title`, `og:description`, `og:type`, `og:url`).
- Responsive/interactive front-end behavior in `js/main.js`: sticky nav on scroll, mobile nav toggle, `IntersectionObserver`-based scroll-reveal animations, animated stat counters, smooth-scroll anchor links, parallax hero effect, 3D tilt-on-hover for cards, page-load fade-in.
- Client-side-only contact form and newsletter form markup (HTML present in `index.html` lines 326–390) with front-end validation attributes (`required`, `type="email"`).
- Pricing page with 3 tiers (Starter $499/mo, Growth $1,999/mo, Enterprise Custom) consistently represented across `index.html` and `pricing.html`.
- Privacy Policy (`privacy.html`) and Terms of Service (`terms.html`) pages present with dated content ("Last updated: February 14, 2026").
- Dependabot configured for `pip` and `github-actions` ecosystems (`.github/dependabot.yml`) — notable mismatch: repo has no Python dependencies to update (see Gap Analysis).
- Three GitHub Actions workflows: `doc-lint.yml` (markdown/frontmatter lint), `ai-review.yml` (AI doc-review gate, partially unimplemented), `swarm-gate.yml` (governance-file presence check).
- Extensive internal documentation suite: `docs/PRD.md`, `docs/ARCHITECTURE.md`, `docs/SECURITY.md`, `docs/DEPLOYMENT.md`, `docs/TEST_STRATEGY.md`, `docs/ROADMAP.md`, `docs/DEVELOPMENT.md`, `docs/RUNBOOK.md`, ADR log, `CHANGELOG.md`.
- Self-authored prior audits already on file (`audit/security_report.md`, `audit/technical_debt.md`, `audit/review_overview.md`, `audit/agent_readiness.md`, `audit/architecture_analysis.md`, `audit/copilot_optimization.md`, `audit/org_audit_2026-03-29.md`, all dated 2026-03-29) that independently corroborate several gaps identified in this review.
- Meta-layer of AI-agent operating rules (`rules/rule_001`–`010`), prompts (`prompts/system/*`, `prompts/agents/*`), and agent role manifests (`agents/*.md`) — this is tooling for *how AI agents should edit this repo's content*, not a feature of the public website.
- `.vscode/tasks.json` with local-dev convenience tasks (`live-server`, Python `http.server`, git status-on-open, manual deploy-push task).

---

## Evidence Ledger

| Evidence ID | Area | Evidence Type | File/Path/Command | Finding | Confidence |
|---|---|---|---|---|---|
| E-001 | App type | Config/doc | `docs/ARCHITECTURE.md` | "Backend Tier: Framework: None"; static HTML frontend | High |
| E-002 | App type | Config | `AGENT.md` | `type: static-site`, no build/test/lint/deploy commands defined | High |
| E-003 | Build tooling | Manifest search | Glob for `package.json`, `requirements.txt`, `pyproject.toml`, etc. | None found anywhere in repo | High |
| E-004 | Contact form | Code | `js/main.js` lines 108–146 | Form submit handler uses `setTimeout` to fake success; comment reads "Simulate form submission" / "In production, you would send this to your backend"; data only goes to `console.log` | High |
| E-005 | Newsletter form | Code | `js/main.js` lines 149–176 | Same simulated-submit pattern as contact form; no real endpoint | High |
| E-006 | Form backend | Grep | Search for `formspree\|netlify\|recaptcha\|honeypot\|action=` across all `*.html` | Zero matches — no third-party form service wired in, despite `docs/SECURITY.md` and `docs/DEPLOYMENT.md` describing Formspree/Netlify Forms as the intended approach | High |
| E-007 | CSP / security headers | Grep | Search for `Content-Security-Policy\|X-Frame-Options\|Strict-Transport-Security` across all `*.html` | Zero matches in any shipped HTML file | High |
| E-008 | CSP gap self-admitted | Doc | `audit/security_report.md` line 12 | Repo's own prior audit (2026-03-29) lists "No CSP" as a Medium-severity finding | High |
| E-009 | Analytics | Grep | Search for `google-analytics\|gtag\|googletagmanager\|G-[A-Z0-9]` across all `*.html` | Zero matches — no analytics tag installed on any page | High |
| E-010 | Analytics gap self-admitted | Doc | `audit/technical_debt.md` line 12 | "Analytics — Not confirmed — High priority" per repo's own audit | High |
| E-011 | Case studies | Glob/content | Search for case-study files/pages; homepage only has 3 short testimonial quotes (`index.html` lines 286–314) | No dedicated case-study page or evidentiary detail (no client logos, no linked proof) exists | High |
| E-012 | Case study gap self-admitted | Doc | `audit/technical_debt.md` line 11, `audit/review_overview.md` lines 23–24 | "Case studies page — Absent — High priority"; "Unverifiable claims... could violate FTC guidelines if not substantiated" | High |
| E-013 | Broken image reference | Code | `index.html` line 24 vs. Glob for `*.png/*.jpg/*.svg/*.webp/*.ico` | JSON-LD references `https://intelastart.com/images/logo.png`; no `images/` directory or any image file exists in the entire repo | High |
| E-014 | Booking/scheduling | Grep/content review | No Calendly/scheduling embed found in any HTML file; all CTAs route to `#contact` anchor or `mailto:` | No booking system present | High |
| E-014b | Booking gap self-admitted | Doc | `audit/technical_debt.md` line 10, `audit/agent_readiness.md` line 24 | "Booking system (Calendly) — Absent — High priority" | High |
| E-015 | Product CI/tests | Directory search | Glob/find for `tests/`, `test/`, `__tests__/`, `spec/`, Lighthouse config, Playwright config | None found | High |
| E-016 | CI workflow scope | Code | `.github/workflows/doc-lint.yml`, `swarm-gate.yml` | Both operate only on Markdown/governance files, not HTML/CSS/JS | High |
| E-017 | AI-doc-review script gap | Code | `.github/workflows/ai-review.yml` lines 41–46 | Workflow calls `scripts/ai-review.sh`; file does not exist; step echoes a warning and no-ops instead of failing | Medium-High |
| E-018 | Self-audit: no tests | Doc | `audit/org_audit_2026-03-29.md` lines 13–19 | "Tests: no... Pre-commit: no... CI: swarm-gate" (only) | High |
| E-019 | Dependabot ecosystem mismatch | Config | `.github/dependabot.yml` | Configured for `pip` ecosystem; repo has zero Python files/dependencies | High |
| E-020 | Secrets hygiene | Glob | Search for `.env`, `.env.*`, `*.pem`, `*.key`, `*secret*`, `*credential*` tracked files | None found except `rules/rule_009_secrets.md` (a policy doc, not a secret) | High |
| E-021 | Accessibility/perf claims vs. verification | Doc | `docs/TEST_STRATEGY.md`, `CONTRIBUTING.md` | Both prescribe Lighthouse ≥90 and axe DevTools checks as gates, but no automation or evidence of a passing run exists in-repo | Medium |
| E-022 | Social/brand overlap | Content | `index.html` lines 377–378, 441; `audit/review_overview.md` line 27 | Intelastart's X/LinkedIn links point to `@aresmaxus` / `aresmax-digital`, a separate brand per the repo's own audit — no dedicated Intelastart social presence | High |
| E-023 | Blog volume | Directory listing | `blog/` contains exactly 3 articles | Confirmed low content volume; repo's own audit flags "Expanded blog (15+ articles) — 3 articles only — Medium priority" (`audit/technical_debt.md` line 16) | High |
| E-024 | Rate limiting / WAF | Grep | Search for `ratelimit\|rate.limit\|limiter\|throttle` | No matches anywhere — not applicable to a static site with no backend, but relevant to spam protection on future form backend | High |
| E-025 | AI/agentic in-product capability | Grep + read | Search for `eval`, `prompt registry`, `model routing`, `fallback`, `RAG`, etc. | All matches are in repo-governance/tooling docs (`rules/rule_006_llm_routing.md`, `prompts/system/claude_system_prompt.md` mentioning "RAG retrieval from SQLite + FAISS" for the *coding agent's own context*, not a site feature) — zero evidence of AI/agentic capability in the shipped website itself | High |
| E-026 | Git activity | Bash | `git log --oneline -20` | 20 commits reviewed; heavy recent activity is documentation/governance-layer churn (audits, PRDs, agent manifests), not site-feature development; last direct content commit dated 2026-06-12 ("seeded README") | High |
| E-027 | Governance files | Glob | `LICENSE`, `SECURITY.md` (root), `CODEOWNERS`, `CONTRIBUTING.md` | `CONTRIBUTING.md` present; `docs/SECURITY.md` present (not root `SECURITY.md`); no `LICENSE` file found; no `CODEOWNERS` file found | High |

---

## Threat Model Summary (STRIDE-brief)

- **Spoofing:** Low surface — no authentication system exists to spoof (correctly out of scope per `docs/PRD.md` §7). Residual risk: no SPF/DKIM/DMARC evidence for `hello@intelastart.com`, so email spoofing of the brand's contact address is unmitigated but unverifiable from this repo alone.
- **Tampering:** Content integrity relies entirely on GitHub Pages' HTTPS delivery and repo push access; no Subresource Integrity (SRI) hashes on any external font/script reference, and no CSP to constrain injected content if a dependency (e.g., Google Fonts) is compromised (E-007).
- **Repudiation:** Not applicable in a meaningful sense — no user actions are logged server-side because there is no server; the simulated form (E-004) means there is also no audit trail of actual lead submissions, which is itself a business risk, not just a security one.
- **Information Disclosure:** Public contact email is exposed directly in JSON-LD (`index.html` line 27), inviting scraping/spam — flagged as Low severity in the repo's own `audit/security_report.md` line 9. No secrets found tracked in the repo (E-020).
- **Denial of Service:** Static GitHub Pages hosting is inherently DoS-resistant at the infrastructure layer; not a meaningful concern for this app type.
- **Elevation of Privilege:** Not applicable — no privilege tiers exist in a static site with no accounts.

---

## AI Governance Summary

**Not applicable to the shipped product** — no AI/agentic capability is evidenced in the intelastart.com website itself (E-025). The repository contains a substantial *AI-coding-agent operating layer* (rules, prompts, agent manifests, swarm-gate CI) that governs how AI assistants are permitted to modify this repo, but this is developer/repo tooling, not a customer-facing feature, and per the task's hard rules is out of scope for feature-request analysis of the product. No prompt registry, model routing, eval harness, cost controls, or audit logging exists for any user-facing AI feature because there is no user-facing AI feature.

---

## Competitive Benchmark Matrix

| Dimension | Industry Standard/Tool | intelastart.com Current State | Relevant? | Gap |
|---|---|---|---|---|
| Error tracking | Sentry (or similar) | Not present; no JS error monitoring | Yes — any static site benefits from front-end error visibility | No error tracking of any kind (FR-006) |
| Web analytics | GA4 / Plausible / Fathom | Not present (E-009) | Yes — explicitly a stated PRD KPI dependency (docs/PRD.md §2 GA4 funnel/session goals) | Cannot measure any PRD-stated KPI today (FR-001) |
| Security headers | OWASP secure-headers baseline (CSP, HSTS, X-Frame-Options) | Not present (E-007), documented as a TODO in `docs/SECURITY.md` | Yes | Doc describes target state; code has zero implementation (FR-002) |
| CI/CD for site changes | Standard static-site CI (HTML validation, Lighthouse CI, link-check, auto-deploy) | Only doc-linting and governance-schema CI exist; no HTML/CSS/JS validation, no Lighthouse CI (E-015, E-016) | Yes | `docs/TEST_STRATEGY.md` and `CONTRIBUTING.md` prescribe checks that have zero automation (FR-004, FR-005) |
| Lead-capture reliability | Formspree / Netlify Forms / HubSpot forms (industry-standard for static sites) | Form is a JS simulation with no backend (E-004, E-006) | Yes — directly threatens the PRD's #1 stated goal ("Generate qualified leads") | Highest-severity gap found (FR-003) |
| Supply-chain hygiene (SLSA, SBOM, secret scanning) | SLSA provenance, Dependabot, gitleaks | Dependabot present but misconfigured for a nonexistent `pip` ecosystem (E-019); no gitleaks/secret-scanning workflow found | Partially — low blast-radius for a static site, but Dependabot misconfig is a concrete, fixable finding | Dependabot tracks the wrong ecosystem; GitHub Actions versions aren't scanned for supply-chain risk beyond Dependabot's own coverage (FR-007) |
| Structured data validity | Google Rich Results Test / schema.org validator | Organization + Service JSON-LD present but references a nonexistent image asset (E-013) | Yes — directly affects SEO rich-result eligibility, a stated PRD goal | Broken `logo` field will fail Google's Merchant/Organization logo validation (FR-008) |

Not relevant to this app type and therefore excluded: SLSA v1.2 provenance/attestation pipelines, OpenTelemetry semantic conventions, DORA deployment metrics, OWASP ASVS levels, NIST SSDF, LangGraph/LangSmith/Langfuse, Temporal, Backstage, GitHub Copilot coding agent/Cursor — none apply to a static marketing site with no backend, no deployment pipeline beyond GitHub Pages auto-publish, and no AI/agentic product surface.

---

## Gap Analysis Summary

The single largest verified gap is that **the site's lead-capture mechanism — its core stated business function per `docs/PRD.md` ("Generate qualified leads... Contact form submissions 10+/month")** — is a client-side simulation that never contacts a server, CRM, or email address (E-004, E-005, E-006). Every form submission is silently discarded to the browser console. This is corroborated by the repo's own prior internal audit dated 2026-03-29, meaning the gap has been known for roughly three months without remediation as of this review.

Close behind: the site makes specific, quantified business claims ("500+ automations deployed," "$2M+ revenue generated," 3 named client testimonials) with zero substantiating evidence (case studies, logos, links) — a self-identified FTC-substantiation risk (E-012). No analytics exist to measure any of the PRD's stated KPIs (E-009, E-010). Security posture described in `docs/SECURITY.md` (CSP, headers) is aspirational documentation with zero corresponding implementation (E-007, E-008). A structured-data image reference is broken (E-013), which will fail Google Rich Results validation. CI/CD only validates Markdown formatting and internal governance-file schemas — it does not build, lint, or test the actual website (E-015, E-016). Dependabot is configured for an ecosystem (`pip`) that doesn't exist in this repo, meaning it currently provides zero real supply-chain coverage (E-019).

**Needs confirmation — excluded from verified count:** Whether GitHub Pages "Enforce HTTPS" is actually toggled on in repository settings cannot be verified from repository file contents alone (it's a GitHub UI/API setting, not a committed file); `docs/SECURITY.md` instructs verifying it but the setting itself is outside this repo's inspectable surface. This is NOT counted as a FR since it may already be correctly configured — flagging only for awareness.

---

## Feature Requests

### FR-001: Wire the Contact Form to a Real Lead-Delivery Backend

**Description:** Replace the `setTimeout`-simulated submit handler in `js/main.js` (lines 108–146) with an actual integration to a third-party form service (Formspree, Netlify Forms, or a HubSpot/CRM form endpoint) so that form submissions are actually delivered to `hello@intelastart.com` or a CRM, matching the approach both `docs/SECURITY.md` and `docs/DEPLOYMENT.md` already prescribe.

**Why It Matters:** This is the site's single stated primary business goal per `docs/PRD.md` §2 ("Generate qualified leads — Contact form submissions — 10+/month"). Currently, zero leads can possibly be captured through the form; every submission is discarded client-side.

**Verification Evidence:** `js/main.js` lines 122–144 contain the comment "// Simulate form submission" and "// In production, you would send this to your backend"; form data is only passed to `console.log('Form submitted:', formData)`. No `action=` attribute, Formspree ID, or fetch/XHR call to any endpoint exists anywhere in the HTML or JS. Confirmed independently by the repo's own `audit/technical_debt.md` ("Contact form with working handler — Email address only — High") and `audit/review_overview.md` ("No contact form handler... increases bounce rate").

**Evidence IDs:** E-004, E-006, E-008 (adjacent), audit corroboration in ledger

**Priority:** P0

**Category:** Conversion / Core Business Function

**ROI Score:** 10 — Directly enables the site's only revenue-generating mechanism (revenue/adoption 25% weight fully realized); zero current lead capture means this is pure upside with no cannibalization risk.

**Risk Score:** 3 — Low complexity (well-documented pattern, third-party service does the heavy lifting), low blast radius (isolated to one form component), no migration needed, but does introduce a new vendor dependency (Formspree/Netlify) and a small privacy-impact surface (form data now leaves the browser to a third party) that must be reflected in `privacy.html`.

**Dependencies:** Choice of form-service vendor (Formspree/Netlify Forms/HubSpot); update to `privacy.html` disclosure language; spam protection (see FR-009).

**Competitive Reference:** Standard practice for every static-site marketing page (Formspree/Netlify Forms are the two most common patterns for GitHub Pages sites specifically, per the repo's own `docs/SECURITY.md`).

**Security/Privacy Impact:** Form data (name, email, company, message) will now transit to a third-party processor — `privacy.html` must be updated to disclose this processor by name; no CRM API secrets should ever appear client-side (already codified in `rules/rule_009_secrets.md` and `CONTRIBUTING.md`).

**Rollout Readiness:** High — this is a scoped, well-understood, low-risk change with existing internal documentation already describing the target implementation.

**Validation Gates:** (1) Submit a real test inquiry and confirm receipt at `hello@intelastart.com` or configured CRM within SLA; (2) Confirm no API keys/secrets appear in page source after integration; (3) Confirm `privacy.html` is updated to name the processor before the change ships to production.

**Acceptance Criteria:** (1) A test form submission arrives in the configured inbox/CRM within 5 minutes; (2) Network tab shows a real POST request to the form-service endpoint on submit; (3) Success and error UI states both render correctly (currently only a hardcoded success path exists — no error path is implemented at all).

---

### FR-002: Implement the Documented CSP and Security Headers

**Description:** Add the Content-Security-Policy `<meta>` tag (or equivalent HTTP header via GitHub Pages/Cloudflare) already drafted in `docs/SECURITY.md` to all HTML pages, and confirm HSTS is enforced at the DNS/CDN layer as the same document instructs.

**Why It Matters:** The repo has fully specified its intended CSP policy in documentation but implemented it in zero of the 10 HTML pages, meaning external script/font/style loads (Google Fonts, Google Tag Manager references, etc.) are currently unconstrained — exactly the gap the repo's own security document was written to close.

**Verification Evidence:** Grep for `Content-Security-Policy|X-Frame-Options|Strict-Transport-Security` across every `*.html` file returned zero matches. `audit/security_report.md` line 12 independently lists "No CSP" as a Medium-severity finding from a prior audit dated 2026-03-29 — meaning this gap has persisted for roughly three months.

**Evidence IDs:** E-007, E-008

**Priority:** P1

**Category:** Security Hardening

**ROI Score:** 5 — Meaningful trust/UX and risk reduction (20% risk weight, 15% trust weight) but no direct revenue lift; mostly a defense-in-depth improvement for a low-attack-surface static site.

**Risk Score:** 3 — Low complexity (copy-paste a meta tag documented already), but requires care to avoid breaking Google Fonts/Analytics if/when added (FR-006/FR-007-adjacent); low blast radius since a misconfigured CSP only affects rendering, not data.

**Dependencies:** Should be sequenced after analytics (FR-006) is added so the CSP's `connect-src`/`script-src` allowlist is written once against the final third-party script set, not twice.

**Competitive Reference:** OWASP secure-headers baseline; the CSP text already exists verbatim in `docs/SECURITY.md` lines 12–21.

**Security/Privacy Impact:** Directly reduces XSS/injection blast radius from any compromised third-party script (fonts, analytics, form widget).

**Rollout Readiness:** High — policy text is pre-written; only needs to be pasted into each page `<head>` and tested for breakage.

**Validation Gates:** (1) Verify no console CSP-violation errors appear on any of the 10 pages after rollout; (2) Confirm Google Fonts and any analytics script still load correctly; (3) Run a header-scanner tool (e.g., securityheaders.com) against the live domain post-deploy and confirm a passing grade.

**Acceptance Criteria:** (1) All 10 HTML pages contain the CSP meta tag; (2) Zero CSP violations logged in browser DevTools on any page; (3) HSTS confirmed active via `curl -I https://intelastart.com` showing `Strict-Transport-Security` header.

---

### FR-003: Add Case Study Evidence to Substantiate Quantified Claims

**Description:** Build at least 2–3 detailed case-study pages (or a dedicated case-studies section) that substantiate the specific numeric claims already published on the homepage ("500+ automations deployed," "$2M+ revenue generated," "80% processing time cut... saved $120K," named testimonials from "Sarah Chen," "Marcus Rodriguez," "Emily Watson").

**Why It Matters:** The repo's own prior audit flags this as a legal/credibility risk: publishing specific, quantified business-outcome claims without any linked or verifiable evidence creates FTC-substantiation exposure and undermines the "Enterprise Evaluator" persona's stated need for "case studies and ROI" per `docs/PRD.md` §3.

**Verification Evidence:** Homepage (`index.html` lines 281–316) contains three testimonial blocks with named individuals and specific dollar/percentage figures, but no case-study page, client logo, or external verification link exists anywhere in the repo (confirmed via directory listing and Glob for case-study-related filenames). `audit/review_overview.md` line 23 independently states: "Unverifiable claims... could violate FTC guidelines if not substantiated," and `audit/technical_debt.md` line 11 lists "Case studies page — Absent — High priority."

**Evidence IDs:** E-011, E-012

**Priority:** P1

**Category:** Trust & Content

**ROI Score:** 6 — Meaningful trust/UX (15% weight) and differentiation (10% weight) impact for the "Enterprise Evaluator" persona explicitly named in the PRD; indirect revenue effect since it targets the highest-value customer segment.

**Risk Score:** 4 — Legal/compliance risk (5% weight) is actually the reverse — NOT doing this is the risk; the risk of doing it is primarily content-creation effort and the need for real, verifiable client data (which may not exist yet, per audit finding "Consulting site without consultants" concern in `audit/review_overview.md` line 25).

**Dependencies:** Requires real client engagement data or explicit "illustrative example" labeling per `CONTRIBUTING.md`'s own content standard ("Testimonials and case studies must be real or clearly marked as illustrative").

**Competitive Reference:** Standard B2B consulting-site pattern; every competitor named implicitly in `docs/PRD.md` §5 ("Competing AI automation agencies") would be expected to have this.

**Security/Privacy Impact:** None directly, though any real client data used must have consent/NDA clearance before publication.

**Rollout Readiness:** Medium — content creation and possible client sign-off required before this can ship, unlike the purely technical FRs above.

**Validation Gates:** (1) Legal/counsel review of all quantified claims before publishing, per the repo's own `audit/security_report.md` recommendation #2; (2) Confirm every testimonial is either real (with consent) or explicitly labeled illustrative per `CONTRIBUTING.md`; (3) Verify new case-study pages are added to `sitemap.xml`.

**Acceptance Criteria:** (1) At least 2 case studies published with either real client attribution or explicit "illustrative" labeling; (2) Homepage testimonial section links to full case studies; (3) `sitemap.xml` updated to include new URLs.

---

### FR-004: Automate the Documented Lighthouse/Accessibility/Link-Check Test Suite in CI

**Description:** Implement a GitHub Actions workflow that actually runs the Lighthouse (Performance/Accessibility/SEO ≥90), axe accessibility, and `linkinator` link-checking procedures that `docs/TEST_STRATEGY.md` and `CONTRIBUTING.md` already prescribe as mandatory gates, but which currently have no corresponding automation anywhere in the repo.

**Why It Matters:** Both `docs/TEST_STRATEGY.md` and the PR checklist in `CONTRIBUTING.md` state these checks as required before every push/merge, but they are entirely manual (or entirely unenforced) today — the only CI that exists (`doc-lint.yml`, `swarm-gate.yml`) validates Markdown and governance-file schemas, not the website itself.

**Verification Evidence:** Directory search for `tests/`, `test/`, `__tests__/`, `spec/`, Lighthouse CI config (`lighthouserc.json` or similar), or Playwright config found nothing. `.github/workflows/` contains exactly 3 workflows, none of which touch `.html`, `.css`, or `.js` files. The repo's own `audit/org_audit_2026-03-29.md` independently confirms "Tests: no."

**Evidence IDs:** E-015, E-016, E-018, E-021

**Priority:** P1

**Category:** CI/CD & Quality Gates

**ROI Score:** 5 — Velocity (15% weight) and trust/UX (15% weight) benefits from catching regressions automatically; no direct revenue impact but reduces the chance of a broken pricing table or inaccessible form shipping to production.

**Risk Score:** 3 — Low complexity (Lighthouse CI and linkinator are well-documented, widely-used GitHub Actions); no migration or blast-radius concern since this is purely additive tooling.

**Dependencies:** None blocking; can be implemented independently of other FRs, though ideally sequenced after FR-001 (contact form) so form-submission testing has a real endpoint to validate against.

**Competitive Reference:** Lighthouse CI is the de facto standard for static-site performance gating; `docs/TEST_STRATEGY.md` §1 and §9 already name Lighthouse and Playwright explicitly as the intended tools.

**Security/Privacy Impact:** None — purely a quality/performance gate.

**Rollout Readiness:** High — tools and thresholds are already fully specified in existing documentation; this is an implementation gap, not a design gap.

**Validation Gates:** (1) New workflow runs successfully on a test PR and produces a Lighthouse report artifact; (2) Workflow fails the PR when a score drops below the documented thresholds (Performance ≥90, Accessibility ≥90, SEO ≥95); (3) `linkinator` step catches at least one intentionally-broken link in a test PR to confirm it's wired correctly.

**Acceptance Criteria:** (1) A GitHub Actions workflow exists that runs on every PR touching `*.html`/`*.css`/`*.js`; (2) The workflow enforces the exact thresholds documented in `docs/TEST_STRATEGY.md` §1; (3) A broken internal link or missing `alt` attribute causes the workflow to fail visibly in the PR checks.

---

### FR-005: Fix Dependabot Configuration to Match Actual Repo Ecosystem

**Description:** Correct `.github/dependabot.yml` to remove or replace the `pip` package-ecosystem entry (the repo has zero Python files or dependencies) and, if any JS tooling is later introduced (e.g., via FR-004's Lighthouse CI or a future build step), add the appropriate ecosystem (`npm`/`github-actions`) instead.

**Why It Matters:** Dependabot currently provides no real supply-chain coverage because it's configured to scan a package ecosystem (`pip`) that doesn't exist in the repository — it will simply find nothing to update, giving a false sense of coverage while the `github-actions` ecosystem entry (which is legitimately useful, since `actions/checkout@v6` etc. are in use) is the only one doing real work.

**Verification Evidence:** `.github/dependabot.yml` lines 3–5 configure `package-ecosystem: "pip"` with `directory: "/"`; Glob/directory search confirms zero `.py`, `requirements.txt`, or `pyproject.toml` files exist anywhere in the repository.

**Evidence IDs:** E-019

**Priority:** P2

**Category:** Supply Chain Hygiene / Config Correctness

**ROI Score:** 2 — Very low direct business impact; this is a hygiene/correctness fix with no user-facing effect.

**Risk Score:** 1 — Trivial, one-line config change with zero blast radius; the only "risk" is doing nothing, which costs nothing either.

**Dependencies:** None.

**Competitive Reference:** Dependabot best practice is to only configure ecosystems that actually exist in a repo to avoid noise/false confidence.

**Security/Privacy Impact:** None directly; marginally improves supply-chain hygiene clarity.

**Rollout Readiness:** High — single-file, single-line change.

**Validation Gates:** (1) Confirm the `pip` entry is removed or repo actually gains Python dependencies to justify it; (2) Confirm `github-actions` entry remains and continues to fire PRs (as seen in git history — `fcea64c chore(deps): bump actions/checkout from 4 to 6`); (3) No Dependabot errors appear in the repo's Insights → Dependency graph tab after the change.

**Acceptance Criteria:** (1) `.github/dependabot.yml` no longer references a nonexistent ecosystem; (2) `github-actions` ecosystem entry is preserved and continues to function (verifiable via existing merged PR #1 in git history); (3) If JS tooling is added later (FR-004), a corresponding `npm` entry is added in the same change.

---

### FR-006: Add Front-End Error Monitoring (Sentry or Equivalent)

**Description:** Add a lightweight JavaScript error-monitoring snippet (e.g., Sentry's browser SDK, or a simpler alternative) to catch and report any runtime JS errors (e.g., a broken `IntersectionObserver`, a null-reference on a missing DOM element) that would otherwise silently degrade the animated/interactive experience with zero visibility to the site owner.

**Why It Matters:** `js/main.js` contains several `document.querySelector` calls without defensive null-checks in some paths (e.g., `document.getElementById('name').value` inside the form handler would throw if the DOM structure ever drifts from the JS assumptions during a future edit) — with no monitoring, such a regression would only be discovered by a human noticing the page "feels broken," not from any alert.

**Why It Matters (cont.):** This directly supports the operational maturity target implied by `docs/ROADMAP.md`'s "Future: Performance optimization" and "Planned: CI/CD improvements" without requiring a backend.

**Verification Evidence:** Grep for `sentry`, `opentelemetry`, `prometheus`, `tracing`, `metrics` across the entire repo returned zero matches in any HTML/JS file (only doc/PRD-adjacent word coincidences). No error-boundary or monitoring script tag exists in any page `<head>` or before `</body>`.

**Evidence IDs:** E-009 (analytics-adjacent absence), general grep sweep (no dedicated evidence ID — negative finding across full-repo keyword sweep)

**Priority:** P2

**Category:** Observability

**ROI Score:** 3 — Low direct revenue impact, but non-trivial opex savings (10% weight) from catching regressions before a customer reports them; a nice-to-have for a single-maintainer site per `docs/PRD.md` §6 ("Maintainer is a solo operator").

**Risk Score:** 2 — Low complexity, well-trodden integration path (single script tag); minor vendor dependency (10% weight) is the only real consideration, plus it must be added to the CSP `script-src`/`connect-src` allowlist from FR-002.

**Dependencies:** Should be sequenced together with or after FR-002 (CSP) since the monitoring script's domain needs to be allowlisted.

**Competitive Reference:** Sentry's browser SDK is the most common lightweight choice for exactly this kind of static-site error monitoring.

**Security/Privacy Impact:** Sentry (or equivalent) captures browser errors which may include user input context — `privacy.html` should be updated to disclose this if PII could appear in error payloads (e.g., form field values in a stack trace).

**Rollout Readiness:** High — trivial technical integration, though privacy-disclosure update is a small dependency.

**Validation Gates:** (1) Deliberately trigger a JS error in a staging/test copy and confirm it appears in the monitoring dashboard; (2) Confirm the monitoring script doesn't violate the new CSP from FR-002; (3) Confirm `privacy.html` is updated if any PII could be captured in error payloads.

**Acceptance Criteria:** (1) Monitoring SDK is present in all 10 HTML pages; (2) A test error successfully appears in the monitoring dashboard within a few minutes of being triggered; (3) No CSP violations result from the added script.

---

### FR-007: Add Web Analytics to Measure Stated PRD KPIs

**Description:** Install GA4 (or a privacy-friendly alternative like Plausible/Fathom) across all pages so the specific KPIs the PRD already commits to measuring — "Contact form submissions," "Pricing page to contact conversion ≥5%," "Blog organic sessions +20% MoM," "Time on page (pricing) >90s" — can actually be measured.

**Why It Matters:** Every KPI in `docs/PRD.md` §2's goals table explicitly names "GA4" or "GA4 / GSC" as the measurement method, but no analytics tag of any kind exists on any page today — meaning none of the PRD's five stated success metrics can currently be tracked at all.

**Verification Evidence:** Grep for `google-analytics|gtag|googletagmanager|G-[A-Z0-9]` across all `*.html` files returned zero matches. `audit/technical_debt.md` line 12 independently lists "Analytics — Not confirmed — High priority," and `docs/DEPLOYMENT.md`'s own post-deploy checklist includes the caveated line "Analytics recording sessions (if configured)" — implying the deploying maintainer was themselves unsure whether analytics was active.

**Evidence IDs:** E-009, E-010

**Priority:** P1

**Category:** Measurement / Analytics

**ROI Score:** 6 — Without this, the business literally cannot know whether any other investment (FR-001 through FR-004) is working; high leverage (5% weight) but foundational enough to rate above its raw weight suggests.

**Risk Score:** 2 — Low complexity (single script tag), but does require a CSP allowlist update (FR-002 dependency) and a privacy-policy disclosure update, plus a decision on cookie-consent banner necessity depending on target jurisdictions (GDPR-adjacent consideration given "Worldwide" `areaServed` in the Service schema).

**Dependencies:** FR-002 (CSP allowlist), possible cookie-consent banner if GA4 (cookie-based) is chosen over a cookieless alternative like Plausible, given `index.html`'s Service schema declares `"areaServed": "Worldwide"`.

**Competitive Reference:** GA4 is explicitly the tool already named in the PRD itself — this FR closes the gap between stated intent and implementation rather than introducing a new idea.

**Security/Privacy Impact:** Adds a third-party tracking script; `privacy.html` must accurately disclose analytics collection per `docs/SECURITY.md`'s own instruction ("Privacy policy... must accurately describe what data is collected via forms and analytics") — currently this instruction cannot even be followed since there's nothing to disclose.

**Rollout Readiness:** High — GA4/Plausible integration is a well-known, low-effort pattern; the main decision is vendor choice (cookie-based vs. cookieless) given the worldwide audience.

**Validation Gates:** (1) Confirm real-time GA4/Plausible dashboard shows a test pageview after rollout; (2) Confirm `privacy.html` is updated with accurate analytics disclosure before going live; (3) If GA4 (cookie-based) is chosen, confirm a consent mechanism is added for GDPR-relevant visitors given the "Worldwide" service area.

**Acceptance Criteria:** (1) Analytics tag present on all 10 pages; (2) At least one of the 5 PRD-stated KPIs (docs/PRD.md §2) is measurable in a dashboard within 24 hours of rollout; (3) `privacy.html` accurately names the analytics provider used.

---

### FR-008: Fix Broken Logo Asset Reference in Structured Data

**Description:** Either add the missing `images/logo.png` file referenced in the homepage's Organization JSON-LD schema, or update the `logo` field to point to an asset that actually exists in the repository.

**Why It Matters:** Google's structured-data validators (Rich Results Test) specifically check that an Organization's `logo` field resolves to a real, appropriately-sized image; a 404 on this field can cause the Organization rich-result eligibility to fail entirely, undermining the SEO goal explicitly stated in `docs/PRD.md` §4.3 ("Organization and Service schema MUST be valid and complete").

**Verification Evidence:** `index.html` line 24 contains `"logo": "https://intelastart.com/images/logo.png"`; a full-repo Glob for every common image extension (`*.jpg`, `*.jpeg`, `*.png`, `*.svg`, `*.webp`, `*.ico`) returned zero files anywhere in the repository — there is no `images/` directory at all.

**Evidence IDs:** E-013

**Priority:** P2

**Category:** SEO / Structured Data Correctness

**ROI Score:** 4 — Direct, if modest, SEO benefit (differentiation/discoverability angle); low effort for the fix (just needs a logo asset created/uploaded).

**Risk Score:** 1 — Trivial fix, zero blast radius, no dependencies.

**Dependencies:** Requires an actual logo image asset to be designed/exported if one doesn't exist outside the repo already.

**Competitive Reference:** Google's own Rich Results structured-data guidelines require a resolvable `logo` URL for Organization markup to be eligible for enhanced search features.

**Security/Privacy Impact:** None.

**Rollout Readiness:** High — purely an asset-upload + one-line HTML fix once the image exists.

**Validation Gates:** (1) Confirm the image URL returns HTTP 200 once deployed; (2) Run the page through Google's Rich Results Test and confirm no "logo" field errors; (3) Confirm the same fix doesn't need to be replicated elsewhere (checked — only `index.html` references it).

**Acceptance Criteria:** (1) `https://intelastart.com/images/logo.png` resolves with a 200 status; (2) Google Rich Results Test shows zero errors on the Organization schema; (3) The logo displays correctly in a manual Google Search Console preview if available.

---

### FR-009: Add Spam Protection to the (Post-FR-001) Contact and Newsletter Forms

**Description:** Once FR-001 wires the form to a real backend, add a honeypot field or reCAPTCHA/hCaptcha as `docs/SECURITY.md` and `docs/TEST_STRATEGY.md` both already prescribe ("protect against spam with reCAPTCHA or honeypot fields"; "Check spam protection (honeypot or reCAPTCHA) is functioning").

**Why It Matters:** Without spam protection, a newly-functional public form (post-FR-001) is immediately exposed to bot-submitted spam, which would pollute the lead pipeline the PRD is trying to build and waste the solo maintainer's triage time.

**Verification Evidence:** Grep for `recaptcha|honeypot` across all HTML files returned zero matches — confirming this genuinely doesn't exist yet, consistent with the fact that the form itself isn't wired to anything yet (FR-001). `docs/TEST_STRATEGY.md` §3 explicitly lists this as a required pre-push check today, even though there's currently nothing to check.

**Evidence IDs:** E-004, E-006 (same negative-finding grep)

**Priority:** P2 (sequenced strictly after FR-001; not urgent standalone since the form doesn't submit anywhere yet)

**Category:** Conversion / Spam Hygiene

**ROI Score:** 3 — Protects the value created by FR-001 rather than creating new value on its own; opex savings (10% weight) from reduced manual spam triage.

**Risk Score:** 2 — Low complexity (honeypot is a zero-dependency HTML/CSS trick; reCAPTCHA is a well-documented script include), small vendor dependency if reCAPTCHA is chosen over a honeypot-only approach.

**Dependencies:** Hard dependency on FR-001 shipping first — there is no form to protect until the backend exists.

**Competitive Reference:** Honeypot fields and Google reCAPTCHA v3 are the two most common patterns for exactly this static-site + third-party-form-service combination, and are named explicitly in this repo's own `docs/SECURITY.md`.

**Security/Privacy Impact:** reCAPTCHA (if chosen over honeypot) introduces a Google-operated third-party script and its own privacy-disclosure obligation; a honeypot field has no privacy impact at all and is the lower-friction choice.

**Rollout Readiness:** High once FR-001 is complete — this is a small additive change to the same form component.

**Validation Gates:** (1) Confirm a scripted/automated form submission (simulating a bot) is successfully blocked or flagged; (2) Confirm a real human submission is unaffected by the new field; (3) If reCAPTCHA is chosen, confirm it's added to the CSP allowlist from FR-002.

**Acceptance Criteria:** (1) Honeypot field or reCAPTCHA widget is present in the contact form HTML; (2) A test bot-style submission (empty honeypot filled, or failing reCAPTCHA) is rejected before reaching the inbox/CRM; (3) A normal human submission still succeeds end-to-end.

---

## Prioritized Implementation Roadmap

**Wave 1 (P0 — ship immediately):**
- FR-001: Wire the contact form to a real backend. This is the single highest-leverage fix and unblocks the site's stated core business function.

**Wave 2 (P1 — ship within the next iteration, can parallelize):**
- FR-007: Add web analytics (needed to measure everything else, including FR-001's success).
- FR-002: Implement documented CSP/security headers (sequence analytics' domain into the allowlist).
- FR-003: Add case-study evidence (content workstream, can run in parallel with the technical FRs).
- FR-004: Automate the documented Lighthouse/accessibility/link-check test suite.

**Wave 3 (P2 — follow-on hardening and cleanup):**
- FR-009: Add spam protection (strictly after FR-001).
- FR-006: Add front-end error monitoring (pairs naturally with FR-002's CSP work).
- FR-008: Fix the broken logo asset reference (quick, isolated win — could actually be done immediately in parallel with Wave 1 given its triviality).
- FR-005: Fix the Dependabot ecosystem misconfiguration (lowest urgency, purely hygiene).

**Sequencing rationale:** FR-001 stands alone at the top because every other conversion-related improvement (FR-003, FR-007, FR-009) is measuring or protecting a pipeline that currently doesn't exist. FR-002 and FR-007 are grouped because both need to agree on the same third-party-script allowlist. FR-008 and FR-005 are cheap, isolated, no-dependency fixes that could realistically be done same-day regardless of wave.

---

## Top 5 Highest-ROI Features

| FR ID | Description | ROI | Risk | Priority |
|---|---|---|---|---|
| FR-001 | Wire contact form to a real lead-delivery backend | 10 | 3 | P0 |
| FR-007 | Add web analytics to measure stated PRD KPIs | 6 | 2 | P1 |
| FR-003 | Add case study evidence to substantiate quantified claims | 6 | 4 | P1 |
| FR-002 | Implement documented CSP and security headers | 5 | 3 | P1 |
| FR-004 | Automate documented Lighthouse/accessibility/link-check suite in CI | 5 | 3 | P1 |

---

## Validation Plan

For each FR, validation follows a consistent three-step approach appropriate to a static-site context with no backend of its own:

1. **Pre-deploy verification** — For code/config changes (FR-001, FR-002, FR-005, FR-006, FR-007, FR-008, FR-009), test in a local server (`python -m http.server` or `live-server`, both already configured in `.vscode/tasks.json`) or a staging branch/preview deploy before merging to `main`, since a push to `main` triggers immediate live production deployment via GitHub Pages (per `docs/DEPLOYMENT.md`).
2. **Post-deploy confirmation** — Use the existing `docs/DEPLOYMENT.md` post-deploy checklist (already documents "Contact form sends correctly," "Analytics recording sessions") as the literal validation script; extend it to explicitly check each new FR's specific acceptance criteria (e.g., after FR-002, run a header-scan tool; after FR-008, run Google's Rich Results Test).
3. **Ongoing monitoring** — Once FR-006 (error monitoring) and FR-007 (analytics) ship, use them to validate that subsequent FRs (and any future content changes) don't silently regress — e.g., a future edit accidentally breaking the form again (FR-001 regression) should now surface as a spike in JS errors or a drop in form-submission analytics events, rather than going unnoticed for three months as it apparently did per the git history and prior audit dates.

Given the maintainer is a solo operator (`docs/PRD.md` §6), the validation plan intentionally avoids requiring dedicated QA headcount or heavyweight tooling — every gate above uses either free third-party tools (Google Rich Results Test, securityheaders.com) or automation that, once built (FR-004), runs unattended in CI.

---

## Executive Summary

Intelastart.com is a solo-operator-maintained, static HTML B2B consulting marketing site (no backend, no build system) whose stated core business function — lead capture via contact form — is currently non-functional: the form only simulates a submission client-side and discards the data, a gap the site's own prior internal audit (dated 2026-03-29) already identified roughly three months before this review. Beyond that headline finding, the site publishes specific, unsubstantiated quantified business claims with no case-study evidence, has zero web analytics despite the PRD naming GA4 as the measurement method for every stated KPI, has documented-but-unimplemented security headers (CSP), and ships a broken image reference in its own SEO structured data. CI/CD exists only for markdown linting and internal AI-agent-governance schema validation — none of it touches the actual website. Nine specific, evidence-backed feature requests are documented above (not padded to 30, consistent with this being a small static site); fixing FR-001 alone would restore the site's fundamental ability to generate the leads it was built to capture, and the remaining eight close well-documented, self-identified gaps between what the repo's own internal documentation says should exist and what is actually implemented in code.
