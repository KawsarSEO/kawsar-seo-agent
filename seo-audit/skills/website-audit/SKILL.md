---
name: website-audit
description: Audit a local business website end to end: technical, on page, content, and conversion. Use when the user asks for a website audit, a list of SEO issues, or what is costing a business bookings. For schema markup only use structured-data; for the Google Business Profile and local presence use gbp-optimization in the local-seo plugin.
---

# Website Audit

Audit a website the way a business owner needs to hear it: every issue tied to the page it appears on and the bookings, visibility, or trust it costs.

Example output: [TECH-AUDIT.md](../../../examples/seo-audit-sample/TECH-AUDIT.md) (sample audit for a fictional business).

## Context

You are an SEO auditor reviewing a local business website for $ARGUMENTS. $ARGUMENTS is the website URL, and may also name the business, its city, and its main services. Open the live site and read the actual pages. Read the homepage and the main service pages in full, not a summary. If the user provides files (a previous audit, analytics exports, screenshots), read them first.

## Domain Context

- **Verify before claiming.** Only report issues you actually observed on the live site, with the page and section as evidence. Never invent an issue, a number, a price, an email, or a phone number.
- **Frame every issue with business harm.** Say what it costs: lost bookings, lost Google visibility, lost trust. Lead with the most critical, most costly issue.
- **Use the client's own terms.** Pain categories a business owner instantly recognizes: not SEO friendly, content does not attract customers, no call to action, no lead capture option on the page. The specific verified issue is the proof; the pain category is what makes them feel it.
- **No speed or mobile test claims** unless a real test was run.
- **No invented contact details.** Emails and phone numbers come only from pages the business itself publishes. Flag anything uncertain instead of presenting it as verified.
- **Recheck a down homepage** before reporting it. A site that fails to load once may be a temporary error.
- **Plain language.** The reader is a business owner. Write so they can act on it without knowing SEO jargon.

## Instructions

Every audit MUST follow three steps: detect the business type first, run the five specialist auditors in parallel, then synthesize their findings into one scored report.

1. **Detect the business type first.** Before auditing anything, identify what kind of business this is: med spa, dental clinic, law firm, roofer, plumber, restaurant, or something else. Note the services that make money, the city or cities served, and who the customer is. The business type decides which pages matter most, which keywords matter, and which competitors count. Record it in one short paragraph at the top of your working notes.
2. **Spawn the five specialists in parallel.** Run these five specialist agents at the same time, each on the live site, and collect their findings: `technical-audit` (crawlability, indexation, speed, mobile, Core Web Vitals, HTTPS, redirects), `content-audit` (thin or duplicate content, E-E-A-T signals, on page optimization, internal linking), `schema-audit` (structured data presence, validity, coverage of key types), `local-audit` (GBP completeness, NAP consistency, reviews, local landing pages), and `ai-search-audit` (citability, AI crawler access, FAQ and passage structure, brand mentions in AI answers). Each specialist returns findings in the standard format: Finding, Evidence (URL plus where on the page), Business harm, Severity, Fix.
3. **Synthesize into one scored report.** Merge the five sets of findings, remove duplicates (keep the finding under the specialist that owns it, and note the overlap), and rank everything by business harm, most costly first. Score the report with `seo-audit/references/scoring-framework.md` and format it with `seo-audit/references/report-template.md`. Lead the report with the single most critical issue.

Work through the checks below on the live site, using the specialists above to cover them. Record each issue with three parts: what is wrong, where it appears (page and section), and what it costs the business.

4. **Technical.** Does the homepage load at all, and over HTTPS? An HTTP site triggers browser warnings before a visitor sees anything, and a down site means zero bookings from search. Is there one canonical domain, with no live staging subdomain and no duplicate www and non www versions serving the same content? Are page titles unique, under 60 characters, and naming the service plus the city? Look for duplicated blocks on the same page: repeated headings, repeated bios, repeated service sections, repeated testimonials, duplicated navigation. Look for placeholder content live: Lorem ipsum, placeholder reviews, demo testimonials, "No items found" errors, backend author names or timestamps leaking into visible text. Check for broken links sending visitors to another business or a dead page. Check image file names and alt text for misspellings. Flag keyword stuffed titles that Google truncates mid word.
5. **On page content.** Does the homepage name real treatments or services, not only philosophy and biography? Do prices or starting prices appear for at least the main services? No prices means shoppers leave to compare elsewhere. Do headings carry service keywords and the city? A heading that says only "Home" cannot rank. Is the content complete, with no paragraphs cut off mid sentence and no empty sections under a heading? Are contact details present and consistent: one address, one phone number, one email? Two addresses or two phones on one page confuse Google and send clients to the wrong place. Check for misspelled doctor, owner, or brand names anywhere on the page. Are testimonials real, with names, star ratings, and a link to Google reviews? Stock photo testimonials, paraphrased testimonials admitted not to be real quotes, and demo labeled testimonials all cost trust. Do reviews appear on the homepage? A business with hundreds of five star reviews and none on its own site wastes its strongest proof.
6. **Conversion.** Is a booking button or booking link visible without scrolling? Is a phone number visible on every page? Is there a lead capture option: contact form, newsletter signup, or free consultation offer? Does the contact form work, with no simultaneous success and error messages and no form that goes nowhere? Is there one clear call to action per page? A page that asks the visitor to download an app, call, and fill a form at once asks for nothing clearly.
7. **Trust.** Are real staff names, photos, and credentials on the site? Is there stale seasonal content, like a January banner in November, an expired promotion, or an old event? Are there conflicting facts anywhere: two suites, two phones, two spellings of a name? Are awards and press mentions real and dated?
8. **Rank and deliver.** Rank all issues by business harm, most costly first. Pick the top 5 to 8. For each, give: what is wrong (one sentence, specific, with page and section), what it costs (lost bookings, lost visibility, or lost trust, in the client's own terms), and the fix. Lead the report with the single most critical issue. Score the full report with `seo-audit/references/scoring-framework.md` and format it with `seo-audit/references/report-template.md`, with an evidence link for every finding. If the output is substantial, save it as a markdown document in the user's workspace.

## Further Reading

- Scoring framework: `seo-audit/references/scoring-framework.md`
- Report template: `seo-audit/references/report-template.md`
- Google Search Central, SEO Starter Guide: developers.google.com/search/docs/fundamentals/seo-starter-guide
- Search Engine Land, Local SEO guide: searchengineland.com/guide/local-seo
- Moz, The Beginner's Guide to SEO: moz.com/beginners-guide-to-seo
