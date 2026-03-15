# Probing Frameworks & Patterns
## Master Guide for User Research Interviews

---

## Purpose

This guide defines structured probing techniques for interviews and usability sessions. While the questioning rulebook covers question quality and bias avoidance, this document focuses on *how to follow up* — the patterns researchers use to move from a surface answer to real behavioral evidence.

Intended for: UX researchers, PMs running interviews, designers moderating usability tests, editorial teams conducting audience research.

**The goal: move from shallow answers → real behavior insights.**

---

## The Core Principle

People rarely explain their behavior accurately. They forget details, rationalize decisions, describe ideal behavior instead of real behavior, and skip over friction they've already solved.

**A probe exists to reconstruct the moment where the behavior actually happened.**

> Always probe the moment *before* and *after* the behavior.

**Example:**
> User: "I usually find recipes pretty easily."
> ❌ Weak: "Great."
> ✅ Strong: "Walk me through the last time you searched for a recipe. What did you type first?"

---

## Probe Type 1: Behavioral Reconstruction

**Goal:** Understand what actually happened, step by step.

People speak in summaries. Researchers need timelines.

**Pattern:** Ask for the last real instance, then walk through it.

Starter probes:
- "Tell me about the last time you cooked dinner using a recipe online."
- "What was the first thing you did?"
- "What happened after that?"

Follow-up probes:
- "What made you choose that recipe?"
- "Did anything slow you down?"
- "What did you do next?"

**Signal:** A step-by-step narrative. If the participant jumps to conclusions ("It was easy"), pull them back to specific actions.

---

## Probe Type 2: Workaround Discovery

**Goal:** Surface unofficial solutions that reveal product gaps.

Workarounds are gold — they mean a user already identified a problem and built their own fix.

**Pattern:** Ask what happens when the expected path breaks down.

Starter probes:
- "What do you usually do when that happens?"
- "Do you substitute something?"
- "Where do you check what to substitute?"

Second-layer probes:
- "Is that something you learned from experience, or did you find it somewhere?"
- "Do you ever look at the comments for that?"

**Signal:** Unofficial workflows. Workarounds often map directly to missing product features.

---

## Probe Type 3: Mental Model Probing

**Goal:** Understand what users *expect* the system to do, before they interact with it.

If the product doesn't match the user's mental model, friction appears — often without the user being able to name it.

**Pattern:** Ask users to articulate their assumptions and decision rules.

Starter probes:
- "How do you decide if a recipe is reliable?"
- "What makes you trust a recipe online?"
- "What do you expect to see before starting a recipe?"

Follow-up probes:
- "What would make you abandon a recipe midway?"
- "What tells you a recipe is beginner-friendly?"

**Signal:** Decision heuristics. Example: "If a recipe has a lot of reviews, I trust it" → social proof mental model. These heuristics reveal design assumptions worth testing.

---

## Probe Type 4: Emotional Impact Probing

**Goal:** Understand the emotional stakes behind a behavior.

Behavior is often driven by emotion, not logic. Surfacing emotional response tells you what *matters*, not just what *happens*.

**Pattern:** Ask what the experience was *like*, not just what happened.

Starter probes:
- "What happens for you when that goes wrong?"
- "What's that like when you're cooking for family?"
- "Has that happened recently?"

Second-layer probes:
- "How did you feel in that moment?"
- "What did you do to recover from that?"

**Signal:** Emotions like stress, embarrassment, frustration, pride. These guide product prioritization — high-emotion friction is usually worth solving.

---

## Probe Type 5: Decision Trigger Probing

**Goal:** Find the real-world moment that prompted the user to act.

Every behavior has a trigger — an event, need, or pressure that kicked it off. Understanding triggers helps with timing, notifications, and entry-point design.

**Pattern:** Ask what caused the session to start.

Starter probes:
- "What made you start looking for that recipe?"
- "What were you trying to solve that day?"

Follow-up probes:
- "Did something prompt that search?"
- "Was it planned, or did it come up spontaneously?"

**Signal:** Real-world triggers — grocery shopping, dinner planning, dietary constraint, time pressure. These shape when and where users engage with the product.

---

## Probe Type 6: Comparison Probing

**Goal:** Surface competitive insight and unmet needs by asking about alternatives.

Users often reveal what they need most by describing what other tools do well — or what they wish existed.

**Pattern:** Ask about other tools in the same space.

Starter probes:
- "Do you use any other recipe apps or websites?"
- "What do those do better than this one?"
- "What do you come here for instead?"

Follow-up probe:
- "If you could combine the best parts of both, what would that look like?"

**Signal:** Competitive differentiation gaps. Often surfaces features users want but haven't requested directly.

---

## Probe Type 7: Silence Probe

**Goal:** Let the participant fill the space with unprompted, authentic detail.

After a participant answers, pause for 3–5 seconds before speaking. Humans fill silence — often with their most honest and unexpected thoughts.

**Example:**
> Participant: "Yeah it was fine."
> Researcher: *[pause]*
> Participant: "Actually the measurements were really confusing."

**Signal:** Silence often unlocks the second layer of a response — the part the participant didn't think to include. Mark `[pause]` in guides at moments where this is especially valuable.

---

## Probe Type 8: Artifact Probe

**Goal:** Anchor the conversation in real evidence rather than memory.

Instead of asking abstract questions, probe using real things the user has done — saved recipes, shopping lists, screenshots, search history.

**Pattern:** Ask the user to show you something they actually made or saved.

Starter probe:
- "Can you show me a recipe you recently saved?"

Follow-up probes:
- "Why this one?"
- "What stood out when you saved it?"
- "Did you end up making it? How did that go?"

**Signal:** Real artifacts reveal real decision-making — things the user chose, not things they imagine they'd choose. Particularly powerful for recipe box, collections, and shopping list research.

---

## When NOT to Probe

Probing can backfire if overused or poorly timed.

Avoid probing when:
- The user clearly cannot remember the specific instance
- The follow-up would become leading (pulling toward a specific answer)
- Probing interrupts natural task flow in a usability test
- The participant shows signs of discomfort or feeling judged

Good probing is **curious, not interrogative.**

---

## Signs a Probe Worked

- The user tells a story (specific, episodic)
- The user corrects themselves ("Actually, what I really do is...")
- The user demonstrates behavior (opens a real app, shows a screenshot)
- An unexpected workflow appears

If answers stay abstract and general, the probe likely missed the behavioral layer — try a different probe type or ask for a specific recent example.

---

## Quick Reference: Probe Type → Use Case

| Probe Type | Use When... |
|---|---|
| Behavioral Reconstruction (1) | You need a step-by-step account of what actually happened |
| Workaround Discovery (2) | User mentions a problem they've "solved" or "worked around" |
| Mental Model (3) | You want to understand expectations before interaction |
| Emotional Impact (4) | User mentions frustration, surprise, or pride |
| Decision Trigger (5) | You want to know what prompted the behavior |
| Comparison (6) | Researching competitive landscape or unmet needs |
| Silence (7) | After any answer — create space for unprompted detail |
| Artifact (8) | User has real saved content, screenshots, or history to show |
