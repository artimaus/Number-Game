# Number Knights — quality pass (October 2026)

A full pass over the built game after arc 3: four focused reviews (game flow, maths tasks, audio and recordings,
words), a visual sweep of every scene in all twelve chapters and every task type at its level, the grown-up panel at
six screen sizes and in dark mode, hands-on interaction tests, and full regression runs of all three arcs.

**Verdict:** the core is solid. About 150,000 generated tasks produced no wrong answers, no run threw a page error,
playback chains can't hang, and the interaction edge cases (double taps, Home mid-task, rotating, speak-button spam,
switching players) behaved. What was found is listed below, most important first. `[x]` means fixed; `[ ]` means
still open (B was done in a second batch). Line references are to the source parts in the build tree (`30-core.js`, `60-game.js`, …).

## A. Fix first — a child or parent would hit these

- [x] **A1. Chapter 1's Goblin Lookout drew the chapter 12 Lookout Stone.** Both stops used `id:"lookout",
  place:"lookout"`, and the arc 3 `PLACES` override won: goblins stood in front of the sea and two signposts on the
  meadow, and the flag-raise after the win was skipped (no `.ourflag`). Fixed: the chapter 12 stop and place are
  `lookoutstone`. Stop ids are now unique across the game.
- [x] **A2. Singulars after "1".** "We have 1 soldiers!", "1 chickens!", "1 villagers!", "1 … stomp off!",
  "1 … are sold!", "1 were hiding!", "4 plus 5 make 9". Fixed: every counted thing has a singular clip (`w1_<thing>`,
  "chicken"), the taking-away calls have singular twins (`stomp_off_1` "…stomps off!", `go_home_1`, `are_sold_1`,
  `roll_away_1`, `go_away_1`, `sail_away_1`, `fly_away_1`), plus `were_hiding_1` "…was hiding!" and `makes_1`
  "makes" for the missing number; `w_soldier` is used after 1 in every arc. The robot voice fills in until they're
  recorded. (Decision: the full set, 33 nouns + 9 twins.)
- [x] **A3. Counting stayed at 1–3 for a child started at a later chapter.** Count/Find targets only grow as numbers
  become "known", and "Start at chapter" never seeded that list; the "Count to 20" try-it button showed 1–3 too.
  Fixed: moving a player forward marks 1…(previous chapter's max) as known for counting and numerals (moving back
  changes nothing; the grown-up can still untick numbers), and practice uses the level's whole range.
- [x] **A4. Answer cards overshot the level's range** (21/22 in "numbers to 20", a 13 at level 5, 9–12 for "7 + 3"
  in the within-10 levels, "11 more make ten"). Fixed in `nearCards`: distractors stay inside the level's numbers
  unless there aren't enough; What comes next keeps its cards at or below the top; the missing number always has four
  cards.
- [x] **A5. Part of the army was off-screen on a 4:3 iPad.** Company slots at x −60 and −125 only exist on wider
  screens. Fixed: the slots fill the on-screen positions first, so the first seven companies are always visible and
  only companies 8–10 sit at the left edge. (Decision: reorder rather than shrink.)
- [x] **A6. Recording UI error paths.** Fixed all four: a microphone denial or an unsupported browser now tells the
  guide (which no longer sits on "Stop / Recording…") and status messages show inside the guide while it's open; a
  microphone track that iOS has ended (screen lock) is reopened, and a `MediaRecorder.start()` failure is reported
  instead of silently killing recording for the session; "Saved" is only shown when the clip was actually stored,
  otherwise a clear "couldn't be saved on this device" message; restoring a *full* backup asks first when the device
  already has recordings or progress.
- [x] **A7. "A ladder!" was never heard** (`say` not awaited; the next prompt cancelled it within a millisecond).
  Fixed: awaited at both call sites.
- [x] **A8. Two Home-button races.** Home while the herald was asking left `G.hearing` stuck (dead "hear again" and
  no repeat on the next fork); Home mid-march let the abandoned march overwrite the next player's scene. Fixed:
  `goHome`/`openParent` reset `hearing`/`repeats`; `marchTo` checks its session before writing the scene; `sceneFor`
  cancels any sliding place and clears `#placeNext`.
- [x] **A9. "…Sir Snivelwick jingling her keys"** in the Aunt Grimhilda line (`st3_4_16`). Fixed: "his keys".
- [x] **A10. Clips the parent was asked to record for nothing.** `fly_away` (filed under Always, so in a brand-new
  player's Record next) — Puffin Point now has a taking-away task so "3 puffins fly away!" is heard (decision: use
  it rather than drop it); `w_berries` (berries only ever compared) — thing-name clips are now only made for the
  kinds of task that say them; `go_away`, `w_company` — marked optional; both `title_prince` and `title_princess`
  demanded for every player — filtered to the player's own title; `h_pick_apples` duplicated `h_apples_back` —
  removed, the orchard uses the chapter 4 call; the tens (30–100) now live in "Numbers" with "From chapter 12"
  instead of under a note saying "Not needed yet".

## B. Worth doing

### Flow edges
- [x] B1. A fork choice is saved before the branch is played (`runFork`); quit mid-branch and the resumed fork can be
  answered the other way, after which the troop check sends the army "back" for a third helping of recruits. Record
  the choice after the branch returns (keep a transient choice for the road strip). Fixed: the choice is saved after the branch returns (the road strip shows it meanwhile).
- [x] B2. The camp right after the Troll King's Keep announces "1 company and 7 soldiers" before the army is topped
  up to 20 (`chapterEnd` advances `P.ch` before `makeCamp`). Top up and redraw after `P.ch++`.
- [x] B3. "Start at chapter" leaves old fork choices (`forks`) and "opening seen" flags (`seenOpen`), so a replayed
  chapter skips its opening and shows both branches lit. Clear them for the chapter moved to.
- [x] B4. The blocked-road drawing can appear on the last raid's land (a snowdrift on chapter 1's meadow): re-render
  the chapter's land before showing the block.
- [x] B5. Locking the tablet mid-narration leaves the cut caption over the next task, and the repeat timer disarms
  itself while hidden; on return the prompt isn't repeated (the speak button still works). Hide the caption when
  `narrate` is cut; re-ask on `visibilitychange` → visible. Fixed: the repeat timer re-arms while hidden, and coming back with a task up asks the prompt again.
- [x] B6. Leaks that are only cosmetic: `joinUp`'s timer and `nutRain` can draw into a new session within a second;
  `chooseFork`'s promise is never settled by Home; `addRam` caps at 4 but the fifth right answer still says
  "h_ram_part"; `G.stepFirst` and `n0` are dead. Fixed: session checks in both timers, Home settles the fork wait, the ram stops at four parts, dead code removed.

### Pedagogy and tasks
- [x] B7. "Count the companies" never asks for 100 (100 is only ever a distractor).
- [x] B8. The arithmetic types (add, sub, num, hide, diff, miss) have no recent-list or spaced repetition, unlike
  counting; the same sum can repeat back to back. Fixed: the sums keep a short recent list and are regenerated if they would repeat.
- [x] B9. Practice "Taking away" at level 8 is the harder stop-4+ version, not the "first taste"; "Find the sign"
  can only be tried at level 5, so the `=` version can't be tried. `sub.sentence` is an object in practice (code
  smell: `late = G.practice || …`). Fixed: practice at level 8 is the first taste; "Find the sign (with =)" is a level 6 try-it button.
- [x] B10. "Which number is bigger?" draws trolls holding the shields in arc 3; the scripts say guards. Fixed: Grey Guards hold the shields from arc 3.
- [x] B11. `hide.sayOpts` lights the seen dots by prompt index, which shifts on the re-ask (no visible effect; test
  the key only). "Which is more?" at level 6 can pair 1 vs 12 while the level text says "close amounts".

### Recording polish
- [x] B12. Record-next narrator lines aren't in the order they're heard: the camp and retreat lines a chapter 1
  child hears on day one are items 50–54 of the guide. Sort narrator lines by `from` like the herald's.
- [x] B13. The guide's 3-2-1 countdown runs before the microphone permission prompt, so the first-ever take is
  "too short". Acquire the mic before the countdown.
- [x] B14. 15 s narrator cap with no warning (the longest lines read storybook-slow get close); suggest 25 s and a
  visible countdown. Silence trimming at −18 dB with a 100 ms tail may clip a final "s"; use 200 ms. Fixed: 25 s for the narrator with a ticking "N s left", 200 ms tail.
- [x] B15. Editing an aunt line flags the uncle recording as changed (`sigOf` hashes both variants); the caption
  fallback is capped at 7 s, too short for long lines; declining the download prompt still clears the "unsaved"
  count; `echo()` buffers can't be stopped by `stopSpeech`; imported clips with unknown keys stay in IndexedDB
  invisibly; `robotOK()` reads voices before `voiceschanged` and can wrongly warn there's no robot voice. Fixed except the download count: a declined download can't be detected, so the "since the last backup" count still resets when the file is offered. Also: recordings whose clip this version no longer uses are listed at the end of the tree with a delete button; signatures now ignore capitals, curly apostrophes and spacing, and carry over once (`sigVer`) where the words didn't change.
- [x] B16. "Record next" wording: "Still to record for chapter 12: 31 story lines and 155 herald clips" counts
  every clip the chapter uses, most of them the everyday ones; say so.

### Words and docs
- [x] B17. British spelling: "toward" ×2 (`st1_2_17`, `st3_1_01`) → "towards"; "skipping stones" (`st2_1_10`) →
  "skimming"; "Pee-yew!" (`st1_4_11`) is American; "Ta-ra!" (`h_intro`) reads as "bye" in Britain. Fixed: towards, skimming, "Pooh, what a pong!", "Ta-daa!".
- [x] B18. Chapter 8→9 join: "At last… / At last…" back to back (`st2_4_21`, `st3_1_01`), and `st2_4_21` mentions
  snow while the block is a storm. Suggested: "The storm blew itself out, and the mountain road was open again." Fixed with the suggested line.
- [x] B19. Panel copy: "Counts: reliably counts to 0" on a fresh profile; "Which is fewer?" → "Which has fewer?";
  the age table ("…8+ → 9") disagrees with DESIGN.md §5.4's; `we_have`'s hint doesn't mention companies. Fixed; the age table in DESIGN.md now matches the panel's.
- [x] B20. Straight and curly apostrophes are mixed across NARR/HERALD/panel; "Grey Guards" vs "grey guards" is
  inconsistent (pick proper name or description); "Siege of the Capital" is the only arc title without "The". Fixed in the story and herald texts (the panel's own strings still mix straight and curly apostrophes); "Grey Guards" is a proper name everywhere; "The Siege of the Capital".
- [x] B21. Chapter scripts vs game: "Which pile/rock has more…" (game says "Which side"); "Let's show him" (clip says
  "them"); "Harvest Hollow sent more friends!" (clip: "The loyal villages sent…"); chapter 1 says "cap of 10" (it's
  5); a lantern listed as a raid treasure; "New clips" lists in arc 3 name old clips; 2-4's "after arc 2" section is
  stale now that arc 3 exists. Fixed.
- [x] B22. DESIGN.md staleness: example lines that aren't in the game (§4 "The woodcutters cleared the road!",
  "Which camp has more goblins?", "n_4"/"well_done" keys), "(proposal)" markers on settled things (camp after 4,
  two ladders, §5.4, the steward warning), §5.4's age table vs the panel's, "3rd grade", gear list (five pieces;
  the game has three), card counts (Find 3–9 banners → 3–4, Look closely 4–9 → up to 6), "Numbers to 100 from 29
  recordings" (28), "one palette per chapter (meadow, woods, marsh, hills, pass)" (twelve lands plus night),
  "more or less" → "more or fewer". Fixed.
- [x] B23. Longest narrator lines (23–25 words with a quote) — `st3_4_15`, `st2_2_14` — could lose a clause for a
  four-year-old listening. Fixed: "every night" dropped; Crackjaw's line ends "Off he hopped, all the way to the Echo Pass."

### Visual
- [x] B24. Dark mode: `--muted` isn't redefined, so the panel's helper text is dark grey on dark navy.
- [x] B25. The number-sentence board shows as a blank white strip for about a second before "9 − 3 = ?" writes
  itself in; draw it with the first piece.
- [x] B26. "100" slightly overruns the shield face (`ttl` 64 → 56 for three digits); the board "?" doesn't pulse
  like the stepping-stone one; `#things .glowspot` opacity overrides the per-task inline values.

## C. iPad-only — code-side mitigations in place; still needs a real-device test

- [x] C1. `speechSynthesis.cancel()` immediately followed by `speak()` is a known WebKit quirk that drops the
  utterance, so an unrecorded prompt can come out silent (the child then waits 12 s for the repeat). Cancel only when
  speaking/pending, or leave ~100 ms after a cancel. Mitigated: `cancel()` only when something is speaking or pending, a 150 ms gap before the next `speak()`, `resume()` if paused, and the utterance is held on to. Confirm on the device.
- [x] C2. The AudioContext is only resumed from "suspended", not iOS's "interrupted" state (after a call or Siri):
  `if (ac.state !== "running") ac.resume()`. Mitigated: the context is resumed whenever it isn't "running" (on every tap and on returning to the page). Confirm on the device.
- [x] C3. The mic is held open from the first take until the panel closes; on iOS that changes audio routing and
  volume and can pitch-shift Web Audio created before `getUserMedia`. Release it shortly after each take. Mitigated: the microphone is opened for each take and closed right after it. Confirm on the device.
- [x] C4. Storage weight: clips are 16-bit WAV at 44/48 kHz, so a full set is ~170 MB in IndexedDB and a full backup
  builds a ~230 MB JSON string in memory (likely to crash an iPad tab); the decoded-buffer cache is never evicted.
  Resample to 16–22 kHz before `wav()`, build the backup from Blob parts, evict old buffers. Mitigated: takes are stored at 22 kHz (less than half the space), backups are assembled from one piece per recording, and the decoded cache keeps the 60 most recently played clips. A full set is now roughly 80 MB.
- [x] C5. Safari deletes site storage (recordings and progress) after seven days without a visit unless the page is
  added to the Home Screen; `navigator.storage.persist()` is a no-op there. Add a Home Screen hint on iOS. Mitigated: the Voices section shows an "add this page to the Home Screen" note on an iPad in Safari (not when already opened from the Home Screen).
- [x] C6. `decode()` has no timeout: if `decodeAudioData` never settles for a clip, that line waits indefinitely
  (not observed). Fast double-tap on a profile card has no guard beyond the 700 ms pointer shim (not tested). Mitigated: decoding gives up after 8 s (the clip counts as unplayable, the robot or caption fills in); a second tap on a player card within 1.5 s is ignored.

## D. Checked and fine

All referenced clips exist and all 300 narrator lines are reachable; every chapter script matches the game's stops
and names; every generator keeps the answer among the cards, never duplicates a card, and never produces a zero or
negative; the difficulty ramp is monotonic; all 90-odd places render on their lands; the siege, feast, crown and
rider sequences run; portrait works (letterboxed); the DOM stays light (3,700 nodes with a 100-soldier army, 10 ms
to redraw); `numJoin` handles 0/10/20/100 and >100; `stale`/`changed`/`todo`/`remindOn` match DESIGN.md §6.
