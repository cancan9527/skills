---
name: prd-review-checklist
description: Review product requirement documents and output issue lists, risks, missing items, and rewrite suggestions before design, development, or testing. Use when a user asks to review a PRD, self-check a requirement document, assess whether a PRD is ready to move forward, or inspect workflow-heavy requirements involving states, buttons, exceptions, approvals, roles, or cross-system writebacks.
---

# PRD Review Checklist

## Overview

Review an existing PRD from a product-review perspective instead of rewriting it from scratch. Focus on whether the document is complete enough, clear enough, and stable enough to enter the next stage.

## Workflow

Follow this sequence:

1. Identify the review context.
2. Scan the PRD structure and determine which sections are present or missing.
3. Review the document against the 10-dimension framework in `references/prd-review-framework.md`.
4. Prioritize blocking issues over polish suggestions.
5. Return a structured review result with conclusion, risks, missing items, and rewrite suggestions.

## Review Context

Infer or confirm these inputs from the user request and PRD:

- Current stage: pre-review, pre-design, pre-development, or pre-testing
- Review focus: generic completeness, workflow logic, state/button rules, data writebacks, approvals, or role/permission clarity
- Domain: general product PRD or workflow-heavy business PRD

If the user does not specify a focus, default to:

- document completeness
- workflow closure
- state/button consistency
- data writeback clarity
- implementation readiness

## Output Rules

Always structure the result in this order:

1. `审查结论`
2. `高风险问题`
3. `缺失项`
4. `补写建议`

At the end of `审查结论`, add a short `维度命中总结` line that states which review dimensions were hit most heavily and what class of weakness they represent.

Use these conclusion labels:

- `可进入下一阶段`
- `补充后再进入下一阶段`
- `暂不建议进入下一阶段`

Use these risk labels:

- `P0 阻塞`
- `P1 高风险`
- `P2 优化项`

Lead with the highest-severity findings. Do not bury blocking issues inside general commentary.
Use `维度命中总结` to explain whether the PRD is mainly weak in scope, roles, objects, workflow closure, exceptions, state/button rules, data writebacks, or implementation readiness.

## Review Heuristics

Apply these heuristics while reviewing:

- Prefer concrete gaps over vague criticism.
- Point to the exact missing rule, missing object, or missing scenario.
- Treat workflow-heavy PRDs as higher-risk when states, buttons, exceptions, approvals, or writebacks are underspecified.
- Separate `缺失项` from `优化建议`.
- Do not ask the user to rewrite everything if a targeted补写 list is enough.

## Workflow-Heavy Requirements

For ERP, MES, approval, document-flow, and operations-heavy PRDs, increase scrutiny on:

- role boundaries
- main and exception flows
- state transitions
- button visibility and disabled logic
- data ownership
- upstream/downstream writebacks

If these areas are underspecified, default the conclusion to at least `补充后再进入下一阶段`.

## Reference Loading

Read `references/prd-review-framework.md` when you need:

- the 10 review dimensions
- the detailed checklist questions
- the standard output template
- workflow-heavy review emphasis

Do not load extra project files unless they are directly relevant to the PRD under review.
