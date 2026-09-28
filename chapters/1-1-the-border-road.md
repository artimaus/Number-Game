# Chapter 1 · The Border Road

**Arc 1 · The Goblin Border** · Level 1 · numbers 1–3 · 3 tasks per stop · party cap 10 · about 10 sets · two
sittings at the default "make camp after 4 stops".

This is the very first chapter a 2-year-old plays. It opens gently with two villages (nothing can fail), meets
goblins at stop 3, and ends with the first siege.

### How to read this script
- **N:** narrator. Optional; plays only if recorded. The line is always shown as a caption, so a grown-up can read
  it aloud.
- **H:** herald. Plays the recording if there is one, the robot voice if not.
- `key`: the clip name, used for recording and for importing files (e.g. `h_onward.m4a`).
- **[Hero]** = the title clip plus the name clip: `title_prince` + `child_leo` → "Prince Leo". Only the herald
  says the hero's name. **The narrator always says "our hero"**, so one narration recording fits every player,
  prince or princess, siblings included.
- Names: the kingdom of **Brightvale**, **Buckleberry** the herald, the goblin chief **Snagglenose**, and the steward,
  **Uncle Grimbald** or **Aunt Grimhilda** (a grown-up setting). Lines that mention the steward are written
  {uncle|aunt}. The caption and recording guide show the version picked; the clip key is the same for both.
- ★★ = a task type this stop favours (picked about twice as often); ★ = can turn up.

---

## The road

| # | Stop | Kind | Sets | Earns |
|---|---|---|---|---|
| 0 | The castle courtyard | Prologue (first play only, tap to skip) | – | – |
| 1 | Millbrook | Village | 1 | Recruits |
| 2 | Duckpond | Village | 1 | Recruits |
| 3 | The Goblin Lookout | Skirmish | 1 (+ retries) | The lookout flies our flag |
| 4 | The Sheep Meadow | Special | 1 | The shepherd joins, and gives a **sheepdog puppy** (the first camp treasure) |
| ⛺ | *Camp: sitting 1 ends* | | | |
| 5 | Berrybush | Village | 1 | Recruits |
| 6 | The Goblin Camp at the Ford | Skirmish | 1 (+ retries) | The ford is free |
| 7 | Bellhill | Village | 1 | Recruits; a warning about the fort |
| 8 | Stumpy Fort | Siege | 2+ (ladders, then the assault) | The fort, and the chapter |
| ⛺ | *Camp: chapter end* | | | |

The party starts at 0 soldiers (just the hero and Buckleberry). It reaches at least 5 (4 villages + the shepherd) and up to
the cap of 10. After the cap, right answers in villages give gear (§5.5 of the design doc).

## Level 1 tasks

| Task | Numbers | On screen | Cards |
|---|---|---|---|
| **Find the number** | 1, 2, 3 | Banners on poles | 3 banners (1, 2, 3), each with its dots underneath |
| **Count them** | 1–3 things, **in a row** (not scattered yet) | In the scene | 3 shields (1, 2, 3) with dots |
| **Which is more?** | Two groups, **at least 3 times as many** (1 vs 3, 1 vs 4, 2 vs 6); things the same size | Two sides of the scene | Tap a side |

- **Targets rotate evenly** (the least-asked number next), as Letter Hunt does with sounds.
- **Help:** first miss, one wrong card fades. Second miss, "Let's count together!" (the things light up as Buckleberry
  counts), then the right card pulses.
- **The very first task ever:** if nothing is tapped for 4 s, the right banner glows softly. This happens once
  only, to show a brand-new player what tapping does.

---

## 0 · Prologue: the castle courtyard
*A castle, a harbour, a ship with striped sails. Taps skip ahead line by line.*

- **N:** "Once upon a time, in the kingdom of Brightvale…" `st1_1_01`
- **N:** "…the king and queen set sail on a voyage of peace." *(the ship sails away; waving)* `st1_1_02`
- **N:** "They left {Uncle Grimbald|Aunt Grimhilda} in charge." *(the steward steps out, smiling a little too
  widely)* `st1_1_03` · *steward line*
- **N:** "'Goblins are bothering the border villages,' said {Uncle Grimbald|Aunt Grimhilda}. 'Go and help
  them, and don't hurry back!'" `st1_1_04` · *steward line*
- **H:** "Ta-ra! I'm Buckleberry, the royal herald! I'll march with you, **[Hero]**!" `h_intro` + title + name
- **H:** "Forward, march!" `h_forward_march`

## 1 · Millbrook (village)
*A windmill, three cottages, villagers peeking from their doorways, chickens pecking about.*

**Arrive**
- **N:** "The first stop was Millbrook, where the big windmill turns." `st1_1_05`
- **H:** *(fanfare)* "Hello, villagers! Who will join us?" `h_hello_village`

**Tasks** (3)
- ★★ Count: "How many villagers?" `how_many_villagers` (villagers in the doorways) or "How many chickens?"
  `how_many_chickens`
- ★ Find: "Find the banner with…" `find_banner` + `num_2` (bunting on the windmill)
- ★ More: "Which side has more chickens?" `which_more_chickens` (two pens)

**Each first-try right answer:** a villager steps out, takes a spear and marches over to the party. **H:** "A new
soldier!" `h_new_soldier`, or "Welcome to the army!" `h_welcome`.
- **Right answer, spoken every time:** Count gets "1, 2, 3. 3 chickens!" `num_…` + `w_chickens`. Find gets "2!".
  More gets "This side has 3!" `this_side_has` + `num_3`.
- **Praise** (about 1 in 3, as Letter Hunt does): "Huzzah!" `praise_huzzah`, "Well done, [Hero]!" `praise_well_done`
  + title + name, "Splendid!" `praise_splendid`, "That's it!" `praise_thats_it`.

**A miss:** "Not quite! That's 1." `not_quite` + `thats` + `num_1`, then help, then the command again.

**End of set**
- If no answer was right first time, one villager joins anyway: "A brave villager joins anyway!" `h_joins_anyway`.
- **H:** "We have 3 soldiers!" `we_have` + `num_3` + `w_soldiers`
- **N:** "The people of Millbrook cheered as the little army marched on." `st1_1_06`
- **H:** "Onward!" `h_onward`

## 2 · Duckpond (village)
*A round pond, a little boathouse with bunting, ducks paddling.*

- **N:** "Next came Duckpond. Quack, quack!" `st1_1_07`
- **H:** *(fanfare)* "Hello, villagers! Who will join us?" `h_hello_village`
- ★★ Count: "How many ducks?" `how_many_ducks` · ★ Find: banners on the boathouse · ★ More: "Which side has more
  ducks?" `which_more_ducks`
- Recruits, end of set and praise as at Millbrook.
- **N:** "Duckpond's bravest friends joined the march." `st1_1_08`

## 3 · The Goblin Lookout (skirmish): first goblins!
*A rickety tree house on stilts. Goblins peek out: green, with big ears, holding pointy sticks. They blow
raspberries (a sound effect).*

**Arrive**
- **N:** "Up in a rickety tree house sat… goblins!" `st1_1_09`
- **H:** "Goblins! Don't worry, [Hero]. Let's show them how clever we are!" `h_goblins_first` + title + name +
  `h_show_clever`. (This
  is the first goblin ever. Later skirmishes use "Goblins! Let's be clever!" `h_goblins`.)

**Tasks** (3)
- ★★ More: "Which side has more goblins?" `which_more_goblins` (goblins at two windows)
- ★ Count: "How many goblins?" `how_many_goblins`
- ★ Find: banners on our soldiers' poles

**Each first-try right answer:** the army takes a step forward; a goblin wobbles and drops its stick (clatter).
Praise as usual.

**Won (2 or 3 of 3 right first time)**
- **H:** "Charge!" `h_charge`
- A cartoon dust cloud with stars, then the goblins scramble down the ladder and run off to the right. Our flag
  goes up on the tree house.
- **H:** "Hooray! They ran away!" `h_ran_away`
- **N:** "The goblins ran off into the bushes, and the lookout flew our flag." `st1_1_10`

**Not yet (0 or 1 of 3)**
- **H:** "Retreat! Retreat!" `h_retreat`. The army scampers back to the left with speed lines, and Buckleberry's trumpet
  goes "wah-wah".
- **N:** "Oops! The goblins were tricky that time." `st_retreat` (used in every chapter)
- **H:** "That's all right. Let's try again!" `h_try_again`
- A fresh set of problems follows. Nothing is lost.

## 4 · The Sheep Meadow (special)
*A meadow, an empty pen, sheep scattered all over, a worried shepherd with a crook. A puppy hides behind her.*

**Arrive**
- **N:** "In the meadow, a shepherd was worried. The goblins had scattered her sheep!" `st1_1_11`
- **H:** "Let's bring the sheep home!" `h_sheep_home`

**Tasks** (3), which can't fail
- ★★ Count: "How many sheep?" `how_many_sheep`
- ★ More: "Which side has more sheep?" `which_more_sheep`
- ★ Find: banners on the pen gate

**Each first-try right answer:** a sheep trots back into the pen. *Baa!*

**End**
- The rest of the sheep trot home.
- The shepherd joins the army (+1 soldier, or gear at the cap).
- The puppy bounds over to Buckleberry: the **first camp treasure**.
- **H:** "A present for our camp!" `h_camp_gift`
- **N:** "To say thank you, the shepherd joined the army and gave them a sheepdog puppy." `st1_1_12`

## ⛺ Camp (sitting 1 ends, at the default setting)
*Dusk. Tents go up, a campfire crackles, and the puppy curls up by the fire.*

1. **N:** "As the sun went down, the army made camp." `st_camp_1` (a generic camp line, with variants `st_camp_2`,
   `st_camp_3`)
2. **H:** "Make camp!" `h_make_camp`
3. The troop shield grows big for a moment. **H:** "We have 5 soldiers!" `we_have` + `num_5` + `w_soldiers`
4. **H:** "Rest now, brave [Hero]. Good night!" `h_rest_now` + title + name + `h_good_night`

**Next sitting opens with:**
- **N:** "Morning came, bright and early." `st_morning`
- **H:** "Wake up! The march goes on!" `h_wake_up`

## 5 · Berrybush (village)
*Bushes heavy with big berries, baskets on a bench.*

- **N:** "Berrybush smelled of sweet berries." `st1_1_13`
- ★★ Count: "How many baskets?" `how_many_baskets` · ★ More: "Which side has more berries?" `which_more_berries`
  (big, round berries) · ★ Find: banners on the bench
- Recruits as usual.
- **N:** "More brave friends joined the march." `st1_1_14`

## 6 · The Goblin Camp at the Ford (skirmish)
*A shallow river crossing, stepping stones, three goblin tents on the near bank.*

- **N:** "At the river crossing, goblins had set up camp." `st1_1_15`
- **H:** "Goblins! Let's be clever!" `h_goblins`
- ★★ More: "Which side has more goblins?" (two tents) · ★ Count: "How many goblins?" · ★ Find
- **Won:** "Charge!", a dust cloud, then the goblins splash across the river and away. Flag up.
- **N:** "Splash! The goblins ran across the river and away." `st1_1_16`
- **Not yet:** as at the lookout.

## 7 · Bellhill (village)
*Cottages on a hillside, a big bell in a little tower.*

- **N:** "Bellhill had a big bell. Ding, dong!" `st1_1_17`
- ★★ Count: "How many villagers?" · ★ Find: banners on the bell tower · ★ More: "Which side has more chickens?"
- Recruits as usual.
- **N:** "'The goblin fort is just over the hill,' the villagers whispered." `st1_1_18`

## 8 · Stumpy Fort (siege)
*A wooden goblin fort built around an enormous tree stump. On top, arms folded, the goblin chief Snagglenose, with a
long pointy nose and a wonky crown. A woodpile sits beside the road.*

**Arrive**
- **N:** "Over the hill stood Stumpy Fort, and on top was the goblin chief, Snagglenose!" `st1_1_19`
- **H:** "A goblin fort! We need ladders!" `h_need_ladders`

**Build round** (3 tasks, can't fail)
- ★★ Find: banners on the woodpile
- ★ Count: "How many logs?" `how_many_logs`
- ★ More: "Which pile has more logs?" `which_more_logs`
- **Each first-try right answer:** soldiers carry a ladder to the wall and lean it there. **H:** "A ladder!"
  `h_a_ladder`
- **End:**
  - Fewer than 2 ladders: **H:** "We need one more ladder!" `h_one_more_ladder`, and another build round follows.
    The ladders already built stay.
  - 2 or more: **H:** "Ready! Up the ladders!" `h_up_the_ladders`

**Assault round** (3 tasks)
- ★★ Count: "How many goblins?" (goblins peeking over the wall)
- ★ More: "Which side has more goblins?" (two watchtowers)
- ★ Find
- **Each first-try right answer:** a soldier climbs a rung higher, and a goblin on the wall drops its stick.
- **Won:**
  - **H:** "Charge!" Soldiers swarm up every ladder, and a dust cloud rolls along the wall. The goblins pour out of
    the back gate. Snagglenose shakes a fist and runs after them.
  - Our flag goes up on the stump.
  - **H:** "Hooray! The fort is ours!" `h_fort_ours`
  - **N:** "Snagglenose ran into the Whispering Woods, shouting, 'You haven't seen the last of me!'" `st1_1_20`
- **Not yet:** retreat, as at the lookout. The ladders stay up, and the next try goes straight to a fresh assault
  round.

**Chapter end**
- **N:** "The Border Road was safe again. But deep in the Whispering Woods, more goblins were waiting…" `st1_1_21`
- A victory screen: trophy, confetti and a fanfare (Letter Hunt's party screen), then camp.

## ⛺ Camp (chapter end)
As before, with the whole army's total.

---

## When the road is blocked (raids)
If the child isn't at level 2 yet when Stumpy Fort falls, the next sitting starts with:
- **N:** "A great tree had fallen across the road into the Whispering Woods." `st1_1_22`
- **H:** "The road is blocked! We'll find a way soon." `h_road_blocked`

Then each stop is a **raid** on a village already freed, picked in turn so the same one doesn't come up twice
running:

| Raid | Scene | Narrator | Favoured tasks |
|---|---|---|---|
| Millbrook | Goblins riding the windmill sails round and round | "Oh no! Goblins were spinning on Millbrook's windmill!" `st1_1_r1` | Count goblins, more |
| Duckpond | Goblins chasing the ducks | "Oh no! Goblins were chasing Duckpond's ducks!" `st1_1_r2` | Count ducks, more |
| Berrybush | Goblins stuffing their cheeks with berries | "Oh no! Goblins were eating all of Berrybush's berries!" `st1_1_r3` | Count baskets, more |
| Bellhill | Goblins ringing the bell, *clang clang clang* | "Oh no! Goblins were ringing Bellhill's bell!" `st1_1_r4` | Count goblins, find |

**Every raid**
- **H:** "Goblins are back! To the village!" `h_raid`
- A skirmish set, as at the lookout.
- **Won:** the villagers cheer and give a **camp treasure**. **H:** "A present for our camp!" `h_camp_gift`
- **Camp treasures, in order:** a flag · a drum · a lantern · bunting · a goat · a bigger tent · a cooking pot · a
  bench · a banner pole · a pony. Later chapters continue the list.
- **Make camp** after the usual number of stops.

**When level 2 arrives** (checked after every set):
- **N:** "The woodcutters cleared the fallen tree!" `st1_1_23`
- **H:** "The road is clear! Onward!" `h_road_clear`
- Chapter 2 (The Whispering Woods) begins.

---

## Clips used in this chapter

### Herald: shared by the whole game (robot voice if not recorded)

The game's grown-up panel (Voices) lists every clip with its key, grouped the same way. If a key here and the panel
ever differ, the panel is right.

| Key | Line |
|---|---|
| `h_intro` | "Ta-ra! I'm Buckleberry, the royal herald! I'll march with you," *(+ Hero)* |
| `h_forward_march` | "Forward, march!" |
| `h_onward` | "Onward!" |
| `h_hello_village` | "Hello, villagers! Who will join us?" |
| `h_new_soldier` / `h_welcome` | "A new soldier!" / "Welcome to the army!" |
| `h_joins_anyway` | "A brave villager joins anyway!" |
| `we_have` | "We have…" |
| `h_goblins_first` / `h_show_clever` / `h_goblins` | "Goblins! Don't worry," *(+ Hero)* / "Let's show them how clever we are!" / "Goblins! Let's be clever!" |
| `h_charge` | "Charge!" |
| `h_ran_away` | "Hooray! They ran away!" |
| `h_retreat` | "Retreat! Retreat!" |
| `h_try_again` | "That's all right. Let's try again!" |
| `h_sheep_home` | "Let's bring the sheep home!" |
| `h_camp_gift` | "A present for our camp!" |
| `h_make_camp` | "Make camp!" |
| `h_rest_now` / `h_good_night` | "Rest now, brave…" / "Good night!" |
| `h_wake_up` | "Wake up! The march goes on!" |
| `h_need_ladders` / `h_a_ladder` / `h_one_more_ladder` / `h_up_the_ladders` | "A goblin fort! We need ladders!" / "A ladder!" / "We need one more ladder!" / "Ready! Up the ladders!" |
| `h_fort_ours` | "Hooray! The fort is ours!" |
| `h_road_blocked` / `h_road_clear` / `h_raid` | "The road is blocked! We'll find a way soon." / "The road is clear! Onward!" / "Goblins are back! To the village!" |
| `find_banner` | "Find the banner with…" |
| `how_many_*` | "How many villagers / chickens / ducks / goblins / sheep / baskets / logs?" (7) |
| `which_more_*` | "Which side has more chickens / ducks / goblins / sheep / berries?" and "Which pile has more logs?" (6) |
| `this_side_has` / `thats` / `not_quite` | "This side has…" / "That's…" / "Not quite!" |
| `lets_count` | "Let's count together!" |
| `w_*` | "soldiers", "villagers", "chickens", "ducks", "goblins", "sheep", "baskets", "logs" (8, for "3 ducks!") |
| `num_1` … `num_10` | "one" … "ten" |
| `praise_*` | "Huzzah!", "Well done,", "Splendid!", "That's it!" (and more later) |
| `title_prince` / `title_princess` | "Prince" / "Princess" |
| `child_<name>` | The player's name |

About 70 herald clips cover this chapter; most are reused for the rest of the game.

### Narrator: chapter 1 (silent if not recorded)
`st1_1_01` … `st1_1_23` (23 story lines), `st1_1_r1` … `st1_1_r4` (4 raid lines), plus the shared `st_retreat`,
`st_camp_1` … `st_camp_3` and `st_morning`. That's **32 lines**, about 5 minutes of recording.
