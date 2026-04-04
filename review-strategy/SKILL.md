---
name: review-strategy
description: Plan and execute review generation, reputation management, and social proof extraction across review platforms (G2, Capterra, Software Advice, Google Reviews, Product Hunt, app stores, Yelp, industry-specific sites). Includes platform selection by business type, solicitation sequences, response playbooks, listing optimization, competitor review analysis, and turning reviews into marketing assets. Use when the user asks about reviews, G2, Capterra, Software Advice, review generation, reputation management, testimonials, social proof, review strategy, listing optimization, review responses, or monitoring brand reputation on review sites.
---

# Review Strategy Skill

## Role
You are an expert in review generation, reputation management, and social proof strategy. You help businesses systematically build their review presence across the right platforms, turn customer satisfaction into public proof, and convert that proof into marketing assets that drive pipeline. You understand that reviews are not a vanity metric -- they are a trust layer that sits between marketing claims and purchase decisions. Every prospect reads them. Most businesses leave them to chance.

## Output Contract
This skill produces exactly:
1. **Platform selection matrix** (primary platforms with rationale, secondary, deprioritized)
2. **Current state assessment** (each platform: rating, review count, trend)
3. **Solicitation plan** (value moments, primary channel, sequence timing, monthly target)
4. **Response playbook** (positive response approach, negative response approach, escalation path)
5. **Listing optimization audit** (per-platform gaps and actions)
6. **Competitor review analysis** (rating, volume, trend, exploitable gaps)
7. **Social proof pipeline** (review-to-asset mapping, content destinations)
8. **Metrics dashboard** (volume targets, response rate targets, conversion targets, corrective actions)

This skill does NOT produce: Review platform integrations, automated collection, or response posting.

## When To Use This Skill
Use this skill when:
- A business needs to build review presence on G2, Capterra, Google, or other platforms
- Review volume is low or ratings are slipping and need a recovery plan
- The business wants to turn existing customer satisfaction into visible social proof
- Listings on review platforms are incomplete or unoptimized
- Competitor reviews reveal exploitable gaps
- Reviews need to be repurposed into testimonials, ad copy, case studies, or sales assets

## Inputs Required

### Required
1. **Business type and model** -- B2B SaaS, local service, consumer app, e-commerce, marketplace, etc.
2. **Current review landscape** -- Where do you have listings? What are current ratings and volumes?
3. **Customer base** -- Rough number of active customers, satisfaction signals (NPS, CSAT, retention)

### Strongly Recommended
4. **ICP profile** -- From `icp-builder` (determines which platforms matter and how to segment solicitation)
5. **Brand voice file** -- From `brand-voice` (ensures review responses and solicitation copy match tone)
6. **Competitor list** -- Top 3-5 competitors to analyze on review platforms

### Optional
7. **Existing review solicitation process** -- What you currently do (or do not do) to ask for reviews
8. **Customer journey map** -- Key milestones, value moments, touchpoints
9. **Sales cycle length** -- Affects timing of review asks
10. **Review platform logins** -- For listing audit and optimization

## Step 1: Platform Selection Framework

Not every platform matters for every business. Select platforms based on business type and buyer behavior.

### Platform Priority Matrix

| Business Type | Primary Platforms | Secondary Platforms | Tertiary |
|---|---|---|---|
| B2B SaaS | G2, Capterra | Software Advice, TrustRadius | Product Hunt, GetApp |
| Local Service | Google Business, Yelp | Angi, HomeAdvisor, BBB | Facebook, Nextdoor |
| Consumer App (iOS) | App Store | Google Play, Product Hunt | Reddit, social proof on site |
| Consumer App (Android) | Google Play | App Store, Product Hunt | Reddit, social proof on site |
| E-commerce | Google Shopping, Amazon | Trustpilot, Sitejabber | Product-specific forums |
| B2B Professional Services | Google Business, Clutch | G2, UpCity | Industry-specific directories |
| Healthcare/Medical | Google Business, Healthgrades | Zocdoc, Vitals | WebMD, RateMDs |
| Restaurant/Hospitality | Google Business, Yelp | TripAdvisor, OpenTable | Facebook, Foursquare |
| SaaS (Developer Tools) | G2, Product Hunt | GitHub stars, Stack Overflow | Hacker News mentions |

### Selection Criteria

For each potential platform, evaluate:

1. **Buyer presence** -- Do your ICPs actually check this platform before purchasing?
2. **Competitor presence** -- Are competitors active here? (If yes, you must be too)
3. **SEO value** -- Do platform listings rank for your category keywords?
4. **Integration with sales** -- Can reviews be embedded in sales materials, proposals, website?
5. **Effort-to-impact ratio** -- How much work to build and maintain vs. how much it influences deals?

Select 2-3 primary platforms. Do not spread thin across 8 platforms with 4 reviews each.

### Execution Branching by Business Type

Different business types require fundamentally different execution plans. Use the matching branch:

**IF B2B SaaS with <50 customers:**
- Focus exclusively on G2. One platform, done well.
- Channel: Personal email from founder or CS lead. No automation yet.
- Target: 2-3 reviews per month. Quality over volume.
- Key tactic: After every positive customer call, send a personalized review request within 2 hours while the goodwill is fresh.
- Do NOT ask during onboarding. Wait for first measurable outcome.

**IF B2B SaaS with 50-500 customers:**
- Primary: G2 + Capterra. Two platforms, parallel effort.
- Channel: Automated post-milestone email + personal asks for strategic accounts.
- Target: 5-10 reviews per month across both platforms.
- Key tactic: Segment by engagement. Power users get personal asks. Casual users get automated sequences.
- Add Software Advice once G2 has 25+ reviews.

**IF local service business (plumbing, HVAC, landscaping, etc.):**
- Primary: Google Business Profile. This is the only platform that matters for local discovery.
- Channel: Post-job SMS or text message. Send within 1 hour of job completion.
- Target: 10+ reviews per month. Volume matters for local SEO.
- Key tactic: Technicians hand the customer a card or send a text before leaving the job site: "If we did a good job today, a Google review helps us a lot."
- Secondary: Yelp and Angi, but only after Google has 50+ reviews.

**IF e-commerce with 1000+ transactions/month:**
- Primary: On-site product reviews (Yotpo, Judge.me, Stamped).
- Channel: Post-delivery automated email with photo upload option.
- Target: 50+ reviews per month. Product pages need fresh, recent reviews.
- Key tactic: Include the product photo in the review request email as a visual trigger. Offer a small incentive (10% off next order) for photo reviews specifically.
- Secondary: Google Shopping reviews, Trustpilot.

**IF marketplace or mobile app:**
- Primary: App Store (iOS) or Google Play (Android).
- Channel: In-app prompt at value moment. Follow Apple/Google guidelines strictly.
- Target: Maintain 4.5+ rating. Volume is secondary to rating for app store ranking.
- Key tactic: Trigger the review prompt after the user's 3rd successful action (not first — too early). Use the native rating dialog, not a custom prompt.
- Never ask after a crash, error, or frustrating moment.

## Step 2: Review Solicitation Strategy

### Timing Framework

The single biggest factor in review quality is WHEN you ask. Ask at the wrong time and you get silence or low-effort responses. Ask at the right time and you get detailed, enthusiastic proof.

**Value moments (ask here):**
- After first measurable outcome (not after signup -- after RESULT)
- After a support interaction rated positively
- After renewal or upgrade decision
- After a milestone: 100th use, 1-year anniversary, specific achievement
- After a customer gives unsolicited positive feedback (strike while warm)

**Anti-patterns (do not ask here):**
- Immediately after purchase (they have not experienced value yet)
- During onboarding friction (they are frustrated, not delighted)
- After a support ticket (unless explicitly resolved and rated positively)
- During billing issues or price increases
- Bulk blast to entire customer base with no segmentation

### Channel Selection

| Channel | Best For | Response Rate | Quality |
|---|---|---|---|
| In-app prompt | SaaS, mobile apps | 5-15% | Medium (often brief) |
| Personal email from CS/AM | B2B with named contacts | 15-30% | High (relationship-driven) |
| Automated email sequence | Scaled B2B and B2C | 3-8% | Medium |
| SMS | Local services, consumer | 8-15% | Medium-low (brief) |
| Post-call/meeting ask | High-touch B2B | 20-40% | Highest (guided) |
| QR code (physical location) | Local, retail, hospitality | 2-5% | Low-medium |
### Solicitation Copy Templates

**Template 1: Personal Email (B2B, from account manager)**

```
Subject: Quick favor -- 2 minutes?

Hey [Name],

Loved hearing about [specific result they shared -- e.g., "the 40% reduction
in onboarding time"]. That is exactly why we built [product].

Would you be open to sharing that on [G2/Capterra]? Takes about 2 minutes
and it genuinely helps other [their role/title]s find us.

Here is the direct link: [platform review link]

No pressure at all. And if you would prefer, I am happy to draft something
based on what you told me and send it over for your approval.

[Signature]
```

**Template 2: Automated Email (post-value-moment)**

```
Subject: You hit [milestone] -- mind sharing your experience?

[Name],

You just [specific achievement: "closed your 50th deal using [product]" /
"completed your 3rd month" / "processed $X in orders"].

That is worth celebrating.

It would mean a lot to our team if you shared a quick review on
[platform]. Other [ICP role]s use these reviews to make their decision,
and your experience is exactly what they need to hear.

[Leave a review -- takes 2 minutes] (button/link)

What to mention (if helpful):
- What problem you were solving when you found us
- What results you have seen so far
- Who you would recommend [product] to

Thanks for being a customer.

[Signature]
```

**Template 3: In-App Prompt (after value moment)**

```
Trigger: [User completes key action for the Nth time / reaches milestone]

"You have [achieved X] with [product]. Nice work.

Would you share your experience on [platform]? It takes 2 minutes
and helps others like you find us."

[Sure, I will share]  [Not right now]  [Do not ask again]
```

**Template 4: Follow-Up (if no response after 5-7 days)**

```
Subject: Re: Quick favor

[Name] -- just bumping this once. Totally understand if now is not
the right time. The link is here whenever: [link]

And if there is anything we could be doing better, I would rather
hear that directly. Always open to feedback.

[Signature]
```

### Solicitation Sequence Logic

```
Day 0: Value moment detected
Day 1: Send initial ask (Template 1 or 2)
Day 5-7: If no response, send follow-up (Template 4)
Day 14: If no response, mark as "asked, not converted" -- do not ask again for 90 days
Day 90+: Re-enter pool for next value moment trigger
```

Never send more than 2 asks per review request cycle. Never ask the same customer more than twice per year.

## Step 3: Review Response Playbook

Responding to reviews is not optional. Response rate directly affects platform ranking, buyer perception, and whether negative reviews define your narrative.

### Response Targets

- **Positive reviews**: Respond to 100% within 48 hours
- **Negative reviews**: Respond to 100% within 24 hours
- **Neutral reviews**: Respond to 100% within 48 hours

### Positive Review Response Template

```
[Name], thank you for this. [Reference something specific they said --
proves you actually read it, not a copy-paste response].

[If they mentioned a specific result]: That [result] is exactly what
we designed [product/feature] to do, and it is great to hear it is
working for your team.

We appreciate you taking the time to share this. It helps other
[their role/industry] teams find us.
```

**Rules for positive responses:**
- Reference something specific from their review (never generic "thanks for the kind words")
- Do not use the response as a sales pitch
- Keep it under 4 sentences
- Match their energy level -- if they wrote 3 sentences, respond with 2-3, not a novel

### Negative Review Response Template

```
[Name], thank you for sharing this. [Acknowledge the specific issue
without being defensive].

[If legitimate issue]: You are right that [issue]. We [have fixed this /
are working on this / understand why that is frustrating]. [Specific
action taken or timeline].

[If misunderstanding]: I want to make sure you get the most out of
[product]. [Clarify without condescending]. Would you be open to
connecting with our team at [email]? I would like to make this right.

[If already resolved]: I see we worked on this with you on [date] --
glad we could get it sorted. If anything else comes up, [contact info].
```

**Rules for negative responses:**
- Acknowledge the issue before explaining or defending
- Never argue publicly. Move detailed resolution to private channels.
- Include a specific next step or resolution
- Do not offer compensation publicly (invites gaming)
- Follow up privately even after public response
- If the issue has been fixed since the review, note the fix with a date

### Fake or Malicious Review Response

```
We take all feedback seriously, but we are unable to find an account
or interaction matching this review. If you are a customer, please
reach out to [email] so we can look into this and make it right.

We have also flagged this for the [platform] review team.
```

Then: flag the review through the platform dispute process with documentation.
## Step 4: Listing Optimization

An unoptimized listing is a wasted listing. Most buyers scan the profile before reading individual reviews.

### Profile Completeness Checklist

For each primary platform:

- [ ] Company description written for the buyer (not the company) -- what problem you solve, for whom
- [ ] Logo, banner, and visual assets are current and high-quality
- [ ] Category selection is accurate (primary + secondary categories)
- [ ] Product screenshots show the product in action, not marketing graphics
- [ ] Feature list is complete and uses buyer language (not internal feature names)
- [ ] Pricing information is current (or intentionally marked "Contact for pricing")
- [ ] Integration/compatibility information is listed
- [ ] Case studies or success stories are linked (if platform supports)
- [ ] Contact and demo CTAs are active and tracked
- [ ] Company size, founded date, and headquarters are accurate

### Competitive Positioning on Listings

On platforms like G2 and Capterra, you are displayed alongside competitors. Optimize for comparison:

1. **Headline/tagline**: Lead with your primary differentiator, not a generic description
2. **Screenshots**: Show the specific feature or workflow that separates you from alternatives
3. **Feature descriptions**: Emphasize capabilities where competitors are weak (informed by Step 6)
4. **Social proof callouts**: Highlight review themes that align with competitor weaknesses

### Platform-Specific Optimization

**G2:**
- Complete the G2 Grid positioning questionnaire thoroughly
- Encourage reviews that mention specific features (affects Grid placement)
- Respond to every review (response rate affects ranking)
- Maintain seasonal review velocity (G2 reports are quarterly)

**Capterra:**
- Maximize the "Capterra Shortlist" criteria: reviews, ratings, popularity signals
- Use all available screenshot slots with annotated product images
- Complete the detailed feature checklist for comparison accuracy

**Google Business:**
- Post weekly updates (Google rewards active profiles)
- Add all relevant categories and attributes
- Upload photos regularly (businesses with 100+ photos get 520% more calls)
- Enable messaging and Q&A, and monitor both
- Ensure NAP (Name, Address, Phone) consistency across all citations

**App Stores:**
- Optimize title, subtitle, and keyword field for search visibility
- Update screenshots for each major release
- Write release notes that reference user-requested features
- Respond to reviews (affects ranking algorithm)

## Step 5: Review Monitoring and Management System

### Monitoring Cadence

| Activity | Frequency | Owner |
|---|---|---|
| Check for new reviews (all platforms) | Daily | Marketing/CS |
| Respond to negative reviews | Within 24 hours | CS lead or founder |
| Respond to positive reviews | Within 48 hours | Marketing or CS |
| Review volume and rating trend report | Weekly | Marketing |
| Full listing audit (all platforms) | Monthly | Marketing |
| Competitor review analysis | Quarterly | Marketing/Strategy |
| Review-to-asset pipeline review | Monthly | Content/Marketing |

### Alert Setup

Configure alerts for:
- Any review under 3 stars (immediate notification to CS lead)
- Any review mentioning a competitor by name
- Review volume dropping below weekly target
- Rating average dropping below threshold (e.g., below 4.3)

### Review Tracking Spreadsheet Structure

```
| Date | Platform | Reviewer | Rating | Key Theme | Responded | Response Date | Asset Candidate | Notes |
|------|----------|----------|--------|-----------|-----------|---------------|-----------------|-------|
```

Track every review. Tag themes. Flag asset candidates. Measure response time.
## Step 6: Competitor Review Analysis

Read your competitors' reviews systematically. They tell you what their customers want, what they hate, and where you can win.

### Analysis Framework

For each top competitor (3-5), analyze their reviews on primary platforms:

**Collect:**
- Total review count and average rating
- Rating trend (improving or declining over 6-12 months)
- Top 10 most helpful positive reviews (what do happy customers love?)
- Top 10 most helpful negative reviews (what do unhappy customers hate?)
- Most frequently mentioned features (positive and negative)
- Response rate and response quality

**Categorize complaints into:**

| Category | Example Complaints | Your Advantage |
|---|---|---|
| Product gaps | "Missing [feature]" | Do you have it? |
| Reliability | "Crashes", "slow", "downtime" | Is yours more stable? |
| Support | "Cannot reach anyone", "slow response" | Is your support better? |
| Pricing | "Too expensive", "hidden fees", "price increase" | Are you more transparent? |
| Onboarding | "Steep learning curve", "took weeks to set up" | Is yours easier? |
| Integration | "Does not work with [tool]" | Do you integrate? |

**Extract actionable intelligence:**

1. **Positioning ammunition** -- Competitor weaknesses mentioned repeatedly in reviews become your ad copy angles and comparison page talking points
2. **Feature priorities** -- Features requested across multiple competitor reviews = validated demand
3. **Messaging gaps** -- What competitors promise in marketing but fail to deliver (per reviews) = trust gap you can exploit
4. **ICP refinement** -- Who leaves negative reviews? Those are prospects dissatisfied with the alternative -- your ideal targets

### Competitive Review Report Format

```
COMPETITOR REVIEW ANALYSIS: [Competitor Name]
Platform: [G2/Capterra/etc.]
Reviews Analyzed: [count] | Avg Rating: [X.X] | Trend: [up/down/flat]

TOP 3 PRAISED THEMES:
1. [Theme] -- mentioned in [X]% of positive reviews
2. [Theme]
3. [Theme]

TOP 3 COMPLAINT THEMES:
1. [Theme] -- mentioned in [X]% of negative reviews | YOUR POSITION: [advantage/parity/gap]
2. [Theme]
3. [Theme]

EXPLOITABLE GAPS:
- [Gap]: [How to use in your marketing]
- [Gap]: [How to use in your marketing]

REVIEW QUOTES TO REFERENCE:
- "[Direct quote from competitor negative review]" -- use in [comparison page / ad / sales deck]
```

## Step 7: Social Proof Extraction

Reviews sitting on third-party platforms are valuable. Reviews repurposed into your own marketing assets are more valuable. Build a pipeline from review to asset.

### Review-to-Asset Pipeline

| Review Type | Asset Output | Where It Goes |
|---|---|---|
| Detailed success story | Testimonial quote (attributed) | Website, landing pages |
| Specific metric mentioned | Data proof point | Ad copy, sales decks |
| Emotional/transformation review | Social media testimonial post | LinkedIn, Twitter, Instagram |
| Comparison to competitor | Comparison page quote | Website comparison pages |
| Feature-specific praise | Feature page testimonial | Product/feature pages |
| Long detailed review | Case study seed (outreach to reviewer) | Blog, sales enablement |
| Multiple reviews on same theme | Testimonial cluster page | Dedicated social proof page |

### Extraction Process

1. **Flag candidates** during daily monitoring (mark "Asset Candidate" = Yes in tracking sheet)
2. **Categorize** by asset type (quote, data point, case study seed, ad copy)
3. **Get permission** if using outside the review platform -- email the reviewer to ask if you can feature their words on your website or in your marketing materials
4. **Format for use:**

**Website testimonial format:**
```
"[Key quote -- 1-2 sentences max, focused on result or transformation]"

-- [Full Name], [Title], [Company] | via [Platform]
```

**Ad copy extraction:**
```
Before: [Pain point from review]
After: [Result from review]
Source: [Platform] review by [verified customer]
```

**Social post format:**
```
Our customers say it better than we ever could:

"[Review quote]"

-- [Name], [Title] at [Company]

[Link to full review on platform]
```

**Case study seed outreach:**
```
Subject: Your [Platform] review -- would you be up for a quick chat?

[Name],

Your [Platform] review caught our attention -- especially the part about
[specific result or detail].

We would love to turn your story into a case study. It would be a 20-minute
conversation about what you were doing before, what changed, and the
results. We handle all the writing.

Would you be open to that?

[Signature]
```

### Social Proof Page Structure

If review volume supports it, build a dedicated social proof page:

```
# What Our Customers Say

## By the Numbers
[Total reviews] reviews across [platforms] | [Avg rating] average rating

## Featured Stories
[3-5 expanded testimonials with photo, name, title, company, and 2-3 sentence quote]

## By Use Case
[Group testimonials by use case or pain point -- helps prospects find relevant proof]

## By Industry / Role
[Group by ICP segment if you serve multiple]

## See For Yourself
[Links to G2, Capterra, Google, etc. profile pages]
```
## Step 8: Metrics and Targets

### Review Volume Targets

| Stage | Monthly New Reviews (per platform) | Minimum Total Reviews |
|---|---|---|
| Early (0-50 customers) | 2-5 | 10+ to establish credibility |
| Growth (50-500 customers) | 5-15 | 50+ for platform ranking |
| Scale (500+ customers) | 15-30 | 100+ for category leadership |

### Key Metrics Dashboard

| Metric | Target | Measurement | If Below Target |
|---|---|---|---|
| Average rating (per platform) | 4.3+ (B2B SaaS), 4.5+ (local/consumer) | Weekly | Audit last 30 days of negatives for recurring themes. Is it a product issue (route to product team) or a service issue (route to CS)? Pause solicitation until root cause is addressed — more reviews at a low rating makes it worse. |
| Review velocity | [stage-appropriate target above] | Monthly | Expand solicitation channels. If email-only, add in-app or SMS. If automated-only, add personal asks from CS. Reduce friction — shorten the link path, offer to draft the review for them. |
| Response rate (all reviews) | 95%+ | Weekly | Assign a specific owner with a daily calendar block. Set up Slack/email alerts for new reviews. If no one owns it, no one does it. |
| Response time (negative) | Under 24 hours | Weekly | Escalation path is broken. Negative reviews need to route to a named person with authority to act. Set up a PagerDuty-style alert for sub-3-star reviews. |
| Response time (positive) | Under 48 hours | Weekly | Batch positive responses during a dedicated 15-minute block each morning. Lower effort than negative, so this is usually a priority problem, not a capacity problem. |
| Solicitation-to-review conversion | 10-20% | Monthly | Timing is wrong — you are asking at the wrong moment. Re-audit your value moments. Also check: is the review link broken? Does it require account creation? Every click of friction halves conversion. |
| Review-to-asset conversion | 15-25% of reviews become marketing assets | Monthly | The pipeline is broken, not the reviews. Assign someone to flag asset candidates weekly. If reviews are too generic to excerpt, your solicitation templates need to prompt for specifics ("What result did you see?"). |
| Profile completeness (per platform) | 100% | Monthly audit | Schedule a 30-minute monthly audit. Use the Profile Completeness Checklist from Step 4. Incomplete profiles leak credibility. |
| Competitor rating gap | Maintain parity or lead | Quarterly | If competitors are pulling ahead, increase velocity AND quality. Analyze their recent positive reviews — what are they doing that earns praise? Address the gap in your product or messaging. |

### Review Impact Measurement

Track these to connect review strategy to business outcomes:

- **Review page to signup/demo conversion rate** -- Are review platform profiles driving pipeline?
- **"How did you hear about us" attribution** -- What percentage cite reviews or specific platforms?
- **Win rate on deals where reviews were shared** vs. deals where they were not
- **SEO traffic to review platform listings** -- Are listings ranking for category keywords?
- **Sales cycle impact** -- Do deals close faster when review links are included in sales process?

## Output Format

Save the complete review strategy to `./docs/marketing/skill-outputs/review-strategy-output.md`. If the file already exists, append the new run with the next version number (see the orchestrator skill's "Saving Outputs to Docs" section for the full versioning convention).

```
REVIEW STRATEGY: [Business Name]
================================

PLATFORM SELECTION:
  Primary: [2-3 platforms with rationale]
  Secondary: [1-2 platforms]
  Deprioritized: [platforms not worth effort now, with reasoning]

CURRENT STATE:
  [Platform]: [rating] ([count] reviews) -- [trend]
  [Platform]: [rating] ([count] reviews) -- [trend]

SOLICITATION PLAN:
  Value moments identified: [list]
  Channel: [primary solicitation channel]
  Sequence: [timing and cadence]
  Monthly target: [number]

RESPONSE PLAYBOOK:
  Positive: [approach summary]
  Negative: [approach summary + escalation path]
  Owner: [who responds]

LISTING OPTIMIZATION:
  [Platform]: [gaps identified and actions]

COMPETITOR REVIEW INTEL:
  [Competitor]: [key exploitable gap]
  [Competitor]: [key exploitable gap]

SOCIAL PROOF PIPELINE:
  Asset targets: [what assets to create from reviews]
  Destinations: [where assets will be used]

METRICS:
  [Key targets with timeline]

90-DAY ACTION PLAN:
  Month 1: [Foundation -- listings, process, initial asks]
  Month 2: [Scale -- systematic solicitation, first asset extraction]
  Month 3: [Optimize -- analyze results, refine timing, expand platforms]
```

## Downstream Skill Handoffs

Review strategy generates assets and intelligence consumed by other skills:

| Output | Consuming Skill | How It Is Used |
|---|---|---|
| Testimonial quotes | `direct-response` | Social proof sections on landing pages |
| Review data points | `dtc-ad-creative` | Ad copy proof elements |
| Case study seeds | `content-strategy` | Case study content pipeline |
| Competitor review intel | `competitor-analysis` | Weakness validation and positioning ammo |
| Social proof posts | `content-atomizer` | Platform-specific testimonial content |
| Review page quotes | `email-sequences` | Social proof in nurture and sales sequences |
| Competitor complaint themes | `positioning-angles` | Differentiation angles grounded in real pain |

## Anti-Patterns to Avoid

### 1. The Spray and Pray
Sending identical review requests to every customer without segmentation.

**BAD:** Mass email blast to all 500 customers: "We'd love a review on G2! Click here." Sent on a Tuesday with no context, no personalization, no trigger event.

**GOOD:** Segmented ask to 15 customers who hit a milestone this month, personalized with their specific result: "Loved hearing about the 40% reduction in onboarding time. Would you share that on G2?"

### 2. The Incentive Trap
Offering rewards that look like buying reviews or violate platform TOS.

**BAD:** "Leave a 5-star review on G2 and get a $50 Amazon gift card!" This violates G2's terms, looks like review manipulation, and produces reviews that read like ads.

**GOOD:** "We're running a campaign to share more customer stories on G2. Everyone who leaves an honest review (positive or constructive) gets early access to our Q3 feature release." The incentive is for participation, not for a rating.

### 3. The Response Robot
Copy-pasting identical responses to every review.

**BAD:** Every review gets: "Thank you for your kind words! We're so glad you're enjoying [Product]. Your feedback means a lot to us!" Prospects reading your reviews notice this immediately.

**GOOD:** "Mike, glad the crew scheduling feature is saving your dispatchers that much time. We just shipped batch scheduling in v4.2 — sounds like your team would get a lot out of it." References their specific comments, adds value.

### 4. The Negative Spiral
Responding to negative reviews defensively or argumentatively.

**BAD:** "Actually, if you had read the documentation, you would know that feature is in Settings > Advanced > Integrations. We're sorry you found it confusing but it's clearly documented." This makes the company look petty and the reviewer vindicated.

**GOOD:** "You're right that finding the integration settings isn't intuitive. We've moved it to the main navigation in our latest update (v4.1). If you're still having trouble, email me directly at [email] — I want to make sure this works for you." Acknowledges, fixes, offers help.

### 5. The Quarterly Panic
Ignoring reviews for months, then doing a mass solicitation push that feels desperate and inauthentic.

**BAD:** Zero review activity for 4 months, then a week before the G2 quarterly report: "URGENT: We need 20 reviews this week! Everyone ask every customer!" The resulting reviews are low-effort, clustered, and obviously manufactured.

**GOOD:** Steady cadence of 3-5 asks per week, triggered by value moments. Reviews arrive naturally over time. No panic because the pipeline runs continuously.

### 6. The Vanity Collector
Pursuing volume of reviews instead of quality and specificity.

**BAD:** 50 reviews that all say "Great product!" or "Easy to use" or "Highly recommend." Zero specifics, zero persuasive weight. A prospect reads 5 of these and learns nothing.

**GOOD:** 20 reviews where each mentions a specific result: "Cut our invoicing time by 3 hours/week," "Went from paper to digital in 2 days," "Saved $12K in the first quarter." These sell. The short generic ones don't.

## Example Output (Partial)

Here is a partially completed strategy for FieldKit (B2B SaaS, FSM software for contractors):

```
REVIEW STRATEGY: FieldKit
================================

PLATFORM SELECTION:
  Primary: G2 (B2B SaaS buyers check G2 first; competitors Jobber and HCP
  have 200+ reviews each -- we need presence here to compete)
  Secondary: Capterra (strong SEO for "field service management software"
  keywords; Software Advice auto-syncs from Capterra)
  Deprioritized: Google Business (no physical location; low relevance for
  SaaS discovery), Product Hunt (good for launch, not ongoing reviews)

CURRENT STATE:
  G2: 4.7 rating (3 reviews) -- critically low volume, invisible in Grid
  Capterra: 0 reviews -- no listing claimed yet
  Software Advice: 0 reviews -- will sync from Capterra once active

SOLICITATION PLAN:
  Value moments identified:
    1. First invoice sent through FieldKit (activation proof)
    2. 30-day mark with >10 jobs completed (sustained usage)
    3. Customer reports time/money saved in support conversation
    4. Renewal or upgrade decision
  Channel: Personal email from founder (current scale allows it)
  Sequence:
    Day 0: Value moment detected
    Day 1: Personal email (Template 1 -- "Loved hearing about [result]")
    Day 6: Follow-up if no response (Template 4 -- light bump)
    Day 14: Mark "asked, not converted" -- wait 90 days
  Monthly target: 3-5 reviews (realistic for <50 customer base)

RESPONSE PLAYBOOK:
  Positive: Founder responds within 24 hours. Reference specific
  detail from their review. Thank them genuinely. No pitch.
  Negative: Founder responds within 12 hours. Acknowledge issue,
  state specific fix or timeline, offer direct contact.
  Owner: James (founder) until customer base exceeds 100, then CS lead.
```

**Example solicitation email for FieldKit:**

```
Subject: Quick favor -- 2 minutes?

Hey Mike,

Loved hearing that FieldKit cut your crew's paperwork time in half --
that's exactly what we built it for.

Would you be open to sharing that on G2? Takes about 2 minutes and
it genuinely helps other contractors find us when they're stuck
comparing Jobber and HCP.

Here's the direct link: [G2 review link]

No pressure at all. And if you'd prefer, I'm happy to draft something
based on what you told me and send it over for your approval.

-- James
```

**Example positive review response:**

```
Mike, thanks for this -- glad to hear the crew scheduling is saving
your dispatchers that much time. We just shipped batch job assignment
in the latest update, which sounds like it'd help your Monday morning
routing even more. Appreciate you taking the time to write this up.
```

## Quality Checks

- [ ] Are platform selections justified by business type and buyer behavior -- not just "be everywhere"?
- [ ] Does the solicitation strategy target value moments, not arbitrary time-based triggers?
- [ ] Are solicitation templates written in the brand voice (referencing docs/brand-voice.md if available)?
- [ ] Do response templates address the specific review content, not use generic copy-paste language?
- [ ] Is the negative review playbook specific enough to handle real scenarios -- not just "be empathetic"?
- [ ] Does the competitor analysis identify specific exploitable gaps with evidence from actual reviews?
- [ ] Is there a clear pipeline from review to marketing asset, with defined owners and cadence?
- [ ] Are metrics tied to business outcomes (pipeline, conversion, win rate), not just vanity numbers (total reviews)?
- [ ] Does the 90-day action plan have specific, assignable tasks -- not vague milestones?
- [ ] Has the strategy been segmented by ICP if multiple customer types exist (referencing docs/icp.md if available)?
- [ ] Are solicitation frequency limits defined to avoid annoying customers?
- [ ] Does the listing optimization go beyond "fill out the profile" to include competitive positioning?
