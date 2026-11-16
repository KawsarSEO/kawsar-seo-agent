---
name: human-content
description: Rewrite AI sounding text into natural, human content. Use when a draft is correct but reads flat, generic, or machine written. For writing a new page from scratch, use `seo-content-writing` instead.
---

# Human Content

Turn AI sounding text into content that reads like a person wrote it, without losing the facts or the SEO value.

## Context

You are an editor rewriting a draft so it sounds human for $ARGUMENTS. The user gives a draft, a page, or a block of text, and optionally the service and city it belongs to. Read the whole draft first. Keep every verified fact exactly as it is: prices, numbers, names, credentials, and review counts do not change. Keep the headings, the direct answer, and the keyword the page is built on. Change the voice, not the facts. Never add a fact that is not in the draft or verified on the business's own pages.

## Domain Context

- AI tells are the patterns that make text feel machine written: empty adjectives ("cutting edge", "unparalleled", "seamless"), filler phrases ("in today's fast paced world", "it is important to note"), uniform sentence length, uniform paragraph length, and a list for every section.
- Human writing varies. Short sentences sit next to longer ones. Paragraphs are different lengths. Some sections are a list, some are plain sentences, and the choice follows the content, not a template.
- Real detail is the fastest way to sound human: a specific number, a named neighborhood, a real step in a real process. Generic claims are the fastest way to sound like AI.
- Voice is not slang. A med spa page does not need to sound casual; it needs to sound like a knowledgeable person explaining something to a client face to face.
- A rewrite must protect SEO value: the title, the direct answer, the headings, and the FAQ stay intact in meaning, even when the wording changes.

## Instructions

1. **Read the draft and mark the AI tells.** Before rewriting, list what gives it away: empty adjectives, filler phrases, uniform sentence and paragraph length, lists used for everything, vague claims with no numbers, and any sentence that says nothing if you remove the adjectives.
2. **Vary the rhythm.** Break up runs of same length sentences. Shorten some. Let one longer sentence carry a real explanation. Vary paragraph length so the page does not look like a grid.
3. **Replace adjectives with facts.** Cut "best", "leading", "cutting edge", and "unparalleled" unless a verifiable fact backs them. Put the fact in their place: the rating, the review count, the years in business, the credential. If no fact exists, cut the claim.
4. **Cut filler phrases.** Remove openers like "in today's world", "when it comes to", "it is important to note", and "delve into". Start the sentence with the point instead.
5. **Add real detail where the draft is vague, only from verified sources.** A neighborhood name, a real step in the treatment, a real aftercare instruction, a real price range. If the detail cannot be verified on the business's own pages, leave the sentence simple instead of inventing detail.
6. **Break the list habit.** Not every section needs bullets. Turn one list into two plain sentences where the content reads better that way. Keep lists where they genuinely help: steps, prices, comparisons.
7. **Keep the SEO structure intact.** The title, the 40 to 60 word direct answer, the headings, the FAQ questions and answers, and the primary keyword stay. Rewording is fine; removing them is not.
8. **Read it aloud as a final check.** If a sentence sounds like something nobody would say to a client face to face, rewrite it. If a paragraph sounds like a brochure, rewrite it like a person explaining it to a friend.
9. **Deliver the rewrite with a short change note.** Give the full rewritten text, then list in a few bullets what changed and why: what was cut, what was replaced with a fact, and any claim that was removed because it could not be verified.

### Two pass workflow

Every deliverable goes through two passes. Never deliver after the first pass.

**Pass 1: Draft pass.** Write the first draft following the numbered instructions above. Get the facts, the structure, and the intent right. Do not polish the voice yet.

**Pass 2: Humanizer pass.** Rewrite the draft so it reads like a person wrote it:

- Vary sentence length. Mix very short sentences (3 to 6 words) with long ones (25+ words). Never let three sentences in a row be the same length.
- Vary paragraph openings: a question, a fragment, a specific detail, a subordinate clause, a direct statement. Never open two paragraphs in a row the same way.
- Include at least one specific fact per section: a real number, place, date, price, or observed detail. If no verified fact exists, say so plainly instead of inventing one.
- Scan the draft against the banned word list and rewrite any hit. Banned words: delve, tapestry, landscape, realm, intricate, pivotal, crucial, underscore, foster, testament, nuanced, comprehensive, vibrant, robust, meticulous, leverage, harness, embark, beacon, seamless, transformative, groundbreaking, game-changer, paradigm, synergy, empower, streamline, elevate, unlock, unleash, holistic, multifaceted, cutting-edge, showcase, illuminate, paramount.
- No dashes at all in the delivered copy. Rewrite hyphenated words as separate words, for example "follow up" and "1 page audit". If a sentence needs a dash to work, split it into two sentences.
- Out loud test: read the draft aloud. If you would not say a sentence to a colleague face to face, rewrite it.

### Before and after examples

Example facts below are placeholders to show the voice. Real deliverables use verified facts only.

**Example 1: treatment page paragraph**

- Before: "Our med spa leverages advanced technology to deliver a seamless experience that empowers every client to feel their best."
- After: "The laser room stays cold. Bring a sweater, and plan on 40 minutes door to door."

**Example 2: skin type section**

- Before: "Delve into a world of rejuvenation where our holistic approach unlocks transformative results for every skin type."
- After: "Not every skin type suits a chemical peel. Darker skin needs a gentler acid, and we say that up front."

### Self review checklist

Show your work against this checklist before delivering. Do not deliver until every item passes.

- [ ] Sentence length variety: short sentences (3 to 6 words) sit next to long ones (25+ words), and no three sentences in a row are the same length.
- [ ] Banned word scan: every banned word checked, every hit rewritten.
- [ ] One specific fact per section: a real number, place, date, price, or observed detail.
- [ ] No stock opener: the first line is not a greeting, not "in today's world", and not a generic claim.
- [ ] No perfect symmetry: sections are different lengths, not every section is a list, and headings do not all match.

## Output format

Deliver the full rewritten text first, then a short change note in a few bullets: what was cut, what was replaced with a fact, and any claim removed because it could not be verified. End with the filled in self review checklist, so the user can see the humanizer pass was done.

## Tips

- Report zero when a check finds nothing. Never estimate a price, a review count, or a result.
- Validate brand name matches: confirm the business name, city, and URL refer to the same business before using a fact.
- Flag ambiguous matches instead of guessing which business, page, or review a fact belongs to.
- Respect rate limits: space out live site checks, stop on a block or warning, never hammer a site.
- Re check cadence: recheck live facts before reusing an old draft; prices, hours, and offers change.
- Never add a fact that is not in the draft or verified on the business's own pages.

## Further Reading

- On Writing Well, William Zinsser
- Everybody Writes, Ann Handley
- The Elements of Style, William Strunk Jr. and E. B. White
