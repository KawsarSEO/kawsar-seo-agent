# Agents

This folder holds the sub agents for The SEO Skills Pack. Each file is one Claude Code sub agent: YAML frontmatter (name, description, tools) plus a body that describes the role and workflow.

There are two groups. Role agents own an area of work. Specialist auditors run in parallel on one audit and return findings for synthesis.

## Role agents

Each role agent owns a set of skills and the work that goes with them. Call the role agent when the user asks for that kind of work.

| Agent | Owns | Skills |
| --- | --- | --- |
| `seo-agent` | Core SEO: audits, keywords, competitors, rank tracking | website-audit, structured-data, keyword-research, competitor-analysis, rank-tracking-free |
| `local-seo-agent` | Local visibility: GBP, reviews, local pack, citations | gbp-optimization, review-management |
| `ai-visibility-agent` | AI search presence: AEO, GEO, AI rank, AI citations, GSC AI reporting | aeo, geo, ai-rank, ai-visibility, gsc-ai-reporting |
| `content-agent` | Content: SEO pages, human content, social content | seo-content-writing, human-content, social-media-content |

Role agents hand work to each other when a task crosses areas. For example, `seo-agent` hands GBP and review work to `local-seo-agent`, AI presence work to `ai-visibility-agent`, and new page copy to `content-agent`.

## Specialist auditors

Five focused auditors run a full website audit in parallel. Each checks one area only and returns findings in a standard format for synthesis.

| Auditor | Checks |
| --- | --- |
| `technical-audit` | Crawlability, indexation, speed, mobile, Core Web Vitals, HTTPS, redirects |
| `content-audit` | Thin or duplicate content, E-E-A-T signals, on page optimization, internal linking |
| `schema-audit` | Structured data presence, validity, coverage of key types (LocalBusiness, FAQ, Review, Service) |
| `local-audit` | GBP completeness, NAP consistency, reviews, local landing pages |
| `ai-search-audit` | Citability, AI crawler access (robots.txt), FAQ and passage structure, brand mentions in AI answers |

Every specialist returns each finding in the same format:

- Finding: one sentence, specific, saying what is wrong.
- Evidence: the page URL, plus where on the page it appears.
- Business harm: what it costs, in the client's own terms.
- Severity: Critical, High, Medium, or Low.
- Fix: one concrete action that resolves it.

Specialists return findings only, not a full report. The orchestrator (usually `seo-agent`, or the `website-audit` skill) synthesizes them into one scored report.

## Orchestration

How a full audit runs:

1. Detect the business type first. Identify what kind of business this is, the services that make money, the city or cities served, and who the customer is. The business type decides which pages matter most, which keywords matter, and which competitors count.
2. Spawn the five specialists in parallel: `technical-audit`, `content-audit`, `schema-audit`, `local-audit`, and `ai-search-audit`. Each reads the live site and returns findings in the standard format above.
3. Synthesize into one scored report. Merge the five sets of findings, remove duplicates (keep the finding under the specialist that owns it, and note the overlap), rank everything by business harm with the most critical and most costly issue first, score it with `seo-audit/references/scoring-framework.md`, and format it with `seo-audit/references/report-template.md`.

## House rules

These apply to every agent in this folder:

1. Verify before claiming. Only report issues actually observed on the live site, with page evidence. Never invent a problem, a number, or a contact detail.
2. Frame every issue with business harm. Lost bookings, lost visibility, lost trust.
3. Lead with the most critical issue. The most costly problem goes first.
4. Plain language. The client is a business owner, not an SEO.
