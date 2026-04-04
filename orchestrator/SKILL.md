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
| **Conversion path** (visitor → lead → customer) | ☐ Have / ☐ Missing | Multiple skills in sequence |
| **Nurture system** (how you stay in touch) | ☐ Have / ☐ Missing | `email-sequences` + `newsletter` |
| **Measurement** (how you know what's working) | ☐ Have / ☐ Missing | `google-analytics` + `ab-test-setup` |
| **CRO** (optimizing what you have) | ☐ Have / ☐ Missing | `page-cro` |
| **SEO health** (technical + content gaps) | ☐ Have / ☐ Missing | `seo-audit` + `content-gap-analysis` + `serp-analyzer` |
| **Content calendar** (scheduled publishing cadence) | ☐ Have / ☐ Missing | `content-calendar` |
| **CRM / outbound** (lead management, B2B outreach) | ☐ Have / ☐ Missing | `hubspot` + `apollo-outreach` |
| **Launch readiness** (go-to-market plan) | ☐ Have / ☐ Missing | `launch-strategy` |

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

17. **Need B2B leads?** Use `apollo-outreach` to research and enrich prospects, `hubspot` to manage the pipeline.

18. **Everything exists but nothing is working?** Go back to the foundation. Usually positioning is off or the offer doesn't resonate. → Re-run `competitor-analysis` + `positioning-angles` with fresh research.

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

#### Tools & Integrations
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `hubspot` | Manages CRM contacts, companies, deals | When managing a sales pipeline. |
| `apollo-outreach` | Researches and enriches B2B leads | When doing outbound prospecting. |

#### Utility
| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| `last30days` | Researches recent trends on Reddit + X + Web | When you need current market intelligence. |
| `content-atomizer` | Repurposes one piece into many platform formats | After producing any long-form content. |
| `skill-refiner` | Audits and improves skill output quality | After any skill produces subpar results. |

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

### Current Skill Registry (2026-02-16)

| Category | Skills |
|----------|--------|
| Foundation | `competitor-analysis`, `positioning-angles`, `icp-builder`, `brand-voice`, `growth-strategy`, `launch-strategy`, `content-strategy` |
| Offers | `offer-strategist`, `hormozi-grand-slam-offer`, `plg-freemium-offer`, `continuity-subscription-offer`, `value-ladder-offer`, `tripwire-offer`, `pricing-strategy` |
| Copy & Content | `direct-response`, `lead-magnet`, `email-sequences`, `newsletter`, `seo-content`, `content-atomizer`, `customer-story` |
| Traffic | `keyword-research`, `dtc-ad-creative`, `linkedin-content`, `thread-writer`, `content-calendar`, `video-strategy` |
| Social Proof & Trust | `review-strategy`, `customer-story` |
| Community & Brand | `community-strategy`, `founder-brand` |
| Measurement | `google-analytics`, `ab-test-setup`, `page-cro` |
| SEO | `seo-audit`, `content-gap-analysis`, `serp-analyzer` |
| Tools | `hubspot`, `apollo-outreach` |
| Utility | `last30days`, `skill-refiner`, `blind-spot-audit` |

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

