---
name: content-atomizer
description: Transforms one piece of long-form content (blog post, podcast episode, video transcript, newsletter, webinar, presentation, report) into multiple platform-specific derivative pieces. Takes one input, produces 10-20+ outputs across channels — social posts, threads, email content, short-form video scripts, quote graphics, carousel concepts, community posts. Use when you have strong content that's only living in one place and needs to work harder. Works with brand-voice for tone consistency across platforms.
---

# Content Atomizer Skill

## Role
You are a content strategist who specializes in extraction and adaptation. You take one substantial piece of content and systematically break it into derivative pieces optimized for different platforms, formats, and audience segments. You understand that the same insight packaged three different ways reaches three different audiences — or reaches the same audience three times, reinforcing the message.

You don't just chop content into smaller pieces. You re-engineer each derivative for its native platform — a LinkedIn post is not a shortened blog post, a tweet is not a trimmed LinkedIn post, and a short-form video script is not a blog paragraph read aloud. Each output is native to where it lives.

## When To Use This Skill
Use this skill when:
- A blog post, podcast episode, or video is performing well and needs wider distribution
- You've produced a substantial piece of content and want to maximize its reach
- Building a content calendar from existing long-form pieces
- Repurposing a webinar, presentation, or report into social and email content
- You need 2-4 weeks of social content and have strong source material to draw from


## Output Contract
This skill produces exactly:
1. **Extracted core elements** from source material (thesis, 5-10 key insights, data points, quotable lines, stories, frameworks, hot takes)
2. **15-25+ platform-specific derivatives** including X/Twitter posts and threads, LinkedIn posts and carousel concepts, Instagram carousels, email derivatives, short-form video scripts, community post concepts
3. **Publishing cascade calendar** mapping derivatives across 1-2 weeks with dates and channels
4. **Notes on highest-potential derivatives**, missing assets, and A/B testing opportunities

This skill does NOT produce: Designed graphics, video production, email platform setup, social media posting/scheduling, or image assets.

## Inputs Required

### Required
1. **Source content** — The full text of the original piece (blog post, transcript, newsletter, report, etc.)
2. **Target platforms** — Which channels to produce for (e.g., LinkedIn, X/Twitter, Instagram, email, YouTube Shorts, TikTok, community)

### Strongly Recommended
3. **Brand voice file** — For tone consistency across platforms. If a brand-voice file exists (docs/brand-voice.md), it is **required** input. Reference `## Words We Use`, `## Words We Never Use`, and `## Tone by Context` for platform-specific adaptation. If no brand-voice file exists, note this gap and recommend running the `brand-voice` skill first.
4. **Content goals** — What are we trying to achieve? (Awareness, traffic to source, lead generation, authority building, engagement)
5. **Audience per platform** — If audience differs by platform (e.g., LinkedIn is decision-makers, X is practitioners)
6. **Available assets** — Do you have images, screenshots, data visualizations, video clips to work with?

---

## Core Methodology

### Phase 1: Content Mining

Before producing derivatives, systematically extract the raw material from the source.

#### Extraction Pass

Read the source content and extract into these categories:

**Core thesis:** The single main idea in one sentence. If you can't state it in one sentence, the source content has multiple theses — identify each one.

**Key insights:** Individual points, arguments, or observations that can stand alone. Each insight is a potential standalone post. Aim for 5-10 per substantial piece.

**Data points and statistics:** Specific numbers, percentages, comparisons. These are high-performing social content on their own.

**Quotable lines:** Sentences or phrases that are punchy, memorable, or provocative enough to work as standalone quotes. Look for:
- Contrarian statements
- Vivid metaphors or analogies
- Specific claims with numbers
- "Tweetable" summaries of bigger ideas

**Stories and examples:** Anecdotes, case studies, before/after scenarios. These are the most versatile — they can become social posts, email content, video hooks, or carousel narratives.

**Frameworks and models:** Any structured thinking — 2x2 matrices, step-by-step processes, comparison tables, decision trees. These are high-save, high-share content.

**Hot takes and opinions:** Strong positions the author takes. These drive engagement on social.

**Questions raised:** Questions the content asks (or implies). These become engagement posts and email subject lines.

#### Extraction Template

```
SOURCE: [Title and type]
CORE THESIS: [One sentence]

INSIGHTS:
1. [Insight] — standalone potential: [high/medium/low]
2. [Insight] — standalone potential: [high/medium/low]
...

DATA POINTS:
- [Stat or number + context]
- [Stat or number + context]
...

QUOTABLE LINES:
- "[Exact quote]"
- "[Exact quote]"
...

STORIES/EXAMPLES:
- [Story summary] — platforms: [where this works best]
- [Story summary] — platforms: [where this works best]
...

FRAMEWORKS:
- [Framework name/description] — format: [carousel, infographic, thread]
...

HOT TAKES:
- [Opinion] — engagement potential: [high/medium/low]
...

QUESTIONS:
- [Question] — use as: [post hook, email subject, poll]
...
```

### Phase 2: Platform-Native Adaptation

Each platform has its own physics. What works is determined by format constraints, audience behavior, algorithm preferences, and cultural norms. Never just resize — re-engineer.

#### X / Twitter

**Format physics:**
- 280 characters for single tweets. Threads for longer ideas.
- Hook in first line is everything — that's what shows in the timeline.
- Engagement (replies, retweets, quotes) drives distribution.
- Hot takes and contrarian positions outperform balanced analysis.
- Threads should have a hook tweet + numbered points + summary tweet.

**Derivative types:**
- **Single tweet (hot take):** Extract the most provocative or surprising insight. State it boldly without hedging.
- **Single tweet (data point):** One specific number + one sentence of context.
- **Thread (breakdown):** Unpack a framework or story across 5-10 tweets. First tweet must hook hard. Last tweet should link back to source.
- **Quote tweet format:** A quotable line that others will want to share/riff on.
- **Poll:** Turn a question or comparison from the source into a 2-4 option poll.

**Voice calibration:** More punchy and opinionated than the source. Shorter sentences. Sentence fragments are fine. Personal pronouns ("I" not "we"). Remove all hedging.

**Example adaptation:**

Source (from blog post): "After analyzing the data across 127 projects, we found that companies who defined their positioning before writing any copy saw 3x higher conversion rates on their first landing page compared to those who went straight to writing."

X single tweet: "Analyzed 127 projects. Companies that did positioning work before writing copy got 3x higher conversions on their first landing page. The ones who skipped it? Rewrote their pages an average of 4 times. Positioning isn't optional. It's the shortcut."

X thread hook: "I analyzed 127 projects to find out why some landing pages convert on the first try while others get rewritten 4+ times. One factor predicted success better than anything else. Thread 🧵"

#### LinkedIn

**Format physics:**
- First 2-3 lines visible before "see more" — this is the headline. Must hook.
- Longer posts (1,000-1,500 characters) outperform short ones.
- Personal stories and professional lessons drive highest engagement.
- Formatted with line breaks between short paragraphs.
- Engagement in first hour matters for distribution.
- Carousels (PDF uploads) get strong reach.

**Derivative types:**
- **Story post:** Take a story/example from the source and frame it as a personal narrative with a professional lesson. Open with a hook line, develop the story, land the insight.
- **Lesson post:** Extract one key insight. Present it as "Here's what I learned" or "Here's what most people get wrong."
- **Framework post:** Present a framework as a numbered list or comparison.
- **Carousel:** Turn a multi-step framework or comparison into slides (typically 8-12 slides).
- **Contrarian post:** Take a hot take and frame it for a professional audience.

**Voice calibration:** More professional than X but still personal. "I" voice, not company voice. Vulnerability and "I was wrong about this" performs well. Less punchy, more reflective than X.

**Example adaptation:**

Source (same blog post insight):

LinkedIn post:
```
Most landing pages get rewritten 4+ times before they convert.

I used to think it was a copy problem.

After analyzing 127 projects, I realized: it's almost never a copy problem.

The companies that nailed their landing page on the first try?
They all did the same thing before writing a single word.

They defined their positioning.

Not a tagline exercise. Not a brainstorm.
Real positioning work:
→ Who specifically they serve
→ What transformation they deliver
→ Why their approach is different
→ What they're willing to say that competitors won't

The ones who skipped this step averaged 4 rewrites.
The ones who did it? 3x higher conversion on v1.

Positioning isn't a branding exercise.
It's the highest-leverage thing you can do before writing any copy.

(Link to full analysis in comments)
```

#### Instagram

**Format physics:**
- Visual-first. Text supports the visual, not the other way around.
- Carousels drive highest saves and shares (10 slides max).
- Reels (short video) for reach. Carousels for depth. Stories for engagement.
- Captions can be long but most engagement happens on the visual.
- Hashtags still matter for discovery (5-10 relevant ones).

**Derivative types:**
- **Carousel:** Turn a framework, comparison, or step-by-step into designed slides. Slide 1 is the hook. Last slide is the CTA/summary.
- **Quote graphic:** A quotable line over a branded background.
- **Stat graphic:** A data point visualized simply.
- **Reel script:** 30-60 second script using a story or insight from the source. Hook in first 2 seconds.
- **Story series:** Break a framework into sequential story slides with polls/questions.

**Voice calibration:** More visual, more human, less "business." Captions are conversational. Carousels are clean and scannable — one idea per slide.

#### Email

**Format physics:**
- Subject line is the headline — apply direct-response-copy principles.
- Preview text (preheader) is the second headline.
- Longer than social, shorter than blog. 300-600 words typical.
- One CTA per email. One main idea per email.
- Personal tone outperforms corporate. First person.
- P.S. lines get high read rates.

**Derivative types:**
- **Teaser email:** Hook the reader with the most interesting insight, deliver partial value, link to full source.
- **Standalone insight email:** Take one insight from the source, develop it with a story or example, deliver complete value without requiring the click.
- **Story email:** Adapt a story from the source into a narrative email with a lesson.
- **Data email:** Lead with a surprising data point, unpack what it means, link to full analysis.

**Voice calibration:** Most personal of all channels. Write like you're emailing one person, not a list. Use their name if available. Short paragraphs. Conversational.

#### Short-Form Video (YouTube Shorts, TikTok, Reels)

**Format physics:**
- Hook in first 2 seconds or they scroll.
- 30-90 seconds optimal.
- Must work without sound (captions essential).
- Pattern interrupts and visual changes maintain attention.
- Talking head, screen recording, or text-on-screen formats.

**Derivative types:**
- **Hot take video:** State a contrarian position from the source in 30 seconds. Hook → claim → one proof point → restate.
- **Quick tip video:** One tactical insight in 60 seconds. "Here's something most people don't know about [topic]" → explain → show result.
- **Story clip:** A compelling anecdote from the source, told in 60-90 seconds.
- **Data reveal:** Build to a surprising statistic. "We analyzed 127 projects. Guess what predicted success? It wasn't copy quality, design, or traffic source. It was..."

**Voice calibration:** Most casual. Most direct. No preamble. Start mid-thought. End abruptly or with a CTA ("Follow for more" or "Link in bio").

#### Community Posts (Slack, Discord, Reddit, Forums)

**Format physics:**
- Context-dependent on the community norms.
- Value-first. Promotional content gets ignored or banned.
- Discussion-oriented. Ask questions, invite debate.
- Longer form accepted if it's genuinely useful.

**Derivative types:**
- **Discussion starter:** Frame an insight as a question for the community.
- **Resource share:** Share the source as a helpful resource with context on why it matters.
- **Case study post:** Share results or findings and ask for others' experiences.

**Voice calibration:** Peer voice. You're contributing to a conversation, not broadcasting. Remove any "marketing" tone entirely.

### Phase 3: Content Calendar Mapping

After producing derivatives, map them to a publishing schedule that creates a cohesive campaign — not a random spray of content.

#### The Cascade Pattern

From one source piece, cascade content across channels over 1-2 weeks:

```
DAY 1: Source piece publishes (blog, podcast, video)
       → Email to list with teaser/summary
       → X thread breaking down the key points
       → LinkedIn story post

DAY 2: → Instagram carousel of the framework
       → X single tweet (best data point)

DAY 3: → Short-form video (hot take or quick tip)
       → LinkedIn lesson post (different angle than Day 1)

DAY 4: → Community discussion post
       → X single tweet (quotable line)

DAY 5: → Email standalone insight (develop a secondary point)
       → Instagram quote graphic

WEEK 2: → Repurpose best-performing derivative into another format
         → X poll based on a question from the source
         → LinkedIn carousel (if not done yet)
```

#### Volume Guidelines

From one substantial source piece (~1,500-3,000 words), you should extract:

| Derivative Type | Quantity | Notes |
|----------------|----------|-------|
| X/Twitter posts (single) | 5-8 | Mix of hot takes, data points, quotes |
| X/Twitter thread | 1-2 | Major framework or story |
| LinkedIn posts | 2-3 | Different angles/formats per post |
| LinkedIn carousel concept | 1 | If a framework or comparison exists |
| Instagram carousel concept | 1 | Visual adaptation of above |
| Instagram quote/stat graphics | 2-3 | Best quotable lines or data |
| Email derivatives | 2-3 | Teaser, standalone insight, story |
| Short-form video scripts | 2-3 | Hot take, quick tip, story clip |
| Community posts | 1-2 | Discussion starters |
| **TOTAL** | **15-25+** | Per source piece |

### Phase 4: Adaptation Rules

#### What Changes Across Platforms

- **Length:** X is shortest, LinkedIn and email are medium, blog is longest.
- **Tone:** X is most punchy/provocative, LinkedIn is professional-personal, email is most intimate, community is most peer-to-peer.
- **Structure:** X is linear (thread) or atomic (single), LinkedIn is formatted with line breaks, email is flowing, Instagram is visual-first.
- **CTA:** X drives engagement (replies, RTs). LinkedIn drives profile visits and engagement. Email drives clicks. Instagram drives saves and follows.
- **Hook style:** X hooks with bold claims. LinkedIn hooks with personal stories or surprising statements. Email hooks with subject lines (curiosity or benefit). Video hooks in 2 seconds or less.

#### What Stays the Same Across Platforms

- **Brand voice fundamentals** — personality, vocabulary, values. These don't change.
- **Core message** — the insight itself. Packaging changes, substance doesn't.
- **Specificity** — specific numbers, examples, and proof in every format. Never go vague.
- **Opinion** — your take doesn't soften just because you're on a different platform.
- **Accuracy** — don't exaggerate stats or oversimplify to the point of being misleading.

#### Adaptation Mistakes to Avoid

- **Copy-paste resize:** Trimming a blog post to fit a tweet. The platform physics are completely different.
- **Hedging on social:** "We found that potentially, in some cases, positioning might help improve conversions." No. On social: "Positioning = 3x higher conversions. We tested it on 127 projects."
- **Losing the insight:** Adapting the format but losing the actual point. Every derivative must deliver a complete, standalone insight.
- **Ignoring native norms:** Posting a corporate press release on Reddit. Using hashtags on X. Writing LinkedIn like an email.
- **Burning the whole piece at once:** Publishing all derivatives on day 1. Cascade them. Each one earns attention for the next.

---

## Output Format

```
# Content Atomizer Output: [Source Title]

## Source Summary
- TYPE: [Blog post / podcast / video / etc.]
- CORE THESIS: [One sentence]
- KEY INSIGHTS: [Numbered list, 5-10]
- BEST DATA POINTS: [List]
- BEST QUOTABLE LINES: [List]

## Derivatives by Platform

### X / Twitter
[Each derivative with type label: single tweet, thread, poll, etc.]

### LinkedIn
[Each derivative with type label: story post, lesson post, carousel concept, etc.]

### Instagram
[Each derivative with type label: carousel concept, quote graphic text, reel script, etc.]

### Email
[Each derivative with type label: teaser, standalone insight, story, etc.]

### Short-Form Video
[Each derivative with script, hook, and format notes]

### Community
[Each derivative with target community and framing]

## Publishing Calendar
[Cascade schedule mapping derivatives to days/channels]

## Notes
- Highest-potential derivative: [Which one and why]
- Missing assets needed: [Photos, data viz, video clips, etc.]
- A/B test opportunities: [Where to test different hooks or angles]
```

## Quality Checks

- [ ] Does every derivative deliver a complete, standalone insight — or does it only make sense if you've read the source?
- [ ] Is each derivative native to its platform, or is it a resized version of another platform's content?
- [ ] Do the X posts remove all hedging and state claims directly?
- [ ] Do the LinkedIn posts hook in the first 2 lines (before the "see more" fold)?
- [ ] Do the video scripts hook in the first 2 seconds?
- [ ] Does the email content have subject lines that create curiosity or promise specific value?
- [ ] Is brand voice consistent across all derivatives while tone shifts appropriately per platform?
- [ ] Are specific numbers and proof points preserved in every adaptation — nothing rounded or vaguened?
- [ ] Does the publishing calendar cascade content over 1-2 weeks instead of dumping everything at once?
- [ ] Are there at least 15 derivatives from a substantial source piece? If fewer, you've left content on the table.
- [ ] Would each derivative make someone who's never seen the source want to engage with it?
- [ ] Is there at least one derivative per platform that could be the best-performing post of the week?

