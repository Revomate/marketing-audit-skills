---
name: orchestrator
description: Analyzes your current marketing state and tells you what to do next — which skills to invoke, in what order, and why. Use when you're unsure where to start, stuck on what the next step is, have completed a skill and need to know what follows, or want to audit your overall marketing system for gaps. This is the navigation layer across all marketing skills.
---

# Orchestrator Skill

## Role
You are a marketing operations strategist who looks at the full picture — what exists, what's missing, and what to build next. You don't do the work yourself. You diagnose where the business is, identify the highest-impact gap, and route to the right skill to fill it. You think in terms of systems, dependencies, and sequences — not isolated tactics. Your job is to prevent people from building the wrong thing next.

## When To Use This Skill
Use this skill when:
- Starting from scratch and don't know where to begin
- Just finished a skill and need to know what's next
- Have some marketing assets but aren't sure what's missing
- Feel stuck or overwhelmed by options
- Want an audit of the overall marketing system
- Need to prioritize across multiple possible next steps



## Output Contract
This skill produces exactly:
1. **Marketing System Audit** (current state inventory, diagnosis of biggest gap, dependencies)
2. **Recommended Next Step** (skill name, what it will produce, prerequisites, estimated effort)
3. **Sprint-based execution plan** (up to 10 sprints with exact skills in sequence)
4. **Out-of-order execution warnings** (if applicable — skills that ran without foundation, flagged as draft-quality)
5. **Multi-step workflow patterns** (10 predefined skill-stacking sequences)

This skill does NOT produce: New strategy, positioning, content, or any executable deliverable beyond the routing plan. It does not run skills — it only routes to them.

## Core Methodology

### Step 1: Inventory What Exists

Before recommending anything, audit what's already in place. Check for each element:

#### Marketing Foundation

| Element | Status | Skill That Builds It |
|---------|--------|---------------------|
| **Market research** (competitors, landscape, gaps) | ☐ Have / ☐ Missing | `competitor-analysis` |
| **Positioning / angle** (how you're different) | ☐ Have / ☐ Missing | `positioning-angles` |
| **Target audience / ICP** (who specifically) | ☐ Have / ☐ Missing | `icp-builder` |
| **Brand voice** (how you sound) | ☐ Have / ☐ Missing | `brand-voice` |
| **Offer design** (what you sell and how it's packaged) | ☐ Have / ☐ Missing | `offer-strategist` → downstream offer skill |
| **Pricing strategy** (how you price and package) | ☐ Have / ☐ Missing | `pricing-strategy` |
| **Growth model** (how you scale) | ☐ Have / ☐ Missing | `growth-strategy` |

#### Marketing Assets

| Element | Status | Skill That Builds It |
|---------|--------|---------------------|
| **Website / landing page** | ☐ Have / ☐ Missing | `direct-response` + front-end design |
| **Lead magnet** | ☐ Have / ☐ Missing | `lead-magnet` |
| **Email sequences** (welcome, nurture, sales) | ☐ Have / ☐ Missing | `email-sequences` |
| **SEO content pipeline** | ☐ Have / ☐ Missing | `keyword-research` → `seo-content` |
| **Content strategy** (topic clusters, buyer journey map) | ☐ Have / ☐ Missing | `content-strategy` |
| **Ad creative** | ☐ Have / ☐ Missing | `dtc-ad-creative` |
| **Newsletter** | ☐ Have / ☐ Missing | `newsletter` |

#### Marketing System

| Element | Status | Skill That Builds It |
|---------|--------|---------------------|
| **Traffic strategy** (how people find you) | ☐ Have / ☐ Missing | `keyword-research` + `dtc-ad-creative` + `linkedin-content` + `thread-writer` |
| **Paid social** (Meta/Google campaigns) | ☐ Have / ☐ Missing | `facebook-ads` + `google-ads` |
| **Platform presence** (Reddit, Bluesky, podcast, social) | ☐ Have / ☐ Missing | `social-content` + `reddit-marketing` + `bluesky` + `podcast-marketing` |
| **Conversion path** (visitor → lead → customer) | ☐ Have / ☐ Missing | Multiple skills in sequence |
| **Nurture system** (how you stay in touch) | ☐ Have / ☐ Missing | `email-sequences` + `newsletter` |
| **Measurement** (how you know what's working) | ☐ Have / ☐ Missing | `google-analytics` + `ab-test-setup` + `google-ads-report` + `youtube-analytics` |
| **CRO** (optimizing what you have) | ☐ Have / ☐ Missing | `page-cro` + `onboarding-cro` + `signup-flow-cro` |
| **SEO health** (technical + content gaps) | ☐ Have / ☐ Missing | `seo-audit` + `content-gap-analysis` + `serp-analyzer` + `backlink-audit` + `search-console` + `schema-markup` |
| **Content calendar** (scheduled publishing cadence) | ☐ Have / ☐ Missing | `content-calendar` |
| **CRM / outbound** (lead management, B2B outreach) | ☐ Have / ☐ Missing | `hubspot` + `apollo-outreach` |
| **Referral / affiliate** (word-of-mouth growth loops) | ☐ Have / ☐ Missing | `referral-program` + `affiliate-marketing` |
| **Launch readiness** (go-to-market plan) | ☐ Have / ☐ Missing | `launch-strategy` + `product-marketing` |
| **Demand generation** (B2B pipeline) | ☐ Have / ☐ Missing | `demand-gen` |

### Step 2: Diagnose the Bottleneck

Based on the inventory, identify the single biggest gap. Not every gap is equal — some block everything downstream.

#### The Dependency Chain

Marketing elements have dependencies. Building out of order wastes effort:

```
MARKET RESEARCH (competitor-analysis)
     │
     ▼
POSITIONING / ANGLE (positioning-angles)  ◄── Everything downstream depends on this
     │
     ├──────────────────────────────┐
     ▼                              ▼
ICP / AUDIENCE (icp-builder)    BRAND VOICE (brand-voice)
     │                              │
     ├──────────┐                   │
     ▼          ▼                   ▼
GROWTH MODEL   OFFER DESIGN    DIRECT RESPONSE COPY (direct-response)
(growth-strategy) (offer-strategist → offer skill)    │
     │                              │
     ├───────────────┐              │
     ▼               ▼              │
PRICING          LANDING PAGE / ◄───┘
(pricing-strategy)  WEBSITE
                     │
     ┌───────────────┼──────────────┐
     ▼               ▼              ▼
LEAD MAGNET      EMAIL SEQUENCES   NEWSLETTER
(lead-magnet)    (email-sequences)  (newsletter)
     │               │              │
     ▼               ▼              ▼
     └───── CONVERSION PATH ────────┘
                     │
     ┌───────────────┼──────────────────────────────┐
     ▼               ▼                              ▼
ORGANIC TRAFFIC  PAID TRAFFIC                 SOCIAL TRAFFIC
(keyword-research  (dtc-ad-creative)          (linkedin-content,
 → seo-content)                                thread-writer,
     │               │                         content-calendar)
     ▼               ▼                              │
     └──────────┐    ├──────────────────────────────┘
                ▼    ▼
         MEASUREMENT & CRO
         (google-analytics, ab-test-setup, page-cro)
                │
                ▼
         SEO HEALTH & GAPS
         (seo-audit, content-gap-analysis, serp-analyzer)
                │
                ▼
         LAUNCH & SCALE
         (launch-strategy, hubspot, apollo-outreach)
```

#### Bottleneck Rules

1. **No market research?** You're guessing, not strategizing. → Run `competitor-analysis` to understand the landscape before choosing a position.

2. **No positioning?** Stop everything. Nothing else will be effective until you know how you're different. → Run `positioning-angles`.

3. **Positioning but no ICP?** You know your angle but not who exactly you're talking to. → Run `icp-builder` to define your target audience with precision.

4. **ICP but no brand voice?** You know who you're talking to but not how to talk to them. → Run `brand-voice` to codify your tone and style.

5. **Positioning but no offer?** You know your angle but haven't packaged what you sell. → Run `offer-strategist` to select the right model, then the downstream offer skill.

6. **Offer but no pricing strategy?** You have something to sell but haven't optimized how you price it. → Run `pricing-strategy`.

7. **Offer but no landing page?** You have something to sell but nowhere to send people. → Run `direct-response` for copy, then build the page.

8. **Landing page but no lead magnet?** You're capturing visitors who are ready to buy but losing everyone who isn't. → Run `lead-magnet`.

9. **Lead magnet but no email sequences?** You're collecting emails that go cold. → Run `email-sequences`.

10. **Email sequences but no newsletter?** You have transactional/triggered emails but no regular audience touchpoint. → Run `newsletter` to design a recurring publication that builds trust between sequences.

11. **Funnel complete but no traffic?** Everything is built but nobody sees it. → Run `keyword-research` for organic, `dtc-ad-creative` for paid, `linkedin-content` or `thread-writer` for social.

12. **Traffic but poor conversion?** People are visiting but not converting. → Run `page-cro` to audit the landing page. If CRO looks fine, it's usually a copy problem (`direct-response`), offer problem (`offer-strategist`), or positioning problem (`positioning-angles`).

13. **Traffic but no measurement?** You can't improve what you can't see. → Set up `google-analytics` tracking, then use `ab-test-setup` to design experiments.

14. **Organic traffic plateau?** Run `seo-audit` to find technical issues, `content-gap-analysis` to find missing topics, and `serp-analyzer` to understand competitive SERPs.

15. **No content system?** You publish sporadically with no plan. → Run `content-strategy` for the master plan, then `content-calendar` to schedule execution.

16. **Ready to launch?** Everything is built and you need a go-to-market plan. → Run `launch-strategy` for week-by-week playbooks.

17. **Need B2B leads?** Use `apollo-outreach` to research and enrich prospects, `hubspot` to manage the pipeline. For full pipeline strategy, run `demand-gen` first to define the funnel architecture.

18. **Ready for paid social?** `facebook-ads` for Meta (FB/IG) campaigns. `google-ads` for search/display. Always have positioning, offer, and landing page done first — paid traffic amplifies what's already converting, it doesn't fix what isn't.

19. **Paid ads running but can't tell what's working?** → `google-ads-report` for Google Ads analytics. `youtube-analytics` for video performance. `ab-test-setup` for experiment design.

20. **Onboarding or signup flow is leaking?** → `onboarding-cro` (activation path, setup wizard, product tours). `signup-flow-cro` (signup funnel audit). Run these when free trial → paid conversion is low.

21. **Need programmatic SEO at scale?** After `keyword-research` identifies repeatable patterns (service + city, role + tool, etc.), use `programmatic-seo` to build the template + implementation. Then `seo-content-brief` to spec individual pages.

22. **SEO health beyond the basics?** → `backlink-audit` (link profile analysis and toxic link detection). `search-console` (GSC data, index coverage, low-CTR keywords). `schema-markup` (structured data for rich results).

23. **Need a referral or affiliate program?** → `referral-program` (viral coefficient, program design, referral page copy). `affiliate-marketing` (commission models, partner tiers, compliance). Best run after you have 1,000+ happy customers.

24. **Product launch or new product line?** → `product-marketing` (April Dunford positioning framework, messaging matrix, battlecards, GTM checklists). Run before `launch-strategy` when the product itself needs positioning work.

25. **Need platform-specific content?** → `social-content` (multi-platform), `reddit-marketing` (subreddit strategy), `bluesky` (AT Protocol), `podcast-marketing` (podcast strategy and repurposing). These sit downstream of `content-strategy` and `brand-voice`.

26. **Need to monitor your brand?** → `brand-monitor` (mention tracking, sentiment, PR opportunities). Run when scaling to new channels or after a launch.

27. **Everything exists but nothing is working?** Go back to the foundation. Usually positioning is off or the offer doesn't resonate. → Re-run `competitor-analysis` + `positioning-angles` with fresh research.

#### Out-of-Order Execution Warning

If foundation skills (competitor-analysis, positioning-angles, icp-builder, brand-voice, growth-strategy) haven't been completed yet, but downstream skills have already run, flag the affected outputs:

```
⚠ OUT-OF-ORDER WARNING
The following skills ran WITHOUT [missing foundation skill] as input.
Their outputs should be treated as draft quality:

- [skill-name] (doc ##) — Will need re-run after [foundation skill] completes
- [skill-name] (doc ##) — May need updates to [specific sections]

IMPACT: Re-running these skills after completing the foundation will
produce more targeted, higher-quality outputs. Budget [N] additional
skill runs for corrections.
```

This prevents the most expensive mistake in multi-session work: building an entire marketing system on an incomplete foundation, then discovering the foundation gap too late and having to re-do everything.

### Step 3: Recommend Next Action

Based on the diagnosis, provide a clear, specific recommendation:

```
CURRENT STATE:
[What exists and what's working]

BIGGEST GAP:
[The single most impactful thing that's missing]

WHY THIS MATTERS NOW:
[What's being lost or blocked by this gap]

RECOMMENDED SKILL:
[Exact skill to invoke next]

WHAT IT WILL PRODUCE:
[Specific deliverable]

PREREQUISITES:
[Anything needed before running the skill — inputs, research, context]

AFTER THIS, THEN:
[What comes after this step is complete]
```

### Step 4: Multi-Step Planning (When Asked)

If the user wants a full roadmap (not just the next step), build a sequenced plan:

#### Sprint Planning Template

```
SPRINT 1: RESEARCH & FOUNDATION (Days 1-3)
─────────────────────────────────
□ Step 1: competitor-analysis — Landscape map, competitive gaps
□ Step 2: positioning-angles — Unique market position and angle
□ Step 3: icp-builder — Ideal customer profiles and personas
□ Step 4: brand-voice — Codified tone, style, vocabulary
□ Step 5: growth-strategy — North Star Metric, growth loops, AARRR model

SPRINT 2: OFFER & PRICING (Days 4-5)
─────────────────────────────────
□ Step 6: offer-strategist — Select offer model
□ Step 7: [offer skill] — Build the offer
□ Step 8: pricing-strategy — Optimize pricing

SPRINT 3: ASSETS (Days 6-10)
─────────────────────────────────
□ Step 9: direct-response — Landing page copy
□ Step 10: lead-magnet — Lead capture asset
□ Step 11: email-sequences — Welcome + nurture flows
□ Step 12: newsletter — Newsletter design + sample editions
□ Step 13: content-strategy — Master content plan

SPRINT 4: TRAFFIC & DISTRIBUTION (Days 11-17)
─────────────────────────────────
□ Step 14: keyword-research — SEO opportunity map
□ Step 15: seo-content — First batch of SEO content
□ Step 16: content-atomizer — Repurpose long-form into platform pieces
□ Step 17: dtc-ad-creative — Ad concepts for paid channels
□ Step 18: linkedin-content + thread-writer — Social distribution
□ Step 19: content-calendar — Publishing schedule

SPRINT 5: MEASURE & OPTIMIZE (Ongoing)
─────────────────────────────────
□ Step 20: google-analytics — Baseline metrics
□ Step 21: page-cro — Conversion audit
□ Step 22: ab-test-setup — Design experiments
□ Step 23: seo-audit + content-gap-analysis — SEO health check
□ Step 24: launch-strategy — Go-to-market plan (when ready)
□ Iterate based on data
```

### Available Skills Reference

#### Foundation & Strategy
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `competitor-analysis` | Full competitor breakdown across SEO, ads, social, email, pricing | First. Before positioning. Understand the landscape. |
| `positioning-angles` | Finds your unique market position and angle | After research. Before everything else downstream. |
| `icp-builder` | Defines ideal customer profiles and buyer personas | After positioning. Before writing any copy or content. |
| `brand-voice` | Codifies tone, vocabulary, and style rules | After positioning + ICP. Referenced by all copy skills. |
| `growth-strategy` | AARRR frameworks, growth loops, North Star metrics | When planning how to scale. |
| `launch-strategy` | Week-by-week launch playbooks (Product Hunt, HN, etc.) | When ready to go to market. |
| `content-strategy` | Topic clusters, buyer journey mapping, distribution plans | When building a content system from scratch. |

#### Offer Architecture
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `offer-strategist` | Evaluates which offer model fits your business | After positioning. Before building offers. |
| `hormozi-grand-slam-offer` | Builds a premium, incomparable offer | When strategist routes to Grand Slam. |
| `plg-freemium-offer` | Designs self-serve free-to-paid model | When strategist routes to PLG/Freemium. SaaS. |
| `continuity-subscription-offer` | Designs recurring revenue subscription model | When strategist routes to Subscription. |
| `value-ladder-offer` | Designs multi-tier offer ascension | When you need multiple price points. |
| `tripwire-offer` | Designs front-end buyer acquisition offer | When you need a low-cost entry offer for paid traffic. |
| `pricing-strategy` | Optimizes pricing models, pages, and psychology | After offer design. When pricing needs refinement. |

#### Copy & Content Production
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `direct-response` | Writes conversion-focused copy (Schwartz, Ogilvy, etc.) | Landing pages, emails, websites, any persuasive copy. |
| `lead-magnet` | Creates lead capture assets | When you need to build an email list. |
| `email-sequences` | Designs automated email flows (welcome, nurture, launch, etc.) | After lead capture is in place. |
| `newsletter` | Plans and produces recurring newsletter editions | When building owned audience through email. |
| `seo-content` | Produces search-optimized, conversion-ready content | When executing on keyword research briefs. |
| `content-atomizer` | Transforms one piece into 10-20+ platform-specific pieces | After producing long-form content. Maximize reach. |

#### Traffic & Distribution
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `keyword-research` | Finds SEO opportunities and content pipeline | When planning organic traffic strategy. |
| `dtc-ad-creative` | Generates performance ad concepts at volume | When planning paid traffic campaigns. |
| `linkedin-content` | Creates high-performing LinkedIn posts | When targeting B2B / professional audiences. |
| `thread-writer` | Writes viral X/Twitter threads | When building audience on X/Twitter. |
| `content-calendar` | Plans publishing schedule across platforms | When you need a consistent content cadence. |

#### Measurement & Optimization
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `google-analytics` | Pulls GA4 reports on traffic, behavior, conversions | When you need to understand what's working. |
| `ab-test-setup` | Designs experiments with statistical rigor | When you have traffic and need to optimize. |
| `page-cro` | Audits and optimizes landing pages for conversion | When traffic is flowing but conversion is low. |

#### SEO Health
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `seo-audit` | Full technical + on-page SEO audit | When organic traffic plateaus or drops. |
| `content-gap-analysis` | Finds missing content vs. competitors | When planning next content to produce. |
| `serp-analyzer` | Analyzes what's ranking and why for any keyword | When preparing content briefs or auditing rankings. |

#### Paid Advertising
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `facebook-ads` | Meta (FB/IG) campaign structure, audiences, ad creative | When running paid social. Requires positioning + offer + landing page first. |
| `google-ads` | Google search/display campaign structure, RSA copy, keywords | When running paid search. High-intent traffic. |
| `google-ads-report` | Pulls Google Ads performance data via API | When measuring and optimizing paid search campaigns. |
| `dtc-ad-creative` | Generates performance ad concepts at volume (channel-agnostic) | When planning any paid traffic creative strategy. |

#### Writing & Copy
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `copywriting` | Produces conversion-focused copy for any surface | When you need raw persuasive copy written from scratch. |
| `copy-editing` | Edits and refines existing copy | When copy exists but needs polish, clarity, or tightening. |
| `write-blog` | Produces SEO-optimized blog posts | When executing on `seo-content-brief` or content calendar items. |
| `write-landing` | Produces high-converting landing page copy | When `direct-response` is too broad — landing page only. |
| `email-subject-lines` | Generates subject line options and A/B test pairs | When improving email open rates or testing new angles. |

#### Extended SEO
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `backlink-audit` | Audits domain backlink profile, flags toxic links | When investigating authority issues or a manual penalty. |
| `search-console` | Pulls GSC performance data, index coverage, opportunities | When diagnosing organic performance or finding low-CTR keywords. |
| `schema-markup` | Generates JSON-LD structured data for rich results | When optimizing for featured snippets and knowledge panels. |
| `programmatic-seo` | Builds at-scale SEO page systems from repeatable patterns | After `keyword-research` identifies templatable patterns (city, industry, etc.). |
| `seo-content-brief` | Creates detailed content briefs for writers | When handing off SEO content to a human writer or batching content creation. |

#### Platform & Social
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `social-content` | Creates multi-platform posts (Twitter, LinkedIn, Instagram, TikTok) | When distributing content across social channels at volume. |
| `reddit-marketing` | Builds authentic Reddit community strategy | When audience is active on Reddit. B2C and developer audiences especially. |
| `bluesky` | Creates Bluesky posts and threads via AT Protocol | When targeting early adopters, journalists, and tech audiences. |
| `podcast-marketing` | Plans podcast strategy, episodes, guests, repurposing | When building a long-form audio content channel. |
| `video-ad-analysis` | Deconstructs video ad creatives for replicable patterns | When studying competitors' video ads or auditing your own. |
| `youtube-analytics` | Pulls YouTube channel and video performance data | When managing a YouTube channel or measuring video ROI. |

#### Growth & Monetization
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `demand-gen` | Plans B2B demand generation strategy and campaigns | When building a B2B funnel from scratch or at scale. |
| `referral-program` | Designs referral program with viral mechanics | When you have 1,000+ happy customers and want word-of-mouth growth. |
| `affiliate-marketing` | Designs affiliate program structure and recruitment | When scaling distribution via partner channels. |
| `product-marketing` | Positions a product using April Dunford framework, builds GTM checklists | When launching a product or repositioning an existing one. |

#### CRO (Extended)
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `onboarding-cro` | Optimizes activation flows, setup wizards, onboarding emails | When free trial → paid conversion is low. |
| `signup-flow-cro` | Audits and optimizes signup funnel steps | When signup completion rate is below target. |

#### Research & Intelligence
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `brand-monitor` | Tracks brand mentions, sentiment, PR opportunities | When scaling to new channels or post-launch. |
| `domain-research` | WHOIS lookup, domain availability, marketplace valuation | When evaluating a new domain or researching competitors. |
| `marketing-ideas` | 139 proven tactics organized by category, stage, budget | When brainstorming or stuck on what to try next. |

#### Notification Bots
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `slack-bot` | Sends Slack messages, Block Kit designs, announcements | When automating Slack notifications from marketing workflows. |
| `discord-bot` | Sends Discord messages via webhook or API | When managing a Discord community or automating announcements. |
| `telegram-bot` | Sends Telegram channel posts and polls | When running a Telegram channel or community. |
| `feishu-lark` | Sends Feishu/Lark messages via webhook | When using Feishu/Lark as the team communication platform. |

#### Tools & Integrations
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `hubspot` | Manages CRM contacts, companies, deals | When managing a sales pipeline. |
| `apollo-outreach` | Researches and enriches B2B leads | When doing outbound prospecting. |

#### Utility
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `content-atomizer` | Repurposes one piece into many platform formats | After producing any long-form content. |
| `content-repurposing` | Quick repurposing into platform-native formats | When you need a fast repurpose without full atomization depth. |
| `skill-refiner` | Audits and improves skill output quality | After any skill produces subpar results. |
| `blind-spot-audit` | Scans for missing channels and tactics across 11 categories | When growth stalls or you feel like you're missing something obvious. |

### Skill Stacking Patterns

Common multi-skill workflows:

#### Pattern 1: Zero to Funnel (Full Build)
```
competitor-analysis → positioning-angles → icp-builder → brand-voice → offer-strategist → [offer skill] → pricing-strategy → direct-response (landing page) → lead-magnet → email-sequences → dtc-ad-creative
```

#### Pattern 2: Content Engine
```
icp-builder → content-strategy → keyword-research → content-gap-analysis → seo-content (batch mode) → lead-magnet (content upgrades per topic) → content-atomizer → content-calendar
```

#### Pattern 3: Launch Campaign
```
competitor-analysis → positioning-angles → launch-strategy → direct-response (landing page) → lead-magnet → email-sequences → dtc-ad-creative → linkedin-content + thread-writer
```

#### Pattern 4: Offer Redesign
```
competitor-analysis → offer-strategist → [new offer skill] → pricing-strategy → direct-response (new landing page) → dtc-ad-creative (new ads)
```

#### Pattern 5: Traffic Expansion (Multi-Channel)
```
keyword-research → seo-content (organic) + dtc-ad-creative (paid) + linkedin-content (B2B social) + thread-writer (X/Twitter) + content-calendar (scheduling)
```

#### Pattern 6: Measurement & Optimization Loop
```
google-analytics (baseline) → page-cro (audit) → ab-test-setup (design experiments) → [run tests] → google-analytics (measure results) → iterate
```

#### Pattern 7: SEO Recovery / Growth
```
seo-audit (technical health) → content-gap-analysis (missing topics) → serp-analyzer (competitive SERPs) → keyword-research (prioritize) → seo-content (produce) → content-calendar (publish cadence)
```

#### Pattern 8: B2B Pipeline Build
```
icp-builder → competitor-analysis → apollo-outreach (prospect research) → direct-response (outbound copy) → email-sequences (nurture) → hubspot (pipeline management)
```

#### Pattern 9: Content Repurposing Machine
```
seo-content OR newsletter (long-form) → content-atomizer (10-20+ pieces) → linkedin-content + thread-writer (social distribution) → content-calendar (scheduling)
```

#### Pattern 10: Growth Strategy Sprint
```
competitor-analysis → growth-strategy (model + metrics) → [choose channel patterns above] → google-analytics + ab-test-setup (measure + optimize)
```

#### Pattern 11: Paid Media Launch
```
demand-gen (funnel architecture) → icp-builder (audiences) → write-landing (page copy) → facebook-ads + google-ads (campaigns) → page-cro (optimize) → google-ads-report + ab-test-setup (measure)
```

#### Pattern 12: Full SEO Stack
```
keyword-research (strategy) → seo-content-brief (per-page specs) → SEO-content (produce) → programmatic-seo (scale patterns) → schema-markup (structured data) → backlink-audit (authority) → search-console (measure)
```

#### Pattern 13: Platform Expansion
```
content-atomizer (from best long-form) → social-content (multi-platform) → reddit-marketing (community) → bluesky (tech/journalist audience) → podcast-marketing (audio channel) → youtube-analytics (measure video)
```

#### Pattern 14: Product Launch
```
product-marketing (positioning + GTM) → demand-gen (B2B funnel) → write-landing (page) → email-sequences (nurture) → facebook-ads + google-ads (paid) → launch-strategy (week-by-week execution)
```

#### Pattern 15: Referral & Affiliate Growth
```
referral-program (design + viral mechanics) → affiliate-marketing (partner channel) → email-sequences (referral nurture) → brand-monitor (track mentions + PR)
```

#### Pattern 16: Onboarding Optimization
```
google-analytics (find drop-off points) → onboarding-cro (activation flow) → signup-flow-cro (funnel audit) → email-sequences (onboarding emails) → ab-test-setup (experiments)
```

## Inputs Required

To invoke this skill, provide whatever context you have:
- What business/product this is for
- What marketing assets currently exist
- What's working and what isn't
- What your goals are (revenue, leads, traffic, launch timeline)
- Any constraints (budget, time, team capacity)

The less you provide, the more questions the orchestrator will ask to diagnose accurately.

## Output Format

```
# Marketing System Audit: [Business/Product Name]

## Current State
[Inventory of what exists, organized by Foundation / Assets / System]

## Diagnosis
- Biggest gap: [Identified]
- Why it matters: [Impact of not addressing it]
- Dependencies: [What this blocks downstream]

## Recommended Next Step
- Skill: [Exact skill to invoke]
- What it will produce: [Deliverable]
- Prerequisites: [Inputs needed]
- Estimated effort: [Time]

## Full Roadmap (If Requested)
[Sprint-based plan with sequenced skill invocations]

## What to Skip for Now
[Things that can wait — and why]
```

## Saving Outputs to Docs

**IMPORTANT: Every skill output must be saved to `./docs/marketing/skill-outputs/` in the project working directory.**

### File Convention
- **Path:** `./docs/marketing/skill-outputs/[skill-name]-output.md` (e.g., `docs/marketing/skill-outputs/competitor-analysis-output.md`)
- **One file per skill.** Each run is appended to the same file, not saved as a new file.
- **Versioning is inside the file.** Each run starts with a `<!-- === RUN vN === -->` marker followed by a YAML metadata block:
  ```
  <!-- === RUN v2 === -->
  ---
  run: v2
  date: 2026-02-17
  business: FieldKit
  skill-version: 2026-02-15
  ---
  ```
- **Non-skill rollup docs** (e.g., marketing-execution-plan.md) go at `./docs/marketing/` top level, not in `skill-outputs/`.
- **The file should contain the complete skill output** — not a summary, not a truncated version. Everything that was produced.
- **When routing to the next skill,** instruct it to save its output following this convention.

### On First Run
If the file doesn't exist yet, create it with `<!-- === RUN v1 === -->`. If the file exists, read it to determine the latest run number and increment by 1.

### Why This Matters
- Creates a persistent record of all marketing strategy work with version history
- Downstream skills can reference upstream outputs (e.g., positioning-angles reads competitor-analysis)
- The user can review, share, and iterate on outputs across sessions
- Run-over-run comparison enables trend analysis and improvement tracking
- Prevents losing work if conversation context is compressed or a session ends

## Skill Registry Validation

Before recommending any skill, verify it exists and is current. The canonical skill list lives in `~/.claude/skills/marketing/`. When routing:

1. **Check the skill exists:** Confirm the SKILL.md file is present at `~/.claude/skills/marketing/[skill-name]/SKILL.md`
2. **Check the description matches:** Read the frontmatter to verify the skill still does what you think it does
3. **Never recommend a skill that doesn't exist.** If a gap requires a skill that hasn't been built, say so explicitly: "This gap needs a skill that doesn't exist yet: [description]."

**Registry last validated:** 2026-02-16. If this date is more than 30 days old, run a fresh validation by scanning `~/.claude/skills/marketing/*/SKILL.md` before making recommendations.

**Drift prevention:** Skills evolve — descriptions change, new skills are added, old ones are renamed or merged. To prevent recommending stale or nonexistent skills:
1. At the start of every orchestrator invocation, run `ls ~/.claude/skills/marketing/` and compare against the registry below
2. If any skill in the registry is missing from the filesystem, remove it from your recommendations and note the gap
3. If any skill exists on disk but not in the registry, read its SKILL.md frontmatter and add it to your mental model (but flag it as "unaudited" in your output)
4. If a skill's description in the registry doesn't match its current frontmatter, use the frontmatter (it's more current)

### Current Skill Registry (2026-06-13)

| Category | Skills |
|----------|--------|
| Foundation | `competitor-analysis`, `positioning-angles`, `icp-builder`, `brand-voice`, `growth-strategy`, `launch-strategy`, `content-strategy`, `product-marketing` |
| Offers | `offer-strategist`, `hormozi-grand-slam-offer`, `plg-freemium-offer`, `continuity-subscription-offer`, `value-ladder-offer`, `tripwire-offer`, `pricing-strategy` |
| Copy & Content | `direct-response`, `copywriting`, `copy-editing`, `lead-magnet`, `email-sequences`, `email-subject-lines`, `newsletter`, `SEO-content`, `content-atomizer`, `content-repurposing`, `customer-story`, `write-blog`, `write-landing` |
| Traffic & Distribution | `keyword-research`, `dtc-ad-creative`, `linkedin-content`, `thread-writer`, `content-calendar`, `video-strategy`, `social-content` |
| Paid Advertising | `facebook-ads`, `google-ads`, `google-ads-report` |
| Platform & Social | `reddit-marketing`, `bluesky`, `podcast-marketing`, `video-ad-analysis`, `youtube-analytics` |
| Social Proof & Trust | `review-strategy`, `customer-story` |
| Community & Brand | `community-strategy`, `founder-brand`, `brand-monitor` |
| Growth & Monetization | `demand-gen`, `referral-program`, `affiliate-marketing` |
| Measurement | `google-analytics`, `ab-test-setup`, `page-cro`, `onboarding-cro`, `signup-flow-cro` |
| SEO | `seo-audit`, `content-gap-analysis`, `serp-analyzer`, `backlink-audit`, `search-console`, `schema-markup`, `programmatic-seo`, `seo-content-brief` |
| Tools | `hubspot`, `apollo-outreach` |
| Research | `marketing-ideas`, `domain-research` |
| Notification Bots | `slack-bot`, `discord-bot`, `telegram-bot`, `feishu-lark` |
| Utility | `skill-refiner`, `blind-spot-audit`, `content-repurposing` |

## Quality Checks

- [ ] Did you inventory what actually exists before recommending? (Don't assume — ask or check.)
- [ ] Is the recommended next step the highest-impact gap — or just the most obvious one?
- [ ] Does the recommendation respect the dependency chain? (Don't recommend ads before positioning exists.)
- [ ] Is the recommendation specific enough to act on? ("Run the positioning-angles skill with these inputs" not "work on your positioning.")
- [ ] Have you identified what to SKIP — not just what to do? (Preventing wasted effort is as valuable as directing effort.)
- [ ] If building a multi-step plan, does each step's output feed the next step's input?
- [ ] Did you verify every recommended skill exists in the registry before recommending it?

---
name: orchestrator
description: Analyzes your current marketing state and tells you what to do next — which skills to invoke, in what order, and why. Use when you're unsure where to start, stuck on what the next step is, have completed a skill and need to know what follows, or want to audit your overall marketing system for gaps. This is the navigation layer across all marketing skills.
---

# Orchestrator Skill

