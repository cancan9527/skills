# Interview Output Template

## Purpose

This reference defines suggested output shapes for business research work.

Use it to turn raw questions, notes, or discussions into structured product artifacts.

## Output Type 1: 调研提纲

Use when the user is preparing to talk to business stakeholders.

```markdown
## 调研目标
- 这次想搞清楚什么

## 建议访谈角色
- 角色A：为什么要问
- 角色B：为什么要问

## 必问问题
- 问题1
- 问题2

## 可选追问
- 问题A
- 问题B

## 这次调研后需要确认的关键判断
- 判断1
- 判断2
```

## Output Type 2: 业务现状整理

Use when the user already has notes and wants a structured summary.

```markdown
## 业务背景
- 当前为什么要处理这个业务

## 关键角色
- 角色A：职责
- 角色B：职责

## 当前流程
1. 第一步
2. 第二步
3. 第三步

## 关键规则
- 规则1
- 规则2

## 异常与边界场景
- 异常1
- 异常2
```

## Output Type 3: 痛点与风险整理

Use when the user wants to understand what is broken or risky.

```markdown
## 核心痛点
- 痛点1
- 痛点2

## 风险点
- 风险1
- 风险2

## 最容易引发需求反复的地方
- 反复点1
- 反复点2
```

## Output Type 4: 后续需求待补问题

Use when the user is moving from research into requirement definition.

```markdown
## 还需要确认的问题
1. 问题1
2. 问题2

## 这些问题分别影响什么
- 问题1：影响范围 / 状态 / 权限 / 回写
- 问题2：影响流程 / 验收 / 联动
```

## Combining Outputs

For most product work, the best combined output order is:

1. `业务现状整理`
2. `关键痛点与风险`
3. `后续需求待补问题`

If the user is still before the interview stage, prefer:

1. `调研提纲`
2. `建议访谈角色`
3. `必问问题`
4. `可选追问`

## Quality Standard

A good research output should make it easy for the next step to happen.

That next step may be:

- writing a PRD
- reviewing a PRD
- drawing a workflow
- defining status and button rules

If the output is still just a transcript, it is not finished yet.
