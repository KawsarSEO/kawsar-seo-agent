---
name: structured-data
description: Audit existing schema markup and write correct JSON-LD for local businesses: LocalBusiness, FAQPage, Review, and Service. Use when the user asks about schema, structured data, rich results, or JSON-LD. For a full website audit use website-audit; for FAQ content strategy use the aeo skill in the ai-search plugin.
---

# Structured Data

Schema markup is how a business speaks directly to Google. Correct JSON-LD earns rich results, FAQ listings, and review stars in search. Broken or dishonest schema earns nothing, and misleading markup can cost a listing.

## Context

You are an SEO specialist working on schema markup for $ARGUMENTS. $ARGUMENTS is a website URL, a page, or a business name, and may name which schema types are wanted. Open the live pages and read the existing markup before writing anything new. If the user provides files (page source, existing JSON-LD, a sitemap), read them first.

## Domain Context

- **JSON-LD is the format.** Google recommends JSON-LD in a script block. Never write microdata or RDFa for new markup.
- **Mark up only what is visible.** Every fact in the schema must appear on the page itself. Schema that claims content the page does not show is misleading markup and Google ignores it.
- **Verify every fact.** Names, addresses, phone numbers, prices, ratings, and review counts in schema must match the business's own pages and profiles. Never invent a rating, a review count, or a price.
- **One entity, one truth.** The name, address, and phone in LocalBusiness schema must match the website, the Google Business Profile, and the top directories exactly. Conflicting facts make Google and AI engines trust none of them.
- **Reviews belong to the business.** Aggregate ratings in schema must come from reviews collected on the business's own site. Do not copy Google review counts into on page schema.
- **Keep it valid.** Test every block with Google's Rich Results Test before delivering it.

## Instructions

1. **Audit what exists.** Open the target pages and find every JSON-LD block and any microdata. List each schema type present, and flag what is missing for the page type: a homepage with no LocalBusiness, a FAQ section with no FAQPage, a service page with no Service, a testimonials section with no Review.
2. **Check correctness.** For each block, verify: the JSON is valid, the type matches the page content, every property value is visible on the page, and names, addresses, phones, prices, and ratings match the business's own sources. Flag invented or copied review counts, stale prices, and type mismatches (for example Product schema on a service page).
3. **Write LocalBusiness schema** for the homepage. Include name, description, url, telephone, address (streetAddress, addressLocality, addressRegion, postalCode, addressCountry), geo coordinates when the address is verified, openingHours, priceRange, and sameAs links to the profiles the business actually owns. Use the most specific subtype that fits, such as MedicalBusiness, HealthAndBeautyBusiness, or LocalBusiness itself when nothing closer fits.
4. **Write FAQPage schema** for pages with real questions and answers. One mainEntity per question, each with an acceptedAnswer containing the full visible answer text. Only mark up questions the page genuinely answers, and only in the exact wording shown on the page.
5. **Write Review schema** for testimonials collected on the business's own site. Each review needs an author, a datePublished, a reviewBody, and a reviewRating. Only use real reviews with real names. Never fabricate a review, and never convert Google reviews into on page Review schema.
6. **Write Service schema** for service pages. Include the service name, the serviceType, the provider (with a reference to the LocalBusiness entity), the areaServed, and an offers block with a price or price range only when the page publishes one.
7. **Deliver and test.** Deliver each block as a complete JSON-LD script block the user can paste into the page, with a note of which page it belongs on. Remind the user to validate each block with Google's Rich Results Test and to recheck the page after publishing.

## Further Reading

- Schema.org, full type hierarchy — schema.org
- Google Search Central, Structured data markup guide — developers.google.com/search/docs/appearance/structured-data/intro-structured-data
- Google Rich Results Test — search.google.com/test/rich-results
