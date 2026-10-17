# Day 45 Progress: Getting Ready for the First Testers, a Full QA Pass, Privacy Records That End

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

**Five plans for the work that does not wait on the company being formed.**
- **Forming the company takes days, and it only blocks the first email to a family.** So I wrote five blueprints for everything else that has to be ready before testers arrive: the agent team fitted to a small first round, a full QA pass, the first marketing materials, every draft a tester will receive, and a security rerun. Each was settled with me in a thinking session and then carried out in its own execution session.
- **The agent team was refitted for the round in one commit.** The roles are written once in a single file and rendered into 25 agent files, and I read the whole diff before keeping it.
- **Four planning documents for the round:** the questions an investor is likely to ask, with honest answers; what operations has to have in place on day one; a sheet for observing a supervised test session; and a measurement plan whose pass and fail thresholds were fixed before any data exists. I took all 25 of the recommendations they raised.

**A full QA pass of everything a family sees outside the main experience.**
- **Two QA agents walked it at three screen sizes, and a stronger reviewer merged their reports.** 22 findings: 1 blocking, 12 annoying, 9 cosmetic. The blocking one was a family account with no learner on it that could not reach its own account settings, so it could not delete itself.
- **The reviewer found what both workers missed:** one learner's result was being shown to every learner in the family, not just the one it belonged to.
- **19 fixes were built, checked and re-walked on a phone.** Two findings I accepted as they are, and wrote down where to recheck them on real devices.

**First marketing materials.**
- **A brand sheet, a message guide, nine graphics and a landing page draft,** all made from screenshots of a local copy with a made-up family, never real accounts.
- **A shared link to the site now shows a picture** instead of a plain text card.
- **Every recruiting draft was rewritten** to match how the round actually admits families now. The posts, the replies and the help page had drifted from the live privacy page, and one pass caught them all.

**Privacy and records.**
- **Writing the marketing copy exposed a gap:** the privacy page described a step the round no longer uses. The page, the product document and the compliance documents were rewritten to say what actually happens, and a lawyer's question list was kept in step.
- **One kind of record had no deletion date.** It now has one, the privacy page lists it, and the nightly cleanup enforces it.
- **The builder stopped itself before shipping a change that would have quietly made things worse for a family later.** I had written that condition into its brief. I chose a fix that keeps the family's experience the same, and it shipped the same night with a test through the real request path.
- **The records now say what actually happened** instead of reusing an older label.

**Verification and deployment.**
- Seven commits, all pushed. One schema change: a column added and a constraint removed.
- Product document 0.98 to 1.00, technical document 0.77 to 0.79.

### Decided
- **Do everything that does not need the company now,** so the first tester is not waiting on preparation once it is formed.
- **Thresholds before data.** What counts as the round working was fixed before anyone plays.
- **No strong-model supervisor on low-risk work** like design and drafts, where I check it myself. Supervisors stay on code, compliance, security, QA and content.
- **Every kind of record gets an end,** enforced by a scheduled job rather than by someone remembering.
- **When a cleanup would change what a family sees, change the data model, not the family's experience.**

### Noticed
- **Writing for parents tested the privacy page better than reading it did.** The first time the copy had to say plainly how a family joins, it no longer matched the page.
- **Workers and reviewers find different things.** In both the QA pass and the planning work, the second reader caught errors of meaning, such as a count of households read as a count of people, that the first had passed.
- **A stop condition in a brief is worth writing.** The builder found the problem exactly where the brief said to look, and stopped instead of choosing for me.
- **A worker's claim about deployment was wrong, and the reviewer checked the build file.** The production build already applies schema changes before the new code serves. Read the config instead of trusting a summary of it.
- **Supervisors on every job cost more than they returned on low-risk work.** One session ran about nineteen agent runs. The rule changed the same day.

## Numbers
- 1,754 automated tests across 167 files, all green (from 1,713 across 165)
- 7 commits since the last note, 86 files, +1,648 / −328 lines
- 1 schema change; 59 tables, 51 migrations
- Product document 0.98 to 1.00, technical document 0.77 to 0.79

## Next
- The third stage of the help redesign, already blueprinted.
- The remaining year levels' interactive steps, one session each.
- After that: a second QA pass over the main experience, a video, and a security rerun.
- Form the company, then the first posts.

## Current Status
- Everything for the first round that does not depend on the company is drafted or built: the agent team, the plans, the marketing materials, the replies, and the privacy records.
- Testing opens once the third stage of the help redesign is built and the company is formed.

## Key Reflections
- **Use waiting time for the work that doesn't wait.** The company being formed blocks one email, not the preparation behind it.
- **Write the stop condition into the brief.** An agent that knows when to stop hands the decision back instead of making it.
- **Saying something plainly is a test of it.** Drafting what a parent reads found the gap that rereading the policy had not.
- **Match the oversight to the risk.** A second strong reviewer earns its cost on code and privacy work, and on design drafts my own read is enough.
