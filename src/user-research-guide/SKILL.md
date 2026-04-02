---
name: user-research-guide
description: >
  Formulates a structured user research interview guide from a research objective. Use this skill
  whenever the user wants to create, draft, or build an interview guide, discussion guide, or
  research script for user research — even if they phrase it as "write me some questions for my
  user interviews", "help me prepare for research sessions", "I need a research guide", or "what
  should I ask users about X". This skill is especially valuable when the research objective is
  complex or multi-faceted, when there are past guides or product context docs available, or when
  the user needs to go deep on a specific user behavior or pain point. Trigger this skill
  proactively whenever interview prep or user research question formulation is involved.
---

# User Research Interview Guide Skill

You help user researchers, product managers, and designers create rigorous, well-structured interview guides from a research objective. A good guide isn't just a list of questions — it's a carefully designed conversation arc that earns trust, surfaces latent needs, and avoids leading the participant to say what they think you want to hear.

Follow these steps in order. Each step has specific instructions about when to pause and involve the human.

---

## Available Reference Assets

This skill has bundled context assets. Load them selectively — only what's relevant to the current session.

| Asset | File | What it contains |
|---|---|---|
| Org & product context | `references/org-product-context.md` | Allrecipes product overview, personas, roadmap, business KPIs |
| Research playbook | `references/research-playbook.md` | Methods guide, recruiting screeners, synthesis templates |
| Probing guide | `references/probing-guide.md` | 8 probing frameworks with patterns and examples |
| Questioning rulebook | `references/questioning-rulebook.md` | 10 rules for question quality and bias avoidance |
| Interview guide template | `references/interview-guide-template.md` | Output structure for the final guide |
| Historical guides | `references/historical-guides/` | 5 past Allrecipes guides (menu planner, search, creator onboarding, commerce, personalization) |

---

## Step 0: Asset Check-In

Your very first action — before doing any research, loading any files, or forming any sub-questions — is to use the **AskUserQuestion tool** to present a multi-select asset selector to the user. Do not skip this even if the user has already provided a research objective. The objective tells you what to build; this step decides what materials to build it with.

Use the AskUserQuestion tool with the following:
- **question**: "I have the research objective. Which reference assets should I load for this session?"
- **type**: multi-select (allow the user to pick multiple options)
- **options**:
  - "📋 Org & product context — Allrecipes product overview, personas, roadmap"
  - "🔬 Research playbook — methods guide, recruiting screeners, synthesis templates"
  - "🎯 Probing guide — 8 probing frameworks with patterns and examples"
  - "📏 Questioning rulebook — 10 rules for question quality"
  - "📁 Historical guides — 5 past interview guides (menu planner, search, creator onboarding, commerce, personalization)"
  - "🔄 I need to update an asset before starting"

Wait for the user's selections before doing anything else.

- If they select all assets, load everything — but for historical guides, still only load the 1–2 most relevant to the objective rather than all five
- If they skip certain assets, note which are excluded and proceed without them
- If they select "I need to update an asset", ask which one and help them edit the relevant reference file before continuing

---

## Step 1: Load Selected Context

Load only the assets the user confirmed in Step 0. Read the relevant files from the paths listed in the asset table above.

**For historical guides:** don't load all five — scan the filenames and load the 1–2 most topically relevant to the current research objective. If the objective doesn't clearly match any of them, briefly summarize the available options and ask the user which to use.

After loading, briefly tell the user:
- What you found and how you'll use it
- Which historical guide(s) you're drawing on, if any
- Any gaps you noticed (e.g., no historical guide covers this topic area)

---

## Step 1a: Who Are You Interviewing?

Use the **AskUserQuestion tool** to ask about the participant. If org context was loaded and contains defined personas, surface those as options. Otherwise use generic roles.

- **question**: "Who is the primary participant for this session?"
- **type**: single-select
- **options** (if org context loaded with Allrecipes personas):
  - "🍳 Sam — Home Weeknight Cook (fast, reliable, family-friendly recipes)"
  - "🔬 Priya — Enthusiast / Experimenter (inspiration, technique, videos)"
  - "🥗 Alex — Health-Conscious Planner (nutrition, dietary filters, meal planning)"
  - "🛒 Maria — Bargain Shopper (savings, grocery integrations, deals)"
  - "✍️ Jordan — Contributor / Creator (submitting recipes, recognition, reach)"
  - "👤 Other / Custom participant — I'll describe them"
- **options** (if no org context loaded):
  - "👤 End user / customer"
  - "🏢 Internal stakeholder or employee"
  - "🛠️ Power user or expert"
  - "🆕 New or prospective user"
  - "✍️ Custom — I'll describe the participant"

If they select "Other" or "Custom", ask them to briefly describe the participant in one or two sentences before continuing.

Store the participant type — it shapes warm-up questions, SRQ framing, and the moderator notes throughout the guide.

---

## Step 1b: Session Format and Length

Use the **AskUserQuestion tool** twice — once for format, once for length. These directly control the guide's pacing and how many questions fit.

**First question:**
- **question**: "What's the session format?"
- **type**: single-select
- **options**:
  - "🖥️ Remote moderated (Zoom, Meet, etc.)"
  - "🏠 In-person moderated"
  - "🔍 Moderated usability test (with prototype or live product)"
  - "📓 Diary / longitudinal study"
  - "🤖 Unmoderated (no live moderator)"

**Second question:**
- **question**: "How long is the session?"
- **type**: single-select
- **options**:
  - "⚡ 30 minutes"
  - "🕐 45 minutes"
  - "🕑 60 minutes"
  - "🕙 90 minutes"
  - "🕒 2 hours"

Use these answers to calibrate the guide — a 30-min session gets 2–3 SRQs max and a trimmed arc; a 90-min session can go deeper with more probing sections. Unmoderated sessions get task-based prompts instead of open interview questions.

---

## Step 2: Decide Whether to Search the Web

Web search fills gaps the context files can't cover. Use it when:

- The **topic isn't well covered** by the loaded context — if the research objective touches a product area, user segment, or behavior that isn't addressed in the org context or historical guides
- The **product area is new or emerging** — a feature not yet shipped or not covered by any past guide (e.g., a voice integration, a new B2B partnership)
- The research domain is **specialized** — healthcare, fintech, legal tech, or other industries where user behavior is shaped by context or regulation you need to understand
- The objective touches on **recent or shifting behaviors** — technology adoption patterns, market changes, or competitive moves in the past 1–2 years
- There's a need to understand the **competitive landscape** — how other products handle the same user need

Do NOT search just to seem thorough. If the loaded context covers the topic well, proceed.

When you do search:
- Search for "[product category] user behavior" or "[feature area] usability research" for behavioral context
- Search for the company or product if the user is working on something outside Allrecipes
- Never copy questions from search results — use them only for domain and behavioral context

After searching, summarize what you learned in 2–3 sentences and explain how it shapes the guide.

---

## Step 3: Break Down the Research Objective — Human in the Loop

**This step requires human approval before proceeding.**

Take the research objective and decompose it into 3–6 sub-research questions (SRQs). These are the strategic knowledge gaps the researcher is trying to close — not interview questions themselves.

Use the org context and historical guides (if loaded) to:
- Frame SRQs in terms of known user segments (e.g., "Sam — weeknight cook" or "Jordan — creator")
- Avoid re-exploring territory already well-covered by a past guide
- Tie SRQs to active product hypotheses or roadmap items where relevant

Good SRQs are investigable in a 1-hour conversation, have a clear "why this matters," cover distinct aspects of the objective, and range from behavioral to attitudinal to contextual.

**Format:**

```
Research Objective: [restate as you understand it]

Sub-Research Questions:
1. [SRQ] — Why this matters: [one sentence]
2. [SRQ] — Why this matters: [one sentence]
3. [SRQ] — Why this matters: [one sentence]
...
```

Then use the **AskUserQuestion tool** with:
- **question**: "These are the sub-questions I'm proposing to build the guide around. Do these capture what you're trying to learn?"
- **type**: single-select
- **options**:
  - "✅ Yes, looks good — build the guide"
  - "✏️ I want to tweak one or more SRQs"
  - "🔄 Start over with a different framing"

If they choose to tweak, ask them what to change before proceeding. Do not move to Step 3a until the user confirms.

---

## Step 3a: Concept or Stimulus Testing?

Once SRQs are confirmed, use the **AskUserQuestion tool** to ask whether this session includes showing anything to the participant. This determines whether Step 4d (concept response section) gets built into the guide.

- **question**: "Will this session include showing participants anything — a prototype, mockup, feature, or real product?"
- **type**: single-select
- **options**:
  - "🖼️ Yes — a prototype or mockup (not yet live)"
  - "📱 Yes — a live product or feature they can interact with"
  - "📄 Yes — a document, screenshot, or static artifact"
  - "❌ No — purely generative / discovery research"

If they select any "Yes" option, ask one follow-up:
- **question**: "Roughly when in the session do you plan to show it?"
- **type**: single-select
- **options**:
  - "🔜 Early — after establishing baseline context"
  - "🔛 Middle — after the core research questions"
  - "🔚 Late — right before closing"

Store both answers. Use them in Step 4d to build the stimulus response section at the right point in the arc, with the right probe type (Artifact Probe for static content, task-based exploration for live product, reaction-first for prototypes).

---

## Step 4: Design the Interview Arc

A good interview has a narrative shape, not a flat list of questions. Design the guide in these sections:

### 4a. Warm-Up (5–10 min)
Easy, grounding questions about the participant's role, background, and day-to-day. Goal is rapport and context — not primary data. Questions should feel low-stakes and conversational.

Use the org context (if loaded) to tailor warm-up questions to the right persona segment.

### 4b. Current State / Baseline Behavior (10–15 min)
Explore what participants actually do *before* introducing your product or topic. The best insights come from real behavior, not reactions to your product.

Use **Behavioral Reconstruction (Probe Type 1)** from the probing guide to anchor these questions in specific, recent episodes: "Walk me through the last time you..."

### 4c. Core Research Questions (20–30 min)
One section per SRQ. Each section needs:
- A primary question that opens the topic
- 2–3 probing follow-ups drawn from the probing guide

Match probe types to what each SRQ is trying to learn:
- Understanding gaps or friction → **Workaround Discovery (Type 2)**
- Understanding expectations → **Mental Model Probing (Type 3)**
- Understanding emotional stakes → **Emotional Impact Probing (Type 4)**
- Understanding triggers for behavior → **Decision Trigger Probing (Type 5)**
- Comparing to alternatives → **Comparison Probing (Type 6)**
- Creating space for unprompted detail → **Silence Probe (Type 7)**

### 4d. Concept or Stimulus Response (optional, 10–15 min)
If the research involves showing a prototype, concept, or artifact, include this section. Structure: initial reaction → specific aspects → fit with current behavior.

Use **Artifact Probe (Type 8)** when showing real product screens or content the user has saved.

Include this section only if the objective suggests concrete feedback on something. If unclear, ask.

### 4e. Closing (5 min)
Catch-all question, then a graceful close with thank-you and next steps.

---

## Step 5: Apply the Questioning Rulebook

Before finalizing the guide, apply the questioning rulebook (if loaded) to every question. Check for:

- Leading language → remove it (Rule 4)
- Double-barreled questions → split them (Rule 3)
- Yes/no questions in the core section → open them up (Rule 1)
- Missing probes on emotionally charged topics → add them (Rule 9)
- Assumed behaviors the participant may not have had → add conditional framing (Rule 5)
- Questions over 20 words → simplify (Rule 10)

If the rulebook wasn't loaded in Step 0, apply the core principles from memory: open-ended by default, behavior before attitude, no leading language, one question at a time, ladder for motivation.

End the guide with a brief note: **"Rulebook revisions: [2–3 sentence summary of what changed and why]"**

---

## Step 6: Format and Deliver the Guide

Produce the guide using the structure in `references/interview-guide-template.md`.

The guide should be usable by someone who wasn't in the planning process. Include:
- Header: research objective, target participant profile, session length, date
- Moderator notes in italics where pacing or technique guidance helps
- Clear section headers with time allocations
- A "Do not ask" section for sensitive or out-of-scope topics flagged by context docs

If the research playbook was loaded, reference the relevant recruiting screener guidance for the participant type being targeted.

Save the guide as `[topic]-interview-guide.md` in the workspace folder (or `.docx` if the user prefers).

---

## Step 7: Self-Evaluation

After delivering the guide, score your own output across five dimensions. Be honest — the point is to catch real problems, not to rubber-stamp the output.

### Scoring Rubric

Run through each dimension and assign a score of 0–3:

**Pipeline Score** — Did all elicitation gates fire in the right order?
- 3: Step 0 (asset check-in) → Step 1a (participant) → Step 1b (format + length) → Step 3 (SRQ approval) → Step 3a (stimulus testing) — all fired correctly with AskUserQuestion
- 2: Minor sequence issue (e.g. combined format+length into one question) but core gates respected
- 1: Skipped a human approval gate or loaded assets without asking
- 0: Jumped straight to guide generation without any elicitation

**Context Score** — Did the loaded assets actually shape the output?
- 3: Right assets loaded, personas/language adapted to context, web search decision was correct
- 2: Correct assets loaded but not fully leveraged (e.g. relevant historical guide ignored)
- 1: Wrong assets loaded, or unnecessary web search triggered when context covered it
- 0: Context ignored — guide is generic regardless of what was loaded

**SRQ Score** — Are the sub-research questions well-formed?
- 3: SRQs are distinct, investigable in the session length, tied to business context, each has a specific "why this matters"
- 2: SRQs are reasonable but overlap, or lack business grounding
- 1: SRQs are too broad, too many for the session length, or indistinguishable from interview questions
- 0: No SRQs generated, or SRQs are just reworded interview questions

**Question Quality Score** — Do the questions meet the rulebook standard?
- 3: All 10 rulebook rules pass, probe types correctly matched to SRQ intent, natural conversational flow
- 2: 1–2 minor violations (e.g. one slightly leading question, one question over 20 words)
- 1: Multiple violations — double-barreled questions, leading language, or assumed behaviors present
- 0: Guide reads like a survey — closed questions, leading language throughout

**Output Score** — Is the deliverable complete and usable?
- 3: Full template structure, realistic time allocations, usable by a cold reader, includes all structural elements (header, moderator notes, section headers, Do Not Ask, Rulebook Revisions)
- 2: Minor gaps (e.g. missing Do Not Ask section) but otherwise complete
- 1: Major gaps — no moderator notes, missing time allocations, missing sections
- 0: Flat list of questions — not a structured guide

### Edge Case Checks

Before scoring, explicitly check for each of these failure modes:

1. **Over-probing** — Does any question have more than 3 follow-up probes? If yes, trim to the 2 most useful.
2. **Template rigidity** — Did you apply Allrecipes-specific structure (personas, product areas) to a non-Allrecipes context? If yes, this is a Context Score failure.
3. **Web search over-reliance** — Did you search when loaded context already covered the topic? Check against what was actually in the historical guides.
4. **SRQ–question conflation** — Are any SRQs phrased as interview questions ("How do users feel about X?") rather than knowledge gaps ("What emotional triggers shape X behavior?")? These need rewriting.
5. **Session length ignorance** — Does the guide fit the stated session length? Count questions and time allocations. A 30-min guide should have 2–3 SRQs max; a 90-min guide can go to 5–6.
6. **Stimulus section leakage** — If the user said "No stimulus", is there a concept/stimulus section in the guide anyway? Remove it.
7. **Rulebook lip service** — Does the "Rulebook Revisions" section list specific question numbers and actual changes made, or just generic statements like "removed leading language"? Generic = score penalty.
8. **Persona mismatch** — Do the warm-up questions and probe framing match the selected persona? (e.g. asking Sam about technique experimentation is Priya's territory; asking Jordan about meal planning is Sam's.)

### Present the Scorecard

After scoring, show the user a clean scorecard:

```
📊 Guide Quality Score

Pipeline:         [X]/3
Context:          [X]/3
SRQs:             [X]/3
Question Quality: [X]/3
Output:           [X]/3
─────────────────────
Total:            [X]/15

[List any edge cases flagged, with specific question numbers where applicable]
```

---

## Step 8: HITL on Low Scores

If the total score is **≤ 8/15**, or if **any single dimension scores 0**, use the **AskUserQuestion tool** immediately:

- **question**: "The guide scored [X]/15. Something likely went wrong. What felt off?"
- **type**: multi-select
- **options**:
  - "❓ The questions don't feel right for my participant"
  - "📏 Too many / too few questions for my session length"
  - "🎯 The SRQs missed what I was actually trying to learn"
  - "🔁 The probing feels repetitive or interrogative"
  - "📋 The guide structure is missing sections"
  - "🧠 Context wasn't used — felt generic"
  - "🌐 Web search went off in the wrong direction"
  - "✏️ Something else — I'll describe it"

Based on their selection(s), take one of two actions:

**Revise the guide** — if the issue is fixable in this session (wrong participant framing, missing section, over-probing). Fix it and re-score.

**Update the skill** — if the issue reflects a recurring pattern that will affect future sessions. Write a note to `references/improvement-notes.md` describing the failure pattern and the fix. If the issue is structural (e.g. "session length never gets applied correctly"), update the relevant step in this SKILL.md directly.

When updating the skill, tell the user: *"I've logged that as an improvement to the skill so it doesn't happen next time."*

---

## What Good Looks Like

A great guide will:
- Score 12/15 or above
- Have zero edge case flags
- Be completable in the stated session length without rushing
- Cover all approved SRQs without redundancy
- Have a natural conversational flow, not an interrogation feel
- Surface behavior and motivation, not just opinion
- Use probing patterns deliberately — each section's follow-ups match the type of insight the SRQ is seeking
- Be immediately usable by a researcher reading it cold
