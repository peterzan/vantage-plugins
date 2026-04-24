<!-- SPDX-License-Identifier: Apache-2.0 -->
<!-- Copyright 2026 Peter Zan -->

# Vantage Plugins

**Critical thinking plugins for AI-generated output.**

Five open-source plugins that add reflective "why" layers to AI productivity tools. Philosophy, History, Psychology, Sociology, and Rhetoric — each examines a question from a different vantage point.

AI productivity plugins tell you *what to do*. Vantage helps you understand *why*.

---

## The Problem

AI plugins for finance, legal, engineering, and other domains produce sophisticated recommendations. But they answer "how" — how to structure a portfolio, how to review a contract, how to prioritize a roadmap. They don't ask:

- Should we do this at all?
- Has this worked before?
- Will people actually follow through?
- Who gains power and who loses it?
- How is the language shaping what we see and what we miss?

Those are the questions that determine whether a recommendation succeeds or fails in the real world. Vantage asks them.

## The Plugins

| Plugin | Prefix | Tools | Asks |
|--------|--------|-------|------|
| **Philosophy** | `phil_` | 13 | *Should we?* — Surfaces assumptions, examines ethics, tests first principles, challenges purpose alignment, traces who benefits, audits evidence quality |
| **History** | `hist_` | 12 | *Has this worked before?* — Finds precedents, maps trajectories, learns from failures, assesses timing |
| **Psychology** | `psych_` | 11 | *Will people actually do this?* — Identifies biases, motivation gaps, emotional barriers, adoption patterns |
| **Sociology** | `soc_` | 11 | *How does this affect communities and power?* — Analyzes power structures, inequality, institutional change, community impact, maps all affected stakeholders |
| **Rhetoric** | `rhet_` | 13 | *How is language shaping perception?* — Deconstructs framing, audits persuasion, detects euphemisms, maps accountability language, audits loyalty orientation |

**60 tools total** — 33 skills for deep analysis, 27 commands for quick checks.

## How They Work

Each plugin works in two modes:

**Standalone** — Ask a question directly. *"What are the hidden assumptions in this proposal?"* → `phil_assumptions` analyzes it.

**Meta-layer** — Run another plugin's output through Vantage. A finance plugin recommends rebalancing a portfolio → `psych_emotion` reveals the client's resistance is shame-driven, not rational → `hist_precedent` shows that high-income professionals who ignored similar advice faced predictable consequences → `rhet_accountability` catches that the AI recommendation says "is suggested" instead of "I recommend," shifting accountability away from the advisor.

The "how" plugins produce the recommendation. Vantage reveals whether it will actually work, who it affects, and what it's hiding.

## Fiduciary Awareness

When Vantage plugins encounter regulated professional domains — finance, legal, healthcare — they naturally surface accountability questions as part of their analysis:

- **Who retains the duty of care** when AI mediates professional advice?
- **Does the language assign or obscure responsibility** for the recommendation?
- **What happens to professional accountability** when judgment is delegated to algorithms?

This isn't a disclaimer appended to the output. It's baked into the analytical methodology — the plugins ask these questions because their frameworks (ethics, institutional analysis, accountability language) lead there organically.

The plugins don't override human judgment or make compliance decisions. They surface the accountability questions so that the human professional — the one who actually holds the duty of care - can address them. The AI provides the perspective. The human retains the responsibility.

Fiduciary awareness was designed into the plugins from day one, informed by research on AI's fiduciary gap in financial services and the broader question of professional duty of care in an AI-mediated world.

## Loyalty Audit

Building on the fiduciary awareness foundation, Vantage includes a dedicated loyalty audit capability distributed across three plugins:

- **`rhet_loyalty`** (Rhetoric) — Analyzes whether recommendation language is optimized for the user's outcome or the provider's liability protection. Different from `rhet_accountability` (which catches responsibility shifts). `rhet_loyalty` asks what the language is optimizing for.

- **`phil_cui_bono`** (Philosophy) — "Who benefits?" Traces the actual flow of benefits from a recommendation across financial, reputational, legal, data, and operational dimensions. Determines whether the stated beneficiary is the actual beneficiary.

- **`phil_epistemology`** (Philosophy) — Audits evidence quality behind claims. When output says "research shows" or "data indicates" — what research? How strong? Correlational or causal? Audits the knowledge claims themselves.

- **`soc_stakeholder_map`** (Sociology) — Maps all affected stakeholders including those excluded from consideration. Uses four-tier identification: primary, direct, ripple effect, and excluded.

- **`/loyalty_check`** (Command) — Rapid audit across all four dimensions. Produces GREEN/YELLOW/RED flags for language loyalty, beneficiary analysis, evidence quality, and stakeholder completeness.

The loyalty audit was designed to detect what the language is optimizing for — the person receiving the advice or the person giving it. It complements the existing accountability tools by asking not just "who owns this recommendation?" but "whose interests does this recommendation actually serve?"

## Structure

```
vantage-plugins/
├── LICENSE
├── README.md
├── philosophy/
│   ├── plugin.json
│   ├── skills/
│   │   ├── assumptions/SKILL.md
│   │   ├── cui_bono/SKILL.md
│   │   ├── dialectic/SKILL.md
│   │   ├── epistemology/SKILL.md
│   │   ├── ethics/SKILL.md
│   │   ├── first_principles/SKILL.md
│   │   ├── purpose/SKILL.md
│   │   └── reframe/SKILL.md
│   └── commands/
│       ├── assumptions_check.md
│       ├── ethics_check.md
│       ├── purpose_check.md
│       ├── reframe_quick.md
│       └── steelman.md
├── history/
│   ├── plugin.json
│   ├── skills/
│   │   ├── consequences/SKILL.md
│   │   ├── failure/SKILL.md
│   │   ├── precedent/SKILL.md
│   │   ├── rhyme/SKILL.md
│   │   ├── timing/SKILL.md
│   │   └── trajectory/SKILL.md
│   └── commands/
│       ├── failure_check.md
│       ├── lesson.md
│       ├── precedent_check.md
│       ├── rhyme_check.md
│       ├── timing_check.md
│       └── trajectory_check.md
├── psychology/
│   ├── plugin.json
│   ├── skills/
│   │   ├── adoption/SKILL.md
│   │   ├── bias/SKILL.md
│   │   ├── emotion/SKILL.md
│   │   ├── group/SKILL.md
│   │   ├── motivation/SKILL.md
│   │   └── narrative/SKILL.md
│   └── commands/
│       ├── adoption_check.md
│       ├── bias_check.md
│       ├── emotion_check.md
│       ├── motivation_check.md
│       └── narrative_check.md
├── sociology/
│   ├── plugin.json
│   ├── skills/
│   │   ├── community/SKILL.md
│   │   ├── diffusion/SKILL.md
│   │   ├── institutional/SKILL.md
│   │   ├── power/SKILL.md
│   │   ├── stakeholder_map/SKILL.md
│   │   └── stratification/SKILL.md
│   └── commands/
│       ├── community_check.md
│       ├── equity_check.md
│       ├── exclusion_check.md
│       ├── institution_check.md
│       └── power_check.md
└── rhetoric/
    ├── plugin.json
    ├── skills/
    │   ├── accountability/SKILL.md
    │   ├── audience/SKILL.md
    │   ├── euphemism/SKILL.md
    │   ├── framing/SKILL.md
    │   ├── loyalty/SKILL.md
    │   ├── narrative/SKILL.md
    │   └── persuasion/SKILL.md
    └── commands/
        ├── accountability_scan.md
        ├── frame_flip.md
        ├── loyalty_check.md
        ├── plain_language.md
        ├── rephrase_accountable.md
        └── spot_spin.md
```

## Skills vs. Commands

**Skills** are deep analysis tools with structured prompt templates. They walk through a multi-step methodology and produce comprehensive output. Use when you need thorough analysis.

**Commands** are quick interventions. They produce concise, focused output — a few sentences, a quick check, a fast reframe. Use when you need a rapid assessment.

Every skill has a corresponding command for its most common use case.

## Using with MCP

Each plugin includes a `plugin.json` that defines its skills, commands, and metadata. The plugins are designed for Model Context Protocol (MCP) servers but the skill templates work with any LLM — they're structured prompts in markdown.

To use a skill directly, open its `SKILL.md` file, replace `{{input_text}}` with your content, and send it to any model. The template handles the rest.

## Designed by Ensemble

These plugins were designed through a six-model AI ensemble — Claude, ChatGPT, Gemini, Llama, Mixtral, and Qwen — with each model contributing distinct capabilities to the design. The ensemble process ensured that no single model's biases dominated the plugin methodologies.

Key ensemble contributions include Gemini's `rhet_accountability` skill (the most directly fiduciary-relevant tool in the suite), Claude's command naming conventions, and cross-model validation of every prompt template.

## Complementary to Existing Plugins

Vantage is designed to work alongside domain-specific plugins, not replace them. It pairs naturally with productivity plugins for finance, legal, engineering, product management, marketing, and other domains.

The domain plugins handle the "how." Vantage adds the "why."

| Domain Plugin Output | Vantage Layer | What It Reveals |
|---------------------|---------------|-----------------|
| Portfolio recommendation | `psych_emotion` | Client's resistance is shame, not ignorance |
| Contract review | `soc_power` | Which party the contract language empowers |
| Product roadmap | `phil_assumptions` | Hidden assumptions about user behavior |
| Marketing campaign | `rhet_framing` | What the messaging highlights and what it hides |
| AI-generated advice | `rhet_accountability` | Whether the language assigns or avoids responsibility |

## License

Apache 2.0. See [LICENSE](LICENSE) for details.

Fork it. Extend it. Make it better. If you improve the fiduciary awareness methodology or add new analytical frameworks, contributions are welcome.

---

*Built by Peter Zan. Designed by a six-model AI ensemble. The plugins look at every question from a different vantage point — assessing the why, not just the how.*
