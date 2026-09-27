# Mobile game plan for a solo dev with a full-time job (Sep 2026)

## 1. What's working right now (the data)

- **Hybrid-casual** (simple core + progression/IAP layer) is the **clearest growth story: +23% to $2.4B in H1 2026**. Mid-core fell 7% ([Singular](https://www.singular.net/blog/top-mobile-games/), [AppMagic H1 2026](https://appmagic.rocks/research/casual-report-H12026/?hl=en)).
- **Puzzle is booming:** $8.1B, about +20%. Merge games are the fastest-growing big genre (+74%, $1.3B).
- **The hottest puzzle sub-genres are sort, screw, block and arrow:**
  - Sort and screw puzzles doubled their IAP revenue since 2024.
  - Block puzzles grew about 10×.
  - **Arrow-escape** games ("Arrows Puzzle Escape") were **#1 in download growth in May 2026** ([Naavik](https://naavik.co/digest/how-niche-subgenres-are-reshaping-the-mobile-puzzle-market/), [Sensor Tower May 2026](https://sensortower.com/blog/top-10-worldwide-mobile-games-by-revenue-and-downloads-in-may-2026), [NextBigGames radar](https://nextbiggames.com/2026/03/26/hybridcasual-puzzle-market-radar-33-trends/)).
- **Twists that win:** a 2D mechanic moved to **3D** (Screwdom), **combining two proven mechanics**, and **fail offers** ("continue for X coins"), which are a major revenue lever ([AppMagic fail offers](https://appmagic.rocks/blog/fail-offers)).
- **Paid ads are getting expensive:**
  - Blended game CPI (cost per install) is **$0.56, up 30% in a year**. North America is **$1.68** ([publisher data](https://vectraplay.com/blog/what-voodoo-looks-for-prototype)).
  - TikTok organic reach dropped from about 15–20% to about **4–8%** in 2026 ([CloutBoost](https://www.cloutboost.com/blog/tiktoks-changing-landscape-for-game-marketing-in-2026-what-developers-need-to-know)).
  - A solo dev **can't outspend** studios, so use **publishers' money** and **organic clips boosted with small paid amounts**.

**Conclusion:** build a **hybrid-casual puzzle game** in a trending sub-genre, with **one clear twist**. It's the best fit for your skills, your time, and your budget.

---

## 2. Which game to build

### Recommended concept: "arrow escape + sort queue", e.g. working title **"Fish Out!"**
- **Core (arrow escape, the fastest-growing mechanic):** a pond full of fish, each pointing in one direction. Tap a fish and it swims out in that direction. If another fish blocks it, it bumps back.
- **Twist (sort/jam queue, a proven hit mechanic):** escaped fish go into a **7-slot bucket**. Three of the same colour clear. If the bucket is full, you fail. This gives you planning depth and a natural **fail offer** ("+1 slot for 900 coins or a rewarded ad").
- **Meta (hybrid layer, IAP):** coins build and decorate an **aquarium**. Boosters include undo, shuffle and an extra slot.
- **Why it's clip-friendly:** satisfying chain clears, a "can you solve this?" still frame, and cute fish all make good short videos.

⚠️ **Before building, spend 1 evening checking for clones:** search Google Play/App Store for "arrow fish", "fish escape puzzle", "tap away fish", and check AppMagic/Sensor Tower free pages. If a near-identical game is already big, **swap the theme or twist** and keep the formula. Alternatives to test:
- **B:** screw puzzle in **3D** with a unique theme (the Screwdom direction)
- **C:** block-jam + merge hybrid (merge is the fastest-growing big genre)
- **D:** colour-sort with physics (liquids or sand)

### What "good" looks like (publisher benchmarks)
- **D1 retention ≥35–40%** (SayGames wants 35%+ with a clear meta), **D7 ≥10–15%**, ≥10 minutes of play on day 0.
- **CPI < $0.40–0.50** on Android in test countries.
- Voodoo and Azur look at prototypes with strong D1. Tilting Point needs D7 ≥20% and D30 ≥8% ([VectraPlay](https://vectraplay.com/blog/what-voodoo-looks-for-prototype)).
- **The reality check:** Voodoo once tested about **1,500 prototypes a year for about 4 launches**. **Plan for several fast prototypes, not one perfect game.**

---

## 3. Tech stack (almost free)
| What | Choice | Cost |
|---|---|---|
| Engine | **Unity** (publisher SDKs are Unity-first; Personal is free under $200k revenue) | €0 |
| Art | Kenney.nl (free), Unity Asset Store packs, simple flat/3D low-poly | €0–150 |
| Sound | freesound.org, Sonniss GDC bundles (free) | €0–30 |
| Ads | **AppLovin MAX** or AdMob (interstitial after level, rewarded for boosters) | €0 |
| IAP | Unity IAP (remove ads €4.99, coin packs, starter pack) | €0 |
| Analytics | **GameAnalytics** + Firebase (retention, funnels, level fail rates) | €0 |
| Store accounts | Google Play $25 once; Apple $99/year | ~€115 |
| iOS builds | Needs a Mac, or **Unity Build Automation / Codemagic** free tier. **Start Android-only** to save money | €0 |

---

## 4. Budget

| Tier | Amount | What it covers |
|---|---|---|
| **Minimum** | **~€150–300** | Google Play + a few assets. Publisher route only (they pay for ads) |
| **Recommended** | **~€800–1,200** | Minimum + Apple account + **€300–500 CPI/retention test** (TikTok/Meta ads, Android, tier-2/3 countries) + **€200–300 boosting organic clips that already work** |
| Scale | Only if **LTV > CPI** | Never scale paid ads before the numbers work |

**Time:** about 8–10 hours a week alongside your job. First prototype in about 4–5 weeks.

---

## 5. 12-week plan

| Week | Do |
|---|---|
| 1 | Research (store trending charts, AppMagic/Sensor Tower free), clone check, paper-prototype 20 levels |
| 2–5 | Unity core loop + 30–40 levels, fail state, rewarded-ad booster, GameAnalytics. **Record clips from week 3** |
| 6 | **Submit to publishers** (see §6). Release a **web build on CrazyGames** (developer portal) for free player data. Post clips daily |
| 7–8 | Iterate on data: level difficulty curve (fail-rate spikes), onboarding (first 60 seconds), D1 |
| 9–10 | Add meta (aquarium, coins), fail offers, IAP. **Soft launch on Google Play** in test countries (e.g., PH, BR, IN, TR) with a €300 CPI + retention test |
| 11–12 | **Decide:** publisher deal → hand over UA. Good own numbers → slowly scale ads + ASO. Weak → **kill it and start prototype #2** with what you learned |

---

## 6. Marketing plan (fits a small budget)

1. **Publishers as your marketing budget.** Pitch a playable prototype + 30–60 second gameplay video to **Voodoo, Homa, SayGames, Azur Games, Kwalee, CrazyLabs, Supersonic (Unity)**. They run CPI tests **with their money**, and if the game works they fund user acquisition for a revenue share ([publisher overview](https://vectraplay.com/blog/what-voodoo-looks-for-prototype), [a studio's Voodoo/Homa story](https://nextbiggames.com/2026/05/09/minigamelab-hybrid-casual-studio-podcast/)). Search "<publisher> publishing submit game" to find each submission form.
2. **Short-form clips (TikTok, YouTube Shorts, Reels).** Puzzle games are ideal for "challenge" content:
   - *"Only 2% solve level 48 — can you?"* (the comments are the algorithm fuel)
   - satisfying chain-clear clips, "I made this game alone after work — day 30"
   - Post **1–2 a day**. TikTok organic reach is weaker in 2026 ([CloutBoost](https://www.cloutboost.com/blog/tiktoks-changing-landscape-for-game-marketing-in-2026-what-developers-need-to-know)), so **boost only the clips that already perform** with €5–20 a day (Spark Ads). Raw gameplay beats polished trailers ([presskit.gg](https://presskit.gg/field-guides/tiktok-indie-game-marketing)).
3. **ASO (free, compounding):**
   - keywords in the title and short description ("arrow puzzle", "escape", "sort")
   - a clear icon, and screenshots showing the core mechanic
   - **Google Play Store Listing Experiments** to A/B test icons for free
4. **Web portals:** CrazyGames (and Poki if accepted) give free players, data and a small revenue share. It's a cheap test before mobile.
5. **Communities:** r/AndroidGaming, r/iosgaming, r/puzzles, r/incremental_games (if it fits), your own Discord for testers.
6. **Later:** cross-promote between your own games once you have 2–3 titles.

---

## 7. Honest expectations
- Most mobile games earn **nothing**. The winning approach is **fast prototypes + strict kill rules** (3–5 prototypes in 6 months).
- A realistic first-game outcome is **€0–500 a month**. A publisher deal or a game with D1 ≥40% is where real money starts.
- Your advantage is **speed and cheap iteration** on proven formulas, not originality or budget.

*Data from web research, Sep 2026. Check chart positions, publisher terms and CPIs before committing.*
