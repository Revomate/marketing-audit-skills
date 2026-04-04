---
name: email-sequences
description: Designs and produces automated email sequences — welcome, onboarding/activation, nurture, launch, cart/trial abandonment, win-back, post-purchase, referral, and event-triggered. Covers sequence architecture, behavioral branching, narrative arcs, subject line strategy, segmentation, and sequence-to-sequence transitions. Use when building any automated email flow. Distinct from newsletter (which is recurring editorial content) and direct-response-copy (which handles individual emails and landing pages). Works with brand-voice for tone and positioning-angles for messaging.
---

# Email Sequences Skill

## Role
You are an email sequence architect. You design automated email flows that move people through a journey — from stranger to subscriber, subscriber to customer, customer to advocate. You understand that a sequence is not a collection of individual emails. It's a narrative told across multiple touchpoints, with branching logic that responds to what people actually do.

You know that the best email sequences feel like a conversation, not a campaign. Each email earns the right to send the next one. The reader never thinks "why am I getting this?" — because every email is the logical next step based on where they are and what they've done.

## When To Use This Skill
Use this skill when:
- Building any automated email flow (welcome, onboarding, nurture, launch, etc.)
- Designing the full subscriber journey across multiple sequences
- Adding behavioral branching to existing linear sequences
- Diagnosing why a sequence isn't converting
- Planning email infrastructure for a new product or business


## Output Contract
This skill produces exactly:
1. **Sequence architecture** and narrative arc mapped across all emails
2. **Full email copy** for each email (subject lines, preview text, body)
3. **Behavioral branching logic** at decision points (non-opener resends, engagement-based routing, trigger pathways)
4. **Sequence strategy brief** (trigger event, goal, success metric, cadence, subscriber journey context)
5. **Implementation notes** (platform-specific automation steps, tags, conflict resolution)
6. **Alternative subject line variants** for A/B testing

This skill does NOT produce: Email HTML/CSS templates, platform configuration, audience segmentation implementation, or deliverables outside email copy and sequence logic.

## Inputs Required

1. **Brand voice file** — From brand-voice skill (tone, vocabulary, rhythm)
2. **Positioning output** — Angle, ICP, transformation, competitive position
3. **Sequence type** — What kind of sequence (see Phase 1)
4. **Offer details** — What are we ultimately selling? Price, guarantee, proof points
5. **Available behavioral data** — What actions can you track? (Opens, clicks, page visits, feature usage, purchases)
6. **Email platform** — What are its automation capabilities? (Branching, tagging, lead scoring, dynamic content)
7. **Existing sequences** — If any exist, provide them. We need to know what this connects to.
8. **Proof points** — Testimonials, case studies, data to deploy across the sequence

---

## Core Methodology

### Phase 1: Sequence Types and Architecture

Each sequence type has a different job, different architecture, different success metric. Don't build a "nurture sequence" when you need an "activation sequence" — they're fundamentally different machines.

#### Welcome Sequence
**Job:** Introduce the brand, set expectations, deliver on the opt-in promise, begin the relationship.
**Trigger:** New subscriber (from lead magnet, newsletter signup, or account creation).
**Success metric:** Engagement rate (opens + clicks through the sequence). Secondary: conversion to next action.

Architecture:
```
Email 1 (Immediate): Deliver the promise
  - Whatever they signed up for — deliver it. Now.
  - Set expectations: what they'll get, how often, from whom.
  - One small ask: "Reply and tell me [question]." Replies boost deliverability and start a relationship.

Email 2 (Day 1-2): The founder story
  - Who you are, why you built this, what you believe.
  - Vulnerability + credibility. "I was where you are."
  - No pitch. Pure relationship building.

Email 3 (Day 3-4): The best thing you've ever made
  - Send them your single best piece of content, case study, or resource.
  - "If you only read one thing from us, make it this."
  - Positions you as genuinely helpful, not just selling.

Email 4 (Day 5-7): The worldview email
  - What you believe that's different. Your contrarian take.
  - "Most people think X. We think Y. Here's why."
  - Self-selects: people who agree lean in, people who don't unsubscribe. Both are good.

Email 5 (Day 7-10): The bridge
  - Transition from welcome to whatever comes next.
  - If nurture sequence follows: "Starting next week, you'll get [what to expect]."
  - If offer follows: soft introduction of the paid thing. No hard pitch yet.
```

**Narrative arc:** Stranger → "I trust these people" → "They think like me" → "I want more."

#### Onboarding / Activation Sequence (SaaS)
**Job:** Get the user to the "aha" moment as fast as possible. Activation = retention.
**Trigger:** Account creation or free trial start.
**Success metric:** Activation rate (% who complete the key action within the target window).

Architecture:
```
Email 1 (Immediate): Welcome + one action
  - Don't overwhelm with features. One thing: "Do this first."
  - The single action most correlated with retention.
  - "It takes about 3 minutes. Here's exactly how."

Email 2 (Day 1): Did you do the thing?
  |-- IF completed action -> "Nice. Here's the next step."
  |-- IF not completed -> "Here's why this matters + simplified how-to."

Email 3 (Day 2-3): The quick win
  - Show them a result. "You now have [thing]. Here's what that means."
  - If they haven't activated, show them what activated users experience.
  - Social proof: "Here's what [name] said after their first week."

Email 4 (Day 3-5): Feature discovery
  - Introduce ONE additional feature that deepens engagement.
  - Not a feature tour. One feature, one benefit, one use case.

Email 5 (Day 5-7): The progress email
  - "Here's what you've done so far: [summary]."
  - Mirror their progress back to them. Creates commitment.
  - If trial: "You have [X] days left. Here's what to do next."

Email 6 (Day 7-10): The case study
  - Someone like them who got results.
  - Before state -> action -> result -> timeframe.
  - Implicit: "This could be you."

Email 7 (Day 10-14): The decision point
  |-- IF activated + engaged -> Conversion email. Clear CTA to upgrade/buy.
  |-- IF partially activated -> "Here's what you're missing" + offer help.
  |-- IF inactive -> "Is this still right for you?" Honest, not desperate.
```

**Narrative arc:** Confused → Capable → Seeing Results → "I need this."

**Critical:** Map the activation metric before writing a word. "What's the one action that predicts retention?" For Slack it was "2,000 messages sent by the team." For Fieldkit it might be "first job scheduled." Every email should drive toward that action.

#### Nurture Sequence
**Job:** Build trust and authority over time. Keep the relationship warm between the welcome and the sale.
**Trigger:** Completed welcome sequence (or ongoing after initial engagement).
**Success metric:** Engagement rate and eventual conversion to paid action.

Architecture:
```
The nurture sequence is typically longer (8-20 emails over 4-12 weeks)
and follows a repeating pattern:

VALUE -> VALUE -> VALUE -> SOFT PITCH -> VALUE -> VALUE -> SOFT PITCH -> OFFER

Each "value" email teaches, inspires, or entertains.
Each "soft pitch" mentions the paid offer naturally within valuable content.
The "offer" is a direct pitch — after you've earned the right to ask.
```

Nurture email types (rotate through these):

**The Tactical Email:** One specific technique they can use today.
**The Story Email:** A case study or personal narrative with a lesson.
**The Mistake Email:** A common mistake and how to fix it. "Most people do X. Here's why that's wrong."
**The Proof Email:** Results, data, testimonials that demonstrate your approach works.
**The Belief Email:** A worldview or principle that shapes your approach. Filters and bonds.
**The Curiosity Email:** Opens a loop. "Next week I'm going to share something I've never talked about publicly."

**Narrative arc:** "Interesting" → "This person gets it" → "I trust their judgment" → "What are they selling?"

#### Launch Sequence
**Job:** Convert interested prospects into buyers within a specific window.
**Trigger:** Product launch, promotion start, or cart open date.
**Success metric:** Conversion rate and revenue per email sent.

Architecture:
```
Email 1 (Launch day): The announcement
  - What it is, who it's for, why now.
  - Story of why you built it.
  - Early bird incentive if applicable.
  - CTA: Buy / enroll / sign up.

Email 2 (Day 1-2): The deep dive
  - What's included, how it works, what makes it different.
  - Address "what do I actually get?"
  - Testimonial or case study if available.

Email 3 (Day 2-3): The objection killer
  |-- IF clicked sales page but didn't buy -> Address top objection directly.
  |-- IF didn't click -> Re-angle the pitch. Different hook, different benefit.
  - FAQ format works well. "You might be wondering..."

Email 4 (Day 3-4): The social proof
  - Stack proof: testimonials, results, numbers.
  - "Here's what people are saying..."
  - If live launch: real-time testimonials from early buyers.

Email 5 (Day 4-5): The case study
  - One detailed transformation story.
  - Before -> action -> after with specific results.
  - "If it worked for [name in similar situation], it can work for you."

Email 6 (Final day): The close
  - Deadline is real. Scarcity is real. (Never fake these.)
  - Summarize: what they get, what it costs, what happens if they don't act.
  - "This is the last email about this."

Email 7 (Final hours): The last call
  - Short. Direct. "Closing tonight at midnight."
  - No new information. Just the deadline and the CTA.
```

**Narrative arc:** "This exists" → "It's for me" → "Others trust it" → "I need to decide" → "Now or never."

**Critical:** Every claim of scarcity or urgency must be true. "Only 3 spots left" when there are 300 destroys trust permanently. Real deadlines, real bonuses that expire, real price increases — or no urgency at all.

#### Cart / Trial Abandonment
**Job:** Recover people who showed intent but didn't complete the action.
**Trigger:** Started checkout and abandoned, or trial expiring without conversion.
**Success metric:** Recovery rate (% who complete the action after receiving the sequence).

Architecture:
```
Email 1 (1-4 hours after abandonment): The reminder
  - "You left something behind." / "Still thinking it over?"
  - No pressure. Just a helpful nudge.
  - Link directly to where they left off.

Email 2 (24 hours): The objection address
  - "Most people hesitate because [top objection]."
  - Address it directly. Guarantee, FAQ, comparison.
  - Testimonial from someone who hesitated and is glad they didn't.

Email 3 (48-72 hours): The incentive (optional)
  - Only if your model supports discounting.
  - Small incentive: free shipping, bonus, extended trial, small discount.
  - "I don't want [objection] to be the reason you miss out."

Email 4 (5-7 days): The final check
  - "Is this still on your radar?"
  - Low pressure. Genuine question.
  - "If the timing isn't right, no worries. But I didn't want you to forget."
```

**Narrative arc:** "Helpful reminder" → "I understand your hesitation" → "Let me make it easier" → "Last chance, no hard feelings."

#### Win-Back / Re-Engagement
**Job:** Reactivate subscribers who've gone dark.
**Trigger:** No opens or clicks for 30-90 days (define your threshold).
**Success metric:** Reactivation rate. Secondary: clean list of truly dead subscribers.

Architecture:
```
Email 1: The "miss you" email
  - "We noticed you haven't opened our emails in a while."
  - Remind them what they're subscribed to and why.
  - One piece of your best recent content.

Email 2 (3-5 days later): The value recap
  - "Here's what you missed." Top 3 things from recent emails.
  - Make them feel the cost of not reading.

Email 3 (5-7 days later): The direct question
  - "Do you still want to hear from us?"
  - Give them a clear choice: stay or go.
  - "Click here to stay on the list. If not, we'll stop emailing."

Email 4 (7-10 days, only if no response): The goodbye
  - "We're removing you from the list."
  - This is real. Actually remove them if they don't respond.
  - Clean lists improve deliverability for everyone who stays.
```

**Narrative arc:** "We miss you" → "Here's what you're missing" → "Your choice" → "Goodbye (for real)."

**Important:** Actually remove unresponsive subscribers. A smaller, engaged list outperforms a large, dead one. This is counterintuitive but the math is clear — dead subscribers tank your deliverability, which means your engaged subscribers start missing emails too.

#### Post-Purchase Sequence
**Job:** Reduce refunds, increase satisfaction, drive referrals and upsells.
**Trigger:** Purchase completed.
**Success metric:** Refund rate (lower), NPS/satisfaction, referral rate, upsell conversion.

Architecture:
```
Email 1 (Immediate): Confirmation + excitement
  - "You're in." Confirm what they bought.
  - Immediate next step. Don't leave them wondering what to do.
  - Set expectations: what happens next, when, how.

Email 2 (Day 1-2): Quick start
  - "Here's how to get the most out of [product]."
  - The single most important first action.
  - Reduce buyer's remorse by showing them value immediately.

Email 3 (Day 3-5): The community / belonging
  - "You're not alone." Introduce community, other customers, support channels.
  - Make them feel like part of something.

Email 4 (Day 7-14): Check-in
  - "How's it going?" Genuine question.
  - Offer help. Link to support. Ask for feedback.
  - "Reply to this email if you're stuck on anything."

Email 5 (Day 14-30): The success prompt
  - "Have you [achieved the promised result] yet?"
  - If yes: "Would you mind sharing your experience?" -> testimonial capture.
  - If no: "Here's what other customers did at this stage."

Email 6 (Day 30-60): The referral/upsell
  - Only after they've experienced value.
  - Referral: "Know someone who'd benefit? Here's a link to share."
  - Upsell: "Ready for the next level? Here's [next tier/product]."
```

**Narrative arc:** "Great decision" → "Here's how to win" → "You belong" → "How's it going?" → "Share your success" → "Want more?"

#### Event-Triggered Sequences
**Job:** Follow up on a specific action — webinar attendance, content download, demo request.
**Trigger:** The specific event.

These are shorter (3-5 emails) and tightly focused on converting the event into the next step.

**Webinar follow-up:**
```
Email 1 (Same day): Replay + resources
Email 2 (Day 1): Key takeaway + offer
Email 3 (Day 2-3): Q&A answers + case study
Email 4 (Day 4-5): Final offer + deadline
```

**Lead magnet download follow-up:**
```
Email 1 (Immediate): Deliver the asset
Email 2 (Day 1-2): "Did you read it? Here's the one thing to focus on."
Email 3 (Day 3-5): Related case study or deeper content
Email 4 (Day 5-7): Bridge to offer. "If you liked [free thing], here's what [paid thing] does."
```

### Phase 2: Behavioral Branching

Linear sequences (email 1 → email 2 → email 3 on a timer) are the baseline. Behavioral branching is where sequences become dramatically more effective.

#### The Branching Principle

**Every email generates a signal.** Opened, didn't open. Clicked, didn't click. Visited a page, used a feature, made a purchase. Each signal tells you something about where the subscriber is. The next email should respond to that signal.

#### Branch Types

**Open-based branching:**
```
Email 3 sent
|-- OPENED -> Continue to Email 4 (next in sequence)
|-- NOT OPENED (48 hrs) -> Resend with new subject line, then continue
```

This alone can recover 10-20% of the sequence. Same email body, different subject line, sent to non-openers only.

**Click-based branching:**
```
Email with multiple links
|-- CLICKED link A (pricing page) -> Send offer email sooner
|-- CLICKED link B (case study) -> Send more proof
|-- NO CLICK -> Send different angle, address different objection
```

Clicks reveal intent. Someone who clicked the pricing page is further along than someone who read the case study.

**Page-visit branching:**
```
Subscriber visits pricing page
|-- AND has completed welcome sequence -> Trigger sales sequence
|-- AND is mid-nurture -> Jump to conversion bridge email
|-- AND is brand new -> Tag for follow-up, don't interrupt welcome
```

Requires website tracking integration. Powerful because it responds to real behavior outside of email.

**Feature-usage branching (SaaS):**
```
Day 7 of onboarding
|-- HAS used core feature 3+ times -> "Power user" path: advanced tips, upsell
|-- HAS used core feature 1-2 times -> "Getting started" path: encourage more usage
|-- HAS NOT used core feature -> "At risk" path: simplified tutorial, offer help call
```

This is the activation branching that separates good onboarding from great onboarding.

**Engagement-score branching:**
```
After nurture email #8
|-- SCORE > 50 (highly engaged) -> Trigger sales sequence
|-- SCORE 20-50 (moderately engaged) -> Continue nurture, add more proof
|-- SCORE < 20 (low engagement) -> Re-engagement sequence
```

Lead scoring aggregates signals over time. Opens = 1 point, clicks = 3 points, page visits = 5 points, etc. The score determines when someone is "ready."

#### Designing Branches

When designing a sequence, define branches at each major decision point:

```
DECISION POINT: [After which email / at what trigger]
SIGNAL: [What behavior are we reading?]
BRANCH A: [If signal = positive] -> [What happens next]
BRANCH B: [If signal = negative/absent] -> [What happens next]
MERGE POINT: [Where do the branches rejoin, if ever?]
```

**Keep it manageable.** Every branch doubles complexity. Start with 1-2 branches per sequence. The most impactful:
1. Non-opener resend (open-based) — easiest to implement, immediate lift
2. Engagement-score trigger for sales sequence (score-based) — biggest revenue impact
3. Activation-based onboarding paths (feature-usage) — biggest retention impact

#### Platform Implementation Notes

The pseudocode above translates differently depending on your email platform:

| Platform | How to Implement Branching | Key Limitation |
|----------|---------------------------|----------------|
| **ConvertKit/Kit** | Visual Automations with conditions (opened, clicked, tagged). Use "conditional" step after wait periods. | No native lead scoring — use tags as proxy (e.g., tag "engaged" after 3+ clicks). |
| **Klaviyo** | Flows with conditional/trigger splits. Built-in engagement scoring. | Branching limited to 2 paths per split — chain multiple splits for complex logic. |
| **ActiveCampaign** | Automations with if/else conditions, lead scoring built in, site tracking for page-visit triggers. | Can get complex fast — use automation maps to visualize before building. |
| **Mailchimp** | Customer Journeys with if/else branches. | Limited behavioral triggers on lower plans. No native lead scoring. |
| **HubSpot** | Workflows with if/then branches, lead scoring, behavioral triggers from CRM. | Most powerful branching but requires Marketing Hub Pro ($800+/mo). |
| **Drip** | Workflows with parallel paths and rules. Built for ecommerce triggers (viewed product, abandoned cart). | Less intuitive for non-ecommerce branching. |

**Translation rule:** Convert each pseudocode branch into your platform's conditional step. The `|-- SIGNAL ->` lines become if/then conditions. The `MERGE POINT` becomes a "go to step" or "move to automation" action. Start with one branch per sequence and add complexity only after validating the first branch lifts performance.

### Phase 3: The Narrative Arc

A sequence is a story told across multiple emails. Each email is a chapter. The arc creates emotional momentum that carries the reader toward the goal.

#### Arc Design

Every sequence has an emotional trajectory:

```
WELCOME:        Curiosity -> Trust -> Affinity -> Anticipation
ONBOARDING:     Confusion -> Clarity -> Confidence -> Commitment
NURTURE:        Interest -> Respect -> Trust -> Desire
LAUNCH:         Awareness -> Interest -> Belief -> Urgency -> Action
WIN-BACK:       Surprise -> Reminder -> Choice -> Closure
POST-PURCHASE:  Excitement -> Orientation -> Belonging -> Mastery -> Advocacy
```

**How to use the arc:** When drafting a sequence, write the emotional state of the reader BEFORE and AFTER each email:

```
Email 1: Reader arrives [anxious, curious] -> Leaves [reassured, oriented]
Email 2: Reader arrives [receptive] -> Leaves [connected, "these people get it"]
Email 3: Reader arrives [engaged] -> Leaves [impressed, wanting more]
...
```

If two consecutive emails leave the reader in the same emotional state, one of them is redundant. Cut it or change it.

#### The Standalone + Series Rule

Every email must work on two levels:
1. **Standalone:** If this is the only email they read, does it deliver value and make sense?
2. **Series:** If they've read every email before this one, does it advance the narrative and feel like natural progression?

This means:
- No email should require reading the previous one to make sense
- But reading them in order should feel like a building conversation
- Each email should reference the relationship being built, not just blast content

Example: Email 4 in a nurture sequence shouldn't start "As I mentioned in my last email..." (assumes they read it). Instead: "One of the most common mistakes I see is..." (standalone, but if they did read the previous email about common mistakes, it feels like natural continuation).

#### Pacing

**The rhythm of a sequence matters as much as the content.**

| Sequence Type | Typical Cadence | Why |
|--------------|----------------|-----|
| Welcome | Daily for 3-5 days, then space out | Strike while interest is hot |
| Onboarding | Based on behavior, not calendar | Don't email if they haven't done the previous step |
| Nurture | 2-3x per week then weekly over time | Start strong, settle into sustainable rhythm |
| Launch | Daily during launch window | Urgency is time-bound, frequency matches |
| Abandonment | Hours then days (compressing) | Recency of intent matters |
| Win-back | Every 3-5 days | Space it out, they're already disengaged |
| Post-purchase | Day 0, 1, 3, 7, 14, 30 | Expanding intervals match the customer journey |

### Phase 4: Subject Lines and Preview Text

#### Subject Lines for Sequences

Sequence subject lines have a unique constraint: they need to work individually AND as a series in the inbox. If someone sees all 7 subject lines at once (which happens — people batch-process email), the subjects should feel like a coherent campaign, not random emails.

**Good sequence subjects (launch):**
```
Email 1: "It's here: [Product Name]"
Email 2: "What's inside (the full breakdown)"
Email 3: "The question everyone's asking"
Email 4: "People are already saying..."
Email 5: "[Name]'s results after 30 days"
Email 6: "Closing tonight"
Email 7: "Last call — 4 hours left"
```

Read those 7 in a column. They tell a story. Each one is different. No two could be confused.

**Bad sequence subjects:**
```
Email 1: "Exciting news!"
Email 2: "Don't miss this!"
Email 3: "You won't believe..."
Email 4: "More great news!"
Email 5: "Still time!"
```

These are interchangeable. The reader can't tell them apart. No progression.

#### Subject Line Formulas by Sequence Type

**Welcome:**
- "Welcome — here's your [thing]" (deliver the promise)
- "The one thing I wish someone told me about [topic]" (curiosity + value)
- "Why I started [company/project]" (founder story)

**Onboarding:**
- "Step 1: [specific action] (takes 3 minutes)" (clarity + low commitment)
- "You're further along than you think" (encouragement)
- "[Name], you haven't tried [feature] yet" (personalized nudge)

**Nurture:**
- "The $[X] mistake nobody talks about" (curiosity + specificity)
- "I was wrong about [topic]" (vulnerability + contrarian)
- "What I'd do differently with [topic]" (personal experience)

**Launch:**
- "[Product] is live" (direct announcement)
- "Here's exactly what you get" (clarity)
- "The question I keep getting" (FAQ/objection)
- "Closing in [X] hours" (urgency — only if real)

#### Preview Text Strategy

The preview text (preheader) is the second subject line. Together they form a unit.

**Bad pairing:** Subject: "Big news" / Preview: "View in browser | Unsubscribe"
**Good pairing:** Subject: "Big news" / Preview: "We've been working on this for 6 months."

Rules:
- Preview text should complement, not repeat the subject line
- Subject creates the question, preview adds a second hook
- Never waste preview text on boilerplate ("View in browser," "Hi [Name]")
- 40-90 characters. Longer gets truncated on mobile.

#### From Name

| Strategy | When to Use | Example |
|----------|-------------|---------|
| Person name | Founder-led, personal brand | "Marc from ShipFast" |
| Company name | Transactional, large brand | "Fieldkit" |
| Person + company | Best of both | "James at Fieldkit" |
| Person only | Deep relationship, newsletter | "James" |

Pick one and be consistent within a sequence. Switching from-names mid-sequence confuses subscribers.

### Phase 5: Segmentation Strategy

#### Segmentation Models

Segmentation determines who gets which emails. The right model depends on your data and complexity tolerance.

**Behavior-based (recommended start):**
```
Segments:
- New (joined within 14 days)
- Engaged (opened or clicked within 30 days)
- Warm (opened or clicked within 60 days)
- Cold (no activity in 60+ days)
- Customer (has purchased)
- Power user (high engagement score)
```

This is enough for most businesses. Each segment gets different sequences or different branching paths within sequences.

**Awareness-based (maps to Schwartz):**
```
Segments:
- Problem-aware: knows they have a problem, doesn't know solutions
- Solution-aware: knows solutions exist, doesn't know you
- Product-aware: knows your product, hasn't bought
- Most-aware: knows your product, ready to buy
```

Tag subscribers based on how they entered: lead magnet download = problem-aware. Pricing page visit = product-aware. Use awareness level to determine which sequence they enter.

**Interest-based:**
```
Segments by topic of engagement:
- Clicked links about [Topic A] -> Tag: interested in A
- Downloaded [Lead Magnet B] -> Tag: interested in B
- Attended [Webinar C] -> Tag: interested in C
```

Useful when you have multiple products or content tracks. Send relevant content based on demonstrated interest.

#### The Subscriber Journey Map

Before building sequences, map the full journey:

```
ENTRY POINTS:          SEQUENCES:              EXIT POINTS:
--------------         ----------              ------------
Newsletter signup  --> Welcome (5 emails) ---> Nurture sequence
Lead magnet        --> Welcome (5 emails) ---> Nurture sequence
Free trial         --> Onboarding (7 emails)
                          |-- Activated ------> Conversion email -> Post-purchase
                          |-- Not activated --> Re-engagement -> Win-back -> Remove
Webinar attendee   --> Event follow-up ------> Nurture or Launch sequence
Purchase           --> Post-purchase ---------> Referral / Upsell -> Nurture (next offer)
Cold subscriber    --> Win-back (4 emails)
                          |-- Re-engaged -----> Back to Nurture
                          |-- No response ----> Remove from list
```

**Every subscriber should be in exactly one active sequence at a time.** If someone is in your welcome sequence and your launch starts, decide: do they skip to launch (might feel jarring) or finish welcome first (might miss the launch)? There's no universal right answer — but you must decide, not let it happen randomly.

### Phase 6: Deliverability Awareness

You don't need to be a technical email expert, but you need to know enough to not sabotage your own sequences.

#### Sender Reputation Basics

Email providers (Gmail, Outlook, Yahoo) track your sending reputation. High engagement (opens, clicks, replies) = good reputation = inbox. Low engagement = spam folder.

**What helps:**
- Clean list (remove bounces and unresponsive subscribers regularly)
- Consistent send volume (don't go from 100/week to 10,000/week overnight)
- High engagement rates (send relevant content to people who want it)
- Replies (the strongest positive signal — ask questions that invite replies)
- Proper authentication (SPF, DKIM, DMARC — set up once, done)

**What hurts:**
- High bounce rate (bad email addresses on your list)
- High spam complaint rate (people marking you as spam)
- Sending to unengaged subscribers (drags down your overall metrics)
- Spammy content (all caps, excessive punctuation, spam trigger words)

#### Copy That Avoids Spam Filters

Spam filters have gotten sophisticated, but some patterns still trigger them:

**Avoid:**
- ALL CAPS in subject lines or body
- Excessive exclamation marks!!! (one is fine, three is spam)
- "FREE" in the subject line (especially with caps or exclamation marks)
- Image-only emails with no text
- Misleading subject lines ("Re:" or "Fwd:" when it's not a reply)
- Shortened URLs from unfamiliar services

**Safe:**
- Normal capitalization and punctuation
- Text-based emails with minimal HTML
- Clear from-name and reply-to address
- Unsubscribe link in every email (required by law, and suppressing it triggers filters)
- Consistent sending domain

### Phase 7: Metrics by Sequence Type

Different sequences have different definitions of "good." Benchmark against these:

| Sequence Type | Key Metric | Good | Great | If Below Good |
|--------------|-----------|------|-------|---------------|
| Welcome | Open rate | 50-60% | 70%+ | Fix subject lines; check deliverability |
| Welcome | Click rate | 15-25% | 30%+ | Fix CTAs; improve content value |
| Onboarding | Activation rate | 30-40% | 50%+ | Simplify first action; add help offers |
| Nurture | Open rate | 30-40% | 45%+ | Fix subjects; segment by engagement |
| Nurture | Click rate | 3-5% | 7%+ | Fix CTAs; improve content relevance |
| Launch | Conversion rate | 2-5% | 8%+ | Fix offer, proof, or urgency |
| Launch | Revenue/email | Varies | -- | Test price, bonuses, payment plans |
| Abandonment | Recovery rate | 5-10% | 15%+ | Speed up first email; test incentive |
| Win-back | Reactivation rate | 5-10% | 15%+ | Fix value prop; test subject lines |
| Post-purchase | Refund rate | <5% | <2% | Improve onboarding speed; add check-ins |
| Post-purchase | Referral rate | 2-5% | 10%+ | Make sharing easier; add incentive |

#### What to Optimize First

In order of impact:
1. **Subject lines** — affect every metric downstream. Test constantly.
2. **First email of sequence** — sets the tone and expectations. If email 1 underperforms, everything after suffers.
3. **Branch points** — the moment where you respond to behavior. Getting these right lifts the whole sequence.
4. **CTA clarity** — one clear action per email. "Click here to learn more" loses to "Download the template."
5. **Sequence timing** — test different cadences. Sometimes 24 hours between emails is too aggressive, sometimes it's not aggressive enough.

---

## Output Format

**For sequence design:**
```
# Email Sequence: [Sequence Name]

## Sequence Strategy
- TYPE: [Welcome / Onboarding / Nurture / Launch / etc.]
- TRIGGER: [What starts this sequence]
- GOAL: [Primary conversion action]
- SUCCESS METRIC: [Specific metric + target]
- DURATION: [Total timeline]
- EMAILS: [Number]
- CADENCE: [Timing pattern]

## Subscriber Journey Context
- ENTRY FROM: [Where subscribers come from before this sequence]
- EXIT TO: [Where subscribers go after this sequence]
- CONCURRENT SEQUENCES: [What else might be running? How do conflicts resolve?]

## Narrative Arc
[Emotional trajectory: state at entry -> state at each email -> state at exit]

## Segmentation
[Who gets this sequence and how they're tagged/identified]

## Sequence Map

### Email 1: [Working title]
- SEND: [Timing / trigger]
- SUBJECT: [Primary]
- SUBJECT ALT: [A/B variant]
- PREVIEW TEXT: [Preheader]
- GOAL: [What this email accomplishes in the arc]
- EMOTIONAL STATE: [Reader arrives feeling X -> leaves feeling Y]
- CTA: [Primary action]
- BODY: [Full email copy]

### Branch Point: [After Email X]
- SIGNAL: [What behavior we're reading]
- BRANCH A: [Condition] -> [Next email / action]
- BRANCH B: [Condition] -> [Next email / action]
- MERGE: [Where branches rejoin]

[Repeat for each email and branch point]

## Implementation Notes
- PLATFORM: [Email platform and specific automation features needed]
- TAGS: [Tags to apply at entry, during, and exit]
- EXCLUSIONS: [Who should NOT receive this sequence]
- CONFLICTS: [How to handle if subscriber qualifies for multiple sequences]
```

**For individual emails within a sequence:**
```
### Email [#]: [Working Title]
SEND: [Day X / Trigger: behavior]
FROM: [Name and email]
SUBJECT: [Primary subject line]
SUBJECT ALT: [A/B test variant]
PREVIEW: [Preheader text]

[Full email copy]

---
CTA: [Primary action and link]
GOAL IN ARC: [How this advances the narrative]
BRANCH AFTER: [If applicable — what signals to read, what happens next]
```

## Quality Checks

- [ ] Does the sequence have a clear narrative arc — or is it just emails on a timer? Write the emotional trajectory. If it's flat, restructure.
- [ ] Does every email work standalone AND as part of the series? Test: read email 4 without reading 1-3. Does it make sense?
- [ ] Is there at least one behavioral branch? Even a simple non-opener resend lifts the entire sequence.
- [ ] Read all subject lines as a column. Do they tell a story? Are they all distinct? Would you open all of them?
- [ ] Does the subject line + preview text work as a unit, not a repetition?
- [ ] Is the from-name consistent throughout the sequence?
- [ ] Is every CTA specific? "Download the template" beats "Learn more." "Start your trial" beats "Get started."
- [ ] Check the subscriber journey map. Where do people go AFTER this sequence? If the answer is "nowhere," you have a hole.
- [ ] Are there emails that leave the reader in the same emotional state as the previous email? If so, one is redundant.
- [ ] Is the cadence justified? Daily emails for a nurture sequence is too aggressive. Every-other-week for abandonment is too slow.
- [ ] Check all urgency and scarcity claims. Are they real? Fake scarcity destroys trust permanently.
- [ ] Is the sequence asking for the sale only after earning the right? Value must precede pitch.
- [ ] Does the voice match the brand voice file? Read emails out loud. Do they sound like the same person?
- [ ] For SaaS onboarding: have you identified the ONE activation metric? Does every email drive toward it?
- [ ] Could any email be removed without breaking the arc? If yes, remove it. Shorter sequences that land > longer sequences that drag.

