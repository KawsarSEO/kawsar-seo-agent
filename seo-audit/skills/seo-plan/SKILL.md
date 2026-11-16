---
name: seo-plan
description: Compose the REPORT.md outputs of other skills into a 90 day SEO plan with phases, owners, success metrics, and a critical path. Use when the user asks for a 90 day SEO plan, an SEO roadmap, what to do first, how to prioritize SEO work, or how to turn audit findings into a plan. This skill does not audit anything itself; it only plans from reports that already exist. For the website audit itself, use `website-audit`. For keyword research, use `keyword-research`. For competitor gaps, use `competitor-analysis`. For AI visibility measurement, use `ai-visibility`.
---

# SEO Plan

Turn finished audit reports into a 90 day plan a business owner can actually follow: what to fix first, who does it, what success looks like, and which tasks block everything else.

Example output: [SEO Plan sample](../../../examples/README.md)

## Context

You are an SEO strategist building a 90 day SEO plan for $ARGUMENTS. $ARGUMENTS is the business name and website, and may include the paths to the input reports and the team available to do the work. This skill composes reports; it does not audit, check, or measure anything itself. Every task in the plan must trace back to a finding in one of the input reports. Never invent a finding, a score, or a task that no input report supports. If a report says something, cite it. If no report says it, leave it out.

## Prerequisites

- Input reports, as REPORT.md files produced by the other skills. The four inputs are:
  - `website-audit` REPORT.md: the site issues, scores, and priority fix list. This is the main input.
  - `keyword-research` REPORT.md: the keyword table, intent, and top 10 priorities.
  - `competitor-analysis` REPORT.md: the gap list and the top 3 recommended moves.
  - `ai-visibility` REPORT.md: the AI visibility score, the competitor comparison, and the fix list.
- What to do when an input report is missing:
  - If the `website-audit` report is missing, the plan cannot be built in full. Produce a partial plan clearly marked as partial, built from whatever reports are available, and put running `website-audit` as the first task of Phase 1. Do not invent site issues to fill the gap.
  - If the `keyword-research` report is missing, plan the keyword work from the target pages named in the website audit, and put running `keyword-research` as a Phase 1 task.
  - If the `competitor-analysis` report is missing, drop the competitor moves from the plan and put running `competitor-analysis` as a Phase 1 task. Do not guess what competitors do.
  - If the `ai-visibility` report is missing, drop the AI visibility work from the plan and put running `ai-visibility` as a Phase 1 task. Do not guess the AI score.
  - If no input report exists at all, do not build a plan. Say which reports are needed and run the audits first.
- The team available to do the work: who writes content, who edits the site, who owns outreach. If the user does not name a team, default to a one person owner plus the SEO, and say so in the plan.
- The business goal for the 90 days, when the user states one: more bookings, more calls, more visibility, or a new service launch. If no goal is stated, default to more bookings from Google and AI search, and say so.

## Domain Context

- A plan is a sequence, not a list. The order matters more than the count. A fix that unblocks five other fixes goes first even when it is not the flashiest item.
- Priority follows impact over effort. Use the priority formula severity times affected pages divided by effort: a critical issue on many pages that is quick to fix outranks a medium issue on one page that takes a week. Score every task this way instead of sorting by gut feeling.
- Every task needs an owner and a done condition. A task with no owner is a wish. A task with no done condition cannot be checked off, so it stays open forever.
- Quick wins belong in Phase 1. The first 30 days should hold fixes the owner can see: a fixed title, a live booking button, a corrected business listing. Visible progress in month one buys trust for the slower work in months two and three.
- AI visibility work is slow work. Entity fixes and quotable facts belong early in the plan, but their results show up late, because AI systems reuse trusted sources until fresh signals change their mind. Put the work in Phase 1 or 2 and the measurement in Phase 3.
- A plan that ignores capacity fails in week two. A one person team cannot do 20 tasks in 30 days. Cap each phase at what the named team can realistically finish, and say what was left out and why.
- Plans go stale. A new audit, a Google update, or a competitor move can change the order. Revisit the plan monthly and reprioritize from fresh reports instead of following a stale order out of habit.

## Process

1. **Collect and read the input reports.** Sources: the REPORT.md files listed in ## Prerequisites, in the user's workspace. Read all four reports end to end. For each report, note the date it was produced, the top findings, and the scores. If a report is older than 60 days, flag it as stale in the plan and treat its findings as unverified until rechecked.
2. **Extract every finding into one task list.** Sources: the priority fix list from `website-audit`, the top 10 keywords from `keyword-research`, the gap list and top 3 moves from `competitor-analysis`, and the fix list from `ai-visibility`. Turn each finding into a task with the source report named, the page or keyword it applies to, and the business harm in the client's own terms. Drop duplicates where two reports name the same fix, and keep the stronger evidence. Never add a task no report supports.
3. **Score and rank the tasks.** Source: the task list from step 2. Score every task with the priority formula severity times affected pages divided by effort. Severity comes from the source report (Critical, High, Medium, Low). Affected pages is the count of pages the fix touches. Effort is a rough size: small (under a day), medium (a few days), large (a week or more). Rank the tasks highest score first. Where two tasks tie, the one that unblocks other tasks goes first.
4. **Find the critical path.** Source: the ranked task list. Mark every task that another task depends on: the homepage rewrite blocks the service page rewrites, the entity fix blocks the AI citation work, the keyword map blocks the new content pages. Lay the dependencies out as a chain, and name the single chain that decides how fast the whole plan can finish. That chain is the critical path. Any delay on it delays the plan.
5. **Split the plan into three phases.** Source: the ranked task list and the critical path. Phase 1, days 1 to 30: quick wins and unblockers, the critical path first tasks, and any missing audit from ## Prerequisites. Phase 2, days 31 to 60: content and authority work, new and rewritten pages, link building starts, AI visibility fixes land. Phase 3, days 61 to 90: measurement, refinement, and the work that only makes sense after the earlier phases. Cap each phase at what the named team can finish. Tasks that do not fit go into a backlog section with the reason they were deferred.
6. **Assign owners and success metrics.** Source: the team named in ## Prerequisites and the metrics in the input reports. Give every task one owner and one done condition: a sentence that is true only when the task is finished. Give every phase one success metric with a starting number from an input report and a target number: for example, website audit score from 62 to 75, AI visibility score from 9 to 18, or 5 keywords on page 1 instead of 2. Targets must be reachable in 90 days; a target no report supports is a guess, not a goal.
7. **Build the plan document.** Save it as REPORT.md using the shape in ## Output format below. Keep the language plain. The reader is a business owner, not an SEO. Every task names its source report, so the owner can check where it came from.
8. **Check the plan before delivering:**
   - [ ] Every task traces to a finding in a named input report.
   - [ ] Missing input reports are named, and running them is a Phase 1 task.
   - [ ] Tasks are ranked by the priority formula, not by gut feeling.
   - [ ] The critical path is named as a chain, with the tasks that block the rest.
   - [ ] Every task has one owner and one done condition.
   - [ ] Every phase has one success metric with a starting number and a target number.
   - [ ] Each phase fits what the named team can finish in 30 days.
   - [ ] No task, score, or target appears that no input report supports.

## Output format

Save the plan and its working task list in the user's workspace under one folder per business:

```
outputs/<business-slug>/seo-plan/
  REPORT.md
  task-list.csv (or .xlsx, one row per task, with source report, priority score, phase, owner, done condition)
```

REPORT.md must contain these sections, in this order:

- Header: business name, website, plan start date, plan end date (90 days later), input reports used with their dates, team available.
- Summary: the business goal for the 90 days, the single most important task, and the expected result in plain words. No result is guaranteed.
- Section 1, Critical path: the chain of tasks that decides how fast the whole plan can finish, in order, with the dependency between each pair of tasks named.
- Section 2, Phase 1, days 1 to 30: tasks in priority order, each with the source report, the page or keyword, the business harm, the owner, and the done condition. Ends with the phase success metric, starting number, and target number.
- Section 3, Phase 2, days 31 to 60: same shape as Phase 1.
- Section 4, Phase 3, days 61 to 90: same shape as Phase 1, plus the measurement tasks that judge the whole plan.
- Section 5, Backlog: tasks that did not fit the 90 days, each with the reason it was deferred.
- Section 6, Missing inputs: input reports that were missing, what was dropped because of them, and the Phase 1 task that produces each one. If nothing was missing, write None.
- Section 7, Risks: what could delay the plan, in plain words, such as a task with no owner, a dependency on a third party, or a stale input report.

## Tips

- Report zero, never estimate. If an input report gives no score for an area, write no score, never a guessed number. If a target cannot be set from a real starting number, leave the target out and say why.
- Validate brand name matches. When the input reports name competitors or cite brand mentions, confirm the names refer to the real businesses in the client's city before building tasks on them. A task built on the wrong competitor is wasted work.
- Flag ambiguous matches. If two input reports disagree, for example one says a page ranks well and another says it is invisible, say so in the plan instead of picking one silently. Put the conflict in Section 7, Risks, with the check that resolves it.
- Respect rate limits. This skill runs no data pulls itself, but the audits it depends on do. Do not ask the user to rerun all four audits at once to feed the plan; use the reports that exist, and schedule the missing ones as Phase 1 tasks.
- Rerun cadence. Revisit the plan monthly, or whenever a fresh input report lands, and reprioritize from the new findings. A plan older than 90 days is a history document, not a plan; build a new one from fresh reports.
- Keep the source reports linked. The plan is only as good as its inputs. Keep the input REPORT.md files with the plan folder, or record their paths in the header, so anyone can trace a task back to its evidence.

## Further Reading

- `website-audit` skill: the site audit that feeds this plan (seo-audit/skills/website-audit/SKILL.md)
- `keyword-research` skill: the keyword priorities that feed this plan (outreach/skills/keyword-research/SKILL.md)
- `competitor-analysis` skill: the gap list that feeds this plan (outreach/skills/competitor-analysis/SKILL.md)
- `ai-visibility` skill: the AI visibility fixes that feed this plan (ai-search/skills/ai-visibility/SKILL.md)
- `seo-audit/references/scoring-framework.md`: the 0 to 100 scoring used by the website audit
- `seo-audit/references/report-template.md`: the report shape the website audit follows
