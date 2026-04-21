# BA artifacts - sample insurance customer portal

reference set of BA artifacts for a fictional insurance self-service portal. inspired by real engagements but fully sanitised - no client data, no real product names. I keep this repo as a living example of the kind of stuff I produce during discovery + delivery.

## what's here
- `requirements/` - scope, srs, glossary, raci
- `process/` - process diagrams (mermaid, renders on github)
- `user-stories/` - stories grouped by epic with AC
- `uat/` - uat plan, test cases, sign-off template
- `decisions/` - small ADRs for the notable choices

## how to read
start with `requirements/scope.md` for context, then `process/` for the as-is/to-be flows, then `user-stories/` for the backlog.

## conventions
markdown only, github renders the bpmn-as-mermaid. user stories: "As a ... I want ... so that ...". AC is given/when/then-ish, not strict gherkin. ADRs are short, michael-nygard style.
