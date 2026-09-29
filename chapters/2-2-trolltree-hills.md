# Chapter 6 · Trolltree Hills

**Arc 2 · The Troll Hills** · Level 6 · numbers 1–20 · 4 tasks per stop · party cap 20 · about 10 sets.

The hills are covered in nut trees (hazelnuts, chestnuts and walnuts), and the trolls are shaking them bare for King
Nutbelly. *Thud, thud,* and down come the nuts, *bonk*, on everyone's heads. That's the chapter's running joke.
Numbers now go up to 20, the **=** sign joins + and −, and two new tasks arrive: **which number is bigger?** and
**look closely**. The troll chief here is **Crackjaw**, who cracks nuts with his teeth. Conventions are as in
[chapter 1](1-1-the-border-road.md) and [chapter 5](2-1-the-stone-bridge.md).

## The road

| # | Stop | Kind | Sets | Earns |
|---|---|---|---|---|
| 0 | Into Trolltree Hills | Opening (first play only) | – | – |
| 1 | Hazelhurst | Village | 1 | Recruits |
| 2 | The Shaking Grove | Skirmish | 1+ | Flag |
| 3 | The Squirrels' Oak | Special | 1 | A **squirrel** comes to live at the camp |
| 4 | Chestnut Green | Village | 1 | Recruits |
| ⛺ | *Camp* | | | |
| 5 | The Big Nut Pile | Skirmish | 1+ | Flag |
| 6 | Walnut End | Village | 1 | Recruits; a warning about the fort |
| 7 | The Nutcracker Fort | Siege | 3+ (ladders, the ram, then the assault) | The fort, and the chapter |
| ⛺ | *Camp: chapter end* | | | |

## Level 6 tasks

| Task | Numbers | On screen | Cards |
|---|---|---|---|
| **Find the number** | 1–20 | Banners | 4 banners |
| **Count them** | 1–20; above 10 in rows of 5 | In the scene | 4 shields, next-door choices |
| **Which is more? / fewer?** | Up to 20, close amounts · size trick | Two sides | Tap a side |
| **Find the sign** | + − **=** | Signposts | 3 signposts |
| **What comes next?** | Up to 20, often across the ten ("9, 10, _", "18, 19, _") | Stones | 3 numeral stones |
| **Count and compare** | Up to 20 | Two groups with their numbers | Tap a side |
| **Which number is bigger?** (new) | Two numbers up to 20: far apart at first (3 vs 15), then close (13 vs 15) | Two trolls holding up shields | Tap a shield |
| **Look closely** (new) | 4 banners at first, up to 6 | Banners that flip face down | Tap a banner |

### The = sign
- **H:** "Find the equals!" `find_the` + `sign_equals`. **Right:** "Equals! Equals means the same." `sign_equals` +
  `equals_means`
- **Tracked as** `sign:=`.

### New: Which number is bigger?
- **H:** "Which number is bigger?" `which_bigger`
- **On screen:** two trolls, each holding up a shield with a number on it. No things to count this time: just the
  numbers.
- **Right:** the bigger shield grows, and the troll holding it looks very proud. **H:** "15 is bigger than 3!"
  `num_15` + `is_bigger_than` + `num_3`
- **Help:** each shield shows its amount as dots in rows of 5, and Buckleberry counts the smaller one together.
- **Tracked as** `big`.

### New: Look closely
- **H:** "Look closely!" `look_closely`. The banners show their numbers for a moment (4 seconds at first, shorter
  later), then flip face down with a flutter. Then: "Find the banner with 7!" `find_banner` + `num_7`
- **Right:** the banner flips up. "7!"
- **Help:** first miss, the tapped banner flips up to show its number, then back down. Second miss: "Look closely!"
  and all of them flip up for another look.
- **Tracked as** `n:7`, with find the number.

---

## 0 · Into Trolltree Hills (opening)
*Rolling hills covered in nut trees. Far off: thud, thud. Nuts come bouncing down the road.*
- **N:** "Beyond the bridge rose Trolltree Hills, covered in nut trees: hazelnuts, chestnuts and walnuts."
  `st2_2_01`
- **N:** "But the trolls were shaking the trees for King Nutbelly. Thud, thud… and down came the nuts. Bonk!"
  `st2_2_02`
- **H:** "Forward, march! Mind your heads!" `h_forward_march` + `h_mind_heads`

## 1 · Hazelhurst (village)
*Cottages under hazel trees; villagers holding empty baskets; nuts scattered in the grass.*
- **N:** "In Hazelhurst, the baskets were empty. The trolls had shaken every nut away!" `st2_2_03`
- ★★ Count: "How many nuts?" `how_many_nuts` (nuts in the grass, in rows of 5 above 10) · ★ Which number is
  bigger? · ★ Find the sign · ★ What comes next?
- **N:** "More brave friends joined the march." `st_joined`

## 2 · The Shaking Grove (skirmish)
*Trolls hugging nut trees and shaking them: thud, thud, thud. Nuts rain down. One troll wears a pot as a helmet.*
- **N:** "In the grove, trolls were shaking the nut trees. Thud, thud, thud! Nuts rained down everywhere."
  `st2_2_04`
- **H:** "Trolls! Let's be clever!" `h_trolls`
- ★★ Which number is bigger? (the trolls hold up the shields) · ★ Count trolls · ★ Count nuts · ★ Look closely
- **Each first-try right answer:** a troll shakes his tree too hard, and a nut bonks him on the head. He sits down,
  dizzy, with little stars. (This is Trolltree Hills' version of dropping a stick.)
- **Won:** **N:** "The trolls stomped off, rubbing their heads." `st2_2_05`
- **Not yet:** the retreat, as in chapter 5.

## 3 · The Squirrels' Oak (special)
*A huge old oak full of holes. Cross squirrels chatter on the branches; all their nuts have been shaken out onto the
grass.*
- **N:** "The trolls had shaken the squirrels' tree, and all their nuts had tumbled out!" `st2_2_06`
- **H:** "Let's put the nuts back!" `h_nuts_back`
- ★★ Count: "How many nuts?" · ★ Look closely (numbers on the tree's holes) · ★ Which number is bigger? · ★ What
  comes next?
- **Each first-try right answer:** a squirrel scurries down, grabs a nut and pops it back into a hole.
- **End:** the rest of the nuts go back. The littlest squirrel hops onto Buckleberry's hat and won't get off.
  - **H:** "A present for our camp!" `h_camp_gift`
  - **N:** "The littlest squirrel liked Buckleberry's hat so much, it came along!" `st2_2_07`

## 4 · Chestnut Green (village)
*A village green with a huge chestnut tree, and children playing with conkers on strings.*
- **N:** "On Chestnut Green, the children played conkers under the big chestnut tree." `st2_2_08`
- ★★ Count villagers · ★ Find the sign (=) · ★ Which number is bigger? · ★ Look closely
- **N:** `st_joined`

## ⛺ Camp
As before. The squirrel nibbles a nut by the fire.

## 5 · The Big Nut Pile (skirmish)
*A mountain of stolen nuts, and trolls with sacks guarding it.*
- **N:** "Trolls were piling up stolen nuts for King Nutbelly. What a big pile!" `st2_2_09`
- ★★ Count and compare: "Which pile has more nuts?" `which_more_nuts` · ★ Count trolls · ★ Which number is bigger?
  · ★ Find
- **Won:** **N:** "The trolls ran off, and the villagers took back their nuts." `st2_2_10`

## 6 · Walnut End (village)
*The last village in the hills: walnut trees and a lookout post. From the hilltop: crack… crunch…*
- **N:** "Walnut End was the last village before Crackjaw's fort." `st2_2_11`
- ★★ Count villagers · ★ Look closely · ★ What comes next? · ★ Find the sign
- **N:** "'Listen,' whispered the villagers. Crack! Crunch! 'That's Crackjaw, cracking nuts with his teeth!'"
  `st2_2_12`

## 7 · The Nutcracker Fort (siege)
*A log fort on the hilltop, with sacks of nuts stacked up like walls. On top sits Crackjaw, cracking a walnut in his
huge square teeth.*
- **N:** "On the hilltop stood the Nutcracker Fort, and on top sat Crackjaw, cracking nuts with his teeth. Crunch!"
  `st2_2_13`
- **H:** "The gate is shut tight! We need ladders and a battering ram!" `h_need_ladders_ram`
- **Build 1: ladders**, as in chapter 5. Minimum **3**.
- **Build 2: the ram**, as in chapter 5. Minimum **the log and the wheels**.
- **Assault:** ★★ Count trolls · ★ Which number is bigger? · ★ Count and compare · ★ Look closely
- **Won:** *BOOM… BOOM… CRASH!*, then the dust cloud. **H:** "Hooray! The fort is ours!" `h_fort_ours`
  - **N:** "Crackjaw was so surprised, he dropped his walnut, bonk, right on his own toe! Then he hopped all the
    way to the Echo Pass." `st2_2_14`
- **Chapter end:** **N:** "Trolltree Hills were quiet again, and the nut trees kept their nuts." `st2_2_15`, then
  the victory screen and camp.

## When the road is blocked
- **N:** "A rockslide had covered the road to the Echo Pass." `st2_2_16`
- **H:** "The road is blocked! We'll find a way soon." `h_road_blocked`

| Raid | Scene | Narrator | Favoured |
|---|---|---|---|
| Hazelhurst | Trolls shaking the hazel trees again; nuts bonking villagers | "Oh no! Trolls were shaking Hazelhurst's trees again!" `st2_2_r1` | Count nuts |
| Chestnut Green | Trolls pinching the children's conkers | "Oh no! Trolls were pinching the conkers on Chestnut Green!" `st2_2_r2` | Which number is bigger? |
| Walnut End | Trolls cracking walnuts on the roofs, CRACK | "Oh no! Trolls were cracking walnuts on Walnut End's roofs!" `st2_2_r3` | Count trolls |

**Cleared (level 7):** **N:** "The villagers and the soldiers cleared the rocks away together!" `st2_2_17` · **H:**
`h_road_clear`

## New clips in this chapter
- **Herald:**
  - `num_13` … `num_20` ("thirteen" … "twenty")
  - `sign_equals` "equals!", `equals_means` "Equals means the same!"
  - `which_bigger` "Which number is bigger?", `is_bigger_than` "is bigger than"
  - `look_closely` "Look closely!"
  - `h_mind_heads` "Mind your heads!", `h_nuts_back` "Let's put the nuts back!"
  - `how_many_nuts`, `which_more_nuts`, `which_fewer_nuts`, `w_nuts`
- **Narrator:** `st2_2_01` … `st2_2_17`, `st2_2_r1` … `st2_2_r3`. That's 20 lines.
