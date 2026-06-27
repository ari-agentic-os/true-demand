<!-- LANG-SWITCH -->

[简体中文](./README.md) · **English**

# 💊 The Willingness-to-Pay Wake-Up Call · true-demand

> **For growth-stage founders** · a real willingness-to-pay validation skill, built for Claude Code.

Your MVP already landed its first seed users — then you hit a wall: activation is dying? You freeze the moment charging comes up? Can't tell whether to add features or pivot?

This skill (internal name `true-demand`) exists to cure the **growth-stage echo-chamber** — it reads the truth out of your seed users' **bills**, not their compliments. It pulls your attention off "is it usable" and back onto the line almost nobody tests — **viability: will they actually pay for this**.

---

## 🎬 The 1-second feel: End-to-End Example

> 💡 Plenty of early projects die of "self-applause." Here's how this Skill helps you sober up fast:

```text
User:
/kickoff I built a browser extension for indie creators — "multi-platform formatting + one-click cross-posting." I ran a beta on a couple of creator communities, and 500+ bloggers (people who write on Xiaohongshu, newsletters, etc.) left their emails and got the beta build. But here's the thing: after installing, most people only use it for "local formatting / making posts look nice" — almost nobody actually clicks the core "one-click sync to every platform" feature (activation is very low). Next month I want to charge $2/mo. Will it just die on arrival? How do I test this?

AI (true-demand):
500 creator emails is a classic "effort-cost illusion." Creators have a natural urge to try anything that "makes their layout prettier" — leaving an email is just a cheap tool-bet on "writing a hit." The fact that they "format but don't sync" tells me you may have built a low-frequency real need (cross-platform distribution) as a high-frequency sidekick (a local beautifier).

Don't flip the subscription switch blind. I've created your validation dashboard locally at dashboard_hypotheses.md.
The make-or-break question here is: "Are these creators looking for a free 'pretty editor,' or will they actually pay $2/mo to end the pain of manually copy-pasting and reformatting across platforms?"

For their current fake-fan state — treating a productivity tool as a free beautify template — I've tailored a guide_true_demand_interview.md (saved locally): an icebreaker that asks a core author about their workflow, plus 5 behavioral probes built to see past creator politeness.

Here's a classic reality-check probe:

❌ Don't ask: "If the sync feature gets stable later, would you subscribe at $2/mo to support it?" (Out of peer encouragement creators will say "cheap, happy to support" — then go blind the moment it's time to pay.)

✅ Do ask: "Last month, to get your content onto different platforms — or just to make it look good — what's the most expensive thing you actually spent money or time on? (A layout-tool VIP, a paid distribution app, hiring a part-time assistant?) Why was it worth it then? Does your current toolset already remove that cost?"

⏸️ Your bottleneck now is booking 3–5 of them. From those 500, pull the 15 who "open the extension weekly but never touch sync," and use the invite I saved to set up calls. Once you've got their real gripes about "why I'd rather copy by hand than click sync," drop them in — we'll run /align to find exactly where their real workflow pain is stuck.
```

---

## 🛠️ Install & quick start

This skill is pure Markdown (`SKILL.md` + `references/`), **compatible with both [Claude Code](https://claude.com/claude-code) and Codex**, and runs with zero dependencies.

### Method 1 — Git clone (recommended)

```bash
git clone https://github.com/ari-agentic-os/true-demand.git
```

Rename the folder to `true-demand` and drop it into your tool's skills directory:

| Tool | Path |
|---|---|
| Claude Code | `~/.claude/skills/true-demand` |
| Codex (macOS / Linux) | `$CODEX_HOME/skills/true-demand` (default `~/.codex/skills/true-demand`) |
| Codex (Windows) | `C:\Users\<username>\.codex\skills\true-demand` |

**Restart your session** and the skill will be picked up.

### Method 2 — ZIP download

On GitHub click `Code → Download ZIP`, unzip, rename the folder to `true-demand`, drop it in the path above, and restart.

### Method 3 — Paste the prompt (any AI tool, zero install)

Don't want to install? Paste the full `SKILL.md` into your chat, prefixed with: "Act as a steady, plain-spoken product advisor for a growth-stage founder, working strictly by the spec below," then paste the `SKILL.md` contents.

### Using it

- **Three entries:** Chinese — `/开局`, `/纠偏`, `/确诊`; English — `/kickoff`, `/align`, `/diagnose`. Type whichever language; it writes the matching files in that language (no Chinese-English salad).
  - **Claude Code:** use them as native commands, or just describe your situation to trigger implicitly.
  - **Codex:** invoke via the `/skills` menu, a `$true-demand` mention, or by describing your situation (the description match triggers it implicitly); typing `/kickoff`-style verbs also works. With no clear language verb, the skill asks once which language to use.
- **De-AI gate (optional dependency):** if `humanizer-zh` (Chinese) / `tool-humanizer` (English) are installed, output is de-AI'd before saving; without them it still works (the skill self-edits for a natural voice).

---

## ⚡ Three core commands (bilingual mirror, file-persisted)

To fit the half-month-to-a-month research cadence of a growth-stage founder, it drops the "grind it out in one chat window" model for three hard, independently-triggerable, locally-persisted actions:

### 🚀 `/开局` · `/kickoff` — diagnose now, hand over the guide
- **When:** your MVP has beta users, but activation is low, no one wants to pay, or the roadmap is a fog.
- **What it does:** ① **See past the surface risk** — pull attention off "usability" back onto the dodged lens, "viability"; ② **Persist context locally** — auto-creates the validation dashboard `dashboard_hypotheses.md`; ③ **Issue a plain-spoken guide** — outputs a hand-de-AI'd Mom Test script `guide_true_demand_interview.md` you can take straight to users.
- **⏸️ Default stop:** the AI steps off here and hands you the stage — go talk to 5 real users with the guide.

### 🎯 `/纠偏` · `/align` — debrief & translate the subtext
- **When:** mid-research, when you feel "they're just being polite" or "I'm not sure."
- **What it does:** plays your outside advisor. You drop in raw notes/transcripts; it reads the subtext objectively — e.g. "I'd buy if my company expensed it" really means *dodging out-of-pocket*, the budget owner isn't them; or it spots that they happily pay big for something else, opening a new pay-point; and it fixes your next interview's posture so false positives don't fool you.

### 🏁 `/确诊` · `/diagnose` — cross-file synthesis & strategic pivot
- **When:** you've talked to 5 real users and you're sitting on a pile of messy notes.
- **What it does:** reads every record under `interview_notes/`, clusters real pay-signals and high-value pains with affinity mapping, runs the Opportunity-Solution Tree (Torres), and hands you a `report_final_diagnosis.md`: **Build** (pay-path works → ship the roadmap) · **Pivot** (current need is fake, but a real one surfaced → reuse tech assets to pivot elegantly) · **Drop** (fully falsified → cut losses).

Full workflow: [`docs/运作流程.en.md`](./docs/运作流程.en.md).

---

## 📂 Local file architecture

```text
projects/true-demand/{Date}_{Project_Name}/
├── dashboard_hypotheses.md         # riskiest assumption · who pays · the decision
├── guide_true_demand_interview.md  # hand-de-AI'd qualitative Mom Test script
├── report_final_diagnosis.md       # affinity clusters + build/pivot/drop
└── interview_notes/                # your 5 raw notes
```

---

## 🧠 The eight methodologies underneath

The talk is plain; the engine strictly executes the gold standard:

| Dimension | Methodology | The gate it enforces |
|---|---|---|
| Commercial&nbsp;red-line | IDEO three lenses | `/kickoff` pins 80% weight on viability, cuts usability vanity |
| Anti-flattery&nbsp;check | The Mom Test | Filters future-intent pleasantries; surfaces real past behavior |
| Deep-motive&nbsp;mining | JTBD | Unpacks the social/emotional pain + switching resistance |
| Pricing&nbsp;breakthrough | Van Westendorp PSM | A price band that won't churn your beta fans |
| Signal&nbsp;convergence | Nielsen's 5-user law | 5 deep interviews ≈ 85% saturation → ends endless research |
| Roadmap&nbsp;fog | Teresa Torres OST | Messy notes → goal-opportunity-solution-experiment |
| Rescue&nbsp;activation | Superhuman core-path subtraction | Subtract features via superuser feedback |
| Code&nbsp;redemption | Minimal-tech-asset pivot | Waste no old code; re-aim it at a higher-ACV scene |

Design rationale + "how to validate the skill itself": [`ABOUT.md`](./ABOUT.md).

---

## License

MIT — see [`LICENSE`](./LICENSE).
