# PI Point Vendor Register

Register date: 2026-07-14

Owner: PI Point security/vendor owner

Review cadence: Critical quarterly; High semiannually; Medium annually; additionally after material incident, architecture change, data-scope change, or new subprocessor.

| Vendor | Service role | PI Point / Smokeball exposure | Criticality | Current control basis | Review status |
| --- | --- | --- | --- | --- | --- |
| Supabase | Database, authentication, storage, Edge Functions and jobs/webhooks | PI Point accounts, assignments, documents, events, encrypted Smokeball OAuth state and backend integration workflows | Critical | RLS, private storage, service-role separation, Edge Functions, provider review, backup/advisor/access evidence | Reviewed 2026-07-08; configuration attachments required |
| Vercel | Frontend hosting, deployments and routing | Public application assets and production routing; no intended Smokeball token storage | Critical | Deployment access, preview/production workflows, headers and provider review | Reviewed 2026-07-08; configuration attachment recommended |
| GitHub | Private source control and CI/CD | Private source, tests, migrations and workflows; no production customer database | Critical | Named access, protected main, required checks and version history | Reviewed 2026-07-08; ruleset/CI attachments recommended |
| Stripe | Checkout, payments, Connect and signed webhooks | Payment workflow identifiers/events; PI Point does not store full card numbers | Critical | Stripe-hosted flows, server-side signature verification and restricted secrets | Reviewed 2026-07-08; account/webhook attachment recommended |
| Smokeball | OAuth, API, SSO/custom actions and Matter-linked workflows | Authorized Matter, contact, document and user context needed for the integration | Critical | OAuth, server-side API model, scoped data, token encryption and launch validation | Integration partner under current review |
| Postmark | Transactional email and webhook events | Recipient email, transactional metadata and delivery events when required | High | Server-side send, authenticated sender/domain and webhook handling | Reviewed 2026-07-08; configuration attachment recommended |
| Twilio | SMS and delivery-status webhooks | Phone number and transactional delivery metadata where enabled | High | Server-side send, restricted credentials, callbacks and compliance processes | Reviewed 2026-07-08; configuration attachment recommended |
| Cloudflare Turnstile | Bot protection | Challenge token and verification context; no intended Smokeball Matter content | High | Server-side Siteverify and restricted secret | Reviewed 2026-07-08; widget evidence recommended |
| Mapping provider | Map/geocoding support | Limited location/search inputs; not intended for Smokeball documents or tokens | Medium | Scoped keys and limited purpose | Annual review |
| Optional AI provider | Optional PI Point CRM email-marketing support only | Not authorized to receive Smokeball Matter, contact, document, OAuth, SSO, payment or assignment data | Conditional | AI usage policy and data boundary | Review when enabled or scope changes |

This sanitized public register excludes provider account IDs, contracts, secrets, customer data and sensitive architecture. Required tenant-configuration evidence is listed in [Provider-console evidence attachments required](provider-console-attachments-required.md).
