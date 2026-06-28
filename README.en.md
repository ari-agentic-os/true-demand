<!-- LANG-SWITCH -->

[简体中文](./README.md) · **English**

# 💊 The Willingness-to-Pay Wake-Up Call · true-demand

> A willingness-to-pay validation skill for builders · Claude Code / Codex / any AI tool.

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

And you already hold the hardest evidence: of 500 installs most only format locally, almost nobody clicks "sync" — that's real behavioral data (not opinions), and it's the loudest signal you have. Use it, don't re-ask it.

Don't flip the subscription switch blind. I've created three local files:
① dashboard_hypotheses.md — riskiest assumption "creators will pay $2/mo to kill the manual cross-posting pain," with pre-committed confirm/kill lines;
② guide_true_demand_interview.md — an icebreaker that asks a core author about their workflow + 5 behavioral probes that see past politeness;
③ plan_recruit_experiment.md — who to recruit, plus one behavioral experiment to run in parallel: a fake-door / pre-sell on "one-click sync" (click it → "$2/mo to unlock"), measured by real clicks and payment, not opinions.

Here's a classic reality-check probe:

❌ Don't ask: "If the sync feature gets stable later, would you subscribe at $2/mo to support it?" (Out of peer encouragement creators will say "cheap, happy to support" — then go blind the moment it's time to pay.)

✅ Do ask: "Last month, to get your content onto different platforms — or just to make it look good — what's the most expensive thing you actually spent money or time on? (A layout-tool VIP, a paid distribution app, hiring a part-time assistant?) Why was it worth it then? Does your current toolset already remove that cost?"

⏸️ Don't overreach on step one: from the 15 who "open it weekly but never sync," book ONE conversation first (scale once it works), and put the fake-door live in parallel. Set an implementation intention — e.g. "DM 3 people by Wednesday." Even one interview, one note, is enough to run /align and see where she's actually stuck.
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

Don't want to install? Paste the full `SKILL.md` into your chat, prefixed with: "Act as a steady, plain-spoken product advisor for a builder validating real willingness-to-pay (founder, solo dev, or PM), working strictly by the spec below," then paste the `SKILL.md` contents.

### Using it

- **Three entries:** Chinese — `/开局`, `/纠偏`, `/确诊`; English — `/kickoff`, `/align`, `/diagnose`. Type whichever language; it writes the matching files in that language (no Chinese-English salad).
  - **Claude Code:** use them as native commands, or just describe your situation to trigger implicitly.
  - **Codex:** invoke via the `/skills` menu, a `$true-demand` mention, or by describing your situation (the description match triggers it implicitly); typing `/kickoff`-style verbs also works. With no clear language verb, the skill asks once which language to use.
- **De-AI gate (optional dependency):** if `humanizer-zh` (Chinese) / `tool-humanizer` (English) are installed, output is de-AI'd before saving; without them it still works (the skill self-edits for a natural voice).

---

## ⚡ Three core commands (bilingual mirror, file-persisted)

Real demand validation usually drags across weeks and several interviews, so it drops the "grind it out in one chat window" model for three hard, independently-triggerable, locally-persisted actions — and strings every round into a loop:

### 🚀 `/开局` · `/kickoff` — diagnose now, hand over the guide
- **When:** your MVP has beta users, but activation is low, no one wants to pay, or the roadmap is a fog.
- **What it does:** ⓪ **Read what you already have first** — if your repo has a PRD / docs / prototype **(and any data — retention/tickets/payments)**, it scans them and extracts the implicit assumptions (as hypotheses to test, not findings), asks only the gaps, and reads your shape (pre-MVP/growth-stage · B2C/B2B) to adapt; ① **See past the surface risk** — pull attention off "usability" back onto the dodged lens, "viability"; ② **Persist locally** — the validation dashboard `dashboard_hypotheses.md` + an anti-flattery Mom Test guide `guide_true_demand_interview.md` + an **action plan** (recruiting list + one behavioral experiment) `plan_recruit_experiment.md`.
- **⏸️ Default stop — start tiny:** talk to ONE person first (not 5), run the experiment in parallel, and one note is enough to come back to `/align`. After diagnose it opens the next round, until you're confidently building or you drop.

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
├── dashboard_hypotheses.md         # riskiest assumption · confirm/kill lines · who pays · validation log
├── guide_true_demand_interview.md  # de-AI'd qualitative Mom Test script
├── plan_recruit_experiment.md      # recruiting plan + one behavioral experiment
├── report_final_diagnosis.md       # affinity clusters · build/pivot/drop · confidence
└── interview_notes/                # your raw notes
```

---

## 🧠 The methodology underneath (not just interviews: eats data · tests real behavior · loops)

The talk is plain; the engine strictly executes the gold standard — and it doesn't just *ask*: it ingests the real data you already have, runs real behavioral experiments in parallel, and loops every round.

| Dimension | Methodology | The gate it enforces |
|---|---|---|
| Reuse&nbsp;existing&nbsp;data | Evidence ladder + triangulation (Ries 2011 · Lincoln & Guba 1985) | Scan the PRD/prototype and ingest real retention/funnel/tickets/payment data as the hardest evidence (ladder rung 5–6); don't re-ask what the data already answers |
| Commercial&nbsp;red-line | IDEO three lenses | `/kickoff` pins 80% weight on viability, cuts usability vanity |
| Anti-flattery&nbsp;+&nbsp;motive | The Mom Test · JTBD | Filters future-intent pleasantries for real past behavior; unpacks the social/emotional pain + switching resistance |
| Real-behavior&nbsp;test | Behavioral experiments + evidence ladder (Ries 2011) | Every interview round runs one pre-sell / fake-door / payment test in parallel — a real charge outranks any stated intent |
| Shape&nbsp;triage | Stage × buyer triage (Blank customer development) | pre-MVP/growth-stage · B2C/B2B each get a different playbook; for B2B, user ≠ champion ≠ budget owner |
| Signal&nbsp;convergence | Thematic saturation / information power (Guest 2006 · Malterud 2016) | Interview per segment until no new themes (~6 to start, ~12 cap); Nielsen's "5" is usability-only, not demand/pricing |
| Clean&nbsp;the&nbsp;inputs | 4-field capture + Ladder of Inference (Argyris · Mom Test) | Split DID/SAID/COMMITTED/MY READ; audit whether the interviewer led or pitched before trusting a note — did > said |
| Pricing&nbsp;breakthrough | Van Westendorp PSM | A price band that won't churn your beta fans |
| Roadmap&nbsp;fog | Teresa Torres OST | Messy notes → goal-opportunity-solution-experiment |
| Rescue&nbsp;activation | Superhuman core-path subtraction | Subtract features via superuser feedback to rescue low activation |
| Code&nbsp;redemption | Minimal-tech-asset pivot | Waste no old code; re-aim it at a higher-ACV scene |
| Pre-set&nbsp;the&nbsp;decision | Confirm/kill line + confidence band | Commit the confirm/kill line before the data; score confidence by saturation × behavioral × cross-segment — never Build on stated-only |
| Tiny&nbsp;first&nbsp;step | Implementation intentions + Tiny Habits (Gollwitzer · Fogg) | Default to ONE conversation + "DM 3 by Wednesday" — cross the kickoff→first-interview drop-off |
| Loop | Build-Measure-Learn (Ries 2011) | `/diagnose` closes one round, logs it, names the next-riskiest assumption, re-opens `/kickoff` |

Design rationale + "how to validate the skill itself": [`ABOUT.md`](./ABOUT.md).

---

## License

MIT — see [`LICENSE`](./LICENSE).
