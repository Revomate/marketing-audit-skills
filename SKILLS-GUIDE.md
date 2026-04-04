# Marketing Skills Guide

41 skills organized into a system. Strategy flows top-down; start at the top, work your way through.

## Quick Start

Don't know where to begin? Run `/orchestrator` — it audits what you have and tells you what to do next.

---

## The Order: Foundation First, Then Build

```
Research → Position → Audience → Voice → Offer → Price → Copy → Capture → Nurture → Traffic → Measure → Optimize
```

Skip a step and everything downstream suffers. The orchestrator enforces this.

---

## All 41 Skills by Category

### 1. Foundation & Strategy

Run these first. Everything else depends on them.

| Skill | What it does | Invoke with |
|-------|-------------|-------------|
| **competitor-analysis** | Maps competitor SEO, ads, social, email, pricing, positioning | `/competitor-analysis` |
| **positioning-angles** | Finds how you're different — your unique angle | `/positioning-angles` |
| **icp-builder** | Defines ideal customer profiles and buyer personas | `/icp-builder` |
| **brand-voice** | Codifies tone, vocabulary, style rules into a reference doc | `/brand-voice` |
| **growth-strategy** | AARRR metrics, growth loops, experimentation frameworks | `/growth-strategy` |
| **launch-strategy** | Week-by-week launch playbooks (Product Hunt, HN, etc.) | `/launch-strategy` |
| **content-strategy** | Topic clusters, buyer journey mapping, distribution plans | `/content-strategy` |

**Typical order:** competitor-analysis → positioning-angles → icp-builder → brand-voice

### 2. Offer Architecture

Design what you sell and how you package it. Run `offer-strategist` first — it picks the right model.

| Skill | What it does | Invoke with |
|-------|-------------|-------------|
| **offer-strategist** | Routes you to the right offer model | `/offer-strategist` |
| **hormozi-grand-slam-offer** | Premium, incomparable offer ($100M Offers method) | `/hormozi-grand-slam-offer` |
| **plg-freemium-offer** | Free-to-paid self-serve model (SaaS) | `/plg-freemium-offer` |
| **continuity-subscription-offer** | Recurring revenue with churn prevention | `/continuity-subscription-offer` |
| **value-ladder-offer** | Multi-tier ascending price points | `/value-ladder-offer` |
| **tripwire-offer** | Low-cost entry offer to acquire buyers | `/tripwire-offer` |
| **pricing-strategy** | Pricing psychology, models, page optimization | `/pricing-strategy` |

**Typical order:** offer-strategist → [specific offer skill] → pricing-strategy

### 3. Copy & Content Production

Write the words that sell. Requires foundation skills to be done first.

| Skill | What it does | Invoke with |
|-------|-------------|-------------|
| **direct-response** | Conversion copy — landing pages, sales pages, emails, ads | `/direct-response` |
| **lead-magnet** | Lead capture assets (checklists, templates, mini-courses) | `/lead-magnet` |
| **email-sequences** | Automated flows — welcome, nurture, launch, win-back, etc. | `/email-sequences` |
| **newsletter** | Recurring newsletter design and edition production | `/newsletter` |
| **seo-content** | Blog posts and pages that rank AND convert | `/seo-content` |
| **content-atomizer** | Turns 1 piece into 10-20+ platform-specific pieces | `/content-atomizer` |

**Typical order:** direct-response (landing page) → lead-magnet → email-sequences → newsletter

### 4. Traffic & Distribution

Get people to see what you built. Run after assets exist.

| Skill | What it does | Invoke with |
|-------|-------------|-------------|
| **keyword-research** | SEO opportunity map and content pipeline | `/keyword-research` |
| **dtc-ad-creative** | Performance ad concepts (static, video, carousel) | `/dtc-ad-creative` |
| **linkedin-content** | High-performing LinkedIn posts and strategy | `/linkedin-content` |
| **thread-writer** | Viral X/Twitter threads and Reddit posts | `/thread-writer` |
| **content-calendar** | Publishing schedule across all platforms | `/content-calendar` |
| **video-strategy** | Video content plans for YouTube, TikTok, Reels, Shorts, webinars | `/video-strategy` |
| **founder-brand** | Founder personal brand as a growth channel — LinkedIn, speaking, thought leadership | `/founder-brand` |

**These can run in parallel** — organic, paid, and social are independent channels.

### 5. Measurement & Optimization

Measure what's working, fix what isn't. Run after traffic is flowing.

| Skill | What it does | Invoke with |
|-------|-------------|-------------|
| **google-analytics** | GA4 reports — traffic, behavior, conversions, audiences | `/google-analytics` |
| **ab-test-setup** | Experiment design with statistical rigor | `/ab-test-setup` |
| **page-cro** | Landing page conversion audit and optimization | `/page-cro` |

**Typical loop:** google-analytics → page-cro → ab-test-setup → run tests → repeat

### 6. SEO Health

Diagnose and fix organic search performance.

| Skill | What it does | Invoke with |
|-------|-------------|-------------|
| **seo-audit** | Full technical + on-page SEO audit | `/seo-audit` |
| **content-gap-analysis** | Finds topics competitors cover that you don't | `/content-gap-analysis` |
| **serp-analyzer** | Analyzes what's ranking and why for any keyword | `/serp-analyzer` |

**Typical order:** seo-audit → content-gap-analysis → serp-analyzer → keyword-research → seo-content

### 7. Proof & Reputation

Build social proof and manage how you show up to prospects.

| Skill | What it does | Invoke with |
|-------|-------------|-------------|
| **customer-story** | Case studies, testimonials, success stories in multiple formats | `/customer-story` |
| **review-strategy** | Review generation, reputation management across G2/Google/Yelp | `/review-strategy` |
| **community-strategy** | Community-led growth — owned communities + participating in existing ones | `/community-strategy` |

**Typical order:** customer-story → review-strategy → community-strategy

### 8. Rollups & Audits

Cross-skill synthesis and gap detection. Run after multiple skills have produced output.

| Skill | What it does | Invoke with |
|-------|-------------|-------------|
| **orchestrator** | Tells you what to do next across all skills | `/orchestrator` |
| **marketing-plan-rollup** | Synthesizes all skill outputs into one 90-day execution plan | `/marketing-plan-rollup` |
| **website-health-rollup** | Consolidates 7 website-focused skill outputs into one site health report | `/website-health-rollup` |
| **blind-spot-audit** | Scans marketing against a full checklist to find what's missing | `/blind-spot-audit` |
| **skill-refiner** | Audits and improves any skill's output quality | `/skill-refiner` |

---

## Common Workflows

### Zero to Funnel
```
competitor-analysis → positioning-angles → icp-builder → brand-voice
→ offer-strategist → [offer skill] → pricing-strategy
→ direct-response → lead-magnet → email-sequences
→ dtc-ad-creative
```

### Content Engine
```
content-strategy → keyword-research → content-gap-analysis
→ seo-content → content-atomizer → content-calendar
```

### Launch Campaign
```
competitor-analysis → positioning-angles → launch-strategy
→ direct-response → lead-magnet → email-sequences
→ dtc-ad-creative → linkedin-content + thread-writer
```

### Founder-Led Growth
```
icp-builder → brand-voice → founder-brand
→ linkedin-content → content-atomizer → content-calendar
→ video-strategy (when ready)
```

### Proof Stack
```
customer-story → review-strategy → community-strategy
→ content-atomizer (repurpose proof into social/email/ads)
```

### Full System Audit
```
blind-spot-audit → orchestrator → [fill gaps]
→ marketing-plan-rollup → website-health-rollup
```

### Optimization Loop
```
google-analytics → page-cro → ab-test-setup → [test] → repeat
```

### SEO Recovery
```
seo-audit → content-gap-analysis → serp-analyzer
→ keyword-research → seo-content → content-calendar
```

---

## Key Rules

1. **Never skip positioning.** Everything downstream depends on it.
2. **Run offer-strategist before building an offer.** It picks the right model so you don't waste time on the wrong one.
3. **Copy comes after voice.** Run brand-voice before writing anything with direct-response.
4. **Don't drive traffic to nothing.** Build the landing page, lead magnet, and email sequences before running ads or SEO.
5. **Measure everything.** Set up google-analytics early. Use ab-test-setup to make decisions with data, not guesses.
6. **When stuck, run /orchestrator.** It diagnoses your biggest gap and tells you exactly what to do next.