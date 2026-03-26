# UAT plan - customer self-service portal MVP

## objective
verify the MVP behaves as specified, from real end users' perspective, before go-live.

## scope
all MVP user stories in `../user-stories/` plus the non-functional requirements in `../requirements/srs.md`.

## out of scope
- performance load testing (separate NFR test team)
- penetration testing (separate security workstream)

## entry criteria
- all MVP stories accepted by PO in sprint reviews
- SIT complete, no Sev 1 / 2 defects open
- UAT environment up with anonymised production-like data
- testers identified and onboarded

## exit criteria
- 100% of UAT cases executed
- 0 Sev 1 / 2 open
- <= 5 Sev 3 open with agreed workaround or fix-after-launch
- sign-off from sponsor + compliance

## participants
- 6 customer-proxy testers (mix of personas Anna / Karl)
- 1 call centre lead (validates call-deflection flows)
- 1 claims lead (validates FNOL data quality)
- 1 compliance / DPO (audit + consent flows)
- 1 BA - test coordination

## indicative schedule (10 working days)
- day 1 - kickoff, env walkthrough
- day 2-4 - identity, policies, personal data
- day 5-7 - claims (FNOL, status, messaging)
- day 8 - defect triage + fix verification
- day 9 - re-test critical defects + regression spot-check
- day 10 - sign-off meeting

## defect severity
- Sev 1 - blocks a critical journey end-to-end, no workaround
- Sev 2 - major function broken, workaround possible
- Sev 3 - minor function broken or cosmetic but visible
- Sev 4 - trivial / suggestion

## tooling
- Jira project `PORTAL` for defects + traceability
- Confluence space for daily UAT reports
- Zoom for screen-recording evidence

## reporting
daily standup summary + end-of-day report. Final report at sign-off includes: cases executed/passed/failed, open defect list with severities, accepted risks, sign-off statements.
