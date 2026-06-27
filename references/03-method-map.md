# 03 · Method Map + Interview Guide (lenses · Mom Test · JTBD)

Two jobs: **(A) which lens is riskiest** (almost always viability at growth stage), and **(B) the
anti-flattery interview guide** `/kickoff` issues. Build the guide in the trigger language.

## A. The three lenses (IDEO / Tim Brown)

> Source: Tim Brown, "Design Thinking," *HBR* June 2008; *Change by Design* (2009); IDEO.org *Field Guide* (2015).

| Lens | The question | The growth-stage trap |
|------|--------------|------------------------|
| **Desirability** | Do they really want it? Painful enough? | "内测好评" is desirability theater — low retention says it's weaker than it looks |
| **Feasibility** | Can you build/deliver it? | You already shipped — usually the *least* risky lens now |
| **Viability** | Will they **pay**, for what, how much? | **The skipped one.** "一收费全员卸载" lives here. Pin 80% of the weight here. |

Name the single riskiest **falsifiable** assumption: a **who** + a **behavior** + a **threshold** —
"{segment} will {pay $X / do a measurable thing} to {outcome}". "People will love it" names none and can't fail.

## B. Method by stage (NN/g)

> Christian Rohrer, "When to Use Which UX Research Methods," NN/g — attitudinal↔behavioral × qual↔quant.
> Jakob Nielsen, "Why You Only Need to Test with 5 Users" (2000) — ~5 per segment ≈ 85% of qualitative signal.

```
Growth-stage (you HAVE seed users):
├─ "Will they pay / which price?"  → generative interviews weighted to past spend  [here + 04]
├─ "Why is activation dying?"      → superuser interviews + subtraction            [05]
└─ "Is the core need even real?"   → Mom Test discovery; if fake → pivot           [06]
```
Lock **5 deep qualitative interviews per segment**, then stop. More is its own 自嗨.

## C. The Mom Test interview guide (what `/kickoff` issues)

> Rob Fitzpatrick, *The Mom Test* (2013); Christensen/Ulwick JTBD. Get **truth**, not encouragement.

**Three rules at the top of every guide:** 1) talk about *their life*, not your idea; 2) ask about *specific
past behavior*, not the future ("when did you last…?" not "would you…?"); 3) talk less, listen more.

```markdown
# 访谈提纲 / Interview Guide — {segment}
## 0. 暖场 / Warm-up (2 min) — consent, "no right answers", NO pitch
## 1. 上次做这件事 / The last time (8 min)
   - 上次你 {做这个核心任务} 是什么时候？带我走一遍。/ Walk me through the last time you {did the job}.
   - 是什么触发的？还有谁/什么工具卷进来？/ What triggered it? Who/what else was involved?
## 2. 卡点 + 现在怎么凑合 / Struggle + current workaround (10 min)
   - 哪儿开始烦/难？你转头用了什么？/ Where did it get annoying? What did you do instead?
   - 现在拿什么顶着（多久一次，上次花了你多少时间/钱/机会）？← 行为证据
## 3. 花钱 + 承诺 / Spend & commitment (8 min) ← VIABILITY, do not skip
   - 你现在为解决这件事花钱买什么吗？多少？谁的预算？/ Do you pay for anything to solve this today? Whose budget?
   - 有没有试过解决然后放弃了——为什么？/ Ever tried to fix this and gave up — why?
## 4. 理想结果 / Desired outcome (5 min) — 如果完美解决，什么会变？怎么衡量"更好"？
## 5. (可选, 最后) 反应 / Reaction (LAST, 5 min) — "tear it apart"; watch for commitment vs polite praise
## 收尾 / Wrap — 还该找谁聊？(referral = mild commitment)
```

## D. Anti-flattery swaps (force these in every guide)

Strip polished-but-useless questions; replace with penetrating behavior-mining:

- ❌ "你希望这个 App 有什么功能？" / "What features do you expect?" → invites vanity
- ❌ "你愿意为这个功能付多少钱？" / "How much would you pay for this?" → a blank check
- 🎯 "你现在是怎么解决这个问题的？" / "How do you currently manage this problem?"
- 🎯 "你还试过什么别的？" / "What else have you tried?"
- 🎯 "上次为解决这事花钱是什么时候，花了多少？" / "When did you last pay for a solution, and how much?"

## E. Bias killers (NN/g)
No leading questions. No feature menus (ask what they *do*, infer the feature). Silence is a tool — let them fill it.
