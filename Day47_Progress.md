# Day 47 Progress: Security Fixes Shipped, Every Year Level's Examples Finished, The Hit That Lands, Small Fixes Before the First Family

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

**The security pass, closed.**
- **The second half of the pass ran:** a review of the code and configuration, then a stronger reviewer that corrected it and reproduced two findings live. Nothing critical, high or medium.
- **One plan fixed everything both halves found,** sixteen items, built by one agent and checked by a stronger one. One finding needed a product decision, and I made it.
- **A scoped review on a running copy said ship with notes.** Every fix held, and the two small notes were accepted in writing in the technical document.
- **Shipped, then checked live after the deploy.** The privacy text went into the packet kept for a lawyer.

**Every year level's worked examples are now step by step.**
- **The last five year levels and the foundation material below them were finished:** 1,035 steps across 527 examples.
- **A stronger model reviewed each year level cold and corrected 120 examples,** most of them a step that gave its own answer away. I fixed a few more myself where something was simply wrong.
- **The review script came back clean on examples the reviewers then had to fix.** It checks the structure, not what an example actually shows, so a reviewer still has to look.
- **The plan had missed one group of examples entirely.** I found it while checking the finished work, and it was done the same day.

**Agents now have to prove their brief was done.**
- **Every agent's report ends with a table:** each thing it was asked to do, whether it was done, and the evidence from the run. The supervisor confirms each row, and I accept nothing without the table and one row checked on disk.
- **Twenty-eight instruction files changed,** almost all regenerated from one source so no agent's rules drift from the others'.

**The hit that lands, and the video re-cut with it.**
- **My own note on the second video was that a hit felt lackluster.** The sound had played when the move started, not when it landed, and it was a pickup blip rather than an impact. Now it plays on the impact, it is a crack with a low thump under it, and I chose it by ear from three candidates on the local copy.
- **The scene jolts and a few bits fly, and nothing else on the page moves under the hit.** Two things used to shift the page a moment later; both were held back until the hit had played.
- **The number that appears with a hit is sized against the scene,** so it reads the same on a phone and a desktop, and on a phone the scene now stays on screen while the learner scrolls to the answer area.
- **Under reduced motion the number had been invisible for weeks.** Every test said it was present; a browser measuring its opacity said it was not. Fixed, with a test that measures.
- **The 30-second video was re-cut on the new build:** every sound cue placed on the frame it belongs to (the recorder's timing drifts, so each cue was read from the frames rather than from one factor), one push-in on the last hit, and the invitation for families on the end card. I chose it over the first cut.

**Small fixes before the first family, in one commit.**
- **Ten decisions in the session, each the recommended option.** Seven from the open-items sweep and three from what the builders measured on the way.
- **For the youngest learners:** the offer of help after a mistake now sits right under the scene instead of below the fold on a desktop; on a phone the header stays one line once the running score joins it, which puts the answer area back at the fold on a standard phone (still below it on the two shortest sizes, where the scene stays in view while the learner scrolls); and when the tallest learning picture opens on the smallest phone the scene keeps at least its top row, where it had been cut to two pixels.
- **For everyone:** larger text no longer makes the scene's cards crowd the figures; a parent playing their child's level keeps keyboard focus on each new question instead of tabbing back in; and the one scroll that remains after a mistake is capped on wide screens so the scene never leaves view.
- **Operations:** the production database role now has a statement timeout, the readiness item found unset, and the migration runner lifts it for itself; the support script that prints a child's sessions honours the same scope as the metrics report, so an operator's own account stays out of a round's view; the half-hourly uptime check now plays the public try-out round end to end instead of only loading a page; and the second racing test got the same fix as the first.
- **Two builders worked in parallel on disjoint files,** each with its own supervisor afterwards. The supervisors earned their keep: one caught an import the tests forbid and a cleanup race that could delete the new test rows mid-run; the other caught a flash on page load, a floor that could have cut a picture off the screen, and a label that had vanished for screen readers.
- **The reply-time sentence for weekends** went into the testers' note and the welcome email, the last words item from the readiness list.

**Getting ready for the first families.**
- **A flaky test was fixed at its cause, twice.** It counted something across the whole test database while other test files changed it; both tests in that file now work in their own isolated slice.
- **The readiness list was turned into exact steps:** six things only I can do in the providers' consoles, each with where to click, then the checks that need a person present.
- **The AI feature's real cost was measured for the first time.** Caching works: a repeat call costs about a tenth of the first.
- **The daily clean-up job was confirmed running on schedule in production,** and a systems check from outside found the live site healthy: every public page answering, every security header present, no server errors in a day, no known dependency vulnerabilities.
- **A command in the readiness notes would have changed production just to read a date.** I replaced it with one that only reads.

**Verification and deployment.**
- Thirteen commits, all pushed. No schema change.
- Product document 1.03 to 1.06, technical document 0.82 to 0.85.

### Decided
- **Content commits no longer wait for me** when the full check is green and the stronger reviewer has passed. Code still does.
- **Fix the test, not the symptom.** I committed the content with the flaky test named in the messages, then fixed the test itself the same day.
- **Fix only what is wrong.** Where an example showed something early but every step still asked its own question, I left it.
- **The restore drill waits for a day I can sit through it.** It needs me at the console, not an agent.
- **Keep the scene on screen over everything else that moves.** Where a scroll after a mistake is by design, it is capped at the scene's top; where a picture and the scene's top row cannot both fit, the picture wins and the guide's words give way, since they are read aloud there anyway.
- **Three asks for the parent area go to a design session, not into today's build:** fewer second-step prompts on a known device, a clearer account menu, and a tab listing what the child is studying in order with their progress. Each touches a rule, so each gets options first.

### Noticed
- **A clean script is not a clean review.** It passed what three reviewers each found 14 to 22 problems in.
- **Heavy jobs starve each other.** The full check, run while agents ran the content checker, timed out in 45 tests that pass on a quiet machine. Today's answer: two builders at once, neither running the full check, and one run by me after both.
- **A pointer a new session can't follow is a bug.** "Line 6" of a list meant a table row, and a fresh session could not tell which. Every pointer now names a row and its title.
- **An agent's summary can claim more than it built.** A release message described changes that were not in the diff, and I rewrote it before committing.
- **A checklist item can be ticked in a plan and still not be true in production.** Reading the live setting is what showed it.
- **A test that reads a file as text breaks when the file changes shape,** and nobody runs it unless the brief names it. The one test the full check failed today was that; the fix list for a brief now includes every test that reads a changed file.
- **"Wholly in view" depends on what was on the screen.** A shorter prompt is drawn larger and moved the answer area six pixels past the fold. The supervisor's own measurement settled it, not the builder's number.
- **A setting changed on a database role reaches pooled connections only when they are recycled.** The live check read the old value for twenty minutes.

## Numbers
- 1,966 automated tests across 175 files (from 1,894 across 172); green twice in a row with no agent running
- 13 commits since the last note, 161 files, +9,425 / −1,744 lines
- 0 schema changes; 60 tables, 52 migrations
- Product document 1.03 to 1.06, technical document 0.82 to 0.85
- Content unchanged at 241 concepts and 173 levels

## Next
- A design session on the three parent-area asks, with options and the security reviewer's view.
- The content corrections that were measured but not yet decided, then the remaining metrics cuts.
- My console steps: spending limits, the hosting plan, alerts reaching my phone, the database and CI figures.
- A check on a real phone and tablet, the company formed, then the first posts.

## Current Status
- Everything planned for the prototype is built, the security pass is closed, every year level's examples are step by step, and the hit lands.
- What's left before the first families is mostly mine: console settings, a real-device check and the company.

## Key Reflections
- **Make agents show their work, not describe it.** A report with a row and evidence for each part of the brief turns "done" into something I can check in a minute.
- **Tools find the same things every time; reviewers find the rest.** The script passed over a hundred examples the reviewers had to fix, and a supervisor's own measurement caught what a builder's number hid.
- **Read the real setting, not the checklist.** Production said what the plan only assumed, twice today.
- **Write for the session that comes after you.** A pointer only works if a fresh session with no memory can follow it.
- **Feel is measured too.** A sound on the wrong frame, a number nobody could see under reduced motion, a page that shifted under a hit: each was a number once someone looked for it.
