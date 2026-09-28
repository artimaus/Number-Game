# Number Game: design draft

A draft to talk through before building. Everything here is up for change; the questions at the end are the
ones that shape the most.

**The idea:** a sibling to Letter Hunt. It uses the same tablet framework, the same grown-up panel and the same "a
grown-up's voice asks, the child taps" loop. The content is numbers and early maths, from "tap the ducks to count
them" at about age 2 up to first-grade work: sums within 20, tens and ones, and numbers to 120.

---

## 1. What we keep from Letter Hunt

Letter Hunt's framework is already built for toddlers on a tablet, so we keep almost all of it:

| Letter Hunt piece | Keep? | Notes |
|---|---|---|
| One self-contained offline HTML file (fonts embedded, no network) | Yes | `Number-Game.html`. Opens from a file, a web address, or a Claude artifact. |
| Screens: start → players → play → party, plus a collection and the grown-up panel | Yes | Same flow and the same big, chunky buttons. |
| Long press counts as a tap; ghost taps are swallowed; no long-press menu, pinch or scroll | Yes | Copied as is. |
| Hold the gear for 1.5 s to open grown-up settings | Yes | |
| `say([...])`: joins recorded clips, with the robot voice filling any gaps | Yes | Numbers are built from clips ("twenty" + "three"). |
| Recording: step-by-step guide, waveform, auto-trim, import files by name, backup/restore | Yes | New clip list (§10). |
| Synthesised sound effects, optional music | Yes | Plus a rising note for each count (§11). |
| Profiles, levels, sets of 3–5 rounds with stars, level up at 85% / down quietly at 50% | Yes | Plus a start level by age and a faster climb (§6). |
| Guess detection (a wrong tap < 0.7 s after the question) | Yes | |
| Review boxes (spaced repetition) and the known-sounds pool | Yes | Tracked per number and per maths fact instead (§7). |
| Help after a miss: fade some wrong cards, then pulse the right one | Changed | Second help becomes "let's count together" (§8). |
| The question repeats after 12 s; cards stay locked while it's spoken | Yes | |
| "Which game do you want to play?" now and then; Take a break; full screen; dark mode | Yes | |
| Level map with try-it chips; progress tiles in green/yellow/red | Yes | Plus an addition-facts grid (§9). |
| Letter collection (letters "wake up") | Changed | Becomes the number collection (§11). |
| Spell my name (a personal button that unlocks) | Changed | Becomes the birthday cake (§11). |

Build approach: **fork the file, not a shared library.** Copy the framework, rename the storage keys
(`numbergame.v1`, IndexedDB `numbergame`), and keep function names parallel (`say`, `ask`, `nextRound`,
`logStep`, `checkLevel`…) so a fix in one game ports easily to the other.

## 2. What's different about numbers

1. **The robot voice can say numbers.** In Letter Hunt it can't say single sounds, so recordings were close to
   essential. Here the robot voice covers everything, and recordings are a warmth upgrade. One exception is
   *tap to count*: the robot voice lags a little on some tablets, and counting has to keep up with the finger. So
   the recording guide should put numbers 1–10 first.
2. **The content is quantity, not only symbols.** A letter is a shape and a sound. A number is a shape, a word *and
   an amount*. So most games need a **scene** (ducks in a pond, carrots on a plate) as well as the card grid. The
   grid stays as the answer picker; the top "target" area becomes the stage.
3. **Two kinds of knowing grow separately.** Knowing *how many* (quantity) and *which numeral* (symbol) are
   tracked apart, just as Letter Hunt keeps letter names and sounds apart. First-grade work adds a third kind:
   maths facts.
4. **The age range is wide** (about 2 to 7). A 5-year-old shouldn't have to climb through ten toddler levels.
   So there's a start level by age and a faster climb for players who are clearly past a level.
5. **Mistakes carry meaning.** Counting a duck twice, or stopping at 4 when asked for 3, tells us exactly what the
   child doesn't yet get (one-to-one counting, and knowing that the last number said is "how many"). The games are
   built so these mistakes can happen and get gentle, specific help.

## 3. The learning path (what the levels follow)

This is the standard early-numeracy progression. Each step builds on the one before:

1. **Seeing small amounts at a glance** (1–3, then to 5): "that's 2" without counting.
2. **Saying the counting words in order**: 1–10, then 20, later 100 and 120.
3. **One-to-one counting**: one number per thing, each thing counted once.
4. **The last number counted is how many.** This is the big milestone around 3½–4. It's tested by "give me N"
   (hand over exactly N) rather than "count these".
5. **Numerals**: knowing the written 1–10, then 0–20, then 2-digit numbers.
6. **Comparing**: more, fewer, the same; which number is bigger.
7. **Order**: what comes next or before; counting on from a number; counting back.
8. **Taking numbers apart and putting them together**: 5 is 2 and 3; ten-frames; pairs that make 10.
9. **Adding and taking away**: first as stories with things, then as number sentences. Within 5 → 10 → 20.
10. **Tens and ones**: 34 is 3 tens and 4 ones; 10 more, 10 less; counting to 120.

Kindergarten and first-grade standards also cover shapes, time, money and measuring. **This draft is numbers only**
(open question 2).

## 4. How a child acts on the screen

Letter Hunt has tap-a-card plus one drag game. Numbers need a few more kinds of touch, all big and forgiving:

| Touch | What it does | Used by |
|---|---|---|
| **Tap to choose** | Tap an answer card (as in Letter Hunt) | Most games |
| **Tap to count** | Tap each thing once; it hops, gets a number badge, and the voice counts. Tapping one that's already counted just bumps it, with no new number. | Count with me, dot-to-dot, birthday cake |
| **Tap to move** | Tap a thing to hop it to the plate; tap it on the plate to hop it back. No dragging needed. | Feed the animal, ten-frames, tens and ones |
| **Drag** (older levels, optional) | As Match the Sound does it, with generous drop zones | Maybe the alligator, maybe tens and ones |

**No timers the child can see, no lives, nothing taken away.** Quick look shows a picture briefly, but answering is
never timed. Fact fluency is judged quietly from response time (§7).

## 5. The games

Each game is a "line" with versions per level, like Letter Hunt's `ACTS` table. Banner colours and icons as in
Letter Hunt.

### Count with me (tap to count)
- **Screen:** 1–10 things (ducks, apples…) spread over the stage. **Voice:** "Let's count the ducks!"
- Each tap on an uncounted duck: it hops, a numbered badge appears (1, 2, 3…), the voice counts, and a note one
  step higher plays. A second tap on a counted duck bumps it; no number.
- After the last one, they all bounce together and a big **3** appears: "3! 3 ducks."
- **Later:** the badges hide at the end and the voice asks "How many ducks?". Answer from numeral cards. A child
  who recounts instead of answering hasn't got "the last number is how many" yet.
- **Big sets (6+):** each tap moves the duck into a tidy line, with its number underneath. This models keeping
  track.
- **Mistakes tracked:** double counts (one-to-one). It can't otherwise be failed, which makes it a good first
  game.

### Show me / How many?
- **Show me N** (number word → amount): "Show me 2!" Tap the card with 2 things among cards of 1 and 3.
- **How many?** (amount → numeral): a group of things on the stage. "How many apples?" Tap 2, 3 or 5.
- Arrangements get harder: dice patterns → in a line → scattered → ten-frames.
- Early on, wrong answers are far apart (2 vs 5); later they're next to each other (4 vs 5).
- **Right:** the things light up one by one as they're counted aloud: "1, 2, 3. 3 apples!"

### Find the number
- A port of Find the letter: "Find 4!" among 3, 4, 9 or 16 numeral cards.
- The range grows 1–3 → 1–5 → 1–10 → 0–20 → 2-digit (§7).
- **Right:** "4!" and, at younger levels, 4 dots appear under the numeral so the symbol stays tied to an amount.

### Quick look (seeing amounts at a glance)
- Reuses the memory-game card flip. A dot card shows for about 1.5 s, then flips face down. "How many did you
  see?" Pick the numeral.
- Dice patterns 1–3 → dice 1–6 → ten-frames 1–10 → a full ten-frame plus some (the teens) → fingers (SVG hands,
  later).
- The point is to stop one-by-one counting and build "5 and 2 more is 7".

### Feed the animal (give me N)
- **Screen:** 🐰 with a plate; a pile of 🥕 below. **Voice:** "Bunny wants 3 carrots!"
- Tap a carrot: it hops to the plate as the voice counts ("1… 2…"). Tap one on the plate: it hops back.
- **Young levels:** the bunny eats as soon as there are 3.
- **Real give-N (about level 4 up):** the child taps the bunny when done. With 3: "Yum, 3 carrots!" With too many:
  "That's 4! Bunny wants 3." Nothing is taken back automatically; the child fixes it.
- **Later:** "Bunny has 2. He wants 5. Give him more!" This is counting on, the first step toward missing-number
  sums.
- Pairs: 🐰🥕 🐵🍌 🐭🧀 🐶🦴 🐿️🌰 🐼🎋.

### More or less
- Two trays: "Which has more?" Tap one. Later: "Which has fewer?" and "Are they the same?"
- The difference shrinks with level: 1 vs 4 → 4 vs 6 → 5 vs 6.
- **Size trick:** from about level 7, the tray with *more* sometimes has smaller or more tightly packed things, so
  the bigger-looking tray isn't always the answer. This makes the child count rather than judge by area.
- **Numerals:** "Which is bigger, 7 or 4?"
- **First grade:** the hungry alligator eats the bigger number (> < =), up to 2-digit numbers.

### Number train (order)
- Train cars 1 2 3 _: "What comes next?" Pick from numeral cards. The train chugs off, saying the whole run.
- Missing in the middle → counting back ("What comes before?") → **Blast off!** (a rocket counting 10 → 0,
  which introduces zero) → counting by 10s, 5s and 2s → windows on a hundred chart (first grade).

### Number memory / Clear the board
- Ports of the memory games: "Look closely! Find 7…", flip, find. Clear the board: several finds per board.
- Later versions mix numerals and dot cards on one board.

### Dot-to-dot
- Numbers scattered on the stage. Tap them in order (1, 2, 3…); a line draws from dot to dot and the voice says
  each number. When the shape closes, it fills with colour and becomes a star, fish, rocket, house…
- **Wrong tap:** that number wiggles. "That's 7. What comes after 4?"
- 1–5 → 1–10 → 1–20 → counting by 2s, 5s and 10s.

### Story sums (adding and taking away)
- **Scenes:** ducks in a pond, a bus with seats, birds on a branch, apples on a tree.
- **Adding:** "2 ducks are swimming… and 1 more!" (it waddles in) "How many now?"
- **Taking away:** "4 birds on a branch. 1 flies away. How many are left?"
- **Bridge to symbols (about level 11 up):** the number sentence builds under the scene as the story happens:
  **2** … **+ 1** … **= ?**. Each part lights up with its part of the story.
- **Help:** "Let's count them together."

### Hiding game (missing part)
- "5 mice. Some ran into the house!" Two mice are still outside. "How many are hiding?"
- **Answer:** the roof lifts and the hiding mice count out: "3 were hiding! 2 and 3 make 5."
- Toddlers love peek-a-boo, and this is the friendliest way into number bonds and missing-number sums.

### Ten-frames / Make ten
- "Make 7": tap cells to fill a ten-frame. "How many more to make 10?"
- Two frames for the teens: "10 and 4 more is 14."

### Tens and ones (first grade)
- "Build 34": tap the rod pile to add a ten ("10, 20, 30"), then the cube pile for ones ("31, 32, 33, 34").
- Then: "What's 10 more than 23?" and hundred-chart hops.

### Fact rocket (first grade)
- 3 + 4 = ? with answer cards. Each right answer adds fuel; a full tank launches the rocket.
- Facts come from review boxes (§7), so tricky ones come back and known ones spread out over days.
- Tricks it teaches: doubles, near-doubles, make ten (8 + 5 = 8 + 2 + 3).

## 6. Level map (draft: 16 levels in 4 bands)

Each round picks a line at random, avoiding the same line twice running, as in Letter Hunt. A line's version
depends on the level. "To N" is the most the level allows; the actual numbers come from what the child knows (§7).

| Lv | Band (rough age) | Numbers | Games at this level |
|---|---|---|---|
| 1 | **Little counters** (2–3) | to 3 | Count with me · Show me (2 cards, far apart) · Feed the bunny (eats by itself) |
| 2 | | to 3 | Count with me · Show me (3 cards) · Find the number (3 cards) · Feed the bunny |
| 3 | | to 5 | Count with me · Quick look (dice to 3) · More or less (big gaps) · Find the number |
| 4 | | to 5 | How many? (numerals) · Feed the bunny (tap when done: real give-N) · Quick look (dice to 5) · Memory (3) |
| 5 | **Preschool** (3–4) | to 10 | Count with me (lines up) · How many? · Find the number (4) · More or less · Number train (next, to 5) |
| 6 | | to 10 | Feed (to 10) · Quick look (dice to 6) · Memory (4) · Number train (to 10) · Dot-to-dot (to 10) |
| 7 | | 0–10 | Quick look (ten-frames) · Which is bigger? (numerals, size trick) · Clear the board (9) · Blast off (10 → 0) |
| 8 | **Kindergarten** (5) | 0–10 | Story sums: adding within 5 · Hiding game within 5 · How many? (ten-frames) · Find the number (9) |
| 9 | | 0–10 | Story sums: taking away within 5 · Hiding game · Train (missing, counting back) · Dot-to-dot (to 20) |
| 10 | | 0–20 | Teens (10 and some more) · Find the number (0–20) · Story sums within 10 · Make ten |
| 11 | | 0–20 | Story sums with the number sentence · Hiding game within 10 · Make ten · Train by 10s |
| 12 | | 0–20 | Fact rocket (+ and − within 5) · Which is bigger? (to 20) · Clear the board (16) · Mixed story sums |
| 13 | **First grade** (6) | 0–20 | Fact rocket within 10 · Story sums within 20 (make ten, doubles) · Missing number (3 + _ = 7) |
| 14 | | to 100 | Tens and ones · Count by 10s · Alligator (> < =, 2-digit) · Fact rocket within 10 |
| 15 | | to 120 | 10 more / 10 less · Hundred chart · Fact rocket within 20 · Find the number (2-digit) |
| 16 | | to 120 | 2-digit + 1-digit and + tens · Mixed fact rocket · Alligator · Clear the board (reversals together) |

**Start level:** when adding a player, the grown-up picks an age or a starting band (2 → L1, 3 → L3, 4 → L5, 5 → L8,
6 → L12). The level can still be changed in settings at any time.

**Faster climb:** Letter Hunt needs 10 rounds at 85% to move up. Here, **5 rounds in a row with every step right
first time** also moves up, so a child who is past a level leaves it within one set. Moving down stays quiet and
slow, as now.

## 7. What's tracked, and how the numbers are chosen

- **Per number**, in review boxes as in Letter Hunt:
  - `q:7`: quantity (how many, show me, give me)
  - `n:7`: the numeral (find, pick the written 7)
- **Per fact** (level 8+): `+:3+4`, `-:7-2`, `b:5=2+3` (number bonds). A fact counts as **fluent** once it's right
  first time and answered within about 4 s, 4 of the last 5 times. The child never sees a clock.
- **Number range:** as with Letter Hunt's known sounds, the pool is the numbers the child knows plus the next two. The
  level sets the ceiling. A level-5 player who knows 1–6 gets 1–8, not 1–10.
- **"Counts to" number:** the highest N where quantities 1…N are all known. The grown-up panel shows it ("Leo
  reliably counts and gives up to 6"). It's the most useful single number to track at this age.

### Look-alikes and sound-alikes (the maths version of b/d/p/q)
- **Look-alike numerals:** 6/9, 2/5, 1/7. Kept off the same board below level 10, then allowed on purpose, as the
  mirror letters are.
- **Sound-alikes:** 13/30, 14/40, 15/50… 19/90. Kept apart until level 15.
- **Reversals:** 12/21, 13/31, 17/71. Kept apart until level 16, then mixed on purpose.
- **Amounts:** close amounts (4 vs 5) are hard to tell apart at a glance. Early boards keep answer choices at least
  2 apart and in a clear ratio; later boards use next-door numbers.

## 8. Help after a miss

- **First miss:** "That's 5." Fade one or two wrong cards, as in Letter Hunt.
- **Second miss:** "Let's count together." The things on the stage light up one at a time with their numbers, then
  the right card pulses. The hint is the skill itself, not only a pointer to the answer.
- **Feed the bunny, too many:** "That's 4! Bunny wants 3." The extra carrot wiggles, but the child moves it.
- **Dot-to-dot, wrong number:** "What comes after 4?" The count so far replays.

## 9. Grown-up panel

The same layout as Letter Hunt, with:
- **Players:** name, **age or birthday** (optional: sets the start level and powers the birthday cake), level,
  start band.
- **Level map** with try-it chips, as now.
- **"Numbers Leo knows":** chips 0–20 in two rows (amount and numeral), plus a "counts to" meter.
- **How it's going:** progress tiles for numbers, plus an **addition grid** (0–10 × 0–10), with each fact green,
  yellow, red or not yet seen. It shows at a glance which facts are solid.
- **Digit style:** *School* (a plain 1, an open 4, as most kids are taught to write them) or *Book* (1 with a foot,
  closed 4). The embedded Andika font already has both through its `cv01`/`cv04` variants, so this costs one CSS
  line.
- **Play:** rounds per set, take a break, let them pick the game, music, full screen. All as now.

## 10. Voice clips

The robot voice covers everything, so recording is optional.

| Group | Clips | Count |
|---|---|---|
| Numbers | "zero" … "twenty", "thirty" … "ninety", "one hundred". 21–120 are built from these ("twenty" + "three") | 29 |
| Phrases | "Let's count the…", "How many…", "Show me…", "Find…", "That's…", "Look quickly!", "How many did you see?", "Which has more?", "Which has fewer?", "Which is bigger?", "The same!", "What comes next?", "What comes before?", "…wants…", "Too many!", "…and… more", "How many now?", "…flies away", "How many are left?", "Some are hiding! How many are hiding?", "…make…", "plus", "take away", "equals", "tens", "ones", "Blast off!", "Happy birthday!", "You are…" | ~30 |
| Things (plural only) | "ducks", "apples", "carrots", "mice"… Scripts are written so a singular is never needed ("…and 1 more!", not "here comes 1 more duck") | ~16 |
| Praise and shared phrases | Same keys as Letter Hunt: `praise_1…8`, `you_did_it`, `level_up`, `kept_trying`, `pick_game`, `go_find`, `my_praise_*` | ~15 |
| Names | `child_<name>` | 1 per player |

About 90 clips, against Letter Hunt's ~150. **Numbers 1–10 come first** in the step-by-step guide (for snappy
counting).

**Sharing with Letter Hunt:** praise, names and the "take a break" line use the *same keys*. So "Restore backup"
here can read a Letter Hunt backup file and take the clips that match. A parent who recorded cheers once gets them
in both games.

## 11. Look, sound and rewards

- **Board:** Letter Hunt's dotted board and card style, so the two feel like siblings, but in a different colour
  (warm sand or peach instead of mint), so they're easy to tell apart. The same palette, shadows and big buttons.
- **Numerals:** Andika, as now (§9 digit style).
- **Things to count:** emoji, as Letter Hunt uses for pictures. They're chosen to be one clear thing each: 🦆 🍎 🐟
  ⭐ 🚗 🐝 🐸 🍓 🎈 🍪 🦋 🐞 🥕 🥚 🐤 🌸. **Never** 🍒 (two cherries), 🍇 (a bunch), 🧦 (a pair) or 🎲 (dots that
  would confuse the count).
- **Other pictures of amounts:** dice dots, ten-frames, the number train, and (first grade) tens rods and ones
  cubes. All drawn in SVG, so they're crisp and themeable.
- **Counting notes:** each count plays the next note of a scale (1 = do, 2 = re…), so counting higher *sounds*
  higher. Adding plays a little chord; taking away has a soft "whoosh".
- **Number collection** (the letter collection's twin): 0–20 as tiles that wake up when both `q:` and `n:` reach
  box 3. Tapping an awake number says its name and shows that many dots in a ten-frame. A row of tens (30…120)
  appears in first grade.
- **Birthday cake** (the twin of "Spell my name"): unlocks at level 3 if an age is set, then gets its own
  home-screen button. A cake shows the child's age in candles, which they tap to light and count: "1, 2, 3, 4…
  Happy birthday! You are 4!" At higher levels: "How old will you be next birthday?" (+1), and "How many more
  candles until you're 10?"
- **Star jar** (optional): the stars earned drop into a jar in groups of ten. "You have 3 tens and 4. 34 stars!"
  The reward teaches tens and ones by itself.

## 12. Build order

Each step is playable on the tablet before the next starts.

1. **Framework port.** Screens, profiles, audio, recording, backup, grown-up panel, and the level table skeleton,
   with the first three games: Count with me, Show me / How many?, and Find the number. Levels 1–2 fully
   playable.
2. **Band 1–2 (levels 1–7).** Feed the bunny, Quick look, More or less, Memory, Number train, Dot-to-dot, number
   collection, birthday cake.
3. **Band 3 (levels 8–12).** Story sums, Hiding game, Make ten, teens, Fact rocket (within 5).
4. **Band 4 (levels 13–16).** Fact rocket to 20, Tens and ones, Alligator, hundred chart, 2-digit numbers.

Before step 1, it may help to make a **clickable mockup** of the new touch styles (tap to count, feed the bunny,
quick look) to try on the tablet, as was done for Match the Sound.

## 13. Open questions

1. **Who's playing, and how old are they now?** This decides which band to build first and to polish most.
2. **Scope:** numbers only, or also shapes, patterns (AB AB), time or money later?
3. **Name:** "Number Hunt", to pair with Letter Hunt, or something else ("Count With Me", "Number Friends")?
4. **Voice:** share praise and name recordings with Letter Hunt through its backup file?
5. **Digit style default:** school-style (plain 1, open 4) or book-style?
6. **Touch:** tap-to-move everywhere, or drag at the older levels as well?
7. **Rewards:** number collection + birthday cake (proposed); add the star jar?
8. **Levels:** does 16 levels with a start-by-age choice feel right, or stay closer to Letter Hunt's 12?
