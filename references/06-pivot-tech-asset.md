# 06 · Minimal-Tech-Asset Pivot (waste no working code)

Reached when `/diagnose` returns **转 / PIVOT**: the current need is fake, but the interviews surfaced a
painfully real one. The goal is an *elegant* pivot — keep the validated new need in front, and reach it by
reusing the maximum of what you already built. Don't trash the codebase; re-aim it.

> Sources: Eric Ries, *The Lean Startup* (2011) — the pivot taxonomy (zoom-in, customer-segment, platform,
> business-architecture, value-capture, etc.); Steve Blank, Customer Development — pivot = a substantive,
> tested change to one part of the model, not a restart.

## 1. Inventory the assets (what survives a pivot)

List what you actually have, independent of the dead use case:
- **Tech assets:** auth, billing, data pipeline, ML models, integrations, infra, a working mobile/web shell.
- **Distribution assets:** the seed-user list, a channel that works (e.g. 小红书 / Product Hunt), a community.
- **Insight assets:** the one painfully real need + the real pay-point you found in the interviews.

## 2. Name the pivot type (Ries)

Pick the smallest pivot that reaches the validated need:
- **Zoom-in:** one feature everyone actually used becomes the whole product.
- **Customer-segment:** same product, the people who'd *pay* are a different segment than you targeted.
- **Value-capture:** the thing works, the *pricing/who-pays model* was wrong (e.g. charge the company, not the user).
- **Platform / business-architecture:** app↔platform, or high-volume-low-margin ↔ low-volume-high-margin (higher ACV).

## 3. Map the real need onto existing assets

Draw the line explicitly: **new need → which existing asset serves it.** The best pivot is the one where the
new, higher-ACV scene is mostly *already built*. If reaching it needs a full rewrite, it's not a pivot — it's
a new company; flag that honestly.

## 4. Re-validate before re-building

A pivot is a new hypothesis, not a fact. Don't build it on faith:
- Write the new riskiest assumption back onto the dashboard and **run a fresh `/kickoff`** on it (5 interviews,
  past spend) before committing engineering.
- Reuse the distribution asset to recruit those interviews fast.

## 5. Output (into the diagnosis report)

- The new validated need + the chosen pivot type.
- The asset-reuse map (new need → existing code/asset), and the honest % that's reuse vs rebuild.
- The single next test that de-risks the pivot before you write new code.
