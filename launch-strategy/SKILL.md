---
name: launch-strategy
description: Plan and execute product launches with week-by-week timelines and channel-specific playbooks. Use when the user asks about launching a product, Product Hunt launch, go-to-market strategy, launch plan, beta program, pre-launch marketing, launch day execution, or post-launch growth. Trigger phrases include "product launch", "launch plan", "Product Hunt", "Hacker News launch", "go-to-market", "GTM strategy", "launch checklist", "pre-launch", "beta launch", "launch day", "launch sequence", "how to launch".
---

# Product Launch Strategy

You are an expert product launch strategist. When the user asks you to plan a launch, prepare for Product Hunt, or build a go-to-market strategy, follow this framework.

## Inputs Required

### Required
1. **Product description** — What you're launching (new product, feature, update, rebrand)
2. **Target audience** — Who is this launch for? (From `icp-builder` if available)
3. **Launch type** — Stealth/Alpha, Closed Beta, Open Beta, Soft Launch, Full Public, or Rolling
4. **Timeline** — Target launch date and how many weeks of prep available
5. **Success metrics** — What does a successful launch look like? (Signups, revenue, PH rank, press coverage)

### Strongly Recommended
6. **Existing audience size** — Email list, social following, community members
7. **Positioning output** — From `positioning-angles` (shapes all messaging)
8. **Brand voice file** — From `brand-voice` (ensures consistent tone across launch assets)
9. **Budget** — Total launch budget and allocation flexibility

### Optional
10. **Competitor timing** — Any competitive launches to avoid or counter
11. **Team capacity** — Who's available and their roles during launch
12. **Existing assets** — Demo video, screenshots, testimonials, case studies already available
13. **Channel constraints** — Channels you can't or won't use


## Output Contract
This skill produces exactly:
1. **Launch type selection** (stealth, closed beta, soft launch, full public, rolling) with timeline
2. **Week-by-week pre-launch timeline** (8+ weeks) with specific tasks per week
3. **Launch day execution checklist** hour-by-hour
4. **Platform-specific playbooks** for Product Hunt and Hacker News
5. **Post-launch phased plan** (weeks 2-8) with specific actions per week
6. **Metrics targets table** (pre-launch, launch day, post-launch KPIs)
7. **Budget allocation framework** with percentage breakdowns
8. **Contingency plan** for top 3 launch risks with mitigation strategies
9. **Downstream skill handoff table** identifying required assets from other skills

This skill does NOT produce: Marketing copy, ads, email sequences, or content pieces.

## Step 1: Gather Launch Context

Establish: product (new/feature/update), target audience, launch type (soft/beta/public), timeline, budget, team size, existing audience (list size, following), relevant channels, competitive timing, success metrics.

## Step 2: Launch Type Selection

| Type | Timeline | Audience | Best For |
|---|---|---|---|
| Stealth/Alpha | Ongoing | 10-50 hand-picked | Validating concept |
| Closed Beta | 2-4 weeks | 50-500 invited | Refining, testimonials |
| Open Beta | 2-4 weeks | Anyone | Waitlist buzz, stress test |
| Soft Launch | 1 week | Existing audience | Low-risk iteration |
| Full Public | 1 day (4-8 week prep) | Everyone | Maximum impact, PR |
| Rolling | 4-8 weeks | Phased access | Manage load, build FOMO |

## Step 3: Pre-Launch (8-4 Weeks Before)

### Week 8-6: Foundation

**Positioning**: One-sentence value prop. Elevator pitch (30s/60s/2min). Positioning statement:
```
For [audience] who [need], [product] is a [category] that [benefit].
Unlike [alternative], we [differentiator].
```

**Landing Page**: Clear headline, demo video, 3 benefits, email capture, social proof, FAQ. Set up analytics and email automation.

**Content Prep**: 3-5 blog posts for launch week, product demo video (60-90s), screenshots, social calendar, press release draft, founder story narrative.

### Week 6-4: Audience Building

**Waitlist Growth**: Building-in-public updates, referral waitlist, content marketing, community engagement (Reddit/Discord/Slack), micro-influencer outreach (20-50 people), LinkedIn founder posts.

**Waitlist Targets**: Solo founder: 500-5,000+. Small team: 1,000-10,000+. Funded: 5,000-50,000+.

**Beta Setup**: Select 50-200 from waitlist. Private feedback channel. Feedback template: What did you try? Success (1-5)? What was frustrating? Would you recommend? Would you pay?

### Week 4-2: Momentum

**Social Proof**: Request testimonials ("[Result] since using [product]. Before [pain]. Now [benefit]."). Collect usage metrics. Video testimonials.

**Amplification**: Newsletter authors, cross-promotion with complementary founders, advisors/investors briefed, "launch support" doc for network.

**Technical**: Load test for 10x traffic. Monitoring/alerting. Scaling plan. War room channel. On-call assignments.

## Step 4: Launch Week

### Day Before
- [ ] Final QA of product, page, links
- [ ] Queue social posts, pre-schedule email
- [ ] Brief team on roles
- [ ] Verify tracking pixels
- [ ] Test payment flows

### Launch Day

**Hour 0**: Publish everywhere. Send waitlist email. Post all social. Submit Product Hunt.
**Hours 1-4**: Respond to every mention/comment. Share traction updates. Fix bugs immediately. DM supporters.
**Hours 4-12**: Publish "why we built this" post. Share customer reactions. Behind-the-scenes content.
**Hours 12-24**: Day 1 recap email. Wrap-up social post. Respond to all tickets. Plan Day 2.

### Product Hunt Playbook

**Prep**: Build maker profile 2+ weeks early. Prepare: tagline (60 chars), description (260 chars), 5+ gallery images, maker comment (200+ words), 60-90s video.

**Launch Day**: Launch 12:01 AM PT. Post maker comment immediately. Share link by 6 AM PT. Respond to every comment within 30 min. Never ask for "upvotes" -- ask for "feedback." Target top 5.

**Post-PH**: Thank community. Add PH badge. Reach out to commenters. Write retrospective.

### Hacker News Playbook

**Title**: "Show HN: [Name] - [What it does in plain English]"
**Comment**: Technical architecture, why built, what's unique, honest limitations.
**Rules**: Post 8-10 AM ET Tue-Thu. Be humble and transparent. No superlatives. Respond to criticism gracefully.

### Social Media Blitz

**Twitter Thread**: (1) Hook + announcement + link, (2) Problem, (3) Solution + screenshot, (4) Proof/metrics, (5) Story/motivation, (6) CTA + link.
**LinkedIn**: Personal story, hook opening, lessons learned, CTA, tag supporters.
**Reddit**: Follow sub rules, lead with value/story, engage extensively.

## Step 5: Post-Launch (Weeks 2-8)

**Week 2**: Recap email, first case study, retargeting ads, media outreach, NPS collection.
**Week 3-4**: SEO content, comparison pages, onboarding optimization, outbound from leads.
**Week 5-6**: Funnel analysis, landing page A/B tests, double down on best channels, referral program.
**Week 7-8**: Scale paid ads, content partnerships, integrations, plan v2 launch.

## Step 6: Metrics

| Phase | Metric | Target |
|---|---|---|
| Pre-Launch | Waitlist sign-ups | [goal] |
| Pre-Launch | Waitlist CR | 20-40% |
| Pre-Launch | Beta activation | 60%+ |
| Launch Day | Sign-ups | [goal] |
| Launch Day | PH rank | Top 5 |
| Post-Launch | Activation rate | 40%+ |
| Post-Launch | D1/D7/D30 retention | 60%/30%/15%+ |
| Post-Launch | Trial-to-paid | 10-25% |
| Post-Launch | NPS | 40+ |

Track channel attribution by quality (activation rate, retention, LTV), not just volume.

## Step 7: Budget Allocation

| Category | % | Activities |
|---|---|---|
| Content | 20-25% | Video, blog, graphics |
| Paid Acquisition | 30-40% | Social ads, search ads, sponsorships |
| PR/Outreach | 10-15% | Media, influencers |
| Tools | 5-10% | Email, analytics, hosting |
| Reserve | 10-15% | Double down on what works |

**Zero-Budget**: Personal network, Product Hunt, Show HN, Reddit, Twitter thread, cold email journalists, cross-promotion, free email tools.

## Output Format

```
LAUNCH PLAN: [Product]
=======================
TYPE: [type] | DATE: [date] | TARGET: [metric]

TIMELINE: Week-by-week activities
CHANNEL PLAYBOOKS: Detailed per-channel plans
CONTENT CALENDAR: Pieces with publish dates
LAUNCH DAY CHECKLIST: Hour-by-hour execution
BUDGET: Category allocation
METRICS: KPIs with targets
RISK MITIGATION: Contingency plans
```

Tailor to the user's resources. A solo founder needs a different plan than a funded startup.

## Launch Type Branching

Not every launch follows the same timeline. Use the launch type to determine scope:

**IF Stealth/Alpha:**
- Timeline: Ongoing, no fixed launch date
- Skip: PR, Product Hunt, social blitz
- Focus: 1-on-1 outreach, hand-picking users, rapid iteration
- Assets needed: Minimal — invite email, feedback form

**IF Closed Beta:**
- Timeline: 2-4 weeks
- Skip: Paid ads, PR (save for public launch)
- Focus: Waitlist → invite flow, feedback loops, testimonial collection
- Assets needed: Landing page, onboarding flow, feedback template

**IF Full Public Launch:**
- Timeline: 4-8 weeks prep
- Full playbook: Pre-launch → launch day → post-launch per Steps 3-5
- Assets needed: Everything — landing page, demo video, press kit, social content, email sequences

**IF Rolling Launch:**
- Timeline: 4-8 weeks, phased access
- Focus: Controlled growth, managing capacity, building FOMO
- Unique: Waitlist with staggered invites, "next batch" email sequences

## Contingency Plans

Plan for the top 3 things that go wrong on launch day:

| Risk | Likelihood | Impact | Contingency |
|------|-----------|--------|-------------|
| **Site goes down** | Medium | Critical | Have a static fallback page. Monitor uptime. War room channel for instant response. Pre-scale infrastructure 3x expected traffic. |
| **Low initial traction** | Medium | High | Pre-schedule "boost" actions: personal outreach to 20 supporters, paid social boost on best-performing post, founder DMs to community leaders. |
| **Negative feedback / bug reports** | High | Medium | Prepared response template: acknowledge, timeline to fix, personal follow-up. Dedicated person monitoring support channels for first 48 hours. |
| **Competitor launches same day** | Low | Medium | Don't panic. Stay the course. Differentiation should already be clear from positioning. Consider accelerating a planned comparison piece. |

## Downstream Skill Handoffs

Launch requires outputs from multiple skills. Request these before starting launch execution:

| Asset Needed | Source Skill | What to Request |
|-------------|-------------|-----------------|
| Launch email sequence | `email-sequences` | Launch sequence type with announcement, social proof, urgency, last chance emails |
| Landing page copy | `direct-response` | Landing page with launch-specific CTA and proof elements |
| Social content | `content-atomizer` | Atomize launch announcement into platform-specific posts |
| Ad creative | `dtc-ad-creative` | Launch day ad concepts for paid amplification |
| Launch thread | `thread-writer` | Twitter/X thread for launch day announcement |

## Quality Checks

- [ ] Is the launch plan scoped to one launch type (not trying to cover all types at once)?
- [ ] Does every week in the timeline have specific, actionable tasks — not vague milestones?
- [ ] Are dependencies between tasks explicit (what must happen before what)?
- [ ] Is there a contingency plan for the top 3 things that could go wrong?
- [ ] Are success metrics defined before launch (not decided after)?
- [ ] Does the plan account for team capacity — or does it assume unlimited bandwidth?
- [ ] Is the post-launch phase (weeks 2-6) as detailed as the pre-launch phase?
