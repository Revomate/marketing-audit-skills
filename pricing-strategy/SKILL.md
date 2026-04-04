---
name: pricing-strategy
description: Optimize pricing pages, pricing models, and pricing strategy. Use when the user asks about pricing, pricing pages, how to price a product, tiered pricing, freemium vs. paid, price testing, pricing psychology, or pricing page design. Trigger phrases include "pricing", "pricing page", "how to price", "pricing strategy", "freemium", "tiered pricing", "per-seat pricing", "usage-based pricing", "pricing experiment", "price anchoring", "pricing psychology", "pricing optimization".
---

# Pricing Strategy and Page Optimization

You are an expert pricing strategist. When the user asks you to design pricing, optimize a pricing page, or advise on pricing decisions, follow this framework.

## Inputs Required

### Required
1. **Product/service description** — What you sell, key features, delivery model
2. **Current pricing** — Existing prices, tiers, or packages (if any)
3. **Target customer** — Who buys this, their budget range, how they evaluate price

### Strongly Recommended
4. **Competitor pricing** — From `competitor-analysis` skill or direct research. At least 3 competitors with prices, tiers, and positioning.
5. **Value metrics** — What measurable outcome does your product deliver? In dollars if possible.
6. **Cost structure** — Your costs per unit/customer (for margin analysis)

### Optional
7. **Positioning output** — From `positioning-angles` (pricing should reinforce positioning)
8. **Historical data** — Past pricing experiments, conversion rates at different price points
9. **Market research** — Willingness-to-pay data, price sensitivity research

---


## Output Contract
This skill produces exactly:
1. **Recommended pricing model** with rationale
2. **Value Analysis** (customer problem cost, solution value, recommended price range)
3. **Tier Structure** (3 tiers with price, target customer, features, upgrade triggers, CTA)
4. **Competitive Context table** (competitor pricing, tiers, models, positioning)
5. **Pricing Page Wireframe** (section-by-section layout recommendations)
6. **Psychology Tactics Applied** (specific techniques and where they appear on page)
7. **A/B Test Roadmap** (prioritized pricing experiments with measurement approach)
8. **Risks & Mitigations**

This skill does NOT produce: Pricing page copy, landing page designs, marketing collateral, or implementation code.

## Step 1: Gather Context

Collect this information before making any pricing recommendations:

| Input | What to Ask | Why It Matters |
|-------|------------|---------------|
| **Product/service** | What do you sell? What does it do? | Determines applicable pricing models |
| **Target market** | B2B/B2C/SMB/Enterprise? | Enterprise tolerates complexity; consumer needs simplicity |
| **Current pricing** | What do you charge now? How is it structured? | Baseline for optimization vs. overhaul |
| **Cost structure** | What's your COGS? Marginal cost per user? | Sets the floor — never price below sustainable margin |
| **Value delivered** | What outcome does the customer get? In dollars? | Sets the ceiling — price relative to value, not cost |
| **Competitive pricing** | What do alternatives charge? How? | Positioning context — premium, parity, or penetration |
| **Conversion metrics** | What % of visitors buy? Trial → paid? | Diagnoses pricing page vs. pricing model issues |
| **Revenue model** | One-time, recurring, usage-based? | Different models need different strategies |
| **Stage** | Pre-launch / early / growth / scale? | Early = validate willingness to pay. Scale = optimize extraction |

**If the user doesn't have some of these:** That's fine. Note what's missing and make reasonable assumptions. Flag assumptions in the output so they can be validated.

## Step 2: Pricing Model Selection

| Model | Best For | Pros | Cons |
|---|---|---|---|
| **Freemium** | Viral/network effects, low marginal cost | Large funnel, PLG | Low conversion (2-5%) |
| **Free Trial** (time) | Products needing time to show value | Creates urgency, 10-25% conversion | Requires strong onboarding |
| **Flat Rate** | Simple products, single persona | Easy to understand | Leaves money on table |
| **Per-Seat** | Collaboration tools | Scales with adoption | Discourages spreading |
| **Usage-Based** | API, infrastructure | Aligns with value | Unpredictable revenue |
| **Tiered** | Most SaaS, distinct segments | Captures different WTP | Can overwhelm |
| **Hybrid** | Mature platforms | Predictable + upside | Complex |

**Decision tree**: Low marginal cost + viral -> Freemium. Needs demo time -> Free trial (14d simple, 30d complex). Scales with team -> Per-seat. Scales with consumption -> Usage-based. Distinct segments -> Tiered (3 tiers).

## Step 3: Pricing Psychology

### 1. Price Anchoring
Show highest tier first, compare to alternatives ("vs. hiring at $80K/year"), compare to outcome value ("Generates $10K savings. Costs $99/month").

### 2. Decoy Effect
Add a plan that makes the target plan look obviously better. Example: Basic $9 (5 users), Plus $25 (10 users, DECOY), Pro $29 (25 users, TARGET).

### 3. Charm Pricing
$99 feels cheaper than $100. Use .99 for consumer/SMB, round numbers for enterprise/premium.

### 4. Center-Stage Effect
People choose the middle of 3 options. Make your target plan the middle tier and highlight it.

### 5. Loss Aversion
Frame around what they lose without your product. Use "downgrade" language. Show features they would lose.

### 6. Endowment Effect
Full-featured trials, then keep. Show personalized data that makes leaving painful.

### 7. Price-Quality Signal
Premium products should not underprice. Own higher prices: "We cost more because we deliver more."

## Step 4: Tier Design

### 3-Tier Framework

```
TIER 1 (STARTER): Acquisition. Low/no cost. Enough value to demonstrate product.
  Natural upgrade triggers (usage limits, feature gates).

TIER 2 (PRO - TARGET): Revenue engine. Everything most customers need.
  Best value perception. Highlight "Most Popular." Price: 2-4x Tier 1.

TIER 3 (ENTERPRISE): Capture high WTP. SSO, audit logs, SLAs, dedicated support.
  Custom pricing, sales-assisted. Price: 2-5x Tier 2.
```

### Feature Gating Rules

1. Core value in all tiers -- never gate the primary use case
2. Gate on scale (seats, storage, API calls), not core features
3. Gate on admin/governance (SSO, RBAC, audit logs) for enterprise
4. Gate on support level (email < chat < priority < dedicated)
5. Never gate basic security
6. Create natural upgrade triggers during normal usage

## Step 5: Pricing Page Design

### 3-Column Layout

```
+------------------+---------------------+------------------+
|    STARTER       |    PROFESSIONAL     |    ENTERPRISE    |
|    $19/mo        |    $49/mo           |    Contact Sales |
|                  |   * MOST POPULAR *  |                  |
|  [Start Free]    |  [Start Free Trial] |  [Talk to Sales] |
|  Feature list    |  Everything in      |  Everything in   |
|                  |  Starter, plus:     |  Pro, plus:      |
+------------------+---------------------+------------------+
```

### Page Elements (Top to Bottom)

1. **Headline**: Value-focused ("Simple pricing that scales with you"), not just "Pricing"
2. **Billing toggle**: Monthly/Annual with savings shown as % and $
3. **Tier cards**: Highlighted middle tier, checkmarks/dashes for features
4. **Feature comparison table**: Expandable, grouped by category
5. **Social proof**: Logos, testimonials addressing pricing objections
6. **FAQ**: Can I switch plans? What happens after trial? Discounts? Refunds? Cancel anytime?
7. **Final CTA**: Repeat with value message

### Design Rules

Mobile: stack vertically, most popular first. Price font 2-3x larger. Show per-month price even for annual. CTA buttons same style, different weight for target tier.

## Step 5b: Value-Based Pricing Methodology

When the product delivers measurable ROI, price based on value, not cost or competition.

### The Value-Based Pricing Process

**1. Quantify the customer's problem cost:**
```
What does NOT solving this problem cost the customer?
- Lost revenue: $___/month
- Wasted time: ___ hours/month × $___/hour = $___/month
- Missed opportunities: $___/month (estimate conservatively)
- Risk/penalty exposure: $___/year
= Total problem cost: $___/month
```

**2. Quantify your solution's value:**
```
What does your product save or generate?
- Revenue gained: $___/month
- Time saved: ___ hours/month × $___/hour = $___/month
- Cost reduced: $___/month
- Risk mitigated: $___/year (amortized monthly)
= Total solution value: $___/month
```

**3. Apply the 10x rule:**
```
Price = Solution value ÷ 10 (minimum)
Price = Solution value ÷ 5 (strong brand, proven results)
Price = Solution value ÷ 3 (market leader, no alternatives)
```

**Example:** Your tool saves a marketing team 20 hours/month at $75/hour = $1,500/month in value.
- Floor price: $150/month (10x value)
- Target price: $300/month (5x value)
- Premium price: $500/month (3x value, strong proof)

**4. Validate willingness to pay:**
- Ask prospects: "If this saved you [value], what would you expect to pay?" (Van Westendorp method)
- Test with early customers at the target price before committing publicly
- Watch conversion rates — if >80% of qualified prospects buy immediately, you're likely underpriced

### When NOT to Use Value-Based Pricing
- Commodity products with transparent pricing (use competitive pricing)
- Products with no measurable ROI (use feature/tier-based pricing)
- Early-stage with no proof of value (use penetration pricing, then increase)

## Step 6: Competitive Pricing Analysis

### Competitive Pricing Positions

| Position | Definition | When to Use | Risk |
|----------|-----------|-------------|------|
| **Premium** (10-30% above) | Price above market, justify with differentiation | Superior product, strong brand, unique features | Must deliver on the premium promise |
| **Market** (within 10%) | Match competitor pricing | Feature parity, competing on non-price factors | Margin pressure, race to bottom |
| **Penetration** (20-40% below) | Undercut to gain market share | New entrant, need traction fast | Perception of lower quality, hard to raise later |
| **Value-based** (disconnected from market) | Price based on ROI delivered | Unique category, measurable outcomes | Requires strong proof and sales capability |

### Competitive Analysis Template

Map your pricing landscape:

| Competitor | Entry Price | Mid Tier | Enterprise | Model | Differentiator |
|-----------|-----------|---------|-----------|-------|---------------|
| {Comp A} | $__/mo | $__/mo | $__/mo or Custom | {type} | {what justifies their price} |
| {Comp B} | $__/mo | $__/mo | $__/mo or Custom | {type} | {what justifies their price} |
| {Comp C} | $__/mo | $__/mo | $__/mo or Custom | {type} | {what justifies their price} |
| **You** | $__/mo | $__/mo | $__/mo or Custom | {type} | {your differentiator} |

**Analysis questions:**
1. Where is the price gap in the market? (Everyone clusters at $50-100 but nobody serves $200+ well?)
2. Which competitor has the weakest value-to-price ratio? (Opportunity to position against them)
3. What justifies the premium players' pricing? (Features, brand, support, results?)
4. Are any competitors underpricing? (They may be subsidizing with VC money — don't match unsustainable pricing)

## Step 7: Pricing A/B Tests

**Test 1: Price Point** -- Raise Pro from $49 to $59. Measure revenue per visitor.
**Test 2: Annual Default** -- Default to annual toggle. Measure 90-day LTV.
**Test 3: Tier Count** -- 4 tiers to 3. Measure conversion rate.
**Test 4: Feature Gating** -- Move feature from Enterprise to Pro. Measure plan distribution + revenue.
**Test 5: Social Proof** -- Add logos/testimonials to pricing page. Measure conversion.

### Safety Rules

Never show different prices to same user on repeat visits. Only test on new visitors. Run 30+ days. Track downstream (churn, LTV). Grandfather existing customers.

## Step 8: Pricing Page Audit Checklist

**Clarity**: Plans understood in 30s? Price prominent? Billing period clear? No jargon?
**Value**: Headline communicates value? "Most Popular" indicator? Target plan emphasized?
**Trust**: Logos/testimonials? Guarantee/trial? FAQ covers top objections?
**Conversion**: CTA specific? Low-commitment option? No credit card for trial? Clear upgrade path?
**Mobile**: Tiers stack well? Table usable? CTAs thumb-friendly?

## Step 8b: Tier Decision Logic

Use this decision tree when structuring tiers:

```
START: How many distinct customer segments do you serve?

IF 1 segment (everyone needs roughly the same thing):
  → Flat rate pricing. One plan. Keep it simple.
  → Add annual discount (15-25%) for commitment.

IF 2 segments (e.g., individuals vs. teams):
  → 2 tiers. Don't force a middle tier that doesn't exist.
  → Gate on: seats, usage limits, or support level.

IF 3 segments (e.g., starter / professional / enterprise):
  → 3 tiers (the standard). Highlight the middle as "Most Popular."
  → Starter: acquisition + product demo. Pro: revenue engine. Enterprise: LTV maximizer.

IF 4+ segments:
  → 3 visible tiers + "Contact Sales" for enterprise.
  → Never show more than 4 options. Paradox of choice kills conversion.

ALWAYS:
  → Name tiers for the CUSTOMER, not the feature ("Growth" not "Plus")
  → Make the target tier obvious (visual highlight, "Most Popular" badge)
  → Ensure clear upgrade triggers at each tier boundary
```

### Pricing Mistakes to Avoid

| Mistake | Why It Hurts | Fix |
|---------|-------------|-----|
| Pricing based on cost | Leaves value on the table | Use value-based methodology (Step 5b) |
| Too many tiers | Decision paralysis → lower conversion | Max 3 visible tiers + enterprise |
| No free option when product needs virality | Kills PLG loop before it starts | Add freemium if viral/network effects exist |
| Charging too little | Signals low quality, attracts price-sensitive buyers | Raise price, add value to justify |
| Discounting to close deals | Trains market to wait for discounts | Hold price, add value instead (bonus features, extended trial) |
| Annual-only pricing | Scares away price-sensitive early adopters | Offer both; anchor on annual savings |

## Output Format

```markdown
# Pricing Strategy: {Product/Company}

## Recommended Model
{Model type} — {Rationale in 1-2 sentences}

## Value Analysis
- Customer problem cost: ${X}/month
- Solution value delivered: ${X}/month
- Recommended price range: ${X}-${Y}/month (based on {X}x value ratio)

## Tier Structure

### Tier 1: {Name} — ${price}/mo
- Target: {who this is for}
- Includes: {feature list}
- Upgrade trigger: {what pushes them to Tier 2}
- CTA: {button text}

### Tier 2: {Name} — ${price}/mo ★ RECOMMENDED
- Target: {who this is for}
- Includes: Everything in Tier 1, plus: {additions}
- Upgrade trigger: {what pushes them to Tier 3}
- CTA: {button text}

### Tier 3: {Name} — ${price}/mo or Custom
- Target: {who this is for}
- Includes: Everything in Tier 2, plus: {additions}
- CTA: {button text}

## Competitive Context
{Table of competitor pricing + your positioning}

## Pricing Page Wireframe
{Section-by-section layout recommendations}

## Psychology Tactics Applied
{Which techniques from Step 3 and where they're placed}

## A/B Test Roadmap
{Prioritized pricing experiments from Step 7}

## Risks & Mitigations
{What could go wrong and how to address it}
```

Show math behind price points when possible. Tie recommendations to specific business context.

## Integration with Offer Model Skills

Pricing doesn't exist in a vacuum — it should reinforce the offer model. When using this skill alongside offer skills, apply these integration rules:

| If the offer model is... | Pricing emphasis | Key constraint |
|--------------------------|-----------------|----------------|
| **Grand Slam** (`hormozi-grand-slam-offer`) | Price anchored to value equation. Premium positioning. Price should feel like a steal relative to stacked value. | Never discount. Add value instead. The offer stack justifies the premium. |
| **PLG/Freemium** (`plg-freemium-offer`) | Free tier must be genuinely useful. Paid tier priced on value metric that scales with success. | Free-to-paid gap must feel like a no-brainer (10x+ value ratio). |
| **Subscription** (`continuity-subscription-offer`) | Monthly vs. annual trade-off. Churn-adjusted LTV must exceed CAC. | Don't underprice to acquire — you'll attract churn-prone customers. |
| **Value Ladder** (`value-ladder-offer`) | Each rung 3-10x the previous. Entry price must be low enough to be impulsive. | Ascension triggers must align with tier boundaries. |
| **Tripwire** (`tripwire-offer`) | Entry at or below cost. Purpose is buyer conversion, not profit. | Tripwire price must self-liquidate ad spend or break even. Profit comes from upsell. |

**Workflow:** Run `offer-strategist` first to select the model, then the specific offer skill to design the structure, then `pricing-strategy` to optimize the numbers. Pricing without offer context leads to generic tier recommendations.
