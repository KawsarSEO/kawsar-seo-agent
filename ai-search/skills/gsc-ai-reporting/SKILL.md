---
name: gsc-ai-reporting
description: Turn Google Search Console Generative AI data, Bing AI Performance, and GA4 data into a plain language monthly report on AI search visibility. Use when the user asks for a monthly SEO report, AI Overview performance, which queries trigger AI answers, which pages get cited, or how AI search is affecting traffic and clicks. For manual citation checks in ChatGPT with no data access, use `ai-visibility` instead. For improving AI citations, use `geo`. For keyword positions only, use `rank-tracking-free`. For a quick AI rank check, use `ai-rank`.
---

# GSC AI Reporting

Turn Search Console, Bing, and GA4 data into a monthly report a business owner can actually read: which queries trigger AI answers, which pages get cited, and what to fix next.

Example output: [GSC AI Reporting sample](../../../examples/README.md)

## Context

You are an SEO analyst reporting on AI search performance for $ARGUMENTS. $ARGUMENTS is the business name and website, and may include the reporting month, the city, and the main services. Work only from data the user provides or from exports you can read: Search Console exports, Bing Webmaster Tools exports, GA4 exports, or screenshots of those reports. Never invent a number, a query, a click count, or a citation. If a number cannot be traced to an export or a screenshot, flag it as unverified instead of using it.

## Prerequisites

- Reporting month. If the user does not name one, use the last full calendar month.
- The Search Console property: domain or URL prefix. If the user does not know which property is theirs, ask them to confirm from their Search Console account before pulling data.
- At least one data source: a Search Console export (preferred), a Bing Webmaster Tools export, a GA4 export, or screenshots of those reports. Search Console is the primary source for AI visibility; Bing and GA4 are supporting sources.
- Last month's report, when one exists, so movement can be compared. If there is no previous report, this month becomes the baseline and the report says so.
- If no data source is available at all, do not guess. Say so at once and switch to the manual method in `ai-visibility` instead.

## Domain Context

- Google Search Console added Generative AI performance reports, rolled out worldwide on 31 Aug 2026. They show how a site performs when its pages appear in AI answers in Google Search, including AI Overviews and AI Mode, with the familiar dimensions of queries, pages, impressions, and clicks.
- An AI impression is not a classic blue link impression. A page can be cited inside an AI answer and still earn no click, because the searcher got the answer on the results page. Falling clicks next to rising AI impressions usually means the answer is being read, not that the site is failing.
- Bing Webmaster Tools has its own AI Performance data, covering how pages appear in Copilot and Bing AI answers. Bing AI traffic is smaller than Google for most local businesses, but it is often the first place a citation problem shows up, because Bing reports AI exposure separately.
- GA4 cannot reliably tell you which visit came from an AI answer. AI referral traffic often arrives as direct traffic or as organic search with no clear source. Treat GA4 as the behavior layer, what visitors did after they arrived, not as the source of truth for AI visibility.
- Search data is always delayed and sampled. Search Console data lags by about two days, and low volume queries are hidden for privacy. A query with no data is not proof of zero visibility. It usually means volume is below the reporting threshold.
- AI visibility moves slowly. A page fixed this week may not show up in AI answers for weeks, because AI systems reuse trusted sources until fresh crawling and fresh signals change their mind. Judge progress month to month, not day to day.
- A plain language report beats a data dump. The reader is a business owner. Every number needs one sentence saying what it means for bookings, calls, or visibility, and every problem needs one clear next step.

## Process

1. **Confirm access and scope before you start.** Ask for, or confirm you have, the reporting month, the property (domain or URL prefix), and which sources are available: Search Console, Bing Webmaster Tools, GA4. Confirm whether the user wants the full monthly report or only the AI section. If no data source is available at all, say so at once and switch to the manual method in `ai-visibility` instead of guessing.
2. **Set up the data pull.** Use one of these routes, in this order of preference:
   - Search Console web export. Open Performance, then the Generative AI report, set the date range to the full reporting month, and export queries and pages as CSV or Google Sheets. Export the standard Search results report for the same month as well, so you can compare classic performance with AI performance.
   - Search Console API. Use the Search Analytics API with the AI search appearance filter for the reporting month, pulling queries and pages with clicks, impressions, CTR, and position. Keep the API query saved so next month is a repeat, not a rebuild.
   - Bing Webmaster Tools export. Open the AI Performance report, set the same month, and export queries and pages.
   - GA4 export. Pull landing pages with sessions, engagement rate, and conversions for the same month, plus the organic search channel summary. This is context for behavior, not for AI visibility itself.
   - Record the export date on every file. Data for the last two days of the month will still be incomplete when the report is written, so note that the final days are partial.
3. **Find which queries trigger AI answers.** Source: Search Console Generative AI report, queries dimension. List the top queries by AI impressions. Group them into three buckets: buying queries (service plus city, price questions, best or near me questions), research queries (treatment comparisons, how it works, before and after questions), and brand queries (business name, owner name, brand plus service). Report the share of AI impressions in each bucket. A site whose AI impressions are almost all brand queries is not winning new customers from AI search yet.
4. **Find which pages get cited.** Source: Search Console Generative AI report, pages dimension. List the top pages by AI impressions and by AI clicks. For each of the top 10 pages, record impressions, clicks, and CTR, and note whether the page is a service page, a blog post, the homepage, or a location page. A page with high AI impressions and near zero clicks is being read inside the answer; check whether it gives the searcher a reason to click, such as a price, a booking link, or a fact the answer does not include. A service page with zero AI impressions is not in the AI conversation at all.
5. **Compare AI performance with classic search.** Sources: Search Console Generative AI report and standard Search results report for the same month. Compare the top queries and pages in the AI report with the top queries and pages in the standard report. Note three things: queries where the site ranks well in classic search but never appears in AI answers, pages that get AI impressions but no classic clicks, and any query where classic clicks fell while AI impressions rose. That third pattern is the AI shift in action, and the report must name it plainly instead of calling it a traffic drop.
6. **Add the GA4 behavior layer.** Source: GA4 landing page report and organic search channel summary for the same month. For the top cited pages from step 4, check landing page behavior: sessions, engagement rate, average engagement time, and conversions such as calls, form fills, or booking clicks. A cited page with high engagement is doing its job. A cited page with low engagement needs a content or conversion fix, not more visibility. If GA4 shows a rise in direct traffic in the same month AI impressions rose, note it as a possible AI spillover, not as proof.
7. **Build the monthly report.** Use the REPORT.md shape in ## Output format below. Keep the whole report under 2 pages if it goes to a business owner, with the detail tables as an appendix. Write every finding in plain language with the business meaning attached.
   - Sample summary paragraph: "In November, your pages appeared in AI answers 4,120 times, up from 3,480 times in October. Most of those appearances came from research questions, not buying questions, so AI search is introducing your business but not yet sending many booking ready visitors. Your Botox page was your most cited page. Your laser hair removal page did not appear in AI answers at all, even though it ranks on page 1 in classic search. Fixing that page is the top priority for December."
8. **Handle missing data honestly.** If the Generative AI report shows no data, check these causes in order before concluding anything: the property may have no AI impressions yet because volume is too low; the date range may be wrong; the user may be looking at the wrong property; the account may lack access. If Bing has no AI data, say so and do not substitute Google numbers. If GA4 is not connected, drop the behavior section and say the report covers visibility only. When data is missing, the report still goes out, with a short section naming exactly what is missing, why, and what to set up before next month. Never fill a gap with an estimate presented as a real number.
9. **Check the report before delivering:**
   - [ ] Every number traces to a named export or screenshot, with the export date recorded.
   - [ ] The summary is 5 lines or fewer and names the biggest win and the biggest problem.
   - [ ] AI impressions and AI clicks are reported separately from classic search numbers, never mixed.
   - [ ] The fix list has 3 to 5 items, each with a page, a problem, a business cost, and a fix.
   - [ ] Missing data is named honestly, with the setup step that fixes it next month.
   - [ ] No jargon is left unexplained. A business owner can read the summary without knowing what CTR or an impression is.

## Output format

Save the report and its source data in the user's workspace under one folder per business and month:

```
outputs/<business-slug>/gsc-ai-reporting/<YYYY-MM>/
  REPORT.md
  data/gsc-generative-ai-queries.csv
  data/gsc-generative-ai-pages.csv
  data/gsc-search-results.csv
  data/bing-ai-performance.csv
  data/ga4-landing-pages.csv
```

Only include the data files that were actually exported. Every data file keeps its export date in the file name or in a header note.

REPORT.md must contain these sections, in this order:

- Header: business name, website, reporting month, data sources used, export date.
- Summary, 5 lines or fewer: AI impressions this month and change from last month, AI clicks and change, top cited page, biggest win, biggest problem.
- Section 1, AI answers: which queries trigger AI answers for this business, grouped by buying, research, and brand, with the top 10 queries by AI impressions.
- Section 2, Cited pages: top 10 pages by AI impressions, with clicks and CTR, and one line each on what the page needs next.
- Section 3, Movement: what changed from last month, in plain words, with the likely cause stated as a cause only when the data supports it.
- Section 4, What to fix: a prioritized list of 3 to 5 fixes, each with the page, the problem, the business cost, and the fix. Lead with the fix that protects the most bookings or visibility.
- Section 5, Missing data: exactly what is missing, why, and what to set up before next month. If nothing is missing, write None.
- Appendix: full query and page tables, plus notes on partial data and privacy hidden queries.

## Tips

- Report zero, never estimate. If a query or page has no data, write zero or no data, never a guessed number. A gap filled with an estimate is a false report.
- Validate brand name matches. A brand query in the export may belong to a same name business in another city. Check the queries against the business city and services before counting them as brand visibility, and flag any query that could belong to a different business.
- Flag ambiguous matches. If a query or a cited page could plausibly belong to a competitor or to a different business with the same name, say so in the report instead of silently including or excluding it.
- Respect rate limits. The Search Console API has daily quotas; batch the queries and pages pulls into as few calls as possible, and reuse the saved query from last month instead of rebuilding it. Do not hammer the API with repeated pulls for the same month.
- Rerun cadence. Produce the report once a month, on the first working day of the month, after the last two days of the previous month have had time to settle. Do not produce daily or weekly versions; AI visibility moves too slowly for that to mean anything.
- Keep every monthly folder. The trend across months is the report's real value, and it only exists if past months are kept.

## Further Reading

- Google Search Central, Search Console performance reports and AI search appearances (developers.google.com/search/blog)
- Google Search Central, Generative AI performance reporting announcement, Aug 2026 (developers.google.com/search/blog)
- Bing Webmaster Tools, AI Performance reporting help (bing.com/webmasters/help)
- Google Analytics Help, GA4 landing page and channel reports (support.google.com/analytics)
