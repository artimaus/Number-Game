# Chapter 12 · The Crown Tower

**Arc 3 · The Stolen Crown** · Level 12 · adding and taking away within 10; counting in tens to 100 · 5 tasks per stop
· army from 8 to 10 companies · about 11 sets. **Arc finale.**

The second note said "Take the crown to the Crown Tower, where nobody will ever find it." The road climbs to the sea
cliffs at sunset: puffins, fishing boats, signal fires, and on the highest cliff the steward's tall Crown Tower. The
steward is there, with **Sir Snivelwick**, a nervous little man who carries the steward's enormous ring of keys. Two new
tasks arrive: **count the companies** (counting in tens to 100) and **the missing number** (4 + ? = 9). The finale needs
the whole army: **10 companies, 100 soldiers**. Conventions are as in [chapter 1](1-1-the-border-road.md),
[chapter 5](2-1-the-stone-bridge.md) and [chapter 9](3-1-the-road-home.md).

## The road

| # | Stop | Kind | Sets | Earns |
|---|---|---|---|---|
| 0 | To the sea cliffs | Opening (first play only) | – | – |
| 1 | Puffin Point | Village | 1 | 5–7 recruits |
| 2 | The Cliff Path | Skirmish | 1+ | The guards join |
| 3 | The Lookout Stone | **Fork** | – | Pick a branch |
| 3a | The Fishing Village | Recruit stop | 1 | A whole company of fisherfolk |
| 3b | The Smugglers' Cove | Special | 1 | 3 recruits and a **sea chest** for the camp |
| ⛺ | *Camp* | | | |
| 4 | The Signal Fires | Skirmish | 1+ | The guards join |
| 5 | Tower Town | Village | 1 | 5–7 recruits; a warning about the tower |
| 6 | The Crown Tower | Troop check, then siege | 3+ | **The crown**, and the arc |
| 🎉 | *The crown feast (arc end)* | | | The **Crown Medal** and a **royal banner** for the camp; then bad news from the capital |

**Troops:** the Crown Tower needs **10 companies**, the whole army: 100 soldiers.

## Level 12 tasks
Everything from level 11 stays in the mix, plus:

| Task | Numbers | On screen | Cards |
|---|---|---|---|
| **Count the companies** (new) | Tens, 10 to 100 | Company banners, each a full ten frame | 4 shields with tens (30, 40, 50, 60) |
| **The missing number** (new) | Within 10 | The sentence with a gap: 4 + ? = 9, over a row of spots | 4 shields |

### New: Count the companies
- **H:** "How many soldiers in 4 companies?" `h_how_many_in` + `num_4` + `w_companies`
- **On screen:** 4 company banners in a row, each a full ten frame of soldiers.
- **Right:** each banner lights as he counts in tens: "10, 20, 30, 40! 4 companies… 40 soldiers!" `num_4` +
  `w_companies` + `num_40` + `w_soldiers`
- **Help:** count in tens together, banner by banner, then the right shield pulses. (If needed, the first banner counts
  in ones, 1 to 10, to show why it's a ten.)
- **Why:** it's the bridge to arc 4 (tens and ones): the army already marches in tens.
- **Tracked as** `tens:4`.

### New: The missing number
- **H:** "4 plus what makes 9?" `num_4` + `plus` + `what_makes` + `num_9`
- **On screen:** the sentence **4 + ? = 9** on a signpost; underneath, a row of 9 spots with soldiers in 4 of them.
- **Right:** soldiers march into the 5 empty spots as he counts on: "5, 6, 7, 8, 9! 4 plus 5 makes 9!" `num_4` +
  `plus` + `num_5` + `makes` + `num_9`
- **Help:** count the empty spots together; then the right shield pulses.
- **Why:** make a company (7 and ? make 10) and hiding (8 is 5 and ?) were this all along, and here it is as a
  sentence.
- **Tracked as** `miss:4+5`.

---

## 0 · To the sea cliffs (opening)
*The forest ends at the sea. Cliffs glowing in the sunset, puffins, fishing boats; far along the cliffs, a tall dark
tower.*
- **N:** "Beyond the forest, the road climbed to the sea cliffs. On the highest cliff stood the Crown Tower."
  `st3_4_01`
- **N:** "{Uncle Grimbald|Aunt Grimhilda} was there, with Sir Snivelwick, who carried all the steward's keys."
  `st3_4_02` · *steward line*
- **H:** "The crown must be in that tower! Forward, march!" `h_crown_tower` + `h_forward_march`

## 1 · Puffin Point (village)
*Cottages on the clifftop, puffins everywhere: on the roofs, the walls, the washing lines.*
- **N:** "Puffin Point was a village where the puffins walked about as if they owned it." `st3_4_03`
- ★★ The missing number · ★ Count the companies · ★ Just the numbers · ★ Hiding (puffins in their burrows) · ★
  Adding
- **Half or more right:** a group joins. **N:** "The people of Puffin Point joined the march, and so did one very
  determined puffin." `st3_4_04`

## 2 · The Cliff Path (skirmish)
*A narrow path along the cliffs, with the sea below. Grey guards in a line across it, holding onto their helmets in the
wind.*
- **N:** "On the cliff path, grey guards held on to their helmets in the wind. 'Nobody passes!'" `st3_4_05`
- **H:** "Grey guards! Let's be clever!" `h_guards`
- ★★ The missing number · ★ How many more · ★ Taking away · ★ Count the companies · ★ Hiding
- **Won:** the cloaks fly off (and blow away over the sea); the guards join. **N:** "The wind blew the grey cloaks
  away over the sea, and the guards cheered and joined the march." `st3_4_06`

## 3 · The Lookout Stone (fork)
*A big flat rock with a view down both ways: a fishing village in a bay, and a hidden cove in the rocks with a strange
boat.*
- **N:** "From the Lookout Stone, they could see a fishing village, and a secret cove." `st3_4_07`
- **H:** "Which way shall we go? The Fishing Village… or the Smugglers' Cove?" `h_which_way` + `fork_fishing` + `or` +
  `fork_cove`

## 3a · The Fishing Village (recruit stop)
*Boats pulled up on the shingle, nets drying, lobster pots.*
- **N:** "In the fishing village, the fisherfolk were mending their nets." `st3_4_08`
- ★★ Count the companies (boats, each with ten fisherfolk) · ★ The missing number · ★ Make a company · ★ Adding · ★
  Taking away
- **Half or more right:** a whole company of fisherfolk joins. "A whole company! Ten soldiers!" `h_whole_company`
- **N:** "The fisherfolk left their nets on the beach, and joined the march." `st3_4_09`

## 3b · The Smugglers' Cove (special)
*A cave in the rocks, and in it the steward's secret boat, loaded with things taken from the villages: baskets, clocks,
teddy bears, a rocking horse.*
- **N:** "In the cove was the steward's secret boat, full of things taken from the villages!" `st3_4_10`
- **H:** "Let's give everything back!" `h_give_back`
- ★★ Taking away ("9 teddy bears… we give back 4!") · ★ The missing number · ★ Hiding (things in the boat) · ★ Adding
  · ★ How many more
- **Each first-try right answer:** a villager comes down the steps and happily takes something home.
- **End:** everything has gone home. 3 villagers join, and at the bottom of the boat is an old sea chest.
  - **H:** "A present for our camp!" `h_camp_gift`
  - **N:** "At the bottom of the boat was an old sea chest. 'Keep it,' said the villagers. 'You've earned it!'"
    `st3_4_11`

## ⛺ Camp
As before. The sea chest sits by the tent; the camp is getting crowded with treasures.

## 4 · The Signal Fires (skirmish)
*Beacon fires on the cliffs, and grey guards running to light them to warn the tower.*
- **N:** "Grey guards were lighting signal fires to warn the steward that the army was coming!" `st3_4_12`
- **H:** "Grey guards! Let's be clever!" `h_guards`
- ★★ Count the companies · ★ The missing number · ★ Just the numbers · ★ How many more · ★ Countdown
- **Each first-try right answer:** a guard's fire goes out with a puff of smoke.
- **Won:** the cloaks fly off; the guards join. **N:** "The guards put out their fires, and joined the march
  instead." `st3_4_13`

## 5 · Tower Town (village)
*A little town at the foot of the cliff. High above: the Crown Tower, with a light in the top window.*
- **N:** "Tower Town sat at the foot of the Crown Tower." `st3_4_14`
- ★★ The missing number · ★ Count the companies · ★ Adding · ★ Taking away · ★ Hiding
- **Half or more right:** a group joins.
- **N:** "'There's a light at the top of the tower every night,' whispered the townsfolk. 'Sir Snivelwick goes up and
  down with his keys, jingle jangle!'" `st3_4_15`

## 6 · The Crown Tower (troop check, then siege: arc finale)
*A tall dark tower on the cliff edge, a spiral stair outside, a great iron-bound door. On the battlements:
{Uncle Grimbald|Aunt Grimhilda}, arms folded, and Sir Snivelwick jingling his keys.*

**Arrive**
- **N:** "There stood the Crown Tower. On top stood {Uncle Grimbald|Aunt Grimhilda}, with Sir Snivelwick jingling
  his keys." `st3_4_16` · *steward line*

**Troop check**
- **H:** "Let's count our army!" `h_count_army`. The companies light one by one as he counts in tens: "10, 20, 30…
  100!" If it's all ten: "10 companies! 100 soldiers!" `num_10` + `w_companies` + `num_100` + `w_soldiers`
- **H:** "We need 10 companies! That's everyone!" `h_we_need` + `num_10` + `w_companies` + `h_everyone`
- **Short:** a make-a-company task with the loose soldiers, then back to the branch not taken; still short, "The loyal
  villages sent more friends!" `h_loyal_send`, until the army is 100.

**Build 1: ladders**, minimum **3**. **Build 2: the ram**, minimum **the log and the wheels**.

**Assault** (5 tasks)
- ★★ The missing number · ★ Count the companies · ★ Just the numbers · ★ How many more · ★ Taking away
- **Won:**
  - *BOOM… BOOM… CRASH!* The door falls; the dust cloud and the discs. The guards run down the spiral stair and away.
    Sir Snivelwick is so startled that he drops all his keys: *jingle-jangle-CLANG!*
  - **H:** "Hooray! The tower is ours!" `h_tower_ours`
  - **N:** "At the very top of the tower was a locked chest. One of Sir Snivelwick's keys fitted, and inside was…
    the crown!" `st3_4_17`
  - **N:** "{Uncle Grimbald|Aunt Grimhilda} had hidden it {himself|herself}, and told everyone it was stolen!"
    `st3_4_18` · *steward line*
  - **N:** "The steward jumped on a horse, and galloped away to the capital." `st3_4_19`
- **Not yet:** the retreat; the ladders and ram stay.

## 🎉 The crown feast (arc end)
*Long tables on the clifftop at sunset, lanterns, every loyal town there: farmers, millers, sailors, foresters,
fisherfolk, even the puffin. The crown sits on a cushion in the middle.*
- **N:** "Every loyal town in Brightvale came to a feast by the sea, to see the crown safe at last." `st3_4_20`
- **H:** "Three cheers for [Hero]! Hip hip, hooray!" `h_three_cheers` + title + name + `h_hip_hooray`
- The **Crown Medal** appears on the hero, next to the Border Medal and the Hill Medal, and a **royal banner** joins
  the camp treasures.
- Confetti and the fanfare. Then *hoofbeats*: a rider comes up the cliff road.
  - **N:** "Then a rider came with news. The steward had locked the gates of the capital, and wouldn't let anyone
    in." `st3_4_21`
  - **N:** "'The king and queen will be home soon,' said our hero. 'We must open those gates!'" `st3_4_22`
  - **H:** "To the capital!" `h_to_capital`
- Then camp.

## After arc 3 (until arc 4 is built)
- **N:** "The capital's great gates were shut and barred. The army made camp, and got ready for the siege…"
  `st3_4_23`
- **H:** "The road is blocked! We'll find a way soon." `h_road_blocked`
- Every stop is then a **raid** on any freed village from the whole arc (all the raids of chapters 9–12). Raids keep
  giving camp treasures. The level stays at 12 until arc 4 exists.

| Raid | Narrator | Favoured |
|---|---|---|
| Puffin Point | "Oh no! Grey guards were chasing the puffins at Puffin Point!" `st3_4_r1` | The missing number |
| Tower Town | "Oh no! Grey guards were back in Tower Town, looking for the keys!" `st3_4_r2` | Count the companies |

## New clips in this chapter
- **Herald:**
  - Numbers in tens: `num_30`, `num_40`, `num_50`, `num_60`, `num_70`, `num_80`, `num_90`, `num_100` ("thirty" …
    "one hundred")
  - Count the companies: `h_how_many_in` "How many soldiers in…"
  - The missing number: `what_makes` "what makes…"
  - The fork: `fork_fishing` "the Fishing Village", `fork_cove` "the Smugglers' Cove"
  - `h_crown_tower` "The crown must be in that tower!", `h_give_back` "Let's give everything back!", `h_everyone`
    "That's everyone!", `h_tower_ours` "Hooray! The tower is ours!", `h_to_capital` "To the capital!"
  - `w_puffins`, `w_teddies`, `w_boats` and the which-more clips for them
- **Narrator:** `st3_4_01` … `st3_4_23`, `st3_4_r1`, `st3_4_r2`. That's 25 lines.

## Arc 3 totals
- **Narration:** about 100 lines across the four chapters.
- **Herald:** about 70 new clips: the army words (company, companies), the fork names, the troop check, the tens to
  100, and the short joining words ("or", "make ten!", "…we can see…", "is… what?").
- **Camp treasures from the arc:** the pumpkin, the ship in a bottle, the wooden deer, the sea chest and the royal
  banner, plus one per raid won. Each fork gives the treasure only on its special branch, so a child who always picks
  the recruit stops keeps the treasures for the raids.
