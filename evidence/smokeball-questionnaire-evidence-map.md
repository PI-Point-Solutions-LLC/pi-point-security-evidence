# Smokeball Supplier Questionnaire Evidence Map

Prepared: 2026-07-14

Every cited item below is either a public URL or is explicitly identified as requiring a separate redacted attachment. No private-repository link is presented as public evidence.

## B1 — Security standards and framework alignment

Claim: PI Point maintains a security program aligned to NIST CSF 2.0 but does not claim ISO, SOC, PCI, or NIST certification.

Public evidence:

- [NIST CSF 2.0 evidence matrix](nist-csf-2-evidence-matrix.md)
- [PI Point Security Policy](https://app.pipointsolutions.com/security)
- [Internal audit function](internal-audit-function.md)
- [Internal audit review record](internal-audit-review-2026-07-14.md)

Limitation: these are management and source records, not independent certification. No certificate should be attached because none is claimed.

## B2 — Formal risk-management process

Claim: PI Point uses a documented, recurring risk-management process.

Public evidence:

- [Risk-management process and current risk summary](risk-management.md)
- [Sanitized current Risk Register](risk-register.md)
- [Vendor Register](vendor-register.md)
- [Dated Vendor Review Record](vendor-review-record-2026-07-14.md)
- [NIST CSF 2.0 evidence matrix — Govern and Identify](nist-csf-2-evidence-matrix.md#govern)
- [Internal audit function — audit method and cadence](internal-audit-function.md#audit-method)
- [PI Point Vulnerability Disclosure](https://app.pipointsolutions.com/vulnerability-disclosure)

The linked sanitized Risk Register is the evidence being provided. A more detailed restricted export is necessary only if Smokeball requests confidential attack-path or remediation detail.

## B3a — Information-security management system

Claim: PI Point has a documented security-management system covering policy, ownership, risk, audit, vendors, access, incidents, recovery, evidence and improvement; it is not a certified ISO 27001 ISMS.

Public evidence:

- [NIST CSF 2.0 evidence matrix](nist-csf-2-evidence-matrix.md)
- [Internal audit function](internal-audit-function.md)
- [Internal audit review record](internal-audit-review-2026-07-14.md)
- [Control ownership and review cadence](control-ownership.md)
- [PI Point Security Policy](https://app.pipointsolutions.com/security)

## B3b — Documented policies, standards, plans and procedures

Claim: PI Point maintains documented security, privacy, incident, continuity, vulnerability and AI/data-boundary policies.

Public evidence:

- [Security Policy](https://app.pipointsolutions.com/security)
- [Privacy Policy](https://app.pipointsolutions.com/privacy)
- [Incident Response](https://app.pipointsolutions.com/incident-response)
- [Vulnerability Disclosure](https://app.pipointsolutions.com/vulnerability-disclosure)
- [Business Continuity](https://app.pipointsolutions.com/business-continuity)
- [AI Usage Policy](https://app.pipointsolutions.com/ai-usage-policy)
- [Terms of Service](https://app.pipointsolutions.com/terms)

## B4 — Internal audit function or external audits

Claim: PI Point operates a management-led internal security audit function appropriate to its size; it does not claim an independent audit.

Public evidence:

- [Internal audit function](internal-audit-function.md)
- [Dated internal audit review record](internal-audit-review-2026-07-14.md)
- [Sanitized Privileged Access Review Record](access-review-record-2026-07-14.md)
- [NIST CSF 2.0 evidence matrix — GV.OV Oversight](nist-csf-2-evidence-matrix.md#govern)

Additional console attachments recommended:

- redacted GitHub Actions run showing security/release checks;
- redacted provider-access review checklist or export;
- redacted Supabase Security Advisor results.

Reason no public console link exists: GitHub Actions details and Supabase dashboard pages require authenticated account access and may expose private repository, project, personnel, or configuration information.

## B5 — Other security arrangements

Claim: PI Point uses layered access, data-security, platform-security, incident and recovery controls.

Public evidence:

- [NIST CSF 2.0 evidence matrix](nist-csf-2-evidence-matrix.md)
- [Smokeball API security evidence](smokeball-api-security.md)
- [Incident Response](https://app.pipointsolutions.com/incident-response)
- [Business Continuity](https://app.pipointsolutions.com/business-continuity)
- [Provider-console attachment register](provider-console-attachments-required.md)

## C1 — Supplier risk assessments

Claim: PI Point assesses suppliers by criticality, data exposure, credentials, control evidence, availability and incident dependency.

Public evidence:

- [Vendor-risk management process and register summary](vendor-risk-management.md)
- [Actual Vendor Register](vendor-register.md)
- [Dated Vendor Review Record](vendor-review-record-2026-07-14.md)
- [Risk-management process](risk-management.md)

Attachment recommended: redacted vendor-review worksheet or provider security-portal evidence for the vendors materially involved in the Smokeball service.

## C2 — Supplier-management program

Claim: PI Point maintains a risk-ranked vendor register and review cadence.

Public evidence:

- [Vendor-risk management process, register and cadence](vendor-risk-management.md)
- [Actual Vendor Register](vendor-register.md)
- [Dated Vendor Review Record](vendor-review-record-2026-07-14.md)
- [Control ownership](control-ownership.md)
- [NIST CSF 2.0 evidence matrix — GV.SC](nist-csf-2-evidence-matrix.md#govern)

## C3 — Assessment of supplier security controls

Claim: PI Point reviews vendor security documentation and available control evidence proportionate to risk.

Public evidence:

- [Vendor-risk management — assessment criteria](vendor-risk-management.md#assessment-criteria)
- [Provider-console attachment register](provider-console-attachments-required.md)

Attachments required for strong corroboration: redacted Supabase, Vercel, GitHub, Stripe, Postmark, Twilio and Cloudflare security/account screenshots or exported assurance documents. Vendor dashboards and contracts are not publicly accessible.

## D1 — Smokeball API use case and scope

Claim: PI Point uses Smokeball OAuth/API workflows for authorized Matter context, contacts, documents and PI Point assignment workflows, with minimized fields and scoped access.

Public evidence:

- [Smokeball API security evidence — use case and data scope](smokeball-api-security.md#d1--use-case-and-data-scope)
- [Privacy Policy](https://app.pipointsolutions.com/privacy)
- [Security Policy](https://app.pipointsolutions.com/security)

Limitation: the application source repository is private. The public technical record contains sanitized source excerpts and file/commit provenance, but full-source review requires controlled repository access or a separately agreed code-review process.

## D2 — Secure API-token storage

Claim: Smokeball OAuth tokens are encrypted with AES-GCM before database storage and the encryption secret remains server-side.

Public evidence:

- [Smokeball API security evidence — token storage and AES-GCM excerpt](smokeball-api-security.md#d2--token-and-secret-storage)
- [Security Policy](https://app.pipointsolutions.com/security)

Attachments required for production corroboration:

- redacted Supabase Edge Function secret-name inventory showing the required Smokeball secret names but no values;
- redacted database schema screenshot/export showing ciphertext columns and server-only access controls;
- optional controlled code-review excerpt signed or acknowledged by the reviewer.

Reason no public Supabase link exists: Supabase project settings, secret inventory and database schema pages require authenticated project access. Secret values must never be public.

## D3 — Backend-only API and authentication calls

Claim: browser clients call PI Point backend functions; Smokeball token exchange/API calls and secrets remain in Supabase Edge Functions.

Public evidence:

- [Smokeball API security evidence — backend-only request path](smokeball-api-security.md#d3--backend-only-request-path)
- [Security Policy](https://app.pipointsolutions.com/security)

Attachment recommended: redacted Supabase function inventory and a network/architecture diagram showing browser → Edge Function → Smokeball API.

## D4 — Additional API safeguards

Claim: PI Point uses HTTPS/TLS, OAuth validation, signed/short-lived launch context, scoped authorization, rate-limit handling, redacted logs and an AI separation boundary.

Public evidence:

- [Smokeball API security evidence — additional safeguards](smokeball-api-security.md#d4--additional-api-safeguards)
- [AI Usage Policy](https://app.pipointsolutions.com/ai-usage-policy)
- [Vulnerability Disclosure](https://app.pipointsolutions.com/vulnerability-disclosure)
- [Security Policy](https://app.pipointsolutions.com/security)

Attachments recommended: redacted passing integration-test output and production HTTPS/header evidence.
