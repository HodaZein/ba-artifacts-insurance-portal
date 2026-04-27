# BA artifacts - sample insurance customer portal

reference set of BA artifacts for a fictional insurance self-service portal. inspired by real engagements but fully sanitised - no client data, no real product names. I keep this repo as a living example of the kind of stuff I produce during discovery + delivery.

**live site:** https://hodazein.github.io/ba-artifacts-insurance-portal/

## what's here

### requirements
- [scope](requirements/scope.md)
- [srs](requirements/srs.md)
- [glossary](requirements/glossary.md)
- [raci](requirements/raci.md)

### process
- [overview](process/README.md)
- [as-is: phone-based address update](process/as-is-phone.md)
- [to-be: portal self-service](process/to-be-portal.md)
- [address update flow](process/address-update.md)
- [first notice of loss (FNOL)](process/fnol.md)

### user stories
- [overview + index](user-stories/README.md)
- [personas](user-stories/personas.md)
- epics: [identity](user-stories/epic-identity.md) - [personal data](user-stories/epic-personal-data.md) - [policies](user-stories/epic-policies.md) - [claims](user-stories/epic-claims.md)

### uat
- [uat plan](uat/uat-plan.md)
- [test cases](uat/test-cases.md)
- [sign-off template](uat/sign-off.md)

### decisions (ADRs)
- [overview](decisions/README.md)
- [0001 - web only for MVP](decisions/0001-web-only-mvp.md)
- [0002 - MFA optional in MVP](decisions/0002-mfa-optional-mvp.md)

## how to read
start with `requirements/scope.md` for context, then `process/` for the as-is/to-be flows, then `user-stories/` for the backlog.

## conventions
markdown only, github renders the bpmn-as-mermaid. user stories: "As a ... I want ... so that ...". AC is given/when/then-ish, not strict gherkin. ADRs are short, michael-nygard style.
