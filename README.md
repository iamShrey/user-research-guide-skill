# User Research Interview Guide — Claude Skill

A Claude skill that generates rigorous, structured user research interview guides from a research objective. Works with any product, team, or research domain.

Built for researchers, product managers, and designers who want to run better interviews — not just generate a list of questions, but design a conversation arc that surfaces real behavior and latent needs.

---

## What it does

Give it a research objective. It produces a complete, ready-to-run interview guide with:

- **Sub-research questions** mapped to the objective (with your approval before building)
- **Interview arc** — warm-up → baseline behavior → core research questions → optional concept response → close
- **Probing follow-ups** matched by type to each research question (behavioral reconstruction, workaround discovery, mental model probing, emotional impact, decision triggers, comparison, silence, artifact probes)
- **Rulebook review** — every question checked for leading language, double-barreled structure, assumed behaviors, and question length
- **Moderator notes** built in throughout

It also uses web search automatically when your context assets don't cover the research topic — so gaps in your docs trigger a search rather than a blind spot.

---

## Install

1. Download `user-research-guide.skill`
2. Double-click to install in Claude (Cowork or Claude Code)
3. Trigger with `/user-research-guide [your research objective]`

On first run, a setup wizard will walk you through loading your team's context. Takes about 2 minutes.

---

## First-time setup

When you install and trigger the skill for the first time, a setup wizard fires automatically. It asks what you have ready:

**Org / product context** — a product brief, PRD, one-pager, or any doc that describes your product and users. The skill uses this to frame interview questions around real user segments and active roadmap hypotheses.

**Research playbook** — your team's methods, recruiting approach, and synthesis process. Used to attach the right recruiting screener and synthesis template to each guide.

**Historical interview guides** — past guides you've run. The skill references the 1–2 most relevant to each new objective, so your guides build on prior work rather than starting from scratch every time. If you don't have past guides, the wizard can generate example templates from past research objectives you describe.

These assets are saved into the skill's own folder and persist permanently. You never have to re-upload them — just update them when things change.

---

## Every session

When you trigger the skill with a research objective, it opens a **multi-select asset picker**:

> Which reference assets should I load for this session?
> - 📋 Org & product context
> - 🔬 Research playbook
> - 🎯 Probing guide
> - 📏 Questioning rulebook
> - 📁 Historical guides
> - 🔄 I need to update an asset before starting

Pick what's relevant. For a quick draft, skip the historical guides. For a deep strategic study, load everything. The skill only loads what you select — keeping context lean and outputs focused.

---

## Updating your assets

Say anything like:
- *"update my org context"*
- *"my research playbook changed"*
- *"add a historical guide"*

The skill treats this as an update request, asks what to change, and overwrites the relevant file.

---

## What ships with the skill

Two types of assets are bundled:

**Universal assets** — ready to use immediately, no setup needed:

- **Probing guide** — 8 probing frameworks with patterns, examples, and a quick-reference table matching probe type to use case (behavioral reconstruction, workaround discovery, mental model probing, emotional impact, decision triggers, comparison, silence, artifact)
- **Questioning rulebook** — 10 rules for question quality: open before you close, behavior before attitude, no leading language, one question at a time, assume nothing, ladder for motivation, use the pause, probe for specificity, handle emotional topics carefully, keep questions short
- **Interview guide template** — the output structure used for every generated guide

**Team-specific slots** — empty on install, filled during setup:
- Org & product context
- Research playbook
- Historical guides folder

---

## Repo structure

```
user-research-guide.skill      # Install this
src/
└── user-research-guide/
    ├── SKILL.md               # Skill instructions
    └── references/
        ├── setup_status.md
        ├── org-product-context.md       # Placeholder
        ├── research-playbook.md         # Placeholder
        ├── probing-guide.md             # ✅ Universal
        ├── questioning-rulebook.md      # ✅ Universal
        ├── interview-guide-template.md  # ✅ Universal
        └── historical-guides/
            └── README.md               # Format guide
```

---

## Customising or forking

The `src/user-research-guide/` folder contains everything. To fork and pre-configure it for your team:

1. Edit `references/org-product-context.md` with your product context
2. Edit `references/research-playbook.md` with your methods and recruiting approach
3. Add historical guides to `references/historical-guides/` following the format in that folder's README
4. Update `references/setup_status.md` to `configured` so the setup wizard doesn't run on first load
5. Repackage using the [Claude skill packager](https://docs.claude.ai) or zip the folder with a `.skill` extension

This is how the Allrecipes pre-configured version in the `examples/` folder was built — same skill, same structure, assets filled in for a specific team.

---

## Examples

The `examples/` folder contains a pre-configured version for an Allrecipes-style recipe platform, showing what the skill looks like with all assets filled in:

- Org context with personas (weeknight cook, health-conscious planner, creator, bargain shopper)
- Research playbook with recruiting screeners and synthesis templates
- 5 historical interview guides covering menu planning, search & discovery, creator onboarding, shoppable recipes, and personalization

Useful as a reference for how to structure your own assets.

---

## Requirements

- Claude (Cowork or Claude Code)
- No external dependencies

---

## License

MIT
