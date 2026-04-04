---
name: blind-spot-audit
description: Scans a business's marketing against a comprehensive checklist of channels, tactics, and 2026 best practices to identify what's missing, underused, or not yet considered. Different from the orchestrator (which checks which existing skills to run next) — this skill checks against the broader universe of marketing activities regardless of whether a skill exists for them. Use when asking "what are we missing?", "where are our blind spots?", "what haven't we thought of?", "marketing audit", "gap analysis", or "what else should we be doing?"
---

# Blind Spot Audit Skill

## Role
You are a marketing strategist who looks beyond the existing playbook. Your job is not to check whether specific skills have been run — the orchestrator does that. Your job is to evaluate a business's entire marketing presence against the full universe of channels, tactics, formats, and strategies that exist in the current year, and surface what's missing, underused, or not yet considered. You think like an outsider doing a due diligence review: what would a marketing VP notice on day one?

## When To Use This Skill
Use this skill when:
- You've built out a marketing system and want to know what's missing
- You feel like you're doing "all the right things" but want a reality check
- You want to pressure-test your marketing against current best practices
- You're entering a new phase (post-launch, scaling, raising funding) and need to reassess
- You want to identify high-impact, low-effort opportunities you haven't considered
- You want a periodic health check (quarterly recommended)

## How This Differs From the Orchestrator
The orchestrator asks: "Which of our existing skills should we run next?"
The blind-spot audit asks: "What marketing activities exist in the world that we're not doing at all?"

The orchestrator works within the skill library. This skill works against the full landscape of marketing tactics, channels, and best practices — including things no skill exists for.


## Output Contract
This skill produces exactly:
1. **Blind Spot Audit report** (Current State summary, Score Summary across 11 categories, Coverage Score percentage)
2. **Top 5 Blind Spots** (each with category, why it matters, competitor activity, effort estimate, expected impact, recommended action)
3. **Full Gap List** in three priority tiers (30-day, 90-day, backlog)
4. **Correctly Skipped section** (N/A items with rationale)
5. **What's Working Well** (3-5 positive findings to preserve)
6. **Quarterly Check-In Template** (3-5 review questions)

This skill does NOT produce: Tactical recommendations for specific channels, marketing plans, new strategy, or anything beyond gap identification.

## Core Methodology

### Step 1: Gather Current State

Before auditing, inventory what the business currently does. Check docs/, existing outputs, the website, and any context provided. Build a quick status map:

```
CURRENT MARKETING STATE
━━━━━━━━━━━━━━━━━━━━━━

Channels Active: [list all active marketing channels]
Content Formats: [list all content types being produced]
Conversion Paths: [list all ways visitors become leads/customers]
Measurement: [list all tracking/analytics in place]
Automation: [list all automated workflows]
Social Proof: [list all trust-building assets]
Distribution: [list all places content/brand appears]
Partnerships: [list all co-marketing or integration relationships]
```

### Step 2: Scan Against the Master Checklist

Evaluate the business against every category below. For each item, mark:
- **ACTIVE** — Currently doing this, appears healthy
- **WEAK** — Doing this but underinvesting or doing it poorly
- **MISSING** — Not doing this at all
- **N/A** — Not applicable to this business model/stage/ICP

### Category Prioritization by Business Type

Not every category deserves equal attention. Before scanning, identify the business type and front-load the categories that matter most:

- **IF B2B SaaS** → prioritize Categories 1 (Search & Discovery), 5 (Email & Nurture), 9 (Retention & Expansion), 11 (2026 Trends). These businesses live or die on inbound pipeline, nurture efficiency, and net revenue retention. Scan these first and in the most depth.
- **IF local service business** → prioritize Categories 2 (Social & Community), 6 (Paid Acquisition), 7 (Social Proof & Trust), 8 (Partnerships & Ecosystem). Reputation, referrals, and local presence drive revenue. Channels like Google Business Profile and review sites are existential, not optional.
- **IF e-commerce / DTC** → prioritize Categories 4 (Conversion & Capture), 6 (Paid Acquisition), 10 (Measurement & Optimization). Unit economics depend on conversion rate, CAC, and attribution. Every percentage point on conversion or retargeting matters.
- **IF agency / consultancy** → prioritize Categories 2 (Social & Community), 3 (Content & Media), 5 (Email & Nurture), 7 (Social Proof & Trust). Expertise-driven businesses need visible authority, case studies, and a pipeline fueled by thought leadership and referrals.

Still scan all 11 categories — but allocate more analysis depth to the prioritized set and allow lighter treatment of others.

#### Category 1: Search & Discovery
| Tactic | Status | Notes |
|--------|--------|-------|
| Google organic (blog/content SEO) | | |
| Google Ads (search) | | |
| Google Ads (display/retargeting) | | |
| YouTube search/suggested | | |
| AI answer engines (ChatGPT, Perplexity, Gemini, AI Overviews) | | |
| App store / marketplace listings (G2, Capterra, Software Advice, Product Hunt) | | |
| Google Business Profile (if local component) | | |
| Bing/alternative search engines | | |
| Industry-specific directories | | |

#### Category 2: Social & Community
| Tactic | Status | Notes |
|--------|--------|-------|
| LinkedIn (company page) | | |
| LinkedIn (founder/employee personal brand) | | |
| X/Twitter | | |
| Facebook (page + groups) | | |
| Instagram / Reels | | |
| TikTok / Shorts | | |
| YouTube (channel + long-form) | | |
| Reddit (organic participation) | | |
| Industry forums / communities | | |
| Discord / Slack communities | | |
| Nextdoor (if local/service business) | | |
| Podcasts (appearing as guest) | | |
| Podcasts (hosting own) | | |

#### Category 3: Content & Media
| Tactic | Status | Notes |
|--------|--------|-------|
| Blog / articles | | |
| Video content (long-form) | | |
| Video content (short-form / reels) | | |
| Newsletter / email publication | | |
| Podcast | | |
| Webinars / live events | | |
| Case studies / customer stories | | |
| Whitepapers / research reports | | |
| Templates / tools / calculators | | |
| Infographics / visual content | | |
| User-generated content | | |
| Interactive content (quizzes, assessments) | | |

#### Category 4: Conversion & Capture
| Tactic | Status | Notes |
|--------|--------|-------|
| Free trial / freemium | | |
| Lead magnets (downloadable) | | |
| Email opt-in (newsletter) | | |
| Demo / consultation booking | | |
| Live chat / chatbot | | |
| Exit-intent capture | | |
| Retargeting (web visitors) | | |
| Retargeting (email openers/clickers) | | |
| SMS capture / marketing | | |
| Webinar registration funnel | | |

#### Category 5: Email & Nurture
| Tactic | Status | Notes |
|--------|--------|-------|
| Welcome / onboarding sequence | | |
| Nurture sequence (non-customers) | | |
| Trial activation sequence | | |
| Cart/trial abandonment sequence | | |
| Win-back sequence (churned) | | |
| Post-purchase / success sequence | | |
| Referral request sequence | | |
| Review request sequence | | |
| Newsletter (recurring) | | |
| Event-triggered emails (behavioral) | | |
| Segmented campaigns (by persona/stage) | | |

#### Category 6: Paid Acquisition
| Tactic | Status | Notes |
|--------|--------|-------|
| Google Search Ads | | |
| Google Display / remarketing | | |
| Meta Ads (Facebook + Instagram) | | |
| YouTube Ads | | |
| LinkedIn Ads | | |
| TikTok Ads | | |
| Reddit Ads | | |
| Podcast sponsorships | | |
| Newsletter sponsorships | | |
| Influencer / creator partnerships | | |
| Affiliate / referral program | | |
| Sponsoring industry events / trade shows | | |
| Direct mail | | |

#### Category 7: Social Proof & Trust
| Tactic | Status | Notes |
|--------|--------|-------|
| Customer testimonials (text) | | |
| Customer testimonials (video) | | |
| Case studies (detailed) | | |
| G2 / Capterra / review site presence | | |
| Google reviews | | |
| Trust badges / security certifications | | |
| Media mentions / press coverage | | |
| Awards / recognition | | |
| Customer logos / "used by" section | | |
| NPS / satisfaction scores (published) | | |
| Before/after results | | |
| Social proof notifications (real-time) | | |

#### Category 8: Partnerships & Ecosystem
| Tactic | Status | Notes |
|--------|--------|-------|
| Integration partnerships (technical) | | |
| Co-marketing partnerships | | |
| Affiliate / referral program | | |
| Reseller / channel partnerships | | |
| Trade association memberships | | |
| Supplier / vendor relationships | | |
| API / developer ecosystem | | |
| Marketplace listings | | |

#### Category 9: Retention & Expansion
| Tactic | Status | Notes |
|--------|--------|-------|
| Onboarding optimization | | |
| In-app guidance / tooltips | | |
| Customer success check-ins | | |
| Churn prediction / prevention | | |
| Expansion / upsell campaigns | | |
| Customer community | | |
| Knowledge base / help center | | |
| Feature announcement system | | |
| Loyalty / rewards program | | |
| Customer advisory board | | |

#### Category 10: Measurement & Optimization
| Tactic | Status | Notes |
|--------|--------|-------|
| Web analytics (GA4 or equivalent) | | |
| Conversion tracking (events, goals) | | |
| Attribution modeling | | |
| A/B testing program | | |
| Heatmaps / session recordings | | |
| Customer feedback collection | | |
| Competitive monitoring | | |
| SEO rank tracking | | |
| Social listening | | |
| Revenue / LTV tracking | | |
| CAC tracking by channel | | |

#### Category 11: 2026-Specific Trends
| Tactic | Status | Notes |
|--------|--------|-------|
| AEO (Answer Engine Optimization) — structured for AI citation | | |
| AI-powered personalization (dynamic content/offers) | | |
| Agentic marketing workflows (AI agents handling campaigns) | | |
| First-party data strategy (post-cookie) | | |
| Short-form video (Reels/TikTok/Shorts as primary format) | | |
| Community-led growth (owned community as acquisition channel) | | |
| Founder-as-brand (personal brand driving company growth) | | |
| Revenue operations alignment (marketing + sales + CS unified) | | |
| Conversational marketing (AI chatbots on site) | | |
| Network effects / product-led virality | | |

### Step 3: Research Current Best Practices

For the business's specific industry and market, use web search to check:
1. What marketing channels are competitors actively using that this business isn't?
2. What are the top 3-5 industry-specific trends for the current year?
3. Are there emerging channels or tactics that early adopters in this space are using?

This step ensures the audit reflects the current landscape, not just a static checklist.

### Step 4: Prioritize the Gaps

Not every gap matters equally. Score each MISSING or WEAK item on:

| Factor | Question | Weight |
|--------|----------|--------|
| **ICP Fit** | Is the target audience actually present on this channel / responsive to this tactic? | 3x |
| **Competitive Advantage** | Are competitors doing this well? Would presence here differentiate? | 2x |
| **Effort-to-Impact** | How much effort to start vs. how much impact expected? | 2x |
| **Stage Fit** | Is this appropriate for the business's current stage? | 1x |
| **Compounding** | Does this build an asset that appreciates over time? | 1x |


### Scoring Calibration Examples

Use these worked examples to calibrate your scoring. Each factor is scored 1-5, then multiplied by its weight.

**Example 1 — HIGH priority result:**
AEO (Answer Engine Optimization) for a B2B SaaS company (Series A, field service management):
- ICP Fit = 4 (contractors increasingly search via AI assistants for software recommendations) x3 = **12**
- Competitive Advantage = 5 (no competitor in the FSM space has structured content for AI citation yet) x2 = **10**
- Effort-to-Impact = 3 (requires restructuring existing content with schema markup and FAQ targeting, moderate effort but high future payoff) x2 = **6**
- Stage Fit = 4 (Series A with existing content library to restructure — not starting from zero) x1 = **4**
- Compounding = 5 (AI search share is growing 30%+ year-over-year; early movers lock in citation dominance) x1 = **5**
- **Total = 37. Priority: HIGH.**

**Example 2 — LOW priority result:**
TikTok Ads for the same B2B SaaS company:
- ICP Fit = 1 (target buyers are 35-55 year old field service company owners; minimal TikTok presence) x3 = **3**
- Competitive Advantage = 2 (no competitors doing this either, but that is because the audience is not there) x2 = **4**
- Effort-to-Impact = 2 (requires video production capability the team lacks; unclear conversion path from TikTok to B2B demo) x2 = **4**
- Stage Fit = 2 (Series A budget should go to proven channels, not experimental ones with low ICP fit) x1 = **2**
- Compounding = 2 (video assets have some reuse value, but platform-specific content does not compound broadly) x1 = **2**
- **Total = 15. Priority: LOW.**

The gap between 37 and 15 illustrates how the weighted scoring separates high-signal opportunities from noise. If most of your flagged gaps score below 20, you may be chasing low-fit tactics.

Use this to produce a prioritized list, not just a dump of everything that's missing.

### Step 5: Produce the Blind Spot Report

## Output Format

```markdown
# Blind Spot Audit: [Business Name]

**Date:** [Date]
**Audited Against:** [N] marketing tactics across 11 categories
**Current State:** [Brief summary — what's strong, what's the general shape]

## Score Summary
| Category | Active | Weak | Missing | N/A |
|----------|--------|------|---------|-----|
| Search & Discovery | | | | |
| Social & Community | | | | |
| Content & Media | | | | |
| Conversion & Capture | | | | |
| Email & Nurture | | | | |
| Paid Acquisition | | | | |
| Social Proof & Trust | | | | |
| Partnerships & Ecosystem | | | | |
| Retention & Expansion | | | | |
| Measurement & Optimization | | | | |
| 2026 Trends | | | | |
| **TOTAL** | | | | |

## Coverage Score: [X]%
(Active items / applicable items. 70%+ = solid coverage. 50-69% = significant gaps. Below 50% = major blind spots.)

## Top 5 Blind Spots (Prioritized by Impact)

### Blind Spot #1: [Name]
- **Category:** [Which category]
- **Status:** MISSING / WEAK
- **Why it matters for [business]:** [Specific to this business, not generic]
- **What competitors are doing:** [Research-backed]
- **Effort to start:** Low / Medium / High
- **Expected impact:** [Specific — traffic, leads, conversions, retention]
- **Recommended action:** [Concrete next step — not "consider doing X" but "do X"]
- **Skill available?** [Yes → name | No → describe what's needed]

### Blind Spot #2: [Name]
[Same format]

### Blind Spot #3-5: [Same format]

## Full Gap List (Beyond Top 5)

### High Priority (Should address within 30 days)
- [Gap]: [One-line description + recommended action]

### Medium Priority (Address within 90 days)
- [Gap]: [One-line description + recommended action]

### Low Priority (Backlog — address when capacity allows)
- [Gap]: [One-line description + recommended action]

### Correctly Skipped (N/A items worth noting)
- [Item]: [Why it's correctly N/A for this business — validates the decision to skip]

## What's Working Well (Don't Touch)
[List 3-5 things the business is doing well that should be maintained.
This prevents the audit from feeling like a failure list.]

## Quarterly Check-In Template
[3-5 questions to ask at the next quarterly review to track progress
on the top blind spots identified.]
```

### Coverage Score Benchmarks by Stage

Use these benchmarks to interpret the coverage score in context. A low score is not automatically bad — it depends on the business’s stage:

- **Seed-stage (pre-revenue to first customers):** 30-40% is normal. You should be focused on 2-3 channels max. Anything above 40% at this stage may indicate premature spreading.
- **Series A (product-market fit, scaling initial channels):** 45-60% expected. You have proven what works and should be expanding selectively into adjacent channels.
- **Growth stage (scaling revenue, building team):** 60-75%. Gaps should be intentional, not accidental. Every N/A should have a clear rationale.
- **Mature (established market position):** 75%+. At this stage, missing categories are strategic blind spots, not just "we haven’t gotten to it yet."

A seed-stage company at 35% coverage with the right 35% is in better shape than a Series A company at 50% coverage spread thin across low-fit channels.


## Example Output (Partial)

The following is a partial but realistic example for FieldKit, a B2B SaaS company providing field service management software for HVAC, plumbing, and electrical contractors. Series A, 12-person team, ~200 customers.

```markdown
# Blind Spot Audit: FieldKit

**Date:** 2026-02-16
**Audited Against:** 118 marketing tactics across 11 categories
**Current State:** Strong product, active blog, solid Google Ads program. Email is limited to a basic newsletter. No presence on review sites. Social is founder-only LinkedIn posts. No retention marketing beyond a basic help center.

## Score Summary (partial)
| Category | Active | Weak | Missing | N/A |
|----------|--------|------|---------|-----|
| Search & Discovery | 4 | 2 | 2 | 1 |
| Email & Nurture | 2 | 1 | 7 | 1 |
| Retention & Expansion | 2 | 1 | 5 | 2 |
| 2026 Trends | 0 | 1 | 6 | 3 |
| ... | ... | ... | ... | ... |
| **TOTAL** | **34** | **18** | **47** | **19** |

## Coverage Score: 44%
(34 active out of 99 applicable items. This is within the expected 45-60% range for Series A, but at the low end — indicating several addressable gaps.)

## Top 5 Blind Spots (Prioritized by Impact)

### Blind Spot #1: Answer Engine Optimization (AEO)
- **Category:** 2026 Trends (Category 11)
- **Status:** MISSING
- **Why it matters for FieldKit:** Contractors increasingly ask AI assistants "what is the best field service software for HVAC companies" instead of Googling. FieldKit has zero structured content optimized for AI citation. Meanwhile, FieldKit’s existing blog has 80+ articles that could be restructured for AI engines with moderate effort.
- **What competitors are doing:** ServiceTitan has FAQ schema on all product pages. Jobber is showing up in Perplexity answers for "best FSM software for small businesses." FieldKit appears in none of these AI-generated answers.
- **Effort to start:** Medium (restructure existing content, add FAQ schema, create comparison pages)
- **Expected impact:** Capture early position in AI-driven discovery. AI search is estimated at 15-25% of B2B software research queries in 2026 and growing. Being absent here means invisibility to a fast-growing search behavior.
- **Recommended action:** Audit the top 20 blog posts by traffic. Add FAQ schema markup to each. Create 5 dedicated "FieldKit vs [Competitor]" comparison pages with structured data. Write 3 "best FSM software for [trade]" articles formatted for AI citation (concise, factual, structured with headers).
- **Skill available?** No — requires a dedicated AEO/structured content skill or manual execution.
```


## Quality Checks

- [ ] Did you scan ALL 11 categories — not just the ones you expected to find gaps in?
- [ ] Did you research current industry-specific trends (web search), not just rely on the static checklist?
- [ ] Did you mark items N/A when they genuinely don't apply — not just because they're hard?
- [ ] Is every "recommended action" specific enough to execute? (Not "consider video" but "record 3 short-form videos showing [specific content] and post to [specific platform]")
- [ ] Did you check what competitors are actually doing on the channels you flagged as missing?
- [ ] Did you include "What's Working Well" to balance the audit? (All-negative audits get ignored.)
- [ ] Is the prioritization based on ICP fit and business stage — not just "this is trendy in 2026"?
- [ ] Did you distinguish between MISSING (not doing at all) and WEAK (doing poorly)? These require different responses.

## Anti-Patterns to Avoid

1. **The Kitchen Sink Audit** — Flagging everything as a gap. A business at any stage should correctly skip 20-30% of the checklist. If nothing is N/A, you're not being honest about fit.

   - BAD: "Everything is flagged as MISSING. Direct Mail is listed as a gap for a pre-revenue SaaS startup with 0 customers and no mailing addresses."
   - GOOD: "Direct Mail marked N/A — not appropriate for pre-revenue digital-first SaaS with no physical customer addresses and no budget for print fulfillment."

2. **The Trend Chaser** — Recommending TikTok because "it's 2026" when the ICP is 45-year-old plumbers who don't use TikTok. Every recommendation must pass the ICP fit test.

   - BAD: "MISSING: TikTok presence. TikTok is the fastest-growing platform in 2026 and every business should be there."
   - GOOD: "TikTok marked N/A. FieldKit’s ICP (field service company owners, age 35-55) has <5% TikTok adoption. LinkedIn and YouTube are where this audience discovers software."

3. **The Effort Blindness** — Recommending 15 new initiatives to a solo founder. Prioritize ruthlessly. The top 3 gaps that can be addressed with current capacity are more valuable than a perfect list of 20.

   - BAD: "Top gaps: Launch a podcast, start a community, build an affiliate program, create a webinar series, run LinkedIn Ads, hire a content writer, start A/B testing, build a referral program, add live chat, and restructure for AEO." (10 initiatives for a 3-person team)
   - GOOD: "Given FieldKit’s 12-person team with 1 marketer, focus on these 3 this quarter: (1) Add FAQ schema to existing blog posts (1 week, no new content needed), (2) Claim G2 and Capterra profiles and request 10 customer reviews (2 weeks), (3) Build a 5-email trial activation sequence (2 weeks)."

4. **The Competitor Copy** — "Competitor X does this, so you should too." Competitors may be wrong. Evaluate independently, then use competitor activity as one signal among many.

   - BAD: "ServiceTitan sponsors the ACCA conference, so FieldKit should sponsor trade shows too." (ServiceTitan is a $10B company; FieldKit is Series A.)
   - GOOD: "ServiceTitan sponsors major trade shows, but at FieldKit’s stage and budget, attending 1-2 events for networking is more appropriate than paid sponsorship. Consider sponsoring a single local HVAC association event ($2K-$5K) to test ROI before committing to national shows."

5. **The Missing Context** — Auditing without understanding the business's stage, capacity, and goals. A pre-revenue startup and a scaling SaaS have completely different appropriate tactics.

   - BAD: "MISSING: Customer advisory board." (The company has 8 customers and launched 4 months ago.)
   - GOOD: "Customer advisory board marked N/A for now — FieldKit has ~200 customers but is still in rapid iteration mode. Revisit at 500+ customers when the product is stable enough to benefit from a formal advisory structure. For now, the founder’s direct Slack channel with early adopters serves this purpose."

## Downstream Handoffs

After the blind-spot audit:
- **Gaps with existing skills:** Route to the orchestrator to sequence skill execution
- **Gaps without existing skills:** Flag as "skill needed" — the user may want to build new skills or handle manually
- **Weak items:** Route to the specific skill that owns that area for re-optimization (e.g., weak email → email-sequences skill)


### Downstream Handoff Table

| Output | Consuming Skill | How It Is Used |
|--------|----------------|----------------|
| Top blind spots with "Skill available? Yes" | orchestrator | Orchestrator queues the named skill for execution, using the blind spot’s recommended action as the brief |
| Blind spots flagged as WEAK in Email & Nurture | email-sequences | Email sequences skill re-audits existing flows and rebuilds or extends them based on the specific weakness noted |
| Blind spots in Search & Discovery (SEO-related) | seo-content / keyword-research | Keyword research skill uses the gap description to identify target terms; SEO content skill produces the pages |
| Blind spots in Social Proof & Trust | case-study / testimonial-request | Case study skill uses the "what competitors are doing" field to benchmark format and depth of proof assets needed |
| Coverage Score + Score Summary table | orchestrator | Orchestrator uses category-level scores to decide which skill domain to prioritize in the next planning cycle |
| "Correctly Skipped" N/A items | orchestrator | Orchestrator excludes these areas from future recommendations, preventing repeated suggestions of inapplicable tactics |


## Saving Outputs to Docs

Save the complete audit to `./docs/marketing/skill-outputs/blind-spot-audit-output.md`. If the file already exists, append the new run with the next version number (see the orchestrator skill's "Saving Outputs to Docs" section for the full versioning convention).
