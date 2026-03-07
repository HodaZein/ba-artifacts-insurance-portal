# SRS — Customer Self-Service Portal (lightweight)

This is an intentionally short SRS focused on the MVP scope. Detailed
behaviour is defined per epic in [`../user-stories/`](../user-stories/).

## 1. Overview
A web portal letting policyholders manage common service tasks online.
See [`scope.md`](scope.md) for goals and stakeholders.

## 2. Functional requirements
| ID    | Requirement                                                          | Priority |
|-------|----------------------------------------------------------------------|----------|
| F-01  | A user can register using a valid email and password                 | Must     |
| F-02  | A user can log in and a session is maintained for 30 minutes idle    | Must     |
| F-03  | A user can enable optional MFA (TOTP authenticator app)              | Should   |
| F-04  | A user can view a list of their active and historical policies       | Must     |
| F-05  | A user can download the policy schedule and certificate as PDF       | Must     |
| F-06  | A user can update postal address, phone, and email                   | Must     |
| F-07  | Email change requires re-verification of the new address             | Must     |
| F-08  | A user can submit a First Notice of Loss for a motor or home policy  | Must     |
| F-09  | A user can attach photos / documents to a claim (max 10, 10 MB ea.)  | Must     |
| F-10  | A user can view current status of an open claim                      | Must     |
| F-11  | A user can exchange messages with the assigned claim handler         | Should   |

## 3. Non-functional requirements
| ID    | Requirement                                                          | Target   |
|-------|----------------------------------------------------------------------|----------|
| N-01  | Time-to-first-document after login (p95)                             | < 30 s   |
| N-02  | Page TTFB on cached login page                                       | < 800 ms |
| N-03  | Availability (business hours)                                        | 99.5%    |
| N-04  | Accessibility                                                        | WCAG 2.1 AA |
| N-05  | All data at rest encrypted                                           | AES-256  |
| N-06  | All data in transit                                                  | TLS 1.2+ |
| N-07  | Personal data retained per existing carrier retention policy         | n/a      |

## 4. Assumptions, dependencies, constraints
See [`scope.md`](scope.md) sections "Assumptions" and "Constraints".

## 5. Open questions
- Q1. Will MFA be mandatory in v2 or remain opt-in?
- Q2. What is the SLA for the policy admin REST API under portal load?
- Q3. Should the portal expose claim history older than 24 months?
