# Round 6 (Defender): build-ready launch cards

Author: DEFENDER, 2026-09-25.

Each card applies the critic's conditions and corrections from `04-critic-verdicts.md` and `05-critic-verdicts.md`.

- **Persona counts are rough.** Anything marked ~ is an order-of-magnitude estimate; [MEMORY] means it wasn't re-verified this session.
- **Default solo stack** (each card names only what differs):
  - Next.js on Vercel, Supabase (Postgres, auth, storage), Stripe Billing;
  - an LLM API (OpenAI or Anthropic), Trigger.dev or Inngest for scheduled jobs;
  - Resend for email, Plausible for analytics.
- **Revenue targets:** "€1k MRR by day 90" is a stretch target. The kill signals are set lower on purpose.

| # | Card | Status | C/S |
|---|---|---|---|
| 2 | KI-Empfehlungs-Index | VALID | 5/7 |
| 7 | LeanKeep | VALID | 4/5 |
| 9 | Nachfolge-Radar Weekly | VALID | 4/4 |
| 12 | SupportUntil (PSTI + CRA Kit) | VALID (slow-burn) | 3/6 |
| 20 | HireLaw Check (+ AI-in-hiring pack) | VALID | 3/6 |
| 37 | SearchShift (+ #42 InboxShift as vertical 2) | VALID | 3/5 |
| 41 | LabelCheck | VALID | 3/5 |
| 44 | AllIn Check | PENDING CRITIC | 3/6 |
| 45 | PFAS Patchwork Check | PENDING CRITIC | 3/5 |
| 36 | SafetyRadar US | PENDING CRITIC | 3/5 |
| 38+40 | CAIK (compliance kit for indie consumer-AI apps) | PENDING CRITIC | 3/4 |

---

## #2 "Wen empfiehlt die KI?" (VALID, 5/7)
**One-liner.** A public German index of which local businesses ChatGPT, Gemini and Perplexity recommend, plus a paid monitor for owners and agencies.
- German name: **KI-Empfehlungs-Index**. English: **AI Local Index**.

**Who pays.** Owners of non-medical DACH local businesses (critic's condition): ~80k salons, ~100k trade firms, ~50k tax practices in DE [MEMORY]. Plus local agencies (white-label).

**MVP (6 weeks)**
1. A prompt library per vertical × city, run through the **OpenAI Responses API web_search with `user_location`**, the Gemini API with Google Search grounding, and the Perplexity Sonar API. **No scraping of AI Mode.**
2. N=10 runs per prompt, aggregated as a **share of mentions**, matched to a Google Places ID (Places API).
3. Public index pages with a methodology page, plus correction and opt-out forms.
4. A free "Empfiehlt ChatGPT meinen Salon?" check, with an optional **Google Business Profile connect** that adds review-velocity percentiles.
5. A paid weekly monitor with a competitor diff and a fix list (reviews, schema.org, Das Örtliche/Gelbe Seiten/ProvenExpert).
6. An agency white-label PDF.

**Pricing.** €19 founding member (after the day-1 noise gate), then €29 for one location; €79 for multiple locations; €199 for agencies.

**Inbound GTM**
- Posts (LinkedIn and Instagram carousels, local Facebook and Reddit city groups):
  1. "Ich habe ChatGPT nach dem besten Friseur in 10 Städten gefragt, 100-mal." (index screenshot)
  2. "Dieser Kölner Salon wird von allen 3 KIs empfohlen. Das macht seine Website anders."
  3. "ChatGPT zeigt jetzt Werbung in DE. Wirst du noch organisch empfohlen?"
- SEO: programmatic "Beste [Beruf] [Stadt] laut ChatGPT" pages (10 cities × 1 vertical first, then 80 × 20).
- Listings and viral loop: OMR Reviews; a "Von der KI empfohlen 2026" badge that links back.

**2-week test (critic).**
- Days 1-2: noise gate. If top-3 overlap is below 60%, publish shares instead of ranks.
- Pass: ≥500 free checks, **≥15 paid founding members or ≥40 card-backed waitlist signups**, and ≥3 agency requests.

**90 days**
- Weeks 1-2: the test above.
- Weeks 3-8: monitor, fix list, agency PDF; 3 verticals × 20 cities.
- Weeks 9-12: agency affiliate (30%); target **€1k MRR** (e.g., 25 × €29 + 1 agency).

**Kill signal.** Fewer than 5 paid in the test: switch to agency-only pricing. Still under €300 MRR at day 90 with agency pricing: stop.

---

## #7 LeanKeep (VALID, 4/5)
**One-liner.** A program kit and proof metric that lets coaches show their rapid-weight-loss clients kept their muscle.

**Who pays.** Online coaches and personal trainers with clients losing weight fast (often on GLP-1s). There are ~350k US fitness trainers [MEMORY], and Trainerize and Everfit serve tens of thousands of coaching businesses [MEMORY]. English-first, global.

**MVP (6 weeks)**
1. 12-week strength-and-protein templates, in three levels.
2. A client PWA for check-ins: weight, waist, photos, and optional Withings, Fitbit or Google Health Connect import for body fat. It says honestly that this is a **proxy**.
3. A **Muscle Retention Score**: estimated lean mass kept, with a confidence band.
4. Opt-in branded result cards.
5. A coach dashboard with CSV export to Trainerize and Everfit.
6. **No drug log, no drug names** (HWG/FTC).

**Stack.** Default, plus a PWA, the Withings API, and Stripe Connect for gyms later.

**Pricing.** $19 founding coach; $29 for up to 15 clients; $79 unlimited; gyms $5 per client.

**Inbound GTM**
- Posts (Instagram Reels, TikTok, coach Facebook groups, r/personaltraining):
  1. "−14 kg, 91% of her muscle kept: the 12-week plan." (result card)
  2. "Coaches: the one number that proves you're not just a diet app."
  3. "3 mistakes that make rapid weight loss burn muscle."
- SEO: a free **Muscle Retention Calculator**, plus "how to coach clients on weight-loss medication" and "strength plan for rapid weight loss".
- Viral loop: every client card carries the coach's and LeanKeep's branding.

**2-week test (critic).**
- A free calculator and a template PDF, 6 short-form posts, and a $19 pre-sale.
- Pass: **≥150 coach signups and ≥15 paid pre-sales.**

**90 days**
- Weeks 1-2: the test.
- Weeks 3-8: templates, PWA, score, cards.
- Weeks 9-12: coach referral ($10 credit) and one continuing-education partner (inbound); target **$1k MRR** (~35 coaches).

**Kill signal.** Fewer than 5 pre-sales: pivot to a one-off $49-99 "rapid weight loss program kit" (critic's fallback). Under $300 MRR at day 90: stop.

**GDPR note.** EU client data counts as health data under Art. 9. Launch in the US and UK first, with explicit consent.

---

## #9 Nachfolge-Radar Weekly (VALID, 4/4)
**One-liner.** A neutral weekly digest of the best DACH businesses for sale, built on original summaries that link to the source ("link, don't copy").
- German name: **Nachfolge-Radar**. Later English edition: **Europe for Sale**.

**Who pays.**
- **Brokers and sellers** who pay to feature a listing.
- **Buyers**: search funders, MBI candidates, SMEs buying competitors, who pay for Pro alerts.
- **Advertisers**, through a public rate card.
- KfW counts about half a million SME owners seeking succession by 2028 [MEMORY].

**MVP (4 weeks; it's a media product)**
1. A beehiiv newsletter with 10 listings a week (2-3 original lines + link).
2. A free "list your business" seller form.
3. A Stripe checkout for "Feature your listing" (€49-99).
4. A public **rate card** plus a Passionfroot page (no outbound sponsor sales).
5. A Pro alerts tier (€19/month) filtered by sector, region and price.
6. SEO landing pages per sector and region.

**Stack.** beehiiv, Next.js pages, Supabase, Stripe. A manual curation workflow with an LLM summarisation assist.

**Inbound GTM**
- Posts (LinkedIn, X "boring business" format):
  1. "5 profitable German businesses for sale this week, all under €500k."
  2. "A 40-year-old bakery in Franconia: €180k EBITDA, no successor."
  3. "What a €1M Mittelstand deal actually looks like: 5 numbers."
- SEO: "[Branche] kaufen [Region]" and "Unternehmensnachfolge [Branche]" pages.
- Listings: newsletter directories (beehiiv Boosts, Swapstack-type).
- Viral loop: sellers share their featured badge, and forwards bring subscribers.

**2-week test (critic).**
- 2 issues, 6 posts, the rate card and the €49 checkout.
- Pass: **≥250 subscribers, ≥40% open rate, ≥2 paid features or inbound sponsor bookings.**

**90 days**
- Weeks 1-2: the test.
- Weeks 3-8: weekly issues, SEO pages, Pro alerts.
- Weeks 9-12: target 1,500 subscribers and **€500-1k a month** (features + Pro + 1 ad slot).

**Kill signal.** Fewer than 100 subscribers at week 2: test the English "Europe for Sale" edition. Under €200 a month at day 90 across both: stop.

---

## #12 SupportUntil: PSTI + CRA Kit and Security-Support Index (VALID, slow-burn, 3/6)
**One-liner.** A public "security updates until…" index of connected products, plus self-serve PSTI/CRA documents for small hardware brands.

**Who pays.** Small connected-product brands selling into the UK and EU: smart home, pet and baby tech, e-bikes, Kickstarter hardware, Amazon OEM sellers. That's ~thousands of brands [estimate]. UK distributors come second.

**MVP (6 weeks)**
1. A crawler that indexes **published** PSTI statements (links only) into "[brand] [model] updates until [date]" pages.
2. A PSTI statement generator per SKU.
3. A hosted VDP page plus security.txt generator.
4. An embeddable "Security updates until 2030" badge (Shopify widget + an image for Amazon).
5. A CRA checklist and templates for the reports to ENISA (CRA reporting has been live since 11 Sep 2026).

**Stack.** Default, plus Playwright for the crawler (public PDFs only) and a Shopify app (Remix template) for the badge.

**Pricing.** Free for 1 SKU; $29/month for 20 SKUs plus VDP hosting; $99/month for the CRA pack.

**Inbound GTM**
- Posts (Reddit r/homeautomation, r/hardware, LinkedIn, Kickstarter creator groups):
  1. "Your smart doorbell stops getting updates in 2027. We indexed 300 PSTI statements."
  2. "The 20 smart-home brands with the longest security support."
  3. "Shipping hardware to the UK: the 3 documents you need."
- SEO: programmatic model pages, plus "PSTI statement template" and "CRA checklist small manufacturer" free tools.
- Marketplace: the Shopify App Store (badge).
- Viral loop: badges link to the index, and press cites the index.

**2-week test (critic).**
- Index of 300 statements, the free generator, the posts.
- Pass: **≥50 brand generator completions, ≥5 signups for the $29 waitlist, and ≥1 press or newsletter pickup.**

**90 days**
- Weeks 1-2: the test.
- Weeks 3-8: VDP hosting, badge app, CRA pack.
- Weeks 9-12: 1,000 index pages; target **$300-500 MRR**. Revenue is expected in 2027 (CRA full obligations, 11 Dec 2027).

**Kill signal.** Fewer than 10 brand completions: keep the index as a passive SEO asset and revisit in Q2 2027. **Don't make this the first build.**

---

## #20 HireLaw Check, with the AI-in-hiring rule pack (VALID, 3/6)
**One-liner.** A Chrome extension and checker that flags job ads breaking pay-transparency and AI-hiring notice rules across US states, Canada and the EU.

**Who pays.** **Staffing agencies and SMB recruiters outside Greenhouse and Ashby**, which already auto-fill pay ranges (critic's rule (c)). That means Workable, BambooHR, JazzHR, and direct Indeed or LinkedIn posting. There are ~20k+ US staffing firms [MEMORY].

**MVP (7 weeks)**
1. A rules engine: 16 states + DC, NYC and Ohio cities, Ontario, and EU countries as they transpose.
2. The **AI-in-hiring pack**:
   - Illinois HB 3773 notice (since 1 Jan 2026);
   - NYC LL144 audit notice (10 business days);
   - Ontario AI disclosure;
   - Colorado SB26-189 from 1 Jan 2027.
3. A paste/URL checker.
4. A Chrome extension (Plasmo) inside the LinkedIn, Indeed and Workable editors.
5. A bulk scan of **public Greenhouse, Lever and Ashby board JSON**.
6. A "Pay-transparent employer" badge.

**Stack.** Default, plus Plasmo and the public ATS board endpoints.

**Pricing.** Free for a single ad; $49/month for SMBs (50 live postings); $149/month for agencies.

**Inbound GTM**
- Posts (LinkedIn recruiter groups, r/recruiting, staffing-association groups as a participant):
  1. "We checked 5,000 public job ads for WA, CO and Ontario roles: X% have no valid range." (aggregates only)
  2. "Illinois now requires an AI notice in hiring. Here's the 2-line version."
  3. "The pay-transparency map 2026, in one picture."
- SEO: programmatic "pay transparency law [state/province/country]" and "AI hiring notice [jurisdiction]" pages.
- Marketplace: Chrome Web Store (Workable and Lever partner directories later).
- Viral loop: the careers-page badge.

**2-week test (critic).**
- A free checker plus a minimal extension, one data post, and a $49 agency plan with card pre-authorisation.
- Pass: **≥300 checks, ≥50 installs, ≥10 agency pre-authorisations.**

**90 days**
- Weeks 1-2: the test.
- Weeks 3-8: the full rules engine, the AI pack, bulk scan.
- Weeks 9-12: target **$1k MRR** (~20 SMBs or 7 agencies).

**Kill signal.** Fewer than 3 pre-authorisations: park until **Jul 2027**, when Washington's cure period ends and the EU transposes.

---

## #37 SearchShift, with #42 InboxShift as vertical 2 (VALID, 3/5)
**One-liner.** Connect Search Console to find out "is it me or Google?", with your AI-era traffic shift benchmarked against anonymous peers in your niche.

**Who pays.**
- **SEO agencies**: the critic says the agency tier must carry revenue. There are ~tens of thousands worldwide [estimate].
- Niche publishers and content-led SaaS teams on the free or cheap tier.

**MVP (6 weeks)**
1. Search Console OAuth (`webmasters.readonly`), with Google OAuth verification and a published privacy policy.
2. **Explicit consent to pooling.**
3. LLM niche classification.
4. k-anonymous pools (n≥20 per niche × country).
5. Share cards and a weekly public Search Traffic Index.
6. An agency white-label PDF.

**Vertical 2 (#42):** only after this card's test passes. Kit App Store OAuth (v4 broadcast stats) plus the Ghost Admin API, as a click benchmark.

**Pricing.** Free for 1 site; $12/month (history, alerts, 5 sites); $49/month for agencies.

**Inbound GTM**
- Posts (X SEO community, r/SEO, r/juststart, r/Blogging, Indie Hackers, LinkedIn):
  1. "412 sites connected: recipe sites −41% clicks year on year, SaaS docs +8%." (live counter)
  2. "Is it you or Google? Compare against 300 peers in 60 seconds." (share card)
  3. "Databox killed its benchmarks in April. Here's the free, pooled replacement."
- SEO: "[niche] Google traffic drop 2026" and "AI Overviews impact [niche]"; the index pages themselves.
- Listings: Product Hunt, SEO tool directories.
- Viral loop: share cards, plus "benchmarked by SearchShift" in agency PDFs.

**2-week test (critic).**
- Launch the connect-and-compare tool with a public counter.
- Pass: **≥400 connected sites, ≥3 niches with n≥20, ≥10 agency waitlist signups at $49.**

**90 days**
- Weeks 1-2: the test.
- Weeks 3-8: agency PDF, alerts, weekly index.
- Weeks 9-12: InboxShift beta (only if the test passed); target **$500-1k MRR** (10-20 agencies).

**Kill signal.** Fewer than 150 connected sites in the test: the data flywheel won't start. Stop, and drop #42 too.

---

## #41 LabelCheck (VALID, 3/5)
**One-liner.** A creator-side check that each post carries the ad and AI labels your country requires.
- German name: **Werbekennzeichnung-Check**.

**Who pays.** **Influencer agencies and talent managers** are the real buyers: France makes advertiser, agency and influencer jointly liable. Then EU creators with brand deals (DE, FR, IT, ES, NL): ~tens of thousands of monetising creators [estimate]. UK and US FTC editions follow.

**MVP (6 weeks)**
1. A **paste-URL/screenshot checker first**, with no OAuth needed (this sidesteps Meta's and TikTok's app review).
2. OCR of caption, thumbnail and first frame.
3. An LLM classifier for commercial signals (brand tags, codes, affiliate links, gifted products).
4. **Fixed rule packs** per country: DE "Werbung/Anzeige" visible up front, FR "Publicité/Collaboration commerciale" plus "Image retouchée/virtuelle", IT, ES, UK, US. Fixed rules keep it on the right side of the RDG.
5. An AI Act Art. 50 deepfake-label check.
6. A **Canva app** (external payments allowed) that stamps compliant labels. Instagram, TikTok and YouTube OAuth comes in week 8+.

**Stack.** Default, plus the Canva Apps SDK and the Meta and TikTok APIs (later).

**Pricing.** A free check; €9/month per creator; **€49/month for agencies** (20 creators, campaign pre-flight).

**Inbound GTM**
- Posts (Instagram Reels, TikTok, LinkedIn for agencies):
  1. "Ich habe 200 meiner Posts gescannt: 14 wären abmahnfähig."
  2. "Werbung vs Anzeige vs Publicité vs #ad vs KI-Label: the EU cheat sheet." (carousel)
  3. "France requires 'Image virtuelle' on AI images. How 30 big accounts handle it."
- SEO: "Werbekennzeichnung Instagram richtig", "collaboration commerciale mention obligatoire", "KI-Bilder kennzeichnen Influencer".
- Marketplace: the Canva Apps Marketplace.
- Viral loop: a "Label-safe" media-kit badge, plus agency white-label.

**2-week test (critic).**
- Paste checker, cheat sheet, 6 videos, €9 and €49 pre-sales.
- Pass: **≥500 checks, ≥20 creator pre-sales or ≥5 agency pre-sales, and ≥1 agency white-label request.**

**90 days**
- Weeks 1-2: the test.
- Weeks 3-8: rule packs, Canva app, OAuth submission.
- Weeks 9-12: target **€1k MRR** (e.g., 12 agencies + 40 creators).

**Kill signal.** Fewer than 5 total pre-sales: pivot to an agency-only campaign pre-flight checker. Under €300 MRR at day 90: stop.

---

## #44 AllIn Check (PENDING CRITIC, 3/6)
**One-liner.** A Chrome extension that walks your checkout and flags hidden fees, jurisdiction by jurisdiction.

**Who pays.**
- Vacation-rental direct-booking sites and independent hotels: ~tens of thousands in the US and UK [estimate].
- Independent venues and ticket sellers.
- Gyms and studios.
- The web agencies that build their booking flows.

**MVP (6 weeks)**
1. A Plasmo extension that captures the displayed price and network responses at each checkout step.
2. LLM extraction of the fee components.
3. A rules engine: the FTC fee rule (tickets and lodging); CA SB 478; MN; VA; CO (1 Jan 2026); CT (1 Jul 2026); MA; the UK DMCC Act; the EU.
4. A report plus an "All-in verified" badge.
5. Weekly headless re-checks (Playwright) for simple flows.
6. A WordPress plugin for booking sites.

**Pricing.** A free one-off check; $29/month for 1 site with monitoring and the badge; $99/month for agencies and property managers (20 sites).

**Inbound GTM**
- Posts (LinkedIn, r/airbnb_hosts, r/VacationRental, hospitality groups):
  1. "We checked 200 direct-booking sites: 6 in 10 add the cleaning fee at the last step."
  2. "The all-in pricing map 2026: 8 US states + UK + EU."
  3. "Connecticut changed on 1 July. Is your gym's 'admin fee' now illegal?"
- SEO: "SB 478 compliance checker", "junk fee law [state]", "drip pricing UK".
- Marketplaces: Chrome Web Store, WordPress.org.
- Viral loop: the badge.

**2-week test (proposed).**
- A free extension, the 200-site aggregate post, and a $29 pre-sale.
- Pass: **≥300 checks, ≥10 paid or pre-authorised, and ≥2 agency requests.**

**90 days**
- Weeks 1-2: the test.
- Weeks 3-8: rules, monitoring, WordPress plugin.
- Weeks 9-12: target **$1k MRR** (~35 sites).

**Kill signal.** Fewer than 3 pre-sales, **or** most prospects run booking engines that are already compliant: stop.

---

## #45 PFAS Patchwork Check (PENDING CRITIC, 3/5)
**One-liner.** A Shopify app showing which products can't ship where because of PFAS bans, with supplier declarations, shipping blocks and an evidence vault.

**Who pays.** DTC apparel, outdoor, textile, cookware and kids' brands on Shopify that sell into the US, France or Denmark. That's ~tens of thousands of stores [estimate]. **Cosmetics comes last**, because Cosmetica's free INCI checker may already serve that segment.

**MVP (7 weeks)**
1. A rules database: category × jurisdiction × effective date × threshold. It covers 18+ states, CA 100→50 ppm (2027), France (Jan 2026) and Denmark (Jul 2026).
2. Catalogue sync plus LLM category mapping (Shopify Admin API).
3. A supplier portal: the brand sends magic links to *its own* suppliers.
4. An evidence vault for lab reports (ppm vs threshold).
5. A shipping-zone block helper.
6. A California cookware-disclosure snippet, plus monthly law alerts.

**Stack.** A Shopify Remix app template with the default stack.

**Pricing.** Free: ban map + 10 SKUs; $39/month (500 SKUs + portal); $129/month (several brands, vault, alerts).

**Inbound GTM**
- Posts (LinkedIn, r/shopify, r/ecommerce, DTC Twitter):
  1. "PFAS ban map 2026: what can't ship where." (map image)
  2. "The PFAS demand letter your apparel brand will get, and the 4 documents that end it."
  3. "France banned PFAS in clothing in January. What US brands shipping to Paris must do."
- SEO: "PFAS ban [state] [category]", a free "PFAS-free supplier declaration template".
- Marketplace: the Shopify App Store.
- Viral loop: the supplier portal and a "PFAS-checked" badge.

**2-week test (proposed).**
- A free ban map plus the declaration template, 3 posts, and a $39 waitlist.
- Pass: **≥200 map users, ≥50 template downloads, ≥10 card-backed waitlist signups.**

**90 days**
- Weeks 1-2: the test.
- Weeks 3-9: the app.
- Weeks 10-12: target **$500-1k MRR**.

**Kill signal.** Fewer than 3 waitlist signups, or brands can't get supplier data at all: stop.

---

## #36 SafetyRadar US (PENDING CRITIC, 3/5 if precision ≥80%)
**One-liner.** A Shopify app that alerts resellers when a product they sell is recalled in the US, Canada, Australia or the UK. Selling a recalled product is illegal under CPSA §19.

**Who pays.** US Shopify and WooCommerce **resellers** of toys, baby products, electronics and household goods: ~tens of thousands of stores [estimate]. Dropshippers come second.

**MVP (6 weeks)**
1. Feed ingestion: the CPSC Recalls API, openFDA enforcement, Health Canada open data, ACCC, UK OPSS.
2. Tiered matching:
   - T1: exact barcode (GTIN) match;
   - T2: brand plus model number;
   - T3: LLM verifier, flagging only at confidence ≥0.9;
   - T4: hazard digest, never a flag.
3. An alert inbox plus a PDF action log (proof of §19 diligence).
4. Weekly public "Recalled this week" pages.
5. A free parent-alert email list, used as distribution.

**Stack.** A Shopify Remix app, plus Supabase pgvector and CLIP embeddings for image review suggestions.

**Pricing.** Free for 25 SKUs; $19/month for 500 SKUs; $49/month for several stores and all feeds.

**Inbound GTM**
- Posts (r/shopify, r/FulfillmentByAmazon, LinkedIn, parent groups for the free alerts):
  1. "Amazon was named in 61% of 2026 US recalls. Is your catalogue next?"
  2. "Recalled this week: 9 kids' products still for sale online." (official notices only)
  3. "Home Depot paid $5.7M for selling recalled products. The one check resellers skip."
- SEO: "[brand] recall [year]" and "[product type] recall" pages.
- Marketplaces: the Shopify App Store, WooCommerce.com.
- Viral loop: the free parent alerts.

**2-week test (critic).**
- 1,000 SKUs from 5 resellers.
- Pass: **≥80% precision on flags.** Coverage is reported honestly.
- Commercial pass: ≥30 installs and ≥5 paid within 4 weeks.

**90 days**
- Weeks 1-2: the precision test.
- Weeks 3-8: the app.
- Weeks 9-12: target **$500 MRR**.

**Kill signal.** Precision below 80% after tuning: **concede** (as committed in round 5).

---

## #38+#40 CAIK: compliance kit for indie consumer-AI apps (PENDING CRITIC, 3/4)
**One-liner.** A drop-in SDK covering chatbot-law disclosures, crisis routing, protocol pages and 48-hour takedowns for small AI chat and image apps.

**Who pays.** SFW, revenue-generating small studios: of the **337 revenue-earning AI companion apps**, a long tail of about 300 small ones (Appfigures); plus AI tutor and wellness chat apps, and AI image/video apps with public galleries. That's ~1-2k buyers globally [estimate]. **NSFW is excluded.**

**MVP (6 weeks)**
1. TS/Python middleware:
   - AI-disclosure and break-reminder timers (every 3 hours in CA and OR, every hour in WA);
   - Koko (Keywords + Helplines APIs) and ThroughLine adapters, plus the model vendor's moderation;
   - **no detection built in-house.**
2. A hosted crisis-response protocol page generator (SB 243 requires publication).
3. An evidence log plus an export for the CA Office of Suicide Prevention report (from Jul 2027).
4. A TIDA intake form, 48-hour SLA timer, paging and PDQ hashing.
5. A jurisdiction checklist (CA, NY, OR, WA, EU AI Act Art. 50, DSA, UK OSA).

**Pricing.** Free protocol page and components; $49/month for chat; $79/month for image; $149/month bundle.

**Inbound GTM**
- Posts (X, Hacker News, r/SideProject, Indie Hackers, the RevenueCat community):
  1. "We audited 100 AI apps' public pages: most lack the crisis protocol SB 243 requires."
  2. "SB 243 in 12 lines of code."
  3. "CA vs NY vs OR vs WA vs EU: what your AI app must show, in one table."
- SEO: "SB 243 compliance checklist", "Take It Down Act AI image app", "crisis protocol template".
- Distribution: npm/PyPI; snippets for Rork, Vibecode, Lovable and Bolt; the founder's build-in-public newsletter.
- Viral loop: "Protocol hosted by CAIK" backlinks.

**2-week test (critic).**
- The free generator plus the 100-app index.
- Pass: **≥10 SFW revenue-generating teams on a card-backed waitlist within 4 weeks.**

**90 days**
- Weeks 1-4: the test.
- Weeks 5-10: chat and image modules.
- Weeks 11-12: target **$1k MRR** (~10 teams).

**Kill signal.** Fewer than 5 waitlist teams: stop. Keep only the free generator as an SEO asset.
