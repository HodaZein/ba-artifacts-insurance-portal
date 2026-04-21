# BA artifacts - sample insurance customer portal

A reference set of BA artifacts for a fictional insurance self-service portal. Inspired by real engagements but fully sanitised - no client data, no real product names.

I keep this repo as a living example of the kind of artifacts I produce during discovery and delivery: BPMN-ish flows, user stories with acceptance criteria, a lightweight SRS, decision records, a UAT plan.

## what's here
- `requirements/` - scope, srs, glossary, raci
- `process/` - process diagrams (mermaid, renders on github)
- `user-stories/` - stories grouped by epic, with AC
- `uat/` - uat plan, test cases, sign-off template
- `decisions/` - small ADRs for the notable choices

## how to read it
start with `requirements/scope.md` for context, then `process/` for the as-is/to-be flows, then `user-stories/` for the backlog.

## conventions
- markdown only, github renders the bpmn-as-mermaid bits
- user stories: "As a ... I want ... so that ..."
- AC: Given / When / Then-ish (not strict gherkin)
- ADRs: short, michael-nygard style
