# 05 — Critic Verdicts (Round 5): new candidates #38-#43

**Author:** CRITIC · **Date:** 2026-09-25
**Inputs:** `04-defender-new-candidates.md`, the brief, and my files 01-04.

**Standard:** the same as Round 4. Criterion 2 means no *dominant* solution. Competition is fatal only under:
- **(a)** a dominant or funded player, a free official tool, or the platform itself already serves this audience;
- **(b)** ≥5 near-identical tools;
- **(c)** a big platform has shipped or announced the feature.

**Verdict labels:**
- **VALID** = passes all 8 criteria, and comes with a 2-week, no-cold-outreach experiment.
- **WOUNDED** = one precise open condition.
- **KILL** = fatal.

---

## 1. Summary

| # | Idea | Verdict | **Critic C/S** | Decisive point |
|---|---|---|---|---|
| 38 | CompanionSafe (SB 243 / chatbot-law kit) | **WOUNDED** | **3/5** | No kit exists and the laws keep multiplying. But the crisis layer is already served by **ThroughLine** (used by OpenAI, Google, Pinterest) and **Koko's free nonprofit APIs**. There are no SB 243 lawsuits yet, and life-safety liability is heavy for a solo student. |
| 39 (+43) | KnockoffWatch → "AuthorRadar" (with ShelfShift as the free hook) | **WOUNDED** | **3/4** | Strong pain and content, no dedicated tool. **But the Creators API is licensed only for apps that drive Amazon sales**, so it can't be used for monitoring. Keepa's terms for a customer-facing alert service are unconfirmed. |
| 40 | TakedownDesk (TIDA/DSA/OSA/DMCA inbox) | **WOUNDED** | **2/4** | No self-serve tool exists, but willingness to pay is weak. FTC attention is on big platforms (letters to Alphabet, Amazon, Apple, Automattic, Discord…), and hosts like Discourse and Automattic can ship forms natively. Only AI image apps look like real buyers. |
| 41 | LabelCheck (creator-side ad/AI label check, EU) | **VALID (conditional)** | **3/5** | No creator-side checker was found in DE or FR, only brand-side, FTC-centric tools. Enforcement is ongoing (Wettbewerbszentrale, DGCCRF, AI Act Art. 50). The content fit is excellent, and EU + UK/US gives a path. |
| 42 | InboxShift (Kit/Ghost click benchmark) | **WOUNDED** | **2/4** | The same engine as #37, with a weaker "why now" and high risk that the email providers do it themselves (Kit and beehiiv hold all the data). Run it only as #37's second vertical. |
| 43 | ShelfShift (KDP sales benchmark) | **Merge into #39** (no standalone verdict) | 2/4 alone | A good viral hook (the Ferriss moment), but uploads add friction and ScribeCount holds the data. It only makes sense as AuthorRadar's free front door. |

**Spot-checks of the defender's rejected directions:** all confirmed, with one caveat on wording (§3).

---

## 2. Verdicts in detail

### #38 CompanionSafe: **WOUNDED. Chance 3 / Scale 5**
**What holds**
- The law stack is real and growing:
  - CA SB 243 has been in force since 1 Jan 2026, with a private right of action and ≥$1,000 per violation ([Skadden](https://www.skadden.com/insights/publications/2025/10/new-california-companion-chatbot-law));
  - New York's companion safeguard law;
  - Oregon SB 1546 and Washington HB 2225 from 1 Jan 2027;
  - AI Act Art. 50 since 2 Aug 2026.
- **Federal preemption is not a threat.** The Dec 2025 executive order **excludes state child-safety AI laws** from preemption, and the DOJ AI Litigation Task Force had filed no suits as of mid-2026 ([Paul Hastings](https://www.paulhastings.com/insights/client-alerts/president-trump-signs-executive-order-challenging-state-ai-laws), [Ropes & Gray](https://www.ropesgray.com/en/insights/alerts/2026/03/examining-the-landscape-and-limitations-of-the-federal-push-to-override-state-ai-regulation)).
- My searches also found **no third-party SB 243 compliance kit**. Law-firm guides tell operators to build it themselves.

**Attacks**
1. **The hardest component is already served by others.**
   - **ThroughLine** runs a verified helpline network across 170+ countries and is "trusted by OpenAI, Google, and Pinterest" ([ThroughLine](https://www.throughlinecare.com/)).
   - **Koko**, a nonprofit, offers a **free** Suicide Prevention Toolkit: a Keywords API plus a Crisis Helplines API by country. Character.AI partnered with both ([Koko](https://platform.kokocares.org/), [GitHub profile](https://github.com/api-evangelist/koko)).
   - Model vendors ship self-harm moderation for free.
   - Under rule (a), the *crisis referral and detection* layer is served. What's left is disclosure timers, a protocol page, logs and the report export: useful, but thin.
2. **No enforcement signal yet.** I found no SB 243 lawsuit filed. The defender flags the same.
3. **Liability and customer quality.**
   - A solo student selling "suicidal-ideation detection" carries life-safety exposure. Character.AI's litigation shows how these cases name every party in the chain.
   - Many companion apps are NSFW businesses with payment-processor risk.
   - Serious players (Character.AI, Replika) build in-house.

**Precise condition to become VALID:** remove self-built risk detection from scope. Position it as **compliance plumbing** (disclosure/break timers, hosted protocol page, jurisdiction matrix, evidence log, annual-report export) that *integrates* Koko or ThroughLine and the model vendors' moderation. Then show **≥10 revenue-generating AI chat app teams** (tutor, wellness, companion; SFW) on a paid waitlist after launching the free protocol-page generator.

**Better packaging:** merge with #40's buyers into one **"compliance kit for indie consumer-AI apps"** (SB 243/NY/OR/WA + TIDA + Art. 50). The same buyer gets more reasons to pay.

---

### #39 KnockoffWatch (+ #43 ShelfShift as the free hook) → **AuthorRadar: WOUNDED. Chance 3 / Scale 4**
**What holds**
- The pain is current and public: Rolling Stone, the Authors Guild, and **Fortune on 14 Sep 2026** ("thousands of AI slop books flood online marketplaces").
- Authors Guild reports cover fake books sold under real authors' names ([Fortune](https://fortune.com/2026/09/14/ai-slop-books-amazon-marketplace-publishing-human-authors/), [Authors Guild](https://authorsguild.org/news/ai-driving-new-surge-of-sham-books-on-amazon/)).
- Amazon still acts **only on reports**, plus KDP's AI-disclosure rule. No platform feature exists (rule (c) not met), and I found no dedicated monitor.
- #43's "Ferriss −80%" hook is superb content.

**Attacks**
1. **The "licensed data" claim is weaker than presented.**
   - The **Creators API terms say applications "should direct sales to Amazon… Applications that do not have this purpose… will be blocked"**, and access pauses if qualifying sales drop ([Amazon Creators API docs](https://affiliate-program.amazon.com/creatorsapi/docs/en-us/concepts/best-programming-practices)). A knockoff monitor is not a sales-driving app, so **the Creators API is out**.
   - That leaves **Keepa**: API from €49/month for 20 tokens/minute ([RevenueGeeks](https://revenuegeeks.com/software/keepa/api)). Its terms for serving alerts to paying third parties are **not public or confirmed**.
2. **Willingness to pay is concentrated.** Knockoffs cluster around bestsellers and launches. Most indie authors will rarely be hit, and $9/month buyers churn once a launch is over.
3. **Public tracker risk.** A "knockoff tracker" naming listings needs neutral, factual framing (defamation and Amazon's terms).

**Precise condition to become VALID:** **written confirmation from Keepa** (or another licensed source) that a paid, customer-facing alerting service using its API is permitted, plus a token budget showing ≤20% of revenue at 500 monitored titles. If that holds, AuthorRadar (a free ShelfShift benchmark and knockoff scan → $9-29 monitoring) is a good content-led product for a global author audience.

---

### #40 TakedownDesk: **WOUNDED. Chance 2 / Scale 4**
**What holds**
- TIDA has been enforceable since 19 May 2026, with penalties up to $53,088 per violation ([FTC](https://www.ftc.gov/news-events/news/press-releases/2026/05/ftc-begins-enforcing-take-it-down-act)). Size doesn't exempt a platform.
- DSA Art. 16 notice-and-action applies to hosting services of all sizes.
- No self-serve multi-regime inbox was found. The enterprise tools (Tremau, Checkstep, Cinder) are sales-led.

**Attacks**
1. **The FTC is looking at big platforms.** Its pre-deadline letters went to Alphabet, Amazon, Apple, **Automattic**, Bumble, **Discord**, Match, Meta, Microsoft, Pinterest, Reddit, SmugMug, Snap, TikTok and X ([WilmerHale](https://www.wilmerhale.com/en/insights/client-alerts/20260615-the-take-it-down-act-goes-live)). Communities hosted *on* those platforms (Discord servers, WordPress.com, Reddit) are covered by the platform. Self-hosted forums face low enforcement risk.
2. **Platform risk for the plugin channel.** Discourse and Automattic are the natural places for a native TIDA/DSA report form (rule (c) risk; not shipped yet).
3. **Hobby forums have no budget.** The only buyers with money and exposure are **AI image/video apps with public galleries**, and a large share of them are NSFW businesses.

**Precise condition to become VALID:** narrow the product to **AI image/video generator apps**, ideally bundled with #38. Using public pages only, publish the defender's own audit of 100 such apps and show **≥10 SFW revenue-generating apps** joining a paid waitlist.

---

### #41 LabelCheck: **VALID (conditional). Chance 3 / Scale 5**
**What I verified**
- **No creator-side checker exists.** German searches turn up law-firm and guide content plus brand-side vetting tools. French searches find only law firms and agency guides.
- The US tools (CreatorScore, AuditSocials) are brand-side and FTC-centric. That's 2 small, off-audience tools, so neither (a) nor (b) applies.
- **The platforms' own paid-partnership toggles are explicitly "not sufficient"** in France, where "#Publicité / collaboration commerciale" is still required ([Village de la Justice](https://www.village-justice.com/articles/collaboration-commerciale-sur-internet-reseaux-sociaux-qui-change-2026-comment,55776.html), [Affilae](https://affilae.com/fr/loi-influenceurs-reseaux-sociaux/)). They are likewise insufficient in Germany, where the label must appear up front and even without direct payment (OLG Karlsruhe 2026 per [urheberrecht.de](https://www.urheberrecht.de/instagram-influencer/)).
- **A second layer arrived on 2 Aug 2026**: the AI Act Art. 50 deepfake/AI-image labels, plus France's "Image retouchée/virtuelle" labels.
- **Joint liability in France** (Art. 8: advertiser, agency and influencer) gives **agencies a budget reason to pay**.

**Why it fits the founder:**
- The content is native: "I scanned my 200 posts", country cheat sheets.
- It's multi-country EU with a UK/US FTC edition as the path, so geography is justified by country-specific rules.
- The Canva app is an inbound channel.
- It's a thin wrapper (OCR + LLM + rule packs).

**Residual risks:**
- creators pay only after an Abmahnung, so **agencies** are the real buyers;
- Meta and TikTok app review for OAuth access (weeks of delay);
- false positives;
- RDG: keep it a checker with fixed rules, per the logic of BGH *Smartlaw*.

**Biggest risk to test first: will creators or agencies pay *before* an enforcement hit?** (Plus: sidestep the platform app-review delay.)

**2-week experiment (no OAuth needed yet)**
- Ship a **free paste-URL/screenshot checker**: OCR of the caption and thumbnail, an LLM classifier for commercial signals, and DE/FR/IT/ES/UK rule packs.
- Publish the "Werbung vs Anzeige vs Publicité vs #ad vs AI label" cheat sheet as carousel and Reel formats.
- Post 6 creator-style videos of the founder scanning public example posts (their own, or with consent).
- Put a €9 creator plan and a **€49 agency plan** on a pre-sale page.
- **Pass:** ≥500 free checks, ≥20 creator pre-sales **or** ≥5 agency pre-sales, and ≥1 inbound agency white-label request.
- **Fail:** fewer than 5 total pre-sales. Then pivot to an agency-only audit product (a campaign pre-flight checker).

---

### #42 InboxShift: **WOUNDED. Chance 2 / Scale 4**
**What holds**
- Clicks versus opens really are shifting with AI inbox summaries.
- newsletterbenchmark.com uses manual entry, and beehiiv publishes annual benchmark reports ([beehiiv](https://www.beehiiv.com/blog/the-state-of-paid-newsletters-2026), [Newsletter Benchmark](https://newsletterbenchmark.com/)). No pooled "connect your account" peer benchmark exists.
- The Kit App Store is a genuine inbound channel.

**Attacks**
1. **The email providers own the pooled data.** Kit publishes creator-wide averages (open rate 44%, click-through 3.7%) ([Kit](https://kit.com/resources/blog/email-marketing-stats)), and beehiiv has platform-wide data and a benchmark report habit. A native "how you compare to similar newsletters" panel is a small release for either of them. Not announced, so not fatal, but it's the highest-probability platform move in this batch.
2. **Low willingness to pay** among small newsletter creators ($9). Agencies are few.
3. **Cold start**, duplicated with #37: two separate pools to fill.

**Precise condition:** run it **only as the second vertical of #37's engine**, after #37's 2-week connection test passes (≥400 connected sites), and after the Kit App Store listing is approved.

---

### #43 ShelfShift: **merged into #39** (standalone 2/4)
The content hook is strong. But uploads add friction, **ScribeCount** already holds cross-platform royalty data and could add benchmarks, and willingness to pay is low. As AuthorRadar's free front door it adds value, so it is judged inside #39.

---

## 3. Spot-checks of the defender's rejected directions

| Direction | Defender's reason | My check | Result |
|---|---|---|---|
| Video-creator likeness/deepfake | YouTube shipped it | YouTube expanded likeness detection to **all creators 18+** from 18-19 May 2026 ([MediaPost](https://www.mediapost.com/publications/article/415170/youtube-rolls-out-likeness-detection-to-all-creato.html), [Social Media Today](https://www.socialmediatoday.com/news/youtube-expands-likeness-detection-to-all-users-over-18/820440/)) | **Confirmed** (rule c) |
| Musician impersonation | Spotify shipped it | Spotify **Artist Profile Protection** beta, 24 Mar 2026 ([Billboard](https://www.billboard.com/pro/spotify-artist-profile-protection-stop-incorrect-uploads/), [Spotify](https://artists.spotify.com/blog/introducing-artist-profile-protection)) | **Confirmed** (rule c) |
| Fake-review extension after Fakespot | 5+ clones | FakeFind, NullFake, RateBud, SureVett, SeekShop, Review Radar and TraceFuse all position as replacements ([RateBud](https://www.ratebud.ai/blog/fakespot-shutting-down-best-alternatives-2026), [SureVett](https://surevett.com/blog/fakespot-alternatives-2026)) | **Confirmed** (rule b) |
| Etsy shop benchmark | "5+ analytics tools (eRank, EverBee, Alura, Marmalead)" | **The reasoning is imprecise.** Those are keyword and competitor-estimate tools, not pooled first-party peer benchmarks. The conclusion probably still holds on other grounds (Etsy's own Marketplace Insights and shop stats, Etsy API commercial-access review, low willingness to pay), but that's **unverified**. | Conclusion likely right, reason wrong; don't cite it as a rule-(b) kill |

I found no rejection that is clearly wrong.

---

## 4. Updated VALID tally (all ideas)

| Status | Ideas | Count |
|---|---|---|
| **VALID** | #2 "Wen empfiehlt die KI?" (5/7) · #7 LeanKeep (4/5) · #9 Nachfolge Weekly (4/4) · #20 HireLaw Check (3/6) · #12 PSTI+CRA Kit (3/6) · #37 SearchShift (3/5) · **#41 LabelCheck (3/5)** | **7** |
| **WOUNDED** (one precise condition) | #30+34 founder media · #36 SafetyRadar (both pending defender work) · **#38 CompanionSafe** · **#39+43 AuthorRadar** · **#40 TakedownDesk** · **#42 InboxShift** | 6 |
| Parked | #8 Zitat-Check | 1 |
| KILL / conceded | all others | — |

**7 VALID.** The most plausible upgrades to reach ~9-10:
1. **#38 + #40 merged** into a compliance kit for indie consumer-AI apps, if the waitlist condition is met.
2. **#39+43 AuthorRadar**, if Keepa confirms the licence.
3. **#36**, if the US-first and precision conditions are met.
4. **#30+34**, if the audience gate is met.

#42 depends on #37 and shouldn't be counted separately until #37's flywheel is proven.
