# Final game idea: "LEAF BLOW" (working title), a leaf-blower colour-sort puzzle

**Status:** validated as far as web research allows (Sep 2026). **No direct clone found.** Details in §2.

---

## 1. How I got here (ideas checked and rejected)

I checked ~15 hybrid-casual mechanics. **Every one except this one already had a colour-sort puzzle version:**

| Concept | Verdict | Existing games |
|---|---|---|
| Arrow escape + tray (Fish/Balloon Jam) | ❌ taken | [Arrow Unjam](https://arrowunjam.com/), [Arrow Jam!](https://apps.apple.com/us/app/arrow-jam-tap-puzzle/id6762192889), [Color Arrow Jam](https://play.google.com/store/apps/details?id=puzzle.arrow.jam.escape.gp&hl=en), fish escape games |
| Dig + sand + gem tray (Dig Jam) | ❌ taken | [Dig Gem Match](https://play.google.com/store/apps/details?id=com.hw.dig.gem.match), [SandFall](https://play.google.com/store/apps/details?id=com.brainamics.sandfall), [Sand Tap!](https://play.google.com/store/apps/details?id=puzzle.sand.tap.sort), [Sand Flow! Collect](https://apps.apple.com/us/app/sand-flow-collect/id6758326067) |
| Thread/embroidery sort | ❌ taken | [Tiny Stitches](https://play.google.com/store/apps/details?id=games.taplab.tinystitches&hl=en), [Thread Sort](https://www.playagame.io/puzzles/thread-sort/), [Wool Art](https://moondropgames.com/game/wool-art-sort-puzzle-3d) |
| Bead / gem pixel sort | ❌ taken | [Pixel Beads](https://play.google.com/store/apps/details?id=com.kiwifun.game.android.pixel.beads), [Gem Sort](https://play.google.com/store/apps/details?id=com.kb.gemsort&hl=en_US) |
| Magnet sort | ❌ taken | [Magnet Sort](https://www.taptap.io/app/33563910), [Magnet Ball Sort](https://play.google.com/store/apps/details?id=com.eightgreatgames.magnetsort&hl=en_US) |
| Vacuum sort | ❌ taken | [Car Sand Vacuum](https://play.google.com/store/apps/details?id=com.comgames.carsandvacuum), [Vacuum Jam](https://apkcombo.com/vacuum-jam-color-sort/vacuum.jam.color.sort), [Candy Vacuum Frenzy](https://apps.apple.com/us/app/-/id6757122393) |
| Luggage / sushi conveyor sort | ❌ taken | 4–5+ each |
| Colour mixing sort | ❌ taken | [Color Spark](https://apps.apple.com/app/id6478590498), [Color Merge](https://play.google.com/store/apps/details?id=com.lvii.colormergegame&hl=en_US) |
| Domino colour chains | ❌ taken | [DominoChains](https://apps.apple.com/us/app/dominochains/id6683305349), [Domino Merge](https://poki.com/en/g/domino-merge) |
| Cannon smash (Smash Fest) | ❌ 38 clones | [Gamigion](https://www.gamigion.com/smash-fest-38-clones-5m-revenue-old-mechanic-new-drama/) |
| Ants eat colour tiles (Colony Flow) | ❌ exists (was top-charting, then pulled over the "Flow" name) | [Gamigion](https://www.gamigion.com/2-top-chart-puzzle-games-are-just-removed/) |
| **Leaf blower + colour sort + tray** | ✅ **no direct match found** | See §2 |

---

## 2. Clone check for "Leaf Blow"

**10 targeted searches:**
- "leaf sort" puzzle, "blow" colour-sort with leaves/bags/blowers
- leaf-blower puzzle apps on Google Play, autumn-leaves cleanup/reveal puzzles
- "Blower Jam" / "Leaf Jam" / "Gust Sort" / "Wind Sort"
- snow-blower sort, fan/wind physics sort

**What exists: the leaf-blower theme, but NOT as a colour-sort puzzle:**
- [Leaf Blower Revolution](https://play.google.com/store/apps/details?id=com.ezplugins.leafblowerrevolution&hl=en_US): idle/incremental (100k+ players on Steam) ([info](https://revolutionidlegame.com/games/leaf-blower-revolution-idle-game/)).
- [Leaf Blower 3D](https://play.google.com/store/apps/details?id=com.KawakGames.LeafBlower3D&hl=en_US): idle collect and upgrade. [Leaf Blower (KGS)](https://play.google.com/store/apps/details?id=com.kgs.leafblower&hl=en_US): gate runner.
- [Clean It Up Alone: Leaf Blower](https://play.google.com/store/apps/details?id=com.GilviusGames.CleanItUpAloneLeafBlower): ASMR cleaning sim. [Leaf Collector](https://play.google.com/store/apps/details?id=com.supteagames.LeafCleaner): move-and-vacuum arcade that reveals pictures.
- [Leaf Blower Co.](https://store.steampowered.com/app/3571710/Leaf_Blower_Co/) (Steam, cozy work sim), [Leafee](https://dudem.itch.io/leafee) (a 2022 game-jam puzzle).
- [Feed Me Oil](https://en.wikipedia.org/wiki/Feed_Me_Oil): an old physics puzzle that uses fans.

**Not found anywhere:** colour-coded blowers + matching leaf bags + a limited slot tray/fail state + a picture reveal, i.e., the hybrid-casual puzzle structure.

⚠️ **Limit:** the Google Play and App Store search pages were blocked for me, so I checked through web search only. **Before coding, spend 15 minutes on both stores** searching: `leaf sort`, `leaf blower puzzle`, `leaf jam`, `blow sort`, `wind sort`, `gust puzzle`, `leaves color sort`, `autumn sort`. If a near-identical game has more than 100k downloads, stop and message me.

---

## 3. Why this is a strong bet

1. **Proven fantasy.** Leaf blowing already works as a *fantasy*: idle games with large audiences, Steam sims, ASMR cleaning apps, and satisfying leaf-blowing videos on TikTok. **It just has never been made into the money-making puzzle format.**
2. **A proven money structure.** The **reveal-by-colour + limited slots + fail offer** structure is the most profitable in the genre:
   - Pixel Flow: $108M+ in 2026; its $5.99 fail offer is ~33% of IAP ([PocketGamer.biz](https://www.pocketgamer.biz/one-genre-three-strategies-how-magic-sort-knit-out-and-pixel-flow-are-redefining-sort-puzzle-monetisation/), [Gamigion](https://www.gamigion.com/top-grossing-hybridcasual-games-released-in-2026/)).
   - Colony Flow, the same structure with a *new verb* (ants eating), reached the top charts.
3. **2026 trend: physics and ASMR.** Marble Sort (~$5M/month) and Sand Loop ($15M) are Voodoo's hits ([AppMagic](https://appmagic.rocks/blog/voodoo-new-big-three/?hl=en)). Leaves swirling in wind is exactly that kind of satisfying physics.
4. **Built-in LiveOps variety that publishers love:** autumn leaves → **winter snow-blower** → spring cherry blossoms → party confetti → desert sand. Same engine, new seasonal events.
5. **A 3-second ad hook:** a thick carpet of mixed-colour leaves, one gust, a whole colour swirls away and part of the garden art appears. Great for low install costs and for TikTok.

---

## 4. Game design (MVP)

**Core loop (10-second readable):**
1. A garden is covered in **hundreds of coloured leaves in layers**. Underneath is a picture: a lawn mosaic, flower bed art, or a patio.
2. **Coloured leaf blowers** wait in a **queue** at the bottom. Each one has a **bag with a capacity** (e.g., 20 leaves).
3. **Tap a blower** → it moves into one of **5 slots on the garden edge**. **You choose which edge** (left/right/top/bottom): wind direction matters. This is the key difference from Pixel Flow, whose shooters only follow the conveyor.
4. Its gust lifts **only leaves of its colour** that are **not covered** by other leaves or obstacles. They swirl into its bag with physics. **A full bag means the blower leaves and frees the slot.**
5. Blowers whose leaves are still buried **stay in their slots**. **All 5 slots blocked means FAIL**, which triggers the fail offer (+1 slot / "Super Gust" / continue).
6. When every leaf is gone, the **picture is revealed**. Level complete.

**Obstacles for depth (introduce one every ~10 levels):**
- Wet leaves (need 2 gusts).
- Rocks and fences that block wind from one side.
- Leaf piles in 3 layers.
- Puddles that trap leaves.
- Hedges you must blow around.
- Gusty-weather levels where wind changes direction.

**Meta and monetization:**
- **Garden restoration:** coins rebuild and decorate your park; each area is a season.
- **Rewarded ads:** extra slot, Super Gust (blows all colours once), undo.
- **Interstitials** only after level ~10, between levels.
- **IAP:** remove ads (€4.99), coin packs, **fail offer (€2.99–5.99)**, starter pack, later a season pass.

**Content goal for the prototype:** 20 hand-made levels. Later, a **level generator + automatic solver** to produce hundreds of levels. That's your CS edge.

---

## 5. Tech plan (Unity 6)

| Part | How |
|---|---|
| Leaves | 300–1,500 **GPU-instanced sprites** with a **custom lightweight physics** (a grid-based wind field + simple velocity/damping, *not* rigid bodies). This runs on low-end Android |
| Layers / covering | Each leaf has a layer index. A leaf is "free" if nothing above it overlaps (spatial hash grid) |
| Wind | Per-blower directional force cone. Only affects same-colour free leaves; the gust pulls them toward the bag spline |
| Blowers / slots / queue | Simple state machine. Queue data per level in JSON/ScriptableObject |
| Picture reveal | A render texture under the leaves, or just the art revealed as leaves leave |
| Juice | DOTween, particle trails, leaf-rustle ASMR sounds (Kenney/Sonniss/Pixabay), haptics |
| SDKs | AppLovin MAX (ads), Unity IAP, GameAnalytics, Firebase Remote Config |
| Free assets | [Kenney](https://kenney.nl/assets) (UI, particles), [Kenney Interface Sounds](https://kenney.nl/assets/interface-sounds), [Sonniss GDC](https://sonniss.com/gameaudiogdc) (wind/leaf SFX), [Pixabay SFX](https://pixabay.com/sound-effects/), [Poly Pizza](https://poly.pizza/) / [Quaternius](https://quaternius.com/) (garden props), [Google Fonts](https://fonts.google.com/). Draw the leaf sprites yourself (simple shapes, 6–8 colours) |

---

## 6. Three-week prototype plan (evenings + weekends)

| Week | Build |
|---|---|
| **0 (1 evening)** | 15-minute store check (terms in §2). Pick a name (avoid "Flow" and existing names; check the stores and EUIPO/USPTO quickly) |
| **1** | Leaf rendering + wind physics spike (1,000 leaves at 60 fps on a cheap Android phone). Colour-gated gusts. Bag capacity |
| **2** | Queue → 5 edge slots, side selection, layers/covering, fail state, win + picture reveal. 10 levels |
| **3** | 20 levels, 2 obstacles, rewarded "+1 slot", fail offer popup (mock IAP), GameAnalytics events (level start/fail/complete), ASMR audio. **Record 3 vertical ad videos (15–30 s)** |
| **4** | Pitch 3–5 publishers at once (check exclusivity): **Voodoo** (physics/ASMR: Sand Loop, Marble Sort), **Rollic**, **SayGames**, **Homa**, **CrazyLabs**, **Azur**, **Supersonic**. Put the web build on **CrazyGames** for free player data |

**Pitch one-pager:**
- The hook: *"Leaf blowing is a proven fantasy (idle, sim and ASMR games; viral videos) that has never had a hybrid-casual puzzle version."*
- The structure: reveal + slots + fail offer.
- The differentiator: aiming the wind direction.
- The LiveOps plan: seasons.
- 20–30 second video + Android build.

---

## 7. Money: what it takes (from `GAME_PUBLISHER_PLAN.md`)

- **Publisher targets:** D1 ≥35–40%, D7 ≥10%, CPI ≤$0.40–0.50.
- **With a publisher at ~50% profit share:** for **€1.5k a month** the game needs **~€3k profit**, i.e. ~6,300 installs a month and ~€3.8k of *their* ad spend. For **€2k**: ~8,300 installs, ~€5k spend.
- **Your costs:** **~€150–600** (Google Play $25, assets, optional €150–300 own CPI test).
- **Don't buy ads yourself** unless: D1 ≥40%, D7 ≥12%, ARPDAU ≥$0.15 and CPI ≤$0.60. At those numbers, €1.5k a month means ~€1.9k/month in ad spend and €4–6k of working capital.

---

## 8. Honest risks
1. **Clones are guaranteed if it works.** "No clones yet" only buys you a head start, typically weeks to a few months. **Speed plus publisher backing is the defence.**
2. **Publishers may see it as "Pixel Flow with leaves".** The **edge aiming, wind physics and layered leaves** must make it play differently. Show that in the video.
3. **Performance:** thousands of leaves on low-end phones need the custom lightweight physics (above), not Unity rigid bodies.
4. **Store search limits:** I couldn't query the stores directly. Do the 15-minute check.
5. **No game is guaranteed:** most prototypes fail publisher tests. If Leaf Blow fails, re-use the engine with the same wind tech for a **snow** or **confetti** variant, or move to the next concept.
