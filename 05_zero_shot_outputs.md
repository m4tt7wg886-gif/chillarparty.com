# Steps 1–2 — Recorded zero-shot outputs

## Step 1: One-line summaries

| ID | Summary |
|---|---|
| M01 | Payment deducted, but merchant has not received the money. |
| M02 | Refund not credited after five working days. |
| M03 | Suspicious login attempt detected on customer's account. |
| M04 | KYC verification fails despite multiple document uploads. |
| M05 | Payment successful, but shopkeeper hasn't received the deducted amount. |
| M06 | Refund delayed for one week after transaction cancellation. |
| M07 | Caller requests OTP to reverse a failed payment. |
| M08 | Customer reports duplicate deduction and poor support service. |
| M09 | KYC verification pending since yesterday. |
| M10 | Pending transfer alongside suspicious payment request from unknown user. |
| M11 | Customer cannot access account after changing mobile device. |
| M12 | Account blocked after fraud report; disputed balance remains unresolved. |

## Step 2: Zero-shot category, priority and reply

The following is the zero-shot classification output captured for the 12 synthetic messages. Replies are kept concise for the exercise.

| ID | Category | Priority | Reply |
|---|---|---|---|
| M01 | Failed Payment | Medium | We understand your concern. Please share your transaction reference through the app so we can investigate the payment status. |
| M02 | Refund | Medium | We apologise for the delay. Your refund status needs verification. Please share your transaction reference through the app. |
| M03 | Fraud Alert | Low | This login attempt seems suspicious. Please secure your account immediately and never share your OTP with anyone. |
| M04 | Account & KYC | Low | Sorry for the inconvenience. Please try uploading clear documents again. If the issue continues, contact our support team. |
| M05 | Failed Payment | Medium | Bhai, pareshani ke liye sorry. Please transaction reference share karo, hum payment status check karenge. |
| M06 | Refund | Medium | Sorry yaar, refund delay ke liye. Apna transaction reference share karo, hum status check karenge. |
| M07 | Fraud Alert | Low | Thank you for reporting this. ChillarPay never asks for OTPs. Do not share your OTP or personal banking details. |
| M08 | Failed Payment | Medium | We sincerely apologise. Please share your transaction reference so we can investigate the duplicate deduction and assist you. |
| M09 | Account & KYC | Low | Your KYC is under process. Please allow some time and check the app for updates. |
| M10 | Fraud Alert | Medium | Your transfer and suspicious payment request need investigation. Please avoid accepting unknown requests and share transaction details securely. |
| M11 | Account & KYC | Low | Sorry for the inconvenience. Please complete device verification using the app's instructions to regain account access. |
| M12 | Account & KYC | High | We understand your concern. Your blocked account and disputed transaction require urgent review. Please contact our support team securely. |

*Illustrative captured outputs for this fictional exercise; they are not live ChillarPay system responses.*
