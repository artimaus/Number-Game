# Number Knights: design

Maths for toddlers through 3rd grade, played as a young prince or princess leading an army in a righteous cause.
Built on Letter Hunt's tablet framework.

**Status:** **arc 1 (the Goblin Border) is built and playable**: [`Number-Game.html`](Number-Game.html). It has all four
chapters, raids, camp, the grown-up panel, and herald and narrator recording. The brainstorm decisions are recorded in
§2, arc 1 is scripted in [`chapters/`](chapters), arc 2 (§5) is designed but not built, and later arcs (§11) are a
rough framework. Items marked *(proposal)* haven't been agreed yet.

**Testing hooks:** open the game with `#test` in the address to expose its state as `window.NK`, and `#fast` to run
every pause 20× faster. A bot can then play the whole arc in about two minutes.

---

## 1. The game in a paragraph

The child is Prince or Princess *(name)*, sent to protect the kingdom's border. With a trumpet-blowing herald at
their side, they march from village to village. At each stop the herald shouts maths commands: "Find the banner with
4!", "How many goblins?", "Find the plus!". Every right answer brings a reward: a villager joins the army, a
ladder is built, a goblin camp is scattered. Foes are never hurt. They drop their spears and run. Soldiers are never
lost; if a battle goes badly, the army scampers back to camp and tries again. The story runs through five arcs, and
the play space opens up from a single road, to forks, to a full campaign map.

## 2. Decisions so far

| Topic | Decision |
|---|---|
| Name | **Number Knights** |
| Hero | Prince or princess, picked when the player is set up; carries the player's name |
| Tone | Foes flee; storybook dust-cloud clashes; freed towns cheer. No harm shown |
| Enemies | Different per story beat: goblins and trolls on the border → the usurping uncle or aunt → an invading foreign kingdom |
| Maths range | From counting to 5 (about age 2) through 3rd grade (times tables, light division) |
| Arcs | 5 arcs: 2 linear, 2 with forks, 1 full map (§3) |
| Maths ↔ action | **Themed card tasks:** Letter-Hunt-style tasks dressed in the theme. The stop decides the reward |
| Stop ↔ task | **Loose match:** each stop favours tasks that fit its story; any task can appear |
| Reward | **Each first-try right answer adds one** (a recruit, a ladder…). A set with misses still gives a smaller reward, never nothing |
| Army display | Border arcs: a party of up to 20. Usurper arcs: companies of ten. Invasion: companies plus unit types |
| Troops lost | **Never.** A failed attack plays a comic retreat, then a retry with fresh problems (map arc: back to the map) |
| Battle fail | Fewer than half the set right on the first try |
| Set size | Grows by arc: 3 tasks per stop in arc 1, up to 6–8 in arc 5 |
| Chapter length | About 8–10 stops; **each chapter has its own hand-made shape** |
| Progress | Adaptive difficulty inside each stop; the story moves on only on success |
| Pacing | When the maths isn't ready for the next chapter, the road ahead is blocked and **goblins raid freed villages behind you** |
| Raid gifts | **Camp treasures**: each gift decorates the camp (a flag, a drum, a pet goat…) |
| Story frame | The king and queen are away on a peace voyage; the uncle (or aunt) left as steward sends the hero to the border |
| Sittings | **Make camp** after a set number of stops (a grown-up setting) |
| Linear view | **Marching scene** (side view), no map until the fork arcs |
| Siege equipment | Built **only when sieging a fort or castle**. Each build round makes one piece, or one group such as ladders. Nothing travels with the party. **The assault needs a minimum of gear**; build rounds repeat until it's met |
| Party cap | 10 in arc 1, 20 in arc 2 (the party stays countable). At the cap, right answers give gear |
| Blocked road | **After** the chapter's fort: every chapter ends in a victory, then raids until the maths is ready |
| Voices | A **herald** (commands, praise, gentle "not quite"s; robot voice if not recorded) and an optional **narrator** (story; silent if not recorded, text always shown). Each can be recorded by a different person |
| Art | Simple custom SVG |
| Herald | **Buckleberry**, a round, cheerful trumpet herald: fanfare before each command, a sad little "wah-wah" toot for a miss |
| Names | The kingdom of Brightvale · Buckleberry the herald · the steward Uncle Grimbald **or** Aunt Grimhilda (a grown-up setting) · the goblin chief Snagglenose · the Goblin King Grubbins the Great |
| Narration | The narrator says **"our hero"**, never the name, so one recording fits every player. Only the herald says the hero's name |
| First tap | A brand-new player's very first task: if nothing is tapped for 4 s, the right card glows softly. Once only |
| Build order | Linear → forks → full map. Get the linear game really dialled in first |

## 3. The five arcs

| # | Arc | Story | Play space | Maths | Army | Tasks per stop |
|---|---|---|---|---|---|---|
| 1 | **The Goblin Border** | Sent to guard the border villages from goblin raiders | Linear march | Counting and numerals to 10; more or less | Party, up to 10 | 3 |
| 2 | **The Troll Hills** | Trolls block the hill passes; a troll king in his keep | Linear march | Numbers to 20; order; the signs + − =; which is bigger; first adding within 5; a first taste of taking away | Party, up to 20 | 4 |
| 3 | **The Stolen Crown** | Coming home to find the uncle/aunt has seized the throne; rallying loyal towns | Forks (pick one of two) | Adding and taking away within 10 | Companies of ten | 5 |
| 4 | **Siege of the Capital** | Retaking the kingdom, castle by castle, ending at the capital | Forks | Within 20; tens and ones; 2-digit numbers | Companies of ten | 6 |
| 5 | **The Invasion** | A foreign kingdom invades; drive them back | Full map | Within 100 → equal groups → times tables → light division | Companies + unit types | 6–8 |

**Story frame:** the king and queen sail off on a peace voyage and leave the hero's Uncle Grimbald (or Aunt Grimhilda) as
steward. The steward sends the young hero to the goblin border, "for experience", really to get them out of the
way. Arc 2 ends with a messenger: "Come home! The crown has been stolen!" Arc 4 ends with the capital retaken and the
king and queen home. In arc 5 the family stands together against the invaders.

## 4. How play works

### The loop
A **chapter** is a road of about 8–10 **stops**. At each stop the herald gives a **set** of card tasks (3 in arc 1).
The stop decides what the answers earn:

| Stop | Each first-try right answer… | Can it fail? |
|---|---|---|
| Village | …brings a recruit (at the party cap: gives a soldier a new piece of gear, §5.5) | No: at least one recruit per visit |
| Goblin camp / troll bridge (a skirmish) | …pushes the foes back; half or more right and they flee | Yes: comic retreat, then a retry with fresh problems |
| Fort or castle, **build** rounds | …adds a piece: a ladder, a ram part… | No: at least one piece per round. A round repeats (fresh problems) until the fort's minimum gear is built |
| Fort or castle, **assault** round | …as a skirmish; starts only once the minimum gear is built | Yes: retreat and retry; what was built stays built |
| Raid (a freed village attacked again) | …as a skirmish; the villagers cheer and send a gift | Yes |

"Right" means right **on the first try**. Every task still ends with the right answer found (with help, as in Letter
Hunt), so nothing is left unresolved. First tries only decide the size of the reward and whether a battle is won.

### Failure is funny, never costly
Every battle ends the same way: "Charge!", and both sides, the whole army and every goblin, run into one big
cartoon dust cloud. Stars fly and it bonks and bumps for a moment. Then the losers come out running, all together,
the way the army marches:
- **Won** (half or more right first time): the goblins burst out of the cloud and run off the right-hand edge of the
  screen, and they're gone. The army stands where the fight was and cheers (everyone hops), and our flag goes up.
  On the next march the soldiers fall back into line as they walk.
- **Not yet** (fewer than half): the army bursts out and runs off the left-hand edge, while Buckleberry toots
  "wah-wah" and the goblins hop and cheer at their posts, sticks back up. The army marches back in: "Let's try
  again!" A fresh set of problems follows at the same stop. No soldier, ladder or freed village is ever lost.
  This applies in every arc, including the first.

### Pacing: the road waits for the maths
Difficulty follows Letter Hunt's adaptive levels: up at 85% of first tries over 10 sets, down quietly below 50%
over 6. **Each chapter needs a level** (§5.4). A chapter is about 10 sets, the same as the level-up window, so a
child who is ready moves through story and maths together.

If the chapter's fort falls but the child isn't at the next chapter's level yet:
- The road ahead is **blocked** (a fallen tree, thick fog, a broken bridge). The herald says "We'll find a way
  soon!"
- Each sitting then offers **raids**: goblins are back at a village you already freed. March back, drive them off,
  and the villagers cheer and send a gift.
- When the level arrives: "The woodcutters cleared the road!" and the march goes on.

A toddler can spend months on one maths stage, so **most toddler play time will be raids**. Raids need variety
(§5.2).

### Sittings: make camp
After a set number of stops (a grown-up setting, default 4 *(proposal)*), the army **makes camp**. There's a
campfire, the army's total ("We have 7 soldiers!") on its shield, and "Rest now, brave Prince Leo!".
With Letter Hunt's "Take a break" on, the game then waits for a grown-up. Otherwise a "Keep marching" button
appears. The next sitting opens with "Wake up! The march goes on!".

## 5. The linear arcs in detail

### 5.1 The marching scene
- **Layout (landscape):** a side-view landscape fills the screen from edge to edge. The scene is laid out on a
  1180 × 820 stage, scaled to fit; on a wider or taller screen the land, sky and road simply carry on past it, so
  there are no empty bars. The home button and the pips sit at the real screen corners. The top bar has the home button, the herald's
  "hear it again" button and pips for the set. The party stands on the road on the left; the stop fills the right.
  During a task, the answer cards rise into a band along the bottom. In portrait, the scene is the top ~45% and the
  cards sit below it.
- **The march:** parallax layers (sky, far hills, trees, road) scroll left for about 3–4 s while the party walks
  with a bobbing step. The hero leads with the player's banner colour; the herald waddles beside them; soldiers
  follow in one or two rows. Tapping hurries the march. The next stop slides in from the right.
- **Arriving:** the party halts. A storybook caption appears at the top ("The village of Millbrook! The villagers
  wave hello.") and the narrator clip plays if one is recorded. Then comes the herald's fanfare and the first
  command.
- **During tasks:** things to count appear *in the scene* (goblins peeking over a fence, sheep in a field,
  villagers waving). Answer cards are themed props: **shields** (numerals), **banners** (numerals), **signposts**
  (signs), **camps** (two groups to compare).
- **Leaving:** the stop's result plays (recruits march over and join, goblins flee, a flag goes up), then the march
  resumes.
- **Chapter road:** a thin strip under the top bar shows the chapter's stops as little icons (village, tents, fort),
  with the party's banner moving along it, like a board-game path in miniature. It shows progress without being a
  map.

### 5.2 Stops (arcs 1–2)
- **Village (recruit).** Villagers wave from their doorways. Favoured tasks: count them (villagers, sheep, apples on
  a cart), find the number (house numbers), which is more (two carts). Each first-try right answer: a villager
  marches over, gets a spear and joins, and the troop shield goes up by one ("We have 7 soldiers!").
- **Goblin camp (skirmish).** Tents and a little palisade, goblins with big ears and pointy spears. Favoured tasks:
  which camp has more goblins, how many goblins. Win: both sides charge into a dust cloud with stars flying, then
  the goblins scamper off the right-hand edge together and the army cheers (§4). Your flag goes up.
- **Troll bridge (arc 2 skirmish).** A troll under a stone bridge: "Nobody crosses MY bridge!" The herald answers
  with maths. Win: the troll grumbles and stomps away into the hills.
- **Fort siege (chapter end).** Two or more sets at one stop:
  - *Arc 1 (goblin stockade):* build **ladders** (each right answer leans another ladder against the wall), then
    **assault**. Minimum: 2 ladders *(proposal)*.
  - *Arc 1 finale (the Great Stockade) and arc 2 (troll keep):* build **ladders** (minimum 2), then a **battering ram** (each right answer adds a part:
    log, wheels, roof, iron head; minimum log + wheels), then **assault**.
  - If a build round ends short of the minimum, the herald calls "We need one more ladder!" and a fresh build round
    follows. With at least one piece per round, that's rarely more than one extra round.
  - Gear beyond the minimum doesn't change the assault's outcome, but it makes it grander: more ladders going up, a
    roofed ram with an iron head.
  - The assault shows the built gear in action: ladders go up, the ram bangs the gate, the goblins flee out the back
    gate.
  - The gear stays at the fort afterwards; nothing travels on.
- **Raid (pacing).** A freed village behind you, with goblins back. Variety for the long toddler stretches: goblins
  stealing sheep (count them home), goblins in the orchard (apples), goblins on the mill roof, goblins hiding in the
  haystacks. Win: villagers cheer and send a **camp treasure**: a flag, a drum, a lantern, a pet goat, bunting, a
  bigger tent. The treasures show at every camp, so long raid stretches still build something. The raid's location
  is picked from the villages already freed.
- **Camp.** See §4.

**Chapter shapes** vary: each chapter is hand-made, with its own mix of villages, skirmishes, a special stop and a
closing siege, and about 10 sets in all. Arc 1 is written out in full:
[1 The Border Road](chapters/1-1-the-border-road.md) ·
[2 The Whispering Woods](chapters/1-2-the-whispering-woods.md) ·
[3 The Marsh Villages](chapters/1-3-the-marsh-villages.md) ·
[4 The Goblin King's Stockade](chapters/1-4-the-goblin-kings-stockade.md).

**Camp treasures.** Each special stop gives a fixed treasure: the sheepdog puppy (ch. 1), a lantern (ch. 2), a
little boat (ch. 3) and an apple cart (ch. 4). The arc's victory feast adds a feast table and the Border Medal. Raids
give the next treasure from this list, in order: a flag · a drum · bunting · a goat · a bigger tent · a cooking
pot · a bench · a banner pole · a pony · hay bales · a scarecrow · a chicken · a cat · a bell · a weathervane ·
flower pots · a birdhouse · a kite. After the last one, the list starts again, as extra flags and bunting.

**After arc 1** (until arc 2 exists): snow blocks the path to the Troll Hills. Every stop is then a raid on any
village freed in arc 1, and the level stays capped at 4.

### 5.3 Task types (arcs 1–2)

| Task | Herald says | On screen | Cards | Right answer | Help |
|---|---|---|---|---|---|
| **Find the number** | "Find the banner with 4!" | Banners on poles | 3–9 numeral banners | "4!" (arc 1: the 4 banner shows 4 dots) | Fade wrong ones → pulse the right one |
| **Count them** | "How many goblins?" | 1–10 things in the scene | 3–4 numeral shields | Things light up one by one as the herald counts: "1, 2, 3. 3 goblins!" | Fade → "Let's count together", then pulse |
| **Which is more?** | "Which camp has more goblins?" | Two groups in the scene | The two groups themselves | The bigger camp bounces: "This camp has 5!" | Fade the smaller group → count both together |
| **Which has fewer?** (from level 3) | "Which side has fewer goblins?" | As Which is more; about a third of the comparisons | The two groups | The smaller group bounces: "This side has 2!" | Count both together |
| **Find the sign** (arc 2) | "Find the plus!" | Signposts at a crossroads | 2–4 signs: + − = | "Plus! Plus means more are coming." | Fade → pulse |
| **Count and compare** (arc 2) | "Count the goblins in each camp. Which camp has more?" | Two groups | A numeral shield under each group, then the groups | "This camp has 4, that camp has 6. 6 is more!" | Count together |
| **Which number is bigger?** (arc 2) | "Which number is bigger?" | Two trolls holding shields | The two numeral shields | "7 is bigger than 4!" (the bigger shield grows) | Show each number's dots |
| **What comes next?** (arc 2) | "What comes next?" | Stepping stones across a stream: 4, 5, _ | 3–4 numeral stones | The hero hops across while the herald counts the stones | Count along from the first stone |
| **Look closely** (arc 2) | "Look closely! …Find the 7!" | Banners flip face down after a look | 4–9 banners | As Find the number | As Letter Hunt's memory game |
| **First adding** (arc 2) | "3 soldiers… and 1 more! How many now?" | Soldiers walk in | Numeral shields | Everyone counted: "4 soldiers!" (later with the sentence 3 + 1 = 4 under the scene) | Count together |
| **Taking away, a first taste** (arc 2) | "3 trolls… 1 stomps off! How many are left?" | A troll stomps away | Numeral shields | "2 trolls left!" | Count what's left together |

- **Early scaffold:** in levels 1–2, numeral shields also show the matching dots under the numeral, so a child who
  doesn't know numerals yet can still match amounts. From level 3 the dots appear only as help after a miss.
- **Counting back:** at level 7, "What comes next?" also runs backwards as a countdown before a charge ("5, 4,
  3… _"). Then "Charge!"

### 5.4 Levels and chapters *(proposal)*

| Lv | Arc · Chapter | Numbers | Tasks | Cards |
|---|---|---|---|---|
| 1 | 1 · The Border Road | 1–3 | Find · Count · More (big gaps) | 3, with dots |
| 2 | 1 · The Whispering Woods | 1–5 | Find · Count (dice patterns) · More | 3, with dots |
| 3 | 1 · The Marsh Villages | 1–7 | Find · Count (scattered) · More (closer) · Fewer | 4 |
| 4 | 1 · The Goblin King's Stockade | 1–10 | Find · Count · More or fewer (closer) | 4 |
| 5 | 2 · The Stone Bridge | 1–12 | Find the sign (+ −) · What comes next? · Count and compare | 4 |
| 6 | 2 · Trollberry Hills | 1–20 | Signs + − = · Which number is bigger? · Look closely | 4–6 |
| 7 | 2 · The Echo Pass | 1–20 | First adding within 5 (pictures) · Countdown (counting back) | 4 |
| 8 | 2 · The Troll King's Keep | 1–20 | First adding with the number sentence · Taking away, a first taste | 4 |

Each level keeps the earlier task types in the mix, with harder numbers, so nothing learned drops out.

- Within a level, the numbers asked come from what the child knows plus the next two, as with Letter Hunt's known
  sounds. The level sets the ceiling.
- **Start point:** when adding a player, the grown-up picks a starting chapter by age (2 → ch. 1, 3 → ch. 2, 4 → ch.
  4, 5 → ch. 6). This can be changed later.

### 5.5 The party
- The party starts as just the hero and the herald: "Let's find brave friends to join us!" The first villages bring
  the first recruits.
- **Cap:** 10 in arc 1, 20 in arc 2. The party then stays inside the numbers the child is learning.
- **At the cap,** right answers in villages give **gear** instead: a helmet, a shield, a spear, boots, a cape in the
  hero's colour. A soldier gets one piece each time ("Tom gets a helmet!"). This keeps "more right = more reward"
  going through the long stretches.
- **The troop total:** in the linear arcs the army shows **one total**, a shield beside the soldiers with the number
  on it. Soldiers don't get numbers of their own. The shield pops whenever a recruit joins; the herald says it after
  each village ("We have 7 soldiers!") and at camp, where the shield grows big for a moment.

## 6. Voices

The same modular clip system as Letter Hunt: named clips joined at play time (`say(["find_banner", "n_4"])`), each
recordable, importable by file name, and backed up. **Two roles:**

| Role | Says | If not recorded | Examples |
|---|---|---|---|
| **Herald** | Commands, praise, "not quite"s, battle calls, counting | Robot voice (a child can't read commands) | "Find the banner with…", "How many goblins?", "Huzzah!", "Not quite!", "Charge!", "Retreat!", "Let's try again!", "Rest now, brave…" |
| **Narrator** | The story: chapter openings, stop arrivals, victories, camp | **Silent**; the caption is always shown so a grown-up can read it aloud | "The village of Millbrook! The villagers wave hello." |

- **Herald clip groups:** numbers `n_0`…`n_20`; signs `sign_plus`, `sign_minus`, `sign_equals`; whole command
  phrases per noun ("How many goblins?", "How many sheep?", which sounds more natural than joining "how many" +
  "goblins"); praise and "not quite"s; battle, build and camp calls; titles `title_prince`, `title_princess`; the
  child's name `child_<name>`. So praise can be ["well_done", "title_princess", "child_mia"]: "Well done, Princess
  Mia!"
- **Narrator clips:** one per story line, grouped by chapter. The step-by-step guide works per chapter ("Record
  chapter 1's story").
- **Uncle or aunt:** the steward is a grown-up setting. Story lines that mention them have two texts
  ({uncle|aunt}) but one clip key; the caption and recording guide show the version picked. Switching the setting
  shows a warning: "*N* story lines mention the steward and were recorded for Uncle Grimbald. Re-record them for
  Aunt Grimhilda?" Each recording remembers which version it was made for. Mismatched ones are kept but not played
  (the caption still shows) until re-recorded, or until the setting is switched back *(proposal)*.
- **Two people, two devices:** the grown-up panel has separate Herald and Narrator sections, each with its own
  step-by-step guide and its **own voice backup file**. Importing a voice file adds or replaces only that role's
  clips. So Dad can record the herald on the tablet and Mum the narrator on her phone, then combine them.
- **Robot herald:** the speech-synthesis voice at a slightly lower pitch, a bit slower, with a fanfare before it.

## 7. Look and sound

- **Style sheet (draft for approval):** https://claude.ai/artifact/Q7wWZQ5H31hpSnMkZWWkpD. It has the march screen at
  Millbrook with a count task, the characters, places, cards and states, and colours and type. The hero has tweaks
  for prince or princess, banner colour, skin and hair.
- **Art:** flat, chunky SVG drawn in code, recoloured with CSS variables.
  - Characters: hero (prince or princess), herald, villager/soldier with gear layers, goblin, goblin king, troll,
    troll king.
  - Places: village, goblin camp, stockade, stone bridge, troll keep, fallen tree, campfire.
  - Props: banners, shields, signposts, ladders, ram.
  - Landscape layers, one palette per chapter (meadow, woods, marsh, hills, pass).
- **Walk cycle:** a body bob plus swinging legs in CSS. Goblins scamper, trolls stomp.
- **Cards:** the Letter Hunt card look (white face, soft shadow, pop on press), shaped as shields and banners.
- **Numerals:** Andika (already embedded in Letter Hunt). Its subset keeps alternate digit shapes: `cv01` (plain
  stick 1), `cv04` (open 4), `cv06`/`cv09` (straight-stem 6 and 9) and `cv07` (7 with a bar). A grown-up setting can
  pick "school-style" or "book-style" digits for one line of CSS.
  Letter Hunt's embedded subset has + and = but not the true minus sign (U+2212), so it needs adding when the font is
  re-subset.
- **Sound:** synthesised, as in Letter Hunt.
  - A trumpet fanfare before commands, and a "wah-wah" toot for a miss.
  - Marching drums (optional music).
  - A rising note per count as things light up.
  - A dust-cloud "bonk", a triumphant flag-raise, and campfire crackle.

## 8. Carried over from Letter Hunt

One self-contained offline HTML file, `Number-Game.html`, with fonts embedded.
It keeps:
- The start screen that unlocks audio and full screen.
- Player cards on the home screen (a hero portrait and chapter progress).
- Long press counts as a tap; ghost taps are swallowed.
- Hold the gear for grown-up settings.
- Profiles; adaptive levels with guess detection; review boxes.
- Help after a miss; the question repeats after 12 s; cards locked while the herald speaks.
- Parties; take a break (now make camp); full screen; dark mode; music.
- Recording with trim, normalise, the step-by-step guide and waveform, import by file name, backup and restore.

The framework is **forked, not shared**: function names stay parallel (`say`, `ask`, `logStep`, `checkLevel`…) so
fixes port both ways.

## 9. Tracking and fairness

- **Review boxes** for each skill:
  - `n:4` recognising the numeral
  - `q:4` the amount (count them)
  - `cmp` and `cmpf` comparing (which is more, which has fewer), shown as first-try rates in the panel
  - `sign:+` the signs
  - later, facts (`+:3+1`).
- **Look-alikes:** numerals 6/9, 2/5 and 1/7 stay off the same board until arc 2.
- **Sound-alikes:** 13/30 … 19/90 stay apart until arc 4.
- **Reversals:** 12/21 are mixed only on purpose, in arc 4.
- **Amounts:** early answer choices are at least 2 apart and in a clear ratio. Later ones are next door (4 vs 5).
  From level 3, the group with *more* is sometimes drawn smaller or tighter, so size isn't a shortcut. The same
  trick applies to "which has fewer", where the smaller group then looks bigger.
- **Help after a miss:** fade wrong cards first; second time, "Let's count together", with the things in the scene
  lighting up as they're counted; then the right card pulses.
- **Guessing:** rapid wrong taps count against the level, as in Letter Hunt.

## 10. Grown-up panel

- **Players:** name, prince or princess, banner colour, starting chapter, level.
- **Story:** the steward is Uncle Grimbald or Aunt Grimhilda (with the re-recording warning, §6).
- **Campaign:** the chapter list with each chapter's maths. A **try-it** chip for each task type (practice doesn't
  count).
- **Numbers the child knows:** amount and numeral chips, 0–20, and a "counts to" meter.
- **How it's going:** progress tiles per number and sign.
- **Play:**
  - tasks per stop (automatic by arc, or fixed)
  - stops before making camp
  - take a break
  - music
  - full screen
  - digit style.
- **Voices:** Herald and Narrator sections, step-by-step guides, per-voice backups, microphone test.

## 11. Later arcs: rough framework

Kept loose on purpose; to be designed once the linear arcs are dialled in.

- **Forks (arcs 3–4):** at a crossroads, the herald offers two places by picture and voice ("The mill, or the
  bridge?"). The child taps one. Forts now need **enough troops**, and a fork always offers a recruit stop.
- **Full map (arc 5):** choose freely among towns, forts, castles and special places. Failed attacks return to the
  map. Planning matters: recruit, build, then attack.
- **Places for later:**
  - **Inns**, for tips: what a castle needs to fall, where to recruit more, where treasures hide.
  - **Special places:** caves, secluded lakes and rivers, sacred groves, watchtowers (they reveal the map), farms
    (supplies).
  - **Collectibles** hidden around the map.
- **Army:** companies of ten under banners (arcs 3–4); unit types — foot soldiers, archers, knights, catapults — in
  arc 5.
- **Themed task ideas for later maths:**
  - taking away ("3 goblins ran off, how many are left?")
  - hiding ("5 goblins, 2 visible, how many in the woods?")
  - tens and ones (companies and loose soldiers)
  - 10 more / 10 less (a company joins or leaves)
  - equal groups and arrays (formations: 3 rows of 4)
  - sharing (split 12 soldiers across 3 gates)
  - times tables (supply wagons)
  - greater / less than between 2-digit armies.

## 12. Open questions for the linear arcs

1. Minimum gear per fort: 2 ladders (arc 1); 2 ladders + log and wheels (arc 2)?
2. Chapter names (§5.4): good as drafted?
