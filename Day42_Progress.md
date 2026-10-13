# Day 42 Progress: Ready for Strangers, the Law Read and Built, Fewer Password Prompts

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

This covers everything since the last note: the evening after it, and today.

**A debugging and performance pass over the whole codebase** (the evening after the last note).
- **89 findings fixed in one pass:** slow queries, the same thing read twice on one page, a scheduled job that stopped at its first failure, and places where an error would have been swallowed.
- **The leftovers of the content review,** and one more rule for how answer choices are generated.

**Ready for a round of strangers.**
- **The operator is told when something needs a person:** errors rising, the AI feature in trouble, a job failing, a new family, a note from a tester. One notice per kind per hour, with nothing about which family.
- **A help page and a page for families who might join,** every claim checked against what the screens do today.
- **Replies to testers' notes,** read inside the product, with a notice that one is waiting, and a way to mark a note done.
- **A web admin page** behind the same access policy as everything else, with a second sign-in step, so routine support no longer needs a terminal.
- **Two red-team passes and a blue-team pass** against a running copy, before any stranger sees it: cross-family access, sessions, the AI boundary, flooding and cost. Every finding fixed with a test or accepted in writing.
- **Slow first loads explained and softened:** the database sleeps when idle; public pages now wake it early, and the admin page shows an outline while it loads.

**Parents asked for their password less.**
- The parent area now closes after half an hour of inactivity rather than half an hour of time, stays open on a device the parent says is their own, and closes when a learner signs in on it. Actions that cannot be undone still ask every time.
- A bug a tester hit, where the dashboard's tabs vanished after one action, turned out to be the same wall closing from another tab; the actions now check the same rule as the pages.

**A legal study, read, verified, and built the same day.**
- **The question was whether a solo founder needs a lawyer for a test round.** Five researchers, 91 sources, every claim re-verified against the primary text (27 of 36 confirmed outright, the rest corrected or softened), then a second pass for what the first had missed: the hosting plan's own terms, the mailbox's terms, the oldest learners' own consent, who owns model-drafted content, the name, the fonts, pending federal law.
- **The verdict:** no law requires a lawyer for this round; the full children's-privacy rule applies with no exemption for size; the product's design removes the usual failure modes; the gaps were paperwork and wording. A bounded review is advisable now and required at the next stage.
- **Everything it listed as required is now built:** the notice parents read is generated from one source and reused wherever it is shown, so copies cannot drift; the privacy page says everything the rules name, down to the operator's telephone and the answer to Do Not Track; data kept "while the account exists" now has an end, with a notice first; the separate choices state law asks for, the oldest learners making their own; parents accept the terms with a box of their own, recorded with the version; the AI feature says it is one wherever it speaks; a written security program, a data map and a reasoned finding live beside the code and change by commit.
- **The round's own rules written down:** who it is for, what the recruiting replies ask, and what is kept as evidence.

**A recruiting department, on paper.**
- **Two agents that draft and never send:** one gathers families channel by channel and keeps the pipeline; the other makes the creative for channels that cost nothing, the page for families, a share kit and the weekly read. I post and send everything myself, and no invite link is ever public.

**Verification and deployment.**
- Eight commits since the last note, all pushed; the last deploy runs eight schema changes itself, all additive.
- Product document 0.89 to 0.93, technical document 0.67 to 0.72.

### Decided
- **The notice is one text,** generated wherever it is shown, never copied by hand.
- **Numbers the law doesn't set are named defaults I confirm,** not choices an agent makes: how long an unused account lives, which year levels are asked themselves.
- **The version of what a parent read is recorded with their agreement.**
- **Testing starts only when everyone is gathered,** and runs a month, so consistency over the month is what gets measured.
- **No budget for recruiting.** Channels that cost nothing, honest claims, the maker named.

### Noticed
- **Legal reading is mostly reading.** The rules say what to show, where, and for how long; almost none of it needed new design, and every gap was a sentence or a date nobody had written down.
- **A verification pass changes a report.** Nine of 36 claims were stated more firmly than their sources allow and two were wrong; the second pass found a dozen topics nobody had looked at.
- **The same bug from a different tab.** A tester's vanished tabs weren't the tab code; a rule applied to pages had not been applied to the actions behind them.
- **"Nothing is saved" was not true.** The no-account demo keeps one anonymous row for a day; the page now says so.
- **A quoting mistake can hide a backslash.** Two edits made through the shell lost their backslashes, and the tests caught both.

## Numbers
- 1,507 automated tests across 157 files, all green
- Content checker green: 241 concepts, 173 levels, 1,564 items, 4.69 million generated questions checked
- 8 commits since the last note, 261 files, +15,270 / −1,981 lines, 63 test files among them (32 new)
- 8 schema changes, all additive; 59 tables, 49 migrations
- Product document 0.89 to 0.93, technical document 0.67 to 0.72
- Two red-team passes and one blue-team pass: every finding fixed or accepted in writing

## Next
- Set the operator's telephone and address on the host, and confirm the hosting plan allows commercial use.
- Confirm the retention periods and the year levels asked themselves.
- Check that the deploy ran its schema changes, then the live pages.
- Begin gathering families through the drafted channels; nothing starts until everyone is gathered.
- An hour with a lawyer over the notice, the privacy page and the terms, when affordable.

## Current Status
- The product is ready for strangers: alerts, help, replies, an admin page, two red-team passes and a blue-team pass behind it.
- The children's-privacy paperwork exists and is enforced by code and tests, with a short list of decisions left for me.
- Recruiting is drafted and waiting on my hand; no family has been contacted yet.

## Key Reflections
- **Read the law before paying someone to.** The study cost a day and answered the question; the hour with a lawyer will now be about the few things that are actually unsettled.
- **Make the legal text a build artifact.** A notice generated from code cannot drift from the screen, and a test holds them together.
- **Verify the verifier.** The study was only as good as its second pass.
- **Strangers change the bar.** What was fine for friends needed rules written down before a stranger saw it.
