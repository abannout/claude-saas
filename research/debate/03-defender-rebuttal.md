# Round 3 (Defender): rebuttal to `02-critic-attack.md` and `03-critic-additions-attack.md`, plus pipeline top-up

Author: DEFENDER, 2026-09-25.

Founder rules applied: inbound only; success chance and scale first; thin wrappers are fine; global by default (DACH-only must be justified).

## 0. Calibration first
I accept the critic's main charge: **my round-1 competitor searches stopped too early.** In this round I re-checked every claim I defend, using:
- `site:`-filtered searches of the Shopify App Store, WordPress.org and the Chrome Web Store (direct fetches of apps.shopify.com were blocked by the proxy);
- Product-Hunt-style and Google "[idea] tool / app" queries;
- GitHub and Apify results where they showed up.

I use the critic's scores as the baseline and move a score only where I have new, sourced evidence.

**Decisions at a glance**

| # | Idea | Critic verdict (C/S) | My decision | New C/S |
|---|---|---|---|---|
| 2 | "Wen empfiehlt die KI?" (local AI-recommendation index) | Survives, conditional (5/7) | **DEFEND** (all 3 conditions accepted, plus new evidence) | **5/7** |
| 20 | Pay-Range Kit → **HireLaw Check** (multi-jurisdiction job-ad compliance) | Wounded (2/5) | **PIVOT (global), with new evidence** | **4/6** |
| 12 | CRA Index → **PSTI + CRA Kit and Security-Support Index** | Wounded (3/6) | **PIVOT (global)** | **3/6** |
| 7 | GLP-1 gym kit → **LeanKeep** (muscle-retention kit for coaches) | Wounded (4/5) | **PIVOT (global)** | **4/5** |
| 9 | Nachfolge-Radar → **sponsor-funded weekly digest** | Wounded (4/4) | **PIVOT (critic's conditions)** | **4/4** |
| 29 | BotCheck → **Shopify Support-Bot QA** plus a small public leaderboard | Wounded (3/6) | **PIVOT (critic's conditions)** | **3/6** |
| 30 + 34 | SherlockWatch + BuilderBench → **one founder-media brand** | Wounded (3/4, 3/5) | **MERGE and PIVOT to media, with SaaS add-ons** | **3/5** |
| 1 | LaunchGuard | Wounded (4/6) | **CONCEDE** | — |
| 3 | Netzbetreiber-Radar | Wounded (3/3) | **CONCEDE** | — |
| 4 | Pflegebudget | Wounded (3/3) | **CONCEDE** | — |
| 6 | MiSpeL optimizer | Wounded (3/5) | **CONCEDE** | — |
| 8 | Zitat-Check | Wounded (3/3) | **CONCEDE** (park) | — |
| 26 | PrintRadar | Wounded (3/4) | **CONCEDE** | — |
| 5, 10, 11, 13-19, 21-25 | round-1 kills | KILL | **ACCEPT** (no contest) | — |
| 27, 28, 31, 32, 33, 35 | round-2b kills | KILL | **ACCEPT** (no contest) | — |
| 36 | **SafetyRadar** (NEW): recall and safety-alert matching for shop catalogues | — | NEW | **3/5** |
| 37 | **SearchShift** (NEW): connect Search Console for a peer traffic benchmark and index | — | NEW | **3/5** |

I checked 18 further new-idea candidates and dropped them because incumbents exist (§5). **I propose 2 new ideas instead of 6-10, rather than pad the list.**

---

## 1. Conditional survivor

### #2 "Wen empfiehlt die KI?": DEFEND (C5/S7)
**I accept all three binding conditions:**
1. **Non-medical verticals first**: trades, restaurants, Steuerberater, fitness studios and hairdressers. No Heilberufe until a lawyer has reviewed the Jameda risk.
2. **A strictly neutral index**: no paid boosts; the same data for everyone; a published methodology (share of mentions over N=10 runs per prompt); a correction and opt-out process. The monitor is sold as a separate product.
3. **Position on German-language prompts and a DACH agency white-label, not on price.**

**New evidence**
- **The public index is still unoccupied.** A search for "according to ChatGPT best [dentist/plumber] [city]" returns only agencies and playbooks (Local Vitals, Scope, Lead Local SEO, DemandConvert), no public city × profession ranking ([Local Vitals](https://getlocalvitals.com/plumbers), [Scope](https://scope.online/for/local-businesses), [Lead Local SEO](https://leadlocalseo.com/blog/how-to-get-recommended-by-chatgpt/)). The monitor layer is crowded; the reference index is not.
- **The timing hook got stronger.** OpenAI started showing **ads in ChatGPT in Germany, Austria and Switzerland on 24 Aug 2026** ([advantago](https://www.advantago.com/en/academy/blog/chatgpt-ads-germany-ai-visibility-organic/), [BeeDynamic](https://beedynamic.io/chatgpt-ads-dach-switzerland-germany-austria/)). DACH SMBs now have a reason to ask "does ChatGPT recommend me?".
- **The methodology can approximate local consumer results.** OpenAI's web_search tool accepts `user_location` with city, region and country ([OpenAI docs](https://developers.openai.com/api/docs/guides/tools-web-search)). Each prompt runs city-localised with web search on, which answers the critic's "API ≠ consumer ChatGPT" point in part.
- **An honest concession:** Local Falcon "supports … all languages" ([Capterra UK](https://www.capterra.co.uk/software/1060015/local-falcon)). German *language* alone is not the moat. The moat is:
  - the **public German-language index** (content + SEO);
  - **DACH directories** (Das Örtliche, ProvenExpert, Gelbe Seiten) in the fix-list;
  - an **agency white-label** in German.

**Strengthened with the critic's "connect your own account" pattern:** the free hook becomes *"Verbinde dein Google-Unternehmensprofil"*. It connects the owner's own Google Business Profile via OAuth (legal, first-party data) and returns an AI-visibility result plus a review-velocity percentile versus peers. The output is a **share card** ("Top 10% Friseure in Köln bei ChatGPT & Google"). Businesses post these proudly, and each card is a viral loop.

**Geography.** DACH-first is justified because the English monitor market is crowded (Local Falcon, Semrush, Yext) while no German public index exists. **Expansion path:** the same engine with local-language prompt libraries and directories: DE → AT/CH → FR/ES/IT/NL/PL editions → an English grid (UK/IE/AU) last. Scale 7 holds.

**Chance 5 / Scale 7.**

---

## 2. Wounded round-1 ideas

### #20 → **HireLaw Check**: multi-jurisdiction job-ad compliance checker. PIVOT (C4/S6)
The critic's condition: *show that the US state-law checkers are missing or enterprise-only, and give a Chrome-extension or ATS-marketplace plan.* Both are met.

**Audience.** Global and English-first:
- US employers with 50-1,000 staff who post in several states;
- staffing agencies and recruiters (US and Canada);
- later, EU employers as countries transpose the directive.

Listing 100 is easy from public ATS job boards and staffing-association directories.

**Why now (new evidence)**
- **Washington litigation wave.** About **700 class actions filed in 2025-26 by six firms**, 272 of them by Justice Law Corporation in H1 2026 alone ([Davis Wright Tremaine](https://www.dwt.com/blogs/employment-labor-and-benefits/2026/08/washington-employment-class-action-surge)). The WA Supreme Court ruled that *any* applicant can sue, with no good-faith requirement ([Fisher Phillips](https://www.fisherphillips.com/en/insights/insights/washington-supreme-court-allows-any-job-applicant-to-sue-under-pay-transparency-statute), [NatLawReview](https://natlawreview.com/article/washington-state-supreme-court-broadly-defines-job-applicants-covered-pay)). Statutory damages are **$100-5,000 per violation**.
- **Real settlements:**
  - Target $2.225M ([TopClassActions](https://topclassactions.com/lawsuit-settlements/closed-settlements/2-225m-target-wage-transparency-class-action-settlement/))
  - Talkdesk up to $2.79M ([ClaimDepot](https://www.claimdepot.com/settlements/epoa-settlement-tdi))
  - Concentric $2.476M ([theclassactionlawsuit](https://www.theclassactionlawsuit.com/settlement/concentric-pay-transparency-settlement/))
  - Jiffy Lube $1.18M ([OpenClassActions](https://openclassactions.com/settlements/jiffy-lube-washington-pay-transparency-class-action-settlement.php))
  - Total employer liability was about **half a billion dollars by Aug 2024** (aggregate figure from a search summary; unverified).
- **Ontario since 1 Jan 2026:** employers with 25+ staff must post pay ranges (spread ≤ $50k) and disclose AI use in screening ([Littler](https://www.littler.com/news-analysis/asap/canada-new-ontario-job-posting-requirements-force-january-1-2026)).
- **The US has 16+ states plus DC** with posting rules ([TheComplyGuide](https://thecomplyguide.com/pay-transparency-laws-by-state-2026-map/)).
- **The EU** had 5 transposed states by Sept 2026, with NL and DE expected in 2027 ([Trusaic](https://trusaic.com/blog/eu-pay-transparency-directive-august-2026-transposition-update/)).

**Competitors: all enterprise-only (verified)**
- **Datapeople** from about $5k/year, **acquired by PayScale** ([Ongig blog](https://blog.ongig.com/hr-content/why-payscale-bought-datapeople/), [Datapeople pricing](https://datapeople.io/pricing/)).
- **Ongig** $17,900-219,000/year; **Textio** custom enterprise pricing ([Ongig](https://blog.ongig.com/job-descriptions/textio-competitors/)).
- **SixFifty** builds policies, not ad checks ([SixFifty](https://www.sixfifty.com/blog/pay-transparency-policy-builder/)).
- An **Apify actor** is a developer data tool ([Apify](https://apify.com/mahender_sam/pay-transparency-checker)).
- **Chrome Web Store:** only *salary estimators* for job seekers (PayPeek, Salary Inspector, Salary Seeker). **No recruiter-side compliance checker found** ([CWS search](https://chromewebstore.google.com/detail/paypeek-instant-salary-ch/aenhepbomobiielgagkkaagkbjaljobj)).
- The gap: SMBs and agencies with more than 10 postings a month have no self-serve tool.

**MVP (6-7 weeks)**
- A rules engine by jurisdiction: 16 US states + DC, BC and ON, and EU countries as they transpose.
- A paste or URL checker.
- A **Chrome extension** that flags problems inside LinkedIn, Indeed and ATS job editors (Greenhouse, Lever, Workable, Ashby): missing or invalid range, benefits line, AI-use disclosure (ON), vacancy disclosure (ON).
- A bulk scan of a company's **public ATS job board**. Greenhouse, Lever and Ashby publish JSON board endpoints intended for embedding, so no job-board scraping is needed.
- A "Pay-Transparent Employer" badge for careers pages.

**Inbound GTM plan**
- Posts:
  1. "We scanned 20,000 job ads on public ATS boards of Washington employers. 11% had no range, the exact issue behind 700 lawsuits." (aggregate only, no naming)
  2. "Ontario's new job-ad rules: the 5 lines your posting must contain since 1 Jan."
  3. A monthly "Pay Transparency Index by state".
- SEO: programmatic "pay transparency law [state/province/country]" and "job posting salary range requirements [X]" pages (40+).
- Marketplaces: Chrome Web Store, plus the Greenhouse, Lever and Workable partner directories.
- Viral loop: the badge on careers pages links back.

**Pricing.** Free single-ad check; $49/month SMB (up to 50 live postings); $149/month for staffing agencies. One WA violation costs up to $5,000 *per applicant*.

**Biggest risk.**
- ATS vendors add native validation.
- The legal-information boundary (disclaimers; no individual advice).
- Upkeep of the rules engine.
- Plaintiff firms may use the tool too (not a business risk).

**Chance 4 / Scale 6.** I'm moving Chance from the critic's 2 to 4 because the pain is litigation-driven and acute, the incumbents are enterprise-only, and there are two inbound stores.

---

### #12 → **PSTI + CRA Kit and Security-Support Index**. PIVOT (C3/S6)
This meets the critic's conditions: English-first and global; a free lead magnet now for the 2027 CRA wave; UK PSTI as today's driver.

**Audience.**
- Small connected-product brands selling into the UK/EU from anywhere: smart home, pet and baby tech, wearables, e-bike apps, Kickstarter hardware, Shenzhen OEM sellers on Amazon.
- UK distributors and retailers, who also have duties under PSTI.

**Why now**
- **PSTI has applied since 29 Apr 2024.** Every in-scope product needs a statement of compliance, a vulnerability-disclosure policy and a **published, defined support period**, with fines of up to £10M or 4% ([techUK](https://www.techuk.org/resource/the-psti-act-for-consumer-iot-explained.html), [QIMA](https://blog.qima.com/eletronics/guide-to-uk-psti-statement-of-compliance)).
- Which? found big brands failing to deliver ([Which?](https://www.which.co.uk/news/article/how-long-will-your-smart-products-last-big-brands-fail-to-deliver-on-new-security-laws-atIYq4m4VP09)).
- **There is no central support-period database.** Consumers are told to search "model + PSTI statement" to find PDFs ([secureiot.house](https://secureiot.house/smart-device-security-support-window-buying-guide-2026/)). Those PDFs are public (e.g., [TP-Link](https://www.tp-link.com/uk/support/psti/), [GL.iNet](https://www.gl-inet.com/en-us/pages/psti)), which makes a legal index possible.
- **CRA** reporting has been live since 11 Sep 2026, and full obligations start 11 Dec 2027.
- **The US Cyber Trust Mark has stalled:** UL withdrew in Dec 2025, ioXt became lead administrator on 13 Apr 2026, and applications aren't open yet ([Nextgov](https://www.nextgov.com/cybersecurity/2026/01/ul-solutions-withdraws-lead-admin-fcc-cyber-label-program-amid-probe-china-ties/410448/), [Cybersecurity Dive](https://www.cybersecuritydive.com/news/fcc-cyber-trust-mark-new-lead-administrator/817437/)). It's a later add-on, not a driver.

**Competitors (checked)**
- Test labs and consultancies (TÜV SÜD, QIMA, 360 Compliance).
- Enterprise disclosure programmes (HackerOne, Intigriti) and free open-source MyOpenVDP.
- Enterprise product security (ONEKEY, Cybellum, Finite State).
- **No self-serve PSTI statement generator** found ([search](https://www.tuvsud.com/en/industries/consumer-products-and-retail/uk-psti)), and **no Shopify app** for PSTI support-period badges in a `site:apps.shopify.com` search.

**MVP (6 weeks)**
- A PSTI statement generator per SKU.
- A hosted disclosure (VDP) page plus security.txt.
- A **"Security updates until 2030" badge** for Shopify, as an embeddable widget and as an Amazon image.
- A CRA readiness checklist and ENISA report templates.
- A **public Security-Support Index** that crawls *published* PSTI statements and links to the sources.

**Inbound GTM plan**
- Posts:
  1. "Your smart doorbell stops getting security updates in 2027. We indexed 1,000 PSTI statements."
  2. "The 20 brands with the longest security support."
  3. "Kickstarter hardware: the 3 documents you need before shipping to the UK."
- SEO: programmatic "[brand] [model] security updates until" pages, "PSTI statement of compliance template", "CRA checklist small manufacturer".
- Channels: the Shopify App Store; the consumer index gets press pickup (Which?-type outlets).

**Pricing.** Free for one SKU; $29/month for up to 20 SKUs plus VDP hosting; $99/month for the CRA pack.

**Biggest risk.** Thin PSTI enforcement means low urgency until the CRA deadline in Dec 2027.

**Chance 3 / Scale 6.** I agree with the critic's score. This is a slow-burn SEO asset positioned for the 2027 buying wave.

---

### #7 → **LeanKeep**: muscle-retention kit for coaches. PIVOT (C4/S5)
**Audience.** English-first, global:
- personal trainers and online coaches whose clients lose weight fast (on GLP-1 medication or otherwise);
- gyms as an upsell.

**Why now**
- Certification bodies are training coaches for exactly this client:
  - **NASM "Understanding Weight Loss Medications"**, updated June 2026 ([NASM](https://www.nasm.org/products/understanding-weight-loss-medications));
  - **ISSA's GLP-1 Weight Loss Support** certification ([ISSA](https://www.issaonline.com/certification/glp-1-weight-loss));
  - Health Coach Institute's course.
- At least **17 fitness clubs had launched GLP-1 programs by early 2026**, including Equinox (search summary; exact source unverified, see [3DLOOK roundup](https://3dlook.ai/content-hub/top-7-remote-body-composition-tools-glp-1-clinics/)).
- Up to 40% of the weight lost can be muscle.

**Competitors (checked)**
- **Trainerize, Everfit and TrueCoach:** comparison reviews list no GLP-1-specific features ([Everfit review](https://blog.everfit.io/everfit-vs-trainerize-vs-truecoach), [FitBudd](https://www.fitbudd.com/insights/everfit-vs-trainerize-vs-truecoach)).
- CoachingPortal is a generic white-label ([Capterra](https://www.capterra.com/p/10038189/CoachingPortal/)).
- FitXpress is a body-scan API for clinics.
- Omada serves health plans and employers.
- Consumer trackers (critic's SAT-12) are B2C.
- **The gap is coach-side**: templates, check-ins and a proof metric.

**MVP (5-6 weeks)**
- 12-week strength-and-protein program templates.
- A client PWA for check-ins (weight, waist, photos, optional InBody/Tanita/Withings import).
- A **Muscle Retention Score** (share of lean mass kept, or a proxy).
- Opt-in, branded result cards; a coach dashboard; CSV export to Trainerize and Everfit.
- **The drug log is dropped** (critic condition a). Only a neutral "rapid weight loss" flag remains.

**Inbound GTM plan**
- Posts:
  1. "Lost 14 kg, kept 91% of her muscle: the 12-week plan." (a coach case study)
  2. "Coaches: the one metric that proves you're not just a weight-loss app."
  3. An opt-in "Muscle Retention Leaderboard" of coaches.
- SEO: "how to coach GLP-1 clients", "training plan rapid weight loss muscle", "muscle retention score".
- Channels: coach Facebook groups, r/personaltraining, and continuing-education partnerships (inbound).
- Viral loop: every client card carries the coach's and LeanKeep's branding.

**Pricing.** $29/month for up to 15 clients; $79/month unlimited; gyms $5 per client.

**Biggest risk.**
- Coaching platforms ship GLP-1 templates.
- Coaches' willingness to pay on top of Trainerize.
- Drug-advertising rules (so no drug names in ads).
- Still unmet: the critic's condition b (5-10 coach interviews) is an action item I haven't done.

**Chance 4 / Scale 5.**

---

### #9 → **Nachfolge-Radar Weekly**: sponsor-funded, link-don't-copy digest. PIVOT (C4/S4)
All three critic conditions are met:
- **(a) Newsletter plus sponsors.** Sponsors are M&A advisors, Sparkassen and Volksbanken, succession financiers, lawyers and valuation firms. Pro alerts cost €19-49/month.
- **(b) Link, don't copy.** 2-3 line original summaries plus an outbound link, and **free seller-first listings**, so there's no database extraction (§87b UrhG).
- **(c) Expansion:** AT/CH → NL → an English "Europe for Sale" edition for international search funders.

**New evidence of the gap.** Existing newsletters are **broker- or portal-specific**:
- KERN sends 12 issues a year about its own mandates ([KERN](https://www.kern-unternehmensnachfolge.com/en/newsletter/));
- Nachfolgekontor covers its own projects ([Nachfolgekontor](https://nachfolgekontor.de/));
- Firmenzukaufen sends a weekly digest of its own portal ([Firmenzukaufen](https://www.firmenzukaufen.de/blog/unternehmen-verkaufen-erfolgreiche-strategien-fr-die-unternehmensnachfolge)).

No neutral cross-portal digest was found.

**Inbound GTM plan.** Posts on LinkedIn/X ("5 profitable German businesses for sale this week, under €500k"), SEO landing pages for "[Branche] kaufen [Region]", and the newsletter itself.

**Biggest risk.** Sponsor demand is unproven, and the pool of paying buyers is small.

**Geography.** DACH is justified (the critic agrees): the English market is saturated and German listings are fragmented.

**Chance 4 / Scale 4.**

---

### Conceded (round 1)
- **#1 LaunchGuard: CONCEDE.** Even the EU-launch angle is taken:
  - [Kukie.io](https://kukie.io/blog/ai-app-builders-gdpr-cookie-banners-audit) publishes cookie-consent audits of AI app builders;
  - CookieCrumbs targets Lovable apps;
  - [howsafeismyapp](https://howsafeismyapp.com/blog/cookie-banner-lovable-app) runs free passive GDPR checks.

  Add the Supabase default change and §202a, and nothing is left to own. The passive "EU launch-readiness" data story can become a segment of the media brand (#30/#34).
- **#3 Netzbetreiber-Radar: CONCEDE.** Germany-only, and done-for-you services (Reonic, Netzanmeldung-Digital, Voltir, Netzio) cover the job.
- **#4 Pflegebudget: CONCEDE.** nui is free via insurers, and an affiliate model isn't SaaS.
- **#6 MiSpeL: CONCEDE.** Hardware API access, and evcc is free.
- **#8 Zitat-Check: CONCEDE and park.** It's Germany-only, and fewer than 5% of decisions are published. It could reopen only if the critic's 100-citation coverage test reaches ≥80%.

---

## 3. Wounded additions (#26-#35)

### #29 → **Shopify Support-Bot QA** plus a small public leaderboard. PIVOT (C3/S6)
This follows both critic conditions: (a) a slow, human-paced leaderboard; (b) a self-serve SMB tier through the **Shopify App Store**.

**Evidence of the gap**
- A `site:apps.shopify.com` search for bot testing and QA returned **no QA app**; only the chatbots themselves appear.
- Tidio Lyro reviews mention "mismatched or irrelevant" answers ([Flyweight](https://flyweight.io/best-ai-chatbot-for-shopify-customer-support-2026)).
- Enterprise QA (Cekura, Maxim, Lorikeet) doesn't sell to Shopify SMBs.

**MVP (6 weeks)**
- Shopify OAuth (read the store's policies and products) plus the merchant's bot widget URL. Testing is **the merchant's own bot, with consent**, so there's no third-party cost issue.
- Auto-generated test questions from the policies (returns, shipping, warranty, discounts).
- A weekly regression run, diffs, and an "AI answers verified weekly" badge.

**Public leaderboard.** 25 brands, 10 harmless questions, monthly. Includes evidence screenshots, a methodology page, a right of reply, and excludes bots billed per resolution.

**Inbound GTM plan**
- Posts: "We asked 25 Shopify brands' AI assistants about their return policy. 6 got it wrong."
- SEO: "test [Tidio/Gorgias] AI accuracy".
- Viral loop: the badge.

**Pricing.** $49-99/month.

**Biggest risk.** Bot vendors add QA themselves; SMB willingness to pay.

**Chance 3 / Scale 6.**

### #30 + #34 → **one founder-media brand** ("Sherlocked" weekly + quarterly "Vibe Coding Index"). MERGE and PIVOT (C3/S5)
Both ideas serve the same audience (indie founders and vibe coders on X, HN and Reddit), so one brand, two franchises:
- **Weekly:** "Sherlocked this week", i.e. platform launches mapped to startup categories.
- **Quarterly:** a lean Vibe Coding Index (3 apps × 6 builders, YouTube-first), meeting the critic's condition (a).

**Revenue**
- Dev-tool sponsors. The TrustMRR sponsor model reached about $44k/month (critic, round 2).
- Builder affiliates: Lovable pays about 20% recurring, up to $100 per subscriber ([OpenAffiliate](https://openaffiliate.dev/programs/lovable)).
- A $9-19/month **platform-risk alert tier**, later an "exposure score" for VCs.

**Gate (critic's condition).** A 6-week test: an X account plus newsletter must reach ≥2k subscribers and 1 paid sponsor. Founder time: about 6 h/week plus one quarterly benchmark sprint.

**Chance 3 / Scale 5.**

### #26 PrintRadar: CONCEDE
The legal-data pivot I would have proposed (seller OAuth → profit per print plus peer benchmark) is already served by **Printago**. It's a "commerce OS" for print farms that turns Shopify, Etsy and TikTok Shop orders into prints and tracks profitability ([Printago](https://printago.io/), [SimplyPrint vs Printago](https://simplyprint.io/alternatives/printago)). MakerWorld's terms forbid the index.

### Accepted kills
**#27, #28, #31, #32, #33, #35.** The critic found incumbents I missed: OpenTrain and aitrainer.work; SocialPeta's 43k-title weekly ranking; TrustMRR's Whop connector plus Whop Trends; Rork's reviewer, AcceptMyApp and AppSmash; marketplaces with built-in view verification; Playgama.

---

## 4. Round-1 kills: ACCEPTED
**#5, 10, 11, 13, 14, 15, 16, 17, 18, 19, 21, 22, 23, 24, 25.** I have no strong new evidence that the critic is factually wrong on any of them. The rebuttals it cited all check out: the VZ NRW free quote check, kostenerstattung-antrag.de, the Shopify EmpCo app, ImmoScout's verified income statements, GitHub PR limits (Feb and Jun 2026), and heatpumpmonitor.org.

---

## 5. Pipeline top-up: two new ideas that passed the checks

### #36 **SafetyRadar**: recall and safety-alert matching for e-commerce catalogues (C3/S5)
**Pitch.** A Shopify/WooCommerce app. It matches your catalogue (titles, brands, GTINs, product types) against **official** recall and alert feeds and alerts you when your product, supplier or product type is flagged:
- US CPSC recalls API
- EU Safety Gate
- UK OPSS
- Australia ACCC
- Health Canada

It also produces a documented action log. A free weekly public **Recall Index** is the content.

**Audience.** Global. Brands and resellers in the highest-risk categories: **cosmetics (36% of EU alerts), toys (16%), electrical (11%)**. They sell on Shopify, Amazon and TikTok Shop, and many are dropshippers sourcing from marketplaces.

**Why now**
- **Safety Gate hit a record 4,671 alerts in 2025 (+13%)**, and Shein and Temu appear "in significant numbers for the first time" ([Euronews](https://www.euronews.com/2026/03/05/record-number-of-dangerous-products-intercepted-by-the-eu-in-2025-safety-report-finds), [EC](https://commission.europa.eu/news-and-media/news/increased-action-against-dangerous-products-eu-2025-2026-03-09_en)).
- Consumer groups found systemic non-compliance on Temu and Shein ([Euroconsumers](https://www.euroconsumers.org/systemic-failures-in-product-compliance-on-temu-and-shein/)).
- In the US, the **CPSC ordered Amazon, as a "distributor", to recall 400,000+ third-party FBA products** (orders of Jul 2024 and Jan 2025; Amazon sued in Mar 2025) ([CPSC](https://www.cpsc.gov/Newsroom/News-Releases/2025/CPSC-Issues-Final-Order-to-Amazon-com-Outlining-Remediation-Plans-for-Hazardous-Products), [NatLawReview](https://natlawreview.com/article/amazon-files-suit-against-cpsc-challenging-cpscs-determination-amazon-distributor)). Marketplaces now push this liability down to sellers.
- **Data is official, public, and free to use.** CPSC has a public recalls API ([CPSC API](https://www.cpsc.gov/Recalls/CPSC-Recalls-Application-Program-Interface-API-Information)). There's no scraping-terms risk (the critic's #1 objection to my round-2 ideas).

**Competitors (checked)**
- **Shopify App Store** (`site:` search): **LotTrack** runs *your own* recalls via lot tracking; **Warnify** shows warning pop-ups. **No external-alert monitoring app found** ([LotTrack](https://apps.shopify.com/lot-track), [Warnify](https://apps.shopify.com/warnify-product-warnings)).
- **Chrome Web Store:** RecallPro, which is consumer-only and CPSC-only ([RecallPro](https://chromewebstore.google.com/detail/recallpro/jdgmnnipocpdpldljkfdbjhcgmpabaoh)).
- **Consumer apps:** Food Recalls & Alerts (about 250k users), Recall Bench, USA Recalls. They serve consumers, not sellers' catalogues ([Recall Bench](https://recallbench.com/)).
- **Apify** CPSC/Safety Gate actors are developer data feeds.
- **Enterprise:** Compliance & Risks, SGS [MEMORY].

**MVP (5-6 weeks)**
- Feed ingestion for 5 jurisdictions.
- Shopify/Woo catalogue sync.
- Brand, model and GTIN matching plus LLM product-type matching.
- An alert inbox, a PDF action log, and weekly public index pages.

**Inbound GTM plan**
- Posts:
  1. "Recalled this week: 9 kids' products still being sold online." (screenshots of *official* notices only)
  2. "Safety Gate set a record: 4,671 alerts. 36% were cosmetics. What sellers keep getting wrong."
  3. "The 10 most-recalled product types this quarter: is your bestseller on it?"
- SEO: programmatic "[product type] recall [year]" and "[brand] recall" pages from official data, plus "GPSR / CPSC seller recall obligations".
- Stores: the Shopify App Store and WooCommerce.com.
- B2C side funnel: free email alerts for parents and pet owners, which builds a list and a sponsor audience.

**Pricing.** Free up to 5 SKUs; $19/month (500 SKUs); $49/month (multi-store, all jurisdictions).

**Biggest risk.**
- Matching errors in both directions.
- Low urgency until something happens to the seller.
- Shopify or a compliance vendor could add it.

**Chance 3 / Scale 5.**

### #37 **SearchShift**: connect Search Console for a peer traffic benchmark and a public index (C3/S5)
**Pitch.** Connect Google Search Console (OAuth, read-only). You see how your clicks, impressions and CTR shifted as AI Overviews and AI Mode spread, **benchmarked against anonymised peers in your niche and country**. You get a **share card** ("We lost 22%; our niche median lost 41%"). A weekly public **Search Traffic Index** by niche is built only from pooled, consented first-party data. This is exactly the critic's "connect your own account → peer benchmark + share card" pattern.

**Audience.** Global, English-first (DE/FR/ES later): bloggers, niche publishers, content-led SaaS teams and SEO agencies.

**Why now**
- AI Overviews appear on **48% of queries (Feb 2026, up from 31% a year earlier)**, and organic CTR falls **34.5-58%** when one is shown ([QuickSEO stats](https://quickseo.ai/blog/google-ai-overviews-statistics-2026-60-data-points-every-seo-should-know); critic's PLAT-09).
- Google's new generative-AI report in Search Console (Jun 2026; global since 31 Aug 2026) **isn't in the API** and shows **no clicks or queries** ([Chudi.dev](https://chudi.dev/blog/search-console-generative-ai-report), [Google](https://developers.google.com/search/blog/2026/06/gen-ai-performance-reports)).
- So publishers still can't answer: "is it me, or is it everyone in my niche?"

**Competitors (checked)**
- Search Console itself (no peer comparison).
- SEO suites (Ahrefs, Semrush/Adobe, Sistrix): third-party *estimates*, not first-party pooled data.
- Search Console analytics tools (SEOTesting, QuickSEO, SEO Gets [features unverified]): single-site views.
- Chartbeat and Parse.ly: enterprise news publishers.
- **No pooled first-party peer benchmark for small sites was found** ([search](https://quickseo.ai/blog/ai-search-vs-google-search-in-2026-40-stats-that-show-why-your-brand-needs-to-track-both)).
- The GEO trackers (critic's SAT-01) measure *AI mentions*, not your traffic versus peers, so this is a different product.

**MVP (5-6 weeks)**
- Search Console OAuth.
- LLM niche classification from the site's content.
- k-anonymous peer pools (≥20 sites per niche and country).
- Dashboards, share cards, weekly index pages, and an agency white-label PDF.

**Inbound GTM plan**
- Posts:
  1. "From 1,200 connected sites: recipe sites -41% clicks YoY, travel -22%, SaaS docs +8%."
  2. "Is it you or Google? Compare your site with 300 peers in 60 seconds."
  3. Weekly Search Traffic Index screenshots, which SEO press can cite.
- SEO: "[niche] Google traffic drop 2026", "AI Overviews traffic impact [niche]".
- Communities: r/SEO, r/juststart, blogger groups, SEO X/LinkedIn.
- Viral loop: share cards, plus "powered by" on agency reports.

**Pricing.** A free benchmark for one site; $12/month (history, alerts, 5 sites); $49/month for agencies.

**Biggest risk.**
- Cold start: credible peer pools need hundreds of connected sites.
- Shrinking publisher budgets.
- Google or the SEO suites could add peer benchmarks.

**Chance 3 / Scale 5.**

### New-idea candidates checked and dropped (incumbent found)
| Candidate | Incumbents that kill it |
|---|---|
| Ghost-job detector / index | 5+ Chrome extensions (Skip This Job, Commit Ghost Job Tracker, GhostJob…), ghostjobs.net ([CWS](https://chromewebstore.google.com/detail/skip-this-job-%E2%80%94-ghost-job/nodldfdkjomniknohmejdimjlejfongd)) |
| "What does ChatGPT say about me" | TrackMyBusiness, Reputation Resolutions, Reputableo ([TrackMyBusiness](https://trackmybusiness.ai/ai-reputation-management-consultants)) |
| Claude Skills leaderboard | skills.sh (Vercel), SkillsMP, Claude Skills Hub ([localskills guide](https://localskills.sh/blog/claude-skills-marketplace-guide)) |
| Auto-renewal / click-to-cancel compliance | RenewalMatrix ($49 report), Churnkey, ProsperStack ([Glama RenewalMatrix](https://glama.ai/mcp/connectors/app.vercel.renewalmatrix/renewalmatrix/tools/check_renewal_compliance)) |
| "Hardest to cancel" index | CancelCompass, JustCancel, GoCancelIt ([CancelCompass](https://cancelcompass.com/best/hardest-to-cancel)) |
| EU cancel-flow tools | Recurflux, Retainly, ChurnNote ([Recurflux](https://recurflux.com/resources/guides/best-cancellation-flow-software-2026)) |
| Influencer ad-disclosure monitoring | CreatorScore, AuditSocials ([AuditSocials](https://www.auditsocials.com/blog/influencer-compliance-guide-ftc-disclosure-rules-platform-tools-2026)) |
| AI Act Art. 50 disclosure widgets | 9+ WordPress plugins, LabelAI on Shopify ([WP.org](https://wordpress.org/plugins/ai-disclosure-for-chatbots/), [LabelAI](https://apps.shopify.com/labelai-ai-image-disclosure)) |
| Cosmetics INCI compliance | Cosmetica's free 15-market checker, cosingchecker ([Cosmetica](https://getcosmetica.com/tools/inci-checker)) |
| Shopify app-developer analytics / benchmark | Cruxify, RevMetrics, Baremetrics, open-source dashboards ([Cruxify](https://cruxify.io/)) |
| Shopify AI-referral attribution | Native Shopify AI channel attribution, Shop Mentions, Comergent ([Shop Mentions](https://shopmentions.com/)) |
| Boutique-fitness benchmarks | Boutique Benchmarks, StudioPulse ([Boutique Benchmarks](https://boutiquebenchmarks.com/)) |
| Steam wishlist benchmark | How To Market A Game benchmark tool ([HTMAG](https://howtomarketagame.com/2025/03/26/benchmarks-how-many-wishlists-can-i-get-from-steam-next-fest/)) |
| YouTube niche/RPM finder (non-English) | NexLev, OutlierKit, vidIQ ([OutlierKit](https://outlierkit.com/blog/best-niche-finder-tools-for-youtube)) |
| Print-farm P&L (#26 pivot) | Printago ([Printago](https://printago.io/)) |
| Consumer recall apps | Food Recalls & Alerts, Recall Bench, RecallPro (so #36 targets *sellers*) |
| Study-in-Germany copilot | Consultancies and content (edvoy, GradGermany, collegedunia) |
| Search Console AI-report benchmark | Not buildable: the report isn't in the API ([Chudi.dev](https://chudi.dev/blog/search-console-generative-ai-report)) |

---

## 6. Updated pipeline and survivor projection
| Tier | Ideas |
|---|---|
| **Most likely survivors** | #2 "Wen empfiehlt die KI?" (5/7) · #20 HireLaw Check (4/6) |
| **Wounded but convertible** (conditions met or testable) | #7 LeanKeep (4/5) · #9 Nachfolge Weekly (4/4) · #12 PSTI+CRA Kit (3/6) · #29 Shopify Bot QA (3/6) · #30+#34 founder media (3/5) |
| **New, not yet attacked** | #36 SafetyRadar (3/5) · #37 SearchShift (3/5) |

**Honest projection: about 6-9 final survivors.** That's below the 10-15 target. I prefer an honest shortfall to padding: 18 more candidates failed the incumbent check in this round. If the debate must reach 10, the most defensible extension is **#2's country editions** (FR/ES/IT/NL/PL). The critic itself called that localisation pattern "the single most reliable" for this founder. Each edition is a separately branded index on the same engine, and they can be run as a portfolio.

**Geography summary.**
- Global by default: #20, #12, #7, #29, #30/#34, #36, #37.
- DACH-first by justification: #2 (with an explicit country-by-country expansion path) and #9 (DACH → NL → an English "Europe for Sale" edition).
