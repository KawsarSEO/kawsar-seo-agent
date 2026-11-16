# Scoring Framework

A 0 to 100 weighted audit score for a local business website. Every full audit scored with this framework, so scores can be compared across businesses and over time.

## Weights

| Section | Max points | Share |
| --- | --- | --- |
| Technical | 25 | 25 percent |
| Content and E-E-A-T | 25 | 25 percent |
| Local and GBP | 20 | 20 percent |
| AI search readiness | 20 | 20 percent |
| Conversion | 10 | 10 percent |
| Total | 100 | 100 percent |

## Grades

Grades apply per section and overall. A section grade uses the percentage of that section max. The overall grade uses the total score out of 100.

| Grade | Overall score | Section percentage | Meaning |
| --- | --- | --- | --- |
| A | 90 to 100 | 90 to 100 percent | Strong. Fix the small gaps and maintain. |
| B | 80 to 89 | 80 to 89 percent | Good. A few clear gaps to close. |
| C | 70 to 79 | 70 to 79 percent | Fair. Real problems costing bookings or visibility. |
| D | 60 to 69 | 60 to 69 percent | Weak. Major gaps need fixing soon. |
| F | 0 to 59 | 0 to 59 percent | Failing. Core problems are costing the business every day. |

Round section percentages to the nearest whole number. Show the total as a whole number out of 100.

## How to score

Start each section at its max points. Deduct points for each verified issue, using the criteria below. Only deduct for issues actually observed on the live site, profile, or directory page. Never deduct for a guess. If a check could not be run (for example, GBP could not be read, or no speed test was run), note it as not checked and do not deduct for it, but do not award full marks by default either: score only what was verified, and say what is missing.

Severity guide for deductions:

- Critical: deduct 5 to 10 points in the section, depending on the section max. The site is down, the homepage does not load, or clients cannot book or contact the business at all.
- High: deduct 3 to 5 points. A major gap costing bookings or visibility every day.
- Medium: deduct 1 to 2 points. A real gap, worth fixing, but not the first priority.
- Low: deduct 0.5 to 1 point. A small polish item. Round the section total to the nearest whole number at the end.

## Technical (25 points)

Score what the `technical-audit` specialist reports.

| Check | Points at stake | Score it high when |
| --- | --- | --- |
| Site loads over HTTPS | 5 | Every page loads over HTTPS, no warnings, homepage loads reliably. Deduct all 5 if the homepage does not load or serves over HTTP. |
| One canonical domain | 4 | One domain version serves content. No live staging subdomain, no duplicate www and non www versions. |
| Crawlability and indexation | 4 | Sitemap present, robots.txt allows key pages, main pages indexable, no important page blocked. |
| Redirects and broken links | 4 | No redirect chains or loops, no links to dead pages or to another business, no visible error text. |
| Mobile usability | 4 | Layout works on a small screen, text readable without zooming, buttons tappable, nothing cut off or overlapping. |
| Speed (only if tested) | 4 | Only score this if a real test was run. Score from the test result. If no test was run, mark it not checked and score the section out of 21, then scale to 25 and note the scaling. |

A site that does not load scores 0 for Technical, whatever else is true.

## Content and E-E-A-T (25 points)

Score what the `content-audit` specialist reports.

| Check | Points at stake | Score it high when |
| --- | --- | --- |
| Service pages name real services | 5 | Homepage and service pages name real treatments or services with clear descriptions, not only philosophy and biography. |
| Titles and headings | 4 | Titles unique, under 60 characters, naming service plus city. Headings carry service keywords and the city. No heading that says only Home. |
| Completeness, no thin or duplicate text | 5 | No empty sections, no paragraphs cut off mid sentence, no duplicated blocks, no city pages that only swap the city name, no placeholder text live. |
| E-E-A-T signals | 5 | Real staff names, photos, and credentials on the site. Real testimonials with names and star ratings. Awards and press mentions real and dated. No stock photo or demo labeled testimonials. |
| Prices and facts | 3 | Prices or starting prices appear for at least the main services. Contact details present and consistent: one address, one phone, one email. |
| Internal linking | 3 | Service pages link to each other and to booking or contact, important pages reachable from the homepage, no orphan pages. |

Deduct 5 points at once if placeholder content (Lorem ipsum, placeholder reviews, demo testimonials) is live on the homepage or a main service page.

## Local and GBP (20 points)

Score what the `local-audit` specialist reports.

| Check | Points at stake | Score it high when |
| --- | --- | --- |
| GBP completeness | 5 | Name, primary category, services with descriptions, hours, photos, posts, Q and A, and attributes all filled in and current. |
| NAP consistency | 5 | Name, address, and phone identical on the website, GBP, and top directories. Deduct 2 points per conflict, up to 5. |
| Reviews | 5 | Rating and count healthy for the niche, recent reviews present, negative reviews answered, reviews visible on the business own site with names, star ratings, and a link to Google reviews. |
| Local landing pages | 5 | One page per city or area served, each with local proof (real address, local reviews, local photos, area specific services). Deduct 2 points per missing or thin city page, up to 5. |

If GBP cannot be read, mark GBP completeness and reviews as not checked, score the section from the checks that were verified, and say what the owner should confirm.

## AI search readiness (20 points)

Score what the `ai-search-audit` specialist reports, with schema coverage from `schema-audit`.

| Check | Points at stake | Score it high when |
| --- | --- | --- |
| Quotable facts | 5 | Homepage states real facts as complete self contained sentences: rating and review count, years in business, credentials, starting prices. No vague claims that no engine could quote. |
| AI crawler access | 3 | Robots.txt allows AI crawlers. Deduct all 3 if AI crawlers are blocked. Mark not checked if robots.txt cannot be read. |
| FAQ and passage structure | 4 | Service pages answer real client questions directly, answers short and self contained, passages make sense out of context. |
| Comparison content | 3 | At least one honest comparison page for the niche, with prices and real differences. |
| Entity consistency for AI | 3 | One name, one address, one phone, one service list across website, GBP, and top directories. |
| Schema coverage for AI | 2 | LocalBusiness schema on the homepage, FAQPage where FAQ content exists, Review or AggregateRating where real reviews exist. |

A business with no quotable facts and no FAQ content scores at most 8 in this section, even if the rest is fine.

## Conversion (10 points)

Score from the audit findings on booking and contact paths.

| Check | Points at stake | Score it high when |
| --- | --- | --- |
| Booking visible without scrolling | 3 | A booking button or booking link is visible at the top of the homepage and service pages, with no scrolling needed. |
| Phone visible on every page | 2 | One phone number, visible in the header or footer of every page. |
| Lead capture option | 3 | At least one working lead capture option: contact form, free consultation offer, or newsletter signup. Form works, with no simultaneous success and error messages and no form that goes nowhere. |
| One clear call to action per page | 2 | Each page asks for one next step clearly. A page asking the visitor to download an app, call, and fill a form at once scores 0 here. |

If the booking link is broken or goes to another business, Conversion scores 0.

## Worked example

A med spa audit scores: Technical 18 of 25, Content and E-E-A-T 16 of 25, Local and GBP 14 of 20, AI search readiness 11 of 20, Conversion 7 of 10. Total 66 of 100, grade D. Section grades: Technical C (72 percent), Content and E-E-A-T D (64 percent), Local and GBP C (70 percent), AI search readiness F (55 percent), Conversion C (70 percent). The report leads with AI search readiness and content as the weakest sections, and the priority fix list starts with the most costly issue in those sections.

## Priority formula

The 0 to 100 score is the headline. The priority fix list in the report is ordered by a second number, the priority score, so the client fixes the most costly and widest reaching problems first.

Priority score = severity x affected pages / effort

Severity uses the same scale as the deduction guide above, as a number:

| Severity | Value | Meaning |
| --- | --- | --- |
| Critical | 10 | Clients cannot book or contact the business at all, or the site does not load. |
| High | 7 | A major gap costing bookings or visibility every day. |
| Medium | 4 | A real gap, worth fixing, but not the first priority. |
| Low | 1 | A small polish item. |

Affected pages is the count of pages the issue touches. A broken booking button on every page counts every main page. A misspelled name on one page counts 1. A homepage only issue counts 1. Cap the count at 20 so one sitewide issue does not crowd out everything else.

Effort is a 1 to 5 estimate of the work to fix it:

| Effort | Value | Meaning |
| --- | --- | --- |
| Quick fix | 1 | Under an hour. Edit text, fix a link, correct a name. |
| Small fix | 2 | A few hours. Rewrite a section, add a page element, fix a form. |
| Medium fix | 3 | A day or two. Rebuild a page section, add schema across templates. |
| Large fix | 4 | A week. Restructure pages, rebuild booking flow, major content work. |
| Major project | 5 | Several weeks. Redesign, migration, or platform change. |

Rank every fix by priority score, highest first, and take the top 10 for the report's priority fix list. Break ties by severity first, then by business harm in the client's own terms. Show the severity, affected pages, effort, and priority score next to each fix so the client can see why it ranks where it does. Fixes outside the top 10 go in an appendix, still ordered by priority score.

## Rules

- Score only what was verified. Note every check marked not checked.
- Show the score table in every report, with section scores, percentages, and grades.
- Re score after fixes using the same criteria, so the client can see progress.
