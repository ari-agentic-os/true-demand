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

## 5. The call (always end here)

```markdown
# 报告_终局确诊 / Final Diagnosis — {project}
## 结论 / Verdict: 做 BUILD | 转 PIVOT | 弃 DROP
## 为什么 / Why (top 3 evidence-backed reasons, with verbatims)
## 守住/崩了 / Held vs broke (per hypothesis on the dashboard)
## 付费可行性 / Viability: who pays · model · price band · confidence (behavioral > stated)
## 下一步 / Next: the single move that most reduces remaining risk
```

- **做 / BUILD** — pain clear + a pay-path that holds → ship the roadmap (top OST branch first).
- **转 / PIVOT** — the current need is fake, but a bleeding-real one surfaced → go to `06-pivot-tech-asset.md`
  and reuse existing code into the new, higher-ACV scene. Don't trash the build.
- **弃 / DROP** — falsified, no pay-path → cut losses, free the time for the next idea. This is a win, not a failure.

Save the report (run through `humanizer-zh` / `tool-humanizer` first). Show the absolute path. Offer to push
confirmed items to the `ops-design-loop` tracker.

> Sources: Osterwalder, *Value Proposition Design* (2014); Torres (2021); Sean Ellis PMF signal (≥40% "very
> disappointed" — only meaningful once there's real usage).
