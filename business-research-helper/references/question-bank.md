# Question Bank

## Purpose

This reference provides reusable business research questions for product work.

Use it to:

- design user interview questions
- fill missing requirement context
- probe unclear workflow logic
- identify pain points before writing PRDs

The goal is not to ask every question. The goal is to choose the smallest set of high-value questions that exposes the real business.

## Core Question Categories

### 1. Background Questions

- Why are we researching this topic now?
- What business problem is driving this discussion?
- What happens if this problem is not solved?
- Which teams or users feel the problem most strongly?

### 2. Role Questions

- Which roles participate in this business process?
- Who initiates the process?
- Who handles each step?
- Who approves or confirms the result?
- Who only views the result but does not operate?

### 3. Current Workflow Questions

- How does the process work today from start to finish?
- What is the entry point?
- What are the main steps?
- Which system, spreadsheet, or offline action is used in each step?
- What marks the end of the process?

### 4. Rule Questions

- What conditions decide whether the process can continue?
- What rules determine pass/fail, go/no-go, or status changes?
- Which actions are role-restricted?
- Are there thresholds, caps, or exception limits?

### 5. Exception Questions

- What are the most common exceptions?
- What happens when data is missing or wrong?
- What happens when the process is rejected, returned, or cancelled?
- Are there partial-completion cases?

### 6. Data Questions

- Which fields are most critical?
- Who creates the data?
- Who modifies it later?
- Which system is the source of truth?
- Does any action write back to upstream or downstream records?

### 7. Pain Point Questions

- Which step is the most troublesome today?
- Which step is the most error-prone?
- Where do people rely on manual follow-up?
- Where does repeated entry happen?
- Where do departments usually argue about ownership?

### 8. Goal Questions

- If the process were improved, what should get better first?
- Is the main goal efficiency, accuracy, transparency, or control?
- Which parts are must-fix and which are just nice-to-have?

## Input-Type Question Packs

### One-Line Topic

Use when the user gives only a short topic such as “incoming inspection”.

Recommended minimum set:

1. What business problem are we trying to understand?
2. Which roles are involved?
3. What is the current workflow?
4. What are the main pain points?
5. Are there status changes, approvals, or writebacks involved?

### Existing Requirement but Still Unclear

Use when a requirement exists but the business logic is shaky.

Recommended minimum set:

1. Which business rules are still unclear?
2. Which roles still have ambiguous responsibility?
3. Which part of the process is not fully closed?
4. Which exceptions have not been confirmed?
5. Which data writebacks are still uncertain?

### Interview Preparation

Use when the user is about to meet business stakeholders.

Recommended minimum set:

1. What is the current way of working?
2. What are the most common exceptions?
3. What causes the most delay or rework?
4. Which fields or documents are most critical?
5. Which decisions should the system enforce later?

### Interview Notes Organization

Use when the user already has notes and needs to identify what is missing.

Recommended minimum set:

1. Which facts are already confirmed?
2. Which points are opinions rather than rules?
3. Which roles or steps are still not explained?
4. Which downstream effects are still unclear?
5. What still needs follow-up before requirement writing?

## Role-Based Question Hints

### Ask Operators

Focus on:

- actual steps
- manual actions
- exceptions
- delays
- repeated entry

### Ask Managers or Approvers

Focus on:

- control points
- approval criteria
- risk concerns
- escalation paths
- final decision logic

### Ask Cross-Department Partners

Focus on:

- handoff timing
- source-of-truth ownership
- writebacks
- misunderstandings between teams

## Stop Rule

Stop asking more questions when the following are already clear enough:

- business objective
- current process
- main roles
- critical rules
- major pain points

Move the remaining uncertainty into `后续需求待补问题` instead of forcing a full interview script every time.
