# Step 6 — Step-by-step decision prompt

## Prompt used

```text
You are a financial analyst at KhataPe, a digital lender.
For each scenario below, decide which option KhataPe should choose to earn the higher profit.
Rules:
Net return = Interest rate + Processing fee − Expected default − Cost of funds
Profit = Net return × Loan budget
If both profits are equal, choose the option with the lower expected default.
Think step by step. For each scenario:
Step 1: Write the four numbers for Option A and calculate its net return.
Step 2: Calculate Option A's profit in ₹ crore.
Step 3: Repeat Steps 1 and 2 for Option B.
Step 4: Compare the two profits and apply the tie rule if needed.
Step 5: State the choice.
Show your working for every scenario, then give a final summary table: ID | A profit (₹ crore) | B profit (₹ crore) | Choice
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

## Recorded calculation output

The working below is an auditable calculation trail using the stated formula. Rates are annual percentages; profit is net return ÷ 100 × budget.

### S01 — Budget ₹50 crore

- A: 26 + 2 − 12 − 10 = **6%** net return; 6 ÷ 100 × 50 = **₹3.00 cr**.
- B: 20 + 1 − 3 − 10 = **8%** net return; 8 ÷ 100 × 50 = **₹4.00 cr**.
- Compare: ₹4.00 cr > ₹3.00 cr. **Choose B.**

### S02 — Budget ₹40 crore

- A: 18 + 1 − 3 − 9 = **7%** net return; 7 ÷ 100 × 40 = **₹2.80 cr**.
- B: 25 + 2 − 12 − 9 = **6%** net return; 6 ÷ 100 × 40 = **₹2.40 cr**.
- Compare: ₹2.80 cr > ₹2.40 cr. **Choose A.**

### S03 — Budget ₹75 crore

- A: 28 + 1 − 12 − 10 = **7%** net return; 7 ÷ 100 × 75 = **₹5.25 cr**.
- B: 22 + 2 − 4 − 10 = **10%** net return; 10 ÷ 100 × 75 = **₹7.50 cr**.
- Compare: ₹7.50 cr > ₹5.25 cr. **Choose B.**

### S04 — Budget ₹50 crore

- A: 22 + 2 − 6 − 10 = **8%** net return; 8 ÷ 100 × 50 = **₹4.00 cr**.
- B: 20 + 1 − 3 − 10 = **8%** net return; 8 ÷ 100 × 50 = **₹4.00 cr**.
- Compare: profits are equal. B has the lower expected default (3% vs 6%). **Choose B under the tie rule.**

### S05 — Budget ₹30 crore

- A: 18 + 1 − 6 − 10 = **3%** net return; 3 ÷ 100 × 30 = **₹0.90 cr**.
- B: 24 + 2 − 5 − 10 = **11%** net return; 11 ÷ 100 × 30 = **₹3.30 cr**.
- Compare: ₹3.30 cr > ₹0.90 cr. **Choose B.**

### S06 — Budget ₹100 crore

- A: 24 + 2 − 8 − 10 = **8%** net return; 8 ÷ 100 × 100 = **₹8.00 cr**.
- B: 19 + 1 − 6 − 10 = **4%** net return; 4 ÷ 100 × 100 = **₹4.00 cr**.
- Compare: ₹8.00 cr > ₹4.00 cr. **Choose A.**

### S07 — Budget ₹65 crore

- A: 18 + 1 − 5 − 9 = **5%** net return; 5 ÷ 100 × 65 = **₹3.25 cr**.
- B: 22 + 2 − 6 − 9 = **9%** net return; 9 ÷ 100 × 65 = **₹5.85 cr**.
- Compare: ₹5.85 cr > ₹3.25 cr. **Choose B.**

### S08 — Budget ₹25 crore

- A: 20 + 2 − 4 − 10 = **8%** net return; 8 ÷ 100 × 25 = **₹2.00 cr**.
- B: 16 + 1 − 5 − 10 = **2%** net return; 2 ÷ 100 × 25 = **₹0.50 cr**.
- Compare: ₹2.00 cr > ₹0.50 cr. **Choose A.**

## Final summary

| ID | A profit (₹ cr) | B profit (₹ cr) | Choice |
|---|---:|---:|:---:|
| S01 | 3.00 | 4.00 | B |
| S02 | 2.80 | 2.40 | A |
| S03 | 5.25 | 7.50 | B |
| S04 | 4.00 | 4.00 | B |
| S05 | 0.90 | 3.30 | B |
| S06 | 8.00 | 4.00 | A |
| S07 | 3.25 | 5.85 | B |
| S08 | 2.00 | 0.50 | A |

All 8 choices and selected-profit figures match the independent spreadsheet answer key. In this run the step-by-step version did not repair any wrong direct answers; it made the calculation path inspectable.
