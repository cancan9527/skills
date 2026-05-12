# PRD Review Framework

## Purpose

Use this framework to review an existing PRD and decide whether it is ready to move into design, development, or testing.

The review should answer four questions:

1. What is wrong?
2. What is risky?
3. What is missing?
4. What should be rewritten or supplemented?

## Output Template

Use this structure:

```markdown
## 审查结论
- 可进入下一阶段 / 补充后再进入下一阶段 / 暂不建议进入下一阶段
- 维度命中总结：本次问题主要集中在 X、Y、Z 维度，说明这份 PRD 的主要短板属于 ________

## 高风险问题
- [P0/P1/P2] 问题描述

## 缺失项
- 缺了什么

## 补写建议
- 建议补什么
```

## Risk Levels

- `P0 阻塞`: Do not recommend moving forward until fixed.
- `P1 高风险`: Likely to cause review churn, implementation ambiguity, or rework.
- `P2 优化项`: Not blocking, but worth improving.

## 维度命中总结规则

Add a `维度命中总结` line at the end of `审查结论`.

Purpose:

- summarize where the review findings are concentrated
- help the reader understand the dominant weakness class of the PRD
- turn a list of issues into a structured diagnosis

Writing pattern:

- `本次问题主要集中在 3、4、5、8、9 维度，说明这份 PRD 的主要短板不在背景描述，而在角色权限、业务对象定义、流程闭环、状态按钮规则和数据回写联动。`

Keep it short:

- mention the most heavily hit dimensions only
- describe the weakness class in one sentence
- do not repeat every issue verbatim

## 10 Review Dimensions

### 1. 需求背景与目标

Check:

- Why is this requirement being done now?
- What problem or pain point does it solve?
- Who is affected?
- What does success look like?
- What happens if the requirement is not implemented?

Typical problems:

- Has feature description but no business reason
- Has pages but no success criteria

### 2. 范围与边界

Check:

- What is included in this phase?
- What is explicitly out of scope?
- Is phase-one scope separated from future ideas?
- Are assumptions mixed with committed scope?
- Are there vague boundaries likely to cause dispute later?

Typical problems:

- Scope is too broad
- “Should have later” is mixed into “must have now”

### 3. 用户角色与权限

Check:

- Which roles are involved?
- What can each role view, edit, submit, approve, or revoke?
- Are there permission differences or read-only views?
- Are special roles missing, such as admin, approver, or observer?
- Are cross-role handoffs clear?

Typical problems:

- Role names exist but permissions do not
- Approval role and operation role are mixed together

### 4. 核心业务对象定义

Check:

- Which core business objects are involved?
- Are names consistent across the document?
- Are key fields defined?
- Are parent-child or upstream-downstream relationships clear?
- Are page labels and business terms aligned?

Typical problems:

- Same object appears under different names
- Pages exist but data objects are not defined

### 5. 主流程闭环

Check:

- Is the happy path complete from start to finish?
- Who triggers each step?
- What does the system do at each step?
- What is the start condition and end condition?
- Is the flow consistent with page descriptions?

Typical problems:

- Steps are skipped or implied but not written
- Flow starts and ends clearly but middle logic is missing

### 6. 异常流程与边界场景

Check:

- Are reject, withdraw, cancel, timeout, failure, and retry covered?
- Are empty data, over-limit, permission denial, and state conflicts covered?
- Are partial success and partial completion scenarios covered?
- Is there a return path after failure?
- Are error messages present without processing rules?

Typical problems:

- Only ideal flow is documented
- Error prompts exist but resolution path does not

### 7. 页面与交互动作

Check:

- Are all relevant pages listed?
- Are entry and exit paths clear?
- Are key actions on each page complete?
- Are modal, drawer, confirmation, and warning interactions specified?
- Do page actions genuinely support the business flow?

Typical problems:

- Buttons are named, but what they do is unclear
- Interaction exists visually but lacks business meaning

### 8. 状态、按钮与流转规则

Check:

- What states exist?
- Which buttons are visible, enabled, or disabled in each state?
- What state change happens after each action?
- Are reverse actions such as revoke, reject, close, or rollback supported?
- Are state rules, button rules, and workflow rules consistent?

Typical problems:

- State list exists but button behavior does not
- Button rules conflict with flow description

### 9. 数据口径、回写与系统联动

Check:

- Which fields change after submit, approve, confirm, or complete?
- Which object receives the writeback?
- Does the PRD define upstream/downstream synchronization?
- Are cross-system integrations covered, such as inventory, purchasing, quality, or approval systems?
- Is there a risk that UI state changes without business data being updated?

Typical problems:

- UI action is defined but writeback target is not
- State changes are described without ownership of the source of truth

### 10. 验收标准与落地可执行性

Check:

- Does each core capability have acceptance criteria?
- Can testing derive test cases from the PRD?
- Can development split work from the PRD?
- Can design produce screens from the PRD?
- Is there enough clarity to judge release readiness?

Typical problems:

- Feature exists but “done” is not defined
- Teams need verbal clarification before they can proceed

## Workflow-Heavy PRD Emphasis

Raise the severity when these are missing:

- state transition rules
- button visibility and disable conditions
- role-specific actions
- exception and rollback flows
- data ownership
- writeback targets
- cross-system synchronization

For these PRDs, incomplete logic in the above areas is usually at least `P1 高风险`, and often `P0 阻塞`.
