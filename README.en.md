<!-- LANG-SWITCH --> [简体中文](./README.md) · **English**

# 💊 The Willingness-to-Pay Wake-Up Call · true-demand  <sub>for growth-stage founders</sub>

> Cure your MVP from the **"everyone loves it until it's time to pay"** syndrome.
> It reads the truth out of your users' **bills**, not their compliments.

A skill for [Claude Code](https://claude.com/claude-code) / Agentic OS, built for founders who **already have
seed users but stalled**: low activation, can't charge, unsure whether to add features or pivot. It's steady,
jargon-free, and doesn't flatter. It drags your attention off "is it usable" and onto the lens almost nobody
tests — **viability (will they actually pay)**.

## The problem it solves

The real danger at growth stage isn't no users — it's **vanity traction**: "求内测" sign-ups, Product Hunt
upvotes, low-friction compliments. High downloads + dying activation usually means you're trapped in a
feature-building echo chamber — and the real cause of death only shows up the moment you charge.

Core axiom: **say ≠ do, and most people test only "say."**

## Three core commands (bilingual mirror, file-persisted)

It drops the "grind in one chat window" model for three hard, independently-triggerable, locally-persisted
actions. Type whichever language; it writes the matching files in that language:

| 中文 | English | What it does | Output |
|---|---|---|---|
| **`/开局`** | **`/kickoff`** | Diagnose now, pin the biggest commercial risk, issue an anti-flattery guide, then step off | dashboard + interview guide |
| **`/纠偏`** | **`/align`** | Mid-research: drop in notes, pierce the subtext, kill false positives | interactive in chat |
| **`/确诊`** | **`/diagnose`** | After 5 interviews, synthesize all notes → a build/pivot/drop call | final diagnosis report |

Full workflow: [`docs/运作流程.en.md`](./docs/运作流程.en.md).

## The eight methodologies underneath

The talk is plain; the engine strictly executes the gold standard:

| Dimension | Methodology | The gate it enforces |
|---|---|---|
| Commercial red-line | IDEO three lenses | `/kickoff` pins 80% weight on viability, cuts usability vanity |
| Anti-flattery lie test | The Mom Test | Filters future-intent pleasantries; forces real past behavior |
| Deep-motive mining | JTBD | Unpacks the social/emotional pain + switching resistance |
| Pricing breakthrough | Van Westendorp PSM | A price band that won't churn your beta fans |
| Signal convergence | Nielsen's 5-user law | 5 deep interviews ≈ 85% saturation → ends endless research |
| Roadmap fog | Teresa Torres OST | Messy notes → goal-opportunity-solution-experiment |
| Rescue activation | Superhuman core-path subtraction | Subtract features via superuser feedback |
| Code redemption | Minimal-tech-asset pivot | Waste no old code; re-aim it at a higher-ACV scene |

Design rationale + "how to validate the skill itself": [`ABOUT.md`](./ABOUT.md).

## Local file architecture

```text
projects/true-demand/{Date}_{Project_Name}/
├── dashboard_hypotheses.md         # riskiest assumption · who pays · the decision
├── guide_true_demand_interview.md  # hand-de-AI'd qualitative Mom Test script
├── report_final_diagnosis.md       # affinity clusters + build/pivot/drop
└── interview_notes/                # your 5 raw notes
```

## Install

Drop this repo into `.claude/skills/true-demand/`. The skill loads `references/` on demand. Chinese output
runs through `humanizer-zh`, English through `tool-humanizer`. Optional: `mkt-icp`, `mkt-positioning`.

## License

MIT — see [`LICENSE`](./LICENSE).
