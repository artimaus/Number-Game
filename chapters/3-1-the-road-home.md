# Chapter 9 · The Road Home

**Arc 3 · The Stolen Crown** · Level 9 · numbers 1–20, adding and taking away within 10 · 5 tasks per stop · army
from 2 to 4 companies · about 11 sets.

The storm blows away and the army marches down out of the hills into Brightvale's autumn farmland: golden fields,
haystacks and orchards heavy with apples. But grey-cloaked guards hold every bridge "by order of the steward", and
{Uncle Grimbald|Aunt Grimhilda} is sitting on the throne. This chapter brings the first **fork in the road**, the
army's **companies of ten**, and one new task: **make a company** (how many more make ten?). Its captain is
**Sergeant Stompwell**, who stomps his enormous boots whenever he's cross.

Conventions (N:, H:, [Hero], ★★/★, clip keys, {uncle|aunt} steward lines) are as in
[chapter 1](1-1-the-border-road.md) and [chapter 5](2-1-the-stone-bridge.md). New for arc 3:
- **The Grey Guards** are ordinary Brightvale folk in grey cloaks and tall grey helmets that wobble down over their
  eyes. They follow the steward's orders, but their hearts aren't in it.
  - **At a skirmish,** once beaten, they throw off their grey cloaks and **join the army**: "We never liked those
    cloaks anyway!" As many join as the red disc showed.
  - **At a fort,** they run off with their captain, as the goblins and trolls did.
- **Companies of ten.** Every ten soldiers march together under a company banner, and up to nine more march loose in
  front. When the loose soldiers reach ten they form a new company: "Ten soldiers! A new company!" The gold disc shows
  the whole army (say 34); the herald says it in companies: "We have 3 companies and 4 soldiers!" That way he never
  needs a number past 10 to say it.
- **Recruiting in arc 3:**
  - A village with half or more right first time (3 of 5) sends a group: one friend for each right answer (3 to 5).
    (About 20 a chapter in all, as each castle needs 2 companies more than the last, so the fork's choice matters.)
  - A fork's recruit stop sends a whole company if half or more are right (5 soldiers if not).
  - A special stop sends 3 soldiers and a camp treasure.
  - Guards beaten at a skirmish join.
  - At the cap (10 companies), recruits become gear.
- **The fork.** At a crossroads Buckleberry holds up two signposts, each with a picture of its place, and says their
  names: "Which way shall we go? Windmill Hill… or the Apple Orchard?" The child taps one. The road strip splits in two
  there and joins again before the fort. The branch not taken stays open: the army can march back to it.
- **Troops matter.** Each fort needs a number of companies (this one needs 4).
  - Before the siege the herald counts the army with the child.
  - If the army is short by less than ten, working out the gap is a make-a-company task: "3 companies and 6 soldiers.
    How many more make 4 companies?"
  - Then the army marches back to the branch it skipped, recruits there and returns.
  - Still short after both branches? The loyal villages send the rest ("Harvest Hollow sent more friends!"). Nobody is
    ever stuck.
- **5 tasks per stop.** A fight is won with 3 or more right on the first try.
- A player who starts in arc 3 (a grown-up setting) brings **2 companies** (20 soldiers) from the hills.

---

## The road

| # | Stop | Kind | Sets | Earns |
|---|---|---|---|---|
| 0 | Home from the hills | Opening (first play only) | – | – |
| 1 | Harvest Hollow | Village | 1 | 3–5 recruits |
| 2 | The Grey Bridge | Skirmish: the first Grey Guards | 1+ | The guards join |
| 3 | The Crossroads | **Fork** | – | Pick a branch |
| 3a | Windmill Hill | Recruit stop | 1 | A whole company |
| 3b | The Apple Orchard | Special | 1 | 3 recruits and a **big orange pumpkin** for the camp |
| ⛺ | *Camp* | | | |
| 4 | The Hay Wagons | Skirmish | 1+ | The guards join |
| 5 | Market Cross | Village | 1 | 3–5 recruits; the steward's big lie |
| 6 | The Toll Castle | Troop check, then siege | 3+ | The castle, and the chapter |
| ⛺ | *Camp: chapter end* | | | |

**Troops:** the army starts at 2 companies and the Toll Castle needs 4. Through Windmill Hill a child who does well
gathers about 25 more; through the Apple Orchard, about 18, so a small army may need to march back for the millers.

## Level 9 tasks

| Task | Numbers | On screen | Cards |
|---|---|---|---|
| **Find the number** | 1–20 | Banners | 4 banners |
| **Count them** | 1–20, in rows of 5 above 10 | In the scene | 4 shields |
| **Adding** | Totals up to 10, with the sentence (3 + 4 = ?) | Things arrive | 4 shields |
| **Taking away** | Within 10, with the sentence (8 − 3 = ?) | Things leave | 4 shields |
| **What comes next? / Countdown** | Up to 20 / down from 20 | Stepping stones | 3 numeral stones |
| **Which number is bigger?** | Up to 20 | Two guards holding up shields | Tap a shield |
| **Make a company** (new) | Up to 10 | A company's ten-frame banner with some soldiers | 4 shields |

- Arc 2's early tasks (find the sign, count and compare, look closely) drop out of the mix; the time goes to adding and
  taking away.

### New: Make a company (how many more make ten?)
- **H:** "7 soldiers. How many more make a company?" `num_7` + `w_soldiers` + `h_more_company`
- **On screen:** a company banner on a pole, with a ten frame painted on it: two rows of five spots. Soldiers stand in
  7 of the spots, and 3 spots are empty.
- **Right:** the missing soldiers march in and fill the frame, one per spot, as he counts on: "8, 9, 10!" Then:
  "7 and 3 make ten!" `num_7` + `and` + `num_3` + `make_ten`, and the banner flies.
- **Help:** count the empty spots together, pointing at each; then the right shield pulses.
- **Where it comes from:** the troop check before each fort asks the same question with the army.
- **Tracked as** `ten:7`.

---

## 0 · Home from the hills (opening)
*The storm clouds roll away. The army marches down into golden autumn fields; far off, the towers of Brightvale's
capital.*
- **N:** "At last the storm blew away, and the army marched down from the hills, toward home." `st3_1_01`
- **N:** "But at the first bridge stood guards in grey cloaks. 'By order of the steward,' they said, 'nobody passes!'"
  `st3_1_02`
- **N:** "{Uncle Grimbald|Aunt Grimhilda} was sitting on the king's throne. 'The crown has been stolen,' {he|she} said,
  'so I shall rule until it is found!'" `st3_1_03` · *steward line*
- **H:** "Forward, march! Let's find that crown!" `h_forward_march` + `h_find_crown`

## 1 · Harvest Hollow (village)
*Fields of wheat and pumpkins, a big red barn, farmers with pitchforks and baskets.*
- **N:** "In Harvest Hollow the farmers were bringing in the harvest." `st3_1_04`
- **H:** *(fanfare)* "Hello, villagers! Who will join us?" `h_hello_village`
- ★★ Adding: "3 pumpkins… and 4 more! How many now?" · ★ Count: "How many haystacks?" `how_many_haystacks` · ★
  Taking away (crows fly off with ears of corn) · ★ Find
- **Half or more right:** a group of farmers marches over, pitchforks and all. **H:** "4 friends join us!" `num_4` +
  `h_join_us`. The gold disc goes up by 4 at once (20 → 24).
- **N:** "The farmers of Harvest Hollow joined the march." `st3_1_05`

## 2 · The Grey Bridge (skirmish): the first Grey Guards
*A stone bridge over a brook. Guards in grey cloaks and wobbly grey helmets cross their pikes across it.*

**Arrive**
- **N:** "Grey guards stood on the bridge. 'Halt! Nobody passes, by order of the steward!'" `st3_1_06`
- **H:** "Guards in grey! Don't worry, [Hero]. Let's show them how clever we are!" `h_guards_first` + title + name +
  `h_show_clever`. (Later skirmishes: "Grey guards! Let's be clever!" `h_guards`.)

**Tasks** (5)
- ★★ Taking away: "8 guards… 3 go home for tea! How many are left?" `num_8` + `w_guards` + `num_3` + `go_home` +
  `how_many_left`
- ★ Adding · ★ Make a company · ★ Which number is bigger? (two guards hold up shields) · ★ Count guards

**Each first-try right answer:** a guard's helmet wobbles down over his eyes. "Hey, who turned out the lights?"

**Won (3 or more of 5)**
- The dust cloud and the discs, as before; then the guards come out of the cloud, **throw their grey cloaks in the
  air**, and walk over to our side. The red disc flies over to the gold one and they add up with a clink.
- **H:** "They threw off their grey cloaks! They're on our side!" `h_cloaks_off`, then "4 guards join us!" `num_4` +
  `h_join_us`
- **N:** "'We never liked those scratchy cloaks anyway,' said the guards, and they joined the march." `st3_1_07`

**Not yet (0 to 2 of 5)**
- The retreat, as in arcs 1–2. **N:** "Oops! The grey guards held on that time." `st_retreat_guards` (shared by
  all of arc 3). **H:** "That's all right. Let's try again!" `h_try_again`

## 3 · The Crossroads (fork)
*A crossroads with a big old signpost. One arm points up a hill to a windmill; the other down a lane to an orchard.*
- **N:** "At the crossroads, the road split in two." `st3_1_08`
- **H:** "Which way shall we go? Windmill Hill… or the Apple Orchard?" `h_which_way` + `fork_windmill` + `or` +
  `fork_orchard`
- Two big signpost cards with pictures: the windmill, the orchard. The child taps one; the army turns that way.
- **The first time:** the road strip on screen splits, and he points: "We can come back for the other one!"
  `h_come_back`

## 3a · Windmill Hill (recruit stop)
*A big windmill turning slowly, sacks of flour, the millers dusted white from head to toe.*
- **N:** "On Windmill Hill, the millers were grinding flour. They were very strong from carrying all those sacks!"
  `st3_1_09`
- ★★ Make a company: "7 sacks of flour on the cart. How many more make ten?" (the ten frame is a cart with ten
  places) · ★ Adding · ★ Taking away · ★ Count: "How many sacks?" `how_many_sacks` · ★ Find
- **Half or more right:** a whole company marches down the hill, white with flour: "A whole company! Ten soldiers!"
  `h_whole_company`. The loose soldiers and the new ten line up, and a new company banner goes up.
- **Fewer:** 5 millers join. "5 friends join us!"
- **N:** "The millers dusted off their hats and joined the march." `st3_1_10`

## 3b · The Apple Orchard (special)
*Rows of apple trees, ladders, baskets. The grey guards have kicked the baskets over, and apples have rolled
everywhere.*
- **N:** "In the orchard, the grey guards had kicked over the apple baskets!" `st3_1_11`
- **H:** "Let's pick up the apples!" `h_pick_apples`
- ★★ Adding: "4 apples in the basket… and 3 more!" · ★ Taking away: "9 apples… a pony eats 2!" `pony_eats` · ★ Make a
  company (a basket with ten places) · ★ Count apples · ★ Which number is bigger?
- **Each first-try right answer:** a few apples roll back into a basket.
- **End:** the baskets are full. 3 apple pickers join, and the orchard folk give the biggest pumpkin in the field.
  - **H:** "A present for our camp!" `h_camp_gift`
  - **N:** "The apple pickers joined the march, and gave the army the biggest pumpkin in Brightvale." `st3_1_12`

## ⛺ Camp
As before; at camp the herald says the army in companies: "We have 3 companies and 1 soldier!" `we_have` + `num_3` +
`w_companies` + `and` + `num_1` + `w_soldier`. The pumpkin (if won) sits by the fire.

## 4 · The Hay Wagons (skirmish)
*Hay wagons stopped on the road, and grey guards poking the hay with their pikes, looking for "the crown thief".*
- **N:** "Grey guards were poking through the hay wagons. 'We're looking for the crown thief!' they said." `st3_1_13`
- **H:** "Grey guards! Let's be clever!" `h_guards`
- ★★ Adding · ★ Make a company · ★ Taking away · ★ Count guards · ★ What comes next?
- **Won:** the cloaks fly off; the guards join. **N:** "The guards jumped down from the hay, and joined our march
  instead." `st3_1_14`

## 5 · Market Cross (village)
*A market square with stalls and a town crier ringing his bell.*
- **N:** "In Market Cross, the town crier was ringing his bell. 'Hear ye! The steward says our hero stole the
  crown!'" `st3_1_15`
- **N:** "'Nonsense!' cried the market folk. 'Our hero would never do that!'" `st3_1_16`
- ★★ Taking away (market stall: "10 pies… 4 are sold!") · ★ Adding · ★ Count · ★ Make a company · ★ Countdown
- **Half or more right:** a group joins.
- **N:** "'The Toll Castle is just ahead,' said the crier. 'Sergeant Stompwell guards it, and he stomps!'" `st3_1_17`

## 6 · The Toll Castle (troop check, then siege)
*A square stone castle straddling the road, with a toll gate and a great wooden door. On the wall: Sergeant Stompwell, a
round man with a moustache and enormous boots, stomping.*

**Arrive**
- **N:** "There stood the Toll Castle. On the wall, Sergeant Stompwell stomped his enormous boots. STOMP! STOMP!"
  `st3_1_18`

**Troop check**
- **H:** "Let's count our army!" `h_count_army`. The companies' banners light up one by one: "We have 3 companies and 6
  soldiers!" (the gold disc pops), then "We need 4 companies!" `h_we_need` + `num_4` + `w_companies`
- **Enough:** "Enough soldiers! Let's take the castle!" `h_enough`
- **Short, by less than ten:** a make-a-company task with the loose soldiers on the company banner: "6 soldiers. How
  many more make a company?" Right: "4 more!" `num_4` + `more`. Then: "Let's go back for more friends!"
  `h_go_back`
  - The army marches back to the crossroads and down the branch it skipped (Windmill Hill or the Apple Orchard), then
    returns and counts again.
  - Still short after both branches: "Harvest Hollow sent more friends!" `h_loyal_send`, and they march in until the
    army has enough.

**Build 1: ladders** (5 tasks, can't fail) · minimum **3**
- ★★ Find · ★ Count: "How many logs?" · ★ Adding · ★ Make a company · ★ What comes next?

**Build 2: the battering ram** (5 tasks, can't fail) · minimum **the log and the wheels**, as in arc 2.

**Assault** (5 tasks)
- ★★ Taking away: "9 guards on the wall… 4 run inside!" · ★ Adding · ★ Count guards · ★ Make a company · ★ Which
  number is bigger?
- **Won:**
  - *BOOM… BOOM… CRASH!* The gate falls; the dust cloud and the discs. The guards run off with Sergeant Stompwell,
    stomping all the way.
  - **H:** "Hooray! The castle is ours!" `h_castle_ours`
  - **N:** "Sergeant Stompwell stomped all the way to the River Towns, STOMP, STOMP, STOMP." `st3_1_19`
- **Not yet:** the retreat; the ladders and ram stay.

**Chapter end**
- **N:** "The road home was open. And somewhere in Brightvale, the real crown was hidden…" `st3_1_20`
- The victory screen, then camp.

---

## When the road is blocked
If the child isn't at level 10 yet when the castle falls:
- **N:** "Sergeant Stompwell had wound up the drawbridge on the river road, and nobody could lower it." `st3_1_21`
- **H:** "The road is blocked! We'll find a way soon." `h_road_blocked`
- The six dots under the block fill as in arc 2.

| Raid | Scene | Narrator | Favoured |
|---|---|---|---|
| Harvest Hollow | Grey guards "inspecting" the pumpkins, and dropping them | "Oh no! Grey guards were bothering Harvest Hollow!" `st3_1_r1` | Adding |
| Windmill Hill | Guards jamming the windmill sails | "Oh no! Grey guards had stopped the windmill!" `st3_1_r2` | Make a company |
| Market Cross | Guards pinning up "Wanted: the crown thief" posters | "Oh no! Grey guards were putting up silly posters in Market Cross!" `st3_1_r3` | Taking away |

- **H:** "Grey guards are back! To the village!" `h_raid_guards`. Beaten raiders run off (they don't join).
- **Cleared (level 10):** **N:** "The millers pulled together, and down came the drawbridge!" `st3_1_22` · **H:**
  "The road is clear! Onward!" `h_road_clear`

---

## New clips in this chapter
- **Herald:**
  - Army: `w_company` "company", `w_companies` "companies", `w_soldier` "soldier", `h_new_company` "Ten soldiers! A
    new company!", `h_join_us` "…join us!", `h_whole_company` "A whole company! Ten soldiers!"
  - The fork: `h_which_way` "Which way shall we go?", `or` "…or…", `h_come_back` "We can come back for the other one!",
    `fork_windmill` "Windmill Hill", `fork_orchard` "the Apple Orchard"
  - Troop check: `h_count_army` "Let's count our army!", `h_we_need` "We need…", `h_enough` "Enough soldiers! Let's
    take the castle!", `h_go_back` "Let's go back for more friends!", `h_loyal_send` "The loyal
    villages sent more friends!"
  - Guards: `h_guards_first` "Guards in grey! Don't worry,", `h_guards` "Grey guards! Let's be clever!",
    `h_cloaks_off` "They threw off their grey cloaks! They're on our side!", `h_raid_guards` "Grey guards are back! To
    the village!", `h_castle_ours` "Hooray! The castle is ours!"
  - Make a company: `h_more_company` "How many more make a company?", `make_ten` "make ten!"
  - `h_find_crown` "Let's find that crown!", `h_pick_apples` "Let's pick up the apples!", `go_home` "…go home for
    tea!", `pony_eats` "A pony eats…", `are_sold` "…are sold!", `roll_away` "…roll away!" (and `go_away` "…go away!"
    for anything else that leaves). Flour sacks use arc 2's "We give away…".
  - `how_many_haystacks`, `w_guards`, `w_haystacks`, `w_pumpkins` and the which-more clips for the new things
- **Narrator:** `st3_1_01` … `st3_1_22`, `st3_1_r1` … `st3_1_r3`, and the shared `st_retreat_guards`. That's 26
  lines.
