# KhataPe Lending Decisions: Direct Answers vs Chain-of-Thought Prompting

**A FinTech case study on when AI can give a quick answer and when it must show its working.**

Author: Arwin Kalra · BBA (FinTech), Chitkara Business School · Tool: ChatGPT · November 2026

## The case
**KhataPe** (fictional) is a digital lender in Indore that lends to kirana shops and students. Every month it must choose between two loan products with different interest rates, fees and default risk. As a Business Analyst, I tested whether AI can pick the more profitable option, and whether asking it to reason step by step makes it more reliable.

## The data
8 synthetic monthly scenarios created with AI, including 3 "trap" scenarios where the higher interest rate makes less profit and 1 tie. I calculated the correct answers in a formula-driven spreadsheet before evaluating the AI outputs.

## Decision rule
Net return = Interest rate + Processing fee − Expected default − Cost of funds  
Profit = Net return ÷ 100 × Loan budget

## Approach
| Step | Prompt type | Task |
|---|---|---|
| 1 | Direct | Which option has the higher interest rate? |
| 2 | Direct | Which option makes more profit? (final answer only) |
| 3 | Chain-of-thought | Same decision, shown with auditable calculations |
| 4 | Step-by-step follow-up | One number changed: does the calculation and choice update? |

## Results
| Metric | Direct | Step by step |
|---|---:|---:|
| Correct choice (/8) | 8 | 8 |
| Correct profit figure (/8) | 8 | 8 |
| Trap scenarios correct (/3) | 3 | 3 |
| Working I could check | No | Yes |

## Key learnings
1. **A direct answer is enough for one-step questions:** All eight higher-interest comparisons were correct; each requires only comparing two rates.
2. **Step-by-step reasoning helps multi-step decisions:** It did not fix any wrong choices in this run because the direct decision output was already 8/8. It did make every rate adjustment, profit and tie-break easier to audit.
3. **Convincing is not the same as correct:** None of the recorded calculations was wrong in this run. The spreadsheet remains the independent check rather than treating a well-formatted explanation as proof.
4. **What the numbers do not show:** RBI digital-lending compliance and borrower-protection obligations, plus collection and servicing costs, can change the real business decision.

## My recommendation to KhataPe
Use AI to organise and explain monthly comparisons, but calculate the official answer in a controlled spreadsheet or lending system with locked formulas. A human analyst should verify input quality, tie-breaks, compliance, borrower impact and costs omitted from this simplified model before the CFO approves a product.

## Skills shown
Prompt engineering · Chain-of-thought prompting · Synthetic data creation · Spreadsheet financial analysis · AI output verification · Lending business basics

## What I learned
- A direct prompt works well for simple, one-step questions.
- A step-by-step audit trail makes calculations easier to inspect and compare against a spreadsheet.
- Step-by-step working can look convincing and still contain a wrong number, so every step must be checked.
- How to create synthetic business scenarios with AI, including deliberate "trap" cases.
- Why I calculate my own answer key in a spreadsheet before testing AI.
- Changing one number is a quick test of whether AI updates the underlying calculation.
- Numbers alone do not make a lending decision; risk, regulation and operating costs matter too.

*KhataPe and all data in this project are fictional and created for learning.*
