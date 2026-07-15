# Vendor and Supply-Chain Risk Management

Reviewed: 2026-07-14

## Process and cadence

PI Point records each material provider's role, workflow/data exposure, criticality, authentication/secrets, existing controls, incident/availability dependency and additional evidence needed.

- Critical vendors: quarterly and after major incident or architecture change.
- High vendors: at least semiannually.
- Medium vendors: annually or when exposure changes.

## Assessment criteria

- service/workflow dependency;
- data processed or stored;
- production criticality;
- credential and access model;
- encryption and webhook/API controls;
- public security/assurance information;
- contractual/security-portal evidence when available;
- incident, availability, fallback and communications posture;
- changes in scope or subprocessors.

## Current critical-provider register summary

| Provider | Role | Criticality | Public corroboration | Restricted evidence needed |
| --- | --- | --- | --- | --- |
| Supabase | Database, auth, storage, Edge Functions | Critical | [Supabase Security](https://supabase.com/security) | Project backup, advisor, access and secret-name screenshots |
| Vercel | Web hosting and deployments | Critical | [Vercel Security](https://vercel.com/security) | Team/access, production project and deployment evidence |
| GitHub | Source control and CI | Critical | [GitHub Security](https://github.com/security) | Private repo ruleset, collaborator and Actions evidence |
| Stripe | Checkout, payments, Connect, webhooks | Critical | [Stripe Security](https://stripe.com/docs/security) | Account/webhook/security-setting evidence |
| Smokeball | OAuth/API and embedded integration | Critical | [Smokeball](https://www.smokeball.com/) | Partner-provided application/security terms |
| Postmark | Transactional email | High | [Postmark Security](https://postmarkapp.com/security) | Stream, webhook and sender-authentication evidence |
| Twilio | SMS and delivery events | High | [Twilio Trust Center](https://www.twilio.com/en-us/trust-center) | Account, sender/compliance and webhook evidence |
| Cloudflare Turnstile | Bot mitigation | High | [Cloudflare Trust Hub](https://www.cloudflare.com/trust-hub/) | Widget/site configuration and analytics evidence |

Public provider pages describe provider controls but do not prove PI Point's tenant configuration. See [provider-console attachments required](provider-console-attachments-required.md).
