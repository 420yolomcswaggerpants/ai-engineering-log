# Day 44 Progress: Help Redesigned From Inside, Steps a Learner Takes, Work That Survives a Cutoff

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

**Help, redesigned before anyone outside tests it.**
- **I decided testing waits until help stops taking a learner out of the main experience.** Until now, asking for help replaced what the learner was doing with a page of text, and the learners who most needed help were the ones least likely to read it. The redesign has five parts, built in three stages, and nothing ships to testers until all three are done.
- **Stage one: the AI feature gets a visible presence and stays alongside the main view** instead of covering it. It was built, then walked by QA at four screen sizes, and the phone layout was reworked the next morning: what stays in view, where keyboard focus goes, and how much room the help takes.
- **My own look on a phone found what the automated walk had passed.** The review page a learner reads before starting was still a wall of text, so it now goes one step at a time and can be worked by hand. Read-aloud is available at every year level instead of being hidden for older learners. An on-screen cue meant to show who was speaking went unnoticed until it carried a name. The help area can now be resized by the learner.
- **Stage two: a learner works through an example themselves instead of reading it.** Every answer is checked exactly by the server, never by the model, and the model is never told what the learner typed.
- **Every interactive step is checked at build time with exact arithmetic,** so a step whose stated result does not follow from its own working fails the build. The first year level's examples were converted and reviewed (about 250 steps), and the two youngest year levels tonight (176 more).
- **Reviewed before it shipped:** the new record the feature keeps was reviewed for privacy, and the public privacy page was updated the same day. A security probe of the new route found three issues, one medium and two low, all fixed first. QA at three sizes found two blocking phone problems, both fixed and re-measured.

**How the work runs now.**
- **Two kinds of session.** A thinking session on the strongest model writes a blueprint for a stage and settles every decision with me. An execution session on the next model down carries it out, reading only the files the blueprint names. The chat is cleared between stages.
- **Every agent run can be continued from files alone.** The brief is on disk before the agent starts, with a section on how to continue a cut-off run, and both the agent and I write progress as we go. The usage limit cut two runs short today, and both picked up from their files.
- **A review script feeds one strong reviewer per year level.** It pulls every interactive step of a year level into one file, with each step's arithmetic recomputed and suspicious patterns flagged. That makes 8 review runs for the remaining year levels instead of about 80.

**The testing round.** Testers now start the week they agree, instead of waiting for a shared start day.

**Two bugs I found this evening, fixed the same evening.**
- **A learner could not see a choice in place before applying it.** Now it is shown in place, with the button to apply it right there, and it can also be applied from the area it belongs to, where the result shows at once.
- **After a change, the browser's Back button showed the old state,** while Forward showed what was saved. Now both show what was saved.
- **Reproduced before fixing.** A browser script showed the old state coming back on the old code, then confirmed the fix at phone and desktop sizes.

**Verification and deployment.**
- Nine commits, all pushed and live. One schema change: two columns added to an existing table.
- Product document 0.94 to 0.98, technical document 0.73 to 0.77.

### Decided
- **No outside testers until all three stages of the help redesign are built.**
- **Thinking on the strongest model, execution on the next one down, and a blueprint in between.** A decision is made once, with me, and written down.
- **The server checks every step, never the model.** The model is told only whether a step was right, never what was typed.
- **Testers start when they say yes.** A family that agreed in the first week should not wait a month to begin.
- **One strong reviewer per year level, fed by a script,** instead of a weaker reviewer per file.
- **See it in place before applying it,** and apply it from where it belongs as well as from where it is chosen.

### Noticed
- **A cold reviewer found a pattern the plan never asked about.** In the youngest year level the right option was predictable from where it sat among the other options in most items. That check now runs on every year level, and both year levels done tonight pass it.
- **Read the code before writing a review rule.** The first year level's reviewers spent effort reordering options whose order the product already varies.
- **A lazily loaded component with no fallback suspended the whole page** on first open and lost keyboard focus. Every lazy load now has its own fallback, and a test fails on one without.
- **The automated walk passed things a person on a phone did not.** A layout can measure right and still read wrong.
- **The documentation said a refresh clears one page; the browser showed it clears them all.** A guard I had added for the other pages did nothing, and came out. Measure the framework, not its summary.
- **A script outside any package ran as the wrong module type** until renamed, because the runner guesses the module type from the nearest package.

## Numbers
- 1,713 automated tests across 165 files, all green (from 1,507 across 157)
- 9 commits since the last note, 144 files, +10,047 / −1,409 lines
- 1 schema change; 59 tables, 50 migrations
- Product document 0.94 to 0.98, technical document 0.73 to 0.77

## Next
- The remaining year levels' interactive steps, one execution session each.
- The third stage of the help redesign, already blueprinted.
- Form the company and reconnect the testing mailbox, then the first posts.

## Current Status
- Two of the three stages of the help redesign are live. The third is designed and waiting, and the remaining year levels' content follows the same plan.
- Testing opens once all three stages are built.

## Key Reflections
- **Decide once, on the best model, and write it down.** An execution session that never has to decide does not need the most capable model or a long chat.
- **Assume every run will be cut off.** Work that lives in files survives a limit, while work that lives in a chat does not.
- **Spend the strong reviewer on judgment, not on arithmetic.** A script recomputes; a reviewer decides whether a learner can follow it.
- **Reproduce the bug before fixing it.** The old code showed the bug on demand, so the fix could be shown to end it, and an unneeded part of the fix could be shown to do nothing.
- **A fresh reader finds what the plan forgot to ask.** The best finding today was one nobody had told the reviewer to look for.
