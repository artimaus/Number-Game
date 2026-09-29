# Chapter 5 · The Stone Bridge

**Arc 2 · The Troll Hills** · Level 5 · numbers 1–12 · 4 tasks per stop · party cap 20 · about 10 sets.

Spring melts the snow on the path, and the army marches into troll country. This chapter brings trolls, numbers past
10, and three new tasks: **find the sign**, **what comes next?** and **count and compare**. It ends with the first
arc 2 siege, which needs 3 ladders and a battering ram.

Conventions (N:, H:, [Hero], ★★/★, clip keys) are as in [chapter 1](1-1-the-border-road.md). New for arc 2:
- **Trolls** are big, round and mossy, with tufty hair, long noses and stompy feet. They're grumbly, not scary, and
  they'd much rather eat nuts than fight. When beaten they stomp off, grumbling.
- **King Nuttletusk**, the Troll King, wants every nut in the hills. His trolls shake the villages' nut trees bare.
  Each chapter has its own troll chief: here it's **Grumbleguts**, the grumpiest bridge troll of all.
- **4 tasks per stop.** A fight is won with 2 or more right on the first try.
- **Discs** (design doc §5.5): the gold disc over our army now counts up to 20, and the red disc shows the trolls.
  A troll camp holds 1–3 trolls (they're big), and a fort holds 3–5 plus its chief.
- A player who starts in arc 2 (a grown-up setting) brings **5 soldiers** from the border.

---

## The road

| # | Stop | Kind | Sets | Earns |
|---|---|---|---|---|
| 0 | Spring in the hills | Opening (first play only) | – | – |
| 1 | Goatsby | Village | 1 | Recruits |
| 2 | The Little Bridge | Skirmish: the first troll! | 1+ | Flag |
| 3 | The Goat Rocks | Special | 1 | The goatherd joins, and gives a **big round cheese** for the camp |
| 4 | Pebbleford | Village | 1 | Recruits |
| ⛺ | *Camp* | | | |
| 5 | The Boulder Road | Skirmish | 1+ | Flag |
| 6 | Crossways | Village | 1 | Recruits; a warning about the bridge |
| 7 | The Great Stone Bridge | Siege | 3+ (ladders, the ram, then the assault) | The bridge, and the chapter |
| ⛺ | *Camp: chapter end* | | | |

## Level 5 tasks

| Task | Numbers | On screen | Cards |
|---|---|---|---|
| **Find the number** | 1–12 | Banners | 4 banners, no dots |
| **Count them** | 1–12, scattered; above 10 they stand in rows of 5, like a ten frame | In the scene | 4 shields |
| **Which is more? / fewer?** | Up to 12, close amounts · size trick | Two sides | Tap a side |
| **Find the sign** (new) | + and − | Signposts | 2 signposts |
| **What comes next?** (new) | Counting on, up to 12 ("4, 5, _") | Numbered stepping stones, planks or rungs | 3 numeral stones |
| **Count and compare** (new) | Two groups, up to 10 each, close together | Two groups, each with its number on a shield | Tap a side |

- **Look-alikes:** 6 and 9 may now share a board. 2/5 and 1/7 may too.
- The first time each new task turns up, the right answer glows softly if nothing is tapped for a few seconds, as
  with the very first task of the game. The signs also get a short introduction (below).

### New: Find the sign
- **H:** "Find the plus!" `find_the` + `sign_plus` · "Find the minus!" `find_the` + `sign_minus`
- **On screen:** signposts, each painted with one sign.
- **Right:** the signpost wobbles proudly. **H:** "Plus! Plus means more are coming." `sign_plus` + `plus_means` ·
  "Minus! Minus means some go away." `sign_minus` + `minus_means`
- **First time:** **H:** "Look! Signs! Every sign means something." `h_first_signs`, then the plus signpost wobbles
  as he says what it means, then the minus.
- **Help:** the wrong signpost fades, and the right one pulses.
- **Tracked as** `sign:+` and `sign:-`.

### New: What comes next?
- **H:** "What comes next?" `whats_next`. The numbered stones light up in turn as he counts them: "4, 5…"
- **On screen:** 2 or 3 numbered stepping stones (planks on a bridge, rungs on a ladder), then a blank one. The
  run starts anywhere from 1 up to 9, so the answer is never more than 12.
- **Cards:** 3 numeral stones: the right one and its next-door neighbours.
- **Right:** the hero hops across, one stone per number, as Buckleberry counts: "4, 5, 6!"
- **Help:** count along from the first stone together, then the right stone pulses.
- **Tracked as** `next:6`.

### New: Count and compare
- **H:** "Let's count both sides!" `lets_count_both`. The things on the left light up as he counts, and a shield with
  their number drops in under them. Then the same on the right: "…4. …6." Then "Which side has more trolls?"
  `which_more_trolls` (sometimes "fewer", as in arc 1).
- **Right:** the side bounces. **H:** "6 is more than 4!" `num_6` + `is_more_than` + `num_4`
- **Why:** it joins an amount to its numeral, one step before comparing bare numbers ("Which number is bigger?", in
  the next chapter).
- **Tracked as** `cmp` and `cmpf`, with "which is more / fewer".

---

## 0 · Spring in the hills (opening)
*Snow sliding off the pine trees, drip, drip; flowers popping up; green hills rolling away, each crowned with a big
shaggy tree.*
- **N:** "Spring came to the border. The snow melted, drip, drop, and the path to the Troll Hills opened at last."
  `st2_1_01`
- **N:** "In the hills lived the trolls: big, grumbly, and very fond of nuts." `st2_1_02`
- **N:** "And Grubbins the Great had run straight to their king, King Nuttletusk, to tell him all about our hero."
  `st2_1_03`
- **H:** "Forward, march!" `h_forward_march`

## 1 · Goatsby (village)
*Stone cottages up a steep hillside, goats standing on the roofs, a goatherd's hut at the top.*
- **N:** "Goatsby was a village so steep that the goats lived on the roofs!" `st2_1_04`
- **H:** *(fanfare)* "Hello, villagers! Who will join us?" `h_hello_village`
- ★★ Count: "How many goats?" `how_many_goats` · ★ Find the sign (signposts at the village gate) · ★ What comes
  next? (numbered steps up the hill) · ★ Find
- **Each first-try right answer:** a villager joins, and the gold disc pops up by one.
- **N:** "The mountain folk of Goatsby joined the march." `st2_1_05`

## 2 · The Little Bridge (skirmish): the first troll!
*A small humpbacked stone bridge over a stream. Two enormous feet stick out from underneath, and a grumpy, mossy face
peers over the side.*

**Arrive**
- **N:** "At a little stone bridge, a big voice rumbled: 'Nobody crosses MY bridge!'" `st2_1_06`
- **H:** "A troll! Don't worry, [Hero]. Let's show him how clever we are!" `h_troll_first` + title + name +
  `h_show_clever`. (Later skirmishes use "Trolls! Let's be clever!" `h_trolls`.)

**Tasks** (4)
- ★★ What comes next? (numbered planks on the bridge)
- ★ Count: "How many trolls?" `how_many_trolls` · ★ Count and compare · ★ Find

**Each first-try right answer:** a troll scratches his head, puzzled. (Goblins dropped their sticks; trolls just get
muddled.)

**Won (2 or more of 4)**
- **H:** "Charge!" `h_charge`. The dust cloud, the discs clink, and the trolls stomp off the right-hand edge,
  grumbling.
- **H:** "Hooray! They stomped away!" `h_stomped_away`
- **N:** "The troll stomped off into the hills, grumbling about clever children." `st2_1_07`

**Not yet (0 or 1 of 4)**
- The retreat, as in arc 1. **N:** "Oops! The trolls were tricky that time." `st_retreat_trolls` (shared by all of
  arc 2). **H:** "That's all right. Let's try again!" `h_try_again`

## 3 · The Goat Rocks (special)
*Tall rocks with little goats stuck on top, bleating. A worried goatherd holds a big round cheese.*
- **N:** "The trolls had chased the goats up the tall rocks, and now they couldn't get down!" `st2_1_08`
- **H:** "Let's help the goats down!" `h_goats_down`
- ★★ Count: "How many goats?" · ★ What comes next? (steps cut into the rock) · ★ Count and compare: "Which rock has
  more goats?" · ★ Find
- **Each first-try right answer:** a goat hops down, rock to rock, to the goatherd. *Maa!*
- **End:** the rest of the goats hop down. The goatherd joins the army (+1, or gear at the cap) and gives them the
  cheese.
  - **H:** "A present for our camp!" `h_camp_gift`
  - **N:** "The goatherd joined the army, and gave them a big round cheese." `st2_1_09`

## 4 · Pebbleford (village)
*A shallow stream full of smooth pebbles, a mill wheel turning, children skipping stones.*
- **N:** "In Pebbleford, the children were skipping stones. Plip, plop!" `st2_1_10`
- ★★ Count: "How many stones?" `how_many_stones` · ★ What comes next? (stepping stones) · ★ Find the sign · ★ More
  or fewer: "Which side has more stones?" `which_more_stones`
- **N:** "More brave friends joined the march." `st_joined`

## ⛺ Camp
As in arc 1: the gold disc grows big for a moment, "We have 12 soldiers!", and the cheese sits by the fire.

## 5 · The Boulder Road (skirmish)
*Trolls on a slope, rolling big round boulders down onto the road and laughing.*
- **N:** "Trolls were rolling boulders onto the road. Rumble, rumble, BUMP!" `st2_1_11`
- **H:** "Trolls! Let's be clever!" `h_trolls`
- ★★ Count and compare: "Which side has more trolls?" · ★ Count trolls · ★ What comes next? · ★ Find the sign
- **Won:** **N:** "The trolls stomped away, and the soldiers rolled the boulders off the road." `st2_1_12`
- **Not yet:** as at the Little Bridge.

## 6 · Crossways (village)
*A crossroads with a well and a little inn. Every signpost has been turned the wrong way round.*
- **N:** "At Crossways, the trolls had turned every signpost the wrong way round!" `st2_1_13`
- ★★ Find the sign (each right answer turns a signpost back) · ★ Count villagers · ★ What comes next? · ★ Find
- **N:** "'The Great Stone Bridge is just ahead,' said the innkeeper. 'And Grumbleguts guards it!'" `st2_1_14`

## 7 · The Great Stone Bridge (siege)
*A huge stone bridge over a deep gorge, with a squat troll tower and a great wooden gate at our end. On the tower:
Grumbleguts, the biggest, grumpiest bridge troll, with a mossy beard down to his knees.*

**Arrive**
- **N:** "There stood the Great Stone Bridge, with a troll tower and a great wooden gate. On top stood Grumbleguts!"
  `st2_1_15`
- **H:** "The gate is shut tight! We need ladders and a battering ram!" `h_need_ladders_ram` (as at arc 1's Great
  Stockade)

**Build 1: ladders** (4 tasks, can't fail)
- ★★ Find · ★ Count: "How many logs?" · ★ What comes next? (numbered rungs on a ladder) · ★ Find the sign
- **Each first-try right answer:** soldiers lean a ladder against the tower. **H:** "A ladder!" `h_a_ladder`
- **Minimum: 3 ladders.** Short of that: "We need one more ladder!" `h_one_more_ladder`, then another round. The
  ladders already up stay.

**Build 2: the battering ram** (4 tasks, can't fail)
- **H:** "Now let's build a battering ram!" `h_need_ram`
- **Each first-try right answer** adds the next part: the log, the wheels, a roof, an iron head. **H:** "A piece of
  the ram!" `h_ram_part`
- **Minimum: the log and the wheels.** Short of that: "The ram needs one more piece!" `h_ram_more`
- **Ready:** "Ready! Bang the gate!" `h_ram_ready`

**Assault** (4 tasks)
- ★★ Count: "How many trolls?" (on the tower) · ★ Count and compare (two towers) · ★ What comes next? · ★ Find
- **Won:**
  - The ram swings: *BOOM… BOOM… CRASH!* The gate falls flat. The army and the trolls run into the dust cloud, the
    discs clink, and the trolls stomp off across the bridge, with Grumbleguts last of all.
  - Our flag goes up on the tower. **H:** "Hooray! The fort is ours!" `h_fort_ours`
  - **N:** "Grumbleguts stomped across the bridge and off into Trolltree Hills, where the nut trees grow."
    `st2_1_16`
- **Not yet:** retreat. The ladders and the ram stay; the next try is a fresh assault round.

**Chapter end**
- **N:** "The Great Stone Bridge was open. And beyond it, in the hills, something went thud… thud… thud…"
  `st2_1_17`
- The victory screen, then camp.

---

## When the road is blocked
If the child isn't at level 6 yet when the bridge falls:
- **N:** "A great flock of sheep sat down in the middle of the bridge, and wouldn't budge!" `st2_1_18`
- **H:** "The road is blocked! We'll find a way soon." `h_road_blocked`

| Raid | Scene | Narrator | Favoured |
|---|---|---|---|
| Goatsby | Trolls sitting on the goats' roofs, which sag | "Oh no! Trolls were sitting on Goatsby's roofs!" `st2_1_r1` | Count trolls |
| Pebbleford | Trolls throwing big stones into the stream, SPLASH | "Oh no! Trolls were splashing everyone in Pebbleford!" `st2_1_r2` | Count and compare |
| Crossways | Trolls turning the signposts round again | "Oh no! Trolls were muddling the signs at Crossways!" `st2_1_r3` | Find the sign |

- **H:** "Trolls are back! To the village!" `h_raid_trolls`
- **Cleared (level 6):** **N:** "The shepherd whistled, and the sheep trotted off the bridge!" `st2_1_19` · **H:**
  "The road is clear! Onward!" `h_road_clear`

---

## New clips in this chapter
- **Herald:**
  - `num_11`, `num_12` ("eleven", "twelve"); the rest up to 20 come in chapter 6
  - Signs: `find_the` "Find the…", `sign_plus` "plus!", `sign_minus` "minus!", `plus_means` "Plus means more are
    coming!", `minus_means` "Minus means some go away!", `h_first_signs` "Look! Signs! Every sign means something."
  - `whats_next` "What comes next?"
  - `lets_count_both` "Let's count both sides!", `is_more_than` "is more than"
  - Trolls: `h_troll_first` "A troll! Don't worry,", `h_trolls` "Trolls! Let's be clever!", `h_stomped_away`
    "Hooray! They stomped away!", `h_raid_trolls` "Trolls are back! To the village!"
  - `h_goats_down` "Let's help the goats down!"
  - `how_many_trolls`, `how_many_goats`, `how_many_stones`; `which_more_…` and `which_fewer_…` for trolls, goats and
    stones; `w_trolls`, `w_goats`, `w_stones`
- **Narrator:** `st2_1_01` … `st2_1_19`, `st2_1_r1` … `st2_1_r3`, and the shared `st_retreat_trolls`. That's 23
  lines.
