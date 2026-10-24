# Project Octahedron (Chakri, alias 85a353883201)

## Current locale (change only this block when the project changes)
- Locale: **Tamil (Singapore), `ta_sg`** (NOT Tamil India ta_in_tn). Earlier: Telugu te_in_ap (tasks 1-14, ended), English India en_in / Aishwarya Kamath (dropped before tasking).
- Persona: one of the 9 ta_sg universes (Keerthana Palanisamy, Ramesh Chandran, Murugan Shanmugam, Prakash Ganesan, Shanthi Anand, Janani Shanmugam, Divya Balan, Ashwin Chandran, Tamilselvi Krishnan). Chosen: **Keerthana Palanisamy** (omni-ta-sg-01, Hougang, 39, education, young parent). Use her for every task. Tasks 31-40 now, 41-50 later on command.
- Prompt script: **English letters only (Tanglish), never Tamil script**, even if the persona types Tamil script (normal keyboard has no Tamil). Not English, not a word-for-word translation.
- Protocol: Hatch RM Style Task — Multilingual v1, mode Preference
- Next task number: task_31 (Tamil Singapore batch 1 = 31-40)
- **PERSONA SPREAD RULE (client flag, 2026-10-22):** Keerthana was 53% of our tasks; the client wants about 11% per ta_sg persona. Until the client posts again, use ONLY these, most needed first: Janani Shanmugam (omni-ta-sg-06), Divya Balan (07), Tamilselvi Krishnan (09), Murugan Shanmugam (03), Ashwin Chandran (08), Prakash Ganesan (04), Shanthi Anand (05). No more Keerthana, no Ramesh Chandran. Spread tasks one persona per task, in that order. HAI dropdown = Tamil (Singapore) > that persona. Tasks 41-44 stay on Keerthana; 45-50 (Keerthana) were dropped and get redone on the new personas.
- HAI persona dropdown: Tamil (Singapore) > Keerthana Palanisamy

## Read before helping with any task
- `HATCH_PROCESS.md`: Hatch steps. Claude drives Hatch up to scoring. Claude never clicks Submit preference, End comparison, Discard or Delete.
- `HAI_WORKFLOW.md`: every HAI form screen with the answer to enter, and the final handover checklist.
- `WRITING_AND_SCORING.md`: prompt rules, locale notes, universe explanation, rationale format, scoring cheat sheet, prompt log.
- `NEEDS_FIXING.md`: every QC error and reviewer send-back with the fix. Check it before every rationale.
- `DRAFTS_TELUGU.md`: dropped Telugu drafts (never reuse those prompts).

All pasteable English text uses the `anthropic-skills:chakri-writing-style` skill: plain, humanized, no em dashes, plain keyboard characters. Prompts copy the persona's own texting style. Full guide: `octahedron-guide.html`.
