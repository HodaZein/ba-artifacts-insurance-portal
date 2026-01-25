# BA Artifacts — Sample Insurance Customer Portal

A reference set of Business Analyst artifacts for a fictional **insurance
self-service portal** project. Inspired by real engagements but fully
sanitised — no client data, no real product names.

I keep this repo as a living example of the BA artifacts I produce during
discovery and delivery: BPMN flows, user stories with acceptance criteria,
a lightweight SRS, decision records, and a UAT plan.

## Contents
| Folder           | What's inside                                              |
|------------------|------------------------------------------------------------|
| `requirements/`  | High-level scope, SRS, glossary, RACI                      |
| `process/`       | BPMN-style process diagrams (Mermaid) for key journeys     |
| `user-stories/`  | User stories grouped by epic, with acceptance criteria     |
| `uat/`           | UAT plan, test cases, sign-off template                    |
| `decisions/`     | Architecture / scope decision records (ADR-style)          |

## How to read this repo
Start with [`requirements/scope.md`](requirements/scope.md) for the
project context, then [`process/`](process/) for the as-is / to-be flows,
then [`user-stories/`](user-stories/) for the backlog.

## Stack & conventions
- Markdown-only, GitHub renders BPMN via Mermaid.
- User stories follow the `As a ... I want ... so that ...` pattern.
- Acceptance criteria written in **Given / When / Then** (Gherkin-ish).
- ADRs follow the [Michael Nygard ADR template](https://cognitect.com/).
