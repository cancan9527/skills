# B端产品经理需求工作流 Skills

这是一组面向 B 端产品经理的可复用 Skills，主要用于支持需求从业务调研、PRD 生成到 PRD 审查的完整工作流。

当前包含 3 个核心 Skill：

- `business-research-helper`
- `function-prd-generator`
- `prd-review-checklist`

它们可以串成一条完整的方法链：

`业务调研 -> PRD生成 -> PRD审查`

---

## Skills 列表

### 1. business-research-helper

用于业务调研和需求摸底，帮助产品经理在写需求前先把业务讲清楚。

适合场景：

- 需求前业务调研
- 用户访谈提纲准备
- 会议纪要 / 调研记录整理
- 流程型业务补调研

典型输入：

- 一句话需求
- 会议纪要
- 访谈记录
- 旧流程 / 原型 / 截图 / 文档

典型输出：

- 调研提纲
- 业务现状整理
- 关键痛点与风险
- 后续需求待补问题

---

### 2. function-prd-generator

用于把零散需求信息整理成结构化 PRD 初稿。

适合场景：

- 调研完成后整理需求文档
- 半成品需求补全
- 流程型需求 PRD 草拟
- 从原型 / 旧模块资料生成一版 PRD

典型输入：

- 业务调研结果
- 半成品需求
- 会议纪要
- 原型 / 截图 / 页面描述
- 旧模块资料

典型输出：

- PRD正文
- 待确认问题
- 风险与依赖

---

### 3. prd-review-checklist

用于审查 PRD 是否足够完整、清晰、稳定，是否适合进入下一阶段。

适合场景：

- PRD 自审
- 评审前检查
- 设计前 / 开发前 / 测试前检查
- 流程型需求质量把关

典型输入：

- PRD 初稿
- 需求文档
- 方案稿
- 页面说明

典型输出：

- 审查结论
- 高风险问题
- 缺失项
- 补写建议
- 维度命中总结

---

## 推荐使用顺序

建议按下面顺序使用这 3 个 Skill：

1. `business-research-helper`
   先把业务现状、角色、流程、规则、痛点梳理清楚

2. `function-prd-generator`
   再把调研结果和零散信息整理成 PRD 初稿

3. `prd-review-checklist`
   最后对 PRD 做结构化审查，提前发现风险和缺项

---

## 目录结构

```text
skills/
├── business-research-helper/
├── function-prd-generator/
└── prd-review-checklist/
