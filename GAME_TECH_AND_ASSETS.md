# Game: tech stack, Godot vs Unity, free assets, clone check (Sep 2026)

## 1. Does "Fish Out!" already exist? **Partly, yes.** Treat it as crowded and differentiate or switch.

| Game | What it is | Overlap |
|---|---|---|
| [Fish Escape – Brain Puzzle](https://play.google.com/store/apps/details?id=gg.dolly.fishescape&hl=en_US) | Tap fish to move them out in the right order and clear the tank, with hooks, predators and currents | **High:** same core (fish arrow-escape) |
| [Fish Simulator Fish Puzzle Game](https://play.google.com/store/apps/details?id=com.emve.fishing.net.rescue.fish.jam.puzzle.game.fishinggames&hl=en_US) | Solve puzzles to get all the fish out of a jam | **High** |
| [Fish Escape – Puzzle Challenge](https://play.google.com/store/apps/details?id=com.fish.escape.sdma.puzzle.challenge&hl=en_US) | Fish escape puzzle | Medium |
| [Fish Sort Puzzle](https://play.google.com/store/apps/details?id=triple.sorting.bubble.fish.match&hl=en_US) | 3D aquarium match-3 sort (since Mar 2026) | Medium (sort + aquarium) |
| [Fish Out](https://apkcombo.com/fish-out/com.Code_V.ProjectFish) | Pipe-rotation fish puzzle | **The name is taken** |

The **exact combination** (arrow-escape + 7-slot colour bucket + aquarium meta) didn't show up in the search. But the theme and core are already used, so **"Fish Out!" as planned is not a fresh idea.**

### Other themes checked: also crowded
- **Airport luggage sort:** 4+ games ([Luggage Sort](https://play.google.com/store/apps/details?id=com.aintdevs.luggagesort), [Airport Sort](https://play.google.com/store/apps/details?id=com.luggage.sort.grill.goods&hl=en-US), [Bag Rush](https://play.google.com/store/apps/details?id=com.felicity.baggagerush), [Baggage Sort](https://play.google.com/store/apps/details?id=com.airport.lost.but.found.games&hl=en_US)). **Skip.**
- **Sushi conveyor sort:** 5+ games, including Tripledot's [Sushi Flow](https://play.google.com/store/apps/details?id=com.tripledot.sushi.conveyor&hl=en_CA). **Skip.**
- **Plain arrow tap-away:** many ([Arrow Out](https://play.google.com/store/apps/details?id=arrow.out.maze.escape.puzzle.game.arrowsout&hl=en_US), [Arrow Escape Puzzle](https://play.google.com/store/apps/details?id=com.lioncube.arrow.escape.puzzle&hl=en_IN), [on CrazyGames](https://www.crazygames.com/game/arrow-exit-puzzle)). **Only viable with a real twist.**

### Alternatives (ranked)
1. **"Balloon Jam": arrow-escape + passenger colour sort (Bus Jam style).** *Recommended.*
   - Hot-air balloons are tethered on a grid, each pointing in a direction. Tap a balloon and it flies off if its path is clear.
   - Coloured passengers queue at the bottom. A balloon can only take off full with **its colour**, so you have to plan which balloon to free first.
   - Meta: collect balloons and decorate sky islands.
   - The search found **no arrow-escape balloon puzzle**. Existing balloon games are arcade flyers ([Balloon Escape](https://play.google.com/store/apps/details?id=com.TuktukGames.BalloonEscape&hl=en_US)).
   - It combines the **fastest-growing mechanic (arrow escape)** with the **proven Bus Jam queue**. Colourful skies make it good for clips.
2. **Fish, differentiated.** Keep the fish theme but make the **7-slot bucket and fail offers** the core (the existing fish games don't show it), add **3D water and physics** (the Screwdom lesson: 2D→3D wins), and pick a new name. Higher risk, because players and stores already associate the theme with other games.
3. **Arrow-escape + merge.** Escaped pieces land on a merge board, and merging unlocks the next level's pieces. Merge is the fastest-growing big genre (+74%). The design is more complex, so try it only for prototype #2.

**Before building (1 evening):**
- Search Google Play and the App Store for "balloon jam", "balloon escape puzzle", "balloon sort", "sky jam", "arrow balloon".
- Check the top results' downloads on AppMagic or Sensor Tower (free pages).
- If a near-identical game has **>1M downloads**, switch to alternative 2 or 3.

---

## 2. Tech stack: Unity or Godot?

### Short answer
- **Going the publisher route** (Voodoo, Homa, SayGames…)? **Use Unity.** Their prototype SDKs are **Unity packages**: Voodoo's **TinySauce** ([Voodoo](https://www.linkedin.com/pulse/voodoo-vision-how-we-work-developers-prototype-youssef-gasmi)) and the Homa SDK, which is configured through Unity Project Settings ([Homa docs](https://sdk.homagames.com/docs/legacy/homa-belly-settings/main.html)).
- **Self-publishing, ads-first, with a web build (CrazyGames) as your test?** **Godot works well.**

### Godot on mobile in 2026: what works and what doesn't
| Area | Status |
|---|---|
| Ads: AdMob | ✅ [Poing Studios AdMob plugin](https://github.com/poingstudios/godot-admob-plugin) (Godot 4.2+, Android + iOS, consent, mediation) |
| Ads: AppLovin MAX | ✅ [AppLovin MAX Godot plugin](https://github.com/AppLovin/AppLovin-MAX-Godot) + [official docs](https://support.axon.ai/en/max/godot/overview/integration) |
| In-app purchases | ⚠️ **Weak.** Old Play Billing plugin, poorly maintained iOS plugins, devs report downgrading Godot versions to make iOS IAP work ([Ziva](https://ziva.sh/blogs/godot-mobile), [forum](https://forum.godotengine.org/t/anyone-using-godot-iap-ios-android-in-app-purchases/143757)) |
| Publisher SDKs | ❌ Unity-first |
| Web export (CrazyGames/Poki) | ✅ Good with GDScript (C# web export isn't supported in Godot 4) |
| Overall | "Ready for premium and ads, not for live-service/IAP-heavy" ([Ziva](https://ziva.sh/blogs/godot-mobile)) |

Hybrid-casual earns much of its money from **IAP and fail offers**, so **Unity is the safer choice for this plan.** Use Godot only if you go **ads-only and web-first**.

### Recommended stack (Unity)
| Layer | Tool | Cost |
|---|---|---|
| Engine | **Unity 6** (Personal: free under $200k/yr revenue) + C# | €0 |
| Rendering | URP; **2D** for the balloon/fish concept, or simple 3D low-poly | €0 |
| Animation / juice | **DOTween** (free on the Unity Asset Store), particle system | €0 |
| UI / text | UI Toolkit or uGUI + TextMeshPro | €0 |
| Ads | **AppLovin MAX** (or Unity LevelPlay / AdMob) | €0 |
| IAP | **Unity IAP** (remove ads, coin packs, starter pack, fail offer) | €0 |
| Analytics | **GameAnalytics** (retention, level funnels) + **Firebase Crashlytics** | €0 |
| Remote tuning / A/B | Firebase Remote Config (difficulty, ad frequency) | €0 |
| Level design | Levels as JSON/ScriptableObjects + a simple in-editor level editor; a **level generator + solver** script (your CS advantage) | €0 |
| Source control / builds | Git + GitHub; Android builds locally; iOS via **Codemagic** or Unity Build Automation if you have no Mac | €0–free tier |
| Stores | Google Play ($25 once), Apple ($99/yr, later) | ~€115 |

### If you pick Godot anyway
- Godot 4.x + GDScript, with the Poing AdMob **or** AppLovin MAX plugin.
- Stay ads-only at first (rewarded + interstitial). Add IAP only after testing the plugins on real devices.
- Web export for CrazyGames. Log retention through the store dashboards, or a small backend (e.g., Supabase) for events.

---

## 3. Free assets (with links)

**Licence rule:**
- **CC0** means free for commercial use, no credit needed.
- **CC-BY** means free, but you must credit the author (e.g., in the settings screen).
- **Avoid "NC" (non-commercial)** licences in a monetised game.

### Art: 2D and 3D
| Asset | Licence | Use for |
|---|---|---|
| [Kenney: Fish Pack](https://kenney.nl/assets/fish-pack) (120 assets) | CC0 | Fish concept |
| [Kenney: all assets](https://kenney.nl/assets) (40k+, 2D/3D/UI/fonts/audio) | CC0 | Everything: UI, particles, icons |
| [Kenney: UI Pack](https://kenney.nl/assets/ui-pack) | CC0 | Buttons, panels, progress bars |
| [Kenney: Particle Pack](https://kenney.nl/assets/particle-pack) | CC0 | Clear/pop/confetti effects |
| [Quaternius: LowPoly Animated Fish](https://quaternius.itch.io/lowpoly-animated-fish) (rigged, swim animation, FBX/OBJ/Blend) | CC0 | 3D fish variant |
| [Quaternius: all packs](https://quaternius.com/) (animals, characters, nature, vehicles) | CC0 | 3D low-poly worlds, sky islands |
| [OpenGameArt: Animated Fish](https://opengameart.org/content/animated-fish) | Check per asset | 2D fish sprites |
| [OpenGameArt](https://opengameart.org/) | Mixed (filter CC0) | Sprites, music, SFX |
| [Poly Pizza](https://poly.pizza/) | CC0 / CC-BY | Low-poly 3D (search "hot air balloon", "cloud", "island") |
| [itch.io free game assets](https://itch.io/game-assets/free) | Check per pack | Themed 2D packs (balloons, skies) |
| [ambientCG](https://ambientcg.com/) / [Poly Haven](https://polyhaven.com/) | CC0 | Textures, HDRIs, water |
| [game-icons.net](https://game-icons.net/) | CC-BY 3.0 (credit) | Booster and shop icons |
| [Google Fonts](https://fonts.google.com/) | OFL (free commercial) | Rounded game fonts (e.g., Fredoka, Baloo) |

### Sound and music
| Asset | Licence | Use for |
|---|---|---|
| [Kenney: Interface Sounds](https://kenney.nl/assets/interface-sounds) and other Kenney audio packs | CC0 | Taps, pops, UI clicks |
| [Sonniss GDC Game Audio Bundles](https://sonniss.com/gameaudiogdc) | Royalty-free, commercial OK | Huge pro SFX library |
| [Pixabay Sound Effects](https://pixabay.com/sound-effects/) / [Pixabay Music](https://pixabay.com/music/) | Pixabay licence (commercial OK) | Whooshes, water, cheerful loops |
| [Freesound](https://freesound.org/) | Mixed; filter to **CC0** | Specific SFX |
| [Incompetech](https://incompetech.com/) | CC-BY (credit) | Background music |

### Free tools
- [Blender](https://www.blender.org/) for 3D, [Krita](https://krita.org/) for 2D painting, [Figma](https://www.figma.com/) for UI mockups, the icon, and store screenshots.

**Asset tips:**
- Stick to **one art style** (e.g., only Kenney flat 2D, or only Quaternius low-poly). Mixed styles look cheap.
- Re-colour assets to your own palette so the game looks unique.
- Keep a `CREDITS.md` listing every asset and its licence (needed for CC-BY, and helpful in publisher due diligence).
