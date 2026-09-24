# Round 2b (Defender): 10 additional candidates, #26 to #35

Author: DEFENDER agent, 2026-09-24. These additions supplement `01-defender-candidates.md`.

**Profile requested by the coordinator.** Each idea should be:
- global and English-first;
- one where the product's output *is* the social content;
- simple to build (thin wrappers or scrapers are fine);
- in an emerging market, avoiding the critic's saturation map (`01-critic-ammunition.md` §2).

**Founder updates applied here:** global by default, inbound-only GTM, and two scores per idea (Chance of reaching the first €1k and then €10k MRR; Scale if it works). "(unverified)" marks single-source or vendor-reported numbers.

---

## 0. What I learned while researching this batch (important for the debate)

1. **In 2026, a public-data "index" can be cloned in days.** Apify already sells scrapers for almost every ecosystem the coordinator listed:
   - Skool rankings ([Apify](https://apify.com/tactful_anvil/skool-communities-scraper))
   - Substack leaderboards ([Apify](https://apify.com/rowsmith/substack-leaderboard-tracker))
   - Whop clipping campaigns ([Apify](https://apify.com/tactful_anvil/whop-content-rewards-scraper))
   - DramaBox/ReelShort rankings ([Apify](https://apify.com/signalbench/short-drama-trends))
   - web-game portals ([Apify](https://apify.com/obliging_persimmon_cki/web-game-distribution-platform-intelligence))
   - SaaS changelogs ([Apify](https://apify.com/runtime/saas-changelog-product-updates-monitor))

   So I ranked higher the ideas that also have:
   - **(a) a user-contributed data flywheel**: crowdsourced quotes, verified revenue, rejection reports, clip audits; or
   - **(b) a transactional revenue hook** that doesn't depend on selling data subscriptions: referral bonuses, verification badges, per-check fees.

2. **Many of the suggested directions already have a reference tool, so I dropped them** (details in §3). Examples: Skool (skoolstats), Substack (Newsletter Insights), Whatnot (Viewnot), Shopify apps (AppstorePulse), Hyrox (5+ tools), prediction markets (60+ dashboards), ChatGPT-ads intelligence (Adthena, Otterly, SE Ranking), podcasts (Rephonic, Podscan), YouTube sponsorship databases (5+), Roblox brands (ROLearn, GEEIQ), verified startup revenue (TrustMRR, which already supports RevenueCat).

3. **What's left are young ecosystems that have real money but no reference brand yet:** micro-dramas, consumer 3D printing, clipping, AI-trainer gigs, AI support agents, and the AI-app-factory wave.

---

## 1. Ranked summary (#26-#35)

| # | Idea | Theme (overall) | Model | Chance | Scale |
|---|---|---|---|---|---|
| 26 | **PrintRadar**: "what 3D prints sell" radar for print farms and designers | Media, games & maker commerce | Prosumer/SMB, global | 5 | 5 |
| 27 | **GigRate**: AI-trainer gig pay index and alerts, monetised by referrals | Creator & gig economy | B2C, global | 5 | 5 |
| 28 | **DramaCharts**: micro-drama title and trope intelligence | Media, games & maker commerce | B2B, global | 4 | 6 |
| 29 | **BotCheck**: public leaderboard of brands' AI support agents, plus QA monitoring | AI agents & startup intel | B2B, global | 4 | 6 |
| 30 | **SherlockWatch**: platform-risk alerts, plus a weekly "Sherlocked this week" index | AI agents & startup intel | B2B SMB/prosumer, global | 4 | 5 |
| 31 | **CreatorProof**: verified-earnings badges and leaderboard for creator businesses | Creator & gig economy | B2B SMB, global | 4 | 5 |
| 32 | **AppGuard**: App Store preflight, rejection index and clone alerts for AI-built apps | Dev & app-builder tools | Prosumer, global | 4 | 5 |
| 33 | **ClipAudit**: independent verification of clipping campaigns, plus a Clipping Index | Creator & gig economy | B2B, global | 4 | 5 |
| 34 | **BuilderBench**: monthly benchmark of AI app builders ("Vibe Coding Index") | Dev & app-builder tools | Content + B2B, global | 3 | 5 |
| 35 | **WebGame Radar**: trend radar across web-game portals and YouTube Playables | Media, games & maker commerce | Prosumer, global | 3 | 4 |

### Theme check across all 35 ideas (max 5 per theme)
To keep the tech-heavy themes under the cap, I re-grouped the round-1 "AI & dev" ideas.

| Theme | Round 1 | Round 2b | Total |
|---|---|---|---|
| EU compliance tools | 12, 13, 14, 17, 20 | none | 5 |
| Home energy & grid | 3, 6, 10, 22, 25 | none | 5 |
| Care, health & family | 4, 7, 11, 19 | none | 4 |
| Work/HR & fleet | 5, 18 | none | 2 |
| Property, public services, SME succession, sovereignty | 9, 15, 16, 24 | none | 4 |
| AI search & professional AI | 2, 8, 21 | none | 3 |
| Dev & app-builder tools | 1, 23 | 32, 34 | 4 |
| AI agents & startup intelligence | none | 29, 30 | 2 |
| Creator & gig economy | none | 27, 31, 33 | 3 |
| Media, games & maker commerce | none | 26, 28, 35 | 3 |

---

## 2. The ideas in detail

### #26 PrintRadar: "what 3D prints actually sell" radar
**Pitch.** A weekly radar of which 3D-printed products are selling and trending. It covers MakerWorld, Printables, Thangs and Cults (downloads, boosts and trending lists), and Etsy, eBay and TikTok Shop listings. Each item links to its licence type, and alerts fire for "rising designs".

**Audience.** Print-farm operators and side-hustlers who sell printed goods, plus 3D designers deciding what to model next.
- Bambu Lab hit **RMB 10B revenue in 2025** (about 30% of the global market) and tripled unit sales ([KrASIA](https://www.kr-asia.com/pulses/161999)).
- MakerWorld had **about 10M monthly active users** and 2.6M original models by the end of 2025 ([3DPrint.com](https://3dprint.com/324181/bambu-lab-says-2025-was-a-breakout-year-10-million-monthly-users-and-real-business-growth/)).
- Coverage says consumer printing "is becoming a real side business for many people".
- Listing 100 customers is easy: r/BambuLab, and Etsy/TikTok Shop sellers tagged "3D printed".

**The new problem, and why now.**
- **Etsy's 10 June 2025 creativity-standards change** bans selling prints of third-party designs, *even with a commercial licence* ([Tom's Hardware](https://www.tomshardware.com/3d-printing/etsy-cracks-down-on-3d-printed-products-new-rules-exclude-many-3d-printed-items-from-listings), [TCT](https://www.tctmagazine.com/from-templates-to-originality-etsy-new-3d-printing-policy/)).
- So sellers now need two things: (1) which *original* design niches are rising, and (2) which channels still allow licensed prints (eBay, TikTok Shop, their own shop).
- Trends move weekly: print-in-place dragons, fidgets, and so on ([Gauge3D](https://gauge3d.com/2026/08/21/%F0%9F%94%A5-whats-hot-on-makerworld-right-now-and-what-im-printing-next/)).

**Current competitors and why they fall short.**
- The platforms' own "trending" pages cover one platform each and show no commerce data.
- Generic Etsy research tools (eRank, EverBee) aren't built around 3D printing or licences.
- Pricing calculators (printcal.co) and blogs.
- I found no cross-platform "demand radar" for print farms (unverified absence).

**MVP (5-7 weeks).**
- Collectors for the public trending pages of MakerWorld, Printables and Thangs, checking terms first and preferring RSS or API where they exist.
- Etsy listing data via the Etsy Open API.
- A trend score: velocity plus the gap between downloads and number of sellers.
- Licence tagging, a weekly digest, niche pages, and a Stripe paywall for alerts and history.

**Inbound GTM plan.**
- Posts (TikTok/YouTube Shorts timelapses, r/BambuLab, r/3Dprinting, X):
  1. "The 10 3D prints selling fastest this week, and which ones you're still allowed to sell after Etsy's ban."
  2. "This articulated octopus went from 0 to 40k downloads in 9 days. Here's the data."
  3. "I printed the #1 rising design and sold out at a market." (before/after)
- SEO: "best selling 3D prints [month]", "what to 3D print and sell", and programmatic pages per niche ("3D printed [fidget/organizer/planter] demand").
- Viral loop: designers share their "Rising on PrintRadar" badge. Weekly newsletter.
- Better strategy: an affiliate deal with filament brands and printer resellers.

**Pricing and willingness-to-pay evidence.** Free weekly top 10. $9/month for sellers (alerts, history, licence filter); $29/month for print farms (niche tracking, export). Comparable Etsy research tools charge similar amounts (unverified). A farm of 20+ printers spends thousands on filament, so one good product pays for a year.

**Biggest risk.**
- Scraping terms at MakerWorld and Etsy; Bambu could close access or build "trending commerce" itself.
- Hobbyist willingness to pay is limited.
- It's a trend market; if 3D printing cools, demand falls.

**Chance 5 / Scale 5.** A booming global hobby-to-business market with very visual content and no clear reference tool yet. The ceiling is a niche SMB/prosumer market.

---

### #27 GigRate: pay index for AI-trainer gigs, plus alerts
**Pitch.** A live index of what AI-training and data-work platforms pay by expertise (coding, law, medicine, languages), with new project alerts, onboarding difficulty and payout reliability reported by users. Revenue comes mainly from platform **referral bonuses**, plus a $7/month alerts tier.

**Audience.** Professionals and students worldwide doing AI-training gigs, a global and English-first market.
- Mercor reports more than 30,000 contractors and more than $1.5M paid per day ([Mercor](https://www.mercor.com/resources/experts/ai-trainer-salary-hourly-rates/), vendor).
- Handshake's AI data business reached about $950M annualised gross revenue by Apr 2026 (secondary, unverified).
- Expert rates run $50-250/h ([opentrain](https://www.opentrain.ai/blog/ai-trainer-salary-and-hourly-pay/)).

**The new problem, and why now.** The labs' demand for expert data exploded in 2025-2026, spread across 20+ platforms (Mercor, Outlier, Handshake AI, micro1, Alignerr, DataAnnotation, Surge and others) that differ widely in pay, reliability and project availability. Workers currently compare notes in scattered Reddit and Discord threads.

**Current competitors and why they fall short.** [AIWorkfinder](https://aiworkfinder.com/) (free aggregator with referral links), AlignList, and listicle sites (theairankings, hirefeed, remowork).
- Where I'd win: **pay-rate data per expertise and country contributed by users** ("Outlier coding evaluators: $52-62/h this week"), payout-reliability scores, and a public index people cite.
- The aggregators list jobs but don't benchmark pay.

**MVP (4-5 weeks).**
- Scrape public listings from 10+ platforms.
- A pay-report form (optionally verified with a screenshot of a pay stub, with PII removed by OCR and blurring).
- An index by expertise, platform and country; alerts by email or Telegram; and referral links with clear disclosure.

**Inbound GTM plan.**
- Posts (TikTok side-hustle niche, LinkedIn for lawyers, doctors and engineers, Reddit):
  1. "AI companies are paying lawyers $120/h to grade chatbots. Here are this week's highest-paying projects."
  2. "Outlier vs Mercor vs Handshake: who actually pays on time? (1,200 worker reports)"
  3. "The AI Gig Pay Index, September: coding evaluators up 8%."
- SEO: programmatic "[platform] pay rate [role]" and "AI training jobs for [nurses/lawyers/German speakers]".
- Viral loop: workers share their "pay report" card, and referral links spread the product.

**Pricing and willingness-to-pay evidence.**
- Mercor pays referrers **20% of the referred person's earnings, from $250 up to $15,000 per referral** ([Mercor referrals](https://www.mercor.com/referrals/), [refer.me](https://refer.me/company-bonus/mercor)).
- Outlier pays **$25-200 per referral** ([HireFeed](https://hirefeed.co.in/blog/outlier-referral-bonus-2026)).
- A handful of successful referrals a month reaches €1k.
- The premium alerts tier is $7/month.

**Biggest risk.**
- Demand cycles: the labs could cut data budgets, or platforms could change their referral programs.
- Platforms may object to scraping (listings are public).
- Scam platforms entering the space, so moderation is needed.
- "Referral-driven" revenue is less predictable than MRR.

**Chance 5 / Scale 5.** A fast path to first revenue through referrals, a global audience, and daily content. The ceiling depends on the AI-data market.

---

### #28 DramaCharts: micro-drama title and trope intelligence
**Pitch.** Daily charts of which micro-drama titles and tropes are rising across ReelShort, DramaBox, NetShort, FlexTV and others. Data comes from the apps' public top lists plus promo-clip views on YouTube, TikTok and Meta. Adds a trope index ("billionaire werewolf -18%"), a "new-release radar", and weekly briefs for producers, writers and ad buyers.

**Audience.** Western micro-drama studios, independent producers, screenwriters, actor agents, AI-drama creators, platform acquisitions teams and UA agencies.
- In Los Angeles, "a permit for another micro-drama every single day" ([Spectrum](https://spectrumlocalnews.com/ca/bay-area/entertainment/2026/01/17/vertical-microdramas-rise)).
- The trade press calls it a "production gold rush" ([Hollywood Reporter](https://www.hollywoodreporter.com/business/business-news/microdrama-series-verticals-production-1236418912/), [Variety](https://variety.com/2026/tv/features/can-microdramas-save-hollywood-why-vertical-boom-isnt-quibi-1236837033/)).

**The new problem, and why now.**
- In-app micro-series revenue is forecast at **$7.8B in 2026**, up from $3.8B ([Deloitte](https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2026/short-form-video-series.html)).
- Revenue outside China is forecast at **$3.6B** ([Screen Daily](https://www.screendaily.com/news/microdrama-revenue-outside-china-to-hit-36bn-in-2026-says-report/5219165.article)).
- Each series costs $100k-300k, so picking the wrong trope is expensive.
- AI-generated and manhua-style dramas are surging (+137% in ad placements, per [36Kr](https://eu.36kr.com/en/p/3853934505818752)).

**Current competitors and why they fall short.**
- Sensor Tower ([report](https://sensortower.com/report/state-of-short-drama-apps-2026)) and Insightrackr work at **app** level, not title or trope level.
- DataEye is China-focused.
- ReelPulse ([site](https://reelpulse.net/)) is "short drama industry intelligence"; I couldn't fetch it, so its depth is unverified.
- An Apify scraper of DramaBox/ReelShort rankings exists.
- Nobody owns the English-language, title-level "Billboard of micro-dramas" yet (unverified).

**MVP (6-8 weeks).**
- Collectors for the top lists on each app's web or public pages (check terms first).
- YouTube Data API views for the official promo channels.
- LLM trope tagging from synopses.
- Daily charts, title pages, a trope index, weekly PDF briefs, and alerts.

**Inbound GTM plan.**
- Posts (LinkedIn for industry; TikTok and X for fans):
  1. "Top 10 micro-dramas this week. 3 are AI-generated."
  2. "The trope index: 'secret heir' is dying, 'contract marriage with the mafia boss' is up 40%."
  3. "We tracked 500 new releases. Here's what hits in week one."
- SEO: programmatic title and trope pages ("[title] episodes/ranking", "best [trope] micro dramas"), which fans search in large numbers, plus B2B landing pages.
- Viral loop: studios share "#1 on DramaCharts" badges, and the press can cite the charts.

**Pricing and willingness-to-pay evidence.** Fans get the free charts (ad-supported). The B2B tier is $99-299/month (history, exports, alerts, trope analytics); custom reports cost $1-3k. Buyers are budgeting $100k-300k per series.

**Biggest risk.**
- Data access: apps can block scraping, and TikTok view data is hard to get legally.
- The B2B buyer pool is small (hundreds to low thousands).
- Sensor Tower or DataEye could add title-level data.

**Chance 4 / Scale 6.**

---

### #29 BotCheck: public leaderboard of brands' AI support agents, plus QA monitoring
**Pitch.** Every week BotCheck "mystery-shops" hundreds of brands' AI support chatbots with the same standard questions (refund policy, cancellation, escalation to a human, made-up discounts). It publishes a public accuracy and helpfulness leaderboard by industry. The paid product is continuous QA monitoring of your *own* AI agent against your policies, with hallucination alerts.

**Audience.** CX and support leads at B2C companies that have deployed Intercom Fin, Zendesk AI, Decagon, Sierra, Ada, Salesforce Agentforce or home-built bots, starting with e-commerce, SaaS, travel and fintech. Listing 100 is easy from vendors' customer showcases.

**The new problem, and why now.**
- AI-agent adoption in service organisations rose from about **39% to 66%** in 2025-2026, per Salesforce research ([Salesforce](https://www.salesforce.com/news/stories/ai-service-agents-improve-customer-satisfaction/), summarised via [Ringly](https://www.ringly.io/blog/ai-customer-service-statistics-2026)).
- Support chatbots hallucinate in **15-27%** of cases in one 2026 benchmark ([IrisAgent](https://irisagent.com/blog/best-llms-for-customer-support-chatbot-2026/), vendor).
- Companies are liable for what their bots say (Moffatt v. Air Canada, 2024 [MEMORY]).

**Current competitors and why they fall short.**
- CX QA tools (Zendesk QA/Klaus, MaestroQA) grade human agents.
- Voice-agent testing platforms (Cekura, Hamming, Coval) [MEMORY] focus on developers testing their own voice agents.
- Model benchmarks (IrisAgent, Vectara) test models, not deployed brand bots.
- I found **no public brand-by-brand leaderboard** (my search turned up none).

**MVP (6-8 weeks).**
- A Playwright harness that opens website chat widgets and runs a standard script.
- LLM grading against each brand's *public* policy pages (refunds, shipping).
- A public leaderboard with anonymised examples.
- Paid: connect your own bot (via API or widget), a policy knowledge base, scheduled regression tests, and Slack alerts.

**Inbound GTM plan.**
- Posts (LinkedIn for CX leaders, X):
  1. "We asked 100 brands' AI support bots the same 10 questions. 31 invented a refund policy."
  2. "The AI Support Leaderboard, Q3: best airline bot, worst telecom bot."
  3. "This bot offered me a 50% discount that doesn't exist. (screen recording)"
- SEO: programmatic pages "[Brand] AI chatbot review/score" and "[Vendor] Fin vs Decagon accuracy".
- Viral loop: top-ranked brands share their "BotCheck A-rated" badge; low-ranked brands find their page and buy monitoring.

**Pricing and willingness-to-pay evidence.** $199-499/month per bot; $999/month for agencies. Buyers already pay about $0.99 per resolution for Intercom Fin (critic's SAT-13), and one bad policy hallucination can cost more than a year of monitoring.

**Biggest risk.**
- Legal and ethical: automated testing of third-party bots may breach site terms, and publishing low scores invites pushback. Mitigate with standard, harmless questions, a methodology page and a right of reply.
- Platform vendors could ship their own QA dashboards (Intercom already has some analytics).
- B2B sales cycles, although the leaderboard makes it inbound.

**Chance 4 / Scale 6.**

---

### #30 SherlockWatch: platform-risk alerts and a "Sherlocked this week" index
**Pitch.** Describe your product in two sentences. SherlockWatch monitors release notes, changelogs and launch events from about 40 platforms (OpenAI, Anthropic, Google, Microsoft, Apple, Shopify, Meta, Notion, Canva, Stripe, Vercel, Lovable and others). It alerts you when a new feature overlaps your product, with a severity score and a suggested response. A public weekly index lists which startup categories just got "Sherlocked" (made redundant by a platform feature).

**Audience.** Founders of SaaS, AI and micro-SaaS companies, indie hackers, and VCs (portfolio monitoring), worldwide. Listing 100 is easy from Product Hunt launches, YC company lists, and TrustMRR listings.

**The new problem, and why now.** 2026 has been the year of platform kills:
- Claude Cowork plugins wiped about $285B of software market cap in a day.
- Claude Code Security hit cyber stocks.
- Shopify Sidekick generates custom apps, and Meta Business Agent is free.
- The critic's own ammunition file lists 24 such platform moves in 20 months (PLAT-01 to PLAT-24 in `01-critic-ammunition.md`).
- The pace means founders can't track it manually, and "is this idea dead?" is now a daily question.

**Current competitors and why they fall short.**
- Competitive-intelligence suites (Klue, Crayon) are enterprise-priced and track named competitors, not platforms.
- Changelog monitors (Apify actors, Visualping, Adversa) just diff pages.
- AI newsletters (TLDR, Ben's Bites) report launches but don't map them to *your* product.
- Nothing does semantic "platform overlap" matching for small teams.

**MVP (4-6 weeks).** Collectors for about 40 changelogs, blogs, docs and RSS feeds; LLM feature extraction; embedding match against user product profiles; severity scoring; email and Slack alerts; and the public weekly index.

**Inbound GTM plan.**
- Posts (X, HN, LinkedIn, r/SaaS, Indie Hackers):
  1. "12 startup categories OpenAI and Anthropic Sherlocked this week."
  2. "Shopify just shipped X. These 40 Shopify apps are now at risk."
  3. "The Sherlock Index: which categories got hit hardest in Q3 2026."
- SEO: programmatic "[platform] new features [month]" and "is [category] dead after [launch]?".
- Viral loop: founders share their "platform-risk score"; VCs forward the weekly index.

**Pricing and willingness-to-pay evidence.** $12/month solo, $49/month team, $299/month for VC portfolio packs. The cost of missing a Sherlock event is months of wasted building.

**Biggest risk.** The content may be more loved than the product: people read the free index and never pay. Low willingness to pay among indie hackers. Newsletters could add matching.

**Chance 4 / Scale 5.** Perfect content fit for the founder's own X and indie community, and very cheap to build.

---

### #31 CreatorProof: verified-earnings badges and leaderboard for creator businesses
**Pitch.** Creators who sell courses, communities or digital products connect their payout sources (Whop, Stan/Stripe, Gumroad, Kajabi, Lemon Squeezy) through read-only access. They get a **verified earnings badge** for sales pages, an income-disclosure page that meets FTC expectations, and an opt-in public leaderboard ("TrustMRR for creators").

**Audience.**
- Whop alone: about 183k sellers, $2.67B lifetime GMV by Feb 2026, and $200M raised from Tether at a $1.6B valuation ([Sacra](https://sacra.com/c/whop/), [RockWater](https://wearerockwater.com/tether-invests-in-whop/)).
- Gumroad: about 17k active creators (secondary).
- Plus Skool and Stan creators. English-first, global.

**The new problem, and why now.**
- Fake-guru income claims and AI-powered course scams are the #1 trust problem in "make money online" ([scam.courses](https://scam.courses/blog/course-red-flags-2026)).
- Whop's marketplace is criticised as spammy ([group.app review](https://www.group.app/blog/whop-review/)).
- The FTC requires income claims to be substantiated ([MEMORY]: FTC Operation AI Comply, 2024; earnings-claims enforcement).
- TrustMRR showed that verified-revenue leaderboards go viral (launched Nov 2025), but it covers Stripe, RevenueCat, Superwall and Creem startups, **not creator platforms** ([TrustMRR](https://trustmrr.com/), [ChatGate](https://chatgate.ai/post/trustmrr)).

**Current competitors and why they fall short.** TrustMRR (startups), generic social-proof widgets (not verified), and platform-internal stats. I found no verified-earnings badge for creators (search found none).

**MVP (5-6 weeks).** Read-only connectors (Stripe restricted keys, and the Whop and Gumroad APIs), a badge embed (JS widget and image), a verified profile page, a disclosure-page generator, an opt-in leaderboard, and Stripe billing.

**Inbound GTM plan.**
- Posts (X and YouTube MMO community, TikTok):
  1. "Only 14% of the 'six-figure' course sellers we checked could verify it." (from opt-ins; illustrative)
  2. "The Verified Creator Leaderboard: top 20 Whop communities by *verified* revenue."
  3. "I verified my income live."
- SEO: "[guru] income verified", "is [course] legit".
- Viral loop: every badge on a sales page links back ("Verified by CreatorProof"), which is the TrustMRR playbook.

**Pricing and willingness-to-pay evidence.** Free profile and leaderboard; $19/month for the badge and disclosure page; $49/month for agencies. Creators pay for anything that lifts conversion, and verified proof is a conversion lever.

**Biggest risk.** TrustMRR adds Whop or Gumroad connectors (Marc Lou ships fast). Whop builds its own verification. Fraudsters could game read-only access by moving money around, and there is defamation risk if we ever label non-verified creators (so: opt-in only).

**Chance 4 / Scale 5.**

---

### #32 AppGuard: preflight, rejection index and clone alerts for AI-built apps
**Pitch.** For people shipping many AI-built mobile apps:
1. **Preflight:** upload metadata, screenshots and a build description. You get a risk score for Guideline 4.3 (spam/copycat), 5.1 (privacy) and the Nov 2025 AI data-sharing consent rule, with fix suggestions.
2. **Rejection Index:** a crowdsourced, public database of what Apple and Google rejected this week, and why.
3. **Clone alerts:** get notified when look-alike apps copy your name, icon or screenshots, with a pre-filled takedown report.

**Audience.** Indie app studios, "app factories", vibe coders shipping to the App Store and Google Play, and agencies. Global and English-first.

**The new problem, and why now.**
- 4.3 is "the number-one killer for AI-built apps in 2026" ([DEV](https://dev.to/russel_dsouza_bd584a3cb2a/why-your-ai-built-app-wont-pass-app-store-review-in-2026-and-7-fixes-that-work-38oc), [PTKD](https://ptkd.com/journal/rejection-guideline-4-3-ai-spam)).
- Apple updated its rules in 2026 to remove copycat apps ([PYMNTS](https://www.pymnts.com/apple/2026/apple-updates-app-store-rules-to-remove-copycat-apps/)).
- Sora-branded fakes flooded the store in late 2025.
- RevenueCat now publishes playbooks against clones ([RevenueCat](https://www.revenuecat.com/blog/growth/protect-app-from-copycats)).
- Apple reportedly blocked updates from vibe-coding apps in Mar 2026 (secondary, unverified).

**Current competitors and why they fall short.**
- [Push My App](https://pushmyapp.ai/blog/app-store-rejection-reasons) (publishes a "rejection reasons index"; whether it has a product is unverified).
- Agency QA services, and enterprise brand protection (Red Points, BrandShield) that is too pricey for indies.
- Appfigures and AppFollow track reviews and rankings, not rejection risk or clones.

**MVP (6-7 weeks).**
- Preflight: an LLM rubric built on Apple's guidelines, a screenshot and metadata similarity check against top apps in the category (App Store search API), and a privacy-consent checklist.
- A rejection-report form feeding the public index.
- Clone watch: daily App Store and Google Play searches for your app's name, keywords and icon (perceptual hash).

**Inbound GTM plan.**
- Posts (X build-in-public, r/iOSProgramming, indie YouTube):
  1. "Apple rejected 212 AI apps our users submitted this month. Here are the top 5 reasons."
  2. "Someone cloned my app in 48 hours. Here's how I got it taken down."
  3. A weekly "Rejection Index".
- SEO: "Guideline 4.3 rejection fix", "App Store rejection [reason]".
- Viral loop: users share their preflight scores, and every rejection report improves the public index.

**Pricing and willingness-to-pay evidence.** $9 per preflight or $19/month; clone watch $9/app/month. A rejection costs days, and a clone can take real revenue (indie apps make $1k-50k MRR per [appopportunity](https://appopportunity.com/blog/indie-app-revenue-models-2026), unverified).

**Biggest risk.** Apple's review is a judgment call, so the score is only probabilistic. Low-cost audience. Apple or Google could improve their own pre-checks. Several blog-content competitors already exist.

**Chance 4 / Scale 5.**

---

### #33 ClipAudit: independent verification of clipping campaigns, plus a Clipping Index
**Pitch.** Brands and creators pay clippers per 1,000 views. ClipAudit independently audits those campaigns across Whop Content Rewards, Vyro, Promote.fun, Lumina and in-house programs. It checks view authenticity (spikes, geography, engagement ratios, account age), duplicate or reposted clips, and cost per real view. A public **Clipping Index** reports the going CPM by niche, the top campaigns, and payout speed.

**Audience.** Brands, streamers, podcasters and app startups funding clipping pools ($1k-100k each), plus clipping agencies.
- Whop's Content Rewards was reportedly paying about $40k per day ([TechBuzz](https://www.techbuzz.ai/articles/clipping-s-perfect-fraud-flywheel)).
- About $887k was paid out in Feb 2026, and there are marketplaces with 62,900+ clippers ([OpenClip](https://openclip.app/clipping), unverified; [Lumina](https://luminaclippers.com/clipping-campaigns)).

**The new problem, and why now.**
- Whop itself called bot fraud "the single biggest threat" and added bot detection plus a 24-hour payout delay ([TechBuzz](https://www.techbuzz.ai/articles/clipping-s-perfect-fraud-flywheel), [FindClout](https://findclout.com/blog/content-rewards-complaints)).
- Brands now spend across several marketplaces, and each one grades its own homework.

**Current competitors and why they fall short.**
- The marketplaces' built-in verification is not neutral and covers one platform each.
- Review sites (FindClout, ClipAffiliates).
- Influencer-fraud tools (HypeAuditor) target creator accounts, not per-clip campaign payouts.

**MVP (6-8 weeks).**
- Brand uploads the campaign's clip URLs or connects a CSV export.
- YouTube Data API metrics, plus public TikTok and Instagram metadata where the terms allow.
- Anomaly scoring and a cost-per-verified-view report.
- A public index built from brands' anonymised aggregates.

**Inbound GTM plan.**
- Posts (X creator-economy crowd, LinkedIn growth marketers):
  1. "We audited $180k of clipping spend. 23% of views looked botted." (illustrative, from real audits)
  2. "Clipping Index, September: gaming CPMs $0.80, finance $3.10."
  3. "The 10 best-performing clipping campaigns this month."
- SEO: "clipping campaign CPM", "is [marketplace] legit", "clipping fraud".
- Viral loop: clean campaigns publish a "ClipAudit verified" report.

**Pricing and willingness-to-pay evidence.** 2-3% of audited spend, or $99-299 per campaign. When a fifth of a $20k pool is fake, a $199 audit pays for itself.

**Biggest risk.**
- Access to platform data (TikTok's API is restricted).
- The marketplaces improve their own detection.
- The market is young and could deflate if the "fraud flywheel" kills demand.

**Chance 4 / Scale 5.**

---

### #34 BuilderBench: the monthly "Vibe Coding Index"
**Pitch.** Every month, BuilderBench builds the same 5 standard apps (CRUD with auth, marketplace, dashboard, AI chat, payments) on about 12 AI builders and agents: Lovable, Bolt, Replit, v0, Base44, Cursor, Claude Code, Codex, Antigravity, Figma Make and others. Each is scored on security (RLS, secrets), performance, cost, time, and how often it needed human rescue. Results go into a public leaderboard and paid deep-dive reports.

**Audience.** Non-technical founders and agencies choosing a builder; builder companies (for competitive benchmarking); investors. The market is huge: Lovable has $500M ARR and 1M projects per week ([TechCrunch](https://techcrunch.com/2026/06/09/lovable-says-it-has-hit-500m-in-annualized-revenue-with-1-million-new-projects-a-week/)), and Cursor, Replit and others are large (critic's SAT-26).

**The new problem, and why now.** Builders now ship weekly, so comparisons go stale fast. Today's comparisons are one-off articles ([Morph](https://www.morphllm.com/best-vibe-coding-tools), [Technically](https://read.technically.dev/p/2026-vibe-coding-tool-comparison), [EPAM](https://www.epam.com/insights/ai/blogs/best-vibe-coding-tools-v0-lovable-bolt-replit-and-figma-make)). There is no repeatable, public benchmark the press can cite, which is what Artificial Analysis provides for models.

**Current competitors and why they fall short.** Articles and YouTube comparisons; model benchmarks (SWE-bench, Artificial Analysis) that test models, not end-to-end app builders.

**MVP (6-8 weeks).** A harness per builder (some manual steps are OK at first), automated checks (the security scanner from #1, Lighthouse, cost logs), a leaderboard site, and the monthly report.

**Inbound GTM plan.**
- Posts:
  1. "We built the same app on 12 AI builders. 7 leaked the database." (a video series)
  2. The monthly "Vibe Coding Index".
  3. "Cheapest builder to ship a SaaS MVP: $14 vs $212."
- SEO: "[builder] vs [builder]" pages across all pairs, and "best AI app builder for [use case]".
- Distribution: builders and their communities share results they win.

**Pricing and willingness-to-pay evidence.**
- Affiliate commissions from builders (programs exist for several; rates unverified).
- $49 detailed reports for founders and agencies.
- $2-5k/year data subscriptions for builder companies and investors.

**Biggest risk.** Monetisation is weak (it's more media than SaaS). Conflict of interest if builders pay. Benchmark maintenance takes real work. A well-known reviewer or Artificial Analysis could launch the same thing.

**Chance 3 / Scale 5.**

---

### #35 WebGame Radar: trend radar for web-game portals
**Pitch.** Tracks new and rising games across Poki, CrazyGames, YouTube Playables, Game Distribution and itch.io (web section), with genre and mechanic tags and estimated plays. Plus a "what to build next" gap analysis for small web-game studios and vibe-coding game makers.

**Audience.** Indie web-game developers and small studios worldwide, a growing group because AI is speeding up production. Poki has more than 100M monthly players ([Poki report](https://poki.com/blog/state-of-web-gaming-report-2026), [Naavik](https://naavik.co/digest/web-gaming-strikes-back/)), and new channels such as YouTube Playables are opening ([Playgama market map](https://wiki.playgama.com/playgama/articles/introducing-the-web-games-industry-market-map-2026)).

**The new problem, and why now.** AI-generated games are flooding the portals, and the portals' own discovery is opaque. Developers need to know which mechanics or memes are rising before they build.

**Current competitors and why they fall short.** The portals' own dashboards (developer-only, for their own games), an Apify scraper, and the Playgama market map. There is no public "SteamDB for web games" (unverified).

**MVP (4-6 weeks).** Collectors for portal listings and ranks (check terms), YouTube Playables catalogue data, a trend score, and genre pages.

**Inbound GTM plan.**
- Posts:
  1. "The 10 fastest-rising web games this week, and the mechanic they share."
  2. "I vibe-coded the #1 trending mechanic in a weekend. Here are its Poki stats." (before/after)
- SEO: "[game] stats", "trending browser games".
- Communities: r/gamedev, r/WebGames, and Discord game jams.

**Pricing and willingness-to-pay evidence.** $9-29/month. But a good portal game typically earns only $200-2,000/month ([Cinevva](https://app.cinevva.com/guides/web-game-monetization)), so willingness to pay is limited.

**Biggest risk.** Low willingness to pay, portals blocking scraping, and a small paying audience.

**Chance 3 / Scale 4.** Included for diversity, and because it's the purest "screenshot the chart" content play. I'd rank it last.

---

## 3. Directions researched and dropped (a reference tool already exists)

| Direction (coordinator list) | Why dropped | Evidence |
|---|---|---|
| Skool community rankings and revenue | skoolstats.com ("#1 intelligence platform for Skool"), RevenueGeeks, an Apify scraper | [skoolstats](https://www.skoolstats.com/), [RevenueGeeks](https://revenuegeeks.com/software/skool/best-communities) |
| Substack/Beehiiv newsletter growth | Newsletter Insights tracks 27k+ newsletters; Substack's official leaderboards; 4+ Apify actors | [Newsletter Insights](https://newsletterinsights.io/), [Substack](https://support.substack.com/hc/en-us/articles/5999320475412-What-are-Substack-leaderboards) |
| Whatnot live-selling analytics | Viewnot, ResellBot, seller Chrome extensions | [Viewnot](https://www.viewnot.com/), [ResellBot](https://resellbot.com/whatnot-seller-tools/) |
| Shopify App Store intelligence | AppstorePulse, StoreCensus, AppJubilee | [AppstorePulse](https://www.appstorepulse.com/), [AppJubilee](https://www.appjubilee.io/shopify-app-store-report-2026) |
| TikTok Shop products | Kalodata, FastMoss, EchoTik | [Kalodata](https://www.kalodata.com/blog/tiktok/top-50-shops-on-tiktok-shop-in-europe-april-2026/) |
| Verified app or startup revenue (RevenueCat-style) | TrustMRR and TrustMRR Mobile (RevenueCat, Superwall) | [TrustMRR RevenueCat](https://trustmrr.com/tech/revenuecat) |
| MCP servers / ChatGPT apps rankings | MCP registries are RED (critic's SAT-14); the ChatGPT app directory (about 2,289 apps) publishes no usage data | [Node8](https://node8.ai/ai-connectors/chatgpt/) |
| Roblox (brand) analytics | ROLearn, GEEIQ, Future Commerce tracker, RoMonitor | [ROLearn](https://rolearn.dev/insights/roblox-analytics-tools-comparison-2026/), [Future Commerce](https://www.futurecommerce.com/posts/roblox-brand-activation-tracker) |
| Hytale servers (new 2026 ecosystem) | 4+ server lists appeared within months | [HytaleServerList](https://hytaleserverlist.me/most-played-hytale-servers), [HytaleTop100](https://hytaletop100.com/hytale-player-count) |
| Prediction-market analytics | 60+ dashboards; Hashdive merged into Unusual Whales | [LaunchPoly](https://launchpoly.com/category/analytics), [Kairos](https://kairos.trade/compare/best-polymarket-tools) |
| Hyrox race analytics | HRP, HyroxDataLab, Rox-Coach, RoxOpt, Race Lab | [HyroxDataLab](https://hyroxdatalab.com/) |
| AI-music (Spotify AI artist) tracker | Deezer's own playlist-scanning tool; SlopTracker | [TechCrunch/Deezer](https://techcrunch.com/2026/07/21/music-streamer-deezer-says-more-than-50-of-daily-uploads-are-ai-generated/), [SlopTracker](https://sloptracker.org/) |
| YouTube sponsorship databases | MeetSponsors, GetYourSponsor, Sponsorship.so, SponsorRadar, SponsorTrace | [vidIQ list](https://vidiq.com/blog/post/companies-matching-youtubers-with-brand-deals/) |
| ChatGPT-ads intelligence | Adthena, Otterly, SE Ranking, AdIntel, GrowByData | [Adthena](https://www.adthena.com/resources/blog/chatgpt-ad-tracking/) |
| Podcast charts and data | Rephonic (YouTube podcast charts), Podscan, Podchaser | [Rephonic](https://rephonic.com/charts/youtube) |
| Competitor changelog monitoring | Many Apify actors, Adversa, Visualping (SherlockWatch #30 is the differentiated angle) | [Apify](https://apify.com/runtime/saas-changelog-product-updates-monitor) |
| "Is this AI tool safe" ratings | Nudge Security publishes 175k+ public SaaS/AI security profiles, including training-data use | [Nudge](https://security-profiles.nudgesecurity.com/) |
| Indie app-idea databases | NichesHunter, BigIdeasDB, AppOpportunity, plus Appfigures and AppMagic | [NichesHunter](https://nicheshunter.app/blog/profitable-app-niches-2026) |
| AI-coding tool market share | Many survey reports (JetBrains, IdeaPlan) plus OpenRouter's public rankings | [JetBrains](https://blog.jetbrains.com/research/2026/08/ai-coding-agent-adoption-2026/) |
| Chrome extensions, Steam, Etsy/POD, faceless YouTube | chrome-stats, SteamDB/Gamalytic, eRank/EverBee, NexLev/Viewstats [MEMORY, not re-verified this session] | none |

## 4. What I'd verify next
1. **Terms and scraping rules:** MakerWorld, Printables, Etsy Open API rules (#26); the micro-drama apps' web top lists (#28); portal terms (#35).
2. **Referral terms:** whether Mercor, Outlier and others allow public referral links on an aggregator site (#27).
3. **Competitor depth:** what ReelPulse actually offers (#28, site blocked for me) and whether Push My App has a preflight product (#32).
4. **Legal risk for BotCheck (#29):** automated chats with third-party bots, and publishing scores (methodology and right of reply).
5. **Connectors for CreatorProof (#31):** which read-only APIs Whop, Gumroad and Kajabi offer.
