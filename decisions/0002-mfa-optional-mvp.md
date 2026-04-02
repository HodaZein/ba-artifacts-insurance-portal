# ADR-0002 — MFA optional in MVP, mandatory in v2

## Status
Accepted — 2026-03-??

## Context
The MVP must balance security with adoption friction. Mandating MFA at
launch could deter less digitally confident customers (persona "Karl"),
while leaving MFA out entirely creates account-takeover risk.

## Decision
Ship MFA as **optional** in the MVP, with strong nudges toward enabling
it. Re-evaluate adoption and incident data 6 months after launch and
make MFA mandatory in v2 for any customer who logs in.

## Consequences
- **Positive:** lower friction at launch, more first-time logins.
- **Negative:** lower baseline security; account-takeover monitoring
  becomes more important.
- **Mitigation:** all sensitive actions (email change, FNOL submission)
  trigger an out-of-band confirmation email even without MFA.
