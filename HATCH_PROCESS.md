# Hatch Process (start to end)

Hatch URL: https://hatch.sims.aws.metafb.cloud/control/
Who does what: **Claude** drives Hatch in the built-in browser. **Chakri** verifies the prompt, does every Submit, and handles sign-in.

## Fixed setup
| Field | Value |
|---|---|
| Mode | Preference (GAIA PREFERENCE in HAI) |
| Name | `85a353883201_task_N` (N = next task number, see the log in WRITING_AND_SCORING.md) |
| Universe | Current locale and persona from CLAUDE.md (now `en_in`, Aishwarya Kamath). Keep the same one for every task |
| Protocol | Hatch RM Style Task — Multilingual v1 (badge "Published v2" is fine). Never plain RM Style, Avocado or Preference-Derived |

## Steps

### 0. Before Hatch (Chakri)
- HAI: click **Start task** first (paid timer starts). Keep the tab open.
- VPN: OpenVPN Connect shows "Securely Connected".

### 1. Create session (Claude, no permission needed)
1. Open the Hatch control page. If the sign-in page shows, stop and ask Chakri to sign in.
2. Click **Preference**, type the name, pick the universe, pick the protocol.
3. Click **+ Create session**. Wait until PROVISIONING changes to **RUNNING**.
4. Click **Open** in the Actions column.

### 2. Guidelines pop-up (Claude)
- Note the **world date and time** (this is "today" in the persona's world).
- Note **Internet: Available** or not.
- Note the app list.
- Ignore its "continue for several rounds" advice. **One prompt only.**
- Close it with the X.
- Save the **session UUID** shown at the top (under "Pairwise comparison").

### 3. Explore Apps (Claude)
Read at least 3 to 4 apps. Do not type in the Message box.
- **Google Calendar**: List view and the next 2 weeks after the world date.
- **WhatsApp**: the 4 to 5 latest chats. Copy real lines to learn how the persona types.
- **Gmail**: latest emails (bookings, college, orders, bills, job mails).
- At least one more: Notion, Docs, Sheets, Drive, Photos, Oura, Nutrition, Health Records, Instagram.
- Find 2 to 4 records from different apps that connect to one goal, with exact dates.
- Chakri may also paste app contents to speed this up.

### 4. Prompt (Claude drafts, Chakri approves)
- Claude gives the prompt + the 2 to 4 sentence "how it relates to the universe" (see WRITING_AND_SCORING.md).
- Chakri pastes the prompt in HAI and confirms.
- Claude must NOT type the prompt in Hatch or click Start annotation until Chakri says so in chat. Only after that OK: **Start comparison**, paste the exact same prompt, **Start annotation**.
- After that, never send another message in this session.

### 5. Read the arms (Claude)
- Wait until both Arm A and Arm B finish. If one says "Something went wrong", is blank or cut off, do not score. See "When it breaks".
- Read the final replies from the **Hatch chat view** (what the user sees and pastes as the transcript). The Trace can show extra things, like citation tags, that the chat hides. Never score something seen only in the Trace.
- Open the **Trace** tab only to check tool calls, apps used and claimed actions.
- Check every fact and every claimed action against Apps (dates, names, places, "sent", "created").
- Note which apps each arm actually called (tool calls in the trace). Memory/skill file reads are not apps.
- Traces: **Copy trace A** goes to HAI Trace A, **Copy trace B** goes to HAI Trace B. Never "Copy both traces". Claude gives the trace text, or Chakri clicks the buttons and pastes.

### 6. Scoring panel (Claude fills, Chakri checks)
- Fill Preference, Absolute quality, all 8 dimensions, Required rationale in Hatch.
- Claude does NOT click Submit preference or End comparison.

### 7. Screenshots (Chakri takes, 3 images for HAI)
1. **Screenshot 1**: Arm A and Arm B replies side by side, text readable.
2. **Scoring panel**: Preference, Absolute quality, all 8 dimensions and the rationale, fully filled.
3. **Confirmed screenshot** (after step 8): Home, **Annotations** tab, **Preference**, the task row showing name, UUID and **COMPLETED**. Crop out the model names.

### 8. Finish (Chakri)
Order: HAI values entered and QC green, then **Submit preference**, then **End comparison**, then check Annotations shows COMPLETED (not "Ended mid-annotation"), then the Confirmed screenshot, then submit in HAI.

## When it breaks
- **"Agent unavailable" / arms closed** (idle timeout): click **Resume saved sessions**. Never click **Discard annotation** (it deletes both replies).
- **Arm failed, blank or cut off**: rename the session `85a353883201_abandonedtask_N` (three-dot menu, Rename), create a new session with the same N, run again. Put the new name and UUID in HAI.
- **Sign-in page**: Chakri signs in. Claude never types passwords.
- Never use Restart or Delete.
- Never try to guess or mention which model is behind each arm.
