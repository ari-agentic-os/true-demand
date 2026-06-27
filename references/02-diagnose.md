# 02 · Diagnose （`/确诊` `/diagnose`） — cross-file synthesis & the call

The endgame. The founder talked to ~5 users; notes are piling up. Read **every** file under
`访谈笔记/` / `interview_notes/`, plus the dashboard, and turn the pile into one decision. Output language =
trigger language. Raw notes don't de-risk anything; a decision does.

## 1. Affinity-map the signal

Pull verbatim observations (behaviors, pains, workarounds, real spend, emotion) onto cards; cluster into
themes; name each. Count how many of the 5 hit each theme — frequency × intensity = priority. Keep the
verbatims attached: they are the evidence and the persuasion.

## 2. Did vs Said (carry the verdicts from `/align`)

Behavioral evidence outranks attitudinal. Any theme that's all "said," no "did," is unvalidated and cannot
support a Build call.

## 3. Opportunity-Solution Tree

> Source: Teresa Torres, *Continuous Discovery Habits* (2021).
Outcome (the business goal) → opportunities (the validated unmet needs) → solution ideas → experiments. This
keeps the roadmap tethered to real needs and de-fogs "what to build next."

## 4. Viability read

- **Who pays · model · price band** — from `04-pricing-psm.md`. If no one ever paid and there's no budget owner, that's the headline.
- **Activation/retention** — if usage is dying, the wound may be too many features, not too few. Pull `05-superhuman-subtraction.md`.

## 5. The call — against the pre-committed lines (not a vibe)

Judge each hypothesis against the **confirm/kill line set at kickoff** (on the dashboard), not a line invented
now. Tie the verdict to the gate and attach a **confidence** — never call BUILD on stated-only evidence or
before saturation (`03` §B); say "not enough signal yet, here's the gap" instead.

| Verdict | Gate |
|---|---|
| **做 / BUILD** | confirm-line met **and** enough of the segment show real behavior/commitment (ladder ≥4, `08`/`10`). Type bar: B2C = a count with real past-spend · B2B = ≥1–2 signed LOI/paid pilot · pricing/PMF = Ellis ≥40% with enough n. → ship the top OST branch first |
| **转 / PIVOT** | current need hit its kill-line, but a different painfully-real need + pay-signal surfaced → `06-pivot-tech-asset.md` (reuse code, don't trash the build) |
| **弃 / DROP** | kill-line hit, no pay-path, **after** saturation → cut losses, free the time. A win, not a failure |

**Confidence = f(** saturation reached? `03` · behavioral-not-said? `10` · consistent across segment **)** → 低/中/高.

```markdown
# 报告_终局确诊 / Final Diagnosis — {project}
## 结论 / Verdict: 做 BUILD | 转 PIVOT | 弃 DROP
## 置信度 / Confidence: 低/中/高 — saturation {到/未到} · evidence {behavioral/said} · cross-segment {一致/不一致}
## 为什么 / Why (top 3 evidence-backed reasons, with verbatims)
## 守住/崩了 / Held vs broke (each hypothesis vs its pre-committed confirm/kill line)
## 付费可行性 / Viability: who pays · model · price band · confidence (behavioral > stated)
## 下一步 / Next: the single move that most reduces remaining risk
```

Save the report (run through `humanizer-zh` / `tool-humanizer` first if installed, else self-edit). Show the absolute path.

> Sources: Osterwalder, *Value Proposition Design* (2014); Torres (2021); Sean Ellis PMF signal (≥40% "very
> disappointed" — only meaningful once there's real usage).
