# Round 5 (Defender): wounded conditions, the #38+#40 bundle, AuthorRadar data, and the final batch #44-#45

Author: DEFENDER, 2026-09-25.
Inputs: `04-critic-verdicts.md`, `05-critic-verdicts.md`, and the coordinator's round-5 tasks.

**Method.** The proxy blocked direct fetches of cpsc.gov, saferproducts.gov, api.fda.gov, gov.uk, open.canada.ca and most vendor sites. Where a fact comes only from a search-result summary, it is flagged **[summary]**. Facts from memory that I could not re-check are flagged **[MEMORY]**.

**Two corrections accepted up front**
- **#20:** my "~700 class actions" figure counted *all* Washington employment class actions, not pay-transparency cases, and SB 5408 adds a 5-business-day cure period until Jul 2027. I accept C3/S6.
- **Etsy drop (round 4):** my reason was wrong. eRank, EverBee, Alura and Marmalead are keyword and competitor-estimate tools, not pooled peer benchmarks. The corrected reason is in §6.

## 0. Decisions at a glance

| Item | Critic's condition | My answer | C/S |
|---|---|---|---|
| **#36 SafetyRadar** | US-first Shopify app + ≥80% match precision on 1,000 SKUs | **DEFEND, US-first.** No Shopify app or self-serve seller tool for US recalls found. Tiered matching design and a 2-week precision test are specified. | **3/5 if the test passes**, else concede |
| **#30+#34 founder media** | 2k subscribers + 1 sponsor in 6 weeks | **CONCEDE as a standalone idea.** It becomes the founder's distribution engine for #37, #9 and the new #38+#40 bundle. | — (not counted) |
| **#38 + #40 → "CAIK"** (compliance kit for indie consumer-AI apps) | Integrate Koko/ThroughLine; ≥10 SFW paying teams; narrow #40 to AI image/video apps | **MERGED as suggested.** 337 revenue-generating AI companion apps exist (Appfigures), so the ≥50 threshold is met several times over. | **3/4** |
| **#39+#43 AuthorRadar** | Written data licence; data ≤20% of revenue | Keepa's terms aren't public. **DataForSEO's Amazon API plus adaptive scheduling** gives about 15% of revenue on paper. Needs written confirmation. | stays **3/4 (conditional)** |
| **#42 InboxShift** | Only as #37's second vertical | **ACCEPTED** | — |
| **NEW #44 AllIn Check** | pattern (a) | Junk-fee and drip-pricing checker: US states + FTC + UK DMCC + EU + Canada | **3/6** |
| **NEW #45 PFAS Patchwork Check** | pattern (a) | Shopify-native PFAS ban map + supplier declarations: 18+ US states + France + Denmark | **3/5** |
| AI-in-hiring disclosure | pattern (a) | **Folded into #20** as a module, as the critic recommended. Not counted as new. | — |
| Pattern (b) connect-account benchmarks | — | **No new idea passes.** YouTube's API policy forbids pooling; Apple, Google Play, RevenueCat, GA4 and Klaviyo already show benchmarks. See §6. | — |
| Pattern (c) B2C | — | **None passes.** 10 B2C directions checked; each is already crowded with clone apps. See §7. | — |

**Honest count:** 2 new ideas pass (#44, #45), not 4-6. I checked 25+ more and dropped them (§8). The coordinator's round-4 calibration made small competitors acceptable, but the same "swarm" pattern keeps appearing in B2C and in anything built around a single deadline.

---

## 1. #36 SafetyRadar: US-first response to the condition (C3/S5 if the precision test passes)

### (a) The US-first case is stronger than my EU version
- **Recalls now run through online channels.** An analysis of all **359 CPSC recalls from 1 Jan to 30 Jul 2026** found **Amazon named in 219 (61%)**. **Half** of the recalls cited an existing mandatory standard, meaning products were sold while failing rules that already existed ([PoliticSphere index](https://www.politicsphere.com/online-marketplace-product-recalls-index/)) [summary].
- **Enforcement is escalating.**
  - The CPSC issued 26 **unilateral warnings** in a year, more than the previous five years combined, mostly for foreign e-commerce sellers ([BriefGlance](https://briefglance.com/articles/mass-recalls-expose-gaps-in-e-commerce-and-product-safety-oversight)) [summary].
  - It has issued its **100,000th takedown notice** for recalled or banned products listed online ([Buchalter, 2026](https://www.buchalter.com/blogs/cpsc-escalates-enforcement-in-2026-expanded-market-oversight-civil-penalties-and-criminal-exposure/)).
- **Selling a recalled product is itself unlawful** under CPSA §19(a)(2)(B) ([CPSC](https://www.cpsc.gov/Business--Manufacturing/Business-Education/ResaleThrift-Stores-Information-Center/Stop-Online-Sale-of-Recalled-Products)). Penalties to date include **Home Depot $5.7M** and **TJX $13M** ([CPSC](https://www.cpsc.gov/Newsroom/News-Releases/2022/TJX-Agrees-to-Pay-13-Million-Civil-Penalty-for-Selling-Offering-for-Sale-and-Distributing-Recalled-Products)). This answers the critic's objection that "brand owners already know their recalls": the buyer is the **reseller**, who carries §19 liability for other brands' products.
- **CPSC eFiling became mandatory on 8 Jul 2026.** Importers must now file certificate data at entry ([GDLSK](https://www.gdlsk.com/new-cpsc-efiling-rule-for-imported-consumer-products-effective-july-8-2026/), [UPS](https://www.ups.com/us/en/shipping/international-shipping/tariffs/cpsc)). Small US importers now deal with CPSC rules every week.

### (b) Feeds (all official and free; direct access was blocked here, so each is confirmed via documentation or search)

| Feed | Access | Match-relevant fields |
|---|---|---|
| **CPSC Recalls API** (saferproducts.gov REST, JSON/XML) | Public | Products, model, **UPCs when reported**, manufacturers, importers, retailers, hazards, remedies, images ([CPSC API](https://www.cpsc.gov/Recalls/CPSC-Recalls-Application-Program-Interface-API-Information), [data.gov](https://catalog.data.gov/dataset/recalls-api)) |
| **openFDA enforcement** (food/drug/device) | Public, weekly, 2004-present | Recalling firm, product description, code info; **UPC/NDC on drug recalls** ([openFDA food](https://open.fda.gov/apis/food/enforcement), [device](https://open.fda.gov/apis/device/enforcement)) |
| **Health Canada Recalls & Safety Alerts** | Open data, JSON/CSV, daily, 33k+ records | Brand, product, affected lots/UPCs in text ([open.canada.ca](https://open.canada.ca/data/en/dataset/d38de914-c94c-429b-8ab1-8776c31643e3)) [summary] |
| **ACCC Product Safety Australia** | Public recall register | Product, supplier, affected batches/SKUs ([Apify feed description](https://apify.com/nexgenwatch/australia-accc-product-recall-watch/api/python)) [summary] |
| **UK OPSS PSD / GOV.UK recalls finder** | Public | Product, barcode/model/batch where notified ([GOV.UK](https://www.gov.uk/product-safety-alerts-reports-recalls), [PSD](https://www.product-safety-database.service.gov.uk/)) |

### (c) US-side competitor check
- **Shopify App Store** (`site:` search "recall CPSC monitoring"): only store-uptime and stock-alert apps. **No catalogue-vs-recall app found.** Earlier checks found only LotTrack (runs *your own* recalls) and Warnify (warning pop-ups).
- **SuperRecall.ai:** 18 regulatory APIs; **Professional plan from $449/month**; targets medtech, pharma, food and consumer goods ([SuperRecall](https://superrecall.ai/)) [summary]. It's priced and positioned for regulated manufacturers, not a $19 Shopify reseller.
- **TrackVision AI:** GS1/EPCIS traceability for grocery and QSR; enterprise ([TrackVision](https://trackvision.ai/solutions/recall-monitoring)).
- **Apify "Recall Exposure Matcher"** (catalogue vs CPSC/openFDA, exact + fuzzy): a developer actor, not a merchant product. It **validates the matching approach** ([Apify](https://apify.com/parviz_a/recall-exposure-matcher-check-your-catalog-against-cpsc-fda)).
- **Amazon** handles recalls for Amazon sellers (the Recalls Logistics Service), so **Shopify/Woo sellers are the uncovered segment**.
- **SafeCart** is EU/Safety Gate only (plus a shopper Chrome extension) ([SafeCart](https://www.safecart.eu/)).

### (d) Matching design, and why ≥80% precision on *flagged* matches is plausible

| Tier | Rule | Action | Expected precision |
|---|---|---|---|
| **T1 GTIN** | Normalise the Shopify variant barcode (UPC-A ↔ EAN-13 ↔ GTIN-14, check digit), then exact match against the recall's UPC list | **Flag** | ~99% (errors only from wrong or reused barcodes) |
| **T2 Brand + model** | Brand matched against the recall's manufacturer/importer/brand names via an alias table, **plus** an exact model token (alphanumeric, ≥4 characters, containing a digit, separators stripped) | **Flag** | High; ~90% [estimate] |
| **T3 Brand + product similarity** | Brand match plus title/description similarity, then an **LLM verifier** that sees both product pages and the recall images | **Flag only above a confidence of 0.9**; otherwise send to review | Tunable to ≥80% |
| **T4 Hazard watch** | Category × hazard (button batteries, infant sleepers, magnets) with no identifier | **Digest only, never a flag** | n/a |

**Precision is a design choice here.** Only T1-T3 above threshold count as "flagged". The honest weakness is **recall (coverage)**: unbranded or white-label marketplace goods without GTINs, which make up much of the foreign e-commerce recall stream, will often land in T3 review or be missed. CLIP image similarity against the recall photos becomes a *review* suggestion, not a flag.

### (e) 2-week test, inbound only
- **Precision set:** 1,000 SKUs from **5 toy, baby or cosmetics resellers**.
  - First choice: opt-in beta users recruited through posts in r/shopify, r/FulfillmentByAmazon and the Shopify Community.
  - Fallback: public Shopify catalogue JSON (a research sample only, with no contact with those stores).
  - Run against 24 months of CPSC, Health Canada and ACCC recalls. Every flag is labelled by hand.
  - **Pass: ≥80% precision.**
- **Coverage set:** 150 CPSC 2025-26 recalls from firms that sell DTC. Measure how many of the recalled SKUs the matcher finds on those brands' own storefronts. **Report recall honestly; no threshold.**
- **Commercial signal:** a free "Recall Check" for 25 SKUs. **Pass: ≥30 installs and ≥5 paid ($19) within 4 weeks.**
- **If the precision test fails: CONCEDE #36.**

**Chance 3 / Scale 5, conditional.** US-first gives a large Shopify reseller base, a statutory selling ban, rising enforcement, and no Shopify-native competitor.

---

## 2. #30+#34 founder media: CONCEDE as a standalone idea; keep it as the distribution engine
I accept the critic's framing. The newsletter isn't a product. It is the founder's build-in-public channel ("Sherlocked this week" + the builder index), run at ≤4 hours a week, whose job is to:
1. **Feed the products that share its audience.** The **#38+#40 bundle** (indie AI-app developers are exactly this readership), **#37 SearchShift** (indie publishers and content-led SaaS), and **#9** (the "buy a boring business" crowd overlaps with indie hackers).
2. **Monetise only opportunistically** through ad networks (beehiiv Ad Network, Passionfroot rate card). No outbound sponsor sales.

It is no longer counted in the tally. The 6-week gate (2k subscribers + 1 sponsor) remains only as the signal for whether to invest more hours in it.

---

## 3. #38 + #40 → **CAIK: compliance kit for indie consumer-AI apps** (C3/S4)

**Pitch.** One SDK plus a dashboard that gives small consumer-AI apps the compliance plumbing the new laws require, **without building life-safety detection ourselves**:
1. **Chat module** (companion, character, tutor, wellness, coach apps):
   - AI-disclosure banners at session start;
   - recurring reminders for minors (every 3 hours in CA and OR, every hour in WA);
   - a hosted, public **crisis-response protocol page** (SB 243 requires one);
   - an evidence log plus an export for the **annual report to the CA Office of Suicide Prevention (from 1 Jul 2027)**;
   - crisis routing **through Koko or ThroughLine** plus the model vendor's free moderation.
2. **Image/video module** (AI generators with public galleries or feeds):
   - a **TAKE IT DOWN** intake form with a 48-hour SLA timer and paging;
   - duplicate removal through PDQ hashes (no image storage);
   - EU DSA Art. 16 notices with statement-of-reasons templates;
   - optional **C2PA/AI labels** for AI Act Art. 50 via SSL.com's free C2PA signing tier.
3. **A jurisdiction matrix and checklist:** CA, NY, OR, WA, the EU AI Act Art. 50, TIDA, DSA and the UK OSA.

**Buyer (narrowed as the critic asked):** SFW, revenue-generating indie and small studios. **NSFW apps are excluded** (payment-processor and liability risk). Hobby forums are dropped.

**Evidence that the buyer pool exists (≥50 revenue-generating apps)**
- **337 active, revenue-generating AI companion apps** worldwide (July 2025), **128 of them launched in 2025**. The top 10% earn 89% of revenue, and about 33 apps have >$1M lifetime spend ([TechCrunch/Appfigures](https://techcrunch.com/2025/08/12/ai-companion-apps-on-track-to-pull-in-120m-in-2025)). That leaves a **long tail of ~300 small revenue-earning companion apps**, even before counting AI tutors, wellness chats and image generators (the image-app count is not quantified here).
- Not every one is SFW. Even so, several times the ≥50 threshold is plausible [estimate].

**Integration partners, not competitors (the critic's point on rule (a))**
- **Koko** (nonprofit): **Keywords API** (credential-gated risk taxonomy; sign-up for a key) and a **public, unauthenticated Crisis Helplines API** by country. It has been deployed by TikTok, Pinterest, Discord and others ([Koko developers](https://developers.kokocares.org/docs), [API profile](https://github.com/api-evangelist/koko)).
- **ThroughLine:** verified helplines in 170+ countries ([ThroughLine](https://www.throughlinecare.com/)); pricing for small developers is not public (unverified).
- CAIK **orchestrates** these services and records the evidence. It never claims to detect risk itself. That removes the critic's liability objection.

**Competitors (checked)**
- **Enterprise trust-and-safety** (Tremau, Checkstep, Cinder, Hive, ActiveFence) is sales-led.
- **Law-firm guides** tell operators to build it themselves.
- **Limina** does PII redaction only.
- **GitHub/Google:** no SB 243 kit found. The one public example is an indie team writing its own `/safety` protocol page ([GitHub PR](https://github.com/hunterblack/closer-ai-web/pull/5)).
- **No self-serve bundle covering chatbot laws + TIDA + Art. 50 exists.**

**MVP (6 weeks)**
- TS/Python middleware with Koko and ThroughLine adapters.
- React/React Native/Flutter disclosure and timer components.
- A protocol-page generator.
- An event log with CSV/PDF export.
- A TIDA form, SLA timer and PDQ hashing.
- The jurisdiction checklist.

**Inbound GTM plan: how the founder reaches app developers without cold outreach**
1. **SEO on the law names developers actually search:**
   - "SB 243 compliance checklist";
   - "companion chatbot law Oregon/Washington";
   - "Take It Down Act AI image app";
   - "AI Act Article 50 chatbot disclosure";
   - "crisis protocol template".
2. **Free protocol-page generator.** Every hosted page links back ("Protocol hosted by CAIK"), so every customer page is a backlink and a referral.
3. **A public "Consumer-AI Safety Index."** An audit of 100 apps' **public** pages (disclosure shown? protocol published? intimate-deepfake report form?) as one image per post on X, LinkedIn and Hacker News.
4. **Developer communities as a participant:** r/SideProject, r/iOSProgramming, r/SaaS, Indie Hackers, the RevenueCat community.
5. **App-builder ecosystems:** npm/PyPI packages; copy-paste snippets and templates for the AI app builders (Rork, Vibecode, Lovable, Bolt) and the Replicate/fal starter kits [partnership reach unverified].
6. **The founder's build-in-public newsletter** (§2): the vibe-coder audience overlaps almost exactly.

**Honest limit:** these developers are reachable, but they buy late, after a lawsuit headline. Law-name SEO is the steadiest channel.

**Pricing.**
- Free: protocol page, disclosure components, checklist.
- $49/month: chat module.
- $79/month: image module.
- $149/month: both, plus the report export and several apps.

**Biggest risk.**
- A small total market: roughly 1-2k SFW buyers globally [estimate].
- No SB 243 lawsuit filed yet.
- Model vendors and app-builder platforms could ship compliance toggles.
- Many buyers wait for enforcement.

**Condition test (as set by the critic).** Launch the free generator plus the index. **Pass: ≥10 SFW revenue-generating teams on a paid waitlist (card pre-authorisation) within 4 weeks.**

**Chance 3 / Scale 4.**

---

## 4. AuthorRadar data licensing (one paragraph, as asked)
- **Keepa:** the public API docs describe keyword product search, and pricing starts around €49/month for 20 tokens a minute ([Keepa docs](https://keepa.com/api-docs/), [RevenueGeeks](https://revenuegeeks.com/software/keepa/api)). But its API terms are **not published on keepa.com**. Only a Scribd copy of "Terms and Conditions for Keepa.com's API" surfaces ([Scribd](https://www.scribd.com/document/751189100/Terms-and-Conditions-for-Keepa-com-s-API)). So a customer-facing alert service **needs Keepa's written confirmation**, exactly as the critic says.
- **The Creators API is out** (it is limited to apps that drive Amazon sales).
- **Two commercial alternatives exist.** Both are third-party collectors, which moves the collection risk to the vendor without eliminating Amazon terms-of-service risk.
  - **Rainforest API (Traject Data):** real-time Amazon search and product data in all Amazon domains. Hobbyist plan $23/month for 500 credits ([Traject](https://trajectdata.com/ecommerce/rainforest-api/), [comparison](https://www.asinspotlight.com/blog/asinspotlight-api-vs-rainforest-api)). **Too expensive per request at scale.**
  - **DataForSEO Merchant API: Amazon.** Products (search listings), ASIN and seller endpoints, pay-as-you-go from about **$0.0015 per task (Standard)** ([pricing](https://dataforseo.com/pricing/merchant/amazon-api), [docs](https://docs.dataforseo.com/v3/merchant-amazon-overview/)) [the products-endpoint price is assumed equal; unverified].
- **Budget at 500 monitored titles:**
  - 2 queries (title, author) × 3 marketplaces × **daily only during a 30-day launch window, weekly otherwise** gives roughly **30-90k tasks a month ≈ $45-135**.
  - Revenue at 500 titles: about 100 authors at $9 ≈ $900, which puts data costs at **about 5-15% of revenue**, meeting the ≤20% condition *if* DataForSEO pricing holds.
- **The free, official Google Books API** adds partial coverage of new titles.
- **Verdict:** the condition looks achievable through DataForSEO plus adaptive scheduling, **pending written terms from DataForSEO (or Keepa) for customer-facing alerts.**

---

## 5. Final batch: pattern (a), enforcement-driven multi-jurisdiction checkers

### #44 **AllIn Check**: junk-fee and drip-pricing checker for consumer checkouts (C3/S6)
**Pitch.** You paste a URL, or click through your own booking or checkout flow with the **Chrome extension**. It records the **first price shown** and **every fee added later** (cleaning, resort, service, booking, card surcharge). It then flags violations per jurisdiction:
- **US:** the FTC fee rule for tickets and lodging; CA SB 478 (all industries); Minnesota; Virginia; Colorado from 1 Jan 2026; Connecticut from 1 Jul 2026; Massachusetts AG regulations; Oregon.
- **UK:** the DMCC Act drip-pricing ban.
- **EU:** the Unfair Commercial Practices Directive and Price Indication rules.
- **Canada:** the Competition Act drip-pricing provisions [MEMORY].

The output is a fix list, an **"All-in verified" badge**, and weekly re-checks as prices change.

**Audience.** Global SMBs with consumer checkouts:
- boutique hotels and **vacation-rental direct-booking sites**;
- independent venues, event organisers and ticket sellers;
- gyms and studios (sign-up and "admin" fees);
- restaurants with online-ordering fees;
- property managers (rental-listing fees);
- the agencies that build these sites.

**Why now**
- **The patchwork keeps growing.** California, Minnesota and Virginia are in force. **Colorado HB25-1090 took effect on 1 Jan 2026**, **Connecticut SB 3 on 1 Jul 2026**, and Massachusetts AG regulations apply. Penalties include **MN up to $25k per violation**, and the **CT AG is seeking $39M** in a related case ([Wiley](https://www.wiley.law/alert-Expanding-Patchwork-of-State-Junk-Fees-Laws-Presents-Compliance-Challenges), [Troutman](https://www.troutman.com/insights/state-attorneys-general-and-continued-enforcement-against-junk-fees-in-2026/)).
- **Private enforcement.** SB 478 runs through the CLRA: **at least $1,000 per violation in class actions** plus attorney fees, and "a stream of class actions" has followed ([Blank Rome](https://www.blankrome.com/publications/price-not-right-early-lawsuits-signal-strict-enforcement-californias-new-drip-pricing), [CA AG](https://oag.ca.gov/hiddenfees)).
- **FTC Rule on Unfair or Deceptive Fees:** live-event tickets and short-term lodging, **effective 12 May 2025** ([Federal Register](https://www.federalregister.gov/documents/2025/01/10/2024-30293/trade-regulation-rule-on-unfair-or-deceptive-fees)).
- **UK:** drip pricing banned since 6 Apr 2025. The **CMA reviewed 400+ businesses in 19 sectors** and opened 8 investigations, including StubHub and viagogo (Nov 2025). Fines run **up to 10% of turnover** ([Sidley](https://www.sidley.com/en/insights/newsupdates/2025/11/uk--competition-and-markets-authority-opens-investigations-into-online-pricing-practices), [CMS](https://cms.law/en/gbr/legal-updates/no-hidden-charges-clamping-down-on-drip-pricing)).

**Competitors (checked)**
- **compliance-framework.com:** a *free* SB 478/FTC scanner with a "Verified Badge" ([site](https://compliance-framework.com/)). California/FTC only; one small player, which validates demand.
- **carmarkup.com:** dealership contracts only.
- **Law-firm guides** (Kolmogorov Law's SMB playbook and others).
- **Chrome Web Store, Shopify and WordPress.org `site:` searches:** no drip-pricing checker, only fee-*adding* apps.
- **No enterprise product focused on this.**

**Winning angle:**
- **multi-jurisdiction** (US states + UK + EU + CA);
- an **extension that walks the real checkout path**, where static URL scanners miss fees added late;
- vertical templates (lodging, ticketing, gyms);
- monitoring and a badge.

This is #20's engine applied to prices.

**MVP (5-6 weeks)**
- An MV3 extension capturing price elements and network responses at each step.
- LLM extraction of price components.
- A rules engine per jurisdiction and industry.
- The report and badge.
- Headless weekly re-checks for simple flows.

**Inbound GTM plan**
- Posts:
  1. "We checked 200 vacation-rental direct-booking sites: 6 in 10 add a mandatory cleaning fee at the last step. That's illegal in CA, MN, VA, CO, CT and the UK." (aggregates only)
  2. "The all-in pricing map 2026: 8 US states + UK + EU in one picture."
  3. "What changed in Connecticut on 1 July (and why your gym's 'admin fee' is now a problem)."
- SEO:
  - "SB 478 compliance checker";
  - "junk fee law [state]";
  - "drip pricing UK DMCC";
  - "cleaning fee all-in price direct booking".
- Marketplaces: Chrome Web Store; WordPress.org (booking-site plugin); Shopify (surcharge flows).
- Viral loop: the badge.

**Pricing.**
- A free one-off check.
- $29/month: 1 site, weekly monitoring, the badge.
- $99/month: agencies and property managers, 20 sites.

**Biggest risk.**
- Booking engines (Lodgify, Guesty, Cloudbeds, Eventbrite) may already show all-in prices for their own customers, which is rule (c) for *those* users, so focus on custom and WordPress booking flows.
- Complex, login-gated flows.
- The legal-information boundary.
- Enforcement is uneven by state.

**Chance 3 / Scale 6.** The same dynamics as #20 (a patchwork, private suits, no self-serve incumbent), with a broader and global audience.

### #45 **PFAS Patchwork Check**: ban map and supplier declarations for DTC brands (C3/S5)
**Pitch.** A Shopify app (plus a web version). It maps every product to PFAS restrictions by jurisdiction, category, effective date and threshold:
- California textiles/apparel (100 ppm, falling to 50 ppm in 2027);
- California's cosmetics ban and cookware online-disclosure rule;
- New York apparel;
- Minnesota Amara's Law;
- Maine, Colorado, Connecticut, Vermont, Washington, Rhode Island, Illinois and New Mexico;
- **France** (cosmetics and clothing textiles since 1 Jan 2026);
- **Denmark** (clothing and footwear from 1 Jul 2026).

It then:
- runs a **supplier portal** that collects "no intentionally added PFAS" declarations and lab reports;
- stores the **evidence** (ppm versus threshold);
- **blocks shipping** to states where a product is banned;
- produces a **response pack** for when a demand letter arrives.

**Audience.** Global DTC apparel, outdoor, textile, cookware, kids' and (later) cosmetics brands selling into the US or France/Denmark. EU brands shipping to California are included.

**Why now**
- **"At least 18 states"** now restrict PFAS in product classes, and **14 states ban intentionally added PFAS in cosmetics** (as of Mar 2026) ([Buchalter](https://www.buchalter.com/blogs/how-state-by-state-product-bans-are-fueling-demand-letters-across-textiles-apparel-and-cosmetics/)).
- **2026 brought a "significant spike in plaintiff demand letters"** across textiles, apparel and cosmetics (same source). That's private enforcement.
- **New rules took effect on 1 Jan 2026** in CO, CT, ME, MN, VT and WA. Minnesota's reporting was due 1 Jul 2026, and further extensions are unverified ([Morgan Lewis](https://www.morganlewis.com/pubs/2026/01/state-regulation-of-pfas-in-consumer-products-continues-to-gain-momentum-in-2026)).
- **The pipeline is large:** nearly 100 new bills in 2026 plus 280 carried over ([MultiState](https://www.multistate.us/insider/2026/3/20/state-pfas-legislation-in-2026-hundreds-of-bills-across-23-states)).
- **Europe:** France's Law 2025-188 has applied since Jan 2026 ([Euronews](https://www.euronews.com/2026/01/01/frances-ban-on-forever-chemicals-comes-into-force-tomorrow-heres-what-will-change), [King & Spalding](https://www.kslaw.com/news-and-insights/france-adotps-a-law-banning-pfas-in-cosmetics-textiles-and-waxing-products)). Denmark sets 50 mg F/kg from 1 Jul 2026, with a sell-off period to 1 Jan 2027 ([SGS](https://www.sgs.com/en/news/2025/09/safeguards-14825-denmark-introduces-national-ban-on-pfas-in-clothing-and-footwear)).

**Competitors (checked)**
- **Enterprise supplier-survey platforms:** Assent, UL Solutions, Z2Data, iPoint, IntegrityNext, Certivo ([Z2Data list](https://www.z2data.com/insights/the-top-8-supplier-compliance-management-software-tools/), [Assent](https://www.assent.com/solutions/product-compliance/pfas/)). They're built for manufacturers with a compliance team.
- **Shopify App Store `site:` search** for "PFAS": only GPSR, PPWR, EUDR and EPR apps. **No PFAS app.**
- **Content trackers** (NonToxicLab, MultiState) are not tools.
- **Caveat:** Cosmetica's free INCI checker may already cover cosmetics ingredients, so **cosmetics comes last**. Launch with textiles, cookware and kids' products.

**Winning angle:** Shopify-native and self-serve at $39; a rules database plus supplier portal plus shipping blocks; the ban map as content.

**MVP (6 weeks)**
- A rules database (category × jurisdiction × date × threshold).
- Catalogue sync with LLM category mapping.
- A supplier portal using magic links sent **by the customer to their own suppliers**.
- The evidence vault.
- A shipping-zone helper.
- The California cookware disclosure block.
- Monthly law-change alerts.

**Inbound GTM plan**
- Posts:
  1. "PFAS ban map 2026: which of your products can't ship to which state." (map image)
  2. "The PFAS demand letter your apparel brand will get, and the 4 documents that end it."
  3. "France banned PFAS in clothing in January. Here's what that means for US brands shipping to Paris."
- SEO:
  - "PFAS ban [state] apparel/cookware";
  - "PFAS-free supplier declaration template";
  - "Minnesota PFAS reporting small business".
- Marketplace and viral loop: the Shopify App Store; the supplier portal (each supplier sees the brand's request); a "PFAS-checked" badge.

**Pricing.**
- Free: ban map + 10 SKUs.
- $39/month: 500 SKUs, supplier portal.
- $129/month: several brands, evidence vault, alerts.

**Biggest risk.**
- Brands often can't get reliable supplier data, and lab tests cost money.
- Enterprise vendors could launch small-business tiers.
- Keeping the rules database current is a heavy load for a solo founder.
- The legal-information boundary.

**Chance 3 / Scale 5.**

### AI-in-hiring disclosure → **folded into #20** (not counted)
The evidence supports the critic's recommendation to widen #20 rather than start a new product:
- **Illinois HB 3773** has been in force since 1 Jan 2026 (mandatory notice, no audit safe harbour) ([RatedWithAI](https://ratedwithai.com/blog/illinois-hb3773-ai-employment-discrimination-2026)).
- **NYC LL144** requires a bias audit plus 10-business-day notice.
- **Colorado repealed and replaced its AI Act with SB26-189**, a transparency-focused ADMT law **effective 1 Jan 2027** ([Davis Wright Tremaine](https://www.dwt.com/blogs/privacy--security-law-blog/2026/05/colorado-ai-act-repeal-new-transparency-law), [Skadden](https://www.skadden.com/insights/publications/2026/06/colorado-repeals-and-replaces-its-ai-act)).
- **Ontario** requires AI-use disclosure in job postings.

HireLaw Check adds an "AI-use notice" rule pack for the same buyers and the same Chrome extension. The notice-drafting space already has vendor content (Warden AI serves HR-tech vendors) and trackers (ailawsbystate.com), so it doesn't stand alone.

---

## 6. Pattern (b), connect-your-own-account benchmarks: no new idea passes

| Platform | Finding | Verdict |
|---|---|---|
| **YouTube Analytics API** | **The API policy forbids** compiling authorised data "unless … viewable ONLY to the content or channel owner", and bans custom scores from averages. Derived metrics need an audited quota-extension approval (from 1 Jun 2026) ([YouTube policies](https://developers.google.com/youtube/terms/developer-policies), [derived-metrics policy](https://developers.google.com/youtube/terms/derived-metrics-policy)). TubeAnalytics already sells niche benchmarks at $29 ([TubeAnalytics](https://www.tubeanalytics.net/product)). | **DROP** (policy + incumbent) |
| **App Store Connect / Google Play** | Apple shows native **peer-group benchmarks** ([Apple](https://developer.apple.com/help/app-store-connect-analytics/benchmarks/peer-group-benchmarks/)). RevenueCat publishes benchmarks from 115k apps plus a free "Subscription App Health" score ([RevenueCat](https://www.revenuecat.com/healthscore)). | **DROP** (rule c) |
| **Google Business Profile** | Already #2's hook | — |
| **Stripe for a vertical** | SaaS is covered (Baremetrics, ChartMogul, TrustMRR); AI apps by the Attrifast benchmark; boutique fitness by Boutique Benchmarks | **DROP** |
| **GA4 / Klaviyo / Mailchimp** | Native benchmarks [MEMORY for GA4 and Klaviyo] | **DROP** |
| **Etsy (correction)** | My round-4 reason was wrong. The better reasons: Etsy's own shop stats and Marketplace Insights, Etsy API commercial-access review, and low willingness to pay [unverified]. Any Etsy product would count as a vertical of #37, like #42. | Not a new idea |

**New evidence for #37 (both directions):** **Databox retired its Benchmarks and Benchmark Groups on 6 Apr 2026.** Those were pooled, anonymised peer benchmarks across GA4, Google Search Console and 130+ integrations ([Databox help](https://help.databox.com/overview-benchmark-groups)) [summary].
- *For #37:* the only multi-source pooled benchmark has left the market.
- *Against #37:* a funded company chose to shut it down, which fits the critic's worry that willingness to pay is weak. Its **agency tier** must carry the revenue.

---

## 7. Pattern (c), B2C: none passes (honest result)
I looked for a specific audience, a new 2025-26 problem, users who pay, and shareable output. Every candidate already has clone apps, usually within months, because consumer-app studios ship fast through the TikTok user-generated-video playbook. It's the same swarm dynamic as deadline-driven compliance.

| B2C candidate | New problem | Why it fails |
|---|---|---|
| US visa / ESTA social-media self-scan | F/M/J vetting (Jun 2025), H-1B (Dec 2025), ESTA proposal | VisaSocialCheck, VisaProfileScan, VisaClean ([VisaClean](https://visaclean.app/)); the ESTA rule is still unfinished and being scaled back ([Skift](https://skift.com/2026/05/22/cbp-social-media-vetting-proposal-revisions/)) |
| Rental-car AI damage proof | Hertz/Sixt UVeye scanners ([CBS](https://www.cbsnews.com/news/hertz-uveye-ai-tech-rental-car-inspections/)) | 6+ apps: Proofr, CarProof, Not My Dent!, Snap&Drive, CarRentPal, carseal ([App Store](https://apps.apple.com/us/app/proofr-rental-protection/id6745433033)) |
| Hyrox result analyser | Hyrox boom | HyroxDataLab, Hyroxy, Prommer, Repz, Hyrox Result API ([HyroxDataLab](https://hyroxdatalab.com/)) |
| UK vet price comparison | CMA order (Sept 2026) | The CMA mandates a price-comparison site, plus vetpricecomparison, WisePet, VetCostIndex ([GOV.UK](https://www.gov.uk/government/news/cma-concludes-market-investigation-with-major-reforms-to-veterinary-sector)) |
| Baby-food heavy-metal lot lookup | AB 899 + MD/VA/IL disclosure laws (2025-26) | The **Olive** app (subscription, own lab tests, recall alerts), Consumer Reports, HMTc ([Olive](https://apps.apple.com/us/app/olive-food-cosmetic-scanner/id6739765789), [CR](https://www.consumerreports.org/babies-kids/baby-food/baby-food-labels-heavy-metals-california-ab899-a5779555429/)) |
| "What does ChatGPT say about me" (individuals) | AI name searches | ReputationDefender, Repumatic, Whitebridge, plus the whole GEO category ([Repumatic](https://www.repumatic.com/ai-reputation-audit-what-do-chatgpt-google-ai-and-perplexity-say-about-your-name/)) |
| Prediction-market P&L and tax | Kalshi/Polymarket boom | PredictionTax, PolyTax ($99), TraderTax, Realize, CountDeFi ([Realize](https://realize.tax/)) |
| Tenant deposit photo proof | CA AB 2801 (2025) | The photo duty is the landlord's; generic timestamp cameras and car-proof apps cover tenants ([Timemark](https://www.timemark.com/blog/california-ab2801-photo-documentation-guide)) |
| Personal "AI-slop" or "AI music in my playlists" share cards | AI slop, 2025-26 | Free extensions; no willingness to pay; Spotify API restrictions [MEMORY] |
| Med-spa GLP-1 ad self-check (prosumer) | FDA warning letters (Mar/Jun 2026) | Loopholes, GetGenAI, AdShield, AuditSocials ([AdShield](https://www.adshield.dev/)) |

**What the founder *can* do in B2C:**
- **#41 LabelCheck** (creators) and **AuthorRadar** (authors) are already **prosumer B2C**: individuals paying €7-29. They're the closest fit in the valid list.
- Build **consumer front-ends of the B2B products as distribution, not revenue**:
  - a "true total price" extension for #44 (a public "hall of shame" as content);
  - parent recall alerts for #36;
  - an "Is this post an ad?" viewer overlay for #41.

---

## 8. Checked and dropped this round (beyond §6-§7)

| Candidate | Killer |
|---|---|
| US state privacy compliance for SMB websites | Swamped (rule b): Termly, iubenda, CookieYes, Osano, Enzuzo, Usercentrics, Cookiebot, Complianz… ([Usercentrics list](https://usercentrics.com/knowledge-hub/cookie-consent-tools/)) |
| Auto-renewal / click-to-cancel (US + UK) | RenewalMatrix and a second renewal-matrix connector; billing platforms (Stripe portal, Recharge) handle cancellation natively; the **UK regime is delayed to spring 2027** ([Reed Smith](https://www.reedsmith.com/articles/dmcc-subscription-rules-delayed-to-spring-2027-key-takeaways-from-the-consultation-response/)) |
| Prop 65 warnings for online sellers | 4+ Shopify warning apps (Warn, Warnify Pro, NotifyMe…) ([Shopify](https://apps.shopify.com/product-notes)) |
| AI voice-agent call-recording consent kit | Content-heavy vendor space (Retell, Thoughtly, Trillet), and **Cekura** tests voice-agent compliance ([Cekura](https://www.cekura.ai/discover/ai-voice-agent-compliance)); rule (c) risk from the platforms |
| Med-spa / telehealth ad compliance | Swamped: Loopholes, GetGenAI, AdShield, AuditSocials ([GetGenAI](https://www.getgen.ai/solutions/ftc-compliance-software)) |
| ChatGPT-Ads tools | (round 4) 5+ tools |
| CA SB 343 recyclability claims (Oct 2026) | How2Recycle is the dominant US label programme [MEMORY] |
| UK Renters' Rights / MTD for individuals | TLA, Lendlord, Goodlord; HMRC's list of 50+ MTD products [MEMORY] |

---

## 9. Updated pipeline after round 5

| Status | Ideas |
|---|---|
| **VALID (critic)** | #2 (5/7) · #7 (4/5) · #9 (4/4) · #20 (3/6, now with an AI-hiring module) · #12 (3/6) · #37 (3/5) · #41 (3/5) |
| **Conditions answered this round, awaiting the critic** | #36 SafetyRadar US-first (3/5 if ≥80% precision) · **CAIK = #38+#40** (3/4, waitlist test) · #39+#43 AuthorRadar (3/4, data-licence confirmation) |
| **New this round** | **#44 AllIn Check (3/6)** · **#45 PFAS Patchwork Check (3/5)** |
| Folded / conceded | #42 → #37 vertical · #30+#34 → distribution engine · #43 → #39's free hook |

**Projection:** 7 VALID today. If #44 and #45 survive and 1-2 of #36, CAIK and AuthorRadar convert, the total is **about 10-11**.

**My recommended first three builds for the founder:**
1. **#2** (highest Chance/Scale).
2. **#44 AllIn Check or #20 HireLaw.** Same extension engine, so build one and add the other as a rule pack.
3. **#41 LabelCheck** (the strongest content fit, prosumer B2C).

The build-in-public newsletter (§2) runs alongside all three as distribution.
