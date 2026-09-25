# SaaS Opportunities: September 2026

**12 ideas that survived a 6-round defender-vs-critic debate**

> **How this was made.** Two research agents debated over 6 rounds.
> - The **defender** researched and pitched ideas.
> - The **critic** attacked them with competitor checks, law and deadline checks, and platform-risk checks.
> - **45 numbered candidates** were debated, and 60+ more were screened out during research.
> - **12 survived. Only 3 of them have a "Chance" score of 4/10 or higher.**
> - The full debate, with every source URL, is in [`research/debate/`](research/debate/).
>
> **What "VALID" means here:** the idea is worth a **2-week test**, not that it's likely to work. Every idea below comes with a concrete test and a pass/fail threshold, and that test is the real filter.

**Your constraints, as applied throughout:**
- B2B or B2C for a *specific* audience, nothing generic.
- **Global by default.** Germany/EU-first only when that is clearly the better bet, and with an expansion path.
- **No cold calls or cold emails.** Marketing comes from social media (you posting the product's output), SEO, marketplaces, and paid ads only after €1k in revenue.
- **Simple is fine.** An API wrapper or small app is OK. Ideas are ranked by **chance of reaching real revenue** first and **scale potential** second.

---

## TL;DR: the ranking

| # | Idea | Who pays | Where | Chance | Scale | Build | Price |
|---|---|---|---|---|---|---|---|
| 1 | **AI Local Index** ("Wen empfiehlt die KI?") | Local businesses + agencies | DACH → EU → UK/AU | **5** | **7** | 5–7 wk | €29–79/mo, €199 agency |
| 2 | **LeanKeep** | Personal trainers & online coaches | Global (EN) | **4** | 5 | 5–6 wk | $29–79/mo |
| 3 | **Nachfolge-Radar Weekly** | Business buyers, brokers, sellers | DACH → "Europe for Sale" | **4** | 4 | 2–4 wk | €49–99 listing, €19/mo Pro |
| 4 | **HireLaw Check** | Staffing agencies & SMB recruiters | US/CA → EU | 3 | 6 | 6–7 wk | $49–149/mo |
| 5 | **AllIn Check** | Venues, gyms, hotels, booking sites, their agencies | US + UK + EU | 3 | 6 | 5–6 wk | $29–99/mo |
| 6 | **SupportUntil** (PSTI + CRA kit) | Small connected-hardware brands | UK/EU, global sellers | 3 | 6 | 6 wk | $29–99/mo |
| 7 | **LabelCheck** | Influencer agencies + creators | EU → UK/US | 3 | 5 | 2–6 wk | €9 creator, €49 agency |
| 8 | **SearchShift** | SEO agencies, bloggers, niche publishers | Global (EN) | 3 | 5 | 5–6 wk | $12–49/mo |
| 9 | **AuthorRadar** | Nonfiction/indie authors, small presses | Global | 3 | 4 | 4–5 wk | $9–99/mo |
| 10 | **PFAS Patchwork Check** | DTC apparel/outdoor/cookware brands | US states + FR/DK | 2 | 5 | 6 wk | $39–129/mo |
| 11 | **SafetyRadar** | Shopify/Woo resellers | US-first, global | 2 | 5 | 5–6 wk | $19–49/mo |
| 12 | **CAIK** (compliance kit for AI apps) | Indie AI chat/image app teams | US + EU | 2 | 4 | 6 wk | $49–149/mo |

**Recommended start:** #1, plus the shared "checker engine" (#5, then #4), with #2 run as a near-zero-build pre-sale test in parallel. See [Start order](#start-order).

---

## The 12 ideas

### 1. AI Local Index / "Wen empfiehlt die KI?" (Chance 5 · Scale 7)

**What it is:** a public index of which local businesses ChatGPT, Gemini and Perplexity recommend, by city × profession. Business owners and agencies pay for a weekly monitor and a fix-list.

- **Who pays:** owners of **non-medical** local businesses (salons, trades, restaurants, tax advisors, studios) and local marketing agencies (white-label).
- **Why now:**
  - People increasingly ask AI assistants "best hairdresser in Köln" instead of Google.
  - **ChatGPT Ads went live in DE/AT/CH on 24 Aug 2026**, so owners now actively wonder whether they still get recommended organically.
  - No public city × profession AI index exists.
- **Competition and your edge:**
  - Local Falcon (from $24.99) proves people pay, but it's an English-first grid tool for agencies.
  - Your edge is a **public German-language index** (SEO + content), DACH directories, and the agency channel.
- **MVP:**
  - Prompt library per vertical × city, run through the **official APIs**: OpenAI web search with `user_location`, Gemini with Search grounding, Perplexity Sonar. **No scraping.**
  - 10 runs per prompt → "share of mentions", matched to Google Places IDs.
  - Public index pages with a methodology and correction/opt-out form.
  - Free "Empfiehlt ChatGPT mich?" check.
  - Paid weekly monitor with competitor diffs and a fix-list.
- **Marketing (no outreach):**
  - Posts: *"Ich habe ChatGPT 100-mal nach dem besten Friseur in 10 Städten gefragt"*, *"Dieser Kölner Salon wird von allen 3 KIs empfohlen – das macht er anders"*, *"ChatGPT zeigt jetzt Werbung in DE. Wirst du noch organisch empfohlen?"*
  - SEO: programmatic "Beste [Beruf] [Stadt] laut ChatGPT" pages.
  - Viral loop: a "Von der KI empfohlen 2026" badge that links back.
- **Expansion:** DE → AT/CH → FR/ES/IT/NL/PL editions (same engine, new language) → English cities.
- **Rules from the critic:**
  - **Skip doctors and other medical listings.** Ranking named doctors while selling to them repeats the *Jameda* case (BGH VI ZR 30/17), where non-paying doctors won deletion.
  - Keep the public index strictly neutral: paying never changes your rank.
- **2-week test:**
  - Days 1–2 are a **noise gate**: are the top-3 results at least 60% stable across 10 runs? If not, publish shares instead of rankings.
  - Then run 1 vertical × 10 cities live with a €19 founding-member checkout.
  - **Pass:** ≥500 free checks, ≥15 paid (or ≥40 card-backed waitlist), and ≥3 agency requests.
- **Biggest risk:** small businesses won't pay €29; AI answers are noisy.
- **Kill signal:** fewer than 5 paid → switch to agency-only pricing. Still under €300 MRR at day 90 → stop.

### 2. LeanKeep (Chance 4 · Scale 5)

**What it is:** a program kit and a "Muscle Retention Score" that lets coaches prove their fast-weight-loss clients (often on GLP-1 drugs like Ozempic) kept their muscle, with shareable client result cards.

- **Who pays:** personal trainers and online coaches. English-first, global (US/UK first because of EU health-data rules).
- **Why now:**
  - GLP-1 use is exploding, and muscle loss is its best-known downside.
  - NASM (course updated June 2026) and ISSA now train coaches specifically for GLP-1 clients.
  - Trainerize, Everfit and TrueCoach have **no GLP-1 features**.
- **MVP:**
  - 12-week strength + protein templates.
  - A client PWA for check-ins, with optional Withings/Fitbit/Health Connect import. It says honestly that body fat is a *proxy*.
  - The score, branded result cards, and CSV export to Trainerize/Everfit.
  - **No drug log and no drug names** (advertising and health-data rules).
- **Marketing:**
  - Posts: *"−14 kg, 91% of her muscle kept: the 12-week plan"* (result card), *"The one number that proves you're not just a diet app"*.
  - SEO: a free **Muscle Retention Calculator**.
  - Viral loop: every client card carries the coach's brand + LeanKeep.
- **2-week test:** calculator + template PDF + $19 pre-sale (about 3 days of work). **Pass:** ≥150 coach signups and ≥15 pre-sales.
- **Biggest risk:** coaches won't pay on top of Trainerize/Everfit.
- **Fallback:** a one-off $49–99 program kit.

### 3. Nachfolge-Radar Weekly (Chance 4 · Scale 4)

**What it is:** a neutral weekly digest of the best DACH businesses for sale. It links to listings and never copies them.

- **Who pays:**
  - Brokers and sellers pay for featured listings (€49–99, self-serve).
  - Buyers (search funders, MBI candidates, SMEs) pay €19/mo for Pro alerts.
  - Sponsors book through a public rate card, so there is no outbound sales.
- **Why now:**
  - Hundreds of thousands of German SME owners seek a successor in the next few years (KfW).
  - Existing newsletters only cover their own mandates; nobody runs a neutral cross-portal digest.
  - The "boring business" / buy-a-business trend is strong on X and LinkedIn.
- **MVP (2–4 weeks, a media product):**
  - beehiiv newsletter + seller form + Stripe checkout for featured listings.
  - Rate card + Pro alerts.
  - SEO pages "[Branche] kaufen [Region]".
- **Marketing:**
  - Posts: *"5 profitable German businesses for sale this week, all under €500k"*, *"A 40-year-old bakery in Franconia: €180k EBITDA, no successor"*.
- **Expansion:** NL → English "Europe for Sale" edition.
- **2-week test:** 2 issues + 6 posts + checkout. **Pass:** ≥250 subscribers, ≥40% open rate, ≥2 paid features or sponsor bookings.
- **Biggest risk:** earning money without doing outbound sponsor sales.

### 4. HireLaw Check (Chance 3 · Scale 6)

**What it is:** a Chrome extension and checker that flags job ads breaking **pay-transparency** and **AI-in-hiring notice** rules across US states, Canada and the EU.

- **Who pays:** staffing agencies and SMB recruiters **not** on Greenhouse/Ashby (those two auto-fill pay ranges). That means Workable, BambooHR, JazzHR, and direct LinkedIn/Indeed posting.
- **Why now:**
  - 16 US states + DC have pay-transparency laws.
  - Ontario's rules have applied since 1 Jan 2026.
  - The EU Pay Transparency Directive is being transposed; Germany missed the June 2026 deadline, so expect 2027.
  - AI-hiring notices: Illinois HB 3773 (since Jan 2026), NYC LL144, Colorado from 2027.
  - Washington settlements have run $1.2–2.8M each.
  - Incumbents are enterprise-only: Datapeople ~$5k/yr, Ongig $17.9k+/yr.
- **Critic's correction:** Washington's SB 5408 gives employers a 5-day cure period until **July 2027**, which dampens urgency until then.
- **MVP:**
  - A rules engine plus the AI-hiring pack.
  - A paste/URL checker.
  - A Plasmo Chrome extension inside the LinkedIn/Indeed/Workable editors.
  - Bulk scan of **public ATS board JSON** (not job-board scraping).
  - A "pay-transparent employer" badge.
- **Marketing:**
  - Posts: *"We checked 5,000 public job ads: X% have no valid range"* (aggregates only), *"The pay-transparency map 2026 in one picture"*.
  - SEO: "pay transparency law [state]" pages.
  - Chrome Web Store listing.
- **2-week test:** **pass** at ≥300 checks, ≥50 installs, ≥10 agency card pre-authorisations.
- **Kill signal:** fewer than 3 pre-authorisations → park until July 2027.

### 5. AllIn Check (Chance 3 · Scale 6)

**What it is:** a Chrome extension that walks through a real checkout and flags hidden fees ("drip pricing"), jurisdiction by jurisdiction.

- **Who pays:** independent venues, gyms and studios, boutique hotels, custom/WordPress booking sites, UK SMBs, and the agencies that build their booking flows. **Not** sites on Airbnb, Vrbo or big booking engines; those already show total prices.
- **Why now:** ongoing, active enforcement.
  - **UK CMA fines under the DMCC Act:** £4.2M (AA/BSM, Apr 2026), £900k (StubHub, Jun 2026), and 3 new drip-pricing investigations (Aug 2026).
  - US: the FTC fee rule; California SB 478 class actions; Colorado (Jan 2026), Connecticut (Jul 2026), MN, VA, MA; plus the EU.
- **Competition:** one free, California/FTC-only scanner (compliance-framework.com). Law firms advise "test your checkout journeys", and this tool *is* that test.
- **MVP:**
  - An extension that captures displayed prices and network responses at each step.
  - LLM fee extraction + a rules engine.
  - A report + "All-in verified" badge.
  - Weekly headless re-checks + a WordPress plugin.
- **Marketing:**
  - Posts: *"We checked 200 booking sites: 6 in 10 add the cleaning fee at the last step"*, *"Connecticut changed on July 1: is your gym's 'admin fee' now illegal?"*
  - SEO: "junk fee law [state]", "drip pricing UK".
  - Listings: Chrome Web Store + WordPress.org.
- **2-week test:** **pass** at ≥300 checks, ≥50 installs, ≥10 paid pre-sales or agency pre-authorisations.
- **Caution:** publish **aggregate** studies. Don't name and shame individual small businesses (legal risk).

### 6. SupportUntil: UK PSTI + EU CRA kit and a Security-Support Index (Chance 3 · Scale 6, slow burn)

**What it is:** a public "security updates until…" index for connected products, plus self-serve compliance documents for small hardware brands: PSTI statement generator, vulnerability-disclosure page, security.txt, CRA templates.

- **Who pays:** small connected-product brands (smart home, pet/baby tech, e-bikes, Kickstarter hardware, Amazon/Shopify sellers) selling into the UK/EU.
- **Why now:**
  - UK PSTI has been in force since April 2024.
  - **EU Cyber Resilience Act vulnerability reporting has been live since 11 Sep 2026**, with full obligations from Dec 2027.
  - No self-serve PSTI generator or support-period index exists.
- **Marketing:**
  - Posts: *"Your smart doorbell stops getting updates in 2027 – we indexed 300 PSTI statements"*.
  - SEO: programmatic model pages.
  - Shopify App Store badge, which links back to the index.
- **2-week test:** **pass** at ≥50 generator completions, ≥5 paid waitlist, ≥1 press pickup.
- **Note:** revenue probably lands in 2027. **Don't build this first.** The index can quietly build up SEO in the meantime.

### 7. LabelCheck (Chance 3 · Scale 5)

**What it is:** a creator-side check that each post carries the **ad label and AI-image label** its country requires (DE "Werbung/Anzeige", FR "Publicité" + "Image retouchée/virtuelle", IT, ES, UK, US).

- **Who pays:** influencer agencies and talent managers (in France, the agency is jointly liable), then creators with brand deals.
- **Why now:**
  - French inspections found problems with 40% of the influencers checked.
  - German "Abmahnungen" (cease-and-desist letters) keep coming.
  - AI Act Art. 50 labelling duties apply from Aug 2026.
  - The platforms' "paid partnership" toggle is **not legally sufficient** in France and Germany.
  - No creator-side checker exists in German or French; the two US tools are brand-side and FTC-focused.
- **MVP:**
  - A **paste-URL/screenshot checker first** (no OAuth, so no Meta/TikTok app review).
  - OCR + an LLM commercial-signal classifier.
  - Fixed country rule packs (fixed rules avoid giving individual legal advice, which German RDG law restricts).
  - A Canva app that stamps compliant labels.
- **Marketing:**
  - Posts: *"Ich habe 200 meiner Posts gescannt: 14 wären abmahnfähig"*, *"Werbung vs Anzeige vs Publicité vs #ad vs KI-Label – the EU cheat sheet"*.
  - Canva Apps Marketplace listing.
- **2-week test:** **pass** at ≥500 checks and ≥20 creator or ≥5 agency pre-sales.
- **Biggest risk:** creators only pay after they've received an Abmahnung.

### 8. SearchShift (Chance 3 · Scale 5)

**What it is:** connect Google Search Console and find out *"is it me or Google?"* Your AI-era traffic change is benchmarked against anonymous peers in your niche, with share cards and a weekly public Search Traffic Index.

- **Who pays:** SEO agencies ($49/mo; this tier has to carry the revenue), then bloggers, niche publishers and content-led SaaS ($12/mo).
- **Why now:**
  - AI Overviews cut click-through heavily.
  - Google's new AI performance report **is not in the Search Console API**.
  - Databox **retired its pooled benchmarks in April 2026**. That leaves the gap open, but it's also a warning.
- **MVP:**
  - Search Console OAuth (needs Google verification) and **explicit consent to pooling**.
  - LLM niche classification and k-anonymous pools (n≥20).
  - Share cards + an agency PDF.
- **Marketing:**
  - Posts: *"412 sites connected: recipe sites −41% clicks YoY, SaaS docs +8%"* (live counter), *"Compare against 300 peers in 60 seconds"*.
  - Channels: r/SEO, r/juststart, SEO Twitter.
- **2-week test:** **pass** at ≥400 connected sites, ≥3 niches with n≥20, ≥10 agency waitlist signups.
- **Biggest risk:** the cold-start problem, because the benchmark is useless until enough sites join.
- **Later:** a newsletter-click version for Kit/Ghost ("InboxShift") as vertical 2, only if this test passes.

### 9. AuthorRadar (Chance 3 · Scale 4)

**What it is:** alerts authors to AI "summary/workbook" knockoffs and to books published under their name that they didn't write, plus a free sales-benchmark hook.

- **Who pays:** nonfiction and indie authors, small presses, literary agents.
- **Why now:** AI knockoff books are a current mainstream story (Fortune, 14 Sep 2026). Existing anti-piracy tools (Book Defender, Blasty) don't cover knockoffs.
- **Data:** a **licensed** Amazon data vendor such as DataForSEO, which explicitly supports building commercial products on its data. **No scraping.** Amazon's own Creators API may not be used for monitoring.
- **Marketing:**
  - Posts: *"Does my book have AI knockoffs?"* free scan, *"Is AI killing my genre?"* share card.
  - Channels: r/selfpublish, BookTok, author newsletters.
- **2-week test:** **pass** at ≥300 scans, ≥20 paid pre-sales, and a measured data cost ≤20% of the price.
- **Biggest risk:** willingness to pay clusters around book launches.

### 10. PFAS Patchwork Check (Chance 2 · Scale 5)

**What it is:** a Shopify app with a PFAS ("forever chemicals") ban map, mapping of your catalogue against the rules, a supplier-declaration portal, shipping-zone blocks and a lab-report vault.

- **Who pays:** DTC apparel, outdoor, cookware and kids' brands shipping to the US, France or Denmark.
- **Why now:**
  - 18+ US states restrict PFAS by category; France has banned it in clothing since Jan 2026, and Denmark since Jul 2026.
  - Demand letters surged in 2026.
  - Tools are enterprise-only (Assent, UL, Z2Data), and **there is no Shopify app**.
- **Marketing:** a shareable **"PFAS ban map 2026"**, SEO "PFAS ban [state] [category]", a free supplier-declaration template, and the Shopify App Store.
- **2-week test:** **pass** at ≥150 catalogue checks and ≥5 paid pre-sales.
- **Risks:** small brands aren't being targeted yet; the real bottleneck is supplier data and lab tests; keeping the rules database current is heavy.

### 11. SafetyRadar (Chance 2 · Scale 5)

**What it is:** a Shopify/Woo app that alerts resellers when a product they sell is recalled, using official feeds: CPSC, openFDA, Health Canada, ACCC, UK OPSS.

- **Who pays:** US resellers of third-party toys, baby, electronics and household goods.
- **Why now:**
  - In the US, **selling a recalled product is itself illegal** (CPSA §19; Home Depot paid $5.7M, TJX $13M).
  - Amazon is named in 61% of 2026 CPSC recalls, and CPSC eFiling became mandatory in July 2026.
  - There's no merchant-facing Shopify app for US recalls; SafeCart.eu covers only the EU.
- **Matching:** exact barcode (GTIN) → brand + model → an LLM verifier that flags only at ≥0.9 confidence.
- **2-week test:** **kill switch** at ≥80% precision on 1,000 real products. CPSC records often lack barcodes, so this is the real risk.
- **Marketing:** a weekly "Recalled this week" index, SEO "[brand] recall", and a free parent-alert list as a side funnel.

### 12. CAIK: compliance kit for indie consumer-AI apps (Chance 2 · Scale 4)

**What it is:** a drop-in SDK for small AI chat and image apps.

- **Chat module:**
  - AI-disclosure and break-reminder timers.
  - Crisis routing through **Koko/ThroughLine** (no self-built risk detection).
  - A hosted crisis-protocol page and an evidence log.
- **Image module:**
  - TAKE IT DOWN Act intake with a 48-hour takedown timer.
  - Image fingerprinting to catch reposts.
  - EU DSA / UK OSA notices.

Details:

- **Who pays:** SFW revenue-generating indie studios. Appfigures counts 337 revenue-earning AI companion apps, about 300 of them small. **Adult apps are excluded.**
- **Why now:**
  - California SB 243 lets users sue directly (from $1,000 per violation).
  - NY is in force, and OR and WA follow in 2027.
  - AI Act Art. 50 applies from Aug 2026.
  - The TAKE IT DOWN Act has been enforced by the FTC since 19 May 2026.
- **Marketing:** SEO "SB 243 compliance checklist", a free protocol-page generator (earns backlinks), a public audit of 100 apps, and npm/PyPI.
- **2-week test:** **pass** at ≥10 SFW revenue-generating teams pre-authorising a card.
- **Risks:** thin budgets (the top 10% of apps take 89% of revenue) and no SB 243 lawsuit yet.

---

## Start order

**Principle:** run the cheap tests in parallel, and build shared engines once.

1. **Week 1: AI Local Index (#1).**
   - Highest chance and scale.
   - Your German is a real advantage, because the index is language-bound.
   - The rankings **are** the social content, exactly like your "top apps this week" format.
   - The day-1 noise gate kills it cheaply if the AI answers are unstable.
2. **Weeks 1–2: one "patchwork checker" engine, starting with AllIn Check (#5), then HireLaw Check (#4) as a second rule pack.**
   - #4, #5, #7 and #10 share one engine: Chrome extension or paste-URL capture → LLM extraction → jurisdiction rules engine → badge → public aggregate index.
   - Start with #5, because enforcement is active *now*.
   - Add #4's rules in time for July 2027 (end of Washington's cure period + the EU transposition wave).
   - LabelCheck (#7) is the natural third rule pack.
3. **In parallel: LeanKeep (#2) as a near-zero-build pre-sale.** A landing page, calculator, PDF and a $19 pre-sale take about 3 days of work. Build the product only if ≥15 coaches pay.

**After 2–4 weeks:** keep the 1–2 ideas that hit their thresholds and kill the rest without sentiment. If nothing passes, Nachfolge-Radar (#3, almost no build) and SearchShift (#8) are the next cheapest tests.

---

## Marketing playbook (no cold outreach)

Your plan (post the product's output, SEO for the long term, ads after €1k) fits these ideas well. Here's how to make it stronger.

1. **Build in public, with the product's output as the content.** Every idea above has a "postable" output: an index, a map, a hall of fame, a result card, a data study. Post it 3–5× a week where the buyers are:
   - LinkedIn for B2B
   - Instagram/TikTok for coaches and creators
   - X and Reddit for SEO/dev/indie audiences
2. **Launch every product with a data study.** Examples: "We checked 200 booking sites…", "We scanned 5,000 job ads…", "We indexed 300 PSTI statements…". A data study works on social media, gets picked up by journalists and newsletters, and earns backlinks. **Publish aggregates, not names of individual small businesses.**
3. **A free tool as the front door, with programmatic SEO behind it.** A free checker or calculator converts visitors. Programmatic pages ("[law] [state]", "[profession] [city]", "[brand] recall") bring long-tail traffic for years.
4. **Marketplaces as inbound channels.** People there are already searching for a solution:
   - Chrome Web Store (#4, #5)
   - Shopify App Store (#6, #10, #11)
   - WordPress.org (#5)
   - Canva Apps (#7)
   - npm/PyPI (#12)
5. **Viral loops built into the product.** Badges that link back ("Von der KI empfohlen", "All-in verified", "Security updates until 2030"), branded share cards (LeanKeep, SearchShift), and "powered by" footers on agency white-label reports.
6. **An owned newsletter.** A build-in-public newsletter across your products turns followers into an audience you own. The critic judged it not strong enough to count as a product on its own, but it's your best distribution channel.
7. **Agency partner program (inbound).** Several ideas (#1, #5, #7, #8) have agencies as multipliers. Offer 30% recurring commission and a white-label tier, so agencies come to you rather than you pitching them.
8. **Paid ads after €1k MRR.** Start with retargeting visitors of your free tools, then Google Ads on high-intent legal keywords ("SB 478 compliance", "PFAS ban California apparel"). Those searchers have an urgent problem.

> In Germany, cold B2B email without prior consent is illegal (§7 UWG). Your no-outreach approach is also the legally safer one.

---

## What the debate taught us (September 2026 market patterns)

1. **Public deadlines get swarmed within weeks.** Examples: EU green-claims checkers, AI Act label widgets (9+ WordPress plugins), EUDR and product-passport tools. What survives is **ongoing enforcement** (private lawsuits, active regulators like the UK CMA) or a **patchwork of rules across jurisdictions that keeps changing**.
2. **The EU is in "omnibus" mode:**
   - CSRD scope was cut by ~80%.
   - AI Act high-risk rules moved to Dec 2027/Aug 2028.
   - The EU deforestation rule (EUDR) was delayed twice.
   - Germany missed the Pay Transparency deadline.
   - **Don't build on pending EU rules.** US state patchworks and the UK's DMCC regime are more reliable drivers.
3. **Indexes built by scraping are fragile and easy to clone.** Apify has a scraper for nearly every ecosystem. Durable data comes from **official feeds**, **the user's own connected accounts (OAuth)**, or **licensed data vendors**.
4. **Platforms close gaps inside their own product within 6–12 months.** Examples: Lovable/Supabase security defaults, GitHub PR limits, YouTube likeness detection, Meta's free WhatsApp business agent. If a problem lives inside one platform, assume that platform will solve it.
5. **Most new ecosystems already have their "ranking site"** (TrustMRR, skoolstats, SocialPeta, Kalodata…). A ranking is ownable only with an unoccupied **language** (#1) or **first-party data** (#8).
6. **Pure consumer (B2C) apps get cloned within months.** The sweet spot is **prosumers who earn money from the output**: coaches, creators, authors. All 10 pure-B2C directions checked were already crowded.
7. **German consumer-paperwork helpers lose** to free official or NGO tools and to RDG (legal-advice) limits. German works as an advantage where the **content asset is language-bound** (#1, #3, #7).
8. **"No competitor" was wrong about half the time on the first search.** Always check the Shopify App Store, Chrome Web Store, Product Hunt, G2 and GitHub before building.

---

## What was killed (and why)

About 30 numbered ideas died. The main reasons, with examples:

- **A free or official tool already exists:**
  - PV-quote checker (Verbraucherzentrale NRW)
  - therapy-cost reimbursement helper (kostenerstattung-antrag.de)
  - care-budget wallet (the nui app, free via insurers)
  - heat-pump efficiency ranking (heatpumpmonitor.org)
- **The platform shipped it:**
  - security scanning for vibe-coded apps (Lovable scans every publish)
  - GitHub PR spam filter (GitHub PR limits)
  - support-bot QA (Gorgias/Tidio test modes)
  - musician impersonation (Spotify, YouTube)
- **An incumbent was missed:**
  - micro-drama charts (SocialPeta)
  - creator revenue verification (TrustMRR)
  - AI-trainer gig pay index (OpenTrain, aitrainer.work)
  - App Store rejection checker (Rork and others)
- **Regulation delayed or weakened:** ESG/CSRD tools, AI Act high-risk tooling, energy-sharing tools (parked until 2027).
- **Crowded:**
  - NIS2 trust centers
  - green-claims scanners
  - AI search-visibility trackers (Profound valued at $1.8B)
  - fake-review extensions
  - n8n agency monitoring
  - Airbnb-host compliance (Chekin)
- **The data source forbids it:** 3D-print trend radar (MakerWorld's terms ban monitoring), YouTube peer benchmarks (the API policy forbids pooling).

Watchlist (not yet valid, one condition each):
- **InboxShift:** only after SearchShift's test passes.
- **Zitat-Check** (AI citation verifier for German lawyers): only if ≥80% of real brief citations can be verified from free sources.

---

## Debate files

| Round | Defender | Critic |
|---|---|---|
| Brief | [00-brief.md](research/debate/00-brief.md) | — |
| 1 | [25 candidates](research/debate/01-defender-candidates.md) | [Saturation map, regulation reality check, platform risks](research/debate/01-critic-ammunition.md) |
| 2 | [10 global additions](research/debate/02-defender-additions.md) | [Attack on the 25](research/debate/02-critic-attack.md) |
| 3 | [Rebuttal + pivots](research/debate/03-defender-rebuttal.md) | [Attack on the additions](research/debate/03-critic-additions-attack.md) |
| 4 | [6 new candidates](research/debate/04-defender-new-candidates.md) | [Verdicts: 6 VALID](research/debate/04-critic-verdicts.md) |
| 5 | [Final batch + fixes](research/debate/05-defender-final-batch.md) | [Verdicts: 7 VALID](research/debate/05-critic-verdicts.md) |
| 6 | [Launch cards (stack, pricing, 90-day plans)](research/debate/06-defender-launch-cards.md) | [Final ranking: 12 VALID](research/debate/06-critic-final-ranking.md) |

*Figures come from web research done 24–25 Sep 2026. Some sites blocked direct fetching, so a few facts rest on search summaries; the debate files mark these as [summary], [unverified] or [MEMORY]. Re-check the key numbers for any idea before you commit to it.*
