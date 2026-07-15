# Cybersecurity Risk-Management Evidence

Reviewed: 2026-07-14

## Process

PI Point identifies risks through architecture/change review, provider advisories, dependency audit, vulnerability reports, security tests, incident/tabletop analysis and vendor reviews. Risks are assessed for likelihood, impact, affected data/workflows and control effectiveness.

Treatment options are remediate, mitigate, accept with rationale, stage for guarded treatment, transfer/provider-manage or mark not applicable. Owners, evidence and follow-up are reviewed quarterly and after material change or incident.

## Current sanitized risk summary

| Risk area | Current treatment |
| --- | --- |
| Evidence distributed across code/providers | Central public evidence map plus restricted operating evidence |
| Privileged/provider access | Named accounts, least privilege, MFA where supported, quarterly review |
| Dependency/application vulnerabilities | Risk-based remediation targets and release/security checks |
| Integration tokens/secrets | Server-side secret management and application-layer token encryption |
| Fragile database permission changes | Staged, tested batches with caller map, rollback and verification |
| Critical vendor dependency | Risk-ranked register, review cadence, status/security evidence and incident coordination |
| Incident and recovery readiness | Documented response/continuity policies, owners, exercises and follow-up |

## Disclosure boundary

The full operating risk register is not public because it can contain sensitive architecture, attack-path, provider and remediation detail. A redacted current export can be provided to Smokeball as an attachment under confidentiality.
