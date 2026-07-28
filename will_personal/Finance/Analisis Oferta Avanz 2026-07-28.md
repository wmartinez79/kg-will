---
tags:
  - finance
  - debts
  - analysis
---

# Loan Offer Analysis — Avanz vs. Ficohsa

Prepared 2026-07-28, updated with the Ficohsa offer. Companion to [[Debt Payoff Analysis]] — does not replace it. See [[Avanz vs Ficohsa Loan Analysis 2026-07-28.pdf|Spanish PDF version]].

## The two offers

| Item | Avanz | Ficohsa |
|---|---|---|
| Pre-approved amount (face) | $10,800.00 | $9,800.00 |
| Disbursement fee | 0% | 2% (=$196.00) |
| Net amount received | $10,800.00 | $9,604.00 |
| Monthly payment | ~$287.00 (insurance included) | $280.35 |
| Term | 60 months | 60 months |
| Quoted nominal rate | 1.5% monthly | 1.5% monthly |

Both quote the same nominal rate (1.5%/mo). But the actual payment each bank quotes doesn't match a pure 1.5%/mo amortization — the real implied rate has to be backed out of the payment to compare properly.

### Verification — real rate implied by the payment

Amortizing at 1.5%/mo over 60 months, the "pure" payment (no insurance/fees) would be:
- Avanz: $10,800 × factor(1.5%,60) ≈ **$274.26** — quoted payment $287.00, difference +$12.74/mo (insurance).
- Ficohsa: $9,800 × factor(1.5%,60) ≈ **$248.86** — quoted payment $280.35, difference +$31.49/mo (insurance + fees) — proportionally **more than double** Avanz's.

Solving for the monthly rate that actually reproduces the quoted payment (on the face amount, before the disbursement fee):

| | Implied monthly rate | Implied effective annual rate |
|---|---|---|
| Avanz | ~1.68%/mo | **~22.1%** |
| Ficohsa | ~1.98%/mo | **~26.5%** |

And once Ficohsa's disbursement fee is also factored in (you receive $9,604 but pay a payment calculated on $9,800), the real cost climbs further:

| | Real monthly rate (net of fee) | Real effective annual rate |
|---|---|---|
| Avanz (0% fee, unchanged) | ~1.68%/mo | ~22.1% |
| Ficohsa (2% fee) | ~2.06%/mo | **~27.7%** |

**Rate conclusion: Avanz is cheaper than Ficohsa (~22.1% real vs. ~27.7% real), even though both advertise the same 1.5% monthly.**

## Why either one is worth doing

BAC's three NIO balances (PriceSmart, Visa, AMEX Black) sit at **45% APR** — the most expensive debt on the books, worse than the existing AVANZ loan (~23.3% est.) and worse than any other loan held. Replacing a chunk of that 45% debt with new debt at ~22–28% real is still an improvement of **~17–23 points**, regardless of which offer is taken.

## Coverage of the target amount (#4 + #6 = $10,028.02)

| | Net amount available | Covers #4+#6 ($10,028.02)? | Surplus / shortfall |
|---|---|---|---|
| Avanz | $10,800.00 | Yes | **+$771.98 surplus** → partial paydown on Visa |
| Ficohsa | $9,604.00 (net of fee) | **No** | **-$424.02 shortfall** — doesn't even cover the two target debts in full |

Ficohsa, as quoted ($9,800 face / $9,604 net), **falls short** of closing #4 (PriceSmart, $2,803.03) + #6 (AMEX Black, $7,224.99) in full — a remainder of $424.02 would stay on one of the two cards, with no room left for Visa. Avanz closes both and leaves a surplus for Visa.

## Recommendation

**Avanz wins on both dimensions that matter:** lower real rate (~22.1% vs. ~27.7%) and enough amount to close #4+#6 in full with a surplus for Visa. Ficohsa isn't just more expensive — it also falls short of the target. There's no scenario where Ficohsa is the better option for this specific purpose, unless Ficohsa offers additional terms not captured here (e.g. relationship discount, consolidation of Ficohsa's own existing loans/cards).

## Proposed allocation (with Avanz)

Target debts, taken from the payoff priority order ([[Debt Payoff Analysis]] #4 and #6 — both 45% APR, same priority tier as #5):

| # | Debt | Balance (NIO) | Balance (USD equiv.) | Rate |
|---|---|---|---|---|
| 4 | BAC PriceSmart CC (NIO) | 102,658.88 | $2,803.03 | 45% |
| 6 | BAC AMEX Black CC (NIO) | 264,610.03 | $7,224.99 | 45% |
| | **Subtotal (#4 + #6)** | | **$10,028.02** | |

Loan surplus: $10,800.00 − $10,028.02 = **$771.98**

That surplus goes as a partial paydown on **#5 BAC Visa CC (NIO)** — the card Will uses as the primary day-to-day spend card (family included), where available credit room is critical.

### Why the surplus goes to Visa, not held as a "buffer"

Holding the surplus as separate cash **doesn't free up credit room** — a card's available room is limit minus balance, so only lowering the balance opens real space. Applying it directly to Visa:
- Frees real credit room on the card (same effect as the "buffer" idea, but real)
- Eliminates 45% interest on that amount, instead of paying ~19.6% on cash sitting idle unused
- Cost of not doing this: ~25 points of spread on $771.98 ≈ **$193/yr** lost for no credit-room benefit

## How much frees up in monthly minimum payments

Once #4 and #6 are fully closed (not #5, which only drops partially):

| Card | Minimum (NIO) | Minimum (USD) |
|---|---|---|
| PriceSmart | 6,798.00 | 11.00 |
| AMEX Black | 16,248.00 | 202.00 |
| **Total freed** | **23,046.00** (~$629.30 @ 36.6243) | **213.00** |

**Total freed in minimum payments: ≈ $842.30/mo**, guaranteed once both accounts hit zero.

Visa's minimum will likely drop too as its balance shrinks, but the bank recalculates the minimum based on remaining balance — can't be quantified without the next statement, so it's not counted as guaranteed freed cash flow (it's unmeasured upside).

## Net cash flow

| Item | Monthly amount |
|---|---|
| Freed (PriceSmart + AMEX Black minimums) | +$842.30 |
| New Avanz payment | -$287.00 |
| **Net freed per month** | **+$555.30** |

Despite taking on $10,800 in new debt, the net effect is freeing ~$555/mo in cash flow — because two 45% card minimums are being retired with a single fixed payment at ~19.6–22.1%.

## Impact on the payoff priority order ([[Debt Payoff Analysis]])

If this offer is executed:
- **#4 (PriceSmart NIO) and #6 (AMEX Black NIO) come off the list** — closed.
- **#5 (Visa NIO) stays open**, with a reduced balance (~160,983 NIO) and remains the daily-spend card — still needs the already-identified "watch item": its balance regrows between EPS pay cycles.
- **The new Avanz loan becomes a debt of its own**, at ~19.6–22.1% effective annual — it would sit in the ~18.6–20% Tier 2 band, alongside Ficohsa loan 0000044006 (18.62%) and Ficohsa loan 2211 (~20% est.), and should be added to [[Loans]] and the priority table once disbursed.
- #3 AVANZ (wife's existing loan, family agreement) and #7/#8 (Ficohsa/Lafise NIO) aren't touched by this offer — they continue on their normal course.

## Open items

1. Once disbursed (Avanz disburses the full requested amount in a single disbursement, $10,800.00), update [[Loans]], [[Credit Cards]], and [[Debt Payoff Analysis]] with the new balances and the new loan line.
2. If Ficohsa is worth reconsidering: confirm whether they'll raise the amount to what's actually needed ($10,028.02+) without raising the fee proportionally, or whether there's some non-financial benefit (e.g. banking relationship, consolidating Ficohsa's own existing debt) that offsets the higher rate — otherwise, Avanz is the offer to take.
