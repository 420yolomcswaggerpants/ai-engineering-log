# Day 54 Progress: Every Session Pinned to Its Version, Two Phone Fixes, a Table Wrong Since It Was Written

## What I Did Today

### Study and Review
- Continued daily concept and vocabulary study, as always.

### Done

**The whole queued wave at once, then three more rounds.**
- **Six agents at a time, the cap at seven,** each job in its own folder with a brief on disk, a report, a supervisor's or reviewer's report and a commit message; four sessions on the day, after one commit the evening before. Every job read its brief and the shared rules from files, so a cut-off run could be continued from disk alone.
- **The agent harness changed under us:** agents of every kind were at times refused when they tried to write their report files, and handed the text back instead. I saved every hand-back to disk verbatim before anything else; by the evening the refusals were rare again, but every brief now says what to do when it happens.

**A play session now keeps the numbers it began under.**
- **Three phases, all shipped today:** the content numbers, then the grouping rules behind the learning content, then the engine numbers. Each session records its configuration version and runs under that version to the end, so a later release can change a number without changing a session already begun. The account's own settings keep reading the newest.
- **The new configuration version is the old one under a new name,** so nothing moved. A test that had passed only because every read took the newest version was corrected, and a new file of ten tests was added, nine of which fail when the pin is forced off.

**Learning content: items made fairer, and a table that was wrong.**
- **Some items were made harder to win by guessing,** switched on item by item after a measurement of 4,500 draws each: one item first, then two dozen more, then three of the six items over one data table. Three others were left off because the measurement showed the change would have made those items easier to guess.
- **A data table behind six items had fifteen cells wrong and three more doubtful since it was written,** so some items could misjudge a learner's answer. An author's measurement found it, a reviewer confirmed it, and a second reviewer checked the corrected table by recomputing every cell from the drawn picture itself. Every item over the table was measured again.
- **Six items that named more than they showed** now name only what they show. Three items now write their answer in the same form as the item itself. Feedback on the youngest learners' typed answers was restored where it had gone missing, on 27 answers.
- **Teaching examples can no longer give away an item's answer,** measured over more than a million draws with no real loss of coverage.
- **The youngest learners' pictures gained new layouts,** with the mix chosen from measured options.

**Two phone-size fixes, found in a browser.**
- **A touch tool on a small phone** now fits whole, with targets big enough for a thumb. A QA agent walked it at 320 and 375 pixels; a supervisor corrected the builder's measurement (it had measured the box, not its content), and the fix was checked in the browser twice.
- **The AI feature's panel shrank to a line under a tall tool** on a small phone, a finding from the same QA pass. It now keeps a minimum height and the tool scrolls under it.

**Housekeeping that mattered.**
- **A moderate advisory in a development tool's dependency,** closed the same day; nothing that ships to a family changed.
- **A document reader's 28 findings checked:** 17 held, and the 11 that needed a change were applied. The engine item carried from the last note was measured first and the existing rule kept. The builder's supervisor moved to the mid-size model after a usage review put it at 40% of the week's usage.
- **15 commits, all pushed,** six pushes, each code push after a full check run; the host's build and CI are green for the last one.
- No schema change.

### Decided
- **The whole queued wave at once,** then every follow-up round on my word, one question at a time with options.
- **Pin a play session to its configuration version:** content numbers first, the grouping rules and the engine numbers later the same day; the new version equal to the old.
- **Make items harder to win by guessing on one item first,** then on the two dozen that measured clean, and on only three of the six over the corrected table: measure the guessing learner, not only the working one.
- **The pictures' new layouts:** chosen from measured options, with the youngest kept on the simplest one.
- **The panel keeps a minimum height** and the tool scrolls under it.
- **The builder's supervisor runs on the cheaper model;** at most seven agents at a time, the lead on the top model only.
- **Close every unused background task** at a session's close: servers, browsers, worktrees, the database container.
- **Two content findings queued rather than rushed,** each to be measured first.

### Noticed
- **A test passed for the wrong reason.** A test forged an older configuration version and still passed, because every read took the newest. Once the pin was real it failed, and was corrected.
- **A table nobody had re-derived was wrong for weeks.** Fifteen cells false and three doubtful, since the day they were authored, under six items. A measurement found it; a reviewer who recomputed every cell from the drawing proved the fix.
- **A change that helped most items would have hurt three.** On some items the change made guessing easier, not harder. Measured per item before the switch, those three stayed off.
- **An author's shortcut is not content.** One author took a shortcut to satisfy a check; the lead replaced it with one honest sentence. Another explained a change as "grading unchanged" without counting; the reviewer counted.
- **Agents again wrote progress times from memory, or none at all.** Git is the source for times.
- **Small tooling traps, each costing time:** a long shell here-document with nested quotes wrote nothing; removing a worktree on Windows leaves an empty folder behind; the change history's recent half runs newest first, so a new entry goes above the last one, not below.
- **The agent harness can keep a finished agent listed as running.** Two were found still listed after their reports were in. The close-out now lists and stops them before "safe to clear".

## Numbers
- 2,397 automated tests across 206 files (from 2,294 across 198); green on a quiet machine before the last push
- 15 commits, 83 files, +3,839 / −492 lines
- Content items unchanged at 1,622; every item checked again under the new version, identical on a sample and by the file itself
- No schema change; 61 tables, 53 migrations
- Product document 1.24 to 1.26, technical document 1.04 to 1.07, essentials 0.3 to 0.5
- Six pushes; five full check runs, one of which flagged the development-tool advisory, closed the same day
- Six agents at a time, four sessions

## Next
- The two queued content findings, measured first, then my word.
- A security review and a browser pass of today's changes, and a documents pass from two readers.
- The open device checks, the playtest sheet and the company paperwork.

## Current Status
- All 15 commits are pushed; the host's build and CI are green for the last push.
- Every play session now runs under the configuration version it recorded; the new version equals the old, so the version change itself changes nothing a family sees.

## Key Reflections
- **Pin a session to its version.** A release must never change a session already begun. Recording the version was not enough; nothing read it back. Now the reads that play a session go through the version it recorded, and a few account-level reads stay on the newest by rule.
- **Recompute from the source, not the table.** A table that looks authoritative is still a claim. The reviewer who derived every cell again from the drawing is the one who proved it right.
- **Measure the guesser too.** A change that makes an item harder for a working learner can make it easier for a guessing one. Both have to be measured before a switch goes on, item by item.
- **A hand-back is a file, not a chat message.** When the harness refused report files, the work survived only because every report was saved to disk before anything else. Every brief says so first.
