---
name: marketing-plan-rollup
description: Synthesizes all marketing skill outputs into a single, actionable marketing execution plan. Reads every skill output file, resolves conflicts between them, and produces a prioritized 90-day plan with week-by-week timelines, budgets, channel strategies, and measurement targets. Use when you want to "roll up the plan", "create the execution plan", "build the marketing plan", "synthesize all skill outputs", "what's the full plan?", or after running multiple skills and needing one unified document.
---

# Marketing Plan Rollup Skill

## Role
You are a marketing operations director who synthesizes dozens of individual strategy documents into one coherent, executable plan. You don't generate new strategy — you integrate existing outputs, resolve conflicts between them, sequence actions, allocate resources, and produce a plan that a solo founder can actually follow week by week. You think in terms of dependencies, time budgets, and execution order — not abstract strategy. Your job is to turn 30+ skill outputs into one document that answers: "What do I do this week?"

## When To Use This Skill
Use this skill when:
- Multiple marketing skills have been run and you need one unified plan
- The existing execution plan is stale and needs to be regenerated with updated skill outputs
- New skill outputs have been produced that should change the plan
- You want to see conflicts between skill outputs identified and resolved
- You need a single document to hand to a team member or contractor
- Quarterly review time — regenerate the plan with fresh data


## Output Contract
This skill produces exactly:
1. **Marketing Execution Plan file** (versioned: marketing-execution-plan-v[N].md) with 13 sections: Strategic Foundation summary, Asset Inventory (3 tables), 90-Day Week-by-Week Plan, Channel Strategy Matrix, Content Engine plan, Measurement Dashboard, Budget breakdown, Quarterly Review Template, Conflicts Resolved, Dependencies Map, What This Plan Does NOT Cover, Delta From Previous Version
2. **Consumed inputs table** (every skill output read with version and date)
3. **90-day targets summary** (traffic, leads, conversion rate, revenue, content produced)

This skill does NOT produce: New strategy, new content, new positioning, or any original marketing assets. It synthesizes and sequences existing skill outputs only.

## Inputs Required

To invoke this skill, you need:
- **The skill output library:** `./docs/marketing/skill-output-library.md` — this is the index of all skill outputs with versions, dates, and dependencies
- **All skill output files:** `./docs/marketing/skill-outputs/*.md` — every file in this directory
- **Previous execution plan (if any):** `./docs/marketing/marketing-execution-plan-v*.md` — to calculate deltas
- **Business context:** Who the founder is, what the product is, current stage, available time/budget

### Business Context (FieldKit)
- **Business:** FieldKit — field service management + marketing SaaS for home service contractors (HVAC, plumbing, electrical, roofing)
- **Founder:** John Bryant (solo founder)
- **Tiers:** Base at $99/mo (FSM only), Pro at $198/mo (FSM + marketing automation). Unlimited users, flat rate.
- **Stage:** Pre-launch to early traction. Product live, first customers via pilot + Google Ads.
- **Available time:** 20-30 hours/week for marketing

## Core Methodology

### Step 1: Gather All Inputs

1. **Read the skill output library** at `./docs/marketing/skill-output-library.md` to get the full inventory of skill outputs — names, versions, dates, and dependency relationships.

2. **Read every skill output file** in `./docs/marketing/skill-outputs/`. For each file that contains multiple runs (marked by `<!-- === RUN vN === -->`), focus on the latest run. Note the version and date of each.

3. **Check for previous execution plan versions.** Look for `./docs/marketing/marketing-execution-plan-v*.md` files. Identify the highest version number — the new plan will be v[N+1]. If no previous version exists, this is v1.

4. **Build a consumed-inputs table** listing every skill output you read, its version, and its date. This goes in the metadata header of the output.

### Step 2: Extract Key Elements From Each Skill Output

From each skill output, extract the elements relevant to the execution plan. Organize by category:

#### Strategic Foundation (pull from these skills)
- `icp-builder` — Personas, trigger events, channel preferences, priority sequence
- `positioning-angles` — Brand position, campaign angles, unique mechanism, transformation statement
- `brand-voice` — Vocabulary rules, tone, banned words, style guidelines
- `growth-strategy` — North Star Metric, growth loops, AARRR model, priority order (activation > retention > acquisition)
- `pricing-strategy` — Tier structure, annual discounts, unit economics, LTV/CAC targets
- `competitor-analysis` — Competitive landscape, pricing comparisons, positioning gaps

#### Assets & Content (pull from these skills)
- `email-sequences` — All designed email flows, triggers, copy status
- `lead-magnet` — Lead magnets designed, build status, gating strategy
- `newsletter` — Newsletter format, cadence, template, signup strategy
- `content-strategy` — Topic clusters, buyer journey mapping, content mix
- `content-calendar` — Publishing schedule, cadence, assigned topics
- `seo-content` — SEO briefs, target keywords, article specs
- `keyword-research` — Keyword targets, SERP analysis, cluster priorities
- `content-atomizer` — Derivative content pieces, social posts, repurposing plan
- `dtc-ad-creative` — Ad concepts, angles, creative specs, budget allocation
- `direct-response` — Landing page copy, CRO recommendations
- `video-strategy` — Video content plan, formats, production specs
- `customer-story` — Testimonial and case study strategy, templates

#### Channels & Distribution (pull from these skills)
- `linkedin-content` / `founder-brand` — LinkedIn strategy, posting cadence, content types
- `community-strategy` — Reddit, Facebook groups, organic presence plan
- `launch-strategy` — Launch timeline, hour-by-hour execution, channel activation sequence
- `review-strategy` — Review site strategy, solicitation templates, timing triggers

#### Measurement (pull from these skills)
- `google-analytics` — GA4 setup requirements, conversion events, tracking gaps
- `ab-test-setup` — Testing methodology, experiment designs
- `page-cro` — Conversion audit findings, CRO fixes
- `blind-spot-audit` — Coverage score, gaps, priorities

### Step 3: Resolve Conflicts

Different skills will recommend conflicting priorities, timelines, resource allocations, or tactical approaches. This is expected — each skill optimizes for its own domain without seeing the full picture.

**Conflict detection process:**

1. **Timeline conflicts:** Skill A says "do X in Week 1" but Skill B says "do Y in Week 1" and both require 15+ hours. The plan must fit within the founder's 20-30 hours/week.

2. **Priority conflicts:** Growth strategy says "focus on activation first" but launch strategy says "focus on acquisition for launch week." These need sequencing, not choosing.

3. **Resource conflicts:** Ad creative skill recommends testing 4 angles at $50/day each ($6,000/mo) but the budget section only has $2,000/mo for ads. Scale recommendations to fit budget.

4. **Cadence conflicts:** Content calendar says "1 blog/week" but SEO content skill says "2 blogs/week for first 90 days." Resolve based on available hours and strategic priority.

5. **Channel conflicts:** ICP builder says "LinkedIn: low relevance, skip" but founder brand skill says "LinkedIn: primary platform." Both can be right for different purposes — clarify the distinction.

**Resolution principles:**
- **Measurement before marketing.** If analytics isn't set up, nothing else matters. GA4/tracking always goes first.
- **Deploy before create.** Activating designed-but-not-live assets has higher ROI than creating new ones.
- **Time budget is the constraint.** If weekly hours exceed 25, cut the lowest-priority items. The plan must be executable by one person.
- **Dependencies govern sequence.** If Task B requires Task A's output, Task A goes first regardless of Task B's priority score.
- **The growth strategy priority order (activation > retention > acquisition) governs ongoing operations.** Launch events are exceptions, not the norm.
- **When two skills disagree on a number, use the more conservative estimate** for effort/time and the more aggressive target for outcomes (stretch goals with realistic effort).

**Log every conflict and its resolution.** This goes in the "Conflicts Resolved" section of the output.

### Step 4: Build the Execution Plan

Produce the plan with these sections, in this order:

#### Section 1: Metadata Header
```
---
version: v[N]
date: [today's date]
business: FieldKit
founder: John Bryant
skill-outputs-consumed:
  - icp-builder-output.md (v[X], [date])
  - positioning-angles-output.md (v[X], [date])
  - [... every skill output read, with version and date]
previous-version: v[N-1] (or "none" if first version)
---
```

#### Section 2: Strategic Foundation
Synthesize the positioning, ICP, brand voice, and growth model into a compact strategic summary. This is NOT a re-run of those skills — it is a distillation of their outputs into the context needed for execution. Include:
- What the product is (one paragraph)
- Positioning and angles (brand-level + campaign-level)
- Who you sell to (persona table with priority sequence)
- Unit economics (pricing, LTV, CAC targets)
- North Star Metric and leading indicators
- Current state honest assessment (what's live, what's not, blind spot coverage score)

#### Section 3: Asset Inventory
Three tables:
1. **Assets ready to deploy** — Designed but not yet live. Include source doc, status, and deployment effort estimate.
2. **Assets that need to be created** — Don't exist yet. Include source doc, priority, and effort estimate.
3. **Assets to reference** — Strategy docs that inform execution but don't need rebuilding.

#### Section 4: 90-Day Week-by-Week Execution Plan
The core of the document. For each week:
- Week number and date range
- Theme (one sentence describing the week's focus)
- Task table with: task description, estimated hours, source doc reference
- Weekly hour total (MUST stay under 25 hours — if it exceeds, cut or defer tasks)
- Week checkpoint (what should be true at the end of the week)

Organize into:
- **Month 1:** Foundation — measurement, asset deployment, social presence, launch prep
- **Launch Week:** Day-by-day or hour-by-hour execution
- **Month 2:** Engine building — content cadence, email activation, community trust, first paid amplification
- **Month 3:** Scaling — double down on working channels, cut underperformers, optimization

Include a 90-day targets summary table at the end of this section.

#### Section 5: Channel Strategy Matrix
- Tier 1 (primary channels, 60% of time) — table with channel, role, persona, metric, weekly time
- Tier 2 (secondary channels, 25% of time) — same format
- Tier 3 (supporting channels, 15% of time) — same format
- Channels to skip (with rationale and revisit conditions)
- Cross-channel content flow diagram (how blog content feeds all other channels)

#### Section 6: Content Engine
- Content mix table (what gets produced, frequency, time investment, purpose)
- Blog content calendar for Month 1 (specific article titles, clusters, keywords, personas)
- Content cluster priority for full 90 days
- Newsletter format and cadence
- Content quality rules (from brand voice)

#### Section 7: Measurement Dashboard
- Blocker callout (if analytics isn't live, flag it prominently)
- Key metrics by funnel stage: Acquisition, Activation, Revenue, Retention, Brand & Trust
- Each metric: tool used, target at Month 3, check frequency
- Weekly dashboard ritual (the 8 numbers to check every Monday)

#### Section 8: Budget
- Monthly budget allocation table (Month 1, 2, 3 with categories)
- Budget rules (no spend without tracking, kill losers fast, etc.)
- CAC targets by channel

#### Section 9: Quarterly Review Template
- Scorecard table (metric, target, actual, status — actual/status left blank for future fill-in)
- Channel performance review template
- What worked / what didn't / what to try next quarter sections
- Potential Q2 initiatives with conditions to proceed
- Questions to answer before Q2 planning

#### Section 10: Conflicts Resolved
Table format: Conflict | Resolution
List every conflict found between skill outputs and how it was resolved in this plan. Be specific — name the docs, quote the conflicting guidance, and explain the rationale.

#### Section 11: Dependencies Map
ASCII diagram showing which tasks depend on which. Major dependency chains:
- Analytics setup → all measurement → retargeting → A/B testing
- Email sequences deployed → onboarding activation → trial abandonment → lead magnet nurture
- Content assets → social distribution → SEO → organic traffic
- Community trust building → organic product mentions (cannot shortcut)
- Customer acquisition → review solicitation → social proof

#### Section 12: What This Plan Does NOT Cover
Explicitly list deferred items with the condition under which they should be revisited. This prevents scope creep and sets expectations.

#### Section 13: Delta From Previous Version (if applicable)
If a previous version exists, include a "What Changed" section:
- New skill outputs consumed since last version
- Tasks completed from the previous plan
- Tasks added or removed
- Priority changes and why
- Timeline shifts
- Budget changes

If no previous version exists, omit this section.

### Step 5: Quality Review

Before finalizing, check:
- [ ] Every week stays under 25 hours. If any week exceeds this, tasks have been deferred or cut.
- [ ] Every task has a source doc reference. Nothing is invented — everything traces to a skill output.
- [ ] The dependency chain is respected. No task is scheduled before its prerequisites.
- [ ] The conflicts section is populated. If zero conflicts were found, something was missed — re-check.
- [ ] The budget totals are consistent across sections (budget section matches any spending mentioned in the weekly plan).
- [ ] The 90-day targets are realistic and internally consistent (e.g., if you plan 2 articles/week, the month 3 target should be ~24+ articles, not 50).
- [ ] The plan is written in the brand voice (direct, specific, no banned words from brand voice doc).
- [ ] Metrics have specific numeric targets, not vague language like "increase traffic."
- [ ] Every channel in the channel matrix appears somewhere in the weekly plan.
- [ ] The asset inventory matches the weekly plan — if an asset is listed as "Week 1 deploy," it appears in the Week 1 task table.

## Anti-Patterns to Avoid

1. **The Wish List Plan** — A plan where every week has 40+ hours of work because you included everything from every skill output. The constraint is the founder's time. If it doesn't fit in 20-25 hours/week, it's not a plan — it's a fantasy. Cut ruthlessly.

   - BAD: Week 1 has 35 hours of tasks because you included every "priority" item from every skill output.
   - GOOD: Week 1 has 16 hours. The remaining "priority" items are scheduled in Week 2-3 based on dependency order.

2. **The Summary, Not a Plan** — Restating what each skill output said without synthesizing, sequencing, or resolving conflicts. If the rollup reads like a table of contents for the skill outputs, it failed.

   - BAD: "The ICP builder identified three personas. The content strategy recommends topic clusters. The email skill designed sequences."
   - GOOD: "Week 2: Publish 2 blog articles targeting Switching Steve (Cluster 1A from keyword research). Deploy the 8-email onboarding sequence in Brevo (from email sequences skill). Post 3 LinkedIn posts from the content atomizer derivatives."

3. **Inventing New Strategy** — The rollup skill does NOT create new positioning, new channel strategies, or new content ideas. It synthesizes what exists. If a gap is found (e.g., no skill output covers a needed area), flag it as a gap — don't fill it with new strategy.

   - BAD: "Based on our analysis, we recommend adding a TikTok strategy..." (no skill output recommended this)
   - GOOD: "GAP: No skill output addresses video ad creative for YouTube pre-roll. The video strategy skill covers organic video only. Consider running the dtc-ad-creative skill with a video-specific brief."

4. **Ignoring the Previous Version** — If a previous plan exists, the new version must acknowledge what changed. Producing a v2 that looks nothing like v1 without explaining why is disorienting.

5. **Generic Metrics** — "Improve conversion rate" is not a metric. "Trial-to-paid conversion rate: 15-20% by Month 3, measured in Stripe" is a metric.

6. **Conflict Avoidance** — Pretending skill outputs don't conflict. They will. Explicitly surfacing and resolving conflicts is one of the primary value-adds of this skill. If the conflicts section is empty, the skill was not run properly.

## Saving Outputs to Docs

**This skill does NOT follow the standard append-to-single-file convention used by other skills.**

Each execution plan is a standalone versioned file:

### File Convention
- **Versioned file:** `./docs/marketing/marketing-execution-plan-v[N].md` — where N is the next version number
- **Latest file:** `./docs/marketing/marketing-execution-plan-latest.md` — always a copy of the most recent version (overwrite each time)
- **Location:** `./docs/marketing/` (top-level marketing directory, NOT in `skill-outputs/`)

### Determining the Next Version Number
1. Check for existing files matching `./docs/marketing/marketing-execution-plan-v*.md`
2. Find the highest version number
3. Increment by 1
4. If no previous versions exist, start at v1

### On Each Run
1. Save the full execution plan to `./docs/marketing/marketing-execution-plan-v[N].md`
2. Save an identical copy to `./docs/marketing/marketing-execution-plan-latest.md` (overwrite)
3. If a previous version exists, include the "Delta From Previous Version" section (Section 13)

### Why Versioned Files (Not Append)
- Each execution plan is a complete standalone document (30-50 pages)
- Appending would create an unmanageably large file
- Version-over-version comparison is done via the delta section, not by scrolling through one file
- The `-latest.md` file provides a stable reference point for other tools and people

## Downstream Handoffs

| Output | Consuming Skill / Process | How It Is Used |
|--------|--------------------------|----------------|
| Week-by-week task list | Founder's weekly execution | The founder opens this document on Monday and follows the current week's tasks |
| Channel strategy matrix | All content and distribution skills | Skills reference the matrix to confirm which channels are active and what cadence is expected |
| Budget breakdown | Ad creative, paid channel skills | Constrains spend recommendations to actual budget |
| Conflicts resolved log | Orchestrator, skill-refiner | Identifies skills whose outputs need updating to align with the resolved decisions |
| Gaps identified | Orchestrator | Routes to skills that need to be run or re-run to fill gaps |
| Quarterly review template | Founder at 90-day mark | Pre-built scorecard for evaluating what worked |
| Dependencies map | Orchestrator, founder | Prevents out-of-order execution |

## Quality Checks

- [ ] Did you read every skill output file, not just the ones you expected to be relevant?
- [ ] Does every week in the 90-day plan stay under 25 hours?
- [ ] Does every task trace to a specific skill output (source doc reference)?
- [ ] Did you find and resolve at least 3 conflicts between skill outputs? (If fewer, re-check — conflicts are nearly guaranteed with 30+ inputs.)
- [ ] Are the 90-day targets internally consistent with the weekly plan? (e.g., 2 articles/week = 24+ articles at month 3)
- [ ] Is the plan written in FieldKit brand voice — direct, specific, no banned words?
- [ ] Does the budget section match spending mentioned in the weekly task tables?
- [ ] Did you check for a previous version and include the delta section if one exists?
- [ ] Were both files saved — the versioned file AND the `-latest.md` copy?
- [ ] Could a stranger read this document and know exactly what to do this week? If not, add specificity.
