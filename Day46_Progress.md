# Day 46 Progress: A Build Stage Shipped, a Second Full QA Pass, a Security Rerun

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

**The third stage of the help redesign, built and shipped.**
- **My own testing changed the plan first.** I used the product the way a family would and wrote down six things to change, from the audio to how steps are shown. They went into the stage's blueprint before anything was built, and a review pass the next day corrected parts of the blueprint that no longer matched the code.
- **A stronger reviewer caught four real defects the builder had missed,** and a QA walk afterwards found nothing blocking. I made one layout call during the walk, and it shipped with the stage.

**A second full QA pass, this time over the main experience.**
- **Two QA agents walked it at three screen sizes, one of them on a throttled phone, and a stronger reviewer merged their reports.** 19 findings: 2 blocking, 8 annoying, 9 cosmetic. One blocking finding was a number shown to the learner that was wrong in some situations; the other was something opening out of view on a phone.
- **Fixed in two rounds and re-walked after each.** The first re-walk found a new problem on desktop, caused by the browser's own scrolling behaviour. I accepted a few limits on the smallest screens and put them on the real-device checklist.
- **One QA agent ended every Node process on the machine,** which took down the server the other agent was using. That is now a written rule in every QA brief.

**Measurement for the first round.**
- **The tools that read the round can now leave out every account that is not part of it,** mine included, so a figure never mixes testers with the people building the product.
- **One family setting now keeps its own history,** written by the database itself rather than by application code, so the record cannot depend on someone remembering to call a helper.
- **The reviewer found two places where left-out accounts still reached a figure.** Both were fixed, and a test now walks the whole schema so a new table cannot slip past.
- **A compliance pass followed:** the privacy page's date moved, and a question about very small groups in the reports went on the list for a lawyer.

**An outside service evaluated, then shelved.**
- **Vendors for one feature were researched from their own terms pages.** One forbids products for children, and the only free tier would have covered a couple of heavy users a day.
- **I shelved it to stop delaying the release.** The full plan stays on disk for later, and the feature keeps using what the device already provides.

**The security rerun, before anyone I don't know uses the product.**
- **Three agents attacked a local copy, each from a different angle, and a stronger reviewer merged their reports and reproduced every finding itself.**
- **The two checks that would block the round both held:** one family can never see another family's data, and deleting an account leaves nothing behind that points to a person. The second was confirmed again with an independent count over every table.
- **Nothing critical or high.** The fixes are planned for the next session, after the second half of the pass.
- **A mistake during the pass:** a test run started in the middle of it deleted the pass's test accounts, because they used a name prefix the test suite already owns. The probes were finished by then, and the rule is now written down.
- **The open questions were settled with the reasons written beside each,** and turned into a fix plan.

**Content and marketing.**
- **Another year level's worked examples became step by step:** 149 steps across 74 examples. A stronger model reviewed every one and corrected twenty.
- **A first short video:** silent stills with captions, then a second version built from real footage of a local copy with a made-up family and the product's own sound. Captions stay in both, for feeds that start muted.

**Verification and deployment.**
- Four commits, all pushed. One schema change: a new table.
- Product document 1.00 to 1.03, technical document 0.79 to 0.82.

### Decided
- **Stop waiting on the outside service.** The release has waited long enough, and what the device provides is good enough for the first round.
- **No limit gets set without data to set it from.** Where one would need a number nobody has measured, it waits for the round's data, with the reason written down.
- **Run the security pass on the development server** when the production build refuses to start against a local database. The production-only behaviour was read in the code instead.
- **Test accounts and operator accounts are left out of every figure,** not only the headline ones.

### Noticed
- **An estimate is not a measurement.** A builder said a change would free about a hundred pixels; measured, it freed three, and I undid it.
- **Shared names are shared state.** A test-account prefix collided with the test suite's own clean-up, and so did a test that counted every account while other test files ran.
- **A guard stopped a workaround, and it was right to.** The session had found a way around a production safety check to run the pass; the guard refused it, the question came to me instead, and the answer was simpler.
- **Real footage beat stills.** The first video was correct; moving footage with the product's own sound is what makes it worth watching.
- **A second reader keeps paying off.** In the build, the QA pass, the measurement work and the security pass, the reviewer found real problems the first agent had passed.

## Numbers
- 1,894 automated tests across 172 files, all green (from 1,754 across 167)
- 4 commits since the last note, 66 files, +6,296 / −558 lines
- 1 schema change; 60 tables, 52 migrations
- Product document 1.00 to 1.03, technical document 0.79 to 0.82

## Next
- The second half of the security pass (a review of the code and configuration), then one round of fixes for everything both halves found.
- The remaining year levels' worked examples, one session each.
- A check on a real phone and tablet, spending limits set, the company formed, then the first posts.

## Current Status
- The help redesign is complete, and both full QA passes are done, with every blocking finding fixed.
- The security rerun found nothing that blocks the round; its fixes are planned and come next.
- Testing opens once those fixes ship, the real-device check is done, and the company is formed.

## Key Reflections
- **Use the product before you plan its next stage.** Six problems from my own testing reshaped the stage before a line was built.
- **Measure before you trust a number,** whether it comes from an agent's estimate or from a summary of a config file.
- **Treat names as shared state.** A prefix or a global count in one place can quietly collide with something somewhere else.
- **When a guard says no, ask instead of looking for another way around it.**
