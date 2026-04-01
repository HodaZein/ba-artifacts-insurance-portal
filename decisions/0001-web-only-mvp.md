# ADR-0001 — Web-only MVP, no native mobile app

## Status
Accepted — 2026-02-?? (kick-off workshop)

## Context
Customers expect a mobile-friendly experience. The product team debated
whether to ship a responsive web portal only, or a web portal plus native
iOS/Android apps from day one.

## Decision
Ship a **responsive web portal only** for MVP. Native apps are deferred
to a post-MVP phase, contingent on adoption metrics from the web portal.

## Consequences
- **Positive:** single codebase, faster time-to-market, lower delivery
  cost, no app-store review cycles in the critical path.
- **Negative:** no offline-first experience, no push notifications
  (email only). Camera access for FNOL photos works but with a slightly
  rougher UX than a native app would offer.
- **Risk:** if competitor experience pulls customers to native, plan for
  a v2 native shell that wraps the web app.
