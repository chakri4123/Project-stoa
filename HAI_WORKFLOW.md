# HAI Task Workflow (screen by screen)

HAI = Handshake AI, where the task, form, QC and pay live. Timer: 65 min paid (up to 75 counted). Language: Telugu conversation, everything Chakri writes in the form is English.

Rule from the form: **do not submit the Hatch session until the HAI values are in and QC passes.**

## Screens in order

| # | Screen | What to enter |
|---|---|---|
| 1 | Welcome / Start task | Click **Start task** before opening Hatch |
| 2 | Important: do not submit Hatch until QC passes (text box) | `Okay` |
| 3 | Important 2: do not submit a Hatch that ended mid-annotation | `Okay` |
| 4 | Your universes / multilingual update | `agree` |
| 5 | Hatch setup check (4 boxes) | Tick Mode, Name, Universe, Protocol (only if all really match) |
| 6 | Quick persona navigation | Continue |
| 7 | Select your Hatch persona | Type the current locale (now `English (India)`), pick the same persona as Hatch (now Aishwarya Kamath). Never "No universe" |
| 8 | Use case category | Category of the goal (see WRITING_AND_SCORING.md). Never Personal Productivity. New one each task |
| 9 | Remember to click "start annotation" (text box) | `Okay` |
| 10 | Apps utilized | Only apps the arms actually called (A + B together), from the Trace |
| 11 | Session name | `85a353883201_task_N` |
| 12 | Session ID | UUID from Hatch top bar |
| 13 | Task prompt | The exact prompt sent, word for word |
| 14 | How the prompt relates to the universe (2 to 4 sentences, English) | Claude's ready text |
| 15 | Response A / Response B transcripts | Copy from the correct arm, no edits, no summary |
| 16 | Trace A / Trace B | Each arm's own Copy trace button. Paste full, no edits |
| 17 | Preference calibration | Continue / `Okay` |
| 18 | Dimension reminders | Continue / `Okay` |
| 19 | Tie audit | Tick "I understand that TIE is only if two responses are IDENTICAL" |
| 20 | Longer is not better | Tick "I understand — longer ≠ better" |
| 21 | No tie for overall preference (text box) | `Okay` |
| 22 | Preference | Same as Hatch (A/B significantly/slightly better) |
| 23 | Absolute quality | Same as Hatch (Perfect / Good / Bad) |
| 24 | Score each dimension | All 8, same as Hatch |
| 25 | Required rationale | Same text as Hatch, word for word |
| 26 | Notes | `None`, or the real issue in plain English |
| 27 | **Screenshot 1** | 1 to 2 images: Arm A and Arm B replies, readable |
| 28 | **Screenshot scoring panel** | 1 to 5 images: Preference, Absolute quality, 8 dimensions, rationale, all filled |
| 29 | Run QC | Fix every red check (see below), rerun until green |
| 30 | (Hatch) | Submit preference, then End comparison |
| 31 | **Confirmed screenshot** | Exactly 1 image: Hatch Home > Annotations > Preference, row with name + UUID + COMPLETED (crop model names) |
| 32 | Confirm Hatch Session ID | UUID again |
| 33 | QC passed + not "Ended mid-annotation" confirmation | `Okay. The Quality Checks were checked and passed, and the Hatch session does not say "Ended mid-annotation". It shows Completed with session ID <UUID>.` (only if true) |
| 34 | Submit | Submit the HAI task |

Order of screens can change a little between task versions. Follow the form, use this table for the answers.

## Final handover checklist (Claude gives ALL of these together every task)
Session name, Session ID, Persona, Category, Apps utilized, Task prompt, 2-4 sentence universe explanation, Preference, Absolute quality, 8 scores, Required rationale, Notes (real issue or None), Confirm Session ID, QC confirmation text, and a reminder of the 3 screenshots.

Before every handover: reload that task's Hatch page and read back the session ID, prompt, 9 saved values, Absolute quality and rationale, so no info from another task gets mixed in. Start the handover with a short "Cross-check" note: what was checked against Hatch, that the prompt and apps are unique versus all other tasks in the log, and that the prompt (persona style), universe explanation and rationale (Chakri style) follow the guide and the md files.

## Known QC errors and fixes
| Check | Meaning | Fix |
|---|---|---|
| AR-10 Trade-off Check | A dimension points to the other arm than the Preference, and the rationale does not explain why | Add one sentence naming that dimension exactly: "Despite A winning Coherence & writing quality, B is still the overall pick, because ..." Clear the old text before pasting |

## Do not
- Do not reuse a similar or paraphrased prompt from earlier tasks.
- Do not change the prompt after it was sent to Hatch (HAI must match word for word).
- Do not put values in HAI that differ from Hatch.
- Do not tick a confirmation that is not true.
