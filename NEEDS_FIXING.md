# Needs Fixing (QC errors and reviewer send-backs)

Use this file when HAI QC flags something, or when a reviewer sends a task back.

**Note:** Once the Hatch session is submitted and ended, a sent-back task usually cannot be fixed. The reviewer issue only lowers the HAI score. So the real fix is to get it right before submitting: follow the guide strictly, never make own exceptions.

## How to fix a sent-back task (only if still editable)
1. Read the reviewer's or QC message fully. Paste it here as a new entry.
2. Find which field it is about (prompt, scores, rationale, screenshots, notes).
3. Scores, Notes and rationale can still be edited. A broken Hatch session cannot be fixed, so redo the task in a new session.
4. Keep Hatch and HAI the same. If a rationale changes in HAI, it must match what was in Hatch.
5. Rerun QC until green, then resubmit.
6. Add the lesson to the "Rules learned" list so it does not happen again.

## Results
- Task 1: sent back, 1 major issue (Absolute quality Good instead of Bad for wrong script). Not fixable.
- Task 2: accepted, 0 major, 0 minor (2026-10-19). Its final rationale is the reference model.
- Task 3: submitted 2026-10-19 after fixing AR-10 and AR-09. Waiting for review.

## Rules learned
- If any dimension points to the other arm than the Preference, the rationale must say why the Preference still wins. Name that dimension exactly.
- The rationale must clearly explain **why the winner is better than the loser, and by how much** ("significantly" or "slightly"). Do not only describe what each arm did.
- **Wrong script = Bad on Absolute quality, always.** If the preferred reply (or a draft inside it) is in Telugu script while the persona types in English letters, Absolute quality must be Bad, even if the reply is the better one. No "it is only the draft" exception. Always follow the strict guide rule over own judgment.
- AR-10 also fires on a Tie (3), even when nothing favors the loser (task 8). Whenever any dimension is a Tie, add: "Even though X is a tie, [winner] is still [slightly/significantly] better overall, because ... matters more for this ask than ...".
- Never write absolute claims like "never", "no", "nothing at all" about a reply (AR-03, task 8: "A never shows any cost" failed because A said "anni 200 lopu"). Reread the whole reply and describe exactly what is there and what is missing.
- Do not score "A opened app X, B did not" as Correctness or Helpfulness (AR-07 access gap, task 10). Score what each reply SAYS: a wrong fact, a missed fact that exists in the universe and that the reply states wrongly, or content quality. Tool use alone is not evidence.
- Give Telugu words their plain, common meaning. Never build a score on a word that has a normal reading or could be a typo (AR-09, task 7).
- If a quote contains an em dash or special symbol, never swap it for a comma. Split it into two exact quotes around the symbol (plain characters rule plus exact quote rule).
- Always write the two style dimensions by their full names: "Style and behavior (High level)" and "Style (Granular)". Never write just "Style" when it could be read as the high-level one, and give Style and behavior its own sentence (AR-02, task 33).
- Quote full phrases exactly. A cut quote that changes the meaning fails AR-09.
- Judge only the chat view text (the transcript). Never quote or score things seen only in the Trace.
- Clear the whole rationale box before pasting a new version, or the check reads the old text.

## Error log

### Task 1 (2026-10-17): AR-10 Octahedron Trade-off Check v1
**Message:** "Your overall pick is B but Coherence & writing quality is rated toward A (2); add one sentence saying why B still wins despite that, or re-check that rating." The reasoning said the rationale mentioned A was better in coherence but did not explain why B was still preferred, so it did not explain why B is significantly better than A.

**First fix that still failed:** "Still B wins overall, because this is only a small reading issue..." It did not name the dimension exactly, so the check failed again.

**Fix that worked:** name the dimension exactly and say why it is outweighed:
> Despite A winning Coherence & writing quality, B is still the overall pick, because a wrong word in the message is a correctness failure that sends Nanna the wrong information, and that outweighs a small reading issue.

### Task 1 (2026-10-18): Reviewer "Major issue", not approved (Vijay)
**Message:** "Great catch on A's mukku checkup, and the rest of the reasoning checks out. But B's whole draft to Nanna is in Telugu script, which you point out yourself, and for this track a wrong-script reply has to be rated Bad on Absolute quality, not Good. B can still be the better one, just change Absolute quality to Bad and keep the reason."

**What went wrong:** The guide says a reply in the wrong script for the persona is a Style fault and a **Bad** on Absolute quality. Bharathi types in romanized Telugu, but B's draft was in Telugu script. Claude picked Good, with the idea that only the draft (not the chat) was in Telugu script. That exception does not exist. The rationale even named the script problem, so the Good rating contradicted its own reason.

**Result:** Could not be fixed (Hatch already submitted). Score lowered. Lesson only.

**Correct answer would have been:** In Hatch and HAI, change Absolute quality from Good to Bad. Keep Preference B significantly better and all 8 scores. In the rationale, change only "Absolute quality: Good." to "Absolute quality: Bad." and the last sentence to:
> B is Bad and not Good, because the whole draft to Nanna is in Telugu script while Bharathi and her father chat in English letters, which is a wrong-script reply, and its opener "Ayyo", a word for shock, also does not fit a normal request.

### Task 2 (2026-10-18): AR-10 again, Helpfulness rated 2 (A) with pick B
**Message:** "the rationale acknowledges A's budget advice strength but does not explicitly state a reason for preferring B overall despite this trade-off."

**What went wrong:** The trade-off sentence only listed A's faults ("A's advice is built on the wrong idea..."). The checker wants a positive reason for B plus a weighing: what B does better, and why that matters more than the dimension A won.

**Fix that was used:**
> Despite A winning Helpfulness, B is still preferred overall, because B gets the travel days right against her real calendar while A gives a wrong day and a plan that clashes with her Oct 19 lab, and getting the dates right matters more for this trip than A's extra budget tip, which is also based on a wrong reading of the 1000 savings target.

### Task 2 (2026-10-18): Claim not supported by the transcript
**Message:** "Re-check the claim that A contains 'raw source tags with long ID numbers' — the supplied transcript of A shows no such tags ... the Style 5 for B loses its key separator."

**What went wrong:** The citation tags (like a calendar tag and long ID numbers in brackets) appeared only in the Trace tab. The Hatch chat view hides them, so the transcript pasted in HAI is clean. Claude judged from the Trace text, so the claim had no proof in the transcript, and Style 5 rested on it.

**Fix:** Removed the tag claim, changed Style from 5 to 4, rebuilt Coherence and Style reasons from the chat text only (A's run-on budget line, A's English opener "Got it Bharathi" vs B's "Sare Bharathi").

**Rule:** Judge only what the user sees in the Hatch chat view (the same text pasted as the transcript). Read final replies from the chat panel, not the Trace. Use the Trace only to check which apps and actions were used.

### Task 3 (2026-10-19): AR-09 Auditor Gate, misquoted the losing arm
**Message:** "B says 'Aadhaar link ayina SBI account loke vastundi' (into the Aadhaar-linked SBI account), which is not the same as blindly assuming SBI. Correct this misrepresentation before using it to justify the Correctness gap."

**What went wrong:** The rationale cut B's sentence to "SBI account loke" and called it "straight into SBI", which made B look wrong. B's full words were reasonable. A shortened quote changed the meaning, and the Correctness score rested on it.

**Fix:** Quote B's full phrase and base Correctness on what is really true: B checked no apps, so it never found the credit advice and reference number that are in her Gmail.

**Rule:** Always quote the full phrase, never a cut piece that changes the meaning. Before calling something an error, reread the whole sentence in the chat view. Prefer "B did not check X" (checkable) over "B is wrong about Y" unless Y is clearly false.

### Task 7 (2026-10-19): AR-09, Telugu glosses disputed
**Message:** "'kaluvalaki' means 'categories/items' not 'canals', and 'veligipoyindi' means 'went away/was spent' not 'burned'; these mistranslations inflate the oddness of B's language and carry the Style=2 rating."

**What went wrong:** The rationale gave literal, dramatic English meanings to words that can also be read normally (or as a typo, veligipoyindi for vellipoyindi). When a word has more than one meaning, the checker takes the normal one, and the Style score rested on these.

**Fix:** Removed both words. Based Style only on a phrase whose meaning is clear ("1000 saving deepam aripokunda undalante", the lamp of the saving does not go out) plus the arrows and symbols, against A's plain "migilina 3200 ni ila panchu".

**Rule:** Only use a Telugu word as evidence when its meaning is clear and not open to a normal reading. Give the plain, common meaning. If a word could be a typo or slang, do not build a score on it. Ask Chakri when unsure about a meaning.

### Hatch error: annotation will not start (2026-10-20)
**Symptom:** "Start annotation" shows "Starting..." for 2 to 3 minutes, then goes back to "Start annotation". The POST /annotation call returns 400 with {"detail":"forked arms never became ready"}.

**Cause:** Hatch could not spin up the two arms, a server capacity limit when many comparisons with live arms are open at the same time. Not a prompt problem.

**Fix:** Start fewer annotations at once (2 to 3). Finish and End comparison on scored tasks to free capacity, then retry. Stay on the page until it shows "Submit preference". If one session keeps failing for a long time, abandon it (rename youralias_abandonedtask_N) and create a new one.

### AR-10 template (use all 3 parts every time)
> Despite [loser] winning [exact dimension name], [winner] is still preferred overall, because [winner] [what the winner does better], while [loser] [its main failure], and [the winner's strength] matters more for this task than [the thing the loser did better].

### Old AR-10 template
> Despite [A/B] winning [exact dimension name], [B/A] is still the overall pick, because [the main failure of the loser] and that outweighs [the small thing the loser did better].

### Batch 21-29 (2026-10-20): process lessons
- The "task_N (A)" and "task_N (B)" rows on Home are the two arms of a running annotation. Never delete them, or the annotation breaks (Chakri deleted 21a/21b once; tasks 21 and 22 had to be restarted).
- A tab can drift back to an earlier comparison page. Before sending a prompt, check location.href holds the right session ID (the task 29 prompt was nearly sent into task 21).
- After an annotation starts, the base exploration session's app data is gone. Read the universe data from an arm session instead.
- Task 29's session ID changed after provisioning (d2b1546d to 47df5b5f). Always reread IDs from Home.

### Calendar List view shows END time (2026-10-22, tasks 45 and 49)
In Hatch Apps > Google Calendar > List, each event shows two date-time lines: START then END. A shortcut that kept only one line kept the END time. Task 45 prompt said "night 11 manikku" (event is 10-11 PM) and task 49 said "4 manikku" (event is 3-4 PM). Both arms read the real times, so only the prompt is off; noted in HAI Notes.
**Rule:** always read the START line (first of the two), or check the Week view, before putting a time in a prompt.
