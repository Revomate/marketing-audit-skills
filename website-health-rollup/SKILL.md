---
name: website-health-rollup
description: Consolidates 7 website-focused skill outputs (SEO Audit, SEO Checklist, Google Analytics, Page CRO, Direct Response, Content Gap Analysis, A/B Test Setup) into a single site health report. Deduplicates overlapping findings, resolves cross-skill conflicts, and produces a prioritized action list. Use when you want to "check site health", "what should I fix on the site?", "website health report", "site audit rollup", or after running website-related skills and needing one consolidated view.
---

# Website Health Rollup Skill

## Role
You are a website operations analyst who consolidates multiple site audits into one unified health report. You don't generate new analysis — you merge existing findings, deduplicate overlapping recommendations, resolve conflicts between audits, and produce a prioritized action list a founder can work through top-to-bottom. Your job is to turn 7 separate website-focused skill outputs into one document that answers: "What's broken, what's working, and what do I fix first?"

## When To Use This Skill
Use this skill when:
- Multiple website-focused skills have been run and findings overlap
- A founder wants one consolidated view of site health instead of reading 7 separate audits
- You need to identify conflicts between different audit recommendations
- Previous site health report is stale after re-running upstream skills
- You want a single prioritized fix list across SEO, CRO, analytics, and content


## Output Contract
This skill produces exactly:
1. **Website Health Report file** (versioned: website-health-report-v[N].md) with 9 sections: Site Health Scorecard (A-F grade), What's Working, Critical Fixes (prioritized), Action List (This Week/Month/Quarter), Conflicts Resolved, Measurement Gaps, What This Report Does NOT Cover, Delta From Previous Version
2. **Pre-flight staleness verdict** (FRESH vs STALE for each of 7 input skills)
3. **Re-run plan** (if staleness detected — stale skills listed in dependency order)

This skill does NOT produce: New audits, code changes, design mockups, or any changes to the site itself.

## Inputs Required

To invoke this skill, you need:
- **The skill output library:** `./docs/marketing/skill-output-library.md` — for version/date metadata on each input
- **7 website-focused skill output files** from `./docs/marketing/skill-outputs/`:
  1. `seo-audit-output.md` — Technical and on-page SEO findings
  2. `seo-checklist-output.md` — SEO implementation checklist
  3. `google-analytics-output.md` — GA4/GTM audit and tracking plan
  4. `page-cro-output.md` — Landing page conversion audit
  5. `direct-response-output.md` — Homepage copy and conversion recommendations
  6. `content-gap-analysis-output.md` — Content gaps vs. competitors
  7. `ab-test-setup-output.md` — Experiment designs and testing methodology
- **Previous rollup versions (if any):** `./docs/marketing/website-health-report-v*.md` — to calculate next version number and delta
- **Business context:** Who the founder is, product stage, site URL

### Business Context (FieldKit)
- **Business:** FieldKit — field service management + marketing SaaS for home service contractors (HVAC, plumbing, electrical, roofing)
- **Founder:** John Bryant (solo founder)
- **Tiers:** Base at $99/mo (FSM only), Pro at $198/mo (FSM + marketing automation). Unlimited users, flat rate.
- **Stage:** Pre-launch to early traction. Product live, first customers via pilot + Google Ads.
- **Site:** https://fieldkit.co

## Core Methodology

### Step 0: Pre-Flight Staleness Assessment

Before reading inputs, determine which upstream skill outputs are stale and need re-running. This step prevents the rollup from producing a report based on outdated audits.

**Skip this step on the very first run** (no previous rollup exists). On all subsequent runs, execute it before proceeding to Step 1.

#### 0a. Get the Previous Rollup Date

Read `./docs/marketing/website-health-report-latest.md` and extract the `date:` field from its YAML metadata. This is the baseline — anything that changed after this date may have made upstream skill outputs stale.

#### 0b. Git Diff Analysis

From the project root, run:

```bash
git log --since="[previous rollup date]" --name-only --pretty=format:"" | sort -u | grep -v '^$'
```

This produces every file that changed since the last rollup. Map each changed file to the upstream skill(s) it affects using the table below.

**File-to-Skill Mapping:**

| File pattern | Affected skill output(s) | Why |
|---|---|---|
| `app/**/page.tsx` (metadata exports), `app/**/layout.tsx`, `next.config.*`, `vercel.json` | SEO Audit, SEO Checklist | Page metadata, redirects, config |
| `**/sitemap*`, `**/robots*` | SEO Audit, SEO Checklist | Crawlability fundamentals |
| `**/*schema*`, `**/*structured-data*`, `**/*jsonld*` | SEO Audit, SEO Checklist | Structured data markup |
| `**/*gtm*`, `**/*analytics*`, `**/*gtag*`, `**/*dataLayer*`, `**/*tracking*` | Google Analytics | Tracking implementation |
| `**/pilot-form*` | Google Analytics | Contains conversion tracking code |
| `app/page.tsx` (content/layout changes), `app/components/**` | Page CRO, Direct Response | Homepage layout, UI components, copy |
| `app/pricing/**` | Page CRO | Pricing page conversion elements |
| `app/features/**` | Page CRO, SEO Audit | Features page content and structure |
| `app/compare/**` | Page CRO, Content Gap Analysis | Comparison page content |
| `**/pricing-toggle*`, `**/faq-accordion*`, `**/SavingsCalculator*` | Page CRO, Google Analytics | Interactive components (UX + tracking) |
| `**/hero*`, `**/cta*`, `**/testimonial*`, `**/social-proof*` | Page CRO, Direct Response | Conversion-critical elements |
| `app/blog/**` | Content Gap Analysis | New or updated blog content |
| `app/templates/**`, `app/tools/**` | Content Gap Analysis | New content types (templates, tools) |
| `**/middleware*`, `**/*experiment*`, `**/*posthog*`, `**/*feature-flag*`, `**/*variant*` | A/B Test Setup | Testing infrastructure |

**Mapping rules:**
- A file matching multiple patterns triggers ALL listed skills.
- `app/page.tsx` is the homepage — changes here affect Page CRO, Direct Response, AND SEO Audit.
- New route directories (e.g., `app/templates/`) indicate new page types — flag Content Gap Analysis.
- If no files match any pattern, the site code hasn't changed and upstream skills are likely current.

**Note:** These patterns are based on the FieldKit repo structure (Next.js 16 on Vercel). If the repo structure changes significantly (e.g., migration to a different framework), update this mapping table.

#### 0c. External Changes Checklist

Some changes happen outside the git repo. Present these yes/no questions to cover non-code changes:

1. **GA4 property settings** — Changed data retention, filters, Google Signals, or linked accounts (Search Console, Google Ads) since the last rollup?
2. **Google Ads** — Updated conversion IDs, created new campaigns, or changed landing page URLs?
3. **GTM web UI** — Added or modified tags/triggers/variables through the GTM interface (not in code)?
4. **DNS / hosting** — Changed domain redirects, SSL config, or Vercel settings?
5. **External tools** — Installed or removed third-party tools (Clarity, PostHog, chat widgets, heatmaps)?
6. **Content published outside git** — Published content through a CMS or external tool that doesn't go through the repo?

Map "yes" answers to affected skills:
- Questions 1-3 → Google Analytics
- Question 4 → SEO Audit, SEO Checklist
- Question 5 → Google Analytics (if tracking tool), Page CRO (if UX tool), A/B Test Setup (if testing tool)
- Question 6 → Content Gap Analysis

#### 0d. Produce Staleness Verdict

Combine git analysis + external checklist into a staleness verdict for each of the 7 input skills:

| Input Skill | Last Run | Git Changes Found | External Changes | Verdict |
|---|---|---|---|---|
| SEO Audit | [date] | [count] files | [yes/no] | STALE / CURRENT |
| SEO Checklist | [date] | [count] files | [yes/no] | STALE / CURRENT |
| Google Analytics | [date] | [count] files | [yes/no] | STALE / CURRENT |
| Page CRO | [date] | [count] files | [yes/no] | STALE / CURRENT |
| Direct Response | [date] | [count] files | [yes/no] | STALE / CURRENT |
| Content Gap Analysis | [date] | [count] files | [yes/no] | STALE / CURRENT |
| A/B Test Setup | [date] | [count] files | [yes/no] | STALE / CURRENT |

**Verdict rules:**
- **STALE** — Git changes affect this skill's domain OR external checklist flagged relevant changes.
- **CURRENT** — No git changes in this skill's domain AND no relevant external changes.

#### 0e. Re-Run Plan

If any inputs are STALE, produce a re-run plan before proceeding to Step 1. Order the re-runs by dependency (from the skill dependency flowchart):

1. **Standalone skills first** (no upstream dependencies): SEO Audit, SEO Checklist, Google Analytics
2. **Skills that depend on standalones**: Page CRO (depends on SEO Audit), Direct Response (depends on Positioning Angles — but PA doesn't change from site fixes, so DR can run in parallel with CRO)
3. **Analytical skills**: Content Gap Analysis, A/B Test Setup

**Present the re-run plan to the user** with the list of stale skills, the recommended order, and the specific git changes that triggered each one. Then:

- **If the user confirms:** Run the stale upstream skills in order, then proceed to Step 1 with fresh inputs.
- **If the user wants to skip re-runs:** Proceed to Step 1 but add a **Staleness Warning** section to the top of the report listing which inputs are stale and which findings may not reflect current site state.

### Step 1: Gather Inputs

1. **Read the skill output library** at `./docs/marketing/skill-output-library.md` to get version and date metadata for each input file.

2. **Read all 7 website-focused skill output files** from `./docs/marketing/skill-outputs/`. For files with multiple runs (marked by `<!-- === RUN vN === -->`), focus on the latest run. Note the version and date of each.

3. **Check for previous website health report versions.** Look for `./docs/marketing/website-health-report-v*.md` files. Identify the highest version number — the new report will be v[N+1]. If no previous version exists, this is v1.

4. **Build a consumed-inputs table** listing every skill output you read, its version, date, and what you extracted from it. This goes in the metadata section.

### Step 2: Extract & Categorize Findings

Pull every finding, recommendation, score, and action item from all 7 inputs. Categorize into these four buckets:

#### Technical Health (primary sources: SEO Audit, SEO Checklist, Google Analytics)
- Site speed, Core Web Vitals, mobile responsiveness
- Crawlability, indexation, sitemap, robots.txt
- Schema markup, structured data
- GA4/GTM implementation status, tracking gaps
- SSL, security headers, broken links
- Meta tags, title tags, canonical tags

#### Conversion & UX (primary sources: Page CRO, Direct Response, A/B Test Setup)
- Page layout, visual hierarchy, above-the-fold content
- CTAs — placement, copy, design
- Social proof, trust signals
- Form design, friction points
- Homepage copy effectiveness
- Proposed experiments and test designs

#### Content Gaps (primary sources: Content Gap Analysis, SEO Audit)
- Missing topic clusters vs. competitors
- Thin or missing pages (service pages, comparison pages, use-case pages)
- Content format gaps (video, tools, calculators)
- Keyword opportunities not covered
- Internal linking gaps

#### Measurement Readiness (primary sources: Google Analytics, A/B Test Setup)
- Which events are tracked vs. not tracked
- Conversion tracking completeness
- A/B testing infrastructure readiness
- Attribution model status
- Dashboard/reporting gaps

**For each finding, record:**
- The finding itself (specific, actionable)
- Source skill(s) — which output(s) it came from
- Priority/severity as stated in the source
- Any score or metric associated with it

### Step 3: Deduplicate & Resolve Conflicts

#### Deduplication Rules

Many findings will appear in multiple skill outputs. This is expected — different audits examine the same site through different lenses.

1. **Identical findings:** Same recommendation in 2+ sources → merge into one item. List all sources. The finding gets a **confidence boost** — if 3 skills independently flag it, it's almost certainly high-priority.

2. **Overlapping findings:** Similar but not identical (e.g., CRO says "add product screenshots to homepage" and A/B Test says "test hero image with product screenshot") → merge into one item, note the nuance from each source.

3. **Complementary findings:** Different aspects of the same issue (e.g., SEO Audit flags "missing alt text" and CRO flags "images need to show product in use") → group together as related items, keep distinct.

#### Conflict Detection & Resolution

Different audits optimize for different goals. Conflicts are expected.

**Common conflict patterns:**

1. **Navigation conflicts:** CRO may want fewer nav links (reduce distraction) while SEO wants more internal links (improve crawlability). **Resolution:** Keep nav focused on conversion-critical pages; add internal links in page body content and footer instead.

2. **Content length conflicts:** SEO wants longer pages (more keywords, topical authority) while CRO wants shorter pages (reduce bounce, faster decisions). **Resolution:** Use expandable sections, tabbed content, or progressive disclosure — long for crawlers, scannable for humans.

3. **Speed vs. richness conflicts:** CRO wants more social proof, videos, interactive elements while SEO/performance audits want fewer resources for faster load. **Resolution:** Lazy-load non-critical elements, prioritize above-the-fold speed.

4. **Priority conflicts:** Different skills assign different priority levels to the same underlying issue. **Resolution:** Use the confidence-boost principle — items flagged by more sources get higher priority. When tied, measurement fixes beat everything (can't optimize what you can't measure).

**Resolution principles (in priority order):**
1. **Measurement before optimization.** If you can't track it, don't optimize it. Analytics/tracking fixes always come first.
2. **Fix before test.** Fix obvious broken things before designing A/B tests around them.
3. **More sources = higher confidence.** A finding from 3 skills outranks a finding from 1 skill.
4. **Quick wins before heavy lifts.** At the same priority level, lower-effort items go first.
5. **Revenue path first.** Fixes on the conversion path (homepage → pricing → trial signup) outrank fixes on secondary pages.

**Log every conflict and its resolution.** This goes in the "Conflicts Resolved" section.

### Step 4: Build Report + Quality Review

Produce the report with the sections defined below, then run the quality checklist before finalizing.

## Output Format (8 Sections)

### Section 1: Metadata
```
---
version: v[N]
date: [today's date]
business: FieldKit
site: https://fieldkit.co
pre-flight: [ran / skipped (first run)]
stale-inputs-found: [count, or 0]
inputs-consumed:
  - seo-audit-output.md (v[X], [date]) [FRESH / STALE — re-run before this rollup]
  - seo-checklist-output.md (v[X], [date])
  - google-analytics-output.md (v[X], [date])
  - page-cro-output.md (v[X], [date])
  - direct-response-output.md (v[X], [date])
  - content-gap-analysis-output.md (v[X], [date])
  - ab-test-setup-output.md (v[X], [date])
previous-version: v[N-1] (or "none" if first version)
---
```

If the user chose to skip re-runs for stale inputs, add a **Staleness Warning** immediately after the metadata:

```
> **STALENESS WARNING:** This report was generated with [N] stale input(s).
> Findings from the following skills may not reflect current site state:
> - [skill name] — last run [date], [X] code changes since then
> - [skill name] — last run [date], external changes reported
>
> Sections most affected: [list sections]. Re-run these skills and regenerate the rollup for an accurate assessment.
```

### Section 2: Site Health Scorecard

Pull scores from the source audits (SEO Audit score, CRO score, GA implementation score) and present them in a unified scorecard. Include:

- **Individual audit scores** — as reported by each source skill, with the scoring scale used
- **Category scores** — Technical Health, Conversion & UX, Content Gaps, Measurement Readiness (derived from the individual scores and finding severity)
- **Overall site health grade** — A/B/C/D/F scale with clear criteria:
  - A: All categories green, no critical fixes
  - B: Minor issues only, no blockers
  - C: Some critical fixes needed but foundation is solid
  - D: Significant gaps, multiple blockers
  - F: Fundamental issues across multiple categories

### Section 3: What's Working

Positive findings across all audits. Things the site does well. This section prevents the report from being purely negative and helps the founder understand what NOT to break while fixing other things.

Format as a bulleted list grouped by category:
- **Technical:** [positive findings]
- **Conversion:** [positive findings]
- **Content:** [positive findings]
- **Measurement:** [positive findings]

### Section 4: Critical Fixes

The merged, deduplicated, prioritized list of issues that need immediate attention. These are blocking revenue, breaking user experience, or preventing measurement.

Table format:

| # | Issue | Impact | Effort | Sources | Notes |
|---|-------|--------|--------|---------|-------|
| 1 | [specific issue] | [High/Med/Low] | [hours estimate] | [skill names] | [resolution if it was a conflict] |

Rules:
- Every item must have at least one source skill reference
- Items flagged by 3+ sources get marked with a confidence indicator
- Impact considers: revenue impact, user experience impact, SEO impact
- Effort estimates in hours (not story points, not t-shirt sizes)
- If an item was a conflict between skills, the Notes column explains the resolution

### Section 5: Prioritized Action List

Three time horizons with specific tasks:

#### This Week (hours 1-20)
Tasks that are urgent, low-effort, or prerequisite to everything else. Primarily: measurement fixes, broken things, quick wins.

| Task | Hours | Source | Why Now |
|------|-------|--------|---------|
| [specific task] | [est.] | [skill] | [rationale] |

**Week total:** [must stay under 20 hours]

#### This Month (weeks 2-4)
Tasks that require more effort or depend on "This Week" items being done first.

| Task | Hours | Source | Depends On |
|------|-------|--------|------------|
| [specific task] | [est.] | [skill] | [prerequisite] |

#### Next Quarter
Larger initiatives, redesigns, content builds, or items that require traffic/data before they're actionable.

| Task | Hours | Source | Trigger Condition |
|------|-------|--------|-------------------|
| [specific task] | [est.] | [skill] | [when to start] |

### Section 6: Conflicts Resolved

Table of every cross-skill conflict found and how it was resolved.

| Conflict | Skill A Says | Skill B Says | Resolution | Rationale |
|----------|-------------|-------------|------------|-----------|
| [short name] | [quote/paraphrase] | [quote/paraphrase] | [what the report recommends] | [why] |

If zero conflicts are found, something was missed — go back and re-check. Website audits examining the same site from different angles will always have tension points.

### Section 7: Measurement Gaps

What can't be measured yet and what needs to be set up before optimization makes sense.

| Gap | Impact | Setup Effort | Source | Priority |
|-----|--------|-------------|--------|----------|
| [what's missing] | [what you can't do without it] | [hours] | [skill] | [1-5] |

Include a **Measurement Readiness Score:** X/10 — "You can measure [X]% of the metrics needed to optimize this site. Until this reaches 8/10, focus on measurement setup over optimization."

### Section 8: What This Report Does NOT Cover

Explicitly list what's out of scope with revisit conditions. This prevents scope creep and sets expectations.

| Deferred Item | Why Deferred | Revisit When |
|---------------|-------------|-------------|
| [item] | [reason] | [condition] |

Examples of things this report does NOT cover:
- Off-site SEO (backlinks, domain authority) — covered by other skills
- Content production (what to write) — covered by content strategy/calendar
- Ad performance — covered by DTC ad creative
- Email/automation — covered by email sequences
- Social media strategy — covered by founder brand / community strategy

### Section 9: Delta From Previous Version (if applicable)

If a previous version exists:
- New/updated inputs since last version
- Fixes completed from previous report
- New issues discovered
- Priority changes and why
- Score changes

If no previous version exists, omit this section.

## Quality Checklist

Before finalizing, verify:
- [ ] Every finding traces to a specific source skill output — nothing is invented
- [ ] Overlapping findings are merged, not duplicated (search for the same recommendation appearing in multiple places)
- [ ] The conflicts section is populated — if empty, re-examine the inputs
- [ ] Action list effort estimates are in hours
- [ ] "This Week" tasks total under 20 hours
- [ ] Measurement gaps are called out before optimization recommendations
- [ ] Scores in the scorecard match what the source skills actually reported
- [ ] What's Working section has at least 3 items (every site does something right)
- [ ] Written in FieldKit brand voice — direct, specific, no fluff
- [ ] The report could be understood by someone who hasn't read any of the 7 source files
- [ ] Both files saved — versioned and `-latest.md` copy

## Anti-Patterns to Avoid

1. **The Copy-Paste Compilation** — Dumping each audit's findings in sequence without merging, deduplicating, or resolving conflicts. If the report reads like 7 audits stapled together, it failed.

   - BAD: "SEO Audit Findings: ... Page CRO Findings: ... GA Findings: ..."
   - GOOD: Findings organized by category with source attribution, overlaps merged, conflicts resolved.

2. **Inventing New Findings** — This rollup consolidates existing analysis. It does NOT run new audits, scan the site, or generate original recommendations. If a gap is found, flag it — don't fill it.

   - BAD: "We also noticed the site could benefit from a chatbot..." (no source skill recommended this)
   - GOOD: "GAP: No input skill assessed chatbot/live chat impact on conversion. Consider running Page CRO with a chat-focused brief."

3. **Ignoring Conflicts** — Pretending all 7 audits agree. They won't. CRO and SEO have inherent tensions. Speed and richness trade off. Surfacing and resolving these conflicts is a primary value-add.

4. **Priority by Loudness** — Assigning priority based on which audit used the strongest language rather than actual impact. A "CRITICAL" label in one audit doesn't automatically outrank a "Medium" from three audits.

5. **Measurement Last** — Listing analytics/tracking fixes at the bottom. Measurement readiness is prerequisite to optimization. If you can't track conversions, redesigning the CTA is pointless.

## Saving Outputs to Docs

**This skill does NOT follow the standard append-to-single-file convention used by other skills.**

Each website health report is a standalone versioned file:

### File Convention
- **Versioned file:** `./docs/marketing/website-health-report-v[N].md` — where N is the next version number
- **Latest file:** `./docs/marketing/website-health-report-latest.md` — always a copy of the most recent version (overwrite each time)
- **Location:** `./docs/marketing/` (top-level marketing directory, NOT in `skill-outputs/`)

### Determining the Next Version Number
1. Check for existing files matching `./docs/marketing/website-health-report-v*.md`
2. Find the highest version number
3. Increment by 1
4. If no previous versions exist, start at v1

### On Each Run
1. Save the full report to `./docs/marketing/website-health-report-v[N].md`
2. Save an identical copy to `./docs/marketing/website-health-report-latest.md` (overwrite)
3. If a previous version exists, include the "Delta From Previous Version" section (Section 9)

### Why Versioned Files (Not Append)
- Each report is a complete standalone document
- Appending would create an unmanageably large file
- Version-over-version comparison is done via the delta section
- The `-latest.md` file provides a stable reference point

## Downstream Handoffs

| Output | Consuming Skill / Process | How It Is Used |
|--------|--------------------------|----------------|
| Prioritized action list | Founder's weekly execution | Work through the "This Week" list each Monday |
| Critical fixes table | Marketing Plan Rollup | Feeds into the 90-day execution plan's early weeks |
| Measurement gaps | Google Analytics skill | Identifies what needs to be re-run or set up |
| Conflicts resolved | Orchestrator, skill-refiner | Identifies skills whose outputs need updating |
| Site health scorecard | Quarterly review | Baseline for measuring improvement over time |
| What's Working | All content/CRO skills | Prevents breaking things that work during optimization |

## Quality Checks

- [ ] Did you run the pre-flight staleness assessment (Step 0) before gathering inputs? (Skip only on first-ever run.)
- [ ] If stale inputs were found, were upstream skills re-run OR was a staleness warning added to the report?
- [ ] Did you read all 7 input files, not just the ones you expected to be relevant?
- [ ] Does every finding trace to a specific skill output (source reference)?
- [ ] Did you find and resolve at least 2 conflicts between skill outputs?
- [ ] Are overlapping findings merged (not duplicated across sections)?
- [ ] Does the scorecard use scores actually present in the source files (not invented)?
- [ ] Is the action list prioritized with measurement/tracking first?
- [ ] Are effort estimates in hours, not vague terms?
- [ ] Is the report written in FieldKit brand voice — direct, specific, no banned words?
- [ ] Did you check for a previous version and include the delta section if one exists?
- [ ] Were both files saved — the versioned file AND the `-latest.md` copy?
