# The SEO Skills Pack

SEO, AEO, GEO, AI Rank, content, outreach, and ads skills for local service businesses, written so an AI agent can actually use them.

**20 skills and 6 commands across 6 plugins**, for [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

**Not sure which skill you need? Start with the [skill index](./INDEX.md)**, every skill in this repo arranged by the situation you are in, plus the pairs most often mistaken for each other.

## Getting started (no coding needed)

These skills run inside an AI coding assistant. The easiest place to use them is Claude Code, and it takes three steps. No terminal required.

**1. Get Claude Code.** It is Anthropic's AI coding assistant and requires a paid Claude plan (claude.com). Download it, sign in, and open it. You only do this once.

**2. Add the suite.** In Claude Code, type this and press enter:

```
/plugin marketplace add KawsarSEO/kawsar-seo-agent
```

This just tells Claude where the skills live. Nothing installs yet.

**3. Pick what you want.** Type `/plugin` and press enter, then open the **Discover** tab. You will see all the collections. Move with the arrow keys, press space to tick the ones you want, and enter to install. That is it.

### I only want one specific plugin

Install one by name:

```
/plugin install outreach@kawsar-seo-agent
```

### Other platforms

Claude Code is not the only way to use these skills.

- **Codex.** This repo ships a Codex plugin manifest at `.codex-plugin/plugin.json`. Install the plugin from this repo in Codex and the skills are available there.
- **Cursor.** This repo ships a Cursor plugin manifest at `.cursor-plugin/plugin.json`. Install the plugin from this repo in Cursor.
- **Any agent with npx skills add.** Run this once:

```
npx skills add KawsarSEO/kawsar-seo-agent
```

This works with Cursor and other agents that support the skills add command.

---

## The six plugins

| Plugin | Skills | Commands | What it covers |
| --- | --- | --- | --- |
| seo-audit | 4 | 1 | Full website audits, structured data, free rank tracking, and 90 day SEO plans: find the issues costing a business bookings, mark up content so search engines understand it, track ranks without a paid tool, and turn findings into a phased plan. |
| local-seo | 2 | 1 | Google Business Profile and reviews: rank in the map pack, win reviews, and keep business details consistent everywhere. |
| ai-search | 5 | 1 | Answer engine and generative engine optimization, AI Rank, AI visibility, and GSC reporting: get featured in snippets, cited by AI search engines, and measured in one report. |
| content | 3 | 1 | Content that ranks and reads human: SEO pages, human sounding rewrites, and social media posts for local businesses. |
| outreach | 4 | 1 | Win local clients: cold outreach emails from website audits, competitor analysis, keyword research, and local link building. |
| ads | 2 | 1 | Paid ads for local service businesses: Google Ads and Facebook and Instagram ads that turn clicks into bookings. |

## New in version 1.1.0

Five new skills:

| Skill | Plugin | What it does |
| --- | --- | --- |
| gsc-ai-reporting | ai-search | GSC and AI search reporting: queries, clicks, and AI citations in one report |
| rank-tracking-free | seo-audit | Free rank tracking: check positions without a paid tool and record them over time |
| link-building | outreach | Local link building: earn links from local sites, directories, and partners |
| ai-visibility | ai-search | AI answer citations: track where AI engines cite the business and grow that coverage |
| seo-plan | seo-audit | Compose audit, keyword research, competitor analysis, and AI visibility outputs into a 90 day SEO plan with phases, owners, success metrics, and a critical path |

## Agents

The `agents/` folder holds 9 agents that use these skills to do longer jobs end to end.

Role agents: `seo-agent`, `local-seo-agent`, `ai-visibility-agent`, `content-agent`. Each one owns a whole area of work: full SEO, local search, AI search visibility, and content.

Specialist audit agents: `technical-audit`, `content-audit`, `schema-audit`, `local-audit`, `ai-search-audit`. Each one audits one part of a business: technical issues, content, structured data, local presence, and AI search visibility.

## House rules

These rules come from real client work and apply to everything the agent produces:

1. **Verify before claiming.** Only report issues actually observed on the live site, with page evidence. Never invent a problem, a number, or a contact detail.
2. **Frame every issue with business harm.** The client should read it and think "yes, I have these mistakes, I need to fix this." Lost bookings, lost visibility, lost trust.
3. **Lead with the most critical issue.** The most costly problem goes first.
4. **Plain language.** The client is a business owner, not an SEO. Say "your homepage has no way for a visitor to book" instead of "missing conversion element."

## About

Built by Mohammad Kawsar. Digital marketing services: SEO, Facebook Ads, Google Ads, and AI Automation.
