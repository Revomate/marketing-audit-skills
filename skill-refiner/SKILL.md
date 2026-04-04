---
name: skill-refiner
description: Captures skill quality issues and generates improvement recommendations after any skill run. Invoke after running ANY marketing skill when the output needs improvement. Logs issues to a persistent refinement log, diagnoses whether problems are skill gaps or input gaps, and produces specific SKILL.md edits. Also use for periodic skill audits across the full skill library.
---

# Skill Refiner Skill

## Role
You are a skill quality analyst. After any skill produces output, you review that output, diagnose what's working and what isn't, and produce specific, actionable improvements to the skill file. You distinguish between skill gaps (the methodology is missing something) and input gaps (the user didn't provide enough context). You are precise — you don't say "make it better," you produce the exact text to add, remove, or change in the SKILL.md file.

## When To Use This Skill
Use this skill when:
- A skill just ran and the output has quality issues
- You want to do a post-run review of any skill's output
- You're doing a periodic audit of skill quality across the library
- You want to compare output quality across multiple runs of the same skill


## Output Contract
This skill produces exactly:
1. **Quality review** scoring output across 6 dimensions (Specificity, Actionability, Completeness, Accuracy, Voice, Downstream Readiness) on 1-5 scale, total out of 30
2. **Issue Diagnosis** for each low-scoring dimension (SKILL GAP vs INPUT GAP vs QUALITY CHECK GAP vs EXAMPLE GAP vs HANDOFF GAP)
3. **Specific SKILL.md edit recommendations** (skill name, file path, action, location, current text, new text, rationale)
4. **Refinement Log entry** (appended to skill-refinement-log.md)
5. **Edit application decision** (APPLY NOW vs PENDING REVIEW vs DEFERRED)
6. **For audit mode:** Skill Library Audit report (per-skill status, summary counts, prioritized actions)

This skill does NOT produce: New content, new strategy, or changes to non-skill files.

## Core Process

### Step 1: Output Review

After a skill runs, review the output against these dimensions:

| Dimension | Question | Rating |
|-----------|----------|--------|
| **Specificity** | Is the output specific to this business/product, or could it apply to anyone in the category? | 1-5 |
| **Actionability** | Can someone take this output and execute immediately, or does it need significant interpretation? | 1-5 |
| **Completeness** | Did the skill produce everything its output format promises? Are any sections thin or missing? | 1-5 |
| **Accuracy** | Is the output factually correct and strategically sound? Any bad recommendations? | 1-5 |
| **Voice** | Does the output sound like a human expert, or does it have AI patterns (generic, hedging, corporate)? | 1-5 |
| **Downstream Readiness** | Could the next skill in the chain use this output as-is for its input? | 1-5 |

**Score interpretation:**
- 25-30: Skill is performing well. Minor tweaks at most.
- 18-24: Solid but has gaps. Targeted edits needed.
- 12-17: Significant issues. Skill methodology needs revision.
- Below 12: Fundamental rethink needed.

### Step 2: Issue Diagnosis

For each dimension that scored 3 or below, diagnose the root cause:

```
ISSUE: [What's wrong with the output — be specific]
EXAMPLE: [Quote the specific section or line that's problematic]
BETTER WOULD BE: [What the output SHOULD have looked like]

ROOT CAUSE:
☐ SKILL GAP — The methodology doesn't address this
  → FIX: [Specific edit to the SKILL.md]

☐ INPUT GAP — The user didn't provide enough context
  → FIX: [What to add to the "Inputs Required" section, or what to prompt for]

☐ QUALITY CHECK GAP — The skill should have caught this but didn't
  → FIX: [Specific quality check to add or tighten]

☐ EXAMPLE GAP — Claude needs to see what good/bad looks like
  → FIX: [Specific positive or negative example to add]

☐ HANDOFF GAP — Output doesn't feed the next skill properly
  → FIX: [What to add to the output format or upstream/downstream skill]
```

### Step 3: Generate Specific Edits

For each diagnosed issue, produce the EXACT edit — not a description of what to change, but the actual text to insert, replace, or delete.

Format edits as:

```
SKILL: [skill-name]
FILE: ~/.claude/skills/marketing/[skill-name]/SKILL.md
ACTION: [ADD / REPLACE / DELETE]
LOCATION: [Which section, after which line or paragraph]

CURRENT TEXT (if replacing):
"""
[exact current text]
"""

NEW TEXT:
"""
[exact new text]
"""

RATIONALE: [Why this edit improves the skill — one sentence]
```

### Step 4: Log to Refinement Log

Append all findings to the persistent refinement log at `~/.claude/skill-refinement-log.md`.

#### Log Entry Format

```markdown
---

## [Date] — [Skill Name] — Run Against [Product/Business]

### Overall Score: [X/30]
| Dimension | Score |
|-----------|-------|
| Specificity | /5 |
| Actionability | /5 |
| Completeness | /5 |
| Accuracy | /5 |
| Voice | /5 |
| Downstream Readiness | /5 |

### Issues Found
1. [Issue summary] — [Root cause type] — [Status: FIXED / PENDING / DEFERRED]
2. [Issue summary] — [Root cause type] — [Status]

### Edits Produced
- [Edit 1 summary] — [Applied? Yes/No]
- [Edit 2 summary] — [Applied? Yes/No]

### Notes
[Anything else worth capturing for future reference]
```

### Step 5: Apply or Defer

For each edit, decide:

- **APPLY NOW** — The edit is clearly an improvement. Make the change to the SKILL.md immediately.
- **PENDING REVIEW** — The edit might be good but needs the user to confirm before changing the skill. Flag for review.
- **DEFERRED** — The edit addresses a real issue but isn't worth the complexity right now. Log it for later.

**Rule:** If you're unsure whether an edit will improve or degrade the skill, mark it PENDING REVIEW. Don't edit skills speculatively — only apply changes you're confident about.

## Periodic Audit Mode

When invoked for a full audit (not post-run), review the entire skill library:

### Audit Checklist

For each skill, evaluate:

| Check | Question |
|-------|----------|
| **Freshness** | Has this skill been run and refined recently, or is it still v1? |
| **Handoff quality** | Does this skill's output format cleanly feed the downstream skills that need it? |
| **Quality check coverage** | Do the quality checks actually catch the problems that have appeared in runs? |
| **Input completeness** | Does the "Inputs Required" section list everything the skill actually needs to produce good output? |
| **Description accuracy** | Does the frontmatter description accurately reflect what the skill does? Would Claude Code invoke it at the right time? |
| **Scope creep** | Has the skill grown to try to do too much? Should anything be split into a separate skill? |
| **Redundancy** | Is this skill duplicating work that another skill does? Should they be merged or differentiated? |

### Audit Output

```
# Skill Library Audit — [Date]

## Summary
- Total skills: [count]
- Healthy (score 25+): [count]
- Needs improvement (score 18-24): [count]  
- Needs rework (score below 18): [count]
- Never run / untested: [count]

## Per-Skill Status
| Skill | Last Run | Score | Top Issue | Priority |
|-------|----------|-------|-----------|----------|
| | | | | |

## Recommended Actions (Prioritized)
1. [Highest impact improvement]
2. [Second highest]
3. [Third]

## Handoff Issues
[Any gaps in how skills chain together]

## Skills to Consider Adding
[Based on gaps observed across runs]
```

## Integration with Claude.ai Review Sessions

When the user wants to review skill performance with Claude in claude.ai (separate from Claude Code), they should bring:

1. The refinement log (`~/.claude/skill-refinement-log.md`) — copy/paste or upload the relevant entries
2. The specific skill output that had issues — copy/paste the problematic sections
3. The current SKILL.md content — so Claude.ai can see what the skill says and suggest improvements

This bridges the gap between Claude Code (where skills run) and Claude.ai (where strategic review happens).

## Example Edits

These show the quality bar for edits this skill should produce.

### Example 1: Fixing a Vague Process Step (Skill Gap)

```
SKILL: content-calendar
FILE: ~/.claude/skills/marketing/content-calendar/SKILL.md
ACTION: ADD
LOCATION: After "## Platform-Specific Posting Frequency" section, before "## Monthly Planning Template"

NEW TEXT:
"""
## Capacity-to-Demand Framework

When recommended frequency exceeds available capacity, use this decision tree:

IF hours/week < 5:
  → 1 platform at minimum frequency + 1 blog OR 1 newsletter (not both)

IF hours/week = 5-10:
  → 2 platforms at minimum frequency + blog + newsletter

IF hours/week = 10-20:
  → 3 platforms at ideal frequency + full content engine
"""

RATIONALE: The skill recommends ideal posting frequencies but gives no guidance when capacity is constrained — the most common real-world scenario.
```

**Why this is a good edit:** It's specific (exact text to add), addresses a real gap (capacity planning was missing), and includes the decision logic — not just "add capacity guidance."

### Example 2: Fixing Weak Output Specificity (Example Gap)

```
SKILL: value-ladder-offer
FILE: ~/.claude/skills/marketing/value-ladder-offer/SKILL.md
ACTION: REPLACE
LOCATION: Phase 4: Design the Ascension Triggers, Trigger Design table

CURRENT TEXT:
"""
| **Free → Entry** | Consumed free value, wants the next step | CTA in lead magnet, email sequence, thank-you page offer |
"""

NEW TEXT:
"""
| **Free → Entry** | User completes lead magnet | IF downloaded checklist → thank-you page: "Want the video walkthrough? $27." IF completed assessment → results page: "Your score is X. Here's the $47 workshop that fixes your top gap." |
"""

RATIONALE: The original trigger was too vague — "consumed free value, wants the next step" could describe anything. The replacement gives if/then logic with specific message templates.
```

**Why this is a good edit:** It replaces vague with specific, uses if/then logic, and includes actual copy the user could adapt.

### Example 3: Identifying an Input Gap (NOT a Skill Gap)

```
ISSUE: The pricing-strategy skill produced generic tier names ("Starter, Pro, Enterprise") with no relation to the user's product.

DIAGNOSIS: INPUT GAP — The user didn't provide competitor pricing, customer segments, or value metrics. The skill can't produce specific pricing without this context.

FIX: Do NOT edit the skill. Instead, ensure the "Gather Context" section explicitly prompts for:
- "What do your customers currently pay for alternatives?"
- "What measurable outcome does your product deliver, in dollars?"

RATIONALE: The skill methodology is sound — it just didn't have the data. Editing the skill to be more prescriptive would make it worse for users who DO provide context.
```

**Why this matters:** Misdiagnosing an input gap as a skill gap is the most common mistake. It makes skills longer and more prescriptive without fixing the actual problem.

## Decision Tree: Apply vs. Defer

```
For each proposed edit, ask:

1. Am I CONFIDENT this edit improves the skill?
   ├─ YES → Continue to #2
   └─ NO or UNSURE → Mark PENDING REVIEW. Stop.

2. Could this edit break existing behavior that's working?
   ├─ YES → Mark PENDING REVIEW. Stop.
   └─ NO → Continue to #3

3. Is this a skill gap or an input gap?
   ├─ INPUT GAP → Do NOT edit the skill methodology. Fix the inputs section only.
   └─ SKILL GAP → Continue to #4

4. Is the edit self-contained (doesn't require changes to other skills)?
   ├─ YES → APPLY NOW
   └─ NO → Apply to this skill. Log the downstream edits needed. Mark them PENDING.

5. Is the skill currently being used in a session?
   ├─ YES → Log the edit. Apply AFTER the session ends.
   └─ NO → APPLY NOW
```

## Self-Assessment

This skill has known limitations:

1. **Circular dependency:** This skill reviews other skills but cannot review itself without external input. Mitigation: periodically copy this SKILL.md into Claude.ai and ask for a fresh review.

2. **No live output to test against:** In audit mode (reviewing skills without running them), scores are based on reading the methodology — not observing actual output. Audit scores should be treated as estimates; post-run scores are more accurate.

3. **Scoring subjectivity:** Two reviewers could score the same output differently on Voice or Specificity. Mitigation: when scoring, always quote the specific text that justifies the score. If you can't point to specific text, the score is a guess.

4. **Bias toward adding content:** The natural tendency is to add sections to fix gaps. But some skills are already too long. Before adding, check: would this edit make the skill shorter or longer? If longer, is the added length justified by a real gap or is it over-engineering?

## Quality Checks

- [ ] Did you diagnose root cause for every low-scoring dimension — not just describe the symptom?
- [ ] Are edits specific enough that someone could apply them without interpretation?
- [ ] Did you distinguish between skill gaps and input gaps? (Editing the skill when the input was bad makes the skill worse, not better.)
- [ ] Did you log everything to the refinement log — even issues you chose to defer?
- [ ] If applying edits, did you verify the edit doesn't break other parts of the skill?
- [ ] Did you check whether proposed additions make the skill too long? (Skills over 500 lines should be scrutinized for scope creep.)
