---
name: function-prd-generator
description: Generate a structured product requirement document for a complete feature from scattered inputs such as one-line requests, meeting notes, partial PRDs, prototypes, screenshots, old modules, or workflow descriptions. Use when a user asks to write a PRD, turn rough requirements into a review-ready draft, or organize workflow-heavy requirements involving roles, states, buttons, approvals, exceptions, or cross-system writebacks.
---

# Function PRD Generator

## Overview

Generate a first-draft PRD for a complete feature instead of reviewing an existing PRD. Focus on turning incomplete, scattered, or mixed inputs into a structured document that can move into review, design, development, or testing discussion.

## Workflow

Follow this sequence:

1. Identify the input type.
2. Determine whether the available information is enough to draft a usable PRD.
3. Ask only the highest-value follow-up questions needed to close major gaps.
4. Build the PRD using the standard structure in `references/prd-structure.md`.
5. Generate a first draft that covers both normal flow and implementation-critical rules.
6. Return the draft together with pending questions and key risks.

## Input Types

Treat these as valid starting points:

- one-line feature requests
- meeting notes or chat summaries
- partial PRDs or rough outlines
- prototypes, screenshots, or page descriptions
- old-system pages, old modules, or change requests
- workflow documents or business process explanations

If the user provides mixed inputs, synthesize them before drafting.

## Follow-Up Rules

Do not ask broad or low-value questions by default. Ask only what is needed to prevent a weak or misleading PRD.

Prioritize gaps in this order:

1. background and goal
2. scope and boundary
3. roles and core business objects
4. main flow
5. exception flow
6. states, buttons, writebacks, and cross-system linkage

For workflow-heavy requirements, increase scrutiny on:

- role boundaries
- process closure
- state transitions
- button visibility and enabled logic
- data ownership
- upstream/downstream writebacks

If the user has already given enough context, do not over-question. Draft the PRD and surface residual uncertainty in `待确认问题` instead.

## Output Rules

Always return results in this order:

1. `PRD正文`
2. `待确认问题`
3. `风险与依赖`

The PRD draft should be structured, not free-form. It should be suitable for further review and should clearly separate:

- confirmed content
- inferred but still uncertain content
- unresolved business decisions

## Reference Loading

Read `references/prd-structure.md` when you need:

- the standard PRD chapter skeleton
- what each section should contain
- common missing items by section

Read `references/requirement-question-bank.md` when you need:

- targeted follow-up questions by input type
- structured question sets for incomplete requirements

Read `references/workflow-heavy-prd-guidelines.md` when the requirement is process-heavy and needs stronger treatment of:

- roles and permissions
- main and exception flows
- states and buttons
- data writebacks
- approvals, to-dos, or cross-system linkage

Do not load extra references unless they are directly relevant to the feature being drafted.
