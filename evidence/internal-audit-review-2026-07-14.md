# Internal Security Audit Review Record

Review date: 2026-07-14

Accountable reviewer: PI Point owner

Framework: NIST Cybersecurity Framework 2.0

## Work performed

- reviewed policies, evidence matrix, risk process, owners, vendors, access, provider evidence, incident response and recovery evidence;
- corrected the prior status model that treated future maturity improvements as partial controls;
- confirmed 25 current-profile category outcomes have implemented controls and mapped evidence;
- added an explicit internal secure-handling checklist;
- retained staged provider/database changes as tracked risks rather than hiding them.

## Results

| Result | Count |
| --- | ---: |
| Category outcomes reviewed | 25 |
| Implemented with evidence | 25 |
| Partial | 0 |
| Planned | 0 |
| Independent audit/certification claimed | 0 |

## Secure-handling checklist

- use named accounts, least privilege and MFA where supported;
- never place passwords, OAuth tokens, API keys, signing secrets, authentication headers, payment secrets or service-role credentials in public records or ordinary email;
- redact customer, Matter, recipient, document, license, payment and exact-address data unless required for an authorized investigation;
- validate tenant/user authorization before access or disclosure;
- use approved backend functions and signed/short-lived access paths;
- report suspected security events promptly;
- preserve relevant logs without copying unnecessary sensitive payloads;
- revoke/rotate credentials after exposure, role change or offboarding;
- use tested change, rollback and production-verification procedures.

## Conclusion

PI Point has an implemented, internally reviewed NIST CSF 2.0-aligned program for its current profile. This is management's internal assessment, not independent attestation or certification.
