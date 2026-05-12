# PRD Structure

## Purpose

This reference defines the standard chapter skeleton for a complete feature PRD.

Use it to:

- decide which sections should exist in the draft
- determine what each section must contain
- detect which gaps still need follow-up questions
- strengthen workflow-heavy PRDs without rewriting the entire structure

The goal is not to force every PRD into the same length. The goal is to ensure the draft is complete enough to support review, design, development, and testing.

## Standard Skeleton

Use this structure by default:

```markdown
# 功能名称 PRD

## 1. 需求背景
## 2. 目标与价值
## 3. 范围与边界
## 4. 角色与权限
## 5. 核心业务对象
## 6. 主流程
## 7. 异常流程
## 8. 页面与交互说明
## 9. 状态与按钮规则
## 10. 数据口径与回写
## 11. 验收标准
## 12. 风险与待确认项
```

If the feature is small, merge adjacent sections instead of deleting critical logic. If the feature is workflow-heavy, keep the full structure.

## Section Guidance

### 1. 需求背景

Explain why the feature exists.

Should cover:

- requirement source
- current pain point
- business context
- what goes wrong if the feature is not built

Common gaps:

- only describing the solution, not the problem
- no business context
- no explanation of urgency

### 2. 目标与价值

Explain what result the feature is expected to produce.

Should cover:

- target users
- business objective
- expected value
- optional success metrics

Common gaps:

- only listing functions
- no target user
- no measure of success

### 3. 范围与边界

Explain what is included in this version and what is not.

Should cover:

- in-scope capabilities
- out-of-scope items
- first-phase vs later-phase split
- business or system boundaries

Common gaps:

- mixing current scope with future ideas
- no explicit “not in scope”
- unclear system boundary

### 4. 角色与权限

Explain who can see, create, edit, approve, confirm, or manage the feature.

Should cover:

- user roles
- permissions by role
- collaboration between roles
- any visibility or edit restrictions

Common gaps:

- roles named but not differentiated
- buttons described without role constraints
- unclear view-only vs editable states

### 5. 核心业务对象

Explain the key business entities used by the feature.

Should cover:

- object names
- object relationships
- key fields
- unique identifiers when relevant
- parent/child or upstream/downstream relationships

Common gaps:

- page names are clear but objects are not
- mixed naming between business terms and UI labels
- no explanation of one-to-many or many-to-many relationships

### 6. 主流程

Explain the normal happy-path flow from start to finish.

Should cover:

- trigger point
- step-by-step flow
- who acts at each step
- what the system does
- completion condition

Common gaps:

- flow starts clearly but has no end condition
- actions described without system response
- missing handoff between roles

### 7. 异常流程

Explain what happens when the normal flow breaks.

Should cover:

- validation failures
- rejection or return
- cancellation or rollback
- partial completion
- repeated submission
- data or status conflicts

Common gaps:

- only happy path is written
- error messages exist but handling logic does not
- no recovery path after failure

### 8. 页面与交互说明

Explain how the feature appears in the UI and how users operate it.

Should cover:

- page entry points
- page sections or tabs
- dialogs, drawers, or secondary views
- key user actions
- basic interaction rules

Common gaps:

- pages listed without action explanation
- no entry/exit path
- interaction described visually but not behaviorally

### 9. 状态与按钮规则

Explain the state machine and action availability.

Should cover:

- state definitions
- visible buttons by state
- enabled or disabled conditions
- action-to-state transitions
- reversal actions such as撤回、驳回、关闭、重新提交

Common gaps:

- status names exist but transition rules do not
- button visibility depends on role or state but is not stated
- forward flow exists but reverse flow does not

Recommended table:

| 当前状态 | 可见按钮 | 可执行角色 | 前置条件 | 执行动作 | 后置状态 |
| --- | --- | --- | --- | --- | --- |

### 10. 数据口径与回写

Explain which data changes and where it is written back.

Should cover:

- key fields updated by each action
- source of truth
- upstream or downstream writebacks
- cross-system linkage
- update timing and synchronization rules

Common gaps:

- pages describe actions but not field changes
- no source-of-truth definition
- cross-system consequences are implied but not written

### 11. 验收标准

Explain what must be true for the feature to be accepted.

Should cover:

- normal flow acceptance
- exception flow acceptance
- role and permission checks
- state transition checks
- data writeback checks
- optional import/export or notification checks

Common gaps:

- “done” is subjective
- only UI is validated
- no testable conditions

### 12. 风险与待确认项

Separate unresolved business decisions from known risks.

Should cover:

- decisions still requiring confirmation
- external dependencies
- domain uncertainties
- implementation risks

Common gaps:

- uncertainty hidden inside the正文
- no distinction between confirmed vs inferred content

## Recommended Output Shape

When generating the PRD draft, prefer this pattern inside each section:

1. short section purpose
2. structured rules or bullets
3. tables where precision matters

Use tables especially for:

- roles and permissions
- field definitions
- state and button rules
- data writebacks
- acceptance criteria

## Workflow-Heavy Strengthening

For ERP, MES, approval, document-flow, and operations-heavy requirements, strengthen these sections:

- `4. 角色与权限`
- `6. 主流程`
- `7. 异常流程`
- `9. 状态与按钮规则`
- `10. 数据口径与回写`
- `11. 验收标准`

In these cases, do not collapse the structure too aggressively. Precision matters more than brevity.

## Minimum Viable PRD

If the input is incomplete and you still need to draft a first version, the minimum usable PRD should still contain:

- background
- scope
- roles
- main flow
- page actions
- state/writeback assumptions when relevant
- pending questions

If one of these is missing, do not pretend the PRD is complete. Surface the gap in `待确认问题`.
