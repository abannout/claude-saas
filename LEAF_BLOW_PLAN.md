# LEAF BLOW: build and pitch plan (Sep 2026)

Leaf Blow is a hybrid-casual colour-sort puzzle about leaf blowing, monetized with IAP + ads, built by a solo dev and pitched to publishers.

---

## 1. Why this game

**The gap**
- Hybrid-casual puzzle is the growth engine: IAP +20% to $4.2B ([Azur Games](https://azurgames.com/blog/hypercasual-and-hybrid-casual-in-2026-full-report/)).
- Its best-earning structure (reveal-by-colour + limited slots + fail offer) makes Pixel Flow $108M+ in 2026. The fail offer alone is ~33% of its IAP ([PocketGamer.biz](https://www.pocketgamer.biz/one-genre-three-strategies-how-magic-sort-knit-out-and-pixel-flow-are-redefining-sort-puzzle-monetisation/)).
- Leaf blowing is a **proven fantasy**: idle games like Leaf Blower Revolution (100k+ Steam players), sims like Leaf Blower Co., ASMR cleaning apps, and viral satisfying videos. **It has never been made into a colour-sort puzzle.**

**Why not other segments**
- Merge-2 is growing fastest (+74%, $1.3B in H1 2026) ([AppMagic via Mellow](https://gamedevreports.substack.com/p/appmagic-mobile-casual-games-in-h1)), but it needs a big content/art team. Not solo-friendly.
- Sort, sand, arrow, thread, bead, magnet, vacuum, dig, domino and colour-mix puzzles are all already cloned (see `GAME_FINAL_IDEA.md`).

**Clone check (13 searches in total):**
- Leaf-blower games exist only as idle/sim/ASMR/arcade: [Leaf Blower Revolution](https://play.google.com/store/apps/details?id=com.ezplugins.leafblowerrevolution&hl=en_US), [Leaf Blower 3D](https://play.google.com/store/apps/details?id=com.KawakGames.LeafBlower3D&hl=en_US), [Clean It Up Alone](https://play.google.com/store/apps/details?id=com.GilviusGames.CleanItUpAloneLeafBlower), [Leaf Collector](https://play.google.com/store/apps/details?id=com.supteagames.LeafCleaner), [I Am Cleaner Simulator](https://play.google.com/store/apps/details?id=com.qlg.leaf&hl=en_US).
- Raking puzzles are only game-jam titles ([Rake It](https://thoof.itch.io/rake-it), [Leafvember](https://miscbill.itch.io/leafvember)).
- **No colour-sort leaf puzzle with a tray found.**
- ⚠️ I couldn't search the stores directly. **Do a 15-minute check** on Google Play + App Store for: `leaf sort`, `leaf blower puzzle`, `leaf jam`, `blow sort`, `wind sort`, `gust puzzle`, `leaves color sort`, `autumn sort`.

---

## 2. Core game design

### Rules (the whole game in 6 lines)
1. A garden is covered in **layers of coloured leaves** (5–8 colours). A picture is hidden underneath.
2. A **queue of coloured blowers** waits at the bottom. The next 3 are visible.
3. **Tap a blower**, then **tap one of the 5 edge slots** (left/right/top/bottom). The blower sits there and **gusts toward the centre**.
4. A gust moves **only uncovered leaves of its colour**. They swirl into the blower's **bag (capacity 10/20/30)**. **Full bag → the blower leaves → the slot is free.**
5. A blower with no reachable leaves of its colour **waits in its slot**. **5 slots full and stuck → FAIL.**
6. **All leaves gone → the picture is revealed** (garden mosaic, flower bed, patio art). Level complete.

**Why it's more than Pixel Flow with leaves:** you **choose the side** you blow from. Rocks, fences and hedges block wind from certain directions, so **position matters as well as order.**

### Obstacles (introduce one every ~8–10 levels)
| Level | Element | Effect |
|---|---|---|
| 1–7 | Basic leaves, 3–4 colours, 2 layers | Tutorial, no fail possible before level 5 |
| 8 | **Rock** | Blocks wind from one side |
| 15 | **Wet leaves** | Need 2 gusts |
| 22 | **Hedge wall** | Splits the garden; pick sides wisely |
| 30 | **Leaf pile (3 layers)** | Deep stacks |
| 40 | **Puddle** | Traps leaves until a gust from the right side |
| 50 | **Windy weather** | A global breeze drifts leaves every few seconds |
| 60+ | Combinations | Hard and super-hard levels every ~5 levels |

### Difficulty curve (drives monetization)
- **Levels 1–6:** easy wins, fast "aha".
- **Level 7:** the first *designed* near-fail. Show the fail offer with a **free "+1 slot"** (teaches the value).
- From then on, a **"Hard"** level every 5 and a **"Super Hard"** every 10. These are where fail offers convert.
- **Level count for the prototype:** 20 (hand-made). **Soft launch:** 150+ (generator + solver).

---

## 3. Meta, economy and monetization

**Meta:** earn coins → **restore a park** area by area (bench, fountain, flower beds). Each area is a season: Autumn Park → Winter Garden (snow blower) → Spring Blossoms → Summer Party (confetti).

**Currency:** coins (soft). No hard currency needed at first.

| Item | Price |
|---|---|
| +1 slot (in-level) | 900 coins **or** rewarded ad |
| Super Gust (blows every colour once) | 1,200 coins |
| Undo | rewarded ad |
| Continue after fail (+2 slots) | 900 coins → 1,900 → then **fail offer IAP** |

**IAP catalogue**
- **Fail offer:** €2.99 (coins + 2 boosters), escalating to €5.99 on Hard levels.
- **Starter pack:** €1.99 (coins + boosters + 24h no-ads), shown once after level 12.
- **Remove ads:** €4.99 (interstitials only; keep rewarded).
- **Coin packs:** €1.99 / €4.99 / €9.99 / €19.99.
- **Later:** a season pass at €4.99/month once LiveOps runs.

**Ads**
- **Rewarded:** +1 slot, undo, double coins at level end, daily spin.
- **Interstitials:** from level 10, max 1 per 2 levels, never after a fail offer.
- **Banner:** none (they hurt retention in puzzle games).

**Rough targets:**
- ARPDAU $0.15+ (hybrid benchmark $0.15–0.50) ([Playio](https://blog.playio.co/arpdau-benchmarks-mobile-games)).
- Ads/IAP ≈ 50/50.

---

## 4. Tech architecture (Unity 6, C#)

| System | Implementation |
|---|---|
| **Leaves** | Struct arrays (position, velocity, colour, layer, state) for 300–1,500 leaves. **GPU-instanced** sprites (`Graphics.RenderMeshInstanced`). **No rigid bodies** |
| **Covering / "free" test** | Spatial hash grid. A leaf is free if no leaf with a higher layer overlaps it. Recompute only around moved leaves |
| **Wind** | Per blower: a directional force cone from its edge slot. Only affects free leaves of its colour. Leaves follow a curl-noise swirl toward the bag point, then get absorbed |
| **Obstacles** | Grid mask. Wind raycasts in cells; rocks/hedges block cells; puddles pin leaves |
| **Blowers / slots / queue** | State machine (Queued → Moving → Blowing → Waiting → Leaving). Level data defines queue order and bag sizes |
| **Level format** | JSON or ScriptableObject: grid size, leaves (colour, layer, pos), obstacles, blower queue, reveal image |
| **Level generator + solver** | Generate a random layered leaf layout → derive the queue from the colour counts → simulate greedy and best-first solvers → keep levels where the solver wins only with ≤N slots (difficulty = min slots needed + branching) |
| **Juice** | DOTween, leaf trails, a rustle ASMR pitch-shifted per gust, haptics on bag full, confetti on reveal |
| **SDKs** | AppLovin MAX, Unity IAP, GameAnalytics, Firebase Crashlytics + Remote Config (tune bag sizes, ad frequency, offer prices) |
| **Performance target** | 60 fps with 1,000 leaves on a ~€150 Android phone |

**Analytics events** (needed for publishers):
- `level_start`, `level_complete`, `level_fail`
- `booster_used{type}`, `fail_offer_shown`, `fail_offer_bought`
- `rewarded_shown{placement}`, `iap_purchase{sku}`
- `tutorial_step{n}`, `session_start`

**Free assets:**
- Leaf sprites: draw them yourself (simple shapes, 6–8 bright colours).
- UI and particles: [Kenney](https://kenney.nl/assets).
- Wind, leaf and UI sounds: [Sonniss GDC](https://sonniss.com/gameaudiogdc), [Pixabay SFX](https://pixabay.com/sound-effects/), [Kenney Interface Sounds](https://kenney.nl/assets/interface-sounds).
- Props: [Quaternius](https://quaternius.com/), [Poly Pizza](https://poly.pizza/).
- Font: [Google Fonts](https://fonts.google.com/) (Fredoka or Baloo).

---

## 5. Build schedule (~4 weeks of evenings + weekends)

| Week | Goal | Done when |
|---|---|---|
| **0** | Store/name check; pick the name; set up Unity + Git | No close clone; repo runs |
| **1** | **Tech spike:** 1,000 instanced leaves, layers, colour-gated wind cone, bag absorption | Smooth on a cheap Android phone; one gust *feels* satisfying |
| **2** | Queue + 5 edge slots + side choice, fail/win, picture reveal, 10 levels, basic UI | A full level loop is playable end-to-end |
| **3** | 20 levels, rock + wet-leaf obstacles, +1 slot (rewarded), fail-offer popup (mock IAP), GameAnalytics events, ASMR audio, haptics | Friends play 20 levels without explanation |
| **4** | Polish the first 60 seconds; **3 ad videos**; Android build; web build for CrazyGames; pitch one-pager | Pitch package ready |

**Test rule:** watch **5 people** play the first 3 minutes without helping them. If they don't understand side-choice by level 3, simplify it.

---

## 6. Ad creatives (the videos publishers test for CPI)
All vertical 9:16, 15–30 s, no logo intro, hook within the first second.
1. **"Satisfying clear":** a full-screen carpet of mixed leaves → one tap → an orange gust swirls away all orange leaves with ASMR rustle → part of a flower mosaic appears → quick cuts of 3 more gusts → full reveal.
2. **"Fail tease":** 4 of 5 slots full, one tap left, the wrong blower chosen → "Can you do better?" (low-IQ-bait style; these usually drive the lowest CPI).
3. **"Seasons":** autumn → snow blower → cherry blossoms, each with a big satisfying clear (shows LiveOps breadth).

---

## 7. Pitching publishers

**Pitch package**
1. Gameplay video (30 s) + the 3 ad creatives.
2. Android APK/AAB with 20 levels + GameAnalytics.
3. A one-pager:
   - hook
   - core loop in 3 bullets
   - differentiator (wind direction + layers)
   - monetization (fail offer + boosters + rewarded)
   - LiveOps seasons
   - market evidence (Pixel Flow/Colony Flow structure; the leaf-blower fantasy proven in idle/sim/ASMR; the physics trend: Marble Sort, Sand Loop)

**Where to submit (pitch 3–5 at once and check exclusivity first):**
| Publisher | Why | Where |
|---|---|---|
| **Voodoo** | Physics/ASMR puzzle hits (Sand Loop, Marble Sort); starts from a video | [voodoo.io/publishing](https://voodoo.io/publishing) |
| **Homa** | Submission platform with a creatives test; ran a jam with a 50% revenue share | [Homa Lab submissions](https://www.homagames.com/homa-lab/submissions-and-creatives) |
| **SayGames** | Wants D1 35%+ with a clear meta | [say.games/publishing](https://say.games/publishing/) |
| **Kwalee** | Self-serve submission | [kwalee.com/publishing](https://www.kwalee.com/publishing) |
| **Rollic** (Color Block Jam) | Puzzle leader | Search "Rollic publishing submit" |
| **CrazyLabs** | CLIK testing dashboard; challenges offered 55% of net revenue | Search "CrazyLabs CLIK submit" |
| Azur, Supersonic | Prototype-stage publishers | Search "<name> publishing submit game" |

**What they test:** a CPI/CTR marketability test on your video (target CPI ≤$0.40–0.50 on US Android), then retention (D1 ≥35–40%, D7 ≥10%) and playtime.

**Terms to check before signing:**
- **Revenue share:** ~50% of net profit is common; higher is possible (55% in CrazyLabs challenges); bonus models net closer to 70/30 ([LinkedIn/Jon Hook](https://www.linkedin.com/pulse/hypercasual-games-publishing-fundamentals-business-model-jon-hook)).
- Recoup rules (what costs they deduct).
- **IP ownership**, and exit/termination if they stop scaling the game.
- Exclusivity during the test.
- Payment timing.

---

## 8. Decision gates

| Gate | Pass | Else |
|---|---|---|
| Store check (week 0) | No near-identical game with >100k downloads | Switch theme (snow/confetti) or concept |
| Playtest (week 3) | 4 of 5 testers understand it by level 3 and want "one more" | Simplify side-choice; improve the gust feel |
| Publisher CPI test | CPI ≤$0.40–0.50 | Test new creatives once; if still high, move on |
| Retention test | D1 ≥35%, D7 ≥10% | Fix onboarding and the difficulty curve; 1–2 iterations max |
| Soft launch | ARPDAU ≥$0.15, ROAS on track | Publisher decides scale; otherwise reuse the engine for the next idea |

---

## 9. Money (see `GAME_PUBLISHER_PLAN.md` for the full maths)
- **Your costs:** ~€150–600 (Google Play $25, optional Apple $99, assets, optional €150–300 own CPI test).
- **With a publisher at ~50% profit share:**
  - **€1.5k a month for you** needs ~€3k game profit ≈ **6,300 installs a month**, ~€3.8k of *their* ad spend.
  - **€2k a month:** ~8,300 installs, ~€5k spend.
- **Don't buy ads yourself** unless D1 ≥40%, D7 ≥12%, ARPDAU ≥$0.15 and CPI ≤$0.60.

## 10. Risks
- **Clones if it works:** speed and publisher backing are the defence.
- **"Pixel Flow re-skin" perception:** show side-choice and layered physics clearly in the video.
- **Performance with many leaves:** use the custom instanced system, not physics bodies.
- **Most prototypes fail publisher tests.** The wind/leaf engine is reusable for snow, confetti or sand variants, so a fail isn't a total loss.
