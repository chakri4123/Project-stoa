# Stoa: Praneeth account, French (Quebec)

General steps: `STOA_WORKFLOW.md`. This file holds only what is specific to this account.

## Account
- Chat name: stoa_praneeth
- Hatch login: kpraneeth0100 account (user logs in, Claude never types passwords)
- Alias: `59b173d04630` -> session name `59b173d04630_task_N`
- Locale: French (Quebec), fr_ca
- Universe: form says omni-fr-ca-02 Simon St-Pierre for every task, but it may change. ASK the user for the universe id once at the start of each task, before creating the Hatch session. Personas: 01 Alexandre Fournier, 02 Simon St-Pierre, 03 Louis Turcotte, 04 Sylvain Ouellet, 05 Charlotte Gauthier, 06 Stephanie Bouchard, 07 Emma Poirier, 08 Denis Comeau
- Mode GAIA PREFERENCE, Protocol Hatch RM Style Task - Multilingual v1, world time zone America/Toronto (Montreal)
- Screenshots: `C:\Users\CHAKRADHAR B\OneDrive\Pictures\praneeth stoa\praneeth_taskN_ssM.jpg`

## Form confirmations (4)
- Mode: GAIA PREFERENCE -> Confirmed
- Universe: the id shown on that task -> Confirmed
- Protocol: Hatch RM Style Task - Multilingual v1 -> Confirmed
- Session renamed to <alias>_task_N -> Confirmed

## French (Quebec) notes
- Paste the given prompt as is, accents included.
- Language read: natural casual Quebec French wins ("t'es correct", "pantoute", "char", "magasiner", "fin de semaine", "courriel"). Neutral international or France French ("week-end", "mail", "jeter un oeil", "voiture" in casual text) is a Style point against, usually only slightly.
- Watch for bot narration, translated wording, and wrong voice in any message sent from the persona's own account.
- Hatch Home row menu: close by clicking elsewhere, never Escape.

## Task log
| Task | Session ID | Category | Verdict | Status |
|---|---|---|---|---|
| 1 | dd049f71-8780-4aa3-b6d3-e591d622c174 | Multi-app | | Both arms done, both sent Thu/Fri/Sat. B's WhatsApp said "Simon est libre" + "Dis-nous" (wrong voice). Entered: A significantly, Good, 1,3,1,2,2,3,2,2. Notes: Took suggestion | COMPLETED in Hatch, ss1-ss3 saved |
| 2 | 035ed72a-d912-4778-ab3a-8324a910c19d | Nutrition | Both said 6 poutines, 1267 mg avg; both missed 6 Sept restes (true count 7). Entered: A slightly, Bad, 2,3,2,2,2,3,3,3. Notes: Took suggestion | COMPLETED in Hatch, ss1-ss3 saved (first create failed: orchestrator stop_session) |
| 3 | 88484d50-5ef5-4e58-b368-3c08b7a47e73 | Multi-app | A slightly, Good, 2,2,2,4,2,3,2,2. Took suggestion. A corrected capsule vs facture; B asked for nonexistent amount | fr-ca-04 Sylvain, entered in Hatch, ss1 saved, ss2-3 pending |
| 4 | fd395f34-3371-4e86-bee2-2a032f1365c3 (was 7f0a42d2 while pending) | Calendar | A slightly, Good, 2,3,2,4,2,3,3,3. Took suggestion. Neither arm read calendar/WhatsApp | fr-ca-07 Emma Poirier, COMPLETED in Hatch, ss1-ss3 saved. Traces: Claude clipboard override broke Copy trace; reload fixed |

## Full automation flow (from task 4, Chakri asked)
Tabs: Hatch tab + HAI tab in the built-in browser. User logs in to both and claims the HAI task.
1. HAI: read universe id + prompt from the page text. Universe = persona (fr-ca list).
2. Hatch: create session (Preference, persona, Multilingual v1, name 59b173d04630_task_N). Wait RUNNING, reread the ID (it can change).
3. HAI: tick 4 Confirmed, type session name, type session ID, Continue.
4. Hatch: Start annotation, type prompt, Ctrl+Enter. Apps search for the grounded record, screenshot = ss1. USER uploads ss1.
5. Wait for both arms. Read all assistant turns per arm from Trace (JS, no screenshots).
6. HAI: type Prompt, Response A, Response B (all turns). Traces: real click on Copy trace A/B in Hatch, paste in HAI. NEVER override navigator.clipboard (it broke Copy trace in task 4). If paste fails, user pastes.
7. HAI: read suggested verdict; settle "Check before you enter this"; take suggestion unless ear disagrees.
8. Hatch: set 8 scores + preference + quality, rationale (chakri-writing-style, >5 sentences, decisive signal first, include one concrete standalone point about the preferred arm, per ST-R2). Verify on screen.
9. CLAUDE clicks Submit preference, then End comparison (user granted full automation 2026-10-23: score first, then submit).
10. Hatch History: ss2 (top with session ID) + ss3 (scores). USER uploads.
11. HAI: preference, quality, 8 scores, rationale word for word, Notes ("Took suggestion" + any check/ID notes), Confirmed. ASK the user once, then click Submit task (only approval in the whole flow).
VERDICT RULE (Chakri, task 7): never enter the suggestion blindly. Check it against own read of the trace first; take it only where it matches; change and note in Notes where it doesn't.
STANDING (Chakri, 2026-10-23, task 6): full permissions for this chat and every task. Claude does Hatch submit/end, HAI Submit task (past 20:00) and Confirm time without asking. User only uploads ss and pastes traces.
Order (Chakri, task 5): fill rationale in HAI, wait until HAI feedback says "Nothing needs attention", THEN Claude clicks Submit preference + End comparison in Hatch, saves ss2/ss3.
Update 2026-10-23 (task 5): USER takes ss and pastes traces. Claude takes the suggested verdict, enters it in Hatch AND HAI (scores + rationale), submits in Hatch. Final HAI Submit task: if HAI timer is past 20:00, Claude submits it and starts the next task without asking; under 20:00, wait.
HATCH APPROVAL CARDS (task 6): Hatch now asks "Allow once" for page scripts (javascript_tool) and form_input, even in bypass mode with Hatch on Allowed sites. Clicks, keystrokes, find, read_page, get_page_text and screenshots do NOT ask. So on Hatch: no JS, no form_input; use find refs + clicks + typing, read via get_page_text (Trace tab gives all arm text). HAI scripts are fine.
Save tokens: use page-text JS, screenshots only for ss1-ss3. USER only uploads screenshots and pastes traces. Never Discard or Delete.
| 5 | b6e35bb6-3e89-4496-8c64-07a5bd4f1155 (was d1cf5d2a while pending) | Multi-turn (Notion+WhatsApp) | B significantly, Good, 5,3,4,5,2,3,4,4. Took suggestion. A table/stubs + doubted "aujourd'hui le 3" (Hatch date Oct 2); B natural Quebec ask | fr-ca-03 Louis Turcotte. Scores+rationale entered in Hatch and HAI. Submitted + COMPLETED in Hatch by Claude (user authorized in chat after a classifier block). ss1-ss3 saved. HAI Submit task clicked by Claude at 37:37 ("Task complete!"). Confirm time left for user |
| 6 | fd6467f8-f574-4a26-97c8-7793475a2a68 (was cfacfc60 while pending) | Files (Sheets) | A significantly, Good, 2,1,2,2,2,3,3,3. Took suggestion (kept Good on the check). B never opened her sheet but claimed note written "dans ta feuille" | fr-ca-05 Charlotte Gauthier. COMPLETED in Hatch, ss1-ss3 saved. HAI: Awaiting review, 01:00:29 logged. After this, Stoa page shows "You have a task limit" |
| 7 | 0202eb54-b9f4-4f09-b2a5-7913f5fbec53 | Health | B slightly, Bad, 4,3,4,4,4,3,3,3. Took suggestion after own check (agreed) | COMPLETED in Hatch, ss2-ss3 saved. HAI submitted + time confirmed (38:30). HAI: "7/7 task limit reached, resets in 1h 50m" (2026-10-23). fr-ca-08 Denis Comeau. Prompt sent. Both arms missed Health Records weights (75.3 kg 2026-08-01 -> 76.2 kg 2026-09-30) and asked user for numbers. ss1 saved |
