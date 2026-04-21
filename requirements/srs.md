# SRS - customer self-service portal (MVP)

Intentionally short. Detailed behaviour lives per epic in `../user-stories/`.

## 1. overview
Web portal letting policyholders manage common service tasks online. See `scope.md` for goals + stakeholders.

## 2. functional requirements
- F-01 register with valid email + password (must)
- F-02 log in, session 30 min idle (must)
- F-03 optional MFA via TOTP authenticator (should)
- F-04 view active + historical policies (must)
- F-05 download policy schedule + certificate as PDF (must)
- F-06 update postal address, phone, email (must)
- F-07 email change requires re-verification of the new address (must)
- F-08 submit FNOL for motor + home (must)
- F-09 attach photos / docs to a claim, max 10 files, 10MB each (must)
- F-10 view current status of an open claim (must)
- F-11 exchange messages with assigned claim handler (should)

## 3. non-functional requirements
- N-01 time-to-first-document after login: < 30s p95
- N-02 page TTFB on cached login page: < 800 ms
- N-03 availability (business hours): 99.5%
- N-04 accessibility: WCAG 2.1 AA
- N-05 data at rest: AES-256
- N-06 data in transit: TLS 1.2+
- N-07 retention follows existing carrier policy

## 4. open questions
- Q1 will MFA become mandatory in v2 or stay opt-in? (lean mandatory, see ADR-0002)
- Q2 SLA for the policy admin REST API under portal load - waiting on IT
- Q3 should the portal show claim history older than 24 months? sponsor to confirm
