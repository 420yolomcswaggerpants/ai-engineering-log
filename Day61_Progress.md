# Day 61 Progress: Three Days, Three Rounds and Twenty-Eight Commits, Second Readers Who Corrected the Figures I Had Shown, and a Release Check Run the Morning After

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

**This note covers three working days, 14 to 16 November: five sessions, three rounds of work, three pushes, twenty-eight commits.** The founder asked for the note to wait on 14 and 15 November, so both days are here.

**Settled from the last note:** the founder confirmed that note's push live, kept the two harder choices it had left with him, and kept his own rule for the engine round.

**14 November, one afternoon session (about 12:50 to 17:00), one push of eight commits.**
- **The round the last note promised:** the wording fix the reviews had flagged went out in the first wave, and the engine question was measured before anything was built. Up to seven agents ran at a time, each from a brief written to disk before it started; every content change was read by an Opus reviewer and every code change by a supervisor before it reached the founder.
- **Committed:** three content changes, four code changes and the documents. The code: an accessibility wording fix; a punctuation fix in one learner-facing sentence; a fix to how an assessment picks its items; and one engine option built switched off, proven identical to the old behaviour while it is off.
- **One cure I had decided on was built, failed its review and was taken out again.** The review showed it did not do what I had said it would; the log says the decision was mine and wrong.
- **Several lanes measured a pattern and left it,** because the only cure found would have been harder on a struggling learner or less true to how learners think. Each is recorded with its figures.
- The founder answered six waiting questions with "go with your recommendations", said "commit" three times and "push" once, after one green release check.

**15 November, overnight to mid-afternoon (two sessions from about 01:20), one push of ten commits.**
- **The founder confirmed the previous push green and live and started the whole queued round.** Seven agents went out at once: one tidy-up of duplicated code and six measures.
- **Two lanes showed that a premise I had carried was wrong.** Both were closed with nothing built, and the documents now say why.
- **A test pass in a real browser at phone sizes led to two faults being found in the live product,** both on a phone held on its side, neither stopping play. A builder fixed both the same morning; a supervisor served the old and the new version side by side in one browser and confirmed the fixes at every size, adding tests of its own.
- **A wording pass on sentences a learner hears:** forty strings in thirteen files, two of which had not always been true.
- **Seven help examples were moved** so that none of them gives away an item beside it.
- **A second engine option was built switched off.** Its supervisor found that the build did one step in a different order from the variant that had been measured and decided; the build was changed to match what was measured.
- **One choice that is harder on a struggling learner in a narrow set of cases was the founder's alone:** he was shown three alternatives with exact counts, chose one, and it went in as its own commit only after a reviewer's recount matched the count he had been shown.
- The documents went to the next version, the release check was green, and the ten commits were pushed at 15:22.

**15 November, evening (about 17:20 to 23:40, one session), ten commits, not pushed that night.**
- **The founder chose "the whole queue" again.** Thirteen lanes ran, nine queued and four added on the way; four measured and were closed with nothing built.
- **Built and committed, each on the founder's word:** five content changes, one test that pins behaviour no test had pinned, an engine limit raised to close a rare edge case, a display fix for small screens, and the content checker widened to cover more of what a learner can be shown.
- **Three times that evening an Opus reviewer found a stronger pattern than the table the founder had already chosen from.** Each time the commit was held, he was asked again with the corrected figures, and each time he kept his choice.
- The founder closed the day at 23:38. My full check on the finished tree had only started; it was stopped and counts for nothing.

**16 November (from about 06:40).**
- The session started from the files alone and confirmed the state: ten commits ahead of the host, nothing gated, nothing running.
- On the founder's word: the container runtime was started, the full check went green on a quiet machine, and the release check with the security baseline went green in a clean copy at 07:07.
- The push waited for his word and went out at 15:58. He confirmed the host's build green and that commit live at 17:13.
- The next round was laid out from the documents' own list, with one reader agent collecting where each item is recorded. No lane in it has started.

### Decided
- **By the founder:** the two queued rounds of 15 November ("the whole queue", twice); every commit, by a typed word or by the question dialog; all three pushes; six questions on 14 November with "go with your recommendations"; three alternatives picked from tables on the evening of 15 November; three answers on the morning's display fixes and how far the evening's display fix reaches; two choices that are harder on a struggling learner in a narrow set of cases, each shown to him with its exact count, and a third, smaller one shown with its measured size; to close 15 November without the release check or the note.
- **By me, and logged with a reason:** on every other measured lane, which alternative was built and which was left; which lanes closed with nothing built; that a bare "commit" from him covers the reviewed work as built and never a harsher alternative, which is always put to him separately.
- **Left for the founder:** whether and when to switch on the two engine options, with the conditions they must meet first; two smaller engine questions; which lanes of the next round run.

### Noticed
- **A table I show the founder is only as good as the search behind it.** Three times in one evening I put figures to him before a reviewer had searched for the strongest pattern, and the reviewer then found it higher. From now on the reviewer's search comes before any table goes to him.
- **The author of a change scores its own new weakness too kindly.** The reviewer's recount is the figure that goes in the documents.
- **My own premises and figures were wrong at least nine times in three days.** Four would have changed what was built: two lanes that showed a premise of mine was wrong, one cure that did not cure, and one brief that said a change would move nothing when it did. A measure caught each of those four before anything shipped; authors and second readers corrected the rest.
- **One sentence I had given the founder, that a change was never harsher, had a narrow exception.** The supervisor found it; it was told to him plainly with the commit.
- **A supervisor changed a file in the shared working tree for a few minutes** while another lane was timing a run there. The rule now: a supervisor changes scratch copies only.
- **Clock times typed from memory drifted,** mine by minutes and two agents' by an hour. Every log line now reads the machine's clock first.
- **Some agents could not write their own report files.** I saved their hand-backs to disk as they arrived, and briefs now say the file is required and how to write it.
- **I launched one agent before its brief was on disk, and it stopped at once.** It was continued once the brief was there.
- **One session ended without writing its day log.** The next session rebuilt it from the round's progress file.
- **The question dialog is how the founder answers fastest,** as long as the reviewed figure is in the question itself. A dialog can also sit for hours: one sat about a hundred minutes and the push dialog nearly nine hours. Work that does not depend on the answer is started before the question is asked.

## Numbers
- 28 commits in the window, all pushed in three pushes (8 on 14 November, 10 on 15 November, 10 on 16 November): 66 files, +2,428 / −335 lines
- By kind: 14 to learning content (one of them a tidy-up that changes nothing a learner sees), 11 to code and tests, 3 to the documents
- 2,789 automated tests across 254 files, from 2,720 across 246; green on a quiet machine before the last push (the step with no database: 1,971 passed, the rest needing a database skipped)
- Content items unchanged at 1,647, every one checked by the content checker across 4,941,000 generated draws, 0 problems; the widened checker now makes about as many draws again, which that figure does not count
- No schema change: 61 tables and 53 migrations, as in the last note
- Product document 1.38 to 1.41, technical document 1.18 to 1.21, essentials unchanged at 0.5
- Security baseline held before each of the three pushes: 40 checks, 0 failed; baseline rows unchanged at 128
- Up to seven agents at a time; no usage-limit stop in the three days

## Next
- The founder: which lanes of the next round run; whether to switch on the two engine options; two smaller engine questions.
- The next round, as laid out: first the items the measures rank weakest, each measured again before anything is built, with the reviewer's search before any table reaches the founder.
- Still open from the last note: the package type check in the standing reviewer rules, and eight old folders on the desktop that wait on the founder's word.
- Still open from before: the device checks (with two more items from this round), the playtest sheet and the company paperwork.

## Current Status
- The main branch and the host's branch are the same commit, the founder has confirmed it live, nothing is uncommitted, and no agent is running.
- The day's work is closed: the container runtime and the database it served are shut down.

## Key Reflections
- **Ask for the strongest case against a figure before anyone chooses from it.** Three choices were made from tables that were too kind, and the tables were mine to check first. None was reversed, but each had to be asked twice.
- **A second reader with its own scripts is not a formality.** In three days the second readers found an untrue sentence of mine, a build that differed from what was measured, a cure that did not work and three tables that were too kind.
- **A stopped check proves nothing.** The run cut off at the close of 15 November had passed its first steps, and I wrote down that it counted for nothing; the morning after, the whole check ran again from the start.
- **Say whose decision it was.** A harsher alternative is never folded into a one-word "commit"; it goes to the founder as its own question with its own figures.
