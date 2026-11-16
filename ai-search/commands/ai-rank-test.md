# /ai-search:ai-rank-test

Tests a business's AI search visibility with a set of buying prompts on ChatGPT, Perplexity, and Google AI Overviews, and records the baseline.

## When invoked with $ARGUMENTS

$ARGUMENTS is a business name and a city, optionally with a service, for example `Radiance Med Spa, Fort Worth` or `Radiance Med Spa, Fort Worth, Botox`.

Follow these steps:

1. Confirm the business. If the user gave a website URL, open it and confirm the exact business name, the city, and the main service. Note the top two or three competitors in the same city.
2. Build a prompt set of 5 to 8 questions a real client would ask, adapted to the niche and city:
   - Best [service] in [city]
   - Best [service] near me in [city]
   - [Business name] reviews
   - [Business name] prices
   - [Service A] vs [Service B] in [city]
3. Run the exact same prompts on ChatGPT, Perplexity, and Google AI Overviews. Ask each prompt as a fresh question and record the date.
4. Record the baseline in a table, one row per prompt per engine, with these columns: Prompt, Engine, Date, Mentioned?, Position, What it said, Wrong facts. Never guess a result or fill in a test that was not run.
5. Diagnose the result:
   - Not mentioned at all: entity problem, fix consistency, quotable facts, service pages, reviews and mentions.
   - Mentioned with wrong facts: find the wrong source and correct it there.
   - Mentioned but below competitors: authority gap, more reviews, fresher content, more mentions.
6. Deliver the report in plain language: how many prompts mentioned the business, which engine was worst, the one most costly gap, and the fixes in order of impact.
7. Set the re test date one week out, using the exact same prompts on the same three engines.
