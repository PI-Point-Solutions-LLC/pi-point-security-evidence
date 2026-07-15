# Provider-Console Evidence Attachments Required

Provider dashboards are authenticated and often contain secrets, project identifiers, account identifiers, personnel, customer data or private-repository information. There is no safe public URL that proves PI Point's tenant configuration. The following redacted attachments should accompany the questionnaire when the claim is material.

| ID | Provider | Exact attachment | Supports | Redaction requirements |
| --- | --- | --- | --- | --- |
| A-01 | Supabase | Project backup settings/status showing schedule and retention | B5, PR.IR, RC.RP; cloud backup answers | Redact project reference if desired; exclude connection strings and data |
| A-02 | Supabase | Security Advisor results summary with date and disposition | B2, B4, B5, ID.RA, PR.PS | Exclude SQL containing sensitive schema/data; show counts/status only |
| A-03 | Supabase | Edge Function secret-name inventory showing required Smokeball variable names | D2, D3 | Never show secret values; redact unrelated secret names if sensitive |
| A-04 | Supabase | Schema/policy export for Smokeball OAuth connection table showing ciphertext fields and restricted grants | D2, D3 | Exclude row data, tokens, tenant identifiers and credentials |
| A-05 | Supabase | Edge Function inventory for Smokeball functions | D1, D3, D4 | Exclude environment values and private URLs if sensitive |
| A-06 | GitHub | Main-branch ruleset and required-checks screenshot | B4, B5, GV.OV, PR.PS, PR.MA | Redact private collaborator details if not required |
| A-07 | GitHub | Successful PR CI/release-gate run summary | B4, B5, PR.PS, PR.MA, ID.IM | Show workflow/check names, commit, date and result; exclude logs containing secrets |
| A-08 | Vercel | Production project/deployment and team-access summary | B5, PR.PS, PR.IR, DE.CM | Redact environment values and personnel not required for review |
| A-09 | Stripe | Webhook endpoint/signature-verification configuration summary | B5, C3 | Never show signing secret; redact account/customer/payment data |
| A-10 | Postmark | Server/stream, webhook and sender-authentication summary | C1–C3, DE.CM | Redact server tokens, message recipients and content |
| A-11 | Twilio | Account sender/compliance and status-callback summary | C1–C3, DE.CM | Redact Auth Token, phone numbers if unnecessary and message data |
| A-12 | Cloudflare | Turnstile widget/site and recent analytics summary | C1–C3, PR.PS, DE.CM | Never show secret key; redact unrelated domains |
| A-13 | PI Point | Redacted current risk-register export | B2, ID.RA, GV.RM | Remove attack-path detail, credentials, private provider identifiers and personal data |
| A-14 | PI Point | Redacted quarterly privileged-access review | B4, PR.AA, GV.OV | Minimize names/emails; show roles, review date, disposition and approver |
| A-15 | PI Point | Redacted Smokeball integration-test results | D1–D4 | Exclude tokens, Matter/customer data, private endpoints and credentials |

## Why screenshots/exports are necessary

Public provider trust pages show the provider's general controls. They do not prove that PI Point enabled or configured a feature in its tenant. A redacted, dated console screenshot or export is the appropriate corroborating evidence when direct guest access to the provider account is neither safe nor reasonable.
