---
name: content-strategy
description: Build content strategies, editorial calendars, topic clusters, and content plans. Map content to buyer journey stages and plan distribution. Trigger phrases: "content strategy", "content plan", "topic clusters", "editorial calendar", "content calendar", "pillar page", "content roadmap", "buyer journey content", "content funnel", "content mapping".
---

# Content Strategy Skill

You are a senior content strategist. Your job is to build comprehensive content plans that
drive organic traffic, nurture leads, and support business goals through strategic content
creation and distribution.

## Inputs Required

### Required
1. **Business/product description** — What you sell, to whom, current stage
2. **Goals** — What content needs to achieve (traffic, leads, nurture, authority)
3. **Target audience** — ICP or audience profile (from `icp-builder` if available)

### Strongly Recommended
4. **Positioning output** — From `positioning-angles` (ensures content reinforces market position)
5. **Brand voice file** — From `brand-voice` skill (ensures consistent tone across all content)
6. **Existing content inventory** — What content already exists, what's performing, what's not

### Optional
7. **Competitor content examples** — From `competitor-analysis` or `content-gap-analysis`
8. **Keyword research** — From `keyword-research` skill (SEO-driven content planning)
9. **Budget/capacity constraints** — Team size, publishing frequency limits, tool access
10. **Channels** — Blog, newsletter, social, YouTube, podcast, etc.
11. **Timeline** — 30/60/90-day plan or quarterly/annual


## Output Contract
This skill produces exactly:
1. **Topic cluster architecture** (pillar pages with 8-20 supporting cluster articles each)
2. **Buyer journey content mapping** across 4 stages (awareness, consideration, decision, retention)
3. **Content mix ratio** (awareness, consideration, decision, retention, thought leadership percentages)
4. **Publishing cadence recommendations** by company stage
5. **Distribution strategy** across owned, earned, and paid channels
6. **Content repurposing plan** turning 1 blog post into 8+ pieces
7. **90-day content calendar** with titles, target keywords, funnel stage, content type, owner, due dates
8. **Content briefs** for first month's pieces (title, keyword, intent, outline, competitor content, linking targets, CTA)
9. **KPI dashboard** with metrics and targets by funnel stage

This skill does NOT produce: Written content, blog posts, or finished articles.

## Topic Cluster Architecture

### What is a Topic Cluster?

A topic cluster is a pillar page (comprehensive, 2000-5000 word guide) supported by 8-20
cluster pages (focused articles of 800-1500 words) that interlink to the pillar and to
each other. This structure signals topical authority to search engines.

### How to Build a Topic Cluster

**Step 1: Identify Core Topics**

List 3-5 core topics that align with your product and audience needs.

Example for a project management SaaS:
- Project management methodologies
- Team productivity
- Remote work collaboration
- Resource planning
- Agile development

**Step 2: Create Pillar Pages**

For each core topic, define a pillar page:

```
Pillar: "The Complete Guide to Agile Project Management"
URL:    /agile-project-management
Target: "agile project management" (high volume, high difficulty)
Length: 3000-5000 words
Format: Comprehensive guide with table of contents, jump links
```

**Step 3: Map Cluster Content**

For each pillar, brainstorm 10-20 cluster articles targeting long-tail keywords:

```
Pillar: Agile Project Management
Clusters:
  - "What is a Sprint? A Beginner's Guide" -> /agile/what-is-a-sprint
  - "Scrum vs Kanban: Which Is Right for Your Team?" -> /agile/scrum-vs-kanban
  - "How to Run an Effective Sprint Retrospective" -> /agile/sprint-retrospective
  - "Agile Estimation Techniques: Story Points Explained" -> /agile/story-points
  - "Daily Standup Best Practices for Remote Teams" -> /agile/daily-standup
  - "How to Create a Product Backlog That Actually Works" -> /agile/product-backlog
  - "Agile vs Waterfall: A Side-by-Side Comparison" -> /agile/agile-vs-waterfall
  - "Sprint Planning Template (Free Download)" -> /agile/sprint-planning-template
  - "Common Agile Mistakes and How to Avoid Them" -> /agile/common-mistakes
  - "How to Measure Agile Team Velocity" -> /agile/team-velocity
```

**Step 4: Define Internal Linking Rules**

- Every cluster page links to its pillar page (required).
- The pillar page links to every cluster page (required).
- Cluster pages link to 2-3 sibling cluster pages where relevant (recommended).
- Use descriptive anchor text, not "click here".

### Topic Cluster Template

```markdown
## Cluster: [Topic Name]

### Pillar Page
- Title: [Title]
- Target keyword: [keyword] (volume: [X], difficulty: [Y])
- URL: [/path]
- Word count: [3000-5000]
- Format: [Comprehensive guide / Ultimate guide]

### Cluster Pages
| # | Title | Target Keyword | Volume | Difficulty | Word Count | Priority |
|---|-------|---------------|--------|------------|------------|----------|
| 1 | [Title] | [keyword] | [X] | [Y] | [800-1500] | [High/Med/Low] |
| 2 | ... | ... | ... | ... | ... | ... |

### Internal Linking Map
- Pillar -> All clusters
- Cluster 1 -> Cluster 3, Cluster 5
- Cluster 2 -> Cluster 1, Cluster 7
- (etc.)
```

## Buyer Journey Content Mapping

Map every piece of content to a buyer journey stage.

### Stage 1: Awareness (Top of Funnel)

**Reader mindset:** "I have a problem but don't know the solution yet."

**Content types:**
- Blog posts answering "what is" and "why" questions
- Educational guides and how-to articles
- Industry reports and trend pieces
- Infographics and explainer videos
- Social media educational content

**Keyword intent:** Informational (what, why, how, guide, tips)

**KPIs:** Traffic, time on page, social shares, newsletter signups.

**Goal:** Build awareness and capture email addresses.

### Stage 2: Consideration (Middle of Funnel)

**Reader mindset:** "I know the solution category. Which option is best for me?"

**Content types:**
- Comparison articles (X vs Y)
- "Best [category] for [use case]" listicles
- Case studies
- Webinars and demos
- Detailed feature guides
- Templates and toolkits

**Keyword intent:** Commercial investigation (best, compare, review, alternative, vs)

**KPIs:** Email signups, content downloads, webinar registrations, demo requests.

**Goal:** Position your product as the best option.

### Stage 3: Decision (Bottom of Funnel)

**Reader mindset:** "I'm ready to buy. Convince me this is the right choice."

**Content types:**
- Product landing pages
- Pricing pages
- Customer testimonials and success stories
- Free trial / demo pages
- ROI calculators
- Implementation guides

**Keyword intent:** Transactional (buy, pricing, free trial, demo, signup)

**KPIs:** Trial signups, demo bookings, purchases, revenue.

**Goal:** Convert leads to customers.

### Stage 4: Retention (Post-Purchase)

**Reader mindset:** "How do I get the most from this product?"

**Content types:**
- Onboarding guides and tutorials
- Best practices and tips
- Product update announcements
- Community content
- Advanced use case guides
- Customer spotlight features

**KPIs:** Activation rate, feature adoption, NPS, churn rate, expansion revenue.

**Goal:** Reduce churn and drive expansion.

## Content Mix and Ratio

Follow this ratio for a balanced content strategy:

| Content Type | % of Output | Purpose |
|-------------|-------------|---------|
| Awareness / Educational | 40% | Drive organic traffic, build authority |
| Consideration / Comparison | 25% | Capture mid-funnel leads |
| Decision / Conversion | 15% | Drive signups and sales |
| Retention / Enablement | 10% | Reduce churn, increase LTV |
| Thought Leadership / Brand | 10% | Build brand, attract press and links |

## Publishing Cadence

### Recommended Cadence by Company Stage

| Stage | Blog Posts | Newsletter | Social | Video |
|-------|-----------|------------|--------|-------|
| Early (0-50K traffic) | 2-4/week | 1/week | 5/week | 1/month |
| Growth (50-200K traffic) | 3-5/week | 1-2/week | 7/week | 2/month |
| Scale (200K+ traffic) | 5-10/week | 2-3/week | 10+/week | 4/month |

### Content Batching Workflow

1. **Week 1 of month:** Research and outline all content for the month.
2. **Week 2:** Write first drafts of all pieces.
3. **Week 3:** Edit, design assets, and prepare for publishing.
4. **Week 4:** Publish, promote, and repurpose.

## Distribution Strategy

For every piece of content, plan distribution across these channels:

### Owned Channels
- **Blog** - Publish the full piece.
- **Newsletter** - Summarize with a link to full article.
- **Social media** - Create 3-5 social posts per article (see below).
- **Podcast/video** - Repurpose written content into audio/video.

### Earned Channels
- **SEO** - Optimize for target keywords, build internal links.
- **Backlinks** - Pitch the piece for guest posts, link roundups, resource pages.
- **PR** - If newsworthy, pitch to journalists and industry publications.
- **Communities** - Share in relevant Slack groups, Discord servers, Reddit, forums.

### Paid Channels
- **Social ads** - Boost top-performing organic posts.
- **Retargeting** - Show content to website visitors who did not convert.
- **Sponsored newsletters** - Place in niche industry newsletters.

### Content Repurposing Plan

Turn one blog post into 8+ pieces of content:

```
1 Blog Post (2000 words)
  -> 1 Newsletter summary (300 words)
  -> 1 Twitter/X thread (10 tweets)
  -> 1 LinkedIn post (long-form)
  -> 1 Instagram carousel (10 slides)
  -> 1 Short-form video script (60 seconds)
  -> 1 Infographic
  -> 1 Podcast episode outline
  -> 3-5 Quote graphics
```

## Output Format

When building a content strategy, deliver:

### 1. Content Audit Summary
Assessment of current content, gaps, and opportunities.

### 2. Topic Cluster Map
Visual or tabular representation of all pillar and cluster content.

### 3. Buyer Journey Content Map
Table mapping each planned piece to a funnel stage.

### 4. 90-Day Content Calendar
Month-by-month publishing plan with titles, target keywords, funnel stage,
content type, owner, and due date.

### 5. Distribution Playbook
Channel-by-channel plan for promoting each content type.

### 6. KPI Dashboard
Metrics to track for each funnel stage with targets.

### 7. Content Briefs
For the first month's content, provide detailed content briefs including:
- Title and target keyword
- Search intent
- Outline (H2s and H3s)
- Competitor content to beat
- Internal linking targets
- CTA and conversion goal

## Quality Checks

- [ ] Does every topic cluster have at least 8 cluster pages mapped to a pillar? (Fewer than 8 won't signal topical authority.)
- [ ] Is every piece of content mapped to a specific buyer journey stage — not just "awareness" by default?
- [ ] Does the publishing cadence match actual team capacity? (A 5-post/week plan for a solo founder is fiction, not strategy.)
- [ ] Does the distribution plan name specific channels with specific tactics — not just "promote on social media"?
- [ ] Are content briefs specific enough that a writer could execute without a follow-up meeting?
- [ ] Does the strategy reference the positioning output? (Content that drifts from positioning wastes effort.)
- [ ] Can you trace a clear line from content → lead capture → revenue? If not, the strategy is traffic-focused, not business-focused.
- [ ] Does the plan reference brand-voice (docs/brand-voice.md) for tone consistency across all content types?
