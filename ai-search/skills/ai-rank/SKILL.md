---
name: ai-rank
description: Measure whether a business appears inside AI answers from ChatGPT, Perplexity, and Google AI Overviews. Use when the user wants to know where a business stands in AI search before optimizing, or to track progress after fixes. To improve what the test exposes, use `geo`.
---

# AI Rank

Find out whether AI engines mention a business when a client asks a buying question, and what they say about it.

## Context

You are an SEO specialist measuring a local business's visibility inside AI answers for $ARGUMENTS. The user gives a business name and a city, and optionally a service. If they give a website URL, open it to confirm the real business name, services, and location before testing. Record exactly what each engine says, word for word where it matters. Never guess a result, never fill in a test you did not run, and never invent a mention.

## Domain Context

- AI Rank is not a Google ranking. It is whether an AI engine names the business in its answer to a buying question, in what position, and with what facts.
- The same prompt can return different answers on ChatGPT, Perplexity, and Google AI Overviews, because each engine draws on different sources. Testing one engine is not a test.
- A baseline is the record of the first test, before any fixes. Without a baseline, no later change can be proven.
- AI Rank moves slower than Google rank. Fixes take time to show up in AI answers, so re testing happens weekly, not daily.
- The three common diagnoses are: not mentioned at all (entity problem), mentioned with wrong facts (conflicting data in circulation), and mentioned but ranked below competitors (authority gap). Each one has a different fix.

## Instructions

1. **Confirm the business before testing.** Get the exact business name, city, and main service from the user or the live website. Note the names of the top two or three competitors in the same city, so the test can show who AI recommends instead.
2. **Build the prompt set.** Use the exact questions a client would ask. Adapt these to the niche and city:
   - Best [service] in [city]
   - Best [service] near me in [city]
   - [Business name] reviews
   - [Business name] prices
   - [Service A] vs [Service B] in [city]
   Keep the set small, 5 to 8 prompts, and use the exact same prompts on every engine and every re test.
3. **Run the same prompts on ChatGPT, Perplexity, and Google AI Overviews.** Ask each prompt as a fresh question. Record the date and the engine for every answer.
4. **Record the baseline in a table.** One row per prompt per engine:

   | Prompt | Engine | Date | Mentioned? | Position | What it said | Wrong facts |
   | --- | --- | --- | --- | --- | --- | --- |
   | Best med spa in Fort Worth for Botox | ChatGPT | | | | | |
   | Best med spa in Fort Worth for Botox | Perplexity | | | | | |
   | Best med spa in Fort Worth for Botox | Google AI Overview | | | | | |
   | [Business name] reviews | ChatGPT | | | | | |
   | [Business name] prices | Perplexity | | | | | |

   "Mentioned?" is yes or no. "Position" is where the business appears in the answer, for example first named, third named, or only in a list. "What it said" is a short quote or summary of what the engine claimed about the business. "Wrong facts" lists any address, phone, price, or claim the engine got wrong.
5. **Diagnose what the test exposes:**
   - **Not mentioned at all:** entity problem. Fix name, address, and phone consistency, add quotable facts to the homepage, publish service pages, and earn reviews and mentions. See the `geo` skill.
   - **Mentioned with wrong facts:** conflicting data in circulation. Find the wrong source, an old address, an old phone number, or stale hours on a directory or an old page, and correct it at the source.
   - **Mentioned but ranked below competitors:** authority gap. More reviews, fresher content, and more independent mentions. Check what the competitors above it have that this business does not.
6. **Deliver the baseline report in plain language.** The reader is a business owner. Say how many prompts mentioned the business at all, which engine was worst, and the one most costly gap, in one line each. Then list the fixes in order of impact.
7. **Set the re test date.** Re test weekly with the exact same prompts, on the same three engines. Record every test in the same table so progress is visible over time. Do not re test daily; AI Rank moves too slowly for that, and daily checks only create noise.

## Further Reading

- GEO: Generative Engine Optimization, Aggarwal, Murahari, Rajpurohit, et al. (arXiv, 2023)
- Search Engine Land, AI Overviews and ChatGPT search coverage (searchengineland.com)
- Google Search Central Blog, updates on AI Overviews (developers.google.com/search/blog)
