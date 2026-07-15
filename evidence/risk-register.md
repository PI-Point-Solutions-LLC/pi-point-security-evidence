# PI Point Cybersecurity Risk Register — Sanitized External Version

Register date: 2026-07-14

Owner: PI Point security program owner

Review cadence: quarterly and after material incident, architecture, provider, data-flow or threat change.

| ID | Risk | CSF areas | Likelihood | Impact | Current controls | Treatment | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| R-001 | Security evidence becomes distributed or stale | GV.OV, GV.RM, ID.IM | Medium | Medium | Evidence matrix/repository, internal audit and dated reviews | Quarterly link/status review | Mitigated / monitored |
| R-002 | Privileged or service access exceeds need | GV.OV, PR.AA | Low–Medium | High | Named accounts, least privilege, MFA where supported and access review | Quarterly review and incident-triggered revocation | Mitigated / monitored |
| R-003 | Database permission change breaks workflows or creates unintended access | PR.AA, PR.DS, PR.PS | Medium | High | RLS, tests, staged changes, caller mapping, rollback and verification | Small tested batches; accept/stage only with rationale | Staged-sensitive |
| R-004 | Application/dependency vulnerability affects production | ID.RA, PR.PS, PR.MA | Medium | High | Dependency/provider review, CI/release gates, intake and remediation targets | Critical 24–72h; High 7d; Medium 30d; Low 90d/maintenance | Mitigated / ongoing |
| R-005 | OAuth/API credential exposure | PR.AA, PR.DS, RS.MI | Low–Medium | High | Server-side secrets, AES-GCM token encryption, restricted access and redacted logs | Rotate/revoke and investigate suspected exposure | Mitigated / monitored |
| R-006 | Critical provider outage or incident | GV.SC, PR.IR, DE.CM, RC.RP | Medium | High | Vendor review, monitoring, continuity/incident processes and backup evidence | Coordinate response, communicate and validate recovery | Mitigated / monitored |
| R-007 | Integration data reaches optional AI | GV.RM, PR.DS | Low | High | Policy/architecture separate optional CRM AI from Smokeball data | Review on provider or data-flow change | Mitigated / monitored |
| R-008 | Incident/recovery process is not exercised frequently enough | RS.MA, RS.IM, RC.RP, RC.IM | Medium | Medium | Policies, ownership, tabletop and review cadence | Repeat exercises and close corrective actions | Mitigated / ongoing |

This is the actual sanitized register supplied for due diligence. It omits exploit detail, customer information, credentials, provider identifiers and confidential remediation detail.
