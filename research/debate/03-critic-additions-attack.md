# 03 — Critic Attack on the New Global Candidates (#26-#35)

**Author:** CRITIC · **Date:** 2026-09-24
**Inputs:** `02-defender-additions.md`, the brief (inbound only, chance first, simple wrappers OK, global by default), and my earlier files (`01-critic-ammunition.md` for SAT/PLAT IDs, `02-critic-attack.md`).
**Scoring:** as in Round 2. Chance = P(€1k, then €10k MRR) for this founder. Scale = the ceiling. All ten ideas are global, so no geography cap applies.

## 0. Up front: the batch is the right *shape*, but most of it fails on data rights or on ownership
Credit where due: this batch answers my portfolio critique. It is global, English-first, content-native and cheap to build. Two structural problems recur, though:

1. **Scraping-based indexes have neither a moat nor a licence.** The defender itself notes that Apify sells scrapers for most of these ecosystems. I found one for **MakerWorld** too ([Apify](https://apify.com/stealth_mode/makerworld-models-details-scraper)), as well as for DramaBox/ReelShort and even for TrustMRR. Several sources explicitly forbid monitoring:
   - **MakerWorld's Terms of Use prohibit any "page-scrape, robot, spider… or any means of artificial intelligence service… to access, acquire, copy… or monitor any portion of the site"** ([MakerWorld ToU](https://makerworld.com/en/user-agreement)).
   - Etsy data requires approved Commercial Access under the API Terms, including caching limits ([Etsy API docs](https://developers.etsy.com/documentation/)).
   - TikTok and Instagram view data isn't legitimately available at scale.

   So an index that anyone can clone in days, and that the source can shut down with one letter, is fragile twice over.
2. **The "no reference tool" claims mostly didn't survive a 10-minute search.** 6 of the 10 already have a direct incumbent (details below).

The ideas that hold up best are the ones whose data comes **from users who connect their own accounts** (first-party, legal, unique) or from **the founder's own tests**, not from scraping someone else's platform.

---

## 1. Verdict table

| # | Idea | Verdict | Defender C/S | **Critic C/S** | Decisive issue |
|---|---|---|---|---|---|
| 26 | PrintRadar (3D-print demand radar) | **WOUNDED** | 5/5 | **3/4** | MakerWorld's terms forbid scraping. Hobbyist willingness to pay is low. |
| 27 | GigRate (AI-trainer pay index + referrals) | **KILL** | 5/5 | **1/3** | Pay indexes already exist (OpenTrain, aitrainer.work, AITraining.jobs, AlignList). Referral links are already mass-posted, and aggregator use is restricted. |
| 28 | DramaCharts (micro-drama title/trope charts) | **KILL** | 4/6 | **2/4** | SocialPeta already publishes weekly title rankings (43k titles) with trope write-ups. ReelPulse, DataEye and shortdramatop exist. |
| 29 | BotCheck (brand AI-bot leaderboard + QA) | **WOUNDED** | 4/6 | **3/6** | Legal and cost exposure from bot-testing third parties. The QA market is crowded (Cekura, Maxim, Confident AI, Lorikeet, and the vendors' own tools). |
| 30 | SherlockWatch (platform-risk alerts + index) | **WOUNDED (pivot to media)** | 4/5 | **3/4** | Great content, weak SaaS willingness to pay. Viable as a sponsor-funded newsletter. |
| 31 | CreatorProof (verified creator earnings) | **KILL** | 4/5 | **1/3** | **TrustMRR already verifies Whop, LemonSqueezy, Polar, Paddle, Creem and Stripe revenue.** Whop Trends ranks Whop products. |
| 32 | AppGuard (App Store preflight + clone alerts) | **KILL** | 4/5 | **1/3** | Rork AI App Store Reviewer, AcceptMyApp, open-source preflight skills, fastlane precheck, and AppSmash's copycat list. |
| 33 | ClipAudit (clipping-campaign verification) | **KILL** | 4/5 | **1/3** | The marketplaces now sell "pay per *verified* view" built in. A neutral auditor can't get TikTok/IG data. |
| 34 | BuilderBench (Vibe Coding Index) | **WOUNDED (affiliate media)** | 3/5 | **3/5** | Model benchmarks exist (Vals Vibe Code Bench, BridgeBench). A platform-level index is open, but it's media, not SaaS. |
| 35 | WebGame Radar | **KILL** | 3/4 | **1/2** | Portal games earn $200-2,000/month, so there's no budget. The defender ranks it last too. |

**Counts for this batch: 0 SURVIVES, 4 WOUNDED, 6 KILL.**

---

## 2. Idea-by-idea

### #26 PrintRadar: "what 3D prints actually sell"
**Attacks**
1. **The core data source forbids it.**
   - MakerWorld's terms ban scraping *and* "monitoring" by bots or AI, and reserve legal action ([MakerWorld ToU](https://makerworld.com/en/user-agreement)).
   - Bambu Lab controls the ecosystem tightly (firmware, Bambu Studio, Handy app). It is building its own commerce layer: the **Commercial License Membership** for selling prints and the **3D Print Farm Map** ([Bambu forum](https://forum.bambulab.com/t/empowering-our-creators-with-new-commercial-license-membership/145511), [Farm Map](https://makerworld.com/en/farm-map-condition)). MakerWorld also publishes its own weekly editorial ("Print This Week"; [MakerWorld](https://makerworld.com/en/topics/PLM2026082801296)).
   - A "trending commerce" tab is an obvious next step for them, which is platform risk (PLAT-type).
2. **Anyone can clone it.** An Apify MakerWorld scraper exists. Etsy research is served by eRank, EverBee and Insight Agent, which already publishes "best-selling 3D printed items on Etsy" pages and an Etsy trend tool ([Insight Agent](https://www.insightagent.app/guides/best-selling-3d-printed-items-etsy)).
3. **Willingness to pay.** Most sellers are hobbyists and side-hustlers. $9/month is low-value and churny. Real print farms are few, and they already know their bestsellers from their own sales.

**What's strong:** a booming global hobby (Bambu at RMB 10B revenue, 10M MakerWorld MAU). The content is superb (timelapses, "top 10 rising prints"). There's a new pain after Etsy's June 2025 policy.

**Verdict: WOUNDED.** What would convince me: a **legal data plan** that doesn't scrape MakerWorld. For example:
- **seller-connected sales data** (Etsy, Shopify or TikTok Shop OAuth, read-only) pooled into an anonymised "what sells" index (first-party flywheel);
- Printables or Thangs data only where an API or permission exists;
- Etsy data only through approved Commercial Access;

plus evidence that ≥50 sellers would connect a shop in exchange for peer benchmarks.

**Chance 3 / Scale 4.**

---

### #27 GigRate: AI-trainer pay index and referral alerts
**Attacks**
1. **The pay index already exists, several times over.**
   - **OpenTrain AI "AI Training Jobs Pay Rates: Hourly Rate Index"** ([OpenTrain](https://www.opentrain.ai/jobs/pay-rates/)).
   - **aitrainer.work**: "Pay Rates in the AI Evaluation Economy (2026): A Cross-Platform Benchmark of 2,082 Active Listings" ([aitrainer.work](https://aitrainer.work/research/ai-training-pay-rate-platform-analysis-2026)).
   - **AITraining.jobs**: "what AI training work really pays, measured daily" ([AITraining.jobs](https://aitraining.jobs/)).
   - **AlignList**: pay ranges plus community reliability reviews ([AlignList](https://alignlist.com/)).
   - AIWorkfinder, aigigjobs.com and Mindrift.
   - The differentiator "we benchmark pay, they only list jobs" is **false**.
2. **The monetisation hook is weak and restricted.**
   - Mercor's referral terms require outreach to be "lawful, consent-based… compliant with anti-spam… platform and messaging rules" ([Mercor referral T&C](https://talent.docs.mercor.com/policies/referral-terms-and-conditions)).
   - Referral codes for Outlier are already dumped on invitation.codes and referralcodes.com, and social referral spam reportedly gets accounts flagged ([HireFeed](https://hirefeed.co.in/blog/outlier-referral-bonus-2026)).
   - Referral income is not MRR and can be switched off overnight.
3. **Volatile demand.** Scale AI cut about 500 contractors in July 2025, and OpenAI and Google pulled work after Meta's Scale deal ([Wikipedia: Scale AI](https://en.wikipedia.org/wiki/Scale_AI)). This labour market is 100% dependent on a few labs' budgets.

**Verdict: KILL.** **Chance 1 / Scale 3.**

---

### #28 DramaCharts: micro-drama title and trope intelligence
**Attacks**
1. **Title-level charts already exist.**
   - **SocialPeta** publishes a **"Short Drama Weekly Ranking"** covering **43k titles**, with named titles, their promoting apps and **trope and theme trend write-ups** ("Family Search Revenge Romance Soars") ([SocialPeta](https://socialpeta.com/en/blog/short-drama-weekly-ranking-43k-titles-compete-as-ai-dramas-rise-and-fruit-themed-melodramas-expand-globally), [SocialPeta 2](https://socialpeta.com/en/blog/short-drama-weekly-ranking-family-search-revenge-romance-soars)).
   - **DataEye-ADX** tracks overseas short-drama ad materials, 4.73M groups in May 2026 ([36Kr](https://eu.36kr.com/en/p/3853934505818752)).
   - **ReelPulse** has rankings, weekly market data and "best DramaBox shows, updated weekly" ([ReelPulse](https://reelpulse.net/guides/best-dramabox-shows)).
   - shortdramatop.com and vitrina.ai also exist, plus the Apify scraper.
   - "Nobody owns the Billboard of micro-dramas" is **false** on the B2B side, and fan-side SEO is already contested.
2. **The buyers are small and served.** Western studios and UA agencies already pay SocialPeta or DataEye for ad intelligence, which is where the title signal actually comes from (ad creative volume, not app top lists).
3. **Data access.** In-app charts aren't public APIs, and TikTok and Meta promo-view data is hard to get legally.

**Verdict: KILL.** **Chance 2 / Scale 4.**

---

### #29 BotCheck: public leaderboard of brands' AI support bots, plus QA
**Attacks**
1. **Legal and cost exposure from mystery-shopping third-party bots at scale.**
   - Most sites' terms prohibit automated access, and chat widgets sit behind bot protection.
   - More seriously, **many vendors bill brands per resolution** (Intercom Fin charges $0.99 per resolution; SAT-13). Automated test chats can **impose real costs** on the brands being tested. That invites cease-and-desist letters rather than badges.
   - Publishing "this bot invented a refund policy" about a named brand is a factual allegation. It needs airtight evidence and a right of reply (defamation, and §824 BGB in DE).
2. **The paid monitoring layer is crowded.**
   - Agent QA and simulation tools: Cekura, Maxim, Confident AI, Galileo, Future AGI, and **Lorikeet** (a support agent with a built-in "Coach" doing continuous QA) ([Lorikeet](https://www.lorikeetcx.ai/articles/ai-qa-simulation-coaching-support-teams-2026), [Maxim](https://www.getmaxim.ai/articles/top-5-platforms-to-simulate-ai-agents-to-ensure-production-reliability-in-2026/)).
   - The support-AI vendors sell "accuracy" as their own feature (Fini claims 98% accuracy; [Fini](https://www.usefini.com/guides/ai-chatbot-customer-service-platforms-tested)), so they'll bundle QA.
3. **The buyer is enterprise CX** (Fin, Decagon and Sierra customers), with $199-499/month and a procurement process. Inbound via LinkedIn is plausible, but the sales cycle is slow for a solo student.

**What's strong:** the public leaderboard is genuinely novel content that is global and press-worthy (vendor blogs rank *platforms*, not *brands*). It's cheap to build with Playwright plus LLM grading.

**Verdict: WOUNDED.** What would convince me:
- (a) **The leaderboard is small, slow and human-paced**: 10 standard questions, monthly, with public evidence, a methodology page and a right of reply. It should avoid vendors that bill per resolution, or disclose that clearly.
- (b) **The paid product targets the underserved SMB tier**: Shopify merchants using Gorgias AI, Tidio Lyro, Shopify Inbox AI and similar. Offer a self-serve $49-99 "policy regression test" sold through the **Shopify App Store**, where enterprise QA tools don't go.

**Chance 3 / Scale 6.**

---

### #30 SherlockWatch: platform-risk alerts and "Sherlocked this week"
**Attacks**
1. **Willingness to pay** from indie hackers for alerts is low. The *content* ("12 categories OpenAI Sherlocked this week") delivers most of the value for free. The defender says so itself.
2. **Substitutes:** TLDR, Ben's Bites, The Rundown and the Killed-by-AI graveyards are free. VC "score your risk" frameworks exist ([Venture Curator](https://www.venturecurator.com/p/ai-startups-model-release-risk)). Klue and Crayon serve teams that can pay.
3. **Matching quality.** Semantic "overlap" alerts will throw false positives. One false "you're dead" alert erodes trust.

**What's strong:** perfect founder-market fit for content (the founder's own X, HN and indie audience), near-zero build cost, zero data-rights risk (public changelogs), and it's global. My own PLAT list shows the news flow is dense.

**Verdict: WOUNDED. Pivot it to a sponsor-funded newsletter plus a free index, with alerts as a light paid tier.** Founder-audience newsletters monetise through dev-tool sponsors, the TrustMRR sponsor model (Round 2). What would convince me: a 6-week test of an X account plus newsletter, targeting ≥2k subscribers and one paid sponsor.

**Chance 3 / Scale 4.**

---

### #31 CreatorProof: verified-earnings badges for creators
**Attacks**
1. **TrustMRR already covers this.** Marc Lou's July 2026 breakdown lists verified revenue from **Stripe ($1.49B), RevenueCat, Superwall, Whop ($3.2M), LemonSqueezy, Polar, Paddle, DodoPayment and Creem** ([Marc Lou on X](https://x.com/marclou/status/2077736510657626203), [TrustMRR FAQ](https://trustmrr.com/faq)). Stan and many course platforms run on Stripe. So "TrustMRR covers startups, not creator platforms" is **wrong**: Whop is already in.
2. **Whop rankings already exist.** **Whop Trends** publishes Whop product rankings by category with revenue estimates across 195k products ([Whop Trends](https://whoptrends.com/rankings)).
3. **Willingness to pay for a badge is doubtful** when TrustMRR listing is free (sponsor-funded). The remaining gap (Gumroad, Kajabi, Skool payouts) is small, and Marc ships connectors in days (the defender's own stated risk).

**Verdict: KILL.** **Chance 1 / Scale 3.**

---

### #32 AppGuard: App Store preflight, rejection index and clone alerts
**Attacks**
1. **Preflight is already a crowded feature.**
   - **Rork's "AI App Store Reviewer"** (from a funded AI app builder) ([Rork](https://rork.com/app-store-reviewer)).
   - **AcceptMyApp** ([AcceptMyApp](https://acceptmy.app/)).
   - **Open-source "app-store-preflight" skills for AI agents** on GitHub ([GitHub](https://github.com/truongduy2611/app-store-preflight-skills)), plus fastlane precheck **[MEMORY]**.
   - **Push My App's** rejection index.
   - The builders (Rork, and presumably others) internalise it, the same platform pattern as #1.
2. **Clone alerts exist too.** **AppSmash** runs daily store sweeps plus a public "Copycat Shame List" ([AppSmash](https://appsmash.tech/copycat-shame)). Enterprise brand protection covers the high end.
3. **The rejection index needs a crowd** that already exists elsewhere (Reddit, the Apple dev forums). Willingness to pay from app-factory indies is $9-19.

**Verdict: KILL.** **Chance 1 / Scale 3.**

---

### #33 ClipAudit: independent verification of clipping campaigns
**Attacks**
1. **Verification is becoming the marketplaces' core feature.**
   - Clipper screens every submission with bot-confidence scoring before payout.
   - clipping.net sells "pay per verified view".
   - Clipify and others advertise viewbot filtering.
   - Whop added bot detection and a payout delay ([Growthr comparison](https://growthr.com/resources/best-clipping-platforms/), [clipping.net](https://clipping.net/brands), [FindClout](https://findclout.com/blog/best-clipping-platform-for-brands)).
   - Brands pick the marketplace that verifies. They won't pay a third party 2-3% on top.
2. **Data access.** Independent view authentication needs TikTok and Instagram data that isn't available at scale to third parties. YouTube Shorts alone is a partial view.
3. **A young, volatile market** (the defender's own "fraud flywheel" risk). The buyer pool of brands running $20k+ pools is small.

**Verdict: KILL.** **Chance 1 / Scale 3.**

---

### #34 BuilderBench: the monthly "Vibe Coding Index"
**Attacks**
1. **Model-level benchmarks exist and get cited.** **Vals AI Vibe Code Bench** (full web apps with Supabase, Stripe and email) ([Vals](https://www.vals.ai/benchmarks/vibe-code)), **BridgeBench V3** (scores security, trustworthiness and cost) ([BridgeMind](https://www.bridgemind.ai/blog/bridgebench-v3-vibe-coding-benchmark)), the academic ViBench, plus "tested and ranked" posts from builders themselves (Emergent, Zite). The *platform-level* monthly index is the only open slot.
2. **It's media, not SaaS.**
   - Affiliate economics: **Lovable pays about 20% recurring (up to $100 per subscriber)** and **Replit pays $10 one-time** ([OpenAffiliate Lovable](https://openaffiliate.dev/programs/lovable), [OpenAffiliate Replit](https://openaffiliate.dev/programs/replit)).
   - €1k/month means roughly 200 active Lovable referrals.
   - Paid "reports" at $49 will sell a handful.
   - Builder-funded data deals create a conflict of interest.
3. **Cost and upkeep.** Building 5 apps on 12 builders monthly takes paid plans, credits and hours, and the harness breaks with every builder update.

**What's strong:** the most citable, shareable asset in the batch ("same app, 12 builders, 7 leaked the DB"). It's global, and it complements #1.

**Verdict: WOUNDED (as affiliate media).** What would convince me: (a) a lean version (3 apps × 6 builders, quarterly, with YouTube as the main surface); (b) confirmation that affiliate terms allow comparison content; (c) a plan for the founder's hours per month.

**Chance 3 / Scale 5.**

---

### #35 WebGame Radar
**Attacks**
1. **No budget.** The defender's own source says a good portal game earns $200-2,000/month ([Cinevva](https://app.cinevva.com/guides/web-game-monetization)).
2. **The portals control the data** and can block scraping. Playgama already runs cross-portal analytics infrastructure for its 4,000+ developers ([Playgama](https://playgama.com/about-us/)).
3. The defender ranks it last.

**Verdict: KILL.** **Chance 1 / Scale 2.**

---

## 3. Running tally across all 35 ideas (before the defender's Round-2 rebuttals)

| Status | Ideas |
|---|---|
| **SURVIVES (conditional)** | #2 "Wen empfiehlt die KI?" |
| **WOUNDED, better odds of converting** (clear, cheap fix; global or content-native) | #1 LaunchGuard → EU Launch Check (passive-only data) · #9 Nachfolge-Radar → sponsor newsletter · #12 CRA → global IoT compliance (CRA + UK PSTI) · #7 GLP-1 → global coach kit · #29 BotCheck → Shopify-SMB bot QA + a slow public leaderboard · #30 SherlockWatch → founder newsletter · #34 BuilderBench → affiliate media |
| **WOUNDED, lower odds** (Germany-only ceiling or hard dependency) | #3 Netzbetreiber-Radar · #4 Pflegebudget · #6 MiSpeL · #8 Zitat-Check · #20 Pay-Range (global pivot) · #26 PrintRadar (data rights) |
| **KILL** | #5, 10, 11, 13, 14, 15, 16, 17, 18, 19, 21, 22, 23, 24, 25, 27, 28, 31, 32, 33, 35 (21 ideas) |

**Realistic survivors today: about 5-8.** That's #2, plus the 4-7 "better odds" wounded ideas *if* the rebuttals deliver the requested evidence. That's short of the 10-15 target, so **more candidates are needed**.

### What kinds of ideas would most likely produce more survivors
1. **First-party data flywheels instead of scraping.** Users connect *their own* account (Shopify, Etsy, Stripe, YouTube, App Store Connect, Google Business Profile) via OAuth and get a **peer benchmark plus a shareable score card**. It's legal, the data is unique, clones can't copy it, and the share card is the content. (Check crowding per niche first.)
2. **Localisation arbitrage of proven US SaaS.** Take a tool with proven willingness to pay that is English-only, and build the German/EU-language version, where the founder's language is a real moat and German SEO is less contested. #2 is the template: Local Falcon and Peec prove the demand, and German prompts and DACH directories make the difference. This is the single most reliable pattern for this founder.
3. **Marketplace-native apps in *new* store categories** (Shopify App Store, Chrome Web Store, WordPress.org, Claude and ChatGPT connector directories), where the store provides inbound discovery. For example, SMB-tier QA for Shopify support bots (#29's pivot), or AI Act Art. 50 disclosure widgets for EU sites. Check the store listings first.
4. **Founder-audience media with a sponsor model** (#30, #34). Low willingness to pay per user doesn't matter if sponsors pay. Distribution is the founder's native X, HN and indie scene.
5. **Avoid:** indexes of platforms whose terms forbid scraping (MakerWorld, micro-drama apps, TikTok), audiences with near-zero budgets (hobbyists, gig workers, OSS maintainers, web-game devs), and anything that TrustMRR, SocialPeta, Apify or a builder platform already does.
