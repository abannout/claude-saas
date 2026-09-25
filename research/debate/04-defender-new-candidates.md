# Round 4 (Defender): new candidates #38-#43

Author: DEFENDER, 2026-09-25.

Founder rules applied:
- Inbound only.
- Success chance and scale come first.
- Thin wrappers are fine.
- Global by default.

Calibration applied (from the coordinator): criterion 2 means **no dominant solution**. One to three small indie competitors are acceptable if the founder has a different audience, language, channel or content angle. An idea fails when any of these is true:
- a funded or dominant player, a free official tool, or the platform itself already serves this exact audience;
- there are 5 or more near-identical tools;
- a big platform has already shipped or announced the feature.

Method:
- Google-style searches.
- `site:`-filtered searches of the Shopify App Store, Chrome Web Store and WordPress.org.
- GitHub repository search.
- Vendor and law-firm pages.
- Many direct page fetches were blocked by the egress proxy (Kit, Canva, meta.discourse.org, vr.org and others), so some facts come from search-result summaries. They are flagged **[summary]**.
- Facts from memory that I could not re-check are flagged **[MEMORY]**.

## 0. Decisions at a glance

| # | Idea | Direction | Geography | C/S |
|---|---|---|---|---|
| 38 | **CompanionSafe**: compliance kit for AI companion and character chatbots (SB 243, NY, OR, WA, EU AI Act Art. 50) | own (UGC-compliance family) | Global (US laws, EU) | **3/5** |
| 39 | **KnockoffWatch**: alerts for AI knockoffs and author-name impersonation on Amazon | #5 creator impersonation | Global | **3/4** |
| 40 | **TakedownDesk**: 48-hour takedown desk for small UGC services and AI image apps (TIDA, DSA Art. 16, UK OSA, DMCA) | #4 UGC compliance | Global | **3/4** |
| 41 | **LabelCheck**: creator-side check of your own posts for ad and AI labels, per EU country | own (revives a round-3 drop under the new calibration) | EU-first, then UK/US | **3/4** |
| 42 | **InboxShift**: connect Kit or Ghost for a click benchmark against peers in the AI-inbox era, with a share card | #8 connect-your-account | Global | **3/4** |
| 43 | **ShelfShift**: "is it AI or is it me?" sales benchmark for nonfiction authors (report upload) | #8 plus own | Global | **2/4** (3/4 if merged into #39) |

**Portfolio note.** The six ideas form two buyer clusters and one pattern family:
- #38 and #40 sell to the same buyer (small AI and UGC app teams) and could share one "trust and safety for indie apps" brand.
- #39 and #43 sell to authors and could share one "AuthorRadar" brand. #43 then becomes #39's free hook.
- #42 and #43 reuse #37 SearchShift's engine (pooled first-party benchmark, share card, public index), which is the critic's recommended pattern.

**Directions that failed** (details in §7):
- n8n agency monitoring: Administrate already sells the exact ROI report.
- Short-term-rental compliance: Chekin dominates; registration is a one-off task.
- Fake-review extension: 5+ clones.
- Music and video impersonation: Spotify and YouTube shipped the features themselves.
- New app stores: mostly no monetisation or no distribution.
- Localisation: no new candidate passed.
- Connect-account benchmarks: Patreon, Gumroad, Etsy and Lemon Squeezy all failed.

---

## 1. #38 **CompanionSafe**: compliance kit for AI companion and character chatbots (C3/S5)

**Pitch.** A drop-in SDK (TS/Python middleware around the LLM call) plus a dashboard. It gives an AI companion, character, AI-friend, tutor or wellness chat app the pieces the new chatbot laws require:
1. **AI disclosure** at session start and on a recurring timer (every 3 hours for minors in CA and OR; every hour in WA).
2. **Detection of suicidal ideation and self-harm** in user messages, with a localised crisis referral (988, Samaritans, TelefonSeelsorge and others).
3. A **minor mode** (self-attestation or an app-store age signal) with break reminders and content limits.
4. A **hosted public "Crisis Response Protocol" page.** SB 243 requires operators to publish their protocol.
5. An **evidence log** that exports to the annual report to the California Office of Suicide Prevention, due from 1 Jul 2027.
6. A **jurisdiction matrix** (CA, NY, OR, WA, EU AI Act Art. 50(1)).

**Audience.** Global. Small and indie studios behind AI companion and character apps, AI tutors and teen-facing chat apps, AI coaching and wellness chats, and companion bots on Discord or Telegram. Many earn real subscription revenue through app stores and Stripe.

**Why now**
- **California SB 243 has been in force since 1 Jan 2026.** It requires disclosure, a crisis-referral protocol published on the website, 3-hourly break reminders for minors, and annual reporting from 1 Jul 2027. It includes a **private right of action with at least $1,000 per violation** ([Skadden](https://www.skadden.com/insights/publications/2025/10/new-california-companion-chatbot-law), [NatLawReview](https://natlawreview.com/article/when-ai-feels-human-californias-sb-243-opens-door-private-lawsuits), [bill text](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202520260SB243)).
- **New York's AI-companion safeguard law** is already in effect ([Fenwick](https://www.fenwick.com/insights/publications/new-yorks-ai-companion-safeguard-law-takes-effect)).
- **Oregon SB 1546** (private right of action, $1,000 per violation) and **Washington HB 2225** (disclosure to minors every hour) were signed in March 2026 and take effect on 1 Jan 2027 ([Mayer Brown](https://www.mayerbrown.com/en/insights/publications/2026/04/oregon-and-washington-join-california-in-enacting-companion-chatbot-laws), [FPF comparison chart](https://fpf.org/wp-content/uploads/2026/04/Comparison-Chart_-Chatbot-Laws-Oregons-SB-1546-Washingtons-HB-2225-and-Californias-SB-243.pdf)).
- **78 chatbot bills were filed in 27 states** in the first weeks of 2026 ([Baker Botts](https://ourtake.bakerbotts.com/post/102mipe/ai-chatbot-regulation-78-state-bills-58-lawsuits)). The rules will multiply.
- The **FTC opened a 6(b) inquiry into AI companions** (Sept 2025; Alphabet, Character.AI, Instagram, Meta, OpenAI, Snap, xAI) ([FTC](https://www.ftc.gov/news-events/news/press-releases/2025/09/ftc-launches-inquiry-ai-chatbots-acting-companions)).
- **EU AI Act Art. 50** transparency duties (disclosure that users are talking to AI) apply from **2 Aug 2026 and were not postponed** by the Digital Omnibus ([aiactblog.nl](https://www.aiactblog.nl/en/posts/article-50-transparency-obligations-practical-2026), [EC FAQ](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).
- **Indie teams are building this by hand.** One public example is a GitHub PR titled "Publish the crisis response protocol at /safety (SB 243)" ([GitHub](https://github.com/hunterblack/closer-ai-web/pull/5)).

**Competitors (checked).** Google and GitHub searches found **no SB 243 compliance kit or SDK**.
- **ThroughLine** provides crisis-helpline infrastructure for platforms ([ThroughLine](https://www.throughlinecare.com/)). It's a data partner, not a compliance kit; its pricing is unverified.
- **Limina** does PII redaction for chatbot transcripts and markets it around SB 243 ([Limina](https://www.getlimina.ai/en/blog/california-sb-243-companion-chatbot-law)). It's adjacent, not a competitor.
- **Enterprise trust-and-safety vendors** (Hive, ActiveFence, Checkstep) sell through sales teams [MEMORY].
- **Law-firm guides** are free, but they're text, not code.

**Winning angle:** self-serve, installable in an hour, priced for 1-10 person studios, covering several jurisdictions, with a public index as content.

**MVP (5-6 weeks)**
- The middleware SDK.
- Risk classification: an open model with an LLM fallback.
- A helpline directory for 30 countries.
- UI components for disclosure and break reminders (web, React Native, Flutter).
- A protocol-page generator.
- An incident log with export.
- A jurisdiction checklist.

**Inbound GTM plan**
- Posts:
  1. "We checked the websites of 50 top AI companion apps: most haven't published the crisis protocol SB 243 requires." (public pages only)
  2. "SB 243 in 12 lines of code: disclosure, break reminders, crisis referral." (code screenshot)
  3. "CA vs NY vs OR vs WA vs EU in one table: what your AI chat app must show, and when."
- SEO:
  - "SB 243 compliance checklist";
  - "companion chatbot law [state]";
  - "crisis response protocol template";
  - "AI Act Article 50 chatbot disclosure".
- Marketplace and viral loop:
  - npm and PyPI packages, plus GitHub;
  - every hosted protocol page carries "Protocol hosted by CompanionSafe";
  - indie AI-app communities (r/SaaS, r/iOSProgramming, the RevenueCat community).

**Pricing.**
- Free: disclosure components and a protocol page.
- $49/month: classifier up to 100k messages, plus logs.
- $199/month: several apps, minor mode, and the annual-report export.

**Biggest risk.**
- **Life-safety domain.** Classifier misses create liability. The product must be positioned as a tool, not legal advice, and the helpline data must be reviewed by humans.
- Model vendors (OpenAI and others) may ship safety defaults that cover part of it.
- Some companion apps are adult-content businesses, so they are unattractive customers.
- A federal push against state AI laws could narrow the rules, although child-safety carve-outs are likely [MEMORY].
- **No lawsuit under SB 243 was found yet [unverified].**

**Chance 3 / Scale 5.** The buyers have money, and legal exposure grows every legislative session. There's no incumbent. Chance isn't 4 only because I haven't found filed SB 243 cases yet, unlike the ~700 suits behind #20.

---

## 2. #39 **KnockoffWatch**: alerts for AI knockoffs and author-name impersonation (C3/S4)

**Pitch.** Enter your books (ASIN or ISBN, title) and pen names. Every day KnockoffWatch scans the Amazon marketplaces (US, UK, DE, FR, ES, IT, CA, AU) through **licensed data**, meaning the Keepa API and/or Amazon's Creators API, plus the Google Books API. It looks for:
- new "Summary of…", "Workbook for…", "Study guide…" and "Companion to…" listings;
- near-identical titles;
- look-alike covers (image embeddings);
- **books published under your name that you didn't write.**

Within 24 hours you get an alert, an evidence PDF and pre-filled text for Amazon's reporting forms. A free public **Knockoff Tracker** covers the current bestsellers.

**Audience.** Global.
- Indie (KDP) authors and traditionally published authors.
- Small presses and literary agents.
- Nonfiction first, because summaries and workbooks cluster there.

**Why now**
- **Rolling Stone** investigated the flood of AI knockoffs on Amazon ([Rolling Stone](https://www.rollingstone.com/culture/culture-features/amazon-ai-book-knockoffs-1235450690/)). The **Authors Guild** reports "a new surge of sham books" ([Authors Guild](https://authorsguild.org/news/ai-driving-new-surge-of-sham-books-on-amazon/)).
- **Knockoffs appear within days of launch.** Marie Arana, president of the Authors Guild Foundation, found "A Summary of LatinoLand" listed under her book the day after release. Authors still catch these by checking by hand ([The Inkplots](https://www.theinkplots.com/p/the-scam-books-showing-up-days-after)).
- **How-to nonfiction is already under AI pressure** (see #43), so every diverted sale hurts more.
- **Data access is legitimate.** Amazon moved its product API to the OAuth-based **Creators API**, and PA-API retired on 15 May 2026 ([dev.to](https://dev.to/th3nate/amazon-pa-api-v5-is-shutting-down-april-30-2026-here-is-what-changes-at-the-auth-layer-22ek), [Amazon doc](https://affiliate-program.amazon.com/creatorsapi/docs/en-us/paapiv5-deprecation)). The **Keepa API** supports keyword product search ([Keepa docs](https://keepa.com/api-docs/)). The founder never scrapes Amazon.

**Competitors (checked).** Google found **no dedicated knockoff monitor for authors**; Amazon acts only on reports.
- **Book Defender** and **Blasty** fight *piracy* (DMCA takedowns on pirate sites), not Amazon knockoffs. A search summary puts Book Defender at about $500-800 per catalogue [summary] ([Book Defender](https://bookdefender.com/)).
- The **Chrome Web Store** has only KDP keyword and niche tools (KDP Scout, KDP Tools) and fake-review extensions ([KDP Scout](https://chromewebstore.google.com/detail/kdp-scout/oihnmfgccedimdhabjedohdmfcibdhoh)).
- **Brand-protection vendors** (Red Points) are enterprise ([Red Points](https://www.redpoints.com/blog/remove-counterfeit-amazon/)).

**Winning angle:** built for authors, focused on launch week, priced at $9, with the public tracker as the content engine.

**MVP (4-5 weeks)**
- A watchlist.
- Daily Keepa and Google Books queries for each marketplace.
- Fuzzy title matching plus an LLM classifier (summary, workbook, impersonation).
- CLIP cover similarity.
- Email alerts and an evidence PDF.
- Public tracker pages for the NYT and Amazon bestseller lists.

**Inbound GTM plan**
- Posts:
  1. "Every book on this week's NYT nonfiction list got a 'summary' knockoff within 72 hours. Receipts." (factual screenshots of public listings, no accusations)
  2. "Launch-day checklist: the 5 knockoff types to look for. We automate it."
  3. "3 books 'by' [author] that [author] never wrote." (with the author's consent)
- SEO:
  - "[title] summary knockoff";
  - "report AI knockoff book Amazon";
  - "someone published a book under my name".
- Viral loop: a free one-off "Does my book have knockoffs?" scan with a shareable result card. Author newsletters and communities (r/selfpublish, writer Discords) pass it on. A reader-side Chrome flag comes later.

**Pricing.**
- A free one-off scan.
- $9/month: 5 titles, checked daily.
- $29/month: 50 titles, with pen names.
- $99/month: presses and agents, 500 titles.

**Biggest risk.**
- **Data terms.** The Creators API and Associates terms tie use to referrals, and Keepa's redistribution terms are unverified. Evidence must stay private to the user, and the tracker should link out rather than republish.
- Amazon could ship an author alert itself.
- Removal depends on Amazon.
- Defamation risk on the public tracker (keep to neutral facts).

**Chance 3 / Scale 4.**

---

## 3. #40 **TakedownDesk**: 48-hour takedown desk for small UGC services and AI image apps (C3/S4)

**Pitch.** One embeddable report form, and one inbox, for every takedown regime a small UGC service faces:
- **TAKE IT DOWN Act** (non-consensual intimate images, including AI "digital forgeries", 48 hours);
- **EU DSA Art. 16** notice-and-action, with statement-of-reasons templates;
- **UK OSA** complaints and record-keeping;
- **DMCA.**

The desk adds:
- SLA timers with Slack, SMS or email paging;
- duplicate removal through perceptual hashes (PDQ), with no images stored;
- an audit log and exports for transparency reports;
- plugins for Discourse, WordPress/BuddyPress and XenForo, plus an API for indie apps.

**Audience.** Global.
- AI image and video generator apps with public galleries.
- Indie social apps.
- Forums and community sites.
- Small creator platforms.

**Why now**
- **TIDA enforcement began on 19 May 2026.** The FTC warned at least 15 companies beforehand. Penalties run up to **$53,088 per violation**. The FTC recommends request tracking and hashing, and it runs **TakeItDown.ftc.gov** for complaints ([FTC blog](https://www.ftc.gov/business-guidance/blog/2026/05/take-it-down-act-enforcement-starts-now-what-know-about-ftc-tida), [WilmerHale](https://www.wilmerhale.com/en/insights/client-alerts/20260615-the-take-it-down-act-goes-live), [Orrick](https://www.orrick.com/en/Insights/2026/06/Nonconsensual-Intimate-Images-Online-Take-It-Down-Act-Enforcement-In-Full-Swing)).
- **The FTC reads "covered platform" broadly:** messaging, gaming and image-sharing forums ([McNees](https://www.mcneeslaw.com/take-it-down-act-ftc-compliance-enforcement/)).
- A small-business guide puts it plainly: "a form that creates a ticket and pages the on-call moderator is worth more than a sophisticated detection model" ([beancount.io](https://beancount.io/blog/2026/08/13/take-it-down-act-48-hour-takedown-small-business-compliance-guide)). That's the MVP.
- **Small community admins are asking for help.** Discourse Meta has 2026 threads on DSA statements of reasons and the annual DSA workflow ([thread 1](https://meta.discourse.org/t/dsa-content-moderation-reporting-statements-of-reasons-requirements/409681), [thread 2](https://meta.discourse.org/t/whats-your-workflow-for-the-annual-eu-dsa-compliance/396390)). The existing "Legal Compliance" Discourse plugin only adds an upload-search filter; I checked its `plugin.rb` ([GitHub](https://github.com/communiteq/discourse-legal-compliance)).

**Competitors (checked)**
- **Enterprise trust-and-safety** platforms are sales-led:
  - Tremau's Nima (Art. 16 forms, transparency reports) ([Tremau](https://tremau.com/resources/are-you-ready-for-your-first-dsa-transparency-report/));
  - Checkstep ([Checkstep](https://www.checkstep.com/dsa-tools-compliance/));
  - Cinder, Hive and ActiveFence [MEMORY].
- **Free pieces, which I integrate rather than rebuild:**
  - the StopNCII hash bank for partner platforms ([StopNCII](https://stopncii.org/how-it-works/));
  - Ofcom's free OSA risk-assessment toolkit ([Ofcom](https://www.ofcom.org.uk/online-safety/illegal-and-harmful-content/ofcom-launches-digital-safety-toolkit-for-online-services)). The founder doesn't build the risk assessment.
- **Store and repo searches:**
  - WordPress.org `site:` search: no TIDA or NCII plugin;
  - GitHub search "take it down" NCII: 0 repositories.

**Winning angle:** self-serve, installable in 15 minutes, priced for teams of 1-20, with four laws in one inbox.

**MVP (5-6 weeks)**
- The form and widget.
- An inbox with SLA timers and paging.
- PDQ hashing plus an upload-time match API.
- Statement-of-reasons templates.
- CSV and PDF exports.
- Discourse and WordPress plugins.

**Inbound GTM plan**
- Posts:
  1. "We checked 100 AI image apps and forums: most have no way to report an intimate deepfake. The law has required one since May." (public pages only)
  2. "TIDA in one picture: the 48-hour clock, what makes a valid notice, what to log."
  3. "DSA + TIDA + OSA + DMCA: one takedown inbox for a 3-person team." (demo GIF)
- SEO:
  - "Take It Down Act compliance small platform";
  - "TIDA takedown form template";
  - "DSA notice and action form";
  - "statement of reasons template".
- Marketplaces: Discourse plugins, WordPress.org, npm.
- Viral loop: "Report content, powered by TakedownDesk" on every form.

**Pricing.**
- Free: form and inbox, 10 notices a month.
- $29/month: paging, hashing, exports.
- $99/month: several sites, the API, and the DSA transparency report.

**Biggest risk.**
- Small forums have small budgets; the best buyers are AI image apps.
- Enterprise trust-and-safety vendors could launch a self-serve tier.
- Handling NCII reports is sensitive (store hashes only).
- If the FTC focuses only on large platforms, urgency drops.

**Chance 3 / Scale 4.** The UK OSA and DSA duties are permanent, which keeps demand going after the TIDA news cycle.

---

## 4. #41 **LabelCheck**: creator-side check of your own posts for ad and AI labels, per EU country (C3/S4)

**Pitch.** Connect your own Instagram, TikTok and YouTube accounts through the official APIs.

LabelCheck flags posts where you tagged a brand, used an affiliate link or discount code, or showed a gifted product, **without the correct label for your country**:
- "Werbung" or "Anzeige" (DE);
- "Publicité" or "Collaboration commerciale" (FR);
- "Pubblicità" (IT);
- "Publicidad" (ES);
- "#ad" (UK/US).

It also checks:
- **AI and retouching labels:** France's "Image retouchée" and "Image virtuelle", and EU AI Act Art. 50(4) deepfake disclosure;
- whether the label is **visible on the thumbnail** (a German enforcement focus);
- France's rule that deals **above €1,000 need a written contract.**

The output is a fix list. A **Canva app** stamps compliant labels onto designs.

**Audience.** EU creators with brand deals (DE, FR, IT, ES, NL first), talent managers and small influencer agencies. The English/FTC edition for the UK and US is the expansion path.

**EU-first is justified** because the existing tools are US/FTC-centric and brand-side, while the EU rules vary by country and language.

**Why now**
- **France:** decree 2025-1137 took effect on 1 Jan 2026 and requires written contracts above €1,000. The DGCCRF inspected 260+ influencers in 2024 and **40% had anomalies** ([So Bang](https://so-bang.fr/loi-influenceurs/), [Haas Avocats](https://www.haas-avocats.com/plateformes/ecommerce/influence-commerciale-comment-la-france-encadre-et-sanctionne/)). A ban on promoting ultra-fast fashion starts on 1 Jan 2027, with fines up to €100,000 ([Kohen Avocats](https://kohenavocats.com/influenceurs-mode-ultra-express-interdiction-janvier-2027-contrats-amende-dgccrf/)).
- **Germany:** the Wettbewerbszentrale acts against posts labelled "Anzeige" in the caption but not in the thumbnail, and creators report cease-and-desist letters (Abmahnungen) ([Wettbewerbszentrale](https://www.wettbewerbszentrale.de/wettbewerbszentrale-schreitet-ein-etliche-influencer-posts-in-social-media-nicht-als-werbung-erkennbar/), [skradde](https://www.skradde.com/post/abmahnung-der-wettbewerbszentrale-wegen-fehlender-werbekennzeichnung-auf-instagram---was-jetzt-zu-tun-ist)) [date of the action unverified].
- **EU AI Act Art. 50 deepfake labelling** has applied since 2 Aug 2026 ([Greenberg Traurig](https://www.gtlaw.com/en/insights/2026/6/deepfakes-chatbots-ai-generated-text-european-commission-details-transparency-obligations-under-the-ai-act)). Creators who post realistic AI images commercially now carry a second labelling duty.
- **The Digital Fairness Act** (proposal expected in Q4 2026) targets influencer marketing ([EP Legislative Train](https://www.europarl.europa.eu/legislative-train/theme-protecting-our-democracy-upholding-our-values/file-digital-fairness-act)). I treat it as a tailwind only, because the critic's REG-L16 rightly calls it too early to build on.

**Competitors (checked)**
- **CreatorScore** does brand-side vetting with FTC disclosure detection ([CreatorScore](https://creatorscore.io/ftc-compliance)).
- **AuditSocials** is FTC-centric ([AuditSocials](https://www.auditsocials.com/influencer-compliance)).
- **impact.com** has brand-side approval workflows.
- **German and French searches** found only law-firm and eRecht24 guides, and **no creator-side automatic checker** ([eRecht24](https://www.e-recht24.de/online-marketing/12272-influencer-werbung-kennzeichnung.html)).
- **The platforms' paid-partnership toggles** are "required but not sufficient" ([AuditSocials guide](https://www.auditsocials.com/blog/influencer-compliance-guide-ftc-disclosure-rules-platform-tools-2026)).

These are two small, US-focused, brand-side tools, which is allowed under the new calibration. This idea **revives** my round-3 drop "influencer disclosure monitoring".

**Winning angle:**
- sold to the creator, not the brand;
- EU country rule packs in local languages;
- AI and retouching labels;
- a free scan as the hook.

**MVP (5 weeks)**
- OAuth for Instagram, TikTok and YouTube.
- Caption analysis plus OCR of the thumbnail and first frame.
- An LLM classifier for commercial signals.
- Rule packs for DE, FR, IT, ES, NL, UK and US.
- The fix-list report.
- The Canva app. Canva allows external payment links ([Canva docs](https://www.canva.dev/docs/apps/accepting-payments/), [community tips](https://www.canva.dev/blog/developers/external-monetization-community-tips/)).

**Inbound GTM plan**
- Posts:
  1. "I scanned my last 200 posts: 14 would get me an Abmahnung. Here's the pattern." (creators film their own scan)
  2. "Werbung vs Anzeige vs Publicité vs #ad: the EU cheat sheet in one image."
  3. "France now requires 'Image virtuelle' on AI images. How 30 big French accounts handle it." (manual review of public posts, no scraping)
- SEO:
  - "Werbekennzeichnung Instagram richtig";
  - "mention collaboration commerciale obligatoire";
  - "AI Act Kennzeichnung KI-Bilder Influencer";
  - "Abmahnung Wettbewerbszentrale Influencer".
- Marketplace and viral loop: the Canva Apps Marketplace; a "Label-safe" badge for media kits; an agency white-label.

**Pricing.**
- A free scan of the last 50 posts.
- €9/month: continuous monitoring of one account.
- €49/month: agencies, 20 creators.

**Biggest risk.**
- **RDG boundary (legal-services law):** it must be a checker, not advice [MEMORY: BGH Smartlaw 2021 allows software document tools].
- API access: TikTok caption access through the Display API [MEMORY].
- False positives.
- Creators often only pay after their first Abmahnung.
- Brand-side vendors could add a creator self-check.

**Chance 3 / Scale 4.**

---

## 5. #42 **InboxShift**: newsletter click benchmark in the AI-inbox era (C3/S4)

**Pitch.** Connect Kit (through the **Kit App Store**) or Ghost. You see your **click** performance against anonymised peers in your niche and list size, before and after AI inbox summaries arrived. You get a share card ("Clicks −6% since Gemini summaries; my niche median −17%"), and a public weekly **Newsletter Click Index** is built from pooled, consented data.

**Audience.** Global: newsletter creators on Kit and Ghost (beehiiv later), newsletter agencies, and operators who sell sponsorships.

**Why now**
- **Apple Mail replaces preview text with AI summaries** (iOS 18.1+), and **Gmail entered its "Gemini era" in early 2026** ([Google](https://blog.google/products-and-platforms/products/gmail/gmail-is-entering-the-gemini-era/), [Stripo](https://stripo.email/blog/ai-summaries-in-email-clients-what-gmail-and-apple-mail-changes-mean-for-marketers/)).
- **Opens went up while clicks fell.** Omeda's Q2 2025 data on 2.03B emails shows the open rate rising from 43% to 45.6% while the unique click rate fell from 4.35% to 3.93% ([Lilach Bullock](https://www.lilachbullock.com/ai-email-summaries-open-rate-small-business/)) [secondary source]. Gmail may auto-open messages to summarise them, which makes open rates even less reliable ([Mailpro](https://www.mailpro.com/blog/ai-inbox-problem-email-marketing)).
- **The industry is moving to clicks as the KPI** ([INMA](https://www.inma.org/blogs/reader-revenue/post.cfm/will-newsletters-survive-the-ai-assault-on-e-mail)). Creators can't tell "is it me or everyone?"
- **Distribution exists.** The Kit App Store has an Analytics category ([Kit Help](https://help.kit.com/en/collections/11463387-kit-app-store)). Kit's v4 API exposes broadcast stats (recipients, opens, clicks, unsubscribes) through OAuth, which public apps must use ([dltHub on Kit API](https://dlthub.com/context/source/convertkit), [Kit v4](https://developers.kit.com/api-reference/upgrading-to-v4)).

**Competitors (checked)**
- **newsletterbenchmark.com** shows medians from public reports. You type in your numbers; there's **no connect and no pooled data** ([sources page](https://newsletterbenchmark.com/sources)).
- **beehiiv** publishes an annual report by industry ([beehiiv](https://www.beehiiv.com/blog/the-state-of-newsletters-2026)). Its dashboard compares each post with your last 10 posts ([beehiiv help](https://www.beehiiv.com/support/article/18794008882839)). Its feature page hints at comparisons with other publications [unverified], so beehiiv is deliberately left for later.
- **Mailchimp** shows industry averages [MEMORY], so it's skipped.
- **Litmus** offers *pre-send* previews of AI summaries, not benchmarks ([Litmus](https://www.litmus.com/blog/ai-generated-summaries)).
- **Kit App Store analytics apps:** Broadcast Boost (revenue) and Whatsdash (reporting). **No peer benchmark found.**

**Winning angle:** pooled first-party click data inside Kit's own store, plus the share card and index as content.

**MVP (4-5 weeks)**
- The Kit OAuth app and the Ghost Admin API.
- LLM niche classification.
- k-anonymous pools (at least 20 newsletters per pool).
- Dashboards, share cards and the weekly index page.

**Inbound GTM plan**
- Posts:
  1. "From 800 connected newsletters: clicks down 11% since Gemini summaries. Finance −3%, recipes −24%."
  2. "Your open rate is lying. Here's your click percentile." (share card)
  3. "5 newsletter formats that survived AI summaries (data)."
- SEO:
  - "good newsletter click rate [niche] 2026";
  - "Gmail AI summary impact on newsletters";
  - "Kit benchmark".
- Marketplace and viral loop: the Kit App Store, share cards, and "verified by InboxShift" on sponsor media kits.

**Pricing.**
- A free benchmark.
- $9/month: history, alerts, per-issue benchmark.
- $39/month: several newsletters or agencies, plus a verified sponsor report.

**Biggest risk.**
- **Cold start**, the same as #37: pools need hundreds of connected newsletters.
- Kit or beehiiv could ship native peer benchmarks.
- Small creators have low willingness to pay.
- Kit's app review.

**Chance 3 / Scale 4.**

---

## 6. #43 **ShelfShift**: "is it AI or is it me?" sales benchmark for nonfiction authors (C2/S4)

**Pitch.** Upload your KDP, Draft2Digital or IngramSpark royalty reports. KDP has no API, so upload is the first-party route. You get an anonymised benchmark by genre, subgenre (BISAC) and format (ebook, print, Kindle Unlimited pages, audio), with year-on-year trends, a **share card**, and a monthly public **Book Sales AI-Impact Index**.

**Audience.** Global: indie and traditionally published nonfiction authors, and small presses.

**Why now**
- **Tim Ferriss (12 Jun 2026):** his catalogue will sell about **80% fewer print copies in 2026 than in 2022**. The yearly declines were −5%, −13% and −46%, with 2026 running at −57%. The post went viral ([Tim Ferriss](https://tim.blog/2026/06/12/has-ai-already-killed-nonfiction/), [GIGAZINE](https://gigazine.net/gsc_news/en/20260617-ai-killed-self-help-nonfiction-book/), [Charlie Hoehn](https://www.charliehoehn.com/2026/08/18/has-ai-killed-the-how-to-book-the-future-of-p/)).
- **Publishers Weekly, as cited by Ferriss:** adult nonfiction −9% in Q1 2026 and self-help units −26.3% year on year [secondary source].
- Authors can't tell whether their own decline is category-wide or fixable.

**Competitors (checked)**
- **ScribeCount** tracks royalties across 40+ platforms. **No peer benchmark was found** ([ScribeCount](https://scribecount.com/explore-sales-dashboard)).
- **Book Report** is a KDP sales dashboard ([Book Report](https://www.getbookreport.com/)).
- **KDP research tools** (Publisher Rocket, KDSPY, BookBeam) *estimate other books' sales* from Best Sellers Rank rather than pooling first-party data [MEMORY].

**Winning angle:** pooled first-party data and a public index. I'd rather offer a ScribeCount import than compete with it.

**MVP (4 weeks)**
- Parsers for KDP, D2D and Ingram reports.
- LLM mapping to BISAC codes.
- k-anonymous pools.
- Dashboards, share cards and the index.

**Inbound GTM plan**
- Posts:
  1. "Ferriss lost 80%. Data from 1,200 authors: self-help −41%, cookbooks −18%, romance +6%."
  2. "Is AI killing your genre? Check in 60 seconds." (share card)
  3. The monthly index chart.
- SEO:
  - "is AI killing nonfiction";
  - "book sales down 2026 [genre]";
  - "KDP sales drop".
- Communities: r/selfpublish and author newsletters. Sponsors are author-service companies.

**Pricing.**
- A free benchmark.
- $7/month: history, subgenre view, alerts.
- $49 one-off category reports.
- Sponsorship.

**Biggest risk.**
- Cold start plus the friction of manual uploads.
- ScribeCount already holds the data and could add benchmarks.
- Low willingness to pay.

**Chance 2 / Scale 4 on its own.** **Recommended: merge it into #39 as the free viral hook** (one "AuthorRadar" brand). The combined product would be C3/S4.

---

## 7. How each of the coordinator's 8 directions came out

| # | Direction | Verdict | Evidence |
|---|---|---|---|
| 1 | n8n/Make/Zapier agency monitoring + client ROI report cards | **DROP**: 5+ tools, and the exact ROI feature already exists | See the table below |
| 2 | STR host compliance (EU STR Regulation, Barcelona, NYC LL18) | **DROP**: a dominant EU player, one-off registration, weak inbound fit | See the table below |
| 3 | Fake-review extension after Fakespot | **DROP**: 5+ near-identical tools | RateBud's alternatives list ([RateBud](https://www.ratebud.ai/blog/fakespot-shutting-down-best-alternatives-2026)); FakeFind, Amazon Fake Review Analyzer and Savinoo in the CWS ([FakeFind](https://chromewebstore.google.com/detail/fakefind-detect-fake-amaz/hfiafkfpmbibckgamoemdlnfafmbbjed)) |
| 4 | UGC compliance (TIDA, UK OSA) for small platforms | **PASS → #40**, with sibling **#38** | No self-serve tool; enterprise vendors only |
| 5 | Creator impersonation and AI knockoffs | **PASS for authors only (#39)**; the music and video versions failed | See the table below |
| 6 | More #2-style localisation of US tools | **No new pass.** #2 and #20 remain the localisation plays | See the table below |
| 7 | Vertical apps in new stores | **Mostly DROP.** Canva is used as a distribution add-on for #41 | See the table below |
| 8 | Connect-your-account benchmarks | **PASS → #42 (Kit/Ghost) and #43 (KDP upload)**; the other platforms failed | See the table below |

### Dropped candidates and the incumbents that kill them

| Candidate | Why it fails (criterion) |
|---|---|
| n8n agency monitoring and ROI cards | **5+ tools, and the feature exists.** Administrate already sells "Time Saved" client ROI reports plus per-client LLM costs, with a free 3-instance plan ([Administrate](https://administrate.dev/features/time-saved-tracking)). Others: AgentPing ([AgentPing](https://agentping.io/n8n-monitoring-for-agencies)), FlowMetr for n8n/Make/Zapier ([GitHub](https://github.com/FlowMetr/FlowMetr)), ageniusdesk-ce, n8n-library, and n8n's native Insights ([n8n docs](https://docs.n8n.io/insights/)). |
| STR host compliance, EU rules map | **A dominant player serves hosts:** Chekin covers EU guest registration, tourist tax and 35+ PMS integrations from €8/month ([Chekin](https://chekin.com/en/blog/regulation-eu-2024-1028/)). GuestAdmin automates submissions ([GuestAdmin](https://guestadmin.io/)). Minut and Rield give the rules content away free. **The platforms enforce registration numbers themselves**, and registration is a one-off task ([EC](https://single-market-economy.ec.europa.eu/news/new-rules-bring-increased-transparency-short-term-rentals-sector-2026-05-20_en)). |
| STR registration-number validation API for small platforms | The national registries expose verification APIs themselves ([Regulation text](https://eur-lex.europa.eu/eli/reg/2024/1028/oj/eng)). Buyers are a few hundred niche platforms, and it doesn't fit inbound marketing. |
| US STR permits (NYC LL18 and others) | RentPermit, STR Comply and Deckard, plus Granicus for cities ([RentPermit](https://www.rentpermit.com/), [Deckard](https://deckard.com/resources/2026-str-regulations)). |
| Musician impersonation | **The platform shipped it:** Spotify Artist Profile Protection, beta Mar 2026 ([Music Ally](https://musically.com/2026/03/24/spotify-cracks-down-on-fake-releases-with-artist-profile-protection-feature/)). |
| Video-creator likeness and deepfakes | **The platform shipped it:** YouTube opened likeness detection to **all creators aged 18+** on 17-19 May 2026 ([MediaPost](https://www.mediapost.com/publications/article/415170/youtube-rolls-out-likeness-detection-to-all-creato.html), [Tubefilter](https://www.tubefilter.com/2026/05/18/youtube-generative-ai-deepfake-likeness-detection-rollout/amp/)). Celebrities are served by Vermillio and Loti. |
| ChatGPT Apps SDK vertical app | For software subscriptions it's **an acquisition channel, not a revenue channel**. Partners reported little traffic, and directory search is still basic [summary] ([OpenAI monetization docs](https://developers.openai.com/apps-sdk/build/monetization), [Phiture](https://phiture.com/asostack/chat-gpt-app-directory/)). |
| Meta smart-glasses app | **No public publishing** was available as of Connect 2026 ([VR.org](https://vr.org/articles/meta-glasses-three-tiers-wearables-toolkit-publishing-connect-2026)). |
| M365 Copilot agent-store app | Monetisation works as a transactable SaaS offer ([Microsoft Learn](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/publish)), but an IT admin must enable it. That means enterprise sales, not inbound. |
| Claude connectors | No monetisation layer, and the critic rates MCP RED-AMBER (SAT map). |
| Canva app (standalone) | External payments are allowed and the marketplace is small, about 300 apps [summary, figure may date from 2024] ([Canva docs](https://www.canva.dev/docs/apps/accepting-payments/), [BusinessWire](https://www.businesswire.com/news/home/20240925330023/en)). No emerging problem justified a standalone app, so it's **used as distribution for #41**. |
| Patreon benchmark | CreatorDash and Creator Metrics already connect accounts ([CreatorDash](https://creator-dash.com/), [Creator Metrics](https://creatormetrics.io/)), and Graphtreon covers public data. The Apple-driven billing migration affects **only 4% of creators** ([TechCrunch](https://techcrunch.com/2026/01/28/apple-tells-patreon-to-move-creators-to-in-app-purchase-for-subscriptions-by-november/), [Patreon](https://www.patreon.com/posts/apple-has-its-on-148395613)). |
| Gumroad and Lemon Squeezy revenue boards | **TrustMRR verifies Gumroad** ([Marc Lou on X](https://x.com/marclou/status/1987867299018354713)) and Lemon Squeezy (founder rule: skip). |
| Etsy shop benchmark | 5+ analytics tools: eRank, EverBee, Alura, Marmalead [MEMORY]. |
| Instrumentl → German grant finder | FörderBase (3,100+ programmes, AI matching), Reflecta Fördermittelkompass, and the free official Förderdatenbank ([FörderBase](https://www.foerderbase.de/), [Reflecta](https://foerdermittelkompass.reflecta.org/?locale=en)). |
| Other US→DE localisations | Rentometer → a free official Mietspiegel; Ownwell → blocked by StBerG (tax-advice law); DoNotPay → blocked by RDG; Rocket Money → Finanzguru dominant (Finanzguru [MEMORY]). |
| EU withdrawal button (§356a BGB, since 19 Jun 2026) | **Deadline swarm:** Händlerbund's Shopify tool, vendidero's free WooCommerce plugin, and several more ([Händlerbund](https://ohn.haendlerbund.de/haendlerbund-news/widerrufsbutton-shopify-plugin), [CMS Admins](https://www.cms-admins.de/produkte/widerrufsbutton-woocommerce/)). |
| ChatGPT Ads benchmark or tool (self-serve since 5 May 2026; DACH since 24 Aug) | **5+ already:** Nakora, Lapis, TruCommerce and chatgptadlibrary publish benchmarks; Ryze, groas and Molin offer tools ([Nakora](https://nakora.ai/chatgpt-ads/conversion-rate-benchmarks), [chatgptadlibrary](https://www.chatgptadlibrary.com/tools/chatgpt-ads-benchmarks), [Molin](https://molin.ai/blog/best-ai-tools-chatgpt-ads-optimization)). |
| AI-app gross-margin dashboard | Margine, MarginDash, Paid.ai, and Stripe's token-markup billing ([Margine](https://margine.io/), [TechCrunch](https://techcrunch.com/2026/03/02/stripe-wants-to-turn-your-ai-costs-into-a-profit-center/)). |
| CIPA wiretap-risk scanner | PieEye, ConsentPixel, Secure Privacy, VaultJS and OneTrust ([PieEye](https://www.pii.ai/scan/fsca), [ConsentPixel](https://consentpixel.com/blogs/cipa-lawsuit-tracker/)). |
| LLM deprecation alerts | 6+ free trackers and Actions ([Quora tracker](https://github.com/quora/model-deprecation-tracker), [LLM Status](https://llmstatus.ai/)). |
| AI Act Art. 50(2) watermarking service | SSL.com has a free C2PA signing tier (May 2026), plus Adobe and others ([SSL.com](https://www.ssl.com/products/content-authenticity/content-credentials/c2pa/)). |
| EU Data Act access-by-design portal | Fiskil targets it ([Fiskil](https://www.fiskil.com/resources/eu-data-act-compliance-guide)); it also overlaps with #12's IoT buyers. |
| UK Renters' Rights Act landlord kit | TLA's checker, Lendlord, Goodlord and the NRLA ([TLA](https://landlordassociation.org.uk/rra-compliance-checker/), [Lendlord](https://theintermediary.co.uk/2026/04/lendlord-introduces-compliance-tool-to-support-renters-rights-act-requirements/)). |
| CA AB 723 altered listing-photo disclosure | Clearmarked, plus MLS rules ([Clearmarked](https://clearmarked.app/ab723-guide), [SDMLS](https://sdmls.com/ab-723-digitally-altered-images-sdmls-requirements/)). |
| Apple Accessibility Nutrition Labels | Still optional, with no deadline ([Access Armada](https://www.accessarmada.com/blog/time-to-prepare-for-apples-accessibility-nutrition-labels/)). |
| "Verified newsletter media kit" | Passionfroot and Paved [MEMORY], so it's folded into #42 as a feature. |

**Pattern confirmed (round-1 observation):** compliance built around a single public deadline gets swarmed within weeks. Examples: the withdrawal button, AB 723, the Renters' Rights Act, AI Act watermarking and ChatGPT Ads. The ideas that passed have one of two properties:
- **ongoing** enforcement through private suits or regulators after the deadline (#38, #40, #41);
- **ongoing** pain that no deadline resolves (#39, #42, #43).

---

## 8. Updated pipeline (all rounds)

| Tier | Ideas |
|---|---|
| Most likely survivors | #2 "Wen empfiehlt die KI?" (5/7) · #20 HireLaw Check (4/6) |
| Wounded but convertible | #7 LeanKeep (4/5) · #9 Nachfolge Weekly (4/4) · #12 PSTI + CRA Kit (3/6) · #29 Shopify Bot QA (3/6) · #30+#34 founder media (3/5) |
| New, not yet attacked (round 3) | #36 SafetyRadar (3/5) · #37 SearchShift (3/5) |
| **New, not yet attacked (round 4)** | **#38 CompanionSafe (3/5)** · **#39 KnockoffWatch (3/4)** · **#40 TakedownDesk (3/4)** · **#41 LabelCheck (3/4)** · **#42 InboxShift (3/4)** · **#43 ShelfShift (2/4; merge into #39)** |

**My ranking of the round-4 ideas by Chance, then Scale:**
1. #38 (3/5)
2. #39 + #43 merged as AuthorRadar (3/4)
3. #40 (3/4)
4. #41 (3/4)
5. #42 (3/4)

With the calibrated criterion 2, the projection rises from about 6-9 to **about 9-13 survivors**, if the critic accepts two or three of the round-4 ideas.
