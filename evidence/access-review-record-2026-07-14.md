# Privileged Access Review Record — Sanitized

Review date: 2026-07-14

Reviewer/accountable owner: PI Point owner

## Scope

GitHub administration/rules; Vercel production access; Supabase roles, service-role use, Edge Function secrets and database paths; Stripe, Postmark, Twilio and Cloudflare privileged access; PI Point admin/support roles; Smokeball application credentials and backend access.

## Criteria

- named authorized person or controlled service identity;
- privilege required for current duties;
- MFA where supported/applicable;
- no browser or ordinary-support exposure of raw secrets;
- unnecessary/former access removed;
- service credentials scoped and rotated/revoked when required;
- evidence retained without secret values.

## Sanitized result

The review confirmed the documented named-account, least-privilege, server-side-secret and periodic-review model. This public record contains no credential, secret or customer data. Redacted provider-console screenshots/exports are still needed to corroborate specific tenant settings externally; see [Provider-console evidence attachments required](provider-console-attachments-required.md).
