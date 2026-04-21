# Project scope - customer self-service portal

## Context
Mid-size general insurance carrier offering motor, home and travel policies. Today, customers call a call centre for documents, claim submission, simple data updates. Avg handling time around 7 min per request and the call centre is a known cost centre.

## Goal
Self-service web portal that lets policyholders do the most common low-risk service tasks online. Target: cut inbound call volume ~30% within 12 months of go-live.

## In scope (MVP)
- registration + login (email + password, optional MFA)
- policy overview (active + historical)
- document download (policy schedule, certificate of insurance)
- update personal data (address, phone, email - email needs re-verification)
- FNOL for motor + home claims
- claim status tracking
- secure messaging with the assigned claim handler

## Out of scope (MVP)
- online quote-and-buy
- premium payment management (stays in finance system)
- broker-facing functionality
- native mobile apps (see ADR-0001)

## Success metrics
- inbound call volume (service requests): -30% vs baseline at 12 months
- FNOL via portal: at least 40% of all FNOLs at 12 months
- post-task CSAT: >= 4.2 / 5
- time-to-first-document after login: < 30s p95

## Stakeholders
- Head of Operations - sponsor, owns the P&L
- Call centre lead - SME, beneficiary of call deflection
- Claims lead - SME, owner of FNOL + claim status
- Compliance / DPO - GDPR + insurance distribution regulation
- IT architecture - integration with policy admin + claims systems

## Assumptions
- policy admin system exposes a REST API for policy reads
- claims system supports webhooks for status changes
- single SSO identity provider for customer accounts

## Constraints
- GDPR, EU data residency
- IDD (insurance distribution directive) - pre-contract info
- WCAG 2.1 AA
- 6 calendar months to MVP
