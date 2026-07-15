# PI Point Vendor Review Record

Review date: 2026-07-14

Reviewer/accountable owner: PI Point owner

Scope: critical and high providers supporting PI Point and the Smokeball integration.

## Review performed

- confirmed each provider's role, exposure, criticality and current dependency;
- reviewed public security/trust material and available private configuration evidence;
- checked authentication, secrets, webhook/API controls and data boundaries;
- identified external-review attachments requiring redaction;
- confirmed cadence and reassessment triggers.

## Results

| Vendor | Result | Remaining external evidence action |
| --- | --- | --- |
| Supabase | Critical backend control basis reviewed | Supply redacted backup, advisor, secret-name, schema/policy and function-inventory evidence as applicable |
| Vercel | Hosting/deployment control basis reviewed | Supply redacted production project/deployment and access summary |
| GitHub | Source/CI control basis reviewed | Supply redacted main-branch ruleset and successful required-check run |
| Stripe | Hosted payment/webhook control basis reviewed | Supply redacted webhook/account security evidence if requested |
| Postmark | Email/webhook control basis reviewed | Supply redacted stream/webhook/sender evidence if relevant |
| Twilio | SMS/status control basis reviewed | Supply redacted sender/compliance/callback evidence if relevant |
| Cloudflare Turnstile | Bot-control basis reviewed | Supply redacted widget/site evidence if relevant |
| Smokeball | Integration security design documented | Complete partner review and supply scoped technical/operating evidence |

Conclusion: the vendor program and current register support a risk-ranked supplier-management process. Public trust pages corroborate provider controls; PI Point tenant configuration requires the identified redacted attachments.

Related evidence: [Vendor Register](vendor-register.md), [Vendor Risk-Management Process](vendor-risk-management.md), [Attachment Requirements](provider-console-attachments-required.md).
