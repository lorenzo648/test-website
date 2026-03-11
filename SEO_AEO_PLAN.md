# SEO & AEO Optimization Plan for Akdo Website

## Context

Akdo's local website (`drafts/website-final/`) has strong design and compelling narrative copy, but zero SEO/AEO infrastructure. No meta descriptions, no structured data, no semantic heading strategy, no keyword targeting. The site is invisible to search engines and AI answer engines. This plan adds SEO/AEO without changing the visual design or creative voice.

**ICP:** Head of Safety / Regional HSE Director at Fortune Global 2000 companies
**Key differentiators:** AI-generated training from client data, 200+ languages, days not months, site-specific content
**Target market:** Global (use both HSE and EHS terminology)
**No VR/immersive keywords** — Akdo has zero VR features
**Target industries:** All high-risk (manufacturing, oil & gas, construction, mining, chemical, logistics)
**Final deployment:** Framer (not static HTML)

---

## Framer vs. Draft — What Goes Where

### Change in the HTML draft (copy/content → copy-paste into Framer)
- H1 and H2 heading text
- Body copy adjustments (keyword integration)
- FAQ sections (questions + answers)
- "Answer-first" paragraphs for AEO
- Alt text for images
- New content blocks ("Who needs this training?", educational paragraphs)

### Configure in Framer directly (not in draft)
- Title tags → Framer SEO settings per page
- Meta descriptions → Framer SEO settings per page
- Open Graph / social sharing tags → Framer OG settings
- Canonical URLs → Framer auto-handles
- Sitemap.xml → Framer auto-generates
- robots.txt → Framer auto-handles
- Schema / JSON-LD → Framer custom code injection
- Favicon, lang attribute → Framer site settings

**Each page section below now tags items as [DRAFT] or [FRAMER].**

---

## Keyword Strategy

### Tier 1: Primary keywords (titles + H1s)

| Page | Primary Keyword | Why |
|------|----------------|-----|
| Homepage | `AI safety training platform` | Category-defining |
| HSE Training | `HSE training software` + `EHS training software` | Global #1 term |
| Sustainability | `ESG training software` + `sustainability compliance training` | Growing, low competition |
| Training Library | `safety training courses` + `HSE training library` | Course catalog searches |
| Course Detail | `[topic] training` (e.g., `confined space entry training`) | High-intent per-topic |
| Security | `GDPR compliant training platform` + `ISO 27001` | Procurement searches |
| Book Demo | `safety training demo` | Bottom of funnel |

### Tier 2: Differentiator keywords (H2s + body copy) — YOUR BLUE OCEAN

- `AI-generated safety training`
- `safety training from incident reports`
- `convert SOPs to training`
- `multilingual safety training software`
- `site-specific safety training`
- `automated safety training content`
- `safety training in 200 languages`

### Tier 3: Industry keywords (body copy + future pages)

- `safety training for manufacturing`
- `HSE training for oil and gas`
- `construction safety training`
- `safety training for chemical industry`
- `safety training for mining`

### Tier 4: Problem/intent keywords (FAQ + AEO)

- `how to improve safety training completion rates`
- `how to scale safety training globally`
- `how to make safety training engaging`
- `safety training ROI`
- `how to automate safety training`

---

## Competitor Benchmark: Pixaera

Pixaera (VR safety training, $5.7M raised, BP/Shell clients) has:
- ~60-80 indexed pages vs. Akdo's 9
- Schema markup on every page (Organization, FAQ, BreadcrumbList)
- Dedicated landing page per training topic with FAQ sections
- Industry-specific pages (construction, manufacturing, energy)
- Weak content production (~2 real SEO blog posts total)
- No G2/Capterra presence
- Blog on subdomain (SEO disadvantage)
- Templated/duplicated content across pages

**Akdo's advantages:** AI-generated (not VR), from client data, 200+ languages, content engine opportunity. Pixaera doesn't target AI keywords at all.

---

## SEO Crash Course (for Lorenzo)

**SEO** = making Google show your site when people search relevant terms. Three layers:
1. **Technical** — can Google find and read your pages? (meta tags, headings, structured data)
2. **On-page** — does your copy contain the words people actually search for? (keywords in titles, headings, body)
3. **AEO** — can AI tools (ChatGPT, Perplexity, Google AI Overviews) extract and cite your content? (structured answers, FAQ schemas)

**Why it matters now:** 89% of B2B buyers use AI for research. If Akdo isn't structured for extraction, buyers won't find you during their AI-assisted vendor evaluation.

---

## Page-by-Page Recommendations

### 1. Homepage (`index.html`)

**Current title:** `Akdo — Safety Training Built From Your Workplace`
**Current H1:** `The AI safety training platform.`
**Meta description:** None

#### Layer 1: URGENT (technical foundations)

- [FRAMER] **Add meta description:** `"Akdo is the AI-powered HSE training platform that turns your SOPs, incident reports, and risk assessments into interactive, multilingual safety training — deployed in days, not months."`
- [DRAFT] **Fix H1 for keyword targeting:** Current H1 "The AI safety training platform" is decent but misses key search terms. Change to: `"AI-Powered HSE Training Platform"` — captures both "AI" and "HSE training platform" which are high-intent keywords
- [FRAMER] **Update title tag:** `"Akdo — AI-Powered HSE & Safety Training Platform"` (under 60 chars, primary keywords front-loaded)
- [FRAMER] **Add Organization schema** (JSON-LD in `<head>`): company name, logo, URL, description
- [FRAMER] **Add lang and canonical tags**

#### Layer 2: HANGING FRUIT (copy adjustments for keyword density)

- **H2 headings need keywords.** Current H2s are creative/emotional ("Three things no other training platform does") — good for conversion but invisible to search. Add a keyword-rich subheading or adjust:
  - Section 3 H2: Add subtitle beneath creative heading: `"AI-generated safety training from your own data — SOPs, incident reports, and risk assessments"`
  - Section "How It Works": `"From SOP Upload to Global Safety Training Deployment in 12 Weeks"` (captures "safety training deployment" and process keywords)
- **Stats bar section** — the numbers (450+ courses, 99.6% completion, 200+ languages, 150+ HSE topics) are currently in the code but need visible text labels that search engines value. Ensure each stat has a clear text label not just styled numbers
- **Add "EHS" alongside "HSE"** — in body copy, use both terms at least once: "HSE (also known as EHS) training" to capture North American search traffic
- **Internal links** — add descriptive anchor text links from homepage to solution pages. Current links just say "HSE Training" in nav. Add contextual in-body links

#### Layer 3: WOULD MAKE THIS PERFECT

- **Add FAQ section** at bottom of homepage with FAQPage schema markup. Questions:
  - "What is AI-powered safety training?"
  - "How long does it take to deploy Akdo?"
  - "What languages does Akdo support?"
  - "How does Akdo create training from incident reports?"
- **Add a paragraph of "answer-first" copy** near the top that AI engines can extract: a 40-60 word definition of what Akdo is and does, structured as a clear declarative statement
- **Structured data:** Add `SoftwareApplication` or `Service` schema for the platform
- **Add breadcrumb schema** sitewide
- **Content block for topical authority:** A short "What is HSE training software?" educational paragraph that positions Akdo as an authority on the topic (not just a vendor)

---

### 2. HSE Training Page (`hse-training.html`)

**Current title:** `HSE Training — Akdo`
**Current H1:** `Your incidents become your best training.`
**Meta description:** None

#### Layer 1: URGENT

- **Add meta description:** `"Turn incident reports, near-misses, and SOPs into interactive, site-specific HSE training. AI-generated safety videos, simulations, and microlearning in 200+ languages. Deployed in days."`
- **Update title tag:** `"HSE Training Software — AI-Powered Safety Training | Akdo"` (targets "HSE training software" — the #1 keyword)
- **Fix H1:** The current creative H1 misses searchable terms entirely. Options:
  - Keep the creative line as a tagline/subtitle and add a keyword H1 above it: `"HSE Training Software That Learns From Your Incidents"`
  - Or keep current H1 and add a visible subtitle: `"AI-powered HSE training software that turns your incident data into interactive, site-specific safety training"`
- **H2 keywords:** Current H2s are emotional ("More training feeds the cycle") — add keyword context:
  - "AI Incident Videos" section: H2 could be `"AI-Generated Safety Training Videos From Your Incident Reports"`
  - "Site-Specific Training": `"Site-Specific Safety Training Built From Your SOPs"`
  - "Interactive Simulations": `"Interactive HSE Training Simulations"`
  - "Global Deployment": `"Global Safety Training Deployment in 200+ Languages"`

#### Layer 2: HANGING FRUIT

- **Include "EHS" keyword** — add "EHS/HSE" or "EHS training software" at least once in body copy
- **Add alt text to all SVG/visual placeholders** — currently no alt attributes on visual elements
- **Comparison table** (vs. DIY/Agency/Akdo) — excellent for SEO. Add a heading above it: `"HSE Training Software Comparison: Akdo vs. Agencies vs. DIY AI Tools"` — this captures comparison keywords
- **Stats section** — wrap numbers in semantic HTML and add labels: "70-80% faster training creation", "99.6% training completion rate", "83% safety violation reduction" — these are extractable facts for AEO
- **Cross-link** to Training Library and Security pages within body copy using descriptive anchors

#### Layer 3: WOULD MAKE THIS PERFECT

- **FAQ section with schema:** "How does AI create safety training?", "How long does HSE training deployment take?", "What training formats does Akdo offer?", "Is AI-generated safety training accurate?"
- **Add industry-specific keyword mentions** in the topics cloud or body: "HSE training for manufacturing", "safety training for oil and gas", "construction safety training"
- **Testimonial/quote schema** for the customer proof section
- **Add "Last updated" timestamp** — AEO signal showing content freshness

---

### 3. Sustainability Page (`sustainability.html`)

**Current title:** `Sustainability & Compliance Training — Akdo`
**Current H1:** `Your ESG policies sit in a folder. Your people sit through a deck.`
**Meta description:** None

#### Layer 1: URGENT

- **Add meta description:** `"AI-powered ESG and sustainability training that turns your compliance policies into engaging, multilingual training. CSRD, ISO 14001, GRI-aligned content deployed globally in days."`
- **Update title tag:** `"ESG & Sustainability Training Software — Compliance Training | Akdo"` (captures "sustainability training software" and "compliance training")
- **Keyword adjustment to H1:** Add subtitle: `"AI-Powered ESG & Sustainability Compliance Training Platform"`
- **Fix H2s for keywords:** "What you're up against" → add keyword subtitle. "What changes with Akdo" → `"How AI Transforms Sustainability & Compliance Training"`

#### Layer 2: HANGING FRUIT

- **Target "ESG training" and "CSRD training"** — these are growing search terms. Mention CSRD, EU Taxonomy, ISO 14001, GRI explicitly in body copy (some already present)
- **Regulatory keyword mentions** — add "corporate sustainability reporting directive training", "sustainability compliance training"
- **Cross-link** to HSE Training page ("Also see our HSE training solution for health & safety compliance")
- **Add stats/proof points** — if available, sustainability-specific completion rates or deployment metrics

#### Layer 3: WOULD MAKE THIS PERFECT

- **FAQ section with schema:** "What is ESG training?", "How to comply with CSRD training requirements?", "What sustainability standards does Akdo cover?"
- **Educational content block** defining sustainability training for the ICP — positions Akdo as thought leader and improves AEO citation potential
- **Regulatory compliance table** — shows which frameworks are covered (CSRD, EU Taxonomy, ISO 14001, GRI, TCFD). Tables are AEO gold

---

### 4. Training Library (`training-library.html`)

**Current title:** `Training Library — Akdo`
**Current H1:** `150+ pre-built training topics.`
**Meta description:** None

#### Layer 1: URGENT

- **Add meta description:** `"Browse Akdo's library of 150+ pre-built HSE and sustainability training modules. AI-customizable courses covering confined space, LOTO, HAZMAT, working at heights, and more."`
- **Update title:** `"HSE Training Library — 150+ Safety & Compliance Courses | Akdo"`
- **H1 keyword optimization:** `"HSE & Safety Training Course Library — 150+ Pre-Built Topics"`
- **Each course card should be a proper link** with descriptive anchor text (they currently link to the course detail page, which is good)

#### Layer 2: HANGING FRUIT

- **Individual course names ARE keywords** — "Confined Space Entry", "Lockout/Tagout (LOTO)", "Working at Heights" — these are what safety managers search. Make sure each course card has its name in an H3 or strong tag that search engines can index
- **Add text content below the grid** describing the library's scope — currently the page is mostly UI with minimal text. Add a 200-word paragraph explaining what the library covers and how customization works
- **Category pages** — each filter category (HSE, Sustainability, Leadership) should ideally have its own URL (e.g., `training-library.html?cat=hse`) — for now, adding category-specific text blocks would help

#### Layer 3: WOULD MAKE THIS PERFECT

- **Each course detail page = SEO landing page** — the `training-library-course.html` template is a major SEO opportunity. Each individual course page can rank for specific safety training keywords (e.g., "confined space entry training", "LOTO training online", "chemical handling training"). Scale this across all 150+ topics
- **Add FAQ schema** on course detail pages: "What does confined space entry training cover?", "Who needs confined space training?"
- **Add Course schema markup** (structured data for educational courses)

---

### 5. Course Detail Template (`training-library-course.html`)

**Current title:** `Confined Space Entry — Training Library — Akdo`
**Current H1:** `Confined Space Entry`
**Meta description:** None

#### Layer 1: URGENT

- **Add meta description:** `"Confined space entry training covering hazard identification, atmospheric testing, permit-to-work procedures, and emergency rescue protocols. Available as microlearning, AI video, or simulation in 200+ languages."`
- **Update title:** `"Confined Space Entry Training — HSE Course | Akdo"` (targets "confined space entry training")
- **Breadcrumbs are good** — add BreadcrumbList schema markup

#### Layer 2: HANGING FRUIT

- **Body copy is already keyword-rich** — the learning objectives and module coverage list naturally contain the right terms. Ensure H2s reflect this: current "What this module covers" is fine but "Learning objectives" could be `"Confined Space Entry Training Learning Objectives"`
- **"Available formats" section** — mention "online confined space training" and "interactive safety training" somewhere in text
- **Add a "Who needs this training?" section** — captures intent queries like "who needs confined space entry training" and adds AEO-extractable content

#### Layer 3: WOULD MAKE THIS PERFECT

- **Course schema (JSON-LD)** with provider, topic, delivery method, language availability
- **FAQ section:** "Is confined space training required?", "How often should confined space training be completed?", "What are the 3 types of confined spaces?"
- **Regulatory requirements paragraph** — "OSHA 29 CFR 1910.146 requires..." — this is what safety managers search before buying training. Adds massive authority

---

### 6. Security Page (`security.html`)

**Current title:** `Security — Akdo`
**Current H1:** `Your safety data deserves safety.`
**Meta description:** None

#### Layer 1: URGENT

- **Add meta description:** `"Akdo's security practices: ISO 27001 certified, SOC 2 Type II audited, GDPR compliant. Your safety data is encrypted, isolated, and never used for model training."`
- **Update title:** `"Security & Compliance — ISO 27001, SOC 2, GDPR | Akdo"`
- **H1 keyword consideration:** The creative H1 is fine for the page tone, but add a visible subtitle: `"ISO 27001 Certified · SOC 2 Type II · GDPR Compliant"`

#### Layer 2: HANGING FRUIT

- **Keywords in H3 blocks** — current H3s ("No hallucinated procedures", "Your data, your IP") are good but could include searchable terms like "AI safety training data security", "GDPR compliant training platform"
- **Expand certification descriptions** — each certification card (ISO 27001, GDPR, SOC 2) has minimal text. Add 2-3 sentences explaining what each means for the customer (this is what procurement teams search for)
- **Add data residency info** — "Data hosted in EU (Germany)" — critical for European enterprise buyers and captures "EU data residency" queries

#### Layer 3: WOULD MAKE THIS PERFECT

- **FAQ section with schema:** "Is Akdo ISO 27001 certified?", "Does Akdo use my data for AI training?", "Is Akdo GDPR compliant?", "Where is my data stored?"
- **Trust Center landing page content** — currently links to external trust center. Consider embedding key info directly
- **Add security whitepaper download** — captures leads while providing enterprise procurement teams what they need

---

### 7. Book a Demo (`book-demo.html`)

**Current title:** `Book a Demo — Akdo`
**Current H1:** `See Akdo in action.`
**Meta description:** None

#### Layer 1: URGENT

- **Add meta description:** `"Book a 30-minute personalized demo of Akdo's AI-powered HSE training platform. See how your SOPs and incident reports become interactive training — live on the call."`
- **Update title:** `"Book a Demo — AI Safety Training Platform | Akdo"`
- **Keep H1 as is** — demo pages should be conversion-focused, not keyword-stuffed

#### Layer 2: HANGING FRUIT

- **"What you'll see" section** — rephrase items to include keywords naturally: "How Akdo's AI creates safety training from your SOPs and incident reports" instead of just "How Akdo creates training from your SOPs and incident reports"
- **Add social proof** — the trusted-by logos are good. Add "Used by HSE teams at Fortune Global 2000 companies" as a visible text line
- **Time commitment clarity:** "30-minute personalized demo" is good — make it more visible (currently in subtitle, could also be in form header)

#### Layer 3: WOULD MAKE THIS PERFECT

- **FAQ under the form:** "How long is the demo?", "Is the demo customized to my industry?", "What do I need to prepare?"
- **HowTo schema** — structured data for the demo booking process
- **Conversion-specific copy:** Add urgency/value: "Most enterprise teams go live in 12 weeks" below the form

---

### 8. Contact (`contact.html`)

**Current title:** `Contact — Akdo`
**Current H1:** `Get in touch.`
**Meta description:** None

#### Layer 1: URGENT

- **Add meta description:** `"Contact Akdo — the AI-powered HSE training platform. Reach out for demos, partnerships, procurement, or general inquiries. Based in Munich, Germany."`
- **Update title:** `"Contact Akdo — HSE Training Platform | Munich, Germany"`
- **Add LocalBusiness schema** with address, email, region

#### Layer 2: HANGING FRUIT

- **Add company info visible on page** — current address is minimal ("Munich, Germany"). Full address helps local SEO and enterprise credibility
- **Response time commitment** is good ("1 business day") — keep it

#### Layer 3: WOULD MAKE THIS PERFECT

- **ContactPage schema** markup
- **Map embed** for Munich office (visual trust signal + local SEO)
- **Separate contact paths** — dedicated security@ email for procurement/security teams

---

### 9. Careers (`careers.html`)

**Current title:** `Careers — Akdo`
**Current H1:** `Make workplaces safer with AI.`
**Meta description:** None

#### Layer 1: URGENT

- **Add meta description:** `"Join Akdo — a Munich-based startup using AI to transform enterprise safety training. Open roles in engineering, AI/ML, and enterprise sales."`
- **Update title:** `"Careers at Akdo — AI Safety Training Startup | Munich"`

#### Layer 2: HANGING FRUIT

- **Job posting schema** (JSON-LD) for each open position — makes jobs appear in Google Jobs search
- **Add job description content** — current listings are just titles. Expanding with 2-3 bullet points per role helps SEO and AEO
- **Company culture keywords** — "AI startup Munich", "safety tech careers"

#### Layer 3: WOULD MAKE THIS PERFECT

- **JobPosting schema** with full structured data for each role
- **Team size and funding mentions** if public — "7-person team", "backed by [investors]" adds credibility signals
- **Glassdoor/LinkedIn links** — E-E-A-T signal

---

## Sitewide Technical SEO (Apply to ALL pages)

### Layer 1: URGENT
1. **Add `<meta name="description">` to every page** (listed above per page)
2. **Add `<link rel="canonical">` to every page** pointing to self
3. **Create `robots.txt`** in site root (allow all, point to sitemap)
4. **Create `sitemap.xml`** listing all 9 pages with lastmod dates
5. **Fix image alt text** — logo alt is just "Akdo" everywhere (fine), but SVG icons and visual placeholders have no alt text
6. **Add viewport and charset** (already present, good)

### Layer 2: HANGING FRUIT
7. **Add JSON-LD Organization schema** to every page (or at minimum homepage)
8. **Consistent internal linking** — every page should link to at least 2-3 other pages with descriptive anchor text (not just nav links)
9. **Heading hierarchy audit** — ensure every page has exactly one H1, and H2s follow logically. No H1 → H3 jumps
10. **Use both "HSE" and "EHS" across the site** — at least once per solution page mention "EHS" to capture US traffic
11. **Add "last updated" dates** to solution pages (AEO signal)

### Layer 3: WOULD MAKE THIS PERFECT
12. **FAQPage schema** on 4+ pages (homepage, HSE, sustainability, security)
13. **BreadcrumbList schema** on all inner pages
14. **SoftwareApplication or Service schema** on homepage
15. **Minify CSS/JS** — currently inline, minor improvement for page speed
16. **Add Open Graph and Twitter Card meta tags** for social sharing
17. **WebP images** when real product images replace placeholders

---

## Priority Keyword Map (page → primary target keywords)

| Page | Primary Keywords | Secondary Keywords |
|------|-----------------|-------------------|
| Homepage | AI safety training platform, HSE training software | AI-powered safety training, EHS training platform |
| HSE Training | HSE training software, AI HSE training | safety training from incident reports, site-specific safety training |
| Sustainability | ESG training software, sustainability compliance training | CSRD training, corporate sustainability training |
| Training Library | HSE training courses, safety training library | online safety training, EHS training courses |
| Course Detail | [topic] training (e.g., "confined space entry training") | [topic] course online, [topic] training requirements |
| Security | safety training data security, GDPR compliant training | ISO 27001 training platform, SOC 2 certified |
| Book Demo | HSE training demo, safety training demo | book demo safety platform |
| Contact | contact Akdo, HSE training Munich | safety training company Germany |
| Careers | AI safety startup careers | Munich AI jobs, safety tech |

---

## Files to Modify

All files in `drafts/website-final/`:
- `index.html` — meta tags, title, H1/H2 adjustments, FAQ section, schema
- `hse-training.html` — meta tags, title, H1 subtitle, H2 keywords, FAQ section, schema
- `sustainability.html` — meta tags, title, H1 subtitle, H2 keywords, FAQ section, schema
- `training-library.html` — meta tags, title, H1, added text content, schema
- `training-library-course.html` — meta tags, title, FAQ section, course schema
- `security.html` — meta tags, title, subtitle, expanded cert descriptions, FAQ section
- `book-demo.html` — meta tags, title, copy tweaks
- `contact.html` — meta tags, title, LocalBusiness schema
- `careers.html` — meta tags, title, JobPosting schema

New files to create:
- `drafts/website-final/robots.txt`
- `drafts/website-final/sitemap.xml`

---

## Verification

After implementation:
1. Open each page in browser, verify all copy reads naturally and design is unchanged
2. View page source to confirm meta tags, schemas, and canonical tags are present
3. Validate structured data using Google's Rich Results Test (paste page source)
4. Check heading hierarchy (one H1, logical H2/H3 nesting)
5. Search for "site:akdo.ai" on Google after deployment to track indexing (future)
6. Test AI extraction by pasting page text into ChatGPT and asking "What is Akdo?" — answers should match your key messages

---

## Approach

We go through this together, page by page. For each page, I'll show you the exact copy changes before writing anything. You approve, we implement. No surprises.

**Order:** Start with Layer 1 (URGENT) across all pages first — this is the biggest bang for effort. Then Layer 2. Then Layer 3 if you want to go further.
