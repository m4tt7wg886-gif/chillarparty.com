# Evaluation answer key

This is the reference key used for the manual comparison in this portfolio exercise. Classification rules choose the dominant actionable issue. Borderline mixed-intent cases are explicitly resolved here so the evaluation is repeatable.

| ID | Expected summary | Gold category | Gold priority | Rationale |
|---|---|---|---|---|
| M01 | Payment deducted, but merchant has not received the money. | Failed Payment | Medium | Payment discrepancy; no reported unauthorised activity. |
| M02 | Refund not credited after five working days. | Refund | Medium | Refund is delayed. |
| M03 | Suspicious login attempt detected on customer's account. | Fraud Alert | Low | Suspicious access alert, but no account loss or unauthorised transaction reported. Escalate security guidance even though the defined triage priority is Low. |
| M04 | KYC verification fails despite multiple document uploads. | Account & KYC | Low | Routine verification failure. |
| M05 | Payment successful, but shopkeeper hasn't received the deducted amount. | Failed Payment | Medium | Same issue as M01, expressed in Hinglish. |
| M06 | Refund delayed for one week after transaction cancellation. | Refund | Medium | Same issue as M02, expressed in Hinglish. |
| M07 | Caller requests OTP to reverse a failed payment. | Fraud Alert | High | Active social-engineering attempt seeking authentication credentials; immediate safety guidance is appropriate. |
| M08 | Customer reports duplicate deduction and poor support. | Failed Payment | Medium | Duplicate deduction needs investigation; message does not explicitly establish unauthorised activity. |
| M09 | KYC verification pending since yesterday. | Account & KYC | Low | Routine status question. |
| M10 | Pending transfer alongside suspicious payment request from unknown user. | Fraud Alert | Medium | Mixed-intent case; fraud concern is dominant for safe triage, while payment remains stuck. |
| M11 | Customer cannot access account after changing mobile device. | Account & KYC | Low | Device verification/access issue without reported suspicious activity. |
| M12 | Account blocked after fraud report; disputed balance unresolved. | Account & KYC | High | Account block is the immediate operational issue; unauthorised transaction should remain linked for fraud review. |

**Important evaluation note:** M07 is High in this revised answer key because the message describes an active attempt to obtain an OTP. This is a safety-first refinement to the initial triage rule. Any reported suspected fraud should receive secure guidance regardless of numeric priority.
