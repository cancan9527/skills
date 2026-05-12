---
name: business-research-helper
description: Prepare, structure, and summarize business research for product work. Use when a user needs help understanding a business domain before writing requirements, improving an incomplete requirement, designing user interview questions, sorting workflow-heavy business logic, identifying pain points, or turning research notes into structured findings for later PRD work.
---

# Business Research Helper

## Overview

Support product managers during business discovery and requirement clarification. Focus on understanding the current business, exposing missing rules, preparing high-value interview questions, and turning scattered research material into structured findings that can feed later requirement definition and PRD writing.

## Workflow

Follow this sequence:

1. Identify the research scenario.
2. Determine what is already known and what is still unclear.
3. Choose the right questioning depth instead of asking everything at once.
4. Organize findings into business current state, roles, process, rules, pain points, and requirement opportunities.
5. Return a structured research output that can directly support requirement refinement.

## Research Scenarios

Use this skill for one or more of these scenarios:

- pre-requirement business discovery
-补调研 for an incomplete requirement or PRD
- interview preparation before meeting business users
-整理 interview notes, chat notes, or workflow notes
- workflow-heavy business analysis such as purchasing, incoming inspection, warehousing, approval, writeback, or exception closure

## Input Types

Treat these as valid starting points:

- one-line business topic
- rough requirement statement
- meeting notes or interview notes
- existing PRD with unclear business logic
- old module descriptions
- process documents, screenshots, prototypes, or workflow charts

If the user provides mixed inputs, synthesize them before deciding what to ask next.

## Follow-Up Rules

Do not start with a giant questionnaire. Ask only the highest-value questions that unblock understanding.

Prioritize in this order:

1. business background and objective
2. roles and responsibilities
3. current workflow
4. rules and judgment points
5. exceptions and edge cases
6. data ownership and writebacks
7. pain points and requirement opportunities

For workflow-heavy research, increase scrutiny on:

- role boundaries
- process handoffs
- state changes
- button or action meaning
- source-of-truth data
- upstream/downstream linkage

If enough information already exists, stop asking and move into structured整理 instead.

## Output Rules

Always return results in a structured way. Choose the closest format below based on the user’s need:

1. `调研提纲`
2. `业务现状整理`
3. `关键痛点与风险`
4. `后续需求待补问题`

If the user explicitly wants interview preparation, lead with `调研提纲`.
If the user explicitly wants整理 after research, lead with `业务现状整理`.

## Reference Loading

Read `references/research-workflow.md` when you need:

- the standard business research flow
- scenario selection guidance
- how to move from调研 to requirement refinement

Read `references/question-bank.md` when you need:

- high-value research questions
- role/process/rule/pain-point oriented question sets
- different packs for different input types

Read `references/workflow-business-research.md` when the topic is process-heavy and needs stronger treatment of:

- status flows
- approvals
- writebacks
- cross-department handoffs
- purchasing, incoming inspection, warehousing, production, or quality scenarios

Read `references/interview-output-template.md` when you need:

- standard output templates
- note整理 structure
- business research summary formats

Do not load extra references unless they are directly relevant to the business topic being researched.
