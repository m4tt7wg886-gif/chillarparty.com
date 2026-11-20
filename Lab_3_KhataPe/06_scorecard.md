# Step 7 — Working check, changed-number test and scorecard

## Part A — Check the working

I selected two trap scenarios, S01 and S02. The calculation trail in 05_cot_decision.md is checked against the independently calculated spreadsheet.

| Scenario | Step | AI result | Spreadsheet result | Correct? |
|---|---|---|---|:---:|
| S01 | Step 1 — A net return | 26 + 2 − 12 − 10 = 6% | 6% | ✔ |
| S01 | Step 2 — A profit | 6 ÷ 100 × 50 = ₹3.00 cr | ₹3.00 cr | ✔ |
| S01 | Step 3 — B net return and profit | 20 + 1 − 3 − 10 = 8%; ₹4.00 cr | 8%; ₹4.00 cr | ✔ |
| S01 | Step 4 — Compare and choose | B; ₹4.00 cr > ₹3.00 cr | B | ✔ |
| S02 | Step 1 — A net return | 18 + 1 − 3 − 9 = 7% | 7% | ✔ |
| S02 | Step 2 — A profit | 7 ÷ 100 × 40 = ₹2.80 cr | ₹2.80 cr | ✔ |
| S02 | Step 3 — B net return and profit | 25 + 2 − 12 − 9 = 6%; ₹2.40 cr | 6%; ₹2.40 cr | ✔ |
| S02 | Step 4 — Compare and choose | A; ₹2.80 cr > ₹2.40 cr | A | ✔ |

## Part B — Change one number (S01)

Original S01 Option B expected default = **3%**. Change only that input by +4 percentage points, to **7%**.

- A is unchanged: 26 + 2 − 12 − 10 = 6%; profit = 6 ÷ 100 × 50 = **₹3.00 cr**.
- Updated B: 20 + 1 − 7 − 10 = 4%; profit = 4 ÷ 100 × 50 = **₹2.00 cr**.
- Updated decision: A at ₹3.00 cr beats B at ₹2.00 cr.

**Does the choice change? Yes.** It changes from B to A. The updated working changes the affected B net return, B profit, comparison and final choice; A remains unchanged.

## Part C — Scorecard

| What you check | Direct (Step 5) | Step by step (Step 6) |
|---|---:|---:|
| Correct choice (out of 8) | 8/8 | 8/8 |
| Correct profit figure (out of 8) | 8/8 | 8/8 |
| Trap scenarios correct (out of 3) | 3/3 | 3/3 |
| Working you could check (yes / no) | No | Yes |

## Reflection (about 150 words)

The direct answer was good enough for Step 4 because comparing two interest rates is a one-step task; all eight outputs matched the source numbers. In Step 5, the direct prompt also got all eight decisions and selected-profit figures right, including the three traps and the tie. Therefore, there were no scenario IDs for step-by-step calculations to fix. Step 6 did not improve measured accuracy in this run, but it made the calculations auditable. For example, S04 shows why the tie rule matters: both options earn ₹4 crore, so Option B is selected because its expected default is lower (3% versus 6%). The calculations are not a complete lending decision. First, KhataPe must consider applicable RBI digital-lending requirements, borrower disclosures, consent and fair recovery practices. Second, it must include collection, servicing and operational costs, which this exercise explicitly ignores. A human analyst should verify the inputs, spreadsheet formulas, compliance and borrower impact before any lending decision.

*All scenarios are synthetic and all calculations are for classroom learning only.*
