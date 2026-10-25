# Stoa: Pandu account, Bengali (Singapore)

General steps: `STOA_WORKFLOW.md`. This file holds only what is specific to this account.

## Account
- Chat name: Pandu Stoa
- Name: Pandu (Kumara Swamy)
- Hatch login: Pandu's own Hatch login (user logs in, Claude never types passwords)
- Alias: `9e3c159539d5` -> session name `9e3c159539d5_task_N`, abandoned `9e3c159539d5_abandonedtask_N` (lowercase)
- Locale: Bengali (Singapore), bn_sg. Never a bn_in_wb (India) universe
- Universe: CHANGES PER TASK. Read the universe id at the top of each task and create the Hatch session on that persona. Persona list: stoa_guide_source.md section 3. Bengali (Singapore): 01 Sayan Pramanik, 02 Kaushik Kundu, 03 Madhumita Sen, 04 Sujoy Guha, 05 Rudra Mukherjee, 06 Srabani Majhi, 07 Kamrul Hossain, 08 Anima Guha, 09 Ankita Bandyopadhyay
- Mode GAIA PREFERENCE, Protocol Hatch RM Style Task - Multilingual v1, world time zone Asia/Singapore
- Screenshots: `<SCREENSHOT_FOLDER>` (NOT GIVEN YET) -> `pandu_taskN_ssM.jpg`

## Form confirmations (4)
- Mode: GAIA PREFERENCE -> Confirmed
- Universe: the id shown on that task (see task log) -> Confirmed
- Protocol: Hatch RM Style Task - Multilingual v1 -> Confirmed
- Session renamed to 9e3c159539d5_task_N -> Confirmed

## Bengali (Singapore) notes
- Paste the prompt exactly as given (its own script and Bengali-English mix). Zoom the box to check it before sending.
- Run the form prompt check (ST-L1) on the given prompt BEFORE creating the Hatch session. Never reword the prompt to beat an alert.
- Language read: natural casual Singapore Bengali with English words wins. Mark down bot narration, translated-sounding wording, wrong register, or a wrong voice in any message sent from the persona's own number.
- Quote Bengali in its original script with the English meaning in brackets. Every other sentence in the rationale is plain English.
- Hatch Home row menu (Stop, Rename, Delete): close it by clicking elsewhere, never Escape.

## Cloud-session workflow (no built-in browser, 2026-10-24)
This chat runs in a cloud session with no built-in browser, so Pandu does all Hatch and form clicks. Claude only checks and writes.
1. Pandu pastes the HAI task text (prompt, gloss, category, grounded records). Claude gives the prompt and session name as ready-to-paste blocks.
2. Pandu runs the form prompt check, creates the Hatch session, renames it, sends the prompt once, and takes ss1. Claude helps find the record from a screenshot.
3. Pandu pastes Trace A, Trace B, both responses and the form's suggested verdict.
4. Claude checks every point against the traces and gives the 8 scores, preference, quality, rationale and Notes as code blocks.
5. Pandu enters them in Hatch, clicks Submit preference and End comparison, takes the panel shots, and copies the same values to the form.
Checks learned on task 61:
- Pasted responses can come in the opposite order to the traces. Match each response to its own trace before pasting on the form.
- Strip "[Request interrupted by user]" from a pasted prompt.
- Form rule: a 3 only where the suggestion names the shared trait. If the suggestion gives 2 or 4, keep it unless there is a real wrong point, and add the AR-10 "Despite" sentence.

## Rationale style (Pandu rule, 2026-10-24)
- Always use the chakri-writing-style skill: simple plain words, short sentences, no long chains joined by commas, no fancy words, no em dashes.
- One idea per sentence. Keep the required parts (opening line, deciding point with quotes, Despite and tie sentences, slightly/significantly reason, quality reason).

## Task log

| Task | Session ID | Category | Verdict | Status |
|---|---|---|---|---|
| 61 | 1edda904-6a74-4567-8f3e-cbed27a03ec7 | Tracker + email | B significantly, Bad, 4,5,4,2,4,3,3,3. Took suggestion. A guessed form dates ("আন্দাজে দিয়েছি"), called Saturdays Friday, venue Punggol (email says Sengkang CC), 3 Oct (tomorrow) marked unpaid. B honest placeholders. Neither read Shirley emails or made a Gmail draft | bn-sg-06 Srabani Majhi. COMPLETED |
| 62 | (reread from Hatch) | Email | B slightly, Bad, 4,3,5,4,3,3,3,3. Took suggestion. Both searched only Gmail, missed Outlook thread (6 short, 4 found, 2 missing). A three English status lines | bn-sg-03 Madhumita Sen. COMPLETED |
| 63 | (reread from Hatch) | Nutrition (tiffin) | A slightly, Good, 2,2,2,3,2,2,3,3. Took suggestion. Prompt edit: Nutrition->নিউট্রিশন (one-check rule). 16 tiffins, avg 361 cal/444 mg, 680 mg tie 11 Sep + 2 Oct. B omitted 11 Sep contents + romanized opener | persona: ask. SUBMITTED |
| 64 | 9e3c159539d5_task_64 | Calendar + email check | B slightly, Good, 4,3,4,4,4,3,3,3. Took suggestion. Prompt edit: Mei Chen->মে চেন, Gmail->জিমেইল, draft->ড্রাফট. 11 Oct Sunday, notice 4-5:30 vs calendar 4-5. Both no draft, both unverified Sunday-closure claim. B flagged mismatch + offered fix; A "On it —" opener | persona: likely bn-sg-09 Ankita Bandyopadhyay (confirm). SUBMITTED |
| 65 | 9e3c159539d5_task_65 | Appointments audit (Gmail vs calendar) | A slightly, Good, 2,3,2,4,3,3,3,3. Took suggestion. Romanised prompt pasted as is. Both found GP 17 Sep (clash 14-22 shift), dental 24 Sep (free), Ma physio 8 Sep (backup hold + 10:04 shift). Neither had Outlook (menu tasting missed by both). B "Got it —" + Hindi "mil gaya"; A offered to calendar past appts. ST-L4 hit: "Style and Style and behavior" residue, fixed | persona: likely bn-sg-09 Ankita Bandyopadhyay (confirm). SUBMITTED |
| 66 | 9e3c159539d5_task_66 | BP readings WhatsApp to daughter | B slightly, Bad, 4,2,4,2,2,3,3,4. Took suggestion. Prompt edit: WhatsApp->হোয়াটসঅ্যাপ. Both sent. B wrong cause 30 Sep "সিঁড়ি ভাঙা" (sheet: avoided stairs); A "Omron-এ মাপা" non-cause + afternoon reading, echoed instruction to daughter. ST-C5 reason box text given | persona: Rudra Mukherjee (from traces; confirm dropdown). SUBMITTED |
| 67 | 9e3c159539d5_task_67 | Research: caregiver support Yishun/Khatib (dialysis) | A slightly, Good, 2,4,2,2,4,3,4,3. Took suggestion. Prompt edit: Yishun/Khatib, dialysis, caregiver support, AIC, family service centre -> Bengali script. Neither read Dover Park mail/contact. A Bengali script but unverified interpreter claims, off-source NKF number, AMKFSC link not in results, tui + "rent pressure". B romanised Bengali (wrong script) but all links sourced. ST-C5 reason given | persona: unconfirmed (B said "Sayan"). SUBMITTED |
