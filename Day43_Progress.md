# Day 43 Progress: A Company of Agents, the Paperwork Tightened, Ready to Recruit

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

**The team, as agents.**
- **Twelve roles a small company has while it tests a prototype,** each an agent definition in the repository: engineer, QA, security, release, operations, product analyst, tester support, recruiting, marketing, learning design, compliance, fundraising writing. Each has the same shape: inputs, jobs named exactly as they are called with an output path and a done-when, the role's rules, the rules every agent holds, and a four-part report.
- **Every worker has a supervisor.** The worker runs on a cheaper model; the supervisor, on a stronger one, runs after it over its output: checks every claim against its source, fixes the files in place, deepens what the worker stopped short of, and ends with a verdict. Nothing reaches me before its supervisor has read it, and I check the supervisor's work myself, in the session, before I act on it: three passes, the last one mine.
- **Tools restricted per role,** so "sends nothing" is a fact of the tool list rather than a promise: the recruiter can read the testing mailbox and create drafts but has no tool that sends; the report-writers cannot edit code.
- **One source file renders all of them,** so a role changes in one place, and the definitions live in the repository, where a cloud session gets them too.
- **A plan that fits the weekly usage limit:** one worker and one supervisor per job by default; parallel workers only split by scope, and only for the coverage roles at a release gate; every agent keeps its context small and stops when the job's done-when is met; after ten runs of a role, the count of what its supervisor had to fix decides whether it ever gets a second worker.

**The recruiting agents narrowed** to the jobs that move one number: families who have agreed to start together. Five jobs for the recruiter (the inbox pass, three posts a week, the referral ask, the weekly report, the start day) and three for the marketing side (the message house, channel copy on request, the weekly read). Planning assumptions written down, to be replaced by measured rates after two weeks of posting; a holding email so nobody goes cold if gathering runs long; who is worth a draft and who is not.

**The paperwork, tightened as far as it goes without counsel,** after I decided to start the round without a lawyer and to seek one before the next stage:
- The privacy notice now says plainly that play is counted across all learners, never about one child, to see whether the product works; the old wording said less than the truth.
- The terms now say an account holder is an adult and the parent or guardian of each child added, limit liability to what was paid, name the state whose law applies, and say how changes are announced. The sign-up box says the same.
- An unused account is deleted after a year, with a notice a month before, where the default had been two years.
- A packet for a lawyer assembled anyway, with the nine questions in order of consequence, for the day it is needed.
- The operator will be a company, formed through a registered agent and a virtual mailbox so that neither a home address nor a personal name is on the public record; the page for families names the maker as I choose to be known, never by the company's legal name.

**Verification and deployment.**
- Six commits, all pushed and live. No schema change.
- Product document 0.93 to 0.94, technical document 0.72 to 0.73.

### Decided
- **Workers on the cheaper model, supervisors on the stronger one, and the third pass is mine,** in the session, never another agent.
- **One agent per job by default.** More agents mean more for me to read, and my reading time is the scarce resource.
- **No lawyer for the test round;** a review before the next stage.
- **A year, not two,** before an unused account is deleted.
- **The company's name is not the product's name,** so the product can be renamed without touching the company.
- **No neighborhood social network** in the channel plan; the next channel down the list instead.

### Noticed
- **The agents' first drafts came in five different shapes.** Only when every role had the same skeleton did the gaps show: jobs without a done-when, rules that were promises rather than tool lists.
- **"Sends nothing" is only true if the tool is missing.** A rule in a prompt is a request; a tool list is a fact.
- **Read the public record before filing.** Every address box on a state form is public; the question is not whether to form a company but where each box points.
- **Shell quoting ate apostrophes twice.** Edits made through a shell with the wrong quoting left escape sequences in two documents; a direct check caught them before they were pushed.
- **A test shared a counter with another file's cleanup** and failed once in the full run, then passed alone and in the rerun. Shared state between test files is a flake waiting to happen.
- **The database container had stopped** after a restart of the machine, and a run with a third of the tests skipped would have looked green. Check what ran, not just the result.

## Numbers
- 1,507 automated tests across 157 files, all green (unchanged)
- 6 commits since the last note, 45 files, +1,636 / −41 lines
- 27 agent definitions: 12 workers, 12 supervisors, 3 older ones
- No schema change; 59 tables, 49 migrations
- Product document 0.93 to 0.94, technical document 0.72 to 0.73

## Next
- Form the company through the agent and mailbox service, then set the operator's details on the host.
- Reconnect the testing mailbox.
- The message house, then the first three posts.
- The first emails to families once the privacy page shows the company, the address and the phone.

## Current Status
- The product is ready for strangers, the team to run the round exists as agents with supervisors, and the paperwork is as tight as it gets without counsel.
- Gathering starts the moment the mailbox is reconnected; nothing goes to a family before the page is complete.

## Key Reflections
- **Make the rule a tool list.** The cheapest way to make an agent unable to do something is not to give it the tool.
- **One source, many renderings.** Twenty-four files kept in step by hand would have drifted within a week.
- **Decide the budget before the first run.** The plan for what runs when, and what runs only at a gate, costs nothing now and everything later.
- **The scarce resource is my reading time.** Every design choice today was really about that.
