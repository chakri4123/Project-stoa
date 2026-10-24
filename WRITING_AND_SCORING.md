# Writing and Scoring

## Whose style for what
| Text | Style |
|---|---|
| **Prompt** (Telugu) | The **persona's own** style, copied from their WhatsApp/emails (romanized Telugu, their words, their code-mixing). No em dashes |
| **2-4 sentence universe explanation** (English) | **Chakri's style**: load `anthropic-skills:chakri-writing-style`, plain humanized words, no em dashes |
| **Required rationale** (English) | **Chakri's style**: same skill, plain humanized words, no em dashes |
| **Notes** (English) | **Chakri's style** |

Chakri's style = plain intermediate English, short sentences, simple everyday words, humanized, no em dashes (—), no fancy words. Load that skill before drafting any English text.

---

## Locale notes
**Tamil (Singapore), ta_sg (current):** prompt in the persona's own mix, mostly Latin-letter Tamil with some Tamil script and natural English/Singlish (lah, can, uncle), copied from their chats and mails. Judge as a native Singapore Tamil speaker: natural or translated, right register (respect forms for elders), the user's language and script, SGD amounts, Singapore places, dates and holidays (Deepavali, Thaipusam). A reply in the wrong script or language for the persona is a Style fault and Bad on Absolute quality. Rationale in English, quoting Tamil words exactly with plain English meaning (Tamil script quotes are fine as quotes; explanation in plain keyboard English).

**English (India), en_in (current):** prompt in natural Indian English, the way the persona types in her chats and mails (her casing, short forms, any Hindi or Marathi words she really mixes in). Not textbook English. Money as Rs, Indian dates (12 Oct), local places. Rationale quotes the replies exactly; no translation needed. Judge register: does the reply sound like a natural Indian English chat, or like a stiff template or an American-sounding bot? A reply in Hindi script or another language when she writes English is a language fault (Bad).

**Telugu (te_in_ap, ended):** romanized Telugu WhatsApp style; Telugu script replies were a wrong-script fault.

## 1. Writing the prompt

### Rules
- **Use 2 to 4 records from different apps** (not only Calendar). Example: a calendar event + a WhatsApp chat + an email or a Sheet/Note. The assistant should have to connect them.
- **Grounded**: every fact in the prompt exists in the persona's apps. Nothing invented.
- **Exact dates**: "Oct 6 Tuesday", not "next week". Check the world date in the guidelines pop-up.
- **Persona's own style**: copy how the persona types in WhatsApp (romanized Telugu, lowercase, words like "nanna", "andi", "kada", English mixed where natural, same emoji habits). Never translate English word for word.
- **No em dashes, no dash separators** in the prompt. Commas and periods only.
- **Feasible**: only ask for what the apps can do. Gmail can draft and send. Calendar, Drive, Docs, Sheets, Notion can be written. WhatsApp sends only in existing chats. Outlook cannot draft. Contacts and Oura are read-only. If Internet is not available, the prompt must be answerable from the persona's data alone.
- **A goal, not steps**: not too vague, not "open sheet X and change B4".
- **Clear done**: it is obvious what a good answer looks like.
- **One goal, one category.** Pick by the goal, not the app.
- **Never reuse or paraphrase** a prompt from the log below.

### Categories (13, Personal Productivity is not allowed)
Companionship / Chat, Learning / Research, Health & Fitness, Shopping, Media Creation, Work Productivity / SMB, Entertainment, Emotional Support, Finance, Travel, Relationships, Legal / Civic, Home Automation.
Least covered (pick first): Companionship / Chat, Legal / Civic, Home Automation, Shopping, Entertainment, Travel.

### Prompt self-check
- [ ] 2 to 4 records from different apps, all real
- [ ] exact dates inside the world's data range
- [ ] persona's voice and script, natural code-mixing
- [ ] no em dashes or dashes
- [ ] feasible app actions, web only if Internet is available
- [ ] a goal with a clear finish, not a step list
- [ ] category matches the goal and is new for Chakri
- [ ] not similar to any earlier prompt

---

## 2. "How the prompt relates to the universe" (2 to 4 sentences, English)

Format: name the records and their apps, then say what the prompt asks and why it fits the persona. Third person, plain words, no em dashes.

Template:
> The prompt is based on real records in [persona]'s universe. [App 1] has [record with date], and [App 2] shows [record]. [One more link if needed.] So the prompt asks Hatch to [goal], which fits her real situation and the way she normally [texts / talks / works].

Task 1 example:
> The prompt is based on real records in Bharathi Dasari's universe. Her Google Calendar has "Ammamma file ready cheyyali" on Oct 5 at 7 PM and "Ammamma mookalla checkup" at Vizianagaram town hospital on Oct 6 at 10 AM, which clashes with her lab hours from 10 to 1 the same day. In her WhatsApp chat with her father Mohan Dasari, she reminds him about the Oct 6 checkup and he says he will take Ammamma himself. So the prompt asks Hatch to draft a simple WhatsApp message for her father, which fits her real situation and her normal way of texting him.

---

## 3. Required rationale

### Format
1. Start: `Preference: B is significantly better than A. Absolute quality: Good.`
2. The main deciding point with quotes from the replies.
3. Which dimensions go to which arm and why (group them, do not write one line per score).
4. **Trade-off sentence** for any dimension that goes against the pick (AR-10 check). It must have 3 parts: the winner's positive reason, the loser's failure, and "X matters more for this task than Y". Template in NEEDS_FIXING.md. Only listing the loser's faults fails the check (task 2).
5. If the longer reply wins, say what the extra content added.
6. Absolute quality reason: Good or Bad names a real flaw, Perfect says why nothing is missing.

### Style
- 7 to 9 sentences. More than 5 is required. Short enough for reviewers.
- English only. Telugu words written **in English letters** in quotes, with the meaning in English: "mukku checkup", meaning nose checkup.
- Plain keyboard characters only. No special symbols copied from replies (【】, †, ₹, →, curly quotes). Describe them in words, e.g. "odd source tags with long ID numbers". Write Rs instead of the rupee sign.
- Plain words, humanized, no em dashes, no "furthermore / notably / robust / nuanced" type words.
- Never just restate a score ("Tone goes to B because B had better tone" says nothing).

### Task 2 final (ACCEPTED, 0 issues): best reference
> Preference: B is slightly better than A. Absolute quality: Bad. The main difference is the travel plan. A says "Oct 18 Saturday" but Oct 18 is a Sunday, and it tells her "Oct 19 full intlo" (stay home all of Oct 19) even though her calendar has lab from 10 to 1 that day, while B says "Oct 19 evening lab ayyaka bus ekkesi" (take the bus on Oct 19 evening after lab) and come back Oct 21 night. B also tells her to confirm the Oct 20 lab with her guide because the holidays mail says it is a holiday, so Correctness, Completeness and Tone go to B. B lists more sleeper options with prices in a clear order, APSRTC from about Rs 659 and private buses like KVR Rs 1143 and Morning Star Rs 1289, while A packs the rates and the budget math into one long run-on line, so Coherence & writing quality goes slightly to B. A opens in English with "Got it Bharathi" in a Telugu chat, while B opens with "Sare Bharathi", which sounds like a normal Telugu reply, so Style and Style and behavior go slightly to B. Helpfulness goes slightly to A, because A takes a clear budget position, "okavaipu APSRTC 659, return private 599" (APSRTC one way and a private bus back), with the PhonePe cashback tip, while B hands the budget back with "ippativaraku entha kharchu ayyindo chepte" (tell me how much you spent so far). Despite A winning Helpfulness, B is still preferred overall, because B gets the travel days right against her real calendar while A gives a wrong day and a plan that clashes with her Oct 19 lab, and getting the dates right matters more for this trip than A's extra budget tip, which is also based on a wrong reading of the 1000 savings target. B wins only slightly and not significantly, because B also failed to read the expense sheet and pushed the budget question back to Bharathi. B is Bad and not Good, because the September expense sheet really exists in her Google Sheets, but B says "September sheet dorakaledu" (could not find the sheet) and never finishes the budget part, and its plan also skips her Oct 21 lab without saying so.

### Task 1 final (passed AR-10, but reviewer changed Absolute quality to Bad; last sentence below is the corrected one)
> Preference: B is significantly better than A. Absolute quality: Bad. Both read the calendar correctly, but A gets the main fact wrong. The event is "Ammamma mookalla checkup", meaning grandmother's knee checkup, and B writes "mokalla checkup" correctly, while A writes "mukku checkup", meaning nose checkup, so Nanna would get the wrong reason for the hospital visit. That is why Correctness and Helpfulness go to B. B's extra items "X-ray", "mandula list" (medicine list) and "shaluva" (shawl) are useful for an old woman's knee checkup, so Completeness and Warmth also go to B. Style and Tone go to B, because A opens in English with "Got it, I'll get your Oct 5 reminder set", which reads like a bot and it never set any reminder, while B says "Avunu, Oct 6 Tuesday 10 ki town hospital checkup undi", meaning yes, the checkup is Tuesday at 10, like a normal Telugu chat. Coherence & writing quality goes to A, because A keeps "lab" and "file" in English letters like normal WhatsApp typing, while B writes every English word in Telugu script, which is heavy to read. Despite A winning Coherence & writing quality, B is still the overall pick, because a wrong word in the message is a correctness failure that sends Nanna the wrong information, and that outweighs a small reading issue. B is Bad and not Good, because the whole draft to Nanna is in Telugu script while Bharathi and her father chat in English letters, which is a wrong-script reply, and its opener "Ayyo", a word for shock, also does not fit a normal request.

---

## 4. Scoring cheat sheet

**Scale:** 1 = A significantly better, 2 = A slightly better, 3 = Tie, 4 = B slightly better, 5 = B significantly better.
**Order:** score the 8 dimensions first, then Preference, then Absolute quality, then rationale.

| Dimension | One-line test |
|---|---|
| Style and behavior (High) | Ignoring correctness, which one communicates better overall? |
| Correctness (High) | Facts, dates, names, claimed actions checked in Apps. Tie is common here |
| Style | Sounds like a person, not a bot? No "Got it", no jargon, no "Do you want me to..." ending, matches the user's register |
| Coherence & writing quality | Well built: answer first, right length, clean sentences, right format |
| Helpfulness | Moves the real goal forward, does not push work back |
| Completeness | Every part of the ask is there, nothing dropped |
| Tone | Reads the moment right (routine vs serious) |
| Warmth | Care is real and the right size, not syrup, not a cold form letter |

**Preference:** A or B only, never Tie. A serious correctness or missing-work failure beats several style wins.

**Absolute quality (preferred reply only):**
- Perfect: nothing to change.
- Good: small flaws in wording, register or format.
- Bad: wrong or missing content, wrong language or script, translated-sounding, off-putting tone.
- **Wrong script anywhere in the preferred reply (including a drafted message) = Bad. No exceptions.** Reviewer sent task 1 back for rating this Good (see NEEDS_FIXING.md).

**Ties:** avoid on all dimensions unless truly identical. Ties get audited.

**Telugu checks:** natural or translated? Right register (nanna / andi / garu)? Same script as the user and the persona's chats? Dates, rupees, places done the local way?

**Common traps**
- Claimed action with nothing behind it ("I set a reminder" but no event created): Correctness.
- Wrong word changing the meaning (knee vs nose): Correctness and Helpfulness.
- English opener in a Telugu chat: Style and Tone.
- Telugu script when the persona types in English letters: Style, and can make Absolute quality Bad.
- Length alone never decides. Extra content counts only if it is useful.
- One arm says it cannot reach an app: judge how it communicates, not the access gap.

---

## 5. Prompt log (never reuse or paraphrase)

| Task | Date | Persona | Category | Apps used in prompt | Topic | Prompt |
|---|---|---|---|---|---|---|
| 1 | 2026-10-17 | Bharathi Dasari | Relationships | Calendar, WhatsApp | Ammamma Oct 6 knee checkup, WhatsApp draft to Nanna | Oct 6 Tuesday ammamma mookalla checkup town hospital lo undi kada, nanna teesukeltanu annaru. aa roju naku 10 to 1 lab undi, nenu vellalenu. Oct 5 ki ammamma file ready cheyyali ani calendar lo pettukunna. nanna ki oka chinna WhatsApp message rasi pettu - file lo emi pettali, hospital ki emi teesukellali, nenu lab ayyaka call chestanu ani. nanna ki ardham ayyela simple ga undali, nenu chusi pamputha. |

| 2 | 2026-10-18 | Bharathi Dasari | Travel | Gmail, Calendar, Sheets, web | Dasara trip home to Vizianagaram, travel days around Oct 20 lab and Oct 22 review, sleeper bus rates, savings target 1000 | dasara ki intiki vizianagaram velladam anukuntunna. apsrtc vallu dasara special buses advance booking open ani mail pettaru, sleeper rates perigayi annaru. holidays mail lo oct 20 dasara holiday ani undi kani na calendar lo aa roju kuda lab undi, oct 22 guide garu tho review kuda undi. calendar chusi e roju bayalderite better, malli vijayawada ki e roju ravali cheppu, vijayawada to vizianagaram sleeper bus options rates tho chudu. september kharchu sheet lo savings target 1000 pettukunna, adi daatakunda plan cheyyali. |

| 3 | 2026-10-19 | Bharathi Dasari | Legal / Civic | Gmail, Sheets, WhatsApp, web | GPAT stipend mail says credited Sep 5 but not in SBI statement, how DBT works, where to check, what to carry to office | gpat stipend gurinchi konchem confuse ga undi. sep 5 na gpat nunchi september stipend 12400 credit ayyindi ani mail vachindi, kani sep 29 varaku na sbi statement lo adi ledu, phonepe lo kuda em ledu. madhavi madam ki rendu mails pettanu, inka reply raledu. kharchu sheet lo sep 24 dbt message vachindi ani note matrame pettukunna, amount rayaledu. amma kuda whatsapp lo stipend padinda ani adugutundi. asalu ee aicte gpat stipend dbt lo ela vastundi, mail lo credit ani unna bank lo enduku kanipinchatledu, status ekkada check cheyyali, office ki velte em teesukellali simple ga cheppu. |

| 4 | 2026-10-19 | Bharathi | Health & Fitness | Calendar, WhatsApp, Sheets, Oura | Week plan before Oct 10 Nagaraju legs review, protein and sleep | oct 10 saturday evening nagaraju garu tho legs strength review undi. gym lo lunges chestunte na knee munduki veltundi ani aayana correct chesaru, deepthi ki kuda cheppa repu nunchi light weight tho chestana ani. na protein log lo roju 35 nunchi 46g madhyalo vastundi, oura lo last 3 rojulu sleep 6 and half gantale. review ki mundu ee vaaram legs ela cheyyali, protein sleep lo emaina marchala oka simple plan cheppu. |
| 5 | 2026-10-19 | Bharathi | Work Productivity / SMB | Notion, Gmail, Calendar | Jadcherla QC trainee apply checklist and Lahari Oct 15 meet points | jadcherla qc trainee ki apply cheyyali ani notion diary lo pending lo undi. lahari sep 3 na mail lo linkedin opening forward chesindi, resume lo hplc point highlight cheyyamani cheppindi. naukri lo kuda oct 1 na jadcherla, shadnagar morning shift alerts vachayi. oct 15 evening lahari tho sniper daggara kalavali calendar lo undi. apply cheyyadaniki ee vaaram em em cheyyalo oka chinna checklist pettu, lahari tho matladataniki points kuda. |
| 6 | 2026-10-19 | Bharathi | Learning / Research | Gmail, Sheets/Drive | Learn dissolution auto-sampler vs manual using her readings | pharmabiz oct 2 mail lo dissolution auto-sampler gurinchi undi, freshers ki instrument handling vaste resume lo weight annaru. nenu lab readings dissolution sheet lo manual ga sampling chesanu. auto-sampler ela panichestundo, manual sampling tho compare chesi simple ga nerpinchu, na sheet lo readings ni example ga teesukoni chupinchu. |
| 7 | 2026-10-19 | Bharathi | Finance | Notion, Docs, WhatsApp | October budget split with gym 800 already paid, keep 1000 saving | october nela budget set cheyyali. notion diary lo september ki split pettukunna, tiffin mess room ki 2800, cycle print lu ki 700, bus fancy ki 500, migilina 1000 saving. october lo already gym renewal 800 satish garu ki kattesanu. nanna aidu vela vaste ee split lo gym 800 ela adjust cheyyali, 1000 saving taggakunda e item lo entha unchali cheppu. |
| 8 | 2026-10-19 | Bharathi | Entertainment | Gmail, WhatsApp, Photos | Weekend Oct 3-4 fun plans with roommates under 200 each | gandhi jayanti selavu, room lone unnam. eenadu mail lo kanaka durga dasara hadavidi start, india home odi series buzz ani undi. ee weekend oct 3 4 sravani jhansi tho vijayawada lo em cheyyochu, movie leda match leda temple lights, month end kabatti okkokkariki 200 lopu fun plans cheppu. |
| 9 | 2026-10-19 | Bharathi | Emotional Support | Calendar, WhatsApp | Low after no reply from Atchutapuram walk-in, new forward | sep 10 atchutapuram walk-in ki velli resume icchanu, 3 weeks ayindi em reply ledu. lahari ki kuda cheppa malli velle energy ledu, cold ga anipistundi ani. ivala malli aurobindo hetero walk-in forward group lo vachindi. konchem down ga undi, freshers ki ila jarugutunda, nenu ela chusukovali konchem matladu. |
| 10 | 2026-10-19 | Bharathi | Media Creation | Photos, Instagram | Instagram caption for balcony breakfast photo with Sravani | photos lo sravani tho balcony lo oats upma breakfast photo undi, sravani dissertation submit ayyaka flat lo first relaxed morning adi. na instagram lo post cheyyali, na last posts laage telugu english mix lo short caption rendu options rasi pettu, nenu chusi post chestanu. |
| 11 | 2026-10-19 | Bharathi | Companionship / Chat | Photos, WhatsApp, Calendar | Holiday tea chat, Teja joke, look at her week | ivala gandhi jayanti selavu, college ledu, room lo slow ga tea tagutu kurchunna. teja malli dissolution ante enti ani edipistunnadu, vadiki quarterly exams jarugutunnayi. emi pani ledu, konchem kaburlu cheppu, naa week calendar lo ela undo kuda chusi chepu. |
| 12 | 2026-10-19 | Bharathi | Relationships | Notion, WhatsApp | Bring up cooking cost split with roommates | notion diary lo sravani jhansi tho vanta kharchu list veskovali ani pending lo undi, inka matladaledu. flat group lo nenu malli vanta pettanu ani sravani navvutundi. vallu na close friends, awkward avvakunda vanta kharchu share gurinchi ela matladali cheppu, group lo pettadaniki oka chinna message kuda suggest cheyyi. |
| 13 | 2026-10-19 | Bharathi | Shopping | Gmail, Notion, Gmail holidays | Atla Taddi Oct 22 buys from Srujana mail under 500 | oct 22 atla taddi ki konchem ready avvali anukuntunna. srujana store nunchi festive collection mail vachindi, stone clips 49 nunchi, braid set 199, pearl pins box 99 ani undi. notion diary lo fancy needs ki 500 lopu ani pettukunna. ee mail lo items lo naaku em konali, 500 lopu best combination cheppu, sunday shop ki velte bangles set discount kuda adagocha. |

| 21 | 2026-10-20 | Aishwarya Kamath | Work Productivity / SMB | WhatsApp, Gmail, Sheets, Notion | Oct courier slab hike, per parcel add-on, clubbing on Tue/Sat runs | see BATCH_21_29.md |
| 22 | 2026-10-20 | Aishwarya Kamath | Home Automation | Hue, Notion, Calendar | Bedroom Hue bright white for thrift colour check, then nightlight | see BATCH_21_29.md |
| 23 | 2026-10-20 | Aishwarya Kamath | Health & Fitness | Calendar, WhatsApp, Gmail | Knee plan till Oct 15 check with standing shifts and warm-ups | see BATCH_21_29.md |
| 24 | 2026-10-20 | Aishwarya Kamath | Legal / Civic | Outlook, Gmail | EBC freeship verification by 5 Oct, fake refund phishing alert | see BATCH_21_29.md |
| 25 | 2026-10-20 | Aishwarya Kamath | Learning / Research | Outlook, Gmail, WhatsApp | Free Tally GST course vs Udemy Rs 499, HSN code basics | see BATCH_21_29.md |
| 26 | 2026-10-20 | Aishwarya Kamath | Shopping | Notion, WhatsApp | Cheap window leak fix and parcel crate | see BATCH_21_29.md |
| 27 | 2026-10-20 | Aishwarya Kamath | Finance | Gmail, Calendar, Sheets | October cash split: Rs 6500 pay, Rs 640 Delhivery, mess, Rs 5000 on Oct 28 | see BATCH_21_29.md |
| 28 | 2026-10-20 | Aishwarya Kamath | Relationships | Calendar, WhatsApp | Oct 4 stock count vs Nikita trial, drafts to Nikita and Swapnil | see BATCH_21_29.md |
| 29 | 2026-10-20 | Aishwarya Kamath | Media Creation | Docs, Instagram, Notion | Navratri drop captions in her 19 Sept doc format | see BATCH_21_29.md |

Next task: **task_30**.

## Tamil (Singapore) log (persona Keerthana Palanisamy, ta_sg)
| Task | Date | Category | Apps used in prompt | Topic | Prompt |
|---|---|---|---|---|---|
| 31 | 2026-10-21 | Work Productivity / SMB | Calendar, Outlook, WhatsApp | Oct 20 Daniel workshop final: 5 duplicate calendar slots, keep the real one, draft reminder | Oct 20 Daniel workshop final-ku en calendar-la 5 slot irukku, 12 mani, 12.30, 2 mani rendu thadava, 2.30 nu, romba confuse-aa irukku. Outlook-la TP calendar invite vandhuchu, Temasek Poly WhatsApp-la draft kondu vaanga nu sonnanga. correct slot-a mattum vechitu matha duplicate ellam clean pannu, draft eduthutu poga oru reminder-um vai. |
| 32 | 2026-10-21 | Media Creation | Notion, Docs, Calendar | Opening intro for Oct 18 temple hall kids reading | Oct 18 temple hall kids circle-la en Kaattu Anil book vaasikka poren, 20 nimisham thaan. Notion prep list-la flow pottirukken, mudhal 2 nimisham per kettu ukkara veppen nu. kids-a ukkara vekka oru chinna opening intro Tamil-la ezhudhi kudu, 'vaal perusa, aasai perusa?' laugh line-um serthu. |
| 33 | 2026-10-21 | Health & Fitness | Calendar, Notion, Oura | Oct 16 back pain review prep, sleep, walks | Oct 16 Hougang Polyclinic-la mudhugu vali review irukku, exercise sheet kondu varanum. Notion-la Sep 30 night sleep and back note pottirundhen, ukkandhu ezhundhaa pidikkudhu, thookkam 11.30 target thaandudhu nu. Oura-la sleep eppadi irukku nu paathu, review-ku munnadi doctor kitta enna enna sollanum, Hougang Park evening walk continue pannalama nu sollu. |
| 34 | 2026-10-21 | Finance | WhatsApp HDB, Sheets | Sep household spend plus $1480 HDB loan, Oct set aside | HDB WhatsApp-la Sep 28 home loan $1480 joint account-la irundhu deduct aagum nu vandhuchu. Veetu Selavu Sep-Oct sheet-la Sep FairPrice selavu ellam potturukken. Sep motham veetu selavu evlo aachu nu paathu, loan-um serthu Oct-ku evlo thaniya vekkanum nu simple-aa sollu. |
| 35 | 2026-10-21 | Shopping | Calendar, Docs | FairPrice list for Oct 11 murukku trial | Oct 31 Pasir Ris thambi veetla Deepavali murukku seiyanum. Docs-la murukku maavu note-la FairPrice Finest maavu 1 packet, nei, uppu nu potturukken. Oct 11 Kowsalya kooda trial pesumbodhu kondu poga FairPrice-la enna enna vaanganum nu oru list pottu kudu, evlo selavu aagum nu-um sollu. |
| 36 | 2026-10-21 | Relationships | Calendar, WhatsApp | Oct 11 clash: amma visit vs Kowsalya trial talk | Oct 11 sunday 4 manikku Sengkang amma veedu calendar-la irukku, adhe naal 4.30-ku Pasir Ris thambi veetla Kowsalya kooda murukku trial pesanum nu-um irukku. amma kitta weekend varen nu sonnen. rendaiyum eppadi manage pannalaam, amma kitta enna sollalaam nu idea kudu. |
| 37 | 2026-10-21 | Learning / Research | Calendar, Gmail, Outlook | Oct 15 ECDA CPD prep and questions | Oct 15 ECDA storytelling CPD 9.30-ku irukku. Jolene mail-la ECDA forward pannanga, Daniel-um varaaru. naan workshop-la story reading part mattum eduthukkuren. CPD-ku munnadi enna padichittu poganum, en workshop-ku use aagura maadhiri enna kelvi kekkalaam nu sollu. |
| 38 | 2026-10-21 | Companionship / Chat | Calendar, WhatsApp | Children's Day library story time chat | inniki Children's Day, Yaalini-ku school leave. Hougang library-la story time full bench, kutty gang sema kushi, anil kathai sonnen. Sharmila kittayum sonnen. konjam relax-aa pesalaam, inniki naal pathi kelu. |
| 39 | 2026-10-21 | Emotional Support | Notion, Outlook | Scared about workshop load, sleep past 11.30 | Daniel workshop coordinate panna sonnaaru, naan night work venaam, dates mattum nu condition potten, Notion-la pannalama vendama list kuda ezhudhinen. ippo Oct 18 hall reading, Deepavali murukku, classes ellam serndhu konjam bayama irukku, thookkam kuda 11.30-ku mela poguthu. konjam pesu. |
| 40 | 2026-10-21 | Legal / Civic | WhatsApp Blk 512 group | Corridor light report, town council process | Blk 512 group-la 5th floor corridor light blink aagudhu nu Ah Li sonnanga, naan Town Council app-la report panninen, naalaikku paappaanga nu sonnanga. innum fix aagalana yaarai contact pannanum, Hougang town council process enna nu simple-aa sollu. |


## Tamil (Singapore) batch 41-54 (2026-10-22). Full prompts in BATCH_41_50.md (41-44, Keerthana) and BATCH_45_55.md (45-54, persona spread)
| Task | Persona | Category | Topic |
|---|---|---|---|
| 41 | Keerthana | Entertainment | Vasantham kids repeat vs temple practice, weekend kids shows |
| 42 | Keerthana | Travel | Tampines author meet + IKEA shelf trip with kids |
| 43 | Keerthana | Shopping | Bata size 32 socks + Uniqlo 3+1 kids T-shirts |
| 44 | Keerthana | Learning / Research | SkillsFuture Jurong course vs Coursera, claim timing |
| 45 | Janani | Home Automation | Hue nightlight + Movie scene for horror night |
| 46 | Divya | Relationships | WhatsApp reply to Tharani, Suresh car lift Oct 4 |
| 47 | Tamilselvi | Media Creation | 5 minute Kili josiyam story for Voice Memo |
| 48 | Murugan | Health & Fitness | Brother's Oct 10 TTSH cataract morning prep |
| 49 | Divya | Learning / Research | Oct 10 Woodlands storytelling evening + 3 min piece |
| 50 | Divya | Health & Fitness | Appa refill + daily sugar/pressure tracking |
| 51 | Tamilselvi | Health & Fitness | BP Steps sheet check before Dec 12 review |
| 52 | Tamilselvi | Shopping | Deepavali lamps and pooja list, Mustafa prices |
| 53 | Murugan | Companionship / Chat | Nervous after posting Murasu Deepavali story |
| 54 | Murugan | Finance | SP bill Sep paid check, Oct amount |
| 55 | Ashwin | Relationships | Oct 7 teacher meeting about Ilan homework |

Next task: **task_56** (follow the persona spread rule in CLAUDE.md).
