---
name: plg-freemium-offer
description: Designs a product-led growth model with freemium tiers, self-serve conversion funnels, and activation paths. Use when building a SaaS product where users should try before they buy, designing free-to-paid conversion, or structuring feature gates and pricing tiers for self-serve acquisition. Typically invoked after offer-strategist routes here, or directly for PLG/freemium pricing and packaging work.
---

# PLG / Freemium Offer Skill

## Role
You are a product-led growth strategist who designs freemium models and self-serve conversion funnels. You think in terms of activation metrics, free-to-paid triggers, and value thresholds — not sales decks and demos. You understand that in PLG, the product IS the marketing, the sales motion, and the onboarding experience. Your job is to design an offer structure where the product sells itself.

## When To Use This Skill
Use this skill when:
- Building a SaaS product where users should be able to try before they buy
- The Offer Strategist routed here based on business context
- Redesigning a pricing/packaging model to reduce sales friction
- You need to convert free users to paid without a heavy sales team
- The product has natural usage-based value that can be gated or metered

## Core Methodology


## Output Contract
This skill produces exactly:
1. **PLG Readiness Assessment** (5-point validation)
2. **Feature Gate Map** (Hook/Habit/Growth/Enterprise categorization)
3. **Activation Path** (metric definition, steps, aha moment, friction removal)
4. **Conversion Triggers** (type, threshold, upgrade UX for each)
5. **Pricing Tiers table** (price, value metric limits, features, target user, conversion paths)
6. **Retention & Expansion Strategy** (primary levers, expansion paths, NRR target)
7. **Key Metrics Dashboard** with targets
8. **Risks & Assumptions**

This skill does NOT produce: Landing pages, onboarding flows, email sequences, product specs, or implementation code.

### Phase 1: PLG Readiness Check

Not every product can run PLG. Before designing the model, validate these prerequisites:

| Prerequisite | Question | Pass/Fail |
|-------------|----------|-----------|
| **Low marginal cost** | Can you serve a free user without meaningful incremental cost? | |
| **Fast time-to-value** | Can a new user experience real value in under 10 minutes? (Ideally under 5) | |
| **Self-serve capable** | Can a user sign up, onboard, and get value WITHOUT talking to a human? | |
| **Natural expansion** | Does usage naturally grow (more seats, more data, more features needed)? | |
| **Observable value** | Can the user clearly SEE the value they're getting (dashboard, output, saved time)? | |

**If 3+ fail:** PLG may not be the right primary model. Consider using PLG as an acquisition layer with a sales-assisted conversion motion instead of pure self-serve.

**If all pass:** You have a strong PLG candidate. Proceed.

### Phase 2: Define the Free-to-Paid Value Threshold

The single most important decision in freemium is: **What's free and what's paid?**

Get this wrong and you either:
- Give away too much (no reason to upgrade)
- Give away too little (users never experience enough value to want more)

#### The Value Threshold Framework

Map your product's features/capabilities into four categories:

**1. Hook Features (Always Free)**
Features that get users in the door and deliver the initial "aha moment."
- Must be genuinely useful on their own — not a crippled demo
- Should showcase the product's core capability
- Should be enough to create habit/dependency
- Ask: "What's the minimum set of features that makes someone say 'this is useful' and come back tomorrow?"

**2. Habit Features (Free with Limits)**
Features that build daily/weekly usage patterns and create switching costs.
- Free up to a usage threshold (records, queries, seats, storage, actions)
- The limit should feel natural, not punitive
- Users should hit the limit through SUCCESS, not through normal exploration
- Ask: "What limit would a successful user naturally outgrow?"

**3. Growth Features (Paid)**
Features that become valuable as the user/team scales.
- Collaboration, team management, advanced permissions
- Integrations with other tools in their stack
- Advanced analytics, reporting, export
- Automation, workflows, bulk operations
- Ask: "What do power users and teams need that individuals don't?"

**4. Enterprise Features (Premium Paid)**
Features that large organizations require.
- SSO, SAML, advanced security
- Admin controls, audit logs, compliance
- Custom integrations, API access, SLAs
- Dedicated support, implementation
- Ask: "What would a 500-person company require before their procurement team approves this?"

#### Output: Feature Gate Map

```
┌─────────────────────────────────────────────────┐
│ HOOK (Free)           │ What gets them in       │
│ • [feature]           │                         │
│ • [feature]           │                         │
├───────────────────────┤                         │
│ HABIT (Free + Limits) │ What builds dependency  │
│ • [feature] — limit   │                         │
│ • [feature] — limit   │                         │
├───────────────────────┤                         │
│ GROWTH (Paid)         │ What scales with them   │
│ • [feature]           │                         │
│ • [feature]           │                         │
├───────────────────────┤                         │
│ ENTERPRISE (Premium)  │ What big orgs need      │
│ • [feature]           │                         │
│ • [feature]           │                         │
└─────────────────────────────────────────────────┘
```

### Phase 3: Design the Activation Path

PLG lives or dies on activation — the moment a new user first experiences real value. If they never activate, they never convert.

#### Define the Activation Metric

The activation metric is NOT "signed up" or "logged in." It's the specific action that correlates with long-term retention and conversion.

Examples (well-known and less obvious):
- Slack: Sent 2,000 messages as a team
- Dropbox: Put one file in one folder on one device
- Zoom: Hosted first meeting
- Loom: Recorded and shared first video (recipient views = viral loop trigger)
- Calendly: First meeting booked by someone else using your link (the invitee becomes aware)
- Airtable: Created a base with 20+ records (data gravity kicks in)
- Miro: Invited a collaborator who made edits (team adoption = sticky)
- Typeform: Collected 10+ responses on a form (data they can't get elsewhere)
- Your product: [Define — what action, done by whom, signals they've experienced the core value?]

**Formula:** "[User type] has done [specific action] within [timeframe]"

#### Map the Activation Path

From signup to activation metric, what are the minimum steps?

```
SIGNUP → STEP 1 → STEP 2 → STEP 3 → ✅ ACTIVATED
```

For each step:
- What does the user need to do?
- What friction exists? How do we remove it?
- Can we pre-populate, automate, or skip this step?
- What happens if they stall here? (Trigger: email, in-app prompt, tooltip)

**Rules:**
- Every step you remove increases activation rate
- Pre-fill everything you can (import data, use defaults, show sample data)
- The first session matters more than anything — design it obsessively
- If activation requires more than 5 steps, you have a problem

#### Design the "Aha Moment" Sequence

The aha moment is when the user thinks: "Oh — THIS is why this exists."

It should happen BEFORE they've invested significant time. Ideally in the first session.

| Element | Description |
|---------|-------------|
| **Trigger** | What brings them to the product? (Ad, referral, search, invite) |
| **First screen** | What do they see immediately after signup? (Not a blank dashboard) |
| **Quick win** | What's the fastest path to a meaningful result? |
| **Aha moment** | What makes them say "I need this"? |
| **Hook** | What brings them back tomorrow? (Notification, incomplete task, scheduled event) |

### Phase 4: Design the Conversion Triggers

Free users become paid users when they hit a threshold where the value they'd unlock is clearly worth the price. Your job is to design those thresholds intentionally.

#### Conversion Trigger Types

**Usage-Based Triggers**
- Hit storage/record/seat limit
- Exceeded free-tier action count
- Need to process more data than free allows
- Team grew beyond free seat cap

**Feature-Based Triggers**
- Need an integration that's paid-only
- Want automation/workflows
- Need advanced reporting or export
- Require team collaboration features

**Value-Based Triggers**
- Product saved/generated measurable $ amount → "You've saved $X this month. Unlock unlimited savings for $Y/month."
- User hit a milestone → "You've managed 50 jobs. Growing businesses use [paid feature] to handle scale."

**Social Triggers**
- Colleague or team member invited them to collaborate (requires paid)
- Shared a report/output that recipients need access to view

#### Conversion Friction Audit

For each trigger, evaluate the upgrade path:

| Question | Ideal Answer |
|----------|-------------|
| How many clicks from trigger to paid? | 2 or fewer |
| Does the user have to talk to anyone? | No (self-serve checkout) |
| Is pricing clear and visible before checkout? | Yes |
| Can they start a trial of paid features before committing? | Yes |
| Is there a monthly option (lower commitment)? | Yes |
| Can they downgrade without penalty if paid isn't right? | Yes |

**Rule:** Every additional step between "I want this" and "I have this" loses a percentage of conversions. Ruthlessly minimize friction.

### Phase 5: Design the Pricing Tiers

#### Tier Architecture

Most successful PLG products use 3-4 tiers:

```
FREE          →  STARTER/PRO    →  TEAM/BUSINESS   →  ENTERPRISE
$0               $X/mo              $Y/mo               Custom
Hook + Habit     Growth features    Scale features       Everything + support
Individual       Individual/small   Teams                Organizations
Self-serve       Self-serve         Self-serve + CS      Sales-assisted
```

#### Pricing Principles for PLG

1. **Price on the value metric** — the unit that scales with customer success (seats, records, transactions, active projects, API calls). When they succeed more, they pay more. This aligns your growth with theirs.

2. **Free must be genuinely useful** — not a trial, not a demo, not crippled. A real product that real people use for real work. If free users aren't getting value, they're not future paid users — they're just server costs.

3. **The jump from free to paid should feel like a no-brainer** — If the user is getting $500/month in value from free and paid costs $49/month with 10x more capability, the upgrade is obvious. If free gives $50 of value and paid costs $49, the calculus is too close.

4. **Annual discount is your friend** — Offer 15-20% off for annual commitment. This improves cash flow, reduces churn, and locks in the relationship.

5. **Don't hide pricing** — PLG is built on transparency and self-serve. If the buyer has to "contact sales" for pricing on your Starter tier, you're not doing PLG.

#### Output: Tier Design Table

| | Free | Starter/Pro | Team/Business | Enterprise |
|---|---|---|---|---|
| **Price** | $0 | $/mo | $/mo | Custom |
| **Value metric** | Up to [X] | Up to [Y] | Up to [Z] | Unlimited |
| **Key features** | | | | |
| **Target user** | | | | |
| **Conversion path** | — | Self-serve | Self-serve | Sales |
| **Support** | Docs/community | Email | Priority | Dedicated |

### Phase 6: Retention & Expansion Design

In PLG, acquisition is only half the game. Retention and expansion revenue drive LTV.

#### Retention Levers

| Lever | How It Works |
|-------|-------------|
| **Data gravity** | The more data they store, the harder it is to leave |
| **Workflow integration** | Once embedded in daily process, switching cost is high |
| **Team adoption** | Individual tools are easy to drop; team tools have organizational inertia |
| **Historical value** | Reports, trends, history only exist in your platform |
| **Integrations** | Connected to other tools in their stack = higher switching cost |

For your product, identify which retention levers are strongest and design features that deepen them.

#### Expansion Revenue Paths

How do existing customers pay you MORE over time?

- **Seat expansion** — Team grows, adds users
- **Usage growth** — More records, projects, transactions
- **Tier upgrade** — Individual → Team → Enterprise
- **Add-ons** — Premium features, integrations, support packages
- **Cross-sell** — Other products in your portfolio

**Net Revenue Retention target:** > 110% (existing customers pay you more this year than last year, even accounting for churn)

#### Retention Benchmarks by PLG Stage

Use these benchmarks to set realistic targets and diagnose problems:

| Metric | Early (Pre-PMF) | Growth | Scale |
|--------|-----------------|--------|-------|
| Week 1 retention | 40-60% | 60-75% | 70-85% |
| Week 4 retention | 15-25% | 25-40% | 35-50% |
| Month 3 retention | 8-15% | 15-25% | 25-40% |
| Free → Paid (lifetime) | 1-3% | 3-7% | 5-10% |
| Monthly paid churn | 8-12% | 5-8% | 3-5% |
| Net Revenue Retention | 80-100% | 100-120% | 110-140% |

**How to use:** If your metrics fall below the "Early" column, the issue is likely product-market fit or activation — not pricing or packaging. Fix the product before optimizing the funnel.

### Phase 7: Metrics That Matter

Define the metrics you'll track to know if the PLG model is working:

| Metric | What It Tells You | Target |
|--------|-------------------|--------|
| **Signup → Activated (%)** | Is the first experience working? | >25% |
| **Activated → Free Active (%)** | Are activated users sticking around? | >40% weekly active |
| **Free → Paid Conversion (%)** | Is the free-to-paid threshold right? | 2-5% of free users |
| **Time to Activation** | How fast do users get value? | < 1 day |
| **Time to Paid Conversion** | How long before free users upgrade? | < 30 days |
| **Monthly Churn (paid)** | Are paid users staying? | < 5% |
| **Net Revenue Retention** | Are customers expanding? | > 110% |
| **CAC Payback Period** | How fast do you recoup acquisition cost? | < 6 months |

## Inputs Required

To execute this skill, provide:
1. **Product description** — What does it do, in plain terms?
2. **Full feature list** — Everything the product can do (we'll sort into tiers)
3. **Target user** — Who uses this day-to-day? Who buys it?
4. **Current pricing (if any)** — What you charge today
5. **Competitors and their pricing** — What alternatives exist and how they package
6. **Cost to serve** — What does a free user cost you? (Hosting, support, etc.)
7. **Growth goals** — Users? Revenue? Timeline?

## Output Format

```
# PLG Offer Design: [Product Name]

## PLG Readiness Assessment
[5-point prerequisite check with pass/fail]

## Feature Gate Map
[Features sorted into Hook / Habit / Growth / Enterprise]

## Activation Path
- Activation metric: [definition]
- Steps: [signup → activated, mapped]
- Aha moment: [what and when]
- Key friction points: [and how to remove them]

## Conversion Triggers
[Each trigger defined with type, threshold, and upgrade UX]

## Pricing Tiers
[Tier table with pricing, features, target user, conversion path]

## Retention & Expansion Strategy
- Primary retention levers: [ranked]
- Expansion paths: [defined]
- NRR target: [number]

## Key Metrics Dashboard
[Metrics table with targets]

## Risks & Assumptions
[What has to be true for this model to work]
```

## Quality Checks

- [ ] Is the free tier genuinely useful, or is it a glorified demo that will frustrate users?
- [ ] Can a user go from signup to activated in under 10 minutes?
- [ ] Is the free-to-paid threshold based on user SUCCESS (not arbitrary limits)?
- [ ] Would a user upgrading at the trigger point feel "this is worth it" or "I'm being forced"?
- [ ] Is pricing transparent and self-serve for at least the first 2 tiers?
- [ ] Are retention levers built INTO the product, not bolted on after?
- [ ] Can you actually afford to serve free users at the projected scale?
- [ ] If 10,000 users signed up for free tomorrow, could you support them?
- [ ] Did you compare retention and conversion targets against the stage-appropriate benchmarks in the Retention Benchmarks table? (Don't set Scale targets for a Pre-PMF product.)
- [ ] Did you define specific, measurable activation metrics — not vague ones like "experiences value"? (Good: "Created 2+ projects within 7 days." Bad: "Gets value from the product.")
