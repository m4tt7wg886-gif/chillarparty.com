# Step 1 — KhataPe case study

**KhataPe** is a fictional digital lender in Indore that gives small loans to kirana shops and college students through its app. Every month it has a fixed budget to lend and must choose between two loan products, Option A and Option B.

The CFO asks the Business Analyst: **Can AI help pick the more profitable option every month? Can we trust a quick answer, or should the calculation be shown so a person can verify it?**

## Decision rules

| Item | Rule |
|---|---|
| Net return | Interest rate + Processing fee − Expected default − Cost of funds (all in % per year) |
| Profit | Net return ÷ 100 × Loan budget |
| Decision | Choose the option with the higher profit. If profits are equal, choose the option with the lower expected default. |
| Ignore | Operating costs, taxes and timing of payments |

## Worked example

Option A: 22% interest + 2% fee − 6% default − 10% cost of funds = 8% net return. On a ₹50 crore budget, profit = 8 ÷ 100 × ₹50 crore = ₹4 crore.

Option B: 18% interest + 1% fee − 3% default − 10% cost of funds = 6% net return. Profit = 6 ÷ 100 × ₹50 crore = ₹3 crore.

KhataPe chooses Option A because its profit is higher.

**Important:** This is a simplified classroom model, not a real lending profitability model or financial recommendation. It intentionally excludes costs and risks listed in the case.
