# Step 5 — Direct prompt: final lending decision only

## Prompt used

```text
You are a financial analyst at KhataPe, a digital lender.
For each scenario below, decide which option KhataPe should choose to earn the higher profit.
Rules:
Net return = Interest rate + Processing fee − Expected default − Cost of funds
Profit = Net return × Loan budget
If both profits are equal, choose the option with the lower expected default.
Give the final answer only. Do not show any working.
Output a table: ID | Choice (A or B) | Profit of chosen option (₹ crore)
Scenarios:
| ID | Budget (₹ cr) | A interest | A fee | A default | A cost of funds | B interest | B fee | B default | B cost of funds |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| S01 | 50 | 26% | 2% | 12% | 10% | 20% | 1% | 3% | 10% |
| S02 | 40 | 18% | 1% | 3% | 9% | 25% | 2% | 12% | 9% |
| S03 | 75 | 28% | 1% | 12% | 10% | 22% | 2% | 4% | 10% |
| S04 | 50 | 22% | 2% | 6% | 10% | 20% | 1% | 3% | 10% |
| S05 | 30 | 18% | 1% | 6% | 10% | 24% | 2% | 5% | 10% |
| S06 | 100 | 24% | 2% | 8% | 10% | 19% | 1% | 6% | 10% |
| S07 | 65 | 18% | 1% | 5% | 9% | 22% | 2% | 6% | 9% |
| S08 | 25 | 20% | 2% | 4% | 10% | 16% | 1% | 5% | 10% |
```

## Recorded AI output

| ID | Choice | Profit of chosen option (₹ cr) | Choice check | Profit check |
|---|:---:|---:|:---:|:---:|
| S01 | B | 4.00 | ✔ | ✔ |
| S02 | A | 2.80 | ✔ | ✔ |
| S03 | B | 7.50 | ✔ | ✔ |
| S04 | B | 4.00 | ✔ | ✔ |
| S05 | B | 3.30 | ✔ | ✔ |
| S06 | A | 8.00 | ✔ | ✔ |
| S07 | B | 5.85 | ✔ | ✔ |
| S08 | A | 2.00 | ✔ | ✔ |

**Result:** 8/8 choices and 8/8 selected-profit figures match the independent spreadsheet answer key. All 3 traps and the tie-break are handled correctly in this run. This is a valid result even though the exercise expected that a direct prompt might struggle.
