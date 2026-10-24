# Stoa: needs-attention alerts and mistakes (all accounts)

Shared by every Stoa account (Charan, Adarsh, Praneeth, anyone new). Read this before every task, together with `STOA_WORKFLOW.md`. Add each new form alert or mistake here with the account, task and fix. Octahedron QC errors stay in `NEEDS_FIXING.md`.

## Form "needs attention" alerts

### ST-L1 Prompt Language Compatibility (Charan, zh_sg, task 1, 2026-10-23)
- **Alert:** "Manual review needed" because the assigned prompt mixes Latin-script app names (ins, Notion, WhatsApp) into Chinese.
- **What we tried:** editing the prompt on the form (Instagram, then a version with no Latin letters). The alert stayed, and then added a new point: "assigned prompt and prompt_as_sent differ in substantive wording". Editing makes it worse.
- **Result:** the user could not submit with the alert showing and abandoned the session. Task 1 was restarted fresh.
- **Rule from now on:**
  1. Paste the given prompt into the form FIRST and run the form check BEFORE you create the Hatch session or send anything. Only go to Hatch once the form shows no needs-attention alert on the prompt.
  2. Do not reword the prompt to beat ST-L1. If the check flags the given prompt itself, ask in #stoa-tasking (or skip/release the task) before you spend Hatch time on it.

### ST-L1 again (Charan, zh_sg, task 8, 2026-10-24)
- **Alert:** "Manual review needed: verify whether substantive English-Chinese code-mixing (doc, polyclinic, calendar) is permitted". Reasoning said "Review alert only; no violation is established", but the form still BLOCKS: no submit, no next step.
- Restarting the session does not help: the same given prompt fires the same alert.
- Seen again on Charan's next Tengah/HDB prompt (English proper nouns HDB, Tengah). Even proper nouns trigger it.
- Task 11 (Tengah) was run anyway to test whether the form submits with ST-L1 showing. Result: COULD NOT SUBMIT, the form blocks with ST-L1 showing.
- **Rule:** if ST-L1 shows on the given prompt at the form check, stop before Hatch. Do not edit the prompt. Post in #stoa-tasking or release/skip the task.

## Hatch mistakes

| Account / task | Mistake | Fix / rule |
|---|---|---|
| Adarsh ta_sg, task 1 | Session made on sg-09 Tamilselvi, but the form showed sg-06 | Read the universe id on EACH task. It changes per task even when the form says it is fixed |
| Adarsh ta_sg, task 2 | Pressed Escape on the Hatch Home row menu, and the abandoned session got deleted | Close that menu by clicking elsewhere, never Escape |
| Praneeth fr_ca, task 2 | First create failed (orchestrator stop_session) | Create again; log it in Notes only if it affects the task |
| Praneeth fr_ca, task 4 | Copy trace button broke (clipboard override) | Reload the Hatch page, then Copy trace works |
| Praneeth fr_ca, task 4 | Session ID changed after provisioning (7f0a42d2 -> fd395f34) | Reread the session ID from Hatch right before the form |
| Charan zh_sg, task 1 | Claude went hunting for ss1 before Start annotation, then clicked Start annotation without the user's go | Follow STOA_WORKFLOW order. Wait for the user's go before Start annotation and sending the prompt |
| Charan zh_sg, task 1 | Hatch Apps view shows only "3 comments" and won't open Instagram comment text | ss1 = the post with session ID and persona visible; quote the comment from the trace |

| Charan zh_sg, task 2 | Claude clicked Copy trace A: it lands on the OS clipboard, but ctrl+v inside the browser pane pastes nothing, and Copy trace then misbehaves for the user | Claude never clicks Copy trace. The user copies both traces. If Copy trace acts up, reload the Hatch page |
| Charan zh_sg, task 2 | Built-in browser cannot upload files; a localhost workaround was blocked | The user uploads ss1 and the panel shots. Claude does not try workarounds |
| Charan zh_sg, task 4 | ST-R3 / ST-L3: form Warmth showed 4 while Hatch and the rationale said Tie (3); a form score flipped after entry | Before final checks, read the form's "Comparative scores" summary and compare all 8 with Hatch. Fix with the Edit pencil next to the score |
| Charan zh_sg, task 1 | History tab opens a temp replay session, so the panel header shows a different ID (dc26e7b9) | The form still gets the real session ID. Panel shots: top of card, middle of rationale, scores (3 images) |

## Judging notes that held up
- Check who the WhatsApp contact is in the chat history before judging tone (Charan task 1: 建忠 was family, so "建忠你好，我是Li Ting" was a stiff self-intro).
- Check the world clock in the Hatch header before calling a time remark wrong (Charan task 1: "晚上赶工辛苦了" was right at 21:12, though the suggestion called it unsupported).
- Tengah task final: edited prompt (Tengah->登加, HDB->建屋局, link->链接) cleared ST-L1. Lessons: rerun Hatch after any prompt edit; never resend or interrupt an arm (B took ~6 min, normal); a SKIP gives no suggested rationale, so ST-R6 blocks until manual review. Task unclaimed, not counted.

## Mistakes so far and the fix (Pandu + Charan, 2026-10-24). Read before every task
1. Changed a suggested score to 3 without the suggestion naming a shared trait (task 61). Fix: keep the suggestion's 2/4 and add a "Despite..." sentence.
2. Pasted responses in a different order than the traces (61). Fix: match each response to its own trace before pasting.
3. Pasted trace cut off (Charan 10). Fix: copy the full trace from Hatch, check the last message is there.
4. Ran Hatch before the ST-L1 check (doc task, Tengah). Fix: run the form prompt check FIRST, then create the Hatch session.
5. Edited the prompt but pasted old traces (Tengah SKIP). Fix: any prompt edit means a brand new Hatch session.
6. Resent the prompt / interrupted an arm because it was slow (Tengah SKIP). Fix: send once, never stop, never resend. Web tasks take 5-8 min. If stuck 15+ min, abandon and start fresh.
7. Tried to submit a SKIP run. Fix: SKIP means no suggestion, so ST-R6 blocks. Rerun cleanly, never force it.
8. Rationale too short for ST-R1 (label line does not count). Fix: opening label line plus at least 7 full sentences.
9. Rationale lines starting with dash/number fail ST-R6. Fix: one plain paragraph, no bullets.
10. Task numbering mixed up (8 vs 9). Fix: only count a task once it is submitted; blocked/unclaimed ones are not numbered.

## Pre-send checklist (every task)
- Form prompt check passed, no ST-L1.
- New Hatch session, renamed 117b62a29422_task_N.
- Prompt pasted once, exactly as in the form. Hands off until both arms finish.
- Each trace shows the prompt once, no "interrupted" notice, full length.
- Suggestion is not SKIP before entering the verdict.
- ST-C5 (advisory): fires when 3+ ratings favour the losing arm. Do not change scores; fill the 'reason for disagreeing' box with the trade-off (task 12).
11. Pasted Trace A into the Trace B box (task 13 SKIP). Fix: check the header says Trace B and the last message is B's reply.
