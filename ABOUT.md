# true-demand — what it is, how it's built, why it's defensible

> Design notes for `付费意愿清醒剂 / The Willingness-to-Pay Wake-Up Call`. For the runtime spec see
> `SKILL.md`; for the user-facing flow see `docs/运作流程.zh.md` / `.en.md`.

## 1. The problem

Growth-stage founders already shipped an MVP and have seed users — and then stall: activation dies, charging
freezes them, the roadmap fogs. They run the *wrong* test (ask friends "do you like it?", get a polite yes),
mistake vanity traction (sign-ups, upvotes) for demand, and discover the truth only when they charge and
everyone churns. One idea drives the whole design: **say ≠ do, and people test only "say."** This skill reads
the **bill**, not the compliment.

## 2. Who it's for

Founders/solo builders **post-MVP, pre-revenue-confidence** — not trained researchers. A researcher knows a
usability test from a demand test; a founder doesn't. The skill carries that judgment and pins the riskiest
lens (almost always **viability**) for them.

## 3. Why three commands instead of one chat

Real validation runs over **weeks**, not one session. So the skill is three file-persisted modes, each
triggerable on its own, sharing a local dashboard:

- **`/开局 /kickoff`** — diagnose + issue the interview guide, then *stop* (hand the stage to the user).
- **`/纠偏 /align`** — mid-research debrief; translate subtext, rule out false positives, fix the next interview.
- **`/确诊 /diagnose`** — cross-file synthesis → build / pivot / drop.

Context lives in `projects/true-demand/{date}_{project}/`, not in a chat window — so a multi-week study survives.

## 4. Bilingual by design

The command's language is the language selector. Chinese commands → Chinese files + a 沉稳靠谱 advisor voice,
de-AI'd via `humanizer-zh`. English commands → English files + an Indie-Hacker / product-advisor voice, de-AI'd
via `tool-humanizer`. Never mixed in one file.

## 5. The methodology underneath (and what each prevents)

It doesn't just *ask* — it ingests the data you already have, runs real behavioral experiments in parallel, gates the decision, and loops.

| # | Methodology | Source | What it stops |
|---|-------------|--------|---------------|
| 1 | Evidence ladder + triangulation | Eric Ries 2011; Lincoln & Guba 1985 | Re-asking what your own usage/payment data already proves; single-source confidence |
| 2 | IDEO three lenses (desirability/feasibility/viability) | Tim Brown, *HBR* 2008; *Change by Design* 2009 | Testing the easy lens; anchors viability |
| 3 | The Mom Test | Rob Fitzpatrick, 2013 | Pitch-y questions → false positives |
| 4 | Jobs To Be Done | Christensen, *HBR* 2016; Ulwick | Feature talk instead of the real job |
| 5 | Behavioral experiments (pre-sell / fake-door / smoke test) | Eric Ries 2011; Cohen 1988 | Trusting opinions over a real action / a real charge |
| 6 | Stage × buyer triage | Steve Blank (customer development) | One-size advice; in B2B, payer ≠ user ≠ champion |
| 7 | Thematic saturation / information power | Guest 2006; Hennink 2022; Malterud 2016 | Endless research — or stopping too early; Nielsen's "5" misapplied to demand |
| 8 | Van Westendorp PSM | van Westendorp, 1976 | Guessing price; "would you pay?" theater |
| 9 | Opportunity-Solution Tree | Teresa Torres, 2021 | Roadmap untethered from validated needs |
| 10 | Core-path subtraction + PMF survey | Rahul Vohra (Superhuman); Sean Ellis | Adding features when you should subtract |
| 11 | Minimal-tech-asset pivot | Eric Ries 2011; Steve Blank | Trashing working code on a pivot |
| 12 | 4-field capture + Ladder of Inference | Chris Argyris; Fitzpatrick 2013 | Blending fact, quote, commitment, and your own read |
| 13 | Pre-committed confirm/kill line + confidence band | RAT / pre-registration practice | Moving the goalposts after the data lands |
| 14 | Implementation intentions + Tiny Habits | Gollwitzer 1999; BJ Fogg 2019 | The kickoff→first-interview drop-off |
| 15 | Build-Measure-Learn loop | Eric Ries 2011 | Treating one round as the whole answer |

Nothing here is homemade — which is what lets the output survive a skeptical investor's "says who?".

## 6. How to validate the skill itself

Judge it the way it judges a product. "It reads well" is desirability theater. The real test is behavioral:
does it (a) pin **viability** when the user drifts to features, (b) refuse to accept unfalsifiable answers,
(c) *stop* after issuing the guide rather than over-producing, (d) call **drop** when the evidence says drop?
If it reaches for a usability test when the open question is "will anyone pay," it failed its own core rule.
Run it 5× on the same brief and check for consistent diagnosis (predictability is part of "good").

## 7. Boundaries

Not for production code, UI/visual design (`impeccable`/`viz`), brand voice (`mkt-brand-voice`), or marketing
copy. It decides *what to test and whether people will pay* — and hands you the guide to go find out.
