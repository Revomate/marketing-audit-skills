# Marketing Skill Library

**Claude Code Workflow Reference  •  41 Skills  •  `~/.claude/skills/marketing/`**

---

## From Scratch: Full Build Sequence

*Each step's output feeds the next step's input. Save outputs to files for cross-session handoff.*

| # | Phase | Action |
|---|-------|--------|
| 1 | Research | Perplexity MCP for market/competitor research. Playwright MCP for screenshots. |
| 2 | Competitors | `/competitor-analysis` — map competitor SEO, ads, social, email, pricing, positioning. |
| 3 | Positioning | `/positioning-angles` — feed it research. Get angle, transformation, voice, ICP. |
| 4 | Audience | `/icp-builder` — define ideal customer profiles and buyer personas. |
| 5 | Brand Voice | `/brand-voice` — translate positioning into persistent voice reference file. All downstream skills read this. |
| 6 | Strategy | `/growth-strategy` — AARRR metrics, growth loops, experimentation frameworks. |
| 7 | Offer | `/offer-strategist` → routes to specific offer skill (Grand Slam, PLG, Subscription, Value Ladder, Tripwire). |
| 8 | Pricing | `/pricing-strategy` — pricing psychology, models, page optimization. |
| 9 | Copy | `/direct-response` — landing page, homepage, website copy. |
| 10 | Lead Capture | `/lead-magnet` — opt-in asset, delivery page, follow-up emails. |
| 11 | Email Flows | `/email-sequences` — welcome, onboarding, nurture, launch, abandonment, post-purchase, win-back. |
| 12 | Newsletter | `/newsletter` — design format, cadence, structure. Produce editions. |
| 13 | SEO Pipeline | `/keyword-research` → `/seo-content` — organic traffic engine. |
| 14 | SEO Health | `/seo-audit` → `/content-gap-analysis` → `/serp-analyzer` — diagnose and fix organic performance. |
| 15 | Paid Traffic | `/dtc-ad-creative` — performance ad concepts at volume. |
| 16 | Social | `/linkedin-content` + `/thread-writer` + `/content-calendar` — organic distribution. |
| 17 | Video | `/video-strategy` — YouTube, TikTok, Reels, Shorts, webinars. |
| 18 | Founder Brand | `/founder-brand` — personal brand as a growth channel. |
| 19 | Content Repurposing | `/content-atomizer` — take any long-form piece → 15-25 platform-native derivatives. |
| 20 | Proof | `/customer-story` → `/review-strategy` → `/community-strategy` — build social proof stack. |
| 21 | Measure | `/google-analytics` → `/page-cro` → `/ab-test-setup` — optimization loop. |
| 22 | Launch | `/launch-strategy` — week-by-week launch playbooks. |
| 23 | Rollup | `/marketing-plan-rollup` — synthesize all outputs into one 90-day plan. |
| 24 | Site Health | `/website-health-rollup` — consolidate 7 website-focused skill outputs. |
| 25 | Blind Spots | `/blind-spot-audit` — scan for what's missing across all channels. |
| 26 | Refine | `/skill-refiner` after any weak output. Log builds over time. |

---

## Already Running: Fill the Gap

`/orchestrator` → tells you the biggest gap → **run that skill** → `/skill-refiner` if output needs work

---
## Skill Stacking Patterns

| Pattern | Sequence |
|---------|----------|
| Zero to Funnel | competitor-analysis → positioning → icp-builder → brand-voice → offer-strategist → [offer skill] → pricing-strategy → direct-response → lead-magnet → email-sequences → dtc-ad-creative |
| Content Engine | content-strategy → keyword-research → content-gap-analysis → seo-content → content-atomizer → content-calendar |
| Launch Campaign | competitor-analysis → positioning → launch-strategy → direct-response → lead-magnet → email-sequences → dtc-ad-creative → linkedin-content + thread-writer |
| Founder-Led Growth | icp-builder → brand-voice → founder-brand → linkedin-content → content-atomizer → content-calendar → video-strategy (when ready) |
| Proof Stack | customer-story → review-strategy → community-strategy → content-atomizer (repurpose proof into social/email/ads) |
| Offer Redesign | offer-strategist → [new offer skill] → pricing-strategy → direct-response (new landing page) → dtc-ad-creative (new ads) |
| Traffic Expansion | keyword-research + seo-content (organic) ‖ dtc-ad-creative (paid) ‖ linkedin-content + thread-writer (social) |
| Newsletter Build | brand-voice → newsletter (design format) → newsletter (produce editions) → content-atomizer (repurpose best editions) |
| Email Infrastructure | brand-voice → email-sequences (map full subscriber journey) → welcome → onboarding → nurture → launch → post-purchase → win-back |
| Content Flywheel | seo-content (or newsletter) → content-atomizer → derivatives feed social/email → social engagement feeds next content topic |
| Full Stack (new brand) | competitor-analysis → positioning → icp-builder → brand-voice → offer-strategist → [offer skill] → pricing-strategy → direct-response → lead-magnet → email-sequences → newsletter → keyword-research → seo-content → dtc-ad-creative → linkedin-content → content-atomizer → content-calendar → founder-brand |
| SEO Recovery | seo-audit → content-gap-analysis → serp-analyzer → keyword-research → seo-content → content-calendar |
| Optimization Loop | google-analytics → page-cro → ab-test-setup → [test] → repeat |
| Full System Audit | blind-spot-audit → orchestrator → [fill gaps] → marketing-plan-rollup → website-health-rollup |
| Video Launch | icp-builder → video-strategy → content-calendar → content-atomizer (repurpose video into text/social) |

---

## Practical Tips

- **Save outputs to files:** "Save the output to docs/positioning.md" — then reference it when invoking the next skill.
- **Brand voice first:** Run `/brand-voice` right after positioning. Save to `docs/brand-voice.md`. Every downstream skill should reference it.
- **SEO batch mode:** Run seo-content Step 0 research once, save the context brief, reference it for all subsequent pages.
- **Content flywheel:** Best newsletter editions and blog posts → `/content-atomizer` → 2 weeks of social content from each piece.
- **Newsletter cadence:** Pick a cadence you can sustain for 52 weeks. Consistency beats frequency. Start weekly.
- **Refinement cadence:** Run `/skill-refiner` after every run. Strategic review in Claude.ai after every 5-10 runs using the log.
- **Context management:** Use Option 1 (clear context + auto-accept) when executing plans. Separate terminals for research vs. execution.
- **Refinement log:** `~/.claude/skill-refinement-log.md` — the bridge between Claude Code and Claude.ai review sessions.
- **Rollups save time:** After running 5+ skills, use `/marketing-plan-rollup` to synthesize and resolve conflicts before executing.
- **Proof early:** Don't wait for perfect case studies. Run `/customer-story` with whatever you have — methodology proof, early results, industry data.

---

## Sample Prompts by Skill

*Copy, adapt, and paste. Replace bracketed context with your specifics.*

---

### Research (MCPs)

**Perplexity MCP** — Deep market research, competitor analysis, trend validation

> "Use Perplexity to do deep research on the field service management software market. I need: top 10 competitors by market share, pricing models, key differentiators, and what customers complain about most. Focus on the $1-5M revenue trades business segment."

> "Research the home remodeling market in Georgetown and North Austin TX. What are homeowners searching for? What do they complain about with contractors? What's the average project size for kitchen and bathroom remodels? What marketing channels are competitors using?"

> "Use Perplexity to research current Google algorithm updates and how AI Overviews are affecting service business websites. I need this as context before running the seo-content skill."

**Playwright MCP** — Browser automation, competitor screenshots, live SERP analysis

> "Use Playwright to screenshot the homepages and pricing pages of Jobber, Housecall Pro, and ServiceTitan. I want to analyze their positioning, hero sections, and how they frame their offers."

> "Use Playwright to search Google for 'kitchen remodeling Georgetown TX' and screenshot the top 5 results. I want to see what's ranking and how they structure their pages before I write competing content."

---

### Navigation & Audits

**`/orchestrator`** — Audits current state, routes to next skill

> "Use the orchestrator skill. Here's what I have for Fieldkit: positioning doc at docs/positioning.md, landing page is live, no lead magnet yet, no email sequences. What should I build next?"

> "I'm stuck. I have a bunch of marketing assets but nothing is converting. Run the orchestrator and tell me where the gap is. Here's what exists: [list assets]"

> "Run a full marketing system audit for Metro Custom Builders. I have a website, Jobber for scheduling, and HighLevel for CRM. No content, no ads, no lead magnets."

**`/blind-spot-audit`** — Scan for missing channels, tactics, opportunities

> "Run a blind-spot audit for my agency. We're doing SEO content, LinkedIn, and email. What channels and tactics are we not even thinking about? Check against 2026 best practices."

> "We feel like we're doing 'all the things' but growth has stalled. Run the blind-spot audit and tell me what's missing that we haven't considered."

**`/marketing-plan-rollup`** — Synthesize all skill outputs into one 90-day plan

> "I've run 12 skills and have outputs scattered across docs/marketing/skill-outputs/. Use marketing-plan-rollup to synthesize everything into one prioritized 90-day execution plan with weekly milestones and budgets."

**`/website-health-rollup`** — Consolidate website-focused skill outputs

> "I've run seo-audit, page-cro, google-analytics, and direct-response for my site. Use website-health-rollup to consolidate all findings, deduplicate, and give me one prioritized fix list."
---

### Foundation

**`/competitor-analysis`** — Full competitive landscape breakdown

> "Use the competitor-analysis skill for Fieldkit. Competitors are Jobber, Housecall Pro, ServiceTitan. Analyze their SEO, ads, social presence, email, pricing, and positioning. Find their weaknesses."

> "Run competitor analysis for my remodeling company in Georgetown TX. I want to know what the top 5 local competitors are doing for marketing — their websites, reviews, ads, and social."

**`/positioning-angles`** — Market position, angle, brand voice, ICP

> "Use the positioning-angles skill for Fieldkit. It's field service management software for trades businesses doing $1-5M revenue. Competitors are Jobber, Housecall Pro, ServiceTitan. Research is at docs/market-research.md. Find me an angle that separates us."

> "Run positioning-angles for Metro Service Pros. We're a handyman business in Georgetown TX. Competitors are mostly solo guys on Craigslist and a few franchises like Mr. Handyman. Our edge is we're fast, professional, and we actually show up when we say we will."

**`/icp-builder`** — Ideal customer profiles and buyer personas

> "Use icp-builder for my AI agency. We serve service businesses doing $1-10M who are losing revenue to manual processes. Build 3 distinct buyer personas with pain points, objections, and buying triggers."

> "Run icp-builder for Metro Custom Builders. We do $50-150K remodeling projects. I need to understand who's actually making the buying decision and what triggers them to start the process."

**`/brand-voice`** — Persistent voice reference file for all downstream skills

> "Use the brand-voice skill for Fieldkit. Positioning output is at docs/positioning.md. I also have our founder's Twitter feed and 3 blog posts — use those as voice samples. Produce the full voice file and save to docs/brand-voice.md."

> "Run brand-voice for Metro Custom Builders. Positioning is at docs/positioning.md. The founder talks like a straight-shooting contractor — no jargon, no BS. He sounds like Mike Holmes, not a marketing agency. Audiences are homeowners in Georgetown TX, mostly 35-55, dual income."

> "We've been getting inconsistent voice across our website, emails, and social. Use the brand-voice skill to codify what our voice should be. Here are 10 pieces of our best existing copy: [attach files]. Extract the patterns and produce a voice reference."

**`/growth-strategy`** — AARRR metrics, growth loops, experimentation frameworks

> "Use growth-strategy for my SaaS. I need a North Star Metric, AARRR funnel breakdown, and 3 growth loops we can test in the next 90 days. We're at $50K MRR with 200 paying customers."

> "Run growth-strategy for my agency. We're at $15K/mo and want to hit $50K/mo in 12 months. Help me identify the growth model — is it more clients, higher ACV, or adding recurring revenue?"

**`/content-strategy`** — Topic clusters, buyer journey mapping, distribution plans

> "Use content-strategy to map our content plan to the buyer journey. ICP at docs/icp.md, positioning at docs/positioning.md. I need topic clusters, content types per funnel stage, and a distribution plan."

**`/launch-strategy`** — Week-by-week launch playbooks

> "Use launch-strategy for our new AI voice agent product. We're targeting trades businesses. I need a 4-week launch plan covering pre-launch, launch week, and post-launch. Budget is $3,000."

> "Plan a Product Hunt launch for Fieldkit. We've never launched there. Give me the full playbook — pre-launch community building, launch day execution, and post-launch momentum."

**`/offer-strategist`** — Evaluates which offer model fits

> "Use the offer-strategist skill for Fieldkit. Positioning is at docs/positioning.md. It's a SaaS product for trades businesses. Help me figure out whether to go freemium, subscription, or some hybrid."

> "Run the offer strategist for my fractional CRO advisory practice. I'm targeting B2B SaaS companies doing $5-25M ARR who need sales leadership but can't afford a full-time CRO. Budget is $10-15K/month per client."

---

### Offer Models

**`/hormozi-grand-slam-offer`** — Premium, incomparable offer design

> "Use the Grand Slam Offer skill. I run a design-build remodeling company. Projects are $50-150K. I want an offer that makes price comparison impossible. Current positioning is at docs/positioning.md."

> "Build a Grand Slam offer for my fractional CRO service. The offer strategist routed me here. I want to package advisory + implementation so prospects can't compare me to a generic sales consultant."

**`/plg-freemium-offer`** — Self-serve free-to-paid (SaaS)

> "Use the PLG freemium skill for Fieldkit. Offer strategist recommended a hybrid PLG + subscription model. Design the free tier, activation path, and conversion triggers. Positioning at docs/positioning.md."

**`/continuity-subscription-offer`** — Recurring revenue model

> "Use the continuity subscription skill for Fieldkit. I need tier design, onboarding-to-activation flow, churn prevention system, and unit economics. The PLG skill already designed the free tier — output at docs/plg-tiers.md."

**`/value-ladder-offer`** — Multi-tier price ascension

> "Use the value ladder skill for my fractional CRO practice. I want to design a full ascension: free content → low-cost entry → core advisory retainer → premium embedded CRO. Revenue goal is $400K/year."

**`/tripwire-offer`** — Low-cost front-end acquisition

> "Use the tripwire offer skill. I need a $27-47 front-end offer for Fieldkit that converts free trial users into paying customers. The value ladder has the full ascension model at docs/value-ladder.md."

**`/pricing-strategy`** — Pricing psychology, models, page optimization

> "Use pricing-strategy for my agency's service packages. I have 3 tiers but nobody picks the middle one. Help me restructure with proper anchoring, decoy pricing, and page layout."

> "Run pricing-strategy for my SaaS. I'm at $49/mo flat rate and want to move to usage-based or per-seat. Help me model the transition without churning existing customers."
---

### Copy & Content

**`/direct-response`** — Landing pages, website copy, ad copy

> "Use the direct-response skill to write the Fieldkit landing page. Reference docs/positioning.md for brand voice and angle, and docs/offer.md for the offer details. Audience is trades business owners, problem-aware level."

> "Use direct-response to rewrite the Metro Custom Builders homepage. Current site is metrocustombuilders.com. Audience is homeowners in Georgetown TX considering a $50-150K remodel. Solution-aware level."

**`/email-sequences`** — Automated email flows

> "Use the email-sequences skill to build a 5-email welcome sequence for new Fieldkit newsletter subscribers. Brand voice at docs/brand-voice.md. After welcome, they should flow into a nurture sequence. Goal is to build trust and move them toward starting a free trial."

> "Design a 7-email SaaS onboarding sequence for Fieldkit free trial users. The activation metric is 'first job scheduled.' Brand voice at docs/brand-voice.md. Include behavioral branching — if they haven't scheduled a job by day 3, branch to a simplified tutorial path."

> "Map the full subscriber journey for Fieldkit. I need: welcome sequence, onboarding sequence, nurture sequence, launch sequence template, post-purchase sequence, and win-back sequence. Show me the journey map with entry points, transitions, and exit points between sequences."

**`/lead-magnet`** — List-building opt-in assets

> "Use the lead magnet skill for Fieldkit. Target audience is trades business owners doing $1-5M who are frustrated with their current software. The paid offer is the Fieldkit subscription. Give me 5-7 concepts scored by conversion potential."

> "Design a lead magnet for Metro Custom Builders that attracts homeowners in Georgetown thinking about a kitchen or bathroom remodel. Needs to bridge to booking a design consultation."

**`/newsletter`** — Newsletter design, format selection, and edition production

> "Use the newsletter skill to design a newsletter for Fieldkit from scratch. Audience is trades business owners doing $1-5M. Goal is trust building and nurture toward paid subscription. Brand voice at docs/brand-voice.md. I'm a solo founder so content capacity is limited — recommend a format I can sustain weekly."

> "Produce this week's Fieldkit newsletter edition. Format is 'The Tactician' (one actionable tactic per week). Topic: how to handle the spring rush — scheduling 3x the normal job volume without dropping balls. Reference docs/brand-voice.md for tone."

> "My newsletter open rates have dropped from 45% to 28% over the last 3 months. Use the newsletter skill to diagnose and redesign. Here are my last 10 subject lines and open rates: [list]. Brand voice at docs/brand-voice.md."

**`/seo-content`** — Search-optimized pages (batch mode)

> "Use the seo-content skill to produce 5 blog posts from the keyword briefs at docs/keyword-clusters.md. Run Step 0 research once and save the context brief, then batch all 5 pages from it."

> "Create a programmatic local landing page template for Metro Custom Builders using seo-content. Target pattern: [service] + [city]. Start with 'kitchen remodeling Georgetown TX' as the first page, then I'll scale to other cities."

**`/content-atomizer`** — One piece of content → 15-25 platform-native derivatives

> "Use the content-atomizer skill on this blog post: docs/blog-spring-scheduling.md. Target platforms: LinkedIn, X/Twitter, Instagram, and email. Brand voice at docs/brand-voice.md. I need 2 weeks of social content from this one post."

> "I just recorded a 45-minute podcast episode. Here's the transcript: [attach]. Use the content-atomizer to extract everything worth repurposing. I need X threads, LinkedIn posts, 3 short-form video scripts, and 2 email derivatives."

---

### Traffic & Distribution

**`/keyword-research`** — SEO opportunity pipeline

> "Use the keyword-research skill for Fieldkit. We're targeting trades business owners searching for FSM software, scheduling tools, and business management solutions. Find quick wins and programmatic SEO opportunities."

> "Run keyword research for Metro Custom Builders. We do kitchen remodels, bathroom remodels, and whole-home renovations in Georgetown and North Austin. Find local SEO opportunities."

**`/dtc-ad-creative`** — Performance ad concepts at volume

> "Use the DTC ad creative skill for Fieldkit. Platform is Meta (FB/IG). Target is trades business owners. Positioning at docs/positioning.md. Generate 3 angles with 3-5 hooks each, in static and video formats. I need enough variations to run a real test."

> "Create Meta ad concepts for Metro Custom Builders targeting homeowners in Georgetown TX. Offer is a free design consultation. I have 3 before/after project photos and 2 customer testimonials to work with."

**`/linkedin-content`** — High-performing LinkedIn posts and strategy

> "Use linkedin-content to write 5 posts for this week. I'm a founder of an AI agency targeting service businesses. Brand voice at docs/brand-voice.md. Mix: 2 insight posts, 1 story, 1 math post, 1 hot take."

> "My LinkedIn posts are getting <500 impressions. Use linkedin-content to audit my last 10 posts and redesign my approach. Profile URL: [link]."

**`/thread-writer`** — Viral X/Twitter threads and Reddit posts

> "Use thread-writer to turn this blog post into an X thread: docs/blog-ai-for-plumbers.md. Make it a story thread — open with a specific scenario, build tension, deliver the insight."

> "Write a Reddit post for r/smallbusiness about how much money businesses lose to missed calls. Not promotional — genuinely helpful. The CTA should be subtle."

**`/content-calendar`** — Publishing schedule across all platforms

> "Use content-calendar to build a 30-day publishing schedule. Channels: LinkedIn (daily), newsletter (weekly), blog (2x/month), X (3x/week). Align with our content pillars from docs/content-strategy.md."

**`/video-strategy`** — Video content plans for YouTube, TikTok, Reels, Shorts, webinars

> "Use video-strategy for my AI agency. I want to start a YouTube channel but I've never done video. Help me pick the right format, plan the first 10 episodes, and give me production guidelines I can follow with just a phone and basic editing."

> "Run video-strategy for my remodeling company. I have amazing before/after footage but I'm just posting it randomly on Instagram. Help me build a real video content strategy across platforms."

**`/founder-brand`** — Founder personal brand as a growth channel

> "Use founder-brand to build my personal brand strategy. I'm the co-founder of an AI agency. I have deep marketing experience and I'm building in public. My company brand is new but I have credibility in the space. Brand voice at docs/brand-voice.md."

> "I'm posting on LinkedIn but it feels random. Use founder-brand to create a positioning strategy for me as a founder — what topics I own, what I avoid, and a 90-day content plan."
---

### SEO Health

**`/seo-audit`** — Full technical + on-page SEO audit

> "Run a full SEO audit on metrocustombuilders.com. Check technical health, on-page optimization, and content gaps. Prioritize fixes by impact."

**`/content-gap-analysis`** — Topics competitors cover that you don't

> "Use content-gap-analysis to compare our blog against the top 3 competitors. Find the topics they rank for that we haven't touched. Competitor URLs: [list]."

**`/serp-analyzer`** — Analyze what's ranking and why for any keyword

> "Use serp-analyzer for 'AI for plumbers.' I want to know what's ranking, why, and how to create something better. Include AI Overview analysis."

---

### Proof & Reputation

**`/customer-story`** — Case studies, testimonials, success stories

> "Use customer-story to create a case study from this project. Client: Martinez family, $85K kitchen remodel, 8 weeks, came in on budget. I have before/after photos and a short quote from the client."

> "I don't have case studies yet. Use customer-story to build an interview guide and outreach sequence so I can collect my first 3 stories from existing clients."

> "Turn this customer testimonial into a full case study, 3 social proof snippets, and an email-ready story: [paste testimonial]."

**`/review-strategy`** — Review generation and reputation management

> "Use review-strategy for my agency. We have 4 Google reviews and zero G2 presence. Build a review generation system — who to ask, when, how, and on which platforms."

> "Our competitor has 200+ Google reviews and we have 12. Use review-strategy to build a catch-up plan that's sustainable, not spammy."

**`/community-strategy`** — Community-led growth

> "Use community-strategy for my AI agency. I want to know which existing communities I should participate in (Reddit, Slack groups, LinkedIn groups, local business groups) and whether building an owned community makes sense at our stage."

> "We're considering starting a Slack community for our clients and prospects. Use community-strategy to tell me if that's the right move, and if so, design the structure, engagement playbook, and launch plan."

---

### Measurement & Optimization

**`/google-analytics`** — GA4 reports and insights

> "Pull a GA4 report for the last 30 days. I want to see: top traffic sources, highest-converting pages, and where people are dropping off in the booking flow."

**`/page-cro`** — Landing page conversion audit

> "Use page-cro to audit our main landing page. Current conversion rate is 1.8% on 2,000 monthly visitors. URL: [link]. Tell me what's killing conversions and what to fix first."

**`/ab-test-setup`** — Experiment design with statistical rigor

> "Use ab-test-setup to design a headline test for our landing page. Current headline: [X]. I have 2 alternatives. Calculate sample size, test duration, and set up the measurement plan."

---

### Quality

**`/skill-refiner`** — Post-run diagnosis + skill edits

> "Use the skill-refiner to review the positioning-angles output I just got. The angles feel generic — they could apply to any FSM tool. Score it and tell me whether the skill needs editing or whether my inputs were too vague."

> "Run a full skill library audit. Check all skills for stale quality checks, handoff gaps, and input completeness. Output a prioritized improvement list."