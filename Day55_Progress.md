# Day 55 Progress: Three Year Levels Reviewed and Reworked Overnight, a Gate That Only Counts When the Machine Is Quiet, Two Tests That Lied

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

**One long session across the night, cut twice by the usage limit and continued both times.**
- **Up to seven agents at a time, the cap, from ten in the evening to noon,** with every job in its own folder: a brief on disk, a report, a reviewer's or supervisor's report with the commit message it proposes. The limit cut all seven at midnight and the work paused again before dawn; each time the progress lines on disk said where every job stood, and every job could have been continued from its files alone.
- **Harness refusals again:** seven agents were refused when they tried to write their reports and handed the text back; I saved each to disk verbatim before anything else.

**Learning content: three year levels reviewed by a teacher's eye the evening before, and most of the briefs built overnight.**
- **27 author runs, each followed by an independent reviewer that recomputed every answer from thousands of draws,** across three year levels, two among the youngest and one in the middle: 50 briefs written, 28 done, and 31 content commits in the window, counting the two from the evening before and one I made by hand. Reviewers fixed in place what they found: descriptions that did not match what they described, an example that handed an item its answer, items a learner could win by a pattern instead of the work, items too long for the youngest learners to follow in one go.
- **Items made fairer to a working learner and harder for a guessing one,** measured per item before and after: in one group a guessing learner had scored about two thirds; after the change, about two fifths.
- **A rule a learner must be told before being asked** is now said in the item itself, in the one place where conventions differ; my choice, recorded in the product document with the reason.
- **The engine gained two measured rules and one bug fix.** The two rules were built switched off and measured per year level, then switched on by my word: on a certain kind of item in the youngest year levels a guessing learner's easy win went from nearly half of draws to a few percent. The bug fix removed values that did not belong to the item.
- **Two authors reached for shortcuts the checks refused;** both were told to remove them, and every brief now forbids them by name.
- **Two commits from the evening before** also landed in this window: the documents made true after two readers' pass, and a guard that a play session can always be finished, from the previous day's security review.

**Four code fixes from a browser pass and the content reviews, each built by one agent and corrected by a second.**
- **The AI feature's panel on a small phone:** it had shrunk to a sliver under a tall tool, and its menu could not be reached by thumb at the largest text size. It now keeps its footing on upright screens and, when a tool needs the room, steps out of its way until the child wants it. Supervisors found and removed two flickers where the panel chased its own height.
- **Keyboard and screen-reader use:** when the AI feature offers help, keyboard focus now lands on the offer instead of eighteen Tabs away, and the offer's words are read with it.
- **The touch number pad:** a learner on a phone could not type an answer of one common form at all, and a learner on a keyboard could lose an item by pressing Enter on a key. Both fixed, the first from the year level where that form first appears, measured rather than assumed.
- **The picture module** gained three new kinds of drawing, and two spoken descriptions that could give a listener the answer can now be kept quiet; the items that need that are the next content briefs. 349,200 pictures drawn in tests with no failure.

**Security and sessions.**
- **Two security passes in the window, nothing above low.** The first, over the previous day's changes, re-graded its one finding to low and it was fixed the same evening. The second, a research pass over the current advisories and the product's safeguards: the advisories are already patched in what ships, one low finding in a safeguard around the AI feature was strengthened the same day with tests, and a new test guards the app's shape. Eleven rows added to the security baseline since the last note, now 128.
- **A parent whose sign-in had quietly ended was told they were still signed in and sent in a circle.** The page now knows when a sign-in has ended, and says so plainly with the form. The child's own sign-in and the parent area's protection were proven unchanged in a browser.
- **Two tests that turned a green tree red:** one picked its sample at random, and in 11 of 300 samples the difference it tested could not show; the other spent nine tenths of its time building what it never read and timed out under load. The host's CI went red on the second for one push, with the previous deployment staying live. Both fixed: the first now chooses a sample known to show the difference and fails loudly if none does; the second runs in about a ninth of the time.

**Housekeeping.**
- **Seven full check runs.** Two were red under the load of seven agents for reasons that were not defects (one of them also tripped by a file edited during the run). One quiet run found a real defect, an item one rule short of the content checker's minimum, fixed before the push. The last was red on four report tests that scan the whole local database, which a day of agent runs had filled with about 850 leftover test accounts; the same four failed at the previous green commit, so the cause was the database and not the code. A fresh empty database beside it, migrated and seeded, made the run green.
- **44 commits, four pushes.** No schema change.

### Decided
- **Start all four groups at once** on the evening's question, and every follow-up round on my word with options.
- **The three year levels' briefs:** which level order to swap, where a reading pass replaces a number, which rule to say before asking, which item to keep as it is because the change would be harder on a struggling learner, what to leave for the round.
- **The engine rules:** the two measured ones on, the third on as a bug fix; one of them limited to the youngest year levels.
- **Commit the panel fix as built, then the compact layout on a later brief;** the threshold for "too little room" chosen from three options.
- **The number pad fix from the year level the measurement showed,** one earlier than the brief said.
- **Keep an account rule as it is, and say it before a parent meets it,** not after.
- **The security items, all four:** the guard test, the stronger safeguard, one check I do myself, and the rest as manual rows.
- **Push, then close with the day's notes.**

### Noticed
- **Three false reds and one true one, and only a quiet machine told them apart.** Two check runs under seven agents failed on luck and on load; the run on an empty machine failed on a real defect its reviewer had missed because that reviewer had not run the checker; the last failed on a database the day had filled.
- **A test that passes by luck fails by luck.** A test chose a random sample; one run in thirty could not show the difference it asserted, and the slow one turned the host's CI red the next morning.
- **A page believed a sign-in that had ended** because it trusted what the browser held instead of checking. The server is the referee; a page that asks the browser is guessing.
- **An author kept editing after its hand-back was accepted,** under its reviewer's feet; it was stopped. An accepted hand-back ends the author's run.
- **One development tree allows one development server;** a builder that needed one drove another job's instead, and inserted test rows by hand into the local database. Noted as conduct, left as local test data.
- **Agents still overwrite a progress line, or grep a file the rules name.** Each was noted, none changed the work.
- **A local test database fills up over a long day.** Agents cut off mid-run never ran their cleanups, and by noon four report tests that scan every account could not finish in their time limits, at the new commit and at the last green one alike. The remedy was a fresh database, not a change to the code; the lasting fix, a report test that does not scale with the leftovers, is queued.
- **History is not for editing:** a builder put its change note into an entry of the change log eleven days old; the supervisor moved it to the current one.

## Numbers
- 2,489 automated tests across 217 files (from 2,397 across 206); green on a quiet machine before the last push
- 44 commits, 86 files, +4,598 / −499 lines, across 31 content commits and 13 code and document commits
- Content items 1,622 to 1,640, every one checked by the content checker across 4,920,000 generated draws
- No schema change; 61 tables, 53 migrations
- Product document 1.26 to 1.28, technical document 1.07 to 1.09, essentials unchanged at 0.5
- Security baseline 117 to 128 rows; two security passes, nothing above low
- Seven full check runs: two red under load, one red on a real defect, one red on a full local database and then green on a fresh one, three green; four pushes
- Up to seven agents at a time; in the window 27 author runs and 27 reviewer runs on content, ten builder and supervisor pairs on code, two QA passes and two security passes, each with its supervisor

## Next
- The content the picture module unlocks: four briefs, each a pair of runs.
- Two queued code briefs: an answer of one common form kept on one line everywhere it is shown, and an account rule said before a parent meets it.
- A report test that does not slow down as test data piles up, and the browser paths the last pass left out.
- The second wave of briefs for the three year levels, and the remaining lanes.
- Confirm the host's build and CI are green for the last push.
- Still open from before: the device checks, the playtest sheet and the company paperwork.

## Current Status
- All 44 commits are pushed, the last five at midday after a green run on a fresh database; the host's CI was red for one push on a test that has since been fixed, and the previous deployment stayed live throughout.
- Three year levels reviewed and most of their briefs built; the rest queued, some with a measurement to run first.

## Key Reflections
- **A gate is a gate only on a quiet machine.** Under load, tests fail for reasons that are not defects, and a lead who reruns without a diagnosis has learned nothing. Finish the jobs, empty the machine, run once, push on green.
- **Choose the sample that proves the claim.** A test that draws at random and asserts a difference will one day draw a sample with none. Pick the sample that is known to differ, and fail loudly when none can be found, so a real regression is a failure and not a lucky pass.
- **Where the suite does not check, the reviewer must.** The content checker holds rules the test suite never runs; a reviewer who skips it hands the defect to the gate, which is the most expensive place to find it.
- **Ask the source of truth, not a copy of it.** A page that trusts a copy will tell a parent something the server no longer believes. The server decides; the page displays.
