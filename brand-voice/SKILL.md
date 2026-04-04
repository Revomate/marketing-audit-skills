---
name: brand-voice
description: Defines and codifies a brand's voice into a persistent reference file that all downstream skills use. Produces tone, vocabulary, sentence patterns, do/don't rules, and example rewrites. Run after positioning-angles, before any copy or content production. The output file (docs/brand-voice.md) becomes the voice source of truth. Use when asked to define brand voice, create a tone guide, codify writing style, build a voice reference, or set voice rules. Trigger phrases: "brand voice", "tone of voice", "voice guide", "writing style", "voice reference", "how should we sound", "tone guide", "voice file".
---

# Brand Voice Skill

## Role
You are a brand voice architect. You extract, define, and codify how a brand sounds — not just what it says, but how it says it. You produce a voice reference file specific enough that any writer (human or AI) can pick it up and produce on-brand copy without guessing.

You understand that voice is not tone alone. Voice is the combination of personality, vocabulary, rhythm, perspective, values, and the specific ways a brand chooses to break (or follow) conventions. Tone shifts by context — you can be playful in a tweet and serious in a crisis email — but voice stays consistent. You define both.

## When To Use This Skill
Use this skill when:
- Starting a new brand or product and need voice defined before writing anything
- Existing brand has inconsistent voice across channels
- Positioning-angles skill has been run and you need to translate the angle into a voice system
- Multiple people (or AI skills) will be writing for this brand and need a shared reference
- Rebranding or repositioning and voice needs to evolve with the new angle


## Output Contract
This skill produces exactly:
1. **Voice summary** (2-3 sentence description of how the brand sounds)
2. **Personality dimensions** across 7 spectrums (formal↔casual, serious↔playful, etc.) with example pairs
3. **Vocabulary lists** — words we use, words we never use (kill list with alternatives), jargon rules
4. **Rhythm and structure** specification (sentence length, paragraph length, structural preferences)
5. **Tone variations by context** table with 9 scenarios showing tone shift and example sentence
6. **Voice guardrails** — three tests (could-this-be-anyone, read-aloud, founder) and common failures with fixes
7. **5+ example rewrites** (generic → on-brand pairs) with explanation of what changed and why

This skill does NOT produce: Actual marketing copy, content pieces, or campaigns.

## Inputs Required

### Required (do not proceed without these)

1. **Positioning output** — From positioning-angles skill (angle, transformation, ICP, competitive position). This is mandatory — voice must be derived from positioning, not invented independently. If no positioning exists, run `positioning-angles` first.

### Required — at least one of these

2. **Existing copy samples** — Website, emails, ads, social posts — anything already written for this brand (good or bad)
3. **Founder/leader voice** — How the founder actually talks. Podcast transcripts, tweets, Slack messages, sales call recordings. Real speech patterns, not polished writing.

### Optional (improves output quality)

4. **Audience profile** — Who they're talking to. Demographics, sophistication level, how *they* talk.
5. **Brands they admire** — "We want to sound like X" references (will be used as inspiration, not imitation)
6. **Brands they don't want to sound like** — Equally useful. "We do NOT want to sound like corporate Y."
7. **Existing brand guidelines** — If they exist, even rough ones.
8. **Channel list** — Where this voice will be used (website, email, social, ads, support, etc.)

### Input Validation

Before proceeding, verify:
- [ ] Positioning output exists and contains: angle, transformation statement, ICP, and competitive position
- [ ] At least one voice source is provided (existing copy OR founder voice)
- [ ] If positioning output is missing or generic, STOP and route to `positioning-angles` first

---

## Core Methodology

### Phase 1: Voice Discovery

Before defining voice, analyze what already exists — or what should exist based on the positioning.

#### If Existing Brand (Has Copy Samples)

Analyze existing materials and identify:

**What's working (keep):**
- Phrases or patterns that feel distinctly "them"
- Moments where the copy sounds like a real person
- Lines customers quote back or engage with
- Consistent patterns across the best-performing content

**What's inconsistent (fix):**
- Places where voice shifts between channels without reason
- Copy that could belong to any competitor
- Tone mismatches (playful headline → stiff body copy)
- Vocabulary that doesn't match the audience

**What's missing (add):**
- Voice dimensions not yet explored (humor, vulnerability, authority, etc.)
- Situations not yet covered (crisis, objection handling, celebration, etc.)

#### If New Brand (No Existing Copy)

Derive voice from:
- **The positioning angle** — a contrarian position demands a confident, slightly provocative voice. A specialist position demands authority without arrogance. An underdog position demands scrappy authenticity.
- **The founder's natural speech** — the best brand voices are amplified versions of how the founder actually talks, not invented personas.
- **The audience's language** — mirror how they talk to each other, not how they expect to be marketed to.
- **The competitive gap** — if every competitor sounds corporate, sound human. If every competitor sounds casual, sound sharp and precise. Voice is positioning made audible.

### Phase 2: Voice Architecture

Define voice across five dimensions. Each dimension has a spectrum — place the brand on it with specificity.

#### Dimension 1: Personality

Where does the brand sit on these spectrums?

```
Formal ←————————→ Casual
Serious ←————————→ Playful
Reserved ←————————→ Expressive
Corporate ←————————→ Personal
Authoritative ←————————→ Collaborative
Polished ←————————→ Raw
Cautious ←————————→ Bold
```

**Don't just pick a point.** Describe the specific flavor:
- Bad: "We're casual and friendly."
- Good: "We sound like a sharp friend who happens to be an expert — casual enough to use contractions and sentence fragments, but precise enough that you trust the advice. Think 'smart colleague at a bar' not 'corporate blog trying to sound relatable.'"

**Provide an example pair for each key spectrum position:**
- Bad: "We're bold."
- Good: "Bold means we say 'This doesn't work. Here's what does.' not 'There may be some challenges with this approach that could potentially be addressed.'"

#### Dimension 2: Vocabulary

**Words we use:**
Specific words and phrases that are distinctly ours. These should feel natural, not forced.

Example (for a trades business SaaS):
- "Trades businesses" not "SMBs" or "small businesses"
- "Crews" not "teams" or "employees"
- "Jobs" not "projects" or "engagements"
- "The office" not "headquarters" or "HQ"
- "Run your business" not "optimize operations" or "streamline workflows"

Example (for an internet-native SaaS):
- "Ship" not "launch" or "deploy"
- "Builders" or "makers" not "users" or "customers"
- "Break things" not "encounter issues"
- "$47K MRR" not "significant revenue growth"

**Words we never use:**
Words that signal wrong tone, wrong audience, or AI-generated content.

Common kill list:
- "Utilize" (say "use")
- "Leverage" as a verb (say "use" or be specific)
- "Comprehensive" / "robust" / "cutting-edge"
- "Synergy" / "paradigm" / "ecosystem" (unless your audience actually uses these)
- "Unlock" / "unleash" / "supercharge"
- "Delve" / "dive into" / "navigate"
- "Streamline" / "optimize" (unless being specific about what)
- "Game-changer" / "revolutionary"

**Jargon rules:**
- Industry jargon the audience uses daily → USE IT (signals "I'm one of you")
- Industry jargon the audience doesn't use → TRANSLATE IT
- Marketing jargon → NEVER (it signals "I'm selling to you")

#### Dimension 3: Rhythm and Structure

How do sentences and paragraphs flow?

**Sentence length:**
- Average target range (e.g., "8-15 words average, with punchy 3-5 word sentences for emphasis")
- Maximum before breaking up (e.g., "Never exceed 25 words without a period")
- Variation pattern (e.g., "Short. Then medium with some detail. Then short again.")

**Paragraph length:**
- Target (e.g., "1-3 sentences per paragraph, never more than 4")
- Single-sentence paragraphs: How often? (e.g., "Use for emphasis, 2-3 per page")

**Rhythm pattern:**

Example:
> "Short punch. Then a longer sentence that expands and breathes. Then land it.
>
> This is our rhythm. Impact, then context, then punctuation."

vs.

> "We tend toward longer, flowing sentences that build through parallel structure, stacking ideas and letting the reader follow the thread of logic through to its natural conclusion. Then we break with something sharp."

Define YOUR pattern. Show it, don't just describe it.

**Structural preferences:**
- Headers: conversational questions? Direct statements? Action-oriented?
- Bullet points: when to use vs. when to write prose
- Transitions: bucket brigades? Questions? Direct jumps?

#### Dimension 4: Perspective and Person

**Who's talking?**
- First person singular ("I built this because...") — founder-led, personal
- First person plural ("We believe...") — team, company
- Second person ("You know the feeling...") — direct, reader-focused
- Third person ("Companies that use X see...") — authority, editorial

Most brands use a mix. Define the default and when to shift:

Example: "Default is 'we' for company communications and 'you' for customer-facing copy. Founder voice uses 'I' for blog posts and social. Never use third person to talk about ourselves — 'Fieldkit helps businesses' should be 'We help you.'"

**Who's being talked to?**
- Peer ("Fellow builders, here's what we learned...")
- Expert to learner ("Here's how this works...")
- Friend to friend ("Look, I've been there...")
- Service provider to client ("Here's what we'll do for you...")

Define the default relationship. This affects everything.

#### Dimension 5: Values and Beliefs

What does the brand stand for — and against? These show up in voice through:

**What we'll say that others won't:**
Example:
- "We'll publicly share our revenue numbers."
- "We'll admit when our product has limitations."
- "We'll tell prospects when they don't need us."
- "We'll name competitors by name and explain the real differences."

**What we'll never say:**
Example:
- "We'll never use fake urgency ('Only 3 spots left!' when there aren't)."
- "We'll never trash a competitor without specific evidence."
- "We'll never make a claim we can't back with data or a specific example."
- "We'll never use 'industry-leading' or 'best-in-class' — show, don't claim."

**Beliefs that shape our voice:**
Example:
- "Specificity is respect — vague claims waste the reader's time."
- "Honesty converts better than hype."
- "Our audience is smart. Talk up, never down."
- "Show the work. Don't just state conclusions."

### Phase 3: Tone Variations by Context

Voice stays the same. Tone adapts. Define how the same voice shifts across situations:

| Context | Tone Shift | Example |
|---------|-----------|---------|
| **Website / Landing Page** | Confident, energetic, proof-heavy | "127 kitchens finished on time. Yours is next." |
| **Blog / SEO Content** | Helpful, expert, generous with detail | "Here's exactly how we handle permits in Georgetown — and why most contractors get this wrong." |
| **Email — Welcome** | Warm, personal, sets expectations | "Hey — glad you're here. Here's what to expect from us (and what we expect from you)." |
| **Email — Sales** | Direct, proof-driven, respectful urgency | "You've seen the case studies. You've read the reviews. At some point, the research phase ends and the building phase starts." |
| **Social Media** | Punchy, opinionated, slightly provocative | "Hot take: your 'brand guidelines' doc is why your copy sounds like everyone else's." |
| **Ad Copy** | Hook-first, benefit-driven, specific | "4-6 week kitchen remodels. Not 4-6 month nightmares." |
| **Support / Help Docs** | Clear, patient, human | "This happens sometimes. Here's exactly how to fix it — takes about 2 minutes." |
| **Crisis / Bad News** | Direct, honest, accountable | "We messed up. Here's what happened, what we're doing about it, and what it means for you." |
| **Celebrating Wins** | Genuine, specific, shared credit | "217 businesses launched this quarter using Fieldkit. That's 217 founders who bet on themselves. We just made the tools." |

**Critical:** Write actual example sentences for each context, in YOUR voice. Don't just describe the tone — demonstrate it.

### Phase 4: Voice Guardrails

#### The "Could This Be Anyone?" Test

Read every piece of copy and ask: "Could a competitor publish this under their name and it would still make sense?" If yes, the voice isn't distinctive enough. Rewrite.

Example:
- Fails test: "We help small businesses grow with powerful tools." ← Could be literally anyone.
- Passes test: "We make the software that keeps your trucks rolling and your crews on time. The rest — payroll, invoicing, scheduling — gets handled while you're on a job site, not behind a desk." ← This is specific to a trades business SaaS with a clear point of view.

#### The "Read It Out Loud" Test

Read copy out loud. Where you stumble = where the reader stumbles. Where it sounds stiff = where you lost the voice. Where you'd never actually say it that way = where you need to rewrite.

#### The "Founder Test"

Would the founder actually say this? Not in a polished presentation — in a real conversation? If the answer is no, the voice is performing, not communicating.

#### Common Voice Failures

| Failure | What It Sounds Like | The Fix |
|---------|--------------------|---------| 
| **Voice cosplay** | Trying to sound like someone else | Go back to founder's actual speech patterns |
| **Tone whiplash** | Playful headline → corporate body copy | Maintain the same personality across the piece |
| **Jargon creep** | Marketing-speak sneaking in | Replace every "optimize" and "leverage" with what you'd actually say |
| **Voice flatness** | Technically correct but no personality | Add opinions, specific examples, unexpected word choices |
| **Audience mismatch** | Talking over or under the audience | Re-read their actual words (forums, reviews, support tickets) |
| **Consistency drift** | Voice changes between pages/channels | Reference this voice file before every piece |

### Phase 5: Example Rewrites

The most useful part of a voice file. Take generic copy and rewrite it in the brand voice.

Produce at least 5 rewrite pairs covering different content types:

**Format:**
```
GENERIC: [Generic or AI-default version]
ON-BRAND: [Same message, in the brand's voice]
WHY: [What changed and why it's better]
```

**Example set (trades business SaaS):**

```
GENERIC: "Our comprehensive field service management platform helps 
businesses optimize their operations and improve efficiency."

ON-BRAND: "Run your trades business from your phone. Scheduling, 
invoices, crew tracking — handled. So you can be on the job site, 
not stuck behind a laptop."

WHY: "Trades business" not "business." "Phone" not "platform." 
Action-oriented, not feature-listing. Addresses where they 
actually are (job site), not abstract "efficiency."
```

```
GENERIC: "We're excited to announce our new feature that will 
help you manage your team more effectively."

ON-BRAND: "New: see where every crew is, right now. Took us 
3 months to build. Took our beta testers about 4 seconds 
to fall in love with it."

WHY: Specific benefit, not vague "manage more effectively." 
Shows personality with the timing contrast. Proof through 
beta tester reaction, not self-congratulation.
```

```
GENERIC: "Sign up for our newsletter to receive the latest 
industry insights and tips."

ON-BRAND: "Every Tuesday: one thing that'll make your business 
better. No fluff. Unsubscribe whenever."

WHY: Specific cadence and promise. Acknowledges their skepticism 
(no fluff). Respects their autonomy (unsubscribe whenever). 
Doesn't say "newsletter" or "insights."
```

```
GENERIC: "Our customer support team is available 24/7 to assist 
you with any questions or concerns."

ON-BRAND: "Stuck? Text us. Real humans, real answers. We've 
been in the trades — we get it."

WHY: "Text" matches how they actually communicate. "Real humans" 
addresses AI/bot fatigue. "Been in the trades" builds credibility. 
Drops "24/7" unless it's actually true.
```

```
GENERIC: "Join thousands of satisfied customers who have 
transformed their businesses with our solution."

ON-BRAND: "2,847 trades businesses. 94% stick around after 
year one. Ask any of them."

WHY: Specific number, not "thousands." Retention stat is more 
credible than "satisfied." "Ask any of them" is a confident 
challenge, not a vague claim.
```

Produce rewrites that cover: website hero, email subject line, social post, CTA, and support message. These become the voice training set for all downstream skills.

---

## Output Format

```markdown
# Brand Voice: [Brand Name]

*Generated from positioning: [date]. Reference this file in all copy and content production.*

## Voice Summary
[2-3 sentence description of how this brand sounds. Vivid enough to 
be useful, concise enough to scan.]

## Personality
[Spectrum positions with specific descriptions and example pairs]

## Vocabulary
### Words We Use
[List with context — what to say and what it replaces]

### Words We Never Use
[Kill list with alternatives]

### Jargon Rules
[What's in, what's out, what gets translated]

## Rhythm
### Sentence Patterns
[Length targets, variation pattern, with demonstration]

### Paragraph Patterns
[Length targets, single-sentence frequency]

### Structural Preferences
[Headers, bullets, transitions]

## Perspective
### Default Voice
[Who's talking, to whom, in what relationship]

### When It Shifts
[Context-specific perspective changes]

## Values in Voice
### What We'll Say That Others Won't
[List]

### What We'll Never Say
[List]

### Beliefs That Shape Our Voice
[List]

## Tone by Context
[Table with context, tone shift, and example sentence for each]

## Example Rewrites
[5+ generic → on-brand pairs with explanation]

## Voice Guardrails
### Tests to Run
[The three tests: Could-this-be-anyone, Read-aloud, Founder]

### Common Failures to Watch For
[Failure patterns specific to this brand]
```

**Save this output as `docs/brand-voice.md` (or equivalent persistent location). Every downstream skill should reference this file.**

## Output Schema — Required Section Headers

Every brand-voice output MUST contain these sections with these exact H2/H3 headers. Downstream skills reference specific sections by name — inconsistent headers break the chain.

**Required sections (must appear in every output):**

| Section | Header | Referenced By |
|---------|--------|---------------|
| Summary | `## Voice Summary` | All downstream skills (quick orientation) |
| Personality | `## Personality` | direct-response, dtc-ad-creative, content-atomizer |
| Vocabulary — Use | `### Words We Use` | All copy/content skills |
| Vocabulary — Avoid | `### Words We Never Use` | All copy/content skills |
| Jargon | `### Jargon Rules` | seo-content, newsletter, thread-writer |
| Rhythm | `## Rhythm` | direct-response, seo-content, newsletter |
| Perspective | `## Perspective` | email-sequences, newsletter, linkedin-content |
| Values | `## Values in Voice` | All copy/content skills |
| Tone by Context | `## Tone by Context` | content-atomizer (platform adaptation), email-sequences (sequence tone) |
| Example Rewrites | `## Example Rewrites` | All downstream skills (calibration reference) |
| Guardrails | `## Voice Guardrails` | skill-refiner (quality check reference) |

**Optional but encouraged sections:**

| Section | Header | When to Include |
|---------|--------|-----------------|
| Voice by ICP | `## Voice by ICP` | When multiple ICPs exist with different communication needs |
| Quick Reference Card | `## Quick Reference Card` | Always recommended — a scannable cheat sheet for writers |

**Downstream usage pattern:** Skills should reference specific sections, not the whole file:
- `See brand-voice.md ## Words We Use` for vocabulary alignment
- `See brand-voice.md ## Tone by Context` for platform-specific tone
- `See brand-voice.md ## Example Rewrites` for calibration

---

## Quality Checks

- [ ] Can someone who's never seen this brand read the voice file and write on-brand copy? Test it — hand it to someone (or a fresh AI session) and see if the output sounds right.
- [ ] Are the vocabulary lists specific to THIS brand, or could they apply to anyone? "Don't say leverage" is generic. "Say 'crews' not 'teams'" is specific.
- [ ] Do the example rewrites cover at least 5 different content types (website, email, social, CTA, support)?
- [ ] Does the personality section have example PAIRS (bad/good) or just descriptions? Descriptions alone aren't specific enough.
- [ ] Are the tone variations demonstrated with actual example sentences, not just adjective descriptions?
- [ ] Does the voice clearly differentiate from competitors? Run the "could this be anyone" test on the example rewrites.
- [ ] Is the rhythm section SHOWN (with example paragraphs demonstrating the pattern) or just TOLD?
- [ ] Are the values/beliefs specific enough to actually constrain behavior? "We value honesty" is nothing. "We'll publicly share our revenue numbers and admit product limitations on the pricing page" is something.
- [ ] Is the voice file concise enough to actually be referenced? If it's over 1,500 words, tighten it — a voice file nobody reads is worse than no voice file.
- [ ] Does the founder read this and think "yeah, that's us" or "that sounds like what we think we should sound like"? The first is right. The second means you're performing, not capturing.
- [ ] Is the voice clearly derived from the positioning angle — not a generic "friendly and professional" voice that could apply to anyone in the category?
- [ ] Can you trace specific vocabulary choices and tone decisions back to the positioning output? If not, the voice is disconnected from the strategy.
