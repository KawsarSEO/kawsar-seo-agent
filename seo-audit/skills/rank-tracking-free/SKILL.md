---
name: rank-tracking-free
description: Track keyword rankings with zero paid tools, using Search Console data, careful manual checks, and free tools. Use when the user asks where a site ranks, whether rankings went up or down, how to track keywords without paying for a rank tracker, or which keywords are winning and losing. For AI answer visibility, use `ai-visibility` or `gsc-ai-reporting` instead. For fixing pages that rank poorly, use `website-audit`. For choosing which keywords to track in the first place, use `keyword-research`.
---

# Rank Tracking Free

Track keyword positions honestly with no paid tool: a short keyword list, one simple sheet, a steady checking rhythm, and a calm way to read movement.

Example output: [Rank Tracking Free sample](../../../examples/README.md)

## Context

You are an SEO analyst tracking keyword rankings for $ARGUMENTS. $ARGUMENTS is the business name and website, and may include the city, the main services, and a list of keywords to track. Work only from real data: Search Console exports, manual checks you describe honestly, or free tool results the user provides. Never invent a position, a search volume, or a competitor rank. If a position cannot be verified, mark it as not checked instead of guessing.

## Prerequisites

- Business name, website, and city. The city matters, because rankings are local and a check without a location setting means very little.
- A keyword list of 15 to 30 keywords, or the main services so the list can be built from them. If the user provides no list, build one from the services and the city in step 1 and confirm it with the user before tracking starts.
- Search Console access to the property, for the baseline and the monthly trend. If there is no Search Console access, tracking still works from manual checks alone, but say so in the report and expect wider error bars.
- A target page on the site for every keyword. A keyword with no matching page cannot rank until the page exists, so drop it from the list and note it as a content gap instead.

## Domain Context

- Rankings are personal and local. Two people searching the same keyword in the same city can see different results, because Google weighs location, search history, device, and time of day. A single manual check is a snapshot, not the truth.
- Search Console average position is the most honest free signal, but it is an average across all searches, all locations, and all devices. A keyword with an average position of 12 may rank 5th for searchers near the business and 20th for searchers across town. Read it as a trend, never as an exact seat number.
- Daily movement is mostly noise. Positions bounce a few places day to day for reasons nobody controls: a competitor published a page, Google tested a layout, a review count changed. A move of 1 to 3 places in a day means nothing on its own. A move of 5 or more places sustained over two weeks means something real happened.
- Track few keywords well, not many keywords badly. A local business needs 15 to 30 keywords: the services it actually sells, in the city it actually serves. A list of 200 keywords is a report nobody reads.
- Rankings are a means, not the goal. A keyword that ranks 3rd and brings no calls is worth less than a keyword that ranks 8th and brings bookings. Always read positions next to clicks, calls, and bookings where that data exists.
- Free tools have limits. Free rank checkers cap the number of keywords and checks, and their data can be days old. Use them as a second opinion, never as the only source, and always record which tool produced which number.

## Process

1. **Build the keyword list first.** Source: the business website (services and location pages) and the user's own list, when provided. Start from the services the business actually sells and the city it serves. Include three types: money keywords (service plus city, such as Botox Fort Worth), research keywords (service plus question, such as how long does Botox last), and brand keywords (business name, owner name). Aim for 15 to 30 keywords total. For each keyword, record the target page on the site, the search intent (buying, research, or brand), and why it matters in one short phrase. Drop any keyword with no matching page on the site; it cannot rank until the page exists.
2. **Set up the tracking sheet.** Use one spreadsheet with one row per keyword and columns for the keyword, target page, intent, baseline position, current position, change, Search Console clicks, Search Console impressions, notes, and last checked date. Keep a second tab for monthly snapshots, with one column per month, so trends stay visible without scrolling through history. Freeze the keyword list for at least one month; changing the list every week makes trends unreadable.
3. **Record the baseline honestly.** Source: Search Console Performance report export, last 28 days. Before judging any movement, record a baseline: for each keyword, the average position, clicks, and impressions over the last 28 days. Where Search Console has no data for a keyword, write "no data" in the baseline, not zero. A keyword with no data is unranked or below the reporting threshold, and that is useful information on its own.
4. **Check on a steady rhythm, not daily.** Check positions once a week, on the same day and at roughly the same time, and do the full monthly review on the first working day of the month. Weekly checks catch real movement early enough to act. Daily checks create anxiety and false alarms. If a client asks for a daily check after a big site change, do it for one week only, then return to weekly.
5. **Do manual checks the clean way.** Source: live Google search in a private or incognito browser window. When you check a position by hand, reduce personalization: use a private or incognito window, sign out of Google, set the search location to the business city, and search on both mobile and desktop for the top 5 money keywords. Record the position of the business listing, the page that ranks, and what sits above it (ads, map pack, AI answer, competitor pages). Note the date, time, device, and location setting with every manual check. Never report a manual check as the ranking without those notes attached.
6. **Pull the Search Console trend every month.** Source: Search Console Performance report export, last 28 days versus the previous 28 days. Export the last 28 days of query data and compare it with the previous 28 days for every tracked keyword. Record clicks, impressions, average position, and CTR. A keyword whose impressions rise and whose average position improves is genuinely gaining visibility. A keyword whose impressions rise but whose position stays flat is riding a seasonal wave, not a ranking win. A keyword whose clicks fall while impressions hold steady usually has a title or snippet problem, not a ranking problem.
7. **Read movement without overreacting.** Use these rules before calling anything a win or a loss:
   - A move of 1 to 3 places in one week is noise. Note it and wait.
   - A move of 4 or more places in one week is worth watching. Check whether the page changed, a competitor changed, or Google updated.
   - A move sustained for two weekly checks in the same direction is a trend. Act on it.
   - A keyword that drops off page 1 to page 2 needs a page review within the week, starting with the checks in `website-audit`.
   - A keyword that jumps onto page 1 needs no celebration yet. Wait for the second weekly check, then check clicks to see whether the new position brings visits.
   - Always check the whole group before judging one keyword. If most keywords moved the same way on the same day, something site wide or Google wide happened, not a single page problem.
8. **Report in plain language with the sheet attached.** The monthly update is short: keywords improved, keywords declined, keywords unchanged, biggest mover in each direction, and one next step per mover. Save it as REPORT.md using the shape in ## Output format below. Attach or link the sheet; never paste the full table into the message body.
   - Sample monthly update: "In November we tracked 22 keywords. 9 improved, 4 declined, and 9 stayed in the same range. Botox Fort Worth moved from position 11 to position 7 and brought 18 more clicks than in October. Laser hair removal Fort Worth slipped from position 6 to position 9, and the page needs a title and content review this month. No keyword moved enough in a single week to call it an emergency. The full sheet is attached, with the November snapshot on the second tab."
9. **Check the tracking setup before delivering:**
   - [ ] The keyword list is 15 to 30 keywords, each with a target page and an intent label.
   - [ ] The baseline is recorded from Search Console, with missing data marked as no data, not zero.
   - [ ] The sheet has a monthly snapshot tab and a last checked date on every row.
   - [ ] Manual checks record date, time, device, and location setting.
   - [ ] The monthly update names movers in both directions and gives one next step for each.

## Output format

Save the tracking sheet and the monthly report in the user's workspace under one folder per business:

```
outputs/<business-slug>/rank-tracking-free/
  tracking-sheet.csv (or .xlsx, one row per keyword, plus a monthly snapshot tab)
  <YYYY-MM>/REPORT.md
  <YYYY-MM>/data/gsc-queries.csv
```

The tracking sheet lives at the top of the folder and is updated in place every week. Each month gets its own subfolder with that month's REPORT.md and the Search Console export it is based on.

REPORT.md must contain these sections, in this order:

- Header: business name, website, city, reporting month, data sources used, last checked date.
- Summary: keywords tracked, keywords improved, keywords declined, keywords unchanged, biggest mover up, biggest mover down.
- Section 1, Movers: one line per keyword that moved 4 or more places, with the old position, the new position, the change in clicks, and one next step.
- Section 2, Steady keywords: keywords that stayed in the same range, in one short paragraph. No action needed, but the report says so instead of ignoring them.
- Section 3, Clicks versus positions: keywords where clicks and positions disagree, and what that means (usually a title or snippet problem, or a seasonal wave).
- Section 4, Next steps: one next step per mover from Section 1, in priority order.
- Section 5, Not checked: keywords with no data or no check this month, marked as no data or not checked, never as zero.

## Tips

- Report zero, never estimate. If Search Console has no data for a keyword, write no data. If a manual check could not be run, write not checked. Never fill a blank with a guessed position.
- Validate brand name matches. A brand keyword may match a same name business in another city. Before counting a ranking as the client's, confirm the result that ranks is the client's own site or listing, by URL and by city.
- Flag ambiguous matches. If a search result could be the client's business or a different business with the same name, say so in the notes column and in the report instead of picking one silently.
- Respect rate limits. Free rank checkers cap the number of keywords and checks per day; spread checks across the week instead of running the whole list at once, and always record which tool produced which number. Do not run automated bulk searches against Google; manual checks stay manual.
- Rerun cadence. Check weekly, on the same day and at roughly the same time, and do the full monthly review on the first working day of the month. Freeze the keyword list for at least one month so trends stay readable.
- Keep every monthly snapshot. The trend across months is the tracking sheet's real value, and it only exists if past months are kept.

## Further Reading

- Google Search Central, Search Console performance report help (support.google.com/webmasters)
- Google Search Central, SEO Starter Guide, measuring results (developers.google.com/search/docs/fundamentals/seo-starter-guide)
- Moz, The Beginner's Guide to SEO, tracking and measuring (moz.com/beginners-guide-to-seo)
