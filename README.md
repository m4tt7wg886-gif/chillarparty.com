# ChillarPay AI Support: From Zero-shot to Few-shot Prompting

**A FinTech case study on when a simple prompt is enough and when AI needs examples.**

Author: Arwin Kalra · BBA (FinTech), Chitkara Business School · Tool: ChatGPT · November 2026

## The case
**ChillarPay** (fictional) is a UPI payments app in Jaipur with 8 lakh users. It receives about 2,000 support messages a day in English and Hinglish, and urgent fraud cases get lost among simple questions. As a Business Analyst, I tested whether AI can sort messages, set priority and draft replies, and what kind of prompt it needs.

## The data
12 synthetic customer messages created for this case study (10 English, 2 Hinglish, 3 deliberately tricky). No real customer data is used. The evaluation key is documented in `04_answer_key.md`.

## Approach
| Step | Prompt type | Task |
|---|---|---|
| 1 | Zero-shot | One-line summary of each message |
| 2 | Zero-shot | Category + priority + reply |
| 3 | Few-shot (3 examples) | Same task as Step 2 |

## Results
Scores below are a documented manual assessment against the answer key in this repository. They are illustrative results from this case-study exercise, not production benchmark results.

| Metric | Zero-shot | Few-shot |
|---|---:|---:|
| Correct category (/12) | 12 | 12 |
| Correct priority (/12) | 11 | 12 |
| Reply follows ChillarPay tone (/12) | 11 | 11 |
| Table format followed (/12) | 12 | 12 |

## Key learnings
1. **Zero-shot is enough for simple tasks:** One-line summaries and common support classifications were generally handled well with clear instructions.
2. **Few-shot teaches company-specific rules:** The examples reinforce the company's response style and safety guidance, while the answer key makes mixed-intent cases M10 and M12 easier to assess consistently.
3. **Hinglish and tricky messages:** The model generally mirrored the Hinglish messages, but mixed-intent messages still needed a defined primary-category rule.
4. **Limitation:** Few-shot examples can overgeneralise their wording; some replies add generic process claims that should be checked against real company policy.

## My recommendation to ChillarPay
Use zero-shot for first-pass summaries and routine triage, with a concise policy prompt and a strict output schema. Use the few-shot version for customer-facing reply drafting where company tone and safety rules matter, while routing fraud alerts and account blocks to a human team.

## Skills shown
Prompt engineering · Zero-shot and few-shot prompting · Synthetic data creation · AI output evaluation · Customer-support operations · FinTech domain knowledge

## What I learned
- Zero-shot prompting (instructions only) works well for simple, common tasks like summarising.
- Few-shot prompting (instructions + solved examples) teaches AI a company's own rules, tone and format.
- Start with the simplest prompt, and add examples only when the output misses the rules.
- How to create a realistic synthetic dataset with AI, without using real customer data.
- Why the answer key must be written before testing, so AI output is judged fairly.
- How to measure AI quality with a scorecard instead of gut feeling.
- AI output must always be checked by a human before business use.

*ChillarPay and all data in this project are fictional and created for learning.*
