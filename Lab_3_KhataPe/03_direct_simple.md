# Step 4 — Direct prompt: higher interest rate

## Prompt used

```text
Here are 8 lending scenarios for KhataPe, a digital lender.
For each scenario, which option has the higher interest rate? Answer only A or B.
Output a table: ID | Higher interest rate
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

| ID | Higher interest rate |
|---|:---:|
| S01 | A |
| S02 | B |
| S03 | A |
| S04 | A |
| S05 | B |
| S06 | A |
| S07 | B |
| S08 | A |

## Observation

All 8 comparisons are correct against the input data. A direct answer is enough here because the task is a single comparison between two interest-rate values; there is no multi-step profit calculation or tie rule.
