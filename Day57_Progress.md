# Day 57 Progress: A Fault Fixed the Same Night, a Day of Failed Deploys Traced to One Test, and Seven Jobs That Survived a Crash and a Cut-Off

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

**Two sessions, from mid-afternoon to the small hours, seven agents at a time, interrupted twice and continued from files both times.**
- **A machine crash twenty minutes into the afternoon and a usage limit that cut all seven running jobs two hours later.** Nothing on disk was lost either time: every job had its brief on disk and a progress line at the top of its report, so each was restarted on the same brief and told to read its own line and its own uncommitted changes first. No job started again from zero; a few measurements that were in flight were run again.
- **About eighty agent runs across the two sessions, and about seventeen further rounds by message:** content authors and their reviewers, builders and their supervisors, one browser pass with its supervisor, one more browser pass on a single change, and three document jobs. A finished agent that is continued by message keeps what it already knows about the files.
- **Each code job in a folder of its own.** The two that met another job's code were moved onto the newest main branch and proven together before either was committed.
- **Both runs stopped at the previous close were finished** from their progress lines.

**A fault that could treat a right answer as wrong, found by an author who stopped as briefed.**
- **On a small set of items, a right answer could be treated as wrong.** A content author stopped, as briefed, when a request could not be built; following that up showed the fault was already in front of learners. I confirmed it with a script before anything else was done.
- **Fixed, measured and seen:** a builder made the change, a supervisor proved it through the real services and corrected two things in the builder's checks, and a tester watched it in a real browser at two phone sizes before it was committed. On the affected items a right answer is now always accepted.
- **Its side effects were looked for, not waited for:** the supervisor showed the change made nothing harsher anywhere, and that two figures in my own report would have started to mislead. Those were corrected in a follow-up the same night, and a third that still reads slightly high now says so where it is printed.
- **The rare grading defect left open the day before is fixed in the engine too,** as planned, measured before and after.

**The host's build had been failing since the previous day's push, and nobody knew.**
- **Every deploy since that push had failed,** so the live site had stayed on an older build. The cause was the clean-up step of one test committed the day before, which asked for a database the host does not have. I had been told the build was green; it was a different check that was green.
- **Fixed in one commit, and the gate changed for good:** every full check run now includes the host's own test step, run locally the way the host runs it, with no database and no settings file.
- **The second and third pushes were confirmed live by the founder** (the first had failed on the host, as above); the last, at the close, is still his to confirm.

**Learning content: twenty-one reviewed commits in four year levels.**
- **Sixteen in the afternoon,** from the reviews of three year levels: wording, drawings and choices mended where the reviews asked, each measured before and after.
- **One group of items rebuilt over four author runs and three reviews,** with the founder choosing its shape twice from measured options. Two of the reviews found a shortcut the run before had left open, and the last one mended a step in an explanation.
- **Two items that had shown every learner the same single question** at their easier levels since they were written. An internal check was so strict that nothing else could pass it. The author's fix removed that; the reviewer then showed the author had measured the wrong thing, and that at the easiest level a simple guess still won nearly two times in three. The reviewer's own fix brought that guess down to about one in three.
- **Six worked examples moved,** confirmed by a reviewer's measurement over 288,000 draws, with one choice about them made by the founder.

**An engine change that closes a whole class of give-aways.**
- **Help can no longer give away the answer it sits beside.** The reviews of the last two days had found cases by hand; a count over every year level showed it was wider than the cases found.
- **Three rounds with its supervisor before it was ready.** As first built it worked and was fast enough, but it made some items easier to guess, which is worse than what it cures. Two refinements from the supervisor's measurements, and the six examples above moved first, brought that within bounds; what remains is queued as content work.
- **Measured on about 1.8 million draws:** the cases it can see fell from 18,553 to 4, at about three percent more work for the generator, with no test near its time limit. What it cannot see is listed, example by example, for the next content wave.

**Five smaller changes for small phones and for parents, each built, checked by a second agent, and committed on the founder's word.**
- **Numbers in a drawing no longer shrink below a readable size** on the smallest phones. Drawings that already read well look exactly as before.
- **The AI feature on a small phone:** every word stays whole at the largest text size, and its reply stays readable in its smallest layout.
- **A line of encouragement now appears only where it is true.** Nothing new is stored about a learner for it.
- **A sentence on a parent's screen that read wrongly in one case, and a title that was cut off** at the largest text size.
- **Two tests that failed only in one late-evening hour** on the days around the autumn clock change. They spaced their data exactly a day apart, and one of those days was twenty-five hours long. Found because an unrelated check went red at 23:41.

**Housekeeping.**
- **Six full check runs and four pushes.** Two runs were red: one on a race between two test files, one on three time-outs. The time-outs were bisected to a single display-rule commit that had made the heaviest content tests about forty percent slower, and fixed. The last two runs were green before each of the night's pushes; one of them ran beside a single agent, against my own rule, and held.
- **The documents updated in three jobs and four commits,** each from the supervisors' corrected sentences and read line by line before the commit; I corrected four sentences across them.
- **The open security-baseline point was read and settled by the founder.**
- **A raw log of the day and a one-page start prompt for the next session,** rewritten at every stage boundary so a cut-off would lose nothing.

### Decided
- **By the founder, in the afternoon:** fix the failing test and run the gate again; commit two code jobs; a display rule's edge case; the engine change, from three ways to make it; the shape of the rebuilt group of items; fix the fault in code; the open security-baseline point.
- **By the founder, at night, from options I put to him, most with a recommendation:** which finished jobs to commit, in three rounds; the minimum size for numbers in a drawing; to leave one rule as it is for the test round, with the alternative named; a further change to the rebuilt items; a choice about how worked examples are chosen; to commit the engine change knowing its cost until the content catches up; and to push.
- **By the founder, after I told him his earlier choice rested on something untrue:** a behaviour he had asked for was built and tested, and then turned out never to run in the product as it stands. He chose to take it out.
- **By me, and said to him:** two refinements to the engine change; one change to the rebuilt items that a reviewer had marked as his (he kept it); which reviewer's fix to take on the two single-question items; to mend by hand what the engine change cannot reach, not to widen it.

### Noticed
- **I was wrong at least three times, and an agent caught each one.** My design for the report follow-up fixed one figure and broke another; the builder measured it and said so. I assumed an older safeguard covered a case; the supervisor showed it did not. I told the founder a thing was true of every item; a reviewer found the one item where it is not. Each was said to the founder the same night.
- **A supervisor's checks run alone do not show a suite-wide slowdown.** I committed a generator change on such a check and the gate went red. A generator change is now timed before and after.
- **"Green" has to say which check.** A day of failed deploys sat behind a message that the build was green.
- **A builder's "nothing changes on a wide screen" was wrong twice.** Both times the claim was reasoned, not looked at, and both times the condition in the code said otherwise.
- **An author can measure carefully and answer the wrong question.** The reviewer's table of what a guessing learner wins, set against the version before, is the check.
- **The harness refused most content authors' and document builders' report files.** I saved each hand-back to disk word for word before doing anything else with it.
- **Agents still type a clock time instead of reading it, and so did I, twice,** in the start prompt. Corrected; the briefs now say "read".

## Numbers
- 2,657 automated tests across 238 files (from 2,578 across 229); green before each of the night's two pushes, the last on a quiet machine
- 38 commits in the window, all pushed: 21 on learning content, 10 on code, 3 on tests, 4 on documents; 58 files, +2,849 / −674 lines
- Four pushes: the four commits waiting from the day before, then 22, 10 and 6
- Content items unchanged at 1,647, every one checked by the content checker across 4,941,000 generated draws
- No schema change; 61 tables, 53 migrations
- Product document 1.29 to 1.32, technical document 1.10 to 1.13, essentials unchanged at 0.5
- Security baseline unchanged at 128 rows; its automated checks held at each gate that ran them
- Six full check runs: two red, four green
- Up to seven agents at a time; about eighty runs across the two sessions, and about seventeen further rounds by message

## Next
- Confirm the host's build is green and live for the last push.
- A content wave of about seventeen files the engine change still needs, each with an author and a reviewer.
- A third item with the same over-strict cause as the two fixed today.
- The content checker's new report lines turned into failures once the content behind them is moved.
- One founder's choice from the afternoon that needs a small code job before its content can be written.
- One item for the founder to keep or move.
- Still open: the package type check in the standing reviewer rules.
- Still open from before: the device checks, the playtest sheet and the company paperwork.

## Current Status
- Everything that was running when the afternoon was cut off is built, checked by a second agent, committed and pushed, in two pushes after green runs. The main branch and the host's branch are the same commit, and nothing is left uncommitted.
- The fault that could treat a right answer as wrong is fixed, and the founder confirmed it live after the first of the night's pushes.

## Key Reflections
- **Work that is written down survives being stopped.** A crash and a cut-off cost no jobs, because every agent's first instruction was to write as it went and every brief said how to carry on.
- **A gate must be able to fail the way production fails.** Mine ran against a database the host does not have, so it passed a commit the host could not build. The gate now runs the host's step the host's way.
- **Measure the cost of a fix before shipping it, and say it out loud.** The engine change removed nearly every case it was built for and, as first built, made something else worse. It shipped only after that was measured, reduced, and put to the founder as a cost.
- **Do not ship what cannot be seen working.** A behaviour was built well and tested well and never ran in the product. Taking it out was the better engineering.
- **Being corrected is the system working.** Three of my own assumptions were wrong today. Each was caught because a second agent was told to prove the claim, not to agree with it.
