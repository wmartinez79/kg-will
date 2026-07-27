---
tags:
  - finance
  - debts
  - analysis
---

# Debt Payoff Analysis

Prepared 2026-07-25 (see [[Debt Payoff Analysis 2026-07-25.pdf|source PDF]]). Total debt (consolidated USD): **$85,951.21** — Loans $45,000.08 (8 open) + Credit Cards $13,848.96 USD + NIO 992,598.11 (≈$27,102.17 @ 36.6243 BCN rate).

## Method
Hybrid **avalanche** (highest interest rate first) with a **quick-win sweep** up front: near-zero balances get cleared immediately regardless of rate — costs almost nothing, frees up minimum-payment cash flow right away, drops open accounts fast. After the sweep, strict avalanche by real/estimated APR. This tiering applies to *extra/discretionary* paydown — minimum payments on every open account still go out on schedule regardless of tier (see [[Credit Cards]] Payment Plan for the current cycle's minimums).

## Rates used
| Debt | Rate | Confidence |
|---|---|---|
| BAC credit cards (PriceSmart, AMEX Black, Visa) — NIO balance | 45% | confirmed |
| Ficohsa credit card — NIO balance | 39% | confirmed |
| Lafise credit card — NIO balance | 35% | confirmed |
| AVANZ loan (wife) | ~23.3% | estimated from implied monthly rate (~1.94%/mo) |
| Ficohsa loan 0000044006 | 18.62% | confirmed — biggest single loan by balance |
| Ficohsa loan 2211 | ~20% (unclear) | estimated; $4 gap in capital calc unexplained |
| BAC credit cards — USD balance | 20.04% | confirmed |
| Ficohsa credit card — USD balance | 19.8% | confirmed |
| Lafise credit card — USD balance | 19% | confirmed |
| BAC loans 007989181 / 010255001 / 011195771 | 16.2% (011195771: 16.92%) | confirmed |
| BAC loan 008781001 | 16.2% | confirmed (lowest balance, swept early regardless) |
| BAC car loan (wife) | 10.5% | confirmed — cheapest debt held |

## Payoff order

**Tier 0 — Quick-win sweep** (do immediately, in parallel with everything below)
1. BAC Visa CC (USD) — $100.03 @ 20.04% — near zero, clear it
2. BAC loan 008781001 — $297.70 @ 16.2% — lowest-balance loan, frees $112.71/mo minimum

**Tier 1 — Top priority: AVANZ (family agreement) + worst-rate NIO credit cards**
3. AVANZ loan (wife) — $7,031.67 @ ~23.3% est. — elevated to Tier 1 by family agreement, not rate — in progress, continue
4. BAC PriceSmart CC (NIO) — NIO 102,658.88 / $2,803.03 @ 45% — smallest of the three BAC NIO balances
5. BAC Visa CC (NIO) — NIO 170,161.18 / $4,646.13 @ 45%
6. BAC AMEX Black CC (NIO) — NIO 264,281.86 / $7,216.02 @ 45% — largest BAC NIO balance
7. Ficohsa CC (NIO) — NIO 311,917.34 / $8,516.68 @ 39% — largest single card balance overall
8. Lafise CC (NIO) — NIO 143,578.85 / $3,920.32 @ 35% — lowest rate in tier, kept last per strict avalanche (considered moving earlier for a quick win, reverted — costs more interest overall)

**Tier 2 — ~18.6–20% band** (ordered by rate, confirmed rates take precedence over estimates)
9. Ficohsa loan 2211 — $5,983.59 @ ~20% unclear — confirm with Ficohsa, $4 gap unexplained
10. BAC AMEX Black CC (USD) — $4,774.47 @ 20.04%
11. Ficohsa CC (USD) — $4,616.62 @ 19.8%
12. Lafise CC (USD) — $4,357.73 @ 19%
13. Ficohsa loan 0000044006 — $15,338.11 @ 18.62% — confirmed lower than earlier estimate (20.3%), drops to bottom of tier despite being biggest single loan; frees $565.28/mo minimum when done

**Tier 3 — BAC installment loans** (rate gap negligible, ordered smallest balance first)
14. BAC loan 007989181 — $1,801.44 @ 16.2% — smallest balance, quick win
15. BAC loan 010255001 — $3,414.28 @ 16.2%
16. BAC loan 011195771 — $6,623.61 @ 16.92% — largest of the three, slightly higher rate too

**Tier 4 — Cheapest debt held** (minimum payment only, no extra here)
17. BAC car loan (wife) — $4,509.68 @ 10.5% — lowest confirmed rate of all debts, don't overpay this one

USD column converts NIO balances @ 36.6243 (BCN official rate); USD-denominated debts repeat the same figure.

## Key takeaways
- The three BAC NIO credit-card balances (45% APR) are the single worst debt held — worse than AVANZ, worse than any loan.
- Ficohsa (39%) and Lafise (35%) NIO card balances also beat AVANZ's estimated rate.
- AVANZ is elevated to Tier 1 by family agreement, not by rate — stays top-priority alongside the NIO card balances even though its ~23.3% est. rate is below all three NIO card rates.
- BAC car loan (10.5%, wife's) is the cheapest debt on the books — minimum payments only, don't send extra cash here while higher-rate debt exists.
- Ficohsa loan 0000044006's confirmed rate (18.62%) came in lower than the earlier estimate — biggest loan balance ($15,338.11) but drops to bottom of the ~19-20% tier.
- Ficohsa loan 2211's exact rate is unclear ($4/mo gap between due amount and calculated capital reduction, unexplained) — worth a call to Ficohsa to confirm before treating it as tied with the ~20% cluster.
- BAC PriceSmart CC's residual $0.11 USD balance was bonificable interest, waived after full USD debt paid — dropped from the sweep, no longer an action item.

## Current Payment Plan (as of 2026-07-26)
| Date | Action | Amount | Source |
|---|---|---|---|
| 2026-08-01 (Sat) | Ficohsa min payment (USD) | $234.43 | EPS income |
| 2026-08-01 (Sat) | Ficohsa min payment (NIO, partial) | NIO 5,000.00 (of 20,218.46 min due) | EPS income |
| 2026-08-01 (Sat) | Visa current debt (USD), paid in full | $100.03 | cash on hand |
| 2026-08-08 (Sat) | Ficohsa min payment (NIO, remainder) | NIO 15,218.46 | EPS income |
| 2026-08-08 (Sat) | Visa — pay down accumulated charges from the week | TBD (accrues 08/01–08/08) | EPS income |
| 2026-07-27 (Mon) | BAC loan 008781001 (Tier 0 #2, $297.70 @ 16.2%), extra paydown | $120.00 | [[Taller Instalaciones Martinez]] income |

Notes:
- Ficohsa min payment due date is 2026-08-11; plan front-loads it across two Saturdays since Will's cash flow runs on the biweekly EPS cycle.
- Going forward, BAC Visa is the primary card for day-to-day personal/family expenses (Will's wife and two older children hold additional cards on the same Visa account) — Visa balance will keep accumulating between EPS paydays and needs a standing payoff step each cycle.

### Review against tier strategy
- **Visa USD payoff (08-01, $100.03) is exactly right** — it's Tier 0 item #1, the quick-win sweep. Good execution, zero conflict with strategy.
- **Ficohsa min payments (both legs) are mandatory upkeep, not discretionary paydown** — correct to send only the minimum here. Ficohsa CC sits at Tier 1 #7 (NIO) and Tier 2 #11 (USD), both behind AVANZ and the three BAC NIO cards; no extra cash should go to Ficohsa beyond the minimum until those higher-tier items are cleared.
- **Tier 0 item #2 (BAC loan 008781001, $297.70 @ 16.2%) now covered** — $120 from Taller Instalaciones Martinez on 07/27 chips it down to ~$177.70. Right target: exactly the other quick win, frees $112.71/mo of minimum-payment cash flow once fully cleared.
- **AVANZ (Tier 1 #3) is ongoing per family agreement, outside this plan** — keep its payments going, don't let it slip while attention is on Visa/Ficohsa.
- **This cycle is minimums-only, no extra avalanche paydown yet** — consistent with the "better perspective in a month" comment; once a month of tracked expenses gives a stable surplus, route extra cash to Tier 0 remainder first, then Tier 1 (AVANZ + BAC NIO cards), not to Visa/Ficohsa which are already at minimum-only status.
- **Watch item:** making BAC Visa the primary spend card means its balance will regrow between paydays (Tier 0's near-zero status won't hold). Budget the 08/08 "pay down accumulated charges" step as a recurring line, not a one-off — otherwise Visa quietly drifts back into the 45%-APR NIO tier instead of staying swept.
## Reuse notes
- Any extra/discretionary paydown cash (beyond scheduled minimums) should follow this tier order, top to bottom.
- Re-derive this analysis if a new rate is confirmed, a balance changes materially, or a debt is fully closed — update tiers rather than starting over, since most rates/order won't move.
- Source data: [[Loans]] and [[Credit Cards]] as of 2026-07-25.
