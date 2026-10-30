# Day 53 Progress: CI Running Again After a Month, the Content Waves Finished, a Shortcut Closed in Two Tries

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

**CI had not run its tests for a month, and nobody knew.**
- **Found from a screenshot of mine:** every run since late September showed one of two checks red. The linter ran out of memory on the hosted runner, which has two cores, so it got a single thread and one process had to hold the whole repository. Every step after the linter (tests, audit, content check, simulator, build) had been skipped since then. The host's own build was green, which is why it looked fine.
- **Reproduced locally** by forcing one thread: it failed at the runner's memory and passed with more. The fix gives the linter more memory everywhere, not just in CI, because the content keeps growing. The first full CI run in a month was green.
- **Then the gate that should have been there:** the host now waits for CI's check before it deploys, and the main branch has a rule requiring it. Both were saved the same afternoon.

**Content wave two finished, and three smaller batches after it.**
- **Batch three and the later lanes,** ten lanes: each an author on the mid-size model, then a reviewer on the larger one that measured again and fixed what it found. Pushed in two gated batches.
- **Three more batches of later content,** nine lanes in all, each started on my word and pushed under the standing word for content once its review passed. The content list ended the afternoon empty.
- **A path too long:** the first gate, run from a deep scratch folder, failed before checking anything because a tool's state file went past the system's path limit. While agents are working, gates now run from a short worktree beside the repository, so the gate checks a fixed commit and the agents keep going.

**The whole code list, one item at a time.**
- **Fourteen items, each put to me with options and a recommendation,** several measured first by a runner before I chose. Built: help that can no longer hand over an answer, a screen reader's label naming only what is there, two new picture layouts (with a phone-width check still mine to do), learning content kept in the question's own form, and the two flaky tests from the last note.
- **Content lanes from the same list:** examples moved off questions they looked like, content rebuilt so the right answer is no longer the odd one out, teaching examples that no longer write out an answer the questions ask.

**A shortcut: measured, a first design failed, a second one switched on.**
- **Measured across all learning content:** some items could be won more often than chance by a pattern rather than by the math, a few hundred of them by a lot. I chose to fix it in the engine, built switched off.
- **The first design passed on averages and failed per item.** The builder's four failing tests were the ones that caught it; the builder proposed changing the test setup so they would pass, and that was refused, because the tests were right. A supervisor measured every item and found the design broke an existing rule on hundreds of them. It stayed off.
- **A lever study found a second design** with almost the same gain that keeps that rule. Built off, checked item by item by a supervisor, then the variant I chose, which gives up a little of the gain for something I value more, built and switched on after a full gate. The shortcut's edge fell on most of the items where it was largest; on dozens of others it grew a little, and four went past the limits I hold. A content lane could not honestly move those four, so they are on the list.
- **For the items the engine could not move, two content lanes.** The reviewers replaced or removed eleven of the twenty explanations the authors wrote: mistakes no learner makes, explanations that were false on some items, and one change that made an item easier instead of harder. What shipped is smaller and true.

**Verification and deployment.**
- 38 commits, all pushed, from seven sessions in one day: fourteen pushes, each after a full check run.
- No schema change.

### Decided
- **Fix the linter's memory everywhere,** not only in CI.
- **The host deploys only after CI's check passes,** and the main branch requires it.
- **Every item on the code list,** one at a time, from measured options; most as recommended, a few my own way.
- **The shortcut is fixed in the engine,** with the variant that gives up a little gain for what I value more.
- **A rule I had set earlier the same evening was relaxed** where the second design needed it; the older rule the design was built around was kept.

### Noticed
- **A green deploy is not a green CI.** The host built and shipped every push while the tests had stopped running a month earlier. One screenshot found it.
- **Averages hide the item that breaks.** The first design looked fine overall and was wrong on hundreds of single items. Every brief now says to judge per item.
- **A test that fails when a feature is switched on is a finding.** The builder wanted to change the test; the supervisor proved the test right.
- **Invented explanations sound plausible.** Fourteen new ones in the first lane; the reviewer replaced six. In the second, the reviewer removed four of six and replaced a fifth.
- **Two tests timed out under load,** with simulations running beside the check. They pass alone in four seconds; they now have the longer timeout the slow tests use.
- **Two agents typed progress times from memory** instead of the clock. Briefs now say the shell clock only, and times come from git.

## Numbers
- 2,294 automated tests across 198 files (from 2,229 across 193); green on a quiet machine before the last push
- 38 commits, 61 files, +2,772 / −592 lines
- Content items unchanged at 1,622
- No schema change; 61 tables, 53 migrations
- Product document 1.22 to 1.24, technical document 1.02 to 1.04
- Fourteen pushes; one gate red on two timeouts under load, green on a quiet rerun
- CI's full pipeline running again for the first time since September 28

## Next
- An engine change for the few items still past my limits: measure first, then my word.
- A phone-width look at the two new layouts, then the content lane held for it.
- The next config version, and three engine items queued behind the switch.
- The open device checks, the playtest sheet and the company paperwork.

## Current Status
- All 38 commits are pushed and the tree is clean; the host's builds for the last two are mine to confirm.
- The shortcut fix is pushed and switched on; it is live once the host's build is confirmed.

## Key Reflections
- **Check the check.** A month of pushes went out on a green deploy while the tests had silently stopped. A pipeline that reports green has to be read, not trusted.
- **Judge the parts, not the whole.** A design that improves the average can still break the rule for hundreds of single items. Measure per item before switching anything on.
- **A failing test is evidence.** The fastest way to lose a rule is to change the test that guards it. That change was refused, and the supervisor that proved the test right was worth the whole job.
- **Reviewers earn their cost on the made-up parts.** Authors under a target invent plausible explanations; a reviewer that recomputes every claim against every case is what keeps them true.
