# Internal Security Audit Function

Effective/reviewed: 2026-07-14

PI Point operates a management-led internal security audit function appropriate to its size and risk profile. It reviews the security program against documented criteria, records findings, verifies remediation and supports rapid updates.

This is not an independent third-party audit, SOC examination, ISO certification or legal compliance opinion.

## Scope

- NIST CSF control outcomes and evidence;
- risk register, owners, treatment and accepted risk;
- privileged and service access;
- critical vendors and their security evidence;
- policies, ownership and review dates;
- CI, release, dependency, security-readiness and regression checks;
- provider security findings and documented exceptions;
- incident, recovery, tabletop and lessons-learned records;
- backup/recovery readiness and security remediation.

## Audit method

1. Review evidence against current architecture.
2. Inspect reproducible security/release checks.
3. Review provider evidence without exposing secrets.
4. Verify owners and cadence.
5. Record findings and risk decisions.
6. Apply approved changes through version control and testing.
7. Verify closure and refresh evidence.

## Cadence

- full NIST CSF evidence review: at least quarterly;
- critical-vendor and privileged-access review: quarterly;
- CI/release/production verification: automatically or per release;
- incident/recovery review: after an incident or tabletop;
- out-of-cycle review: after material architecture, integration, vendor, data-flow, threat or regulatory change.

Sensitive screenshots, contracts, credentials, tokens and unredacted provider exports are retained only in restricted storage. See the [attachment register](provider-console-attachments-required.md).
