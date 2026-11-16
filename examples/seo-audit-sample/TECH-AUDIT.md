# Technical SEO Audit: Northwind Med Spa

> SAMPLE OUTPUT. Fictional business. All data in this file is fictional and invented for demonstration only. Northwind Med Spa, northwind-medspa.example, and Maple Falls do not exist. Do not treat any number here as real.

**Business:** Northwind Med Spa (fictional)
**Website:** northwind-medspa.example (fictional domain)
**City:** Maple Falls (fictional city)
**Audit date:** 17 Nov 2026
**Audited by:** Sample run of the website audit skill
**Pages crawled in this sample:** 24

## Overall score

| Section | Weight | Score | Grade |
| --- | --- | --- | --- |
| Technical SEO | 25 | 14 | F |
| Content and E-E-A-T | 25 | 16 | D |
| Local SEO and Google Business Profile | 20 | 13 | D |
| AI search readiness | 20 | 9 | F |
| Conversion | 10 | 6 | D |
| **Overall** | **100** | **58** | **F** |

Grading scale used in this sample: A is 90 to 100 percent of the section maximum, B is 80 to 89 percent, C is 70 to 79 percent, D is 60 to 69 percent, F is below 60 percent. Section scores add up to the overall score: 14 plus 16 plus 13 plus 9 plus 6 equals 58 out of 100.

Summary in one line: the site is findable but not competitive. Search engines can crawl most pages, yet thin content, missing local signals, and weak conversion paths cost this fictional business bookings every week.

## Top 10 fixes, ranked by priority

Priority score equals severity x affected pages / effort. Severity is rated 1 to 5, where 5 is most severe. Effort is rated 1 to 5, where 1 is quickest. A higher priority score means fix it first.

| Rank | Fix | Severity | Affected pages | Effort | Priority score |
| --- | --- | --- | --- | --- | --- |
| 1 | Write unique title tags and meta descriptions for service pages | 5 | 18 | 2 | 45.0 |
| 2 | Compress images and add descriptive alt text | 4 | 20 | 2 | 40.0 |
| 3 | Add one clear H1 to every page that is missing one | 5 | 14 | 2 | 35.0 |
| 4 | Fix broken internal links and redirect the 4 dead URLs | 4 | 16 | 2 | 32.0 |
| 5 | Expand thin service pages to cover benefits, process, and aftercare | 5 | 12 | 2 | 30.0 |
| 6 | Add LocalBusiness schema to the homepage and contact page | 3 | 18 | 2 | 27.0 |
| 7 | Link blog posts to the matching service pages | 4 | 12 | 2 | 24.0 |
| 8 | Add a visible booking button to every service page | 5 | 9 | 2 | 22.5 |
| 9 | Publish a services FAQ page answering the top 10 client questions | 3 | 14 | 3 | 14.0 |
| 10 | Add staff bios with credentials and photos | 4 | 6 | 2 | 12.0 |

Worked example for rank 1: 5 x 18 / 2 equals 45.0. Worked example for rank 8: 5 x 9 / 2 equals 22.5.

## Technical SEO: 14 out of 25, grade F

The site loads and is indexed, but crawl efficiency and page speed hold it back.

* 18 of 24 pages share the same generic title tag, "Northwind Med Spa", so search engines cannot tell the service pages apart. Evidence: /services/botox, /services/laser-hair-removal, /services/facials, and /services/microneedling all use the identical title.
* Largest Contentful Paint on mobile is 4.2 seconds in this fictional sample, driven by uncompressed hero images. Evidence: / (homepage hero image, 2.8 MB in this sample) and /services/laser-hair-removal (gallery images over 1 MB each).
* 4 internal links point to pages that return a 404. Evidence: links from /blog/skin-care-tips to /services/old-facial-page, and from /about to /team/old-bio-page.
* The XML sitemap lists 24 pages but includes 3 redirect chains and 1 URL that no longer exists.
* No hreflang or international targeting is needed for this single city fictional business, so that check is marked not applicable.

## Content and E-E-A-T: 16 out of 25, grade D

Content exists for every service, but most pages are too thin to rank or to persuade a reader to book.

* 12 service and treatment pages have fewer than 300 words and no before and after guidance, no process steps, and no aftercare notes. Evidence: /services/botox (210 words in this sample), /services/chemical-peel (185 words), /services/microneedling (240 words).
* 14 pages have no H1 at all, and 5 pages have two H1 tags. Evidence: /services/facials has no H1; /pricing has two H1 tags.
* Author and credential signals are missing. No staff page lists licenses or years of experience, and no page names the medical director. Evidence: /about and /team.
* The blog has 6 posts, but none link to a service page and none target a Maple Falls local query. Evidence: /blog/skin-care-tips, /blog/what-is-microneedling.
* Positive note in this sample: service descriptions are accurate and readable, with no keyword stuffing found.

## Local SEO and Google Business Profile: 13 out of 20, grade D

Local visibility is the biggest missed opportunity for this fictional Maple Falls business.

* No LocalBusiness schema exists anywhere on the site, so search engines get no structured name, address, phone, hours, or service data. Evidence: homepage source at / and /contact.
* Name, address, and phone details are inconsistent. The footer shows one phone number and the contact page shows a different one in this fictional sample. Evidence: / (footer) versus /contact.
* The fictional Google Business Profile in this sample has 11 reviews and no posts in the last 90 days, and 3 of 8 services are missing from the profile.
* Only 2 pages mention Maple Falls or nearby fictional neighbourhoods by name. Evidence: / and /contact mention Maple Falls; no service page does.
* No location page exists for the fictional Maple Falls neighbourhoods the spa claims to serve.

## AI search readiness: 9 out of 20, grade F

AI engines rarely cite this fictional site, because it gives them little structured, quotable material.

* No FAQ schema and no HowTo content exist, so there is almost nothing for an AI answer engine to quote directly. Evidence: /services/botox and /services/laser-hair-removal have no FAQ block at all.
* Service pages do not answer the questions clients actually ask, such as how long results last, what it costs, and who should avoid the treatment.
* The site has no concise service summaries of 40 to 60 words that an AI engine could lift as a direct answer.
* Brand mentions outside the site are thin in this sample: 3 fictional directory listings and no local press mentions.
* A full citation breakdown for this fictional business is shown in the companion sample report, examples/ai-visibility-sample/REPORT.md.

## Conversion: 6 out of 10, grade D

Visitors who do arrive find it harder to book than it should be.

* 9 service pages have no booking button above the fold; the only path is a small contact link in the footer. Evidence: /services/botox, /services/facials, /services/chemical-peel.
* The booking form asks for 9 fields before showing any availability, which is a long form for a first visit enquiry.
* No trust signals appear near the booking step: no review count, no star rating, and no guarantee or cancellation note.
* The phone number is not click to call on mobile on 6 pages in this sample.
* Positive note: the contact page loads fast and the form itself works, with a confirmation message after submit.

## What to do first

1. Fix ranks 1 to 3 from the priority table above. They are quick, they touch most of the site, and they improve rankings, AI citations, and click through rate at the same time.
2. Then fix the booking path (rank 8) before spending anything on ads or new content. Traffic that cannot book easily is wasted traffic.
3. Then publish the FAQ page (rank 9) and the staff bios (rank 10) to lift the content and trust scores together.

## Method note

This is a sample output. Scores, page counts, word counts, load times, review counts, and all findings are invented to show the shape of a real audit. A real skill run produces this same file shape with real measured data for a real business.
