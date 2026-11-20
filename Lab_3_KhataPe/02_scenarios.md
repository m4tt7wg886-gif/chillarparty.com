# Steps 2–3 — Synthetic scenarios and independent answer key

## Data-generation prompt

```text
You are helping me build a realistic test dataset for a business case study.
KhataPe is a fictional digital lender in Indore. Every month it chooses between two loan products, Option A and Option B.
Create 8 monthly decision scenarios (S01 to S08).
For each scenario give:
- Loan budget in ₹ crore (between 10 and 100)
- For Option A and for Option B: interest rate %, processing fee %, expected default %, cost of funds %
Rules:
- Use whole numbers or one decimal place only.
- Interest rate between 12% and 30%; processing fee between 0% and 3%; expected default between 1% and 12%; cost of funds between 8% and 12%.
- In 3 scenarios, the option with the HIGHER interest rate must make LESS profit because its expected default is much higher.
- In 1 scenario, both options must make exactly the same profit.
- Do NOT calculate profit and do NOT say which option is better.
Output a table with these columns: ID | Budget (₹ crore) | A interest | A fee | A default | A cost of funds | B interest | B fee | B default | B cost of funds
```

## Scenario dataset

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

## Step 3 — Independent spreadsheet calculation

I entered the scenario inputs in a spreadsheet and used formulas before comparing the AI decision outputs.

- Net return (%) = Interest + Fee − Expected default − Cost of funds
- Profit (₹ crore) = Net return (%) ÷ 100 × Budget (₹ crore)
- Choice = higher profit; if equal, choose the option with lower expected default.

| ID | A net return (%) | A profit (₹ cr) | B net return (%) | B profit (₹ cr) | Correct choice |
|---|---:|---:|---:|---:|:---:|
| S01 | 6.0 | 3.00 | 8.0 | 4.00 | B |
| S02 | 7.0 | 2.80 | 6.0 | 2.40 | A |
| S03 | 7.0 | 5.25 | 10.0 | 7.50 | B |
| S04 | 8.0 | 4.00 | 8.0 | 4.00 | B |
| S05 | 3.0 | 0.90 | 11.0 | 3.30 | B |
| S06 | 8.0 | 8.00 | 4.0 | 4.00 | A |
| S07 | 5.0 | 3.25 | 9.0 | 5.85 | B |
| S08 | 8.0 | 2.00 | 2.0 | 0.50 | A |

The formula-driven workbook is supplied separately as KhataPe_Lending_Answer_Key.xlsx.

## Dataset quality check — first finding

- **Three trap scenarios found:** S01, S02 and S03. In each, the higher-interest option has a lower profit because its expected default rate is substantially higher.
- **One exact tie found:** S04. Both options return 8.0% net and ₹4.00 crore profit. Option B wins the tie-break because its expected default is 3%, compared with 6% for Option A.
- The remaining four scenarios have no tie, and the higher-profit option is selected by the formula.

The generated data satisfies the requested “3 traps + 1 tie” pattern.
