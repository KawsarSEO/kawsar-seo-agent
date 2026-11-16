---
name: ai-visibility
description: Measure whether a brand and domain get cited in AI answers across ChatGPT and AI search, compare against competitors, and produce a prioritized fix list. Use when the user asks if AI mentions the business, how visible a brand is in ChatGPT, whether AI answers recommend the business, or how it compares with competitors in AI answers. For a quick AI rank check, use `ai-rank`. For the data led monthly report from Search Console and Bing, use `gsc-ai-reporting`. For improving citations, use `geo`. For classic keyword positions, use `rank-tracking-free`.
---

# AI Visibility

Find out whether AI answers mention the business at all, how it compares with competitors, and what to fix first when it is invisible. No paid tool required.

Example output: [AI Visibility sample report](../../../examples/ai-visibility-sample/REPORT.md)

## Context

You are an SEO analyst measuring AI visibility for $ARGUMENTS. $ARGUMENTS is the business name and website, and may include the city, the main services, and up to 3 competitors to compare against. Work only from checks you actually run or results the user provides: real prompts, real AI answers, real cited sources. Never invent a citation, a mention, or a competitor result. Record the date, the tool, and the exact prompt for every check, because AI answers change from day to day.

## Prerequisites

- Business name, website, city, and main services. The city matters, because AI answers are local and a check without a city in the prompt means very little.
- Up to 3 competitors to compare against. If the user does not name any, pick the top 3 competitors from a Google search for the main service plus the city, verify each one is a real competing business, and confirm the choice with the user before checking starts.
- Access to at least one AI answer source: ChatGPT first, then at least one more the user cares about, such as Google AI Overviews or Perplexity. If only one source is available, use it and say so in the report; the score is then a single source score, not a cross tool score.
- A logged out browser session or a fresh chat with no prior conversation about the business, so earlier chats do not bias the answers.

## Domain Context

- AI visibility means being cited, named, or recommended inside an AI answer, not ranking in a classic list of links. A business can rank on page 1 of Google and still be invisible in ChatGPT, because AI answers draw on a smaller set of trusted sources.
- AI answers vary. The same prompt can give different answers in different sessions, locations, and accounts. One check proves nothing. A pattern across a set of prompts, checked on more than one day, is the real signal.
- Brand prompts and buying prompts test different things. A brand prompt ("What is Bright Glow Med Spa?") tests whether the AI knows the business exists. A buying prompt ("Best med spa in Fort Worth for Botox") tests whether the AI recommends it to a new customer. A business can pass the first and fail the second.
- Citations follow trust signals: a clear and consistent business entity, verifiable facts with numbers, real reviews, independent mentions, fresh dated content, and pages that answer questions directly. A business missing most of these is usually missing from AI answers too.
- Competitor comparison is the point. Being mentioned once means little until you know whether competitors are mentioned ten times. Always measure the business next to the same competitors, with the same prompts, on the same day.
- Manual checks are honest and repeatable when they are structured. A fixed prompt set, a simple scoring sheet, and a steady monthly rhythm beat an expensive tool used once.

## Process

1. **Define the prompt set before checking anything.** Build 12 to 15 prompts in three groups. Write them the way a real customer would ask, not the way an SEO would.
   - Brand prompts (3 to 4): the business name alone, the business name plus city, the business name plus a service.
   - Buying prompts (5 to 6): best service in city, service near me, service cost in city, best provider for a specific concern.
   - Research prompts (4 to 5): treatment A versus treatment B, how a treatment works, what to ask before booking, aftercare questions.
   - For each prompt, record the exact wording, the group, and the service it tests. Freeze the set for the month so results stay comparable.
2. **Run the manual checks the clean way.** Sources: ChatGPT first, then at least one more AI answer source the user cares about, such as Google AI Overviews or Perplexity. Use a logged out browser session or a fresh chat with no prior conversation about the business. Ask each prompt exactly as written, one per fresh chat where the tool allows it, and record the full answer or a screenshot. Run the full set on two different days in the same week and keep both rounds; a mention that appears in only one round is a weak signal.
3. **Score every answer the same way.** For each prompt and each tool, record: was the business named, was the business website cited or linked, was the business recommended, which competitors were named, and how many sources were cited in total. Use a simple 0 to 3 score per prompt: 0 means not mentioned, 1 means named only, 2 means named with a fact or a link, 3 means recommended as a top choice. Add the scores into a total per tool and a total overall. A business scoring near zero across buying prompts is invisible where it matters most.
4. **Compare against competitors on the same prompts.** Sources: the same AI answer tools, the same prompt set, the same day. Run the identical prompt set for up to 3 competitors and score them the same way. Build a small comparison table with one row per prompt group and one column per business, showing total scores and the number of prompts where each business was recommended. Name the competitor that AI answers favor most, and note which of its pages or sources get cited. That citation pattern is the clearest clue about what the business is missing.
   - Sample comparison summary: "Across 14 prompts in ChatGPT, Bright Glow scored 9 out of 42 and was recommended in 1 prompt. Glow Studio scored 24 and was recommended in 6 prompts, mostly on buying prompts. Radiant Skin scored 18. The gap is widest on price and best of prompts, where Glow Studio is cited from its service pages and its Google reviews, and Bright Glow is not mentioned at all."
5. **Diagnose why the business is missing.** Sources: the live business website, the Google Business Profile, and the directories and listings the AI answers cite for competitors. When the score is low, check these causes in order and record what you find for each: the business entity is inconsistent across the website, Google Business Profile, and directories; the website has no quotable facts with real numbers; the service pages do not answer the exact questions in the prompt set; the business has few or no visible reviews; there are no independent mentions, press, or directory listings for AI systems to confirm; content is undated or stale. Every cause you name must be tied to a page or source you actually checked.
6. **Produce the prioritized fix list.** Turn the diagnosis into 5 to 8 fixes, ranked by likely impact on AI visibility, most important first. For each fix, give the problem in one sentence, the evidence (which prompts failed and what competitors do instead), the page or source to fix, and the fix itself. Lead with entity and fact fixes before content fixes, because AI systems will not cite a business they cannot identify or verify. Save the full output as REPORT.md using the shape in ## Output format below.
7. **Handle total invisibility with a clear first month plan.** If the business scores zero across the whole prompt set, say so plainly and do not soften it. The first month plan is: fix the entity everywhere, publish quotable facts with real numbers on the homepage, answer the top 5 buying questions on the service pages, get real reviews visible on the site and on Google, and earn at least one independent mention. Recheck the same prompt set after 30 days. Set the expectation honestly: a business starting from zero should expect small movement in month one, not a top recommendation.
8. **Repeat monthly and report the trend.** Rerun the same prompt set once a month, on the same tools, and record the total score, the score per prompt group, and the competitor totals. The monthly update is short: score this month and change from last month, prompts newly won, prompts newly lost, and the top 3 fixes for next month. Keep every monthly sheet so the trend is visible over time. Change the prompt set only when the business adds a service or a competitor closes; changing prompts monthly makes trends unreadable.
9. **Check the audit before delivering:**
   - [ ] The prompt set has 12 to 15 real customer worded prompts in three groups, frozen for the month.
   - [ ] Every check records the date, the tool, the exact prompt, and the score.
   - [ ] The full set ran on two different days, and both rounds are recorded.
   - [ ] Competitors were scored on the same prompts, on the same day, with the same method.
   - [ ] The fix list has 5 to 8 items, each with evidence, a page or source, and a fix.
   - [ ] Total invisibility, when found, is stated plainly with a first month plan attached.

## Output format

Save the prompt score sheet and the report in the user's workspace under one folder per business:

```
outputs/<business-slug>/ai-visibility/
  prompt-score-sheet.csv (or .xlsx, one row per prompt per tool per round)
  <YYYY-MM>/REPORT.md
```

The prompt score sheet lives at the top of the folder and gains a new set of rows each month. Each month gets its own subfolder with that month's REPORT.md.

REPORT.md must contain these sections, in this order:

- Header: business name, website, city, reporting month, AI tools checked, check dates (both rounds).
- Summary: total score out of the maximum, score per prompt group, prompts where the business was recommended, biggest gap versus the leading competitor.
- Section 1, Prompt results: the full prompt set grouped by brand, buying, and research, with the score per prompt per tool and the round it was recorded in.
- Section 2, Competitor comparison: one row per prompt group and one column per business, showing total scores and the number of prompts where each business was recommended, plus the pages or sources the leading competitor is cited from.
- Section 3, Diagnosis: the causes checked in step 5, each with what was found and the page or source it was found on.
- Section 4, Fix list: 5 to 8 fixes ranked by likely impact, each with the problem, the evidence, the page or source to fix, and the fix itself.
- Section 5, First month plan: only when the business scores zero across the whole prompt set. The five first month actions from step 7, with the honest expectation attached. If the score is above zero, write Not applicable, score above zero.
- Section 6, Trend: score this month and change from last month, prompts newly won, prompts newly lost. In the first month, write Baseline month, no prior score.

## Tips

- Report zero, never estimate. If the business is not mentioned in an answer, score it 0. Never round a weak mention up, and never guess what the AI would have said on a different day. A zero is a finding, not a failure of the check.
- Validate brand name matches. An AI answer may name a same name business in another city. Before counting a mention, confirm the city, the service, or the website matches the client's business. A mention of the wrong business is a zero for the client, with a note.
- Flag ambiguous matches. If an answer names a business that could be the client or a same name business elsewhere, and the answer gives no city, link, or detail to tell them apart, record it as ambiguous in the score sheet and in the report instead of scoring it either way.
- Respect rate limits. AI tools throttle rapid prompting; run the prompt set at a steady pace, one prompt per fresh chat where the tool allows it, and spread the two rounds across two different days. Do not script bulk prompt runs against a chat interface.
- Rerun cadence. Rerun the same prompt set once a month, on the same tools. Change the prompt set only when the business adds a service or a competitor closes, so trends stay readable.
- Keep every monthly sheet. The trend across months is the audit's real value, and it only exists if past months are kept.

## Further Reading

- GEO: Generative Engine Optimization, Aggarwal, Murahari, Rajpurohit, et al. (arXiv, 2023)
- Google Search Central, guidance on AI Overviews and helpful content (developers.google.com/search/blog)
- Search Engine Land, AI search visibility coverage (searchengineland.com)
