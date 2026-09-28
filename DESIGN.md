# Number Knights: design

Maths for toddlers through 3rd grade, played as a young prince or princess leading an army in a righteous cause.
Built on Letter Hunt's tablet framework.

**Status:** the brainstorm decisions are recorded in §2. The two linear arcs (§5) are being designed in detail and
built first. Later arcs (§11) are a rough framework for the future. Items marked *(proposal)* haven't been agreed
yet.

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
| Chapter length | About 8–10 stops |
| Progress | Adaptive difficulty inside each stop; the story moves on only on success |
| Pacing | When the maths isn't ready for the next chapter, the road ahead is blocked and **goblins raid freed villages behind you** |
| Sittings | **Make camp** after a set number of stops (a grown-up setting) |
| Linear view | **Marching scene** (side view), no map until the fork arcs |
| Siege equipment | Built **only when sieging a fort or castle**. Each build round makes one piece, or one group such as ladders. Nothing travels with the party |
| Voices | A **herald** (commands, praise, gentle "not quite"s; robot voice if not recorded) and an optional **narrator** (story; silent if not recorded, text always shown). Each can be recorded by a different person |
| Art | Simple custom SVG |
| Herald | A round, cheerful trumpet herald: fanfare before each command, a sad little "wah-wah" toot for a miss |
| Build order | Linear → forks → full map. Get the linear game really dialled in first |

## 3. The five arcs

| # | Arc | Story | Play space | Maths | Army | Tasks per stop |
|---|---|---|---|---|---|---|
| 1 | **The Goblin Border** | Sent to guard the border villages from goblin raiders | Linear march | Counting and numerals to 10; more or less | Party, up to 10 *(proposal)* | 3 |
| 2 | **The Troll Hills** | Trolls block the hill passes; a troll king in his keep | Linear march | Numbers to 20; the signs + − =; first adding within 5 | Party, up to 20 | 4 |
| 3 | **The Stolen Crown** | Coming home to find the uncle/aunt has seized the throne; rallying loyal towns | Forks (pick one of two) | Adding and taking away within 10 | Companies of ten | 5 |
| 4 | **Siege of the Capital** | Retaking the kingdom, castle by castle, ending at the capital | Forks | Within 20; tens and ones; 2-digit numbers | Companies of ten | 6 |
| 5 | **The Invasion** | A foreign kingdom invades; drive them back | Full map | Within 100 → equal groups → times tables → light division | Companies + unit types | 6–8 |

**Story sketch** *(proposal)*: the king and queen sail off on a peace voyage and leave the hero's uncle (or aunt) as
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
| Fort or castle, **build** rounds | …adds a piece: a ladder, a ram part… | No: at least one piece per round |
| Fort or castle, **assault** round | …as a skirmish, using what was built | Yes: retreat and retry; what was built stays built |
| Raid (a freed village attacked again) | …as a skirmish; the villagers cheer and send a gift | Yes |

"Right" means right **on the first try**. Every task still ends with the right answer found (with help, as in Letter
Hunt), so nothing is left unresolved. First tries only decide the size of the reward and whether a battle is won.

### Failure is funny, never costly
Fewer than half right first time in a battle set: the herald toots "wah-wah", and the army runs back to camp with
speed lines and dust puffs. "Retreat! …Let's try again!" A fresh set of problems follows at the same stop. No
soldier, ladder or freed village is ever lost.

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
campfire, the herald counts the troops (each soldier lights up with a number), and "Rest now, brave Prince Leo!".
With Letter Hunt's "Take a break" on, the game then waits for a grown-up. Otherwise a "Keep marching" button
appears. The next sitting opens with "Wake up! The march goes on!".

## 5. The linear arcs in detail

### 5.1 The marching scene
- **Layout (landscape):** a side-view landscape fills the screen. The top bar has the home button, the herald's
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
  marches over, gets a spear and joins, and the herald counts the party ("7 soldiers!").
- **Goblin camp (skirmish).** Tents and a little palisade, goblins with big ears and pointy spears. Favoured tasks:
  which camp has more goblins, how many goblins. Win: a dust-cloud clash with stars flying, then goblins drop their
  spears and scamper off to the right. Your flag goes up.
- **Troll bridge (arc 2 skirmish).** A troll under a stone bridge: "Nobody crosses MY bridge!" The herald answers
  with maths. Win: the troll grumbles and stomps away into the hills.
- **Fort siege (chapter end).** Two or more sets at one stop:
  - *Arc 1 (goblin stockade):* build **ladders** (each right answer leans another ladder against the wall), then
    **assault**.
  - *Arc 2 (troll keep):* build **ladders**, then a **battering ram** (each right answer adds a part: log, wheels,
    roof, iron head), then **assault**.
  - The assault shows the built gear in action: ladders go up, the ram bangs the gate, the goblins flee out the back
    gate.
  - The gear stays at the fort afterwards; nothing travels on.
- **Raid (pacing).** A freed village behind you, with goblins back. Variety for the long toddler stretches: goblins
  stealing sheep (count them home), goblins in the orchard (apples), goblins on the mill roof, goblins hiding in the
  haystacks. Win: villagers cheer and send a gift (a recruit or a piece of gear). The raid's location is picked from
  the villages already freed.
- **Camp.** See §4.

**A typical chapter** *(proposal)*: village → goblin camp → village → village → goblin camp → village → special stop
(sheep meadow, troll bridge…) → fort (build + assault). That's 8 stops and about 10 sets.

### 5.3 Task types (arcs 1–2)

| Task | Herald says | On screen | Cards | Right answer | Help |
|---|---|---|---|---|---|
| **Find the number** | "Find the banner with 4!" | Banners on poles | 3–9 numeral banners | "4!" (arc 1: the 4 banner shows 4 dots) | Fade wrong ones → pulse the right one |
| **Count them** | "How many goblins?" | 1–10 things in the scene | 3–4 numeral shields | Things light up one by one as the herald counts: "1, 2, 3. 3 goblins!" | Fade → "Let's count together", then pulse |
| **Which is more?** | "Which camp has more goblins?" | Two groups in the scene | The two groups themselves | The bigger camp bounces: "This camp has 5!" | Fade the smaller group → count both together |
| **Find the sign** (arc 2) | "Find the plus!" | Signposts at a crossroads | 2–4 signs: + − = | "Plus! Plus means more are coming." | Fade → pulse |
| **First adding** (arc 2) | "3 soldiers… and 1 more! How many now?" | Soldiers walk in | Numeral shields | Everyone counted: "4 soldiers!" (later with the sentence 3 + 1 = 4 under the scene) | Count together |

- **Early scaffold:** in levels 1–2, numeral shields also show the matching dots under the numeral, so a child who
  doesn't know numerals yet can still match amounts. From level 3 the dots appear only as help after a miss.
- **Later variant:** "Look closely!" versions of Find the number (the banners flip face down, as Letter Hunt's
  memory game does) from about level 4.

### 5.4 Levels and chapters *(proposal)*

| Lv | Arc · Chapter | Numbers | Tasks | Cards |
|---|---|---|---|---|
| 1 | 1 · The Border Road | 1–3 | Find · Count · More (big gaps) | 3, with dots |
| 2 | 1 · The Whispering Woods | 1–5 | Find · Count (dice patterns) · More | 3, with dots |
| 3 | 1 · The Marsh Villages | 1–7 | Find · Count (scattered) · More (closer) | 4 |
| 4 | 1 · The Goblin King's Stockade | 1–10 | Find (incl. "look closely") · Count · More | 4 |
| 5 | 2 · The Stone Bridge | 1–12 | + Find the sign (+ −) | 4 |
| 6 | 2 · Trollberry Hills | 1–20 | Signs + − = · Which number is bigger? (numerals) | 4–6 |
| 7 | 2 · The Echo Pass | 1–20 | + First adding within 5 (pictures) | 4 |
| 8 | 2 · The Troll King's Keep | 1–20 | First adding within 5 with the number sentence | 4 |

- Within a level, the numbers asked come from what the child knows plus the next two, as with Letter Hunt's known
  sounds. The level sets the ceiling.
- **Start point:** when adding a player, the grown-up picks a starting chapter by age (2 → ch. 1, 3 → ch. 2, 4 → ch.
  4, 5 → ch. 6). This can be changed later.

### 5.5 The party
- The party starts as just the hero and the herald: "Let's find brave friends to join us!" The first villages bring
  the first recruits.
- **Cap** *(proposal)*: 10 in arc 1, 20 in arc 2. The party then stays inside the numbers the child is learning, so
  when the herald counts the troops at camp, the child can count along.
- **At the cap,** right answers in villages give **gear** instead: a helmet, a shield, a spear, boots, a cape in the
  hero's colour. A soldier gets one piece each time ("Tom gets a helmet!"). This keeps "more right = more reward"
  going through the long stretches.
- The herald counts the party at every camp, with each soldier lighting up in turn. It's a counting model every
  sitting.

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
- **Two people, two devices:** the grown-up panel has separate Herald and Narrator sections, each with its own
  step-by-step guide and its **own voice backup file**. Importing a voice file adds or replaces only that role's
  clips. So Dad can record the herald on the tablet and Mum the narrator on her phone, then combine them.
- **Robot herald:** the speech-synthesis voice at a slightly lower pitch, a bit slower, with a fanfare before it.

## 7. Look and sound

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
- **Sound:** synthesised, as in Letter Hunt.
  - A trumpet fanfare before commands, and a "wah-wah" toot for a miss.
  - Marching drums (optional music).
  - A rising note per count as things light up.
  - A dust-cloud "bonk", a triumphant flag-raise, and campfire crackle.

## 8. Carried over from Letter Hunt

One self-contained offline HTML file (renamed to `number-knights.html` when building starts), with fonts embedded.
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
  - `q:4` the amount (count them, which is more)
  - `sign:+` the signs
  - later, facts (`+:3+1`).
- **Look-alikes:** numerals 6/9, 2/5 and 1/7 stay off the same board until arc 2.
- **Sound-alikes:** 13/30 … 19/90 stay apart until arc 4.
- **Reversals:** 12/21 are mixed only on purpose, in arc 4.
- **Amounts:** early answer choices are at least 2 apart and in a clear ratio. Later ones are next door (4 vs 5).
  From level 3, the group with *more* is sometimes drawn smaller or tighter, so size isn't a shortcut.
- **Help after a miss:** fade wrong cards first; second time, "Let's count together", with the things in the scene
  lighting up as they're counted; then the right card pulses.
- **Guessing:** rapid wrong taps count against the level, as in Letter Hunt.

## 10. Grown-up panel

- **Players:** name, prince or princess, banner colour, starting chapter, level.
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

1. Party cap: 10 in arc 1 and 20 in arc 2 (so the party stays countable), or 20 throughout?
2. Siege: should build rounds make the assault easier (e.g. each piece built counts as one right answer), or are they
   spectacle only?
3. Blocked road: after the chapter's fort (as drafted), or before it (the fort waits)?
4. Arc 2 extra tasks: add "What comes next?" (number order) or the "look closely" memory version?
5. The story sketch in §3: keep the king and queen on a voyage, or something else?
6. Chapter layout (§5.2) and chapter names (§5.4): good as drafted?
