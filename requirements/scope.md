# Project Scope — Customer Self-Service Portal

## Context
The client is a mid-size general insurance carrier offering motor, home
and travel policies. Today, customers contact a call centre to retrieve
documents, submit claims, or update personal data. Average handling time
per request is **~7 minutes** and the call centre is a known cost centre.

## Goal
Deliver a **self-service web portal** that lets policyholders perform
the most common, low-risk service tasks online, reducing inbound call
volume by an estimated **30%** within 12 months of go-live.

## In scope (MVP)
- Customer registration and login (email + password, optional MFA)
- Policy overview (active and historical)
- Document download (policy schedule, certificate of insurance)
- Personal data updates (address, phone, email — with re-verification)
- First Notice of Loss (FNOL) for motor and home claims
- Claim status tracking
- Secure messaging with claim handler

## Out of scope (MVP)
- Online policy purchase or quote-and-buy
- Premium payment management (handled by existing finance system)
- Broker-facing functionality
- Native mobile applications

## Success metrics
| Metric                                    | Baseline | Target (12 mo) |
|-------------------------------------------|----------|----------------|
| Inbound call volume (service requests)    | 100%     | -30%           |
| FNOL submissions via portal               | 0%       | ≥ 40%          |
| Customer satisfaction (CSAT, post-task)   | n/a      | ≥ 4.2 / 5      |
| Time-to-first-document after login        | n/a      | < 30 s (p95)   |

## Stakeholders
| Stakeholder         | Role                                            |
|---------------------|-------------------------------------------------|
| Head of Operations  | Sponsor, P&L owner                              |
| Call Centre Lead    | SME, beneficiary of call-deflection             |
| Claims Lead         | SME, owner of FNOL & claim-status flows         |
| Compliance / DPO    | GDPR & insurance-distribution regulation        |
| IT Architecture     | Integration with policy admin & claims systems  |

## Assumptions
- The existing policy admin system exposes a REST API for policy reads.
- The claims system supports webhook notifications for status changes.
- A single SSO identity provider will be used for customer accounts.

## Constraints
- GDPR; data residency in the EU.
- Insurance Distribution Directive (IDD) — pre-contract information.
- Web Content Accessibility Guidelines (WCAG) 2.1 AA.
- Project budget timeline locked at **6 calendar months** to MVP.
