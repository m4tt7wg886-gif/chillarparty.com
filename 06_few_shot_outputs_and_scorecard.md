# Step 3 — Few-shot output and evaluation scorecard

## Few-shot output

| ID | Category | Priority | Reply |
|---|---|---|---|
| M01 | Failed Payment | Medium | Sorry for the trouble. Failed payments usually reverse automatically; please share the transaction ID so we can track it. |
| M02 | Refund | Medium | Sorry for the delay. Please share your transaction ID so we can check your refund status. |
| M03 | Fraud Alert | Low | This login attempt looks suspicious. Please secure your account and never share your OTP with anyone. |
| M04 | Account & KYC | Low | Sorry for the inconvenience. Please upload clear documents again or contact support if verification continues to fail. |
| M05 | Failed Payment | Medium | Bhai, pareshani ke liye sorry. Failed payments usually automatically reverse ho jaate hain. Transaction ID share karein taaki hum check kar sakein. |
| M06 | Refund | Medium | Sorry yaar, refund delay ke liye. Apna transaction ID share karo, hum refund status check karenge. |
| M07 | Fraud Alert | High | This sounds like a fraud attempt. Never share your OTP; ChillarPay never asks for it. |
| M08 | Failed Payment | Medium | Sorry for the trouble. Please share your transaction ID so our team can investigate the duplicate deduction. |
| M09 | Account & KYC | Low | Your KYC is being processed. Please check the app for status updates. |
| M10 | Fraud Alert | Medium | Please avoid responding to unknown payment requests. Share the transaction details securely so our team can investigate. |
| M11 | Account & KYC | Low | Please follow the device verification instructions in the app to regain access to your account. |
| M12 | Account & KYC | High | We apologise. Please contact official in-app support urgently about your blocked account and unauthorised-transaction dispute. |

## Manual scorecard

Counts are out of 12 messages. The scores are illustrative manual judgments for this learning exercise, not a validated benchmark. Category and priority are judged against `04_answer_key.md`; tone assesses empathy, safety and concise language; format assesses table structure and required columns.

| Metric | Zero-shot | Few-shot |
|---|---:|---:|
| Correct category (/12) | 12 | 12 |
| Correct priority (/12) | 11 | 12 |
| Reply follows ChillarPay tone (/12) | 11 | 11 |
| Table format followed (/12) | 12 | 12 |

## Interpretation
- Category assignments match the reference answer key in both recorded outputs.
- Few-shot examples reinforce the reply style and safe handling of credential requests.
- The one priority difference is M07: the zero-shot output marked the active OTP-solicitation attempt Low, while the answer key and few-shot output mark it High.
- A model can mirror Hinglish while still needing checks for accurate classification and non-promissory wording.
- The scorecard is qualitative and should be repeated with multiple runs before any production decision.
- Human review remains mandatory for suspected fraud, account blocks and disputes.

## Limitations
This is a small synthetic dataset. It does not represent real customer distributions, actual ChillarPay policy, regulatory requirements, or a production evaluation. The output samples and hand-scored metrics should be treated as classroom evidence only.
