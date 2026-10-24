# Project Stoa: task workflow (all languages)

Stoa is Octahedron i18n Comparisons with changes. Use Octahedron files as the base for Stoa, never Stoa rules for Octahedron work.
Full client guide: `stoa_guide_source.md`. Alerts and mistakes from all accounts: `STOA_NEEDS_ATTENTION.md` (read before every task). Per-account file: `STOA_<NAME>_<LOCALE>.md` (example `STOA_ADARSH_TA_SG.md`).

## What is different from Octahedron
- The prompt is given on the task (in the locale's language and script, with an English gloss and the records it is grounded in). Small wording tweaks only. Never change asks, names, dates, amounts, language or script. Octahedron script rules (like Latin-only Tanglish) do NOT apply.
- Category comes with the task. One fixed universe for all tasks on the account.
- Send only the task prompt. No follow-up turns to either arm.
- The form makes a suggested verdict. Check it, then write the rationale in your own words.
- Order: verdict in Hatch first, Submit preference + End comparison, then copy the same values to the form.
- 20 minutes per task. Rejections are final, so check everything before submit.

## Steps (Hatch + HAI form)
| # | Where | What |
|---|---|---|
| 1 | VPN | OpenVPN Connect shows Securely Connected |
| 2 | Hatch | Log in with the account's own Hatch login. The browser pane shares one login across all chats, so do not switch accounts in it while another project is running |
| 3 | Hatch | Create session: Mode GAIA PREFERENCE, the account's universe, Protocol Hatch RM Style Task - Multilingual v1. Wait for RUNNING |
| 4 | Hatch | Rename to `alias_task_N` (lowercase). Abandoned: `alias_abandonedtask_N` |
| 5 | Form | 4 confirmations (mode, universe, protocol, session name) -> Confirmed |
| 6 | Form | Session name and Session ID (UUID from Hatch, copied exactly, each in its own field). Reread the ID from Hatch first |
| 7 | Hatch | Click Start annotation, paste the given prompt, send |
| 8 | Hatch | Universe screenshot: Apps tab > search all apps for the record named in "Grounded in" > open it (for a doc, "Open in Google Docs" shows the text). Session ID and persona visible at the top |
| 9 | Hatch | Wait until both arms finish. No error, no missing reply, no cut-off. Broken = retry or abandon and recreate, never submit |
| 10 | Form | Prompt as sent, Response A, Response B (reply text only, exactly as in Hatch). Trace A / Trace B: user copies with each arm's Copy trace |
| 11 | Form | Read the suggested verdict. Settle every item under "Check before you enter this" against the trace (Trace tab > tool call > Show input shows what was really sent) |
| 12 | Hatch | Enter the 8 scores, preference, absolute quality, rationale. Claude enters them; the user clicks Submit preference and End comparison |
| 13 | Hatch | Panel screenshot from the History tab (preference, absolute quality, rationale, 8 scores, session ID). Usually 2 images: top of the card, then scrolled to the scores |
| 14 | Form | Claude fills the form verdict (8 scores, preference, quality, rationale, Notes) right after entering it in Hatch, BEFORE the user submits (user rule, 2026-10-23). Same values as Hatch, word for word |
| 15 | Form | Notes: "Took suggestion", or one sentence on what changed and why, plus any Hatch error. Confirm and submit |

## Scores and verdict
- 1 = A significantly better, 2 = A slightly, 3 = Tie, 4 = B slightly, 5 = B significantly. A 3 only where both arms share the trait.
- Preference A or B, never a tie. Absolute quality of the preferred arm: Perfect, Good, Bad.
- **Our own verdict, every task (Chakri rule, 2026-10-23):** the form's suggestion is only one input, never the final call. Score it ourselves with the Octahedron scoring cheat sheet (`WRITING_AND_SCORING.md` section 4) and the QC lessons in `NEEDS_FIXING.md`, plus `STOA_NEEDS_ATTENTION.md`.
  - Check every suggested point against the replies and traces. A suggestion can be wrong (Charan task 6: it called B's "女儿" unconfirmed, but the user wrote "我妈妈", so it was true; Correctness changed 2 to 3).
  - Order: 8 dimensions first, then Preference, then Absolute quality.
  - A serious correctness or missing-work failure beats several style wins. When the work is equal, the voice decides (hype like "!! 🚀✨" on a serious question is off-putting).
  - Absolute quality: Perfect = nothing to change; Good = small wording, register or format flaws; Bad = wrong or missing content, wrong script, translated-sounding, off-putting tone. Preferred does not mean good (Charan task 4: B missed the PA email and never answered, so Bad).
  - Same as the suggestion: Notes "Took suggestion". Different: one Notes sentence saying what changed and why.
- Before the final checks, compare all 8 form scores with Hatch one by one (a form score once flipped on its own).

## Rationale rules
English, more than five sentences, decisive signal first, quoted words with English meaning in brackets, one or two sentences per point. No bullets, no score list, no em dashes in own words. Plain Chakri style (chakri-writing-style skill).

Write it in the Octahedron format (`WRITING_AND_SCORING.md` section 3, accepted examples there), every task:
1. Open with: `Preference: B is significantly better than A. Absolute quality: Good.`
2. The main deciding point, with the reply's own words quoted and explained.
3. Group the dimensions by arm and say why (no one line per score, never just restate the score).
4. For every dimension that goes to the losing arm, the AR-10 sentence from `NEEDS_FIXING.md`: "Despite [loser] winning [exact dimension name], [winner] is still preferred overall, because [winner] [does what better], while [loser] [main failure], and [winner's strength] matters more for this task than [what the loser did better]."
5. For any Tie: "Even though [dimension] is a tie, [winner] is still [slightly/significantly] better overall, because ... matters more for this ask than ...".
6. Why slightly and not significantly (or the other way).
7. Absolute quality reason: Good or Bad names the real flaw, Perfect says why nothing is missing.

**Length (newest client instruction from Slack, 2026-10-24, overrides older "7 to 9 sentences"):** keep the rationale short, about 5 to 6 sentences minimum ("minimum 4-5 lines but still short"), with only what is needed to support the rating. Cut the suggestion's notes hard when humanizing. Keep: the opening line, the deciding point with one or two quotes, one AR-10 "Despite..." sentence covering all dimensions that favor the loser, one "Even though ... tie" sentence covering all ties, and the quality reason. Drop extra quotes and repeated points.

Language of the rationale: write every sentence in English (Stoa guide: "Rationale in English", "in your own full sentences, in English"; the form says the same). The only non-English allowed is the arm's own words, quoted exactly in the original language and script (Chinese characters for zh_sg, Tamil script for ta_sg, accents for fr_ca) with the English meaning in brackets, for example "是真的" (it is true). Never write whole sentences in Chinese or any other language. The Octahedron "Telugu words in English letters" rule was for that track only; Stoa quotes in the original script.

Also: no absolute claims ("never", "nothing") unless exactly true; plain keyboard characters only, so describe emoji in words ("with rocket and sparkle emojis") instead of pasting them; the same rationale goes word for word into Hatch and the form.

## Screenshots
Save to the account's screenshot folder as `<name>_taskN_ssM.jpg` (ss1 = universe record, ss2+ = submitted panel).

## Never
- Claude never clicks Submit preference, End comparison, Discard, or Delete, and never logs in or out of accounts.
- Never send a second message to an arm. Never submit a broken comparison.
