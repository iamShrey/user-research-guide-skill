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

This skill supports any product, team, or research domain. It ships with universal assets (probing frameworks, questioning rules, output template) and a first-time setup wizard to load your team's specific context.

---

## Available Reference Assets

| Asset | File | Status |
|---|---|---|
| Org & product context | `references/org-product-context.md` | Set up by user |
| Research playbook | `references/research-playbook.md` | Set up by user |
| Probing guide | `references/probing-guide.md` | ✅ Ready |
| Questioning rulebook | `references/questioning-rulebook.md` | ✅ Ready |
| Interview guide template | `references/interview-guide-template.md` | ✅ Ready |
| Historical guides | `references/historical-guides/` | Set up by user |

---

## On Every Load: Check Setup Status

Before anything else, read `references/setup_status.md`.

- If the file contains **`not_configured`** → run the **First-Time Setup Wizard** below
- If the file contains **`configured`** → skip to **Step 0: Asset Check-In**

---

## First-Time Setup Wizard

*This runs once — the first time the skill is triggered after install.*

Welcome the user and explain what's happening:

> "Welcome! This is the first time you're running the User Research Guide skill. It ships with universal probing frameworks and question-quality rules, but works best when loaded with your team's context. Let's take 2 minutes to set that up. You can skip anything you don't have yet."

---

### Wizard Step 1: Inventory

Use the **AskUserQuestion tool**:
- **question**: "What context do you have ready to add? (You can always come back and add more later)"
- **type**: multi-select
- **options**:
  - "🏢 Org / product context — product overview, user personas, roadmap"
  - "🔬 Research playbook — your team's methods, recruiting approach, synthesis process"
  - "📁 Historical guides — past interview guides you've run"
  - "⏭️ Skip setup — I'll use the skill with generic assets for now"

If they choose "Skip setup", write `configured` to `references/setup_status.md` and proceed directly to Step 0.

---

### Wizard Step 2: Collect each selected asset

For each asset the user selected, collect the content. There are two ways they might provide it:

**Option A — File upload:**
If the user uploads a file, it will appear in the uploads folder. Read it from there.

**Option B — Paste in chat:**
Ask them to paste the content directly. Use the **AskUserQuestion tool**:
- **question**: "[Asset name]: please paste your content below, or upload a file."
- **type**: free-text

#### Org & product context
Ask: *"Please upload your org/product context doc (a product brief, PRD, one-pager, or any doc that describes your product and users) — or paste the content directly."*

A useful org context doc typically includes:
- What the product does and who it's for
- Key user segments or personas
- Current product areas and known friction points
- Roadmap priorities or active hypotheses

Once received, write the content to `references/org-product-context.md` using the SKILL_DIR path provided at load time.

#### Research playbook
Ask: *"Do you have a research playbook, methods guide, or process doc? Upload or paste it — or skip if you don't have one yet."*

A useful research playbook typically covers:
- Research methods your team uses and when
- Recruiting criteria and screener questions
- How you synthesize and share findings

Once received, write to `references/research-playbook.md`.

#### Historical guides
Ask how many guides they want to add:

Use the **AskUserQuestion tool**:
- **question**: "For historical guides: do you have past interview guides to upload, or would you like me to help generate example templates based on past research you've run?"
- **type**: single-select
- **options**:
  - "📤 I have past guides to upload or paste (1–5 files)"
  - "✍️ Help me generate examples from past objectives I describe"
  - "⏭️ Skip for now"

**If they upload/paste guides:** collect each one (ask them how many, then collect one at a time). Save each to `references/historical-guides/[topic-slug].md`. Derive a sensible filename from the research objective at the top of each guide.

**If they want generated examples:** ask them to describe 3–5 past research objectives in a few words each (e.g. "onboarding usability", "checkout drop-off", "enterprise admin workflows"). For each, generate a complete, realistic interview guide using the structure in `references/interview-guide-template.md`. Save each to `references/historical-guides/`. These are starting templates — they can refine them over time.

**Format reminder for historical guides** — each file should include at minimum:
- Research objective (1 paragraph)
- Sub-research questions (3–6)
- Target participant description
- Full guide sections following the interview-guide-template structure

---

### Wizard Step 3: Confirm and finish

Once all selected assets are saved, write `configured` to `references/setup_status.md`.

Tell the user:

> "Setup complete. Your assets are saved and will be available every time you run this skill. You can update any of them anytime by saying 'update my research assets'."

Then proceed directly to Step 0 for the current session (don't make them re-trigger the skill).

---

## Step 0: Asset Check-In

Your very first action for every normal session — before doing any research, loading files, or forming sub-questions — is to use the **AskUserQuestion tool** to present an asset selector.

Use the AskUserQuestion tool with:
- **question**: "I have the research objective. Which reference assets should I load for this session?"
- **type**: multi-select
- **options** (include only assets that are configured — check each file for `not_configured` before listing it):
  - "📋 Org & product context" *(only if org-product-context.md is configured)*
  - "🔬 Research playbook" *(only if research-playbook.md is configured)*
  - "🎯 Probing guide — 8 probing frameworks and patterns"
  - "📏 Questioning rulebook — 10 rules for question quality"
  - "📁 Historical guides" *(only if historical-guides/ has at least one .md file beyond README.md)*
  - "🔄 I need to update an asset before starting"

Wait for the user's selections before doing anything else.

- Load only what they selected
- For historical guides, load the 1–2 most topically relevant to the objective — not all of them
- If they select "I need to update an asset", ask which one, help them update it, then re-present this selector
- If no company-specific assets are configured yet, note this and offer to run setup: *"Your team-specific assets haven't been configured yet. Want to set them up now, or proceed with the universal assets only?"*

---

## Step 1: Load Selected Context

Read the files for each asset the user confirmed. Use the SKILL_DIR path provided at load time to resolve file paths.

After loading, briefly tell the user:
- What context you found and how you'll use it
- Which historical guide(s) you're drawing on, if any
- Any gaps (e.g. no historical guide matches the current topic)

---

## Step 2: Decide Whether to Search the Web

Web search fills gaps the context files can't cover. Use it when:

- The **topic isn't well covered** by the loaded context — the objective touches a product area, user segment, or behavior not addressed in any loaded asset
- The **product area is new or emerging** — not covered by any historical guide
- The research domain is **specialized** — healthcare, fintech, legal tech, logistics, developer tools, or other areas where behavior is shaped by industry-specific context
- The objective touches on **recent or shifting behaviors** — adoption patterns, competitive moves, or market changes in the past 1–2 years
- There's a need to understand the **competitive landscape**

Do NOT search just to seem thorough. If loaded context covers the topic well, skip it.

When searching: use targeted queries for behavioral context ("$domain user behavior", "$feature usability research"). Never copy questions from search results — only use them for domain context.

Summarize what you learned in 2–3 sentences and explain how it shapes the guide.

---

## Step 3: Break Down the Research Objective — Human in the Loop

Decompose the research objective into 3–6 sub-research questions (SRQs) — the strategic knowledge gaps the researcher is trying to close.

Use loaded context to:
- Frame SRQs in terms of known user segments (from org context, if loaded)
- Avoid re-exploring territory already covered by a historical guide
- Tie SRQs to active roadmap hypotheses where relevant

Good SRQs are investigable in a 1-hour session, have a clear "why this matters," cover distinct aspects, and range from behavioral to attitudinal to contextual.

**Format:**
```
Research Objective: [restate as you understand it]

Sub-Research Questions:
1. [SRQ] — Why this matters: [one sentence]
2. [SRQ] — Why this matters: [one sentence]
...
```

Then use the **AskUserQuestion tool**:
- **question**: "These are the sub-questions I'm proposing to build the guide around. Do these capture what you're trying to learn?"
- **type**: single-select
- **options**:
  - "✅ Yes, looks good — build the guide"
  - "✏️ I want to tweak one or more SRQs"
  - "🔄 Start over with a different framing"

If they choose to tweak, ask what to change before proceeding. Do not move to Step 4 until the user confirms.

---

## Step 4: Design the Interview Arc

Design the guide in these sections:

### 4a. Warm-Up (5–10 min)
Rapport and context — not primary data. Low-stakes, conversational questions about the participant's role and day-to-day. Use org context (if loaded) to tailor to the right user segment.

### 4b. Current State / Baseline Behavior (10–15 min)
Understand what participants do *before* introducing your product or topic. Anchor in specific recent episodes using **Behavioral Reconstruction (Probe Type 1)** from the probing guide: "Walk me through the last time you..."

### 4c. Core Research Questions (20–30 min)
One section per SRQ. Each needs a primary question and 2–3 probing follow-ups. Match probe types to what each SRQ is trying to surface:
- Gaps / friction → **Workaround Discovery (Type 2)**
- Expectations → **Mental Model Probing (Type 3)**
- Emotional stakes → **Emotional Impact Probing (Type 4)**
- Behavior triggers → **Decision Trigger Probing (Type 5)**
- Comparison to alternatives → **Comparison Probing (Type 6)**
- Space for unprompted detail → **Silence Probe (Type 7)**

### 4d. Concept / Stimulus Response (optional, 10–15 min)
Only if the objective involves feedback on a prototype or artifact. Use **Artifact Probe (Type 8)**. If unclear whether this applies, ask.

### 4e. Closing (5 min)
Catch-all question + graceful close.

---

## Step 5: Apply the Questioning Rulebook

Apply `references/questioning-rulebook.md` (if loaded) to every question. Check for:
- Leading language → remove it
- Double-barreled questions → split them
- Yes/no questions in core sections → open them up
- Missing probes on emotionally charged topics → add them
- Assumed behaviors participant may not have had → add conditional framing
- Questions over 20 words → simplify

End the guide with: **"Rulebook revisions: [2–3 sentence summary of what changed and why]"**

---

## Step 6: Format and Deliver

Produce the guide using `references/interview-guide-template.md`. Include:
- Header: objective, target participant, session length, date
- Moderator notes in italics
- Clear section headers with time allocations
- "Do not ask" section for any sensitive or out-of-scope topics flagged by context

Save as `[topic]-interview-guide.md` in the workspace folder (or `.docx` if the user prefers).

---

## Updating Assets

If the user says anything like "update my research assets", "edit my org context", "add a historical guide", or "my playbook changed" — treat this as an asset update request. Ask which asset they want to update, collect the new content, overwrite the relevant file, and confirm.

---

## What Good Looks Like

A great guide will:
- Be completable in the stated session length without rushing
- Cover all approved SRQs without redundancy
- Have a natural conversational flow, not an interrogation feel
- Surface behavior and motivation, not just opinion
- Use probing patterns deliberately — probe types matched to SRQ intent
- Be immediately usable by a researcher reading it cold
