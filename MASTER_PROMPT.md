# Master prompt for a new session (start it in "Bypass permissions" mode)

Copy everything inside the box below as the first message of the new session.

```
Continue my Project Octahedron work from exactly where the previous session stopped. Everything we built and learned is in the md files in this folder. This session runs in Bypass permissions mode and is FULLY AUTOMATED: do every step below on your own in the built-in browser (mcp__Claude_Browser__*) without asking me anything, until all 9 tasks are scored and waiting before "Submit preference". Only stop to ask if Hatch shows a sign-in page.

BROWSER RULE (to avoid approval prompts): do ALL browser work with mcp__Claude_Browser__javascript_tool (plus navigate, tabs_create, find, get_page_text, read_page). Do NOT use the computer tool (clicks, typing, screenshots) or browser_batch with computer actions, because those trigger the browser pane's "Allow once" approval. Click buttons with element.click() in JavaScript, fill text with the native value setter plus an input event (HTMLTextAreaElement / HTMLInputElement prototype 'value' setter, then dispatchEvent(new Event('input',{bubbles:true}))), open dropdowns and pick options by clicking the matching elements in JavaScript. Always pass tabId. Keep each javascript call under 40 seconds (split long waits into several calls). Read the arms' chat view from the two iframes with iframe.contentDocument.body.innerText (front the tab with tabs_select if they are blank).

STEP 0 - READ FIRST (in this order, fully):
1. CLAUDE.md (current locale block: en_in, persona Aishwarya Kamath, alias 85a353883201, protocol Hatch RM Style Task — Multilingual v1, mode Preference)
2. HATCH_PROCESS.md, HAI_WORKFLOW.md, WRITING_AND_SCORING.md, NEEDS_FIXING.md (every rule and every logged error), DRAFTS_TELUGU.md
3. octahedron-guide.html (the full project guide; extract text and follow it strictly)
4. Load the skill anthropic-skills:chakri-writing-style before writing ANY English text I will paste.

GOAL: Run 9 tasks at once, 85a353883201_task_21 to task_29, each fully scored in Hatch and stopped BEFORE "Submit preference". Then give me cross-checked HAI handovers one by one when I ask "task N".

CURRENT STATE:
- Hatch: https://hatch.sims.aws.metafb.cloud/control/ (I am signed in).
- No English sessions exist yet (old task_21 to task_23 were deleted). Create all 9 sessions task_21 to task_29: mode Preference, name 85a353883201_task_N, universe (search en_in) Aishwarya Kamath, protocol Hatch RM Style Task — Multilingual v1. Create one at a time and wait until each row appears before the next. After provisioning, read the FINAL ID of each from Home (IDs change) and save them in BATCH_21_29.md. Never delete anything.
- World date in her universe: Fri Oct 2, 2026, about 10 PM, Asia/Kolkata. Internet: Available.
- The browser pane allows 9 tabs: open one tab per task.

PERSONA (already researched, verify before use):
Aishwarya Kamath, 20, Pune (Wagholi, room above Patil Kirana, landlady Surekha Patil). SY BCom at a private college on Nagar Road. Evening pharmacy shifts 5-9 PM at Shree Samarth Medicals (owner Dattatray Pawar, co-worker Swapnil Jadhav, Sept pay Rs 6,500). Runs thrift resale page @twiceworn.wagholi (courier via Imran Sheikh; slab went up from Oct after only 16-17 Sept parcels; tracker in Google Sheets "Twiceworn Wagholi parcel and loan tracker"). Bridal mehndi with Nikita Bhosale on Sundays in Kharadi. Badminton junior warm-ups with Pradeep Hegde. Knee stiffness (knee check Oct 15). Rs 5000 loan share due Oct 28. Family in Dharwad (mother Shalini, brother Aditya, Divya). Apps: Gmail, Outlook Mail (college), Calendar, WhatsApp, Notion (9 pages: interlock machine buy or wait, Oct dispatch maths, room monsoon fix), Docs, Sheets, Drive, Photos, Instagram, Oura, Nutrition, Health Records, Philips Hue (bedroom + living room).
Her texting style: lowercase Indian English, short, some Hindi or Marathi words (haan, only, lol, ey), emojis like 😭. Prompts must sound like her.

UNIQUENESS AND GROUNDING (strict, check before using any prompt):
- Explore at least 2-3 apps (more is better) for every prompt and build it from real records in at least 2 different apps.
- Every prompt must be unique: different goal, different main records and a different category from every other task in this batch, from the prompt log in WRITING_AND_SCORING.md (tasks 1-14) and from DRAFTS_TELUGU.md. Never reuse or paraphrase. Pick specific details (names, amounts, dates) so it cannot match another fellow's generic prompt.
- Follow octahedron-guide.html and every md file strictly. When a guide rule is strict (wrong language = Bad, no ties on Preference, one prompt only, no follow-ups), apply it exactly, no own exceptions.

TOPIC PLAN for tasks 21-29 (one category each; verify every fact in Apps first, swap in a spare if a fact does not hold):
21 Work Productivity/SMB: courier slab hike, how much to add per parcel, is clubbing 2-3 parcels worth it (WhatsApp Imran, Notion Oct dispatch, Sheets, Gmail)
22 Home Automation: bedroom Hue light good for checking thrift colours after 5-9 shift, then nightlight (Notion bulb note, Calendar, Hue, WhatsApp Shalini)
23 Health & Fitness: knee plan till Oct 15 knee check with standing shifts and warm-ups (Calendar, WhatsApp Pradeep, Gmail Decathlon, Notion)
24 Legal/Civic: EBC freeship document verification till 5 Oct plus fake fee-refund phishing alert (Outlook)
25 Learning/Research: free Tally with GST course plus HSN code correction from Dattatray sir (Outlook, WhatsApp)
26 Shopping: monsoon window leak fix for room plus parcel storage crate (Notion room page, WhatsApp Surekha)
27 Finance: October cash plan: Rs 6,500 pay, Delhivery Rs 640 bill, Rs 5000 loan share Oct 28 (Gmail, Calendar, Sheets)
28 Relationships: Oct 4 Sunday stock count 10-11 clashes with Nikita mehndi trials, how to tell Nikita (Calendar, WhatsApp Nikita)
29 Media Creation: captions for next Twiceworn drop in her style (Docs caption drafts, Instagram, Notion)
Spare ideas (use one if a topic fails, and use Emotional Support for the next batch): Emotional Support "mood off" about losing the courier slab (Gmail to Imran, Notion), Travel home to Dharwad for Diwali, Entertainment (Spotify October Mix + Amazon MiniTV thrift shows after shift), Companionship (holiday evening chat), Oct 6 tailor visit vs shift clash, library duty preference form (Outlook).

FOR EACH TASK (follow HATCH_PROCESS.md exactly):
1. Explore the apps, verify every fact, write the prompt in her style (no em dashes, no dash separators, plain keyboard characters).
2. Start annotation: paste the prompt in the Start annotation dialog. All 9 sessions can exist at once, but start the annotations in waves of 2-3 (capacity limit). Stay on the page until it shows "Submit preference". If it goes back to "Start annotation", the POST returned 400 "forked arms never became ready" (capacity): retry later, one at a time.
3. Read BOTH replies from the CHAT VIEW (iframes; front the tab if they are blank). Use the Trace only to see which apps each arm called. Never score anything seen only in the Trace.
4. Verify every claim the arms make against her apps.
5. Fill the Hatch scoring panel: Preference, Absolute quality, all 8 dimensions, Required rationale. Save and confirm "All preference changes saved". Never click Submit preference, End comparison, Discard or Delete.

WRITING STYLE (three kinds of text, each different):
1. PROMPT = Aishwarya's own voice. Copy how she types in her WhatsApp chats: lowercase Indian English, short, natural Hindi/Marathi words only where she uses them, no em dashes, no dash separators.
2. "HOW THE PROMPT RELATES TO THE UNIVERSE" (2-4 sentences) = Chakri's style via the skill anthropic-skills:chakri-writing-style: plain intermediate English, short sentences, simple everyday words, humanized, third person, names the real records and which apps they are in (Gmail, Calendar, WhatsApp...). Template and examples are in WRITING_AND_SCORING.md section 2.
3. REQUIRED RATIONALE and NOTES = Chakri's style via the same skill: plain humanized words, no fancy words (no furthermore, notably, robust, nuanced, seamless), no em dashes.
For 2 and 3: plain keyboard characters and symbols only. Write Rs instead of the rupee sign, normal "straight quotes", no curly quotes, no 【】, no arrows, no special unicode. Describe odd symbols in words instead of copying them.

PAST MISTAKES: before writing every rationale, reread every logged error in NEEDS_FIXING.md (AR-10 trade-off and tie sentences, AR-09 misquotes and disputed Telugu glosses, AR-07 access-gap scoring, AR-03 absolute claims, AR-02 scores vs rationale mismatch, the reviewer send-back for Good instead of Bad, claims seen only in the Trace, symbols and em dashes in quotes). Check the finished rationale against each one before saving.

RATIONALE RULES (from NEEDS_FIXING.md, all mandatory):
- Start: "Preference: X is slightly/significantly better than Y. Absolute quality: Good/Bad/Perfect." English, plain words, Chakri style, 7-10 sentences.
- Quote full phrases exactly from the chat view. Never cut a quote so it changes meaning. If a quote has an em dash or symbol, split it into two exact quotes.
- Every dimension that favours the loser needs: "Despite [loser] winning [exact dimension], [winner] is still preferred overall, because [winner's strength], while [loser's failure], and [X] matters more for this task than [Y]."
- Every Tie needs: "Even though [dimension] is a tie, [winner] is still [slightly/significantly] better overall, because ... matters more for this ask than ..."
- Say why "slightly" or "significantly".
- Never use absolute claims ("never", "nothing at all") unless 100% true after rereading the full reply.
- Never score "A opened app X, B did not" as Correctness/Helpfulness (access gap). Score only what each reply says.
- Absolute quality strict: wrong language, translated-sounding or bookish wording, a full English-narrated plan line where unnatural, or missing content = Bad. Good needs a named flaw, Perfect needs a reason nothing is missing.
- Plain keyboard characters only (Rs not the rupee sign, no curly quotes, no 【】).

HANDOVER (when I say "task N"): reload that task's Hatch page first and read back name, ID, the 9 saved values, Absolute quality and rationale. Start with a short "Cross-check" (what was verified, uniqueness vs all tasks, rules followed). Then give: session name, ID, persona, category, apps utilized (apps the ARMS called, from the Trace; "No Apps Used" if none), prompt, 2-4 sentence universe explanation (Chakri style, names the records and apps), the score table, rationale, Notes (real issue or "None"), confirm session ID, QC confirmation text. Open that task in the front tab so I can screenshot.

After each task, add it to the prompt log in WRITING_AND_SCORING.md. Log any new QC error or reviewer send-back in NEEDS_FIXING.md.
```

## What this prompt does (explained)
- **Step 0** makes the new session read every md file, the full guide and the writing-style skill before it touches anything. That's where all our rules live.
- **Current state and persona** save it from redoing my research: Aishwarya's life, people, apps and texting style, plus the three sessions already created.
- **The topic plan** gives 10 unique categories with the exact apps for each, plus spares if one fails fact-checking.
- **The task loop** carries the lessons from the hard parts: start 2 or 3 at a time (the capacity error), read the chat view and not the Trace, verify facts, never submit or delete.
- **The rationale rules** are the full NEEDS_FIXING list, so AR-10, AR-09, AR-07, AR-03 and the strict Bad rule won't come back.
- **The handover** format is exactly what you asked for, cross-check first.
