# Requirement Question Bank

## Purpose

This reference defines how to ask follow-up questions before generating a PRD draft.

Use it to:

- decide whether follow-up questions are needed at all
- prioritize the smallest set of high-value questions
- adapt the questions to the user’s input type
- strengthen workflow-heavy requirements without over-questioning

The goal is not to ask everything. The goal is to ask just enough to avoid generating a weak or misleading PRD.

## Core Rule

Ask questions only when missing information would materially weaken one of these areas:

- background and goal
- scope and boundary
- roles and permissions
- core business objects
- main flow
- exception flow
- state/button rules
- data writebacks or cross-system linkage

If the user has already provided enough information to draft a review-ready first version, do not keep asking. Generate the PRD and surface the remaining uncertainty in `待确认问题`.

## Follow-Up Priority

Ask in this order:

1. why this feature exists
2. what this version includes and excludes
3. who uses it and who handles it
4. what the key business objects are
5. how the normal flow works
6. what happens when the flow fails or changes
7. how states, buttons, and writebacks behave

If you can only ask a few questions, prioritize the first missing items in this order rather than trying to cover everything.

## Do-Not-Ask Rules

Avoid asking:

- questions that can be inferred safely from the provided material
- low-value formatting questions
- every section question at once
- detailed implementation questions before the business flow is clear

Do not turn the interaction into an interview unless the input is genuinely too thin to draft anything useful.

## Base Question Set

Use these as the first-pass question categories.

### 1. Background and Goal

- Why is this feature being proposed now?
- What business problem or user pain does it solve?
- Who benefits most from it?
- What result should improve if this feature works?

### 2. Scope and Boundary

- What is included in this version?
- What is explicitly not included?
- Is this a new feature, a change to an old feature, or a partial upgrade?
- Are there adjacent functions that should stay out of scope for now?

### 3. Roles and Permissions

- Which roles are involved?
- Which role initiates the process?
- Which role reviews, edits, approves, or confirms?
- Are there visibility or edit restrictions by role?

### 4. Core Business Objects

- What are the main business objects or documents in this feature?
- Are they one-to-one, one-to-many, or many-to-many?
- Are there important identifiers, states, or key fields?
- Is there an upstream or downstream object this feature depends on?

### 5. Main Flow

- What is the entry point?
- What are the main steps from start to finish?
- Who performs each step?
- What marks the process as complete?

### 6. Exception Flow

- What happens if a step fails validation?
- Can the process be cancelled, withdrawn, rejected, or reopened?
- What happens when data is missing, duplicated, or conflicting?
- Is there a partial-completion scenario?

### 7. State, Button, and Writeback Rules

- What states exist?
- What buttons or actions are available in each state?
- Which actions change the state?
- Which fields or external records are updated after each action?

## Input-Type Question Packs

Choose the pack that best matches the user’s input. Combine packs only when needed.

### One-Line Requirement

Use when the user gives only a short statement such as “make a special certificate application flow”.

Ask for:

- business background
- target roles
- version scope
- main process
- major outputs or results

Recommended minimum set:

1. What problem is this feature solving?
2. Which roles use it?
3. What should this version cover?
4. What is the normal flow from start to finish?
5. Does it involve states, approvals, or cross-system updates?

### Meeting Notes or Chat Summary

Use when the user provides fragmented discussion material.

Ask for:

- missing business decisions
- unresolved scope
- unclear object names
- unclear ownership between roles

Recommended minimum set:

1. Which points in these notes are already decided?
2. Which parts are still open for confirmation?
3. What is the main process we should treat as baseline?
4. Which roles are responsible for each step?

### Partial PRD or Outline

Use when the user already has sections but the document is incomplete.

Ask for:

- missing sections
- unclear rules
- unclosed flow
- missing exceptions or writebacks

Recommended minimum set:

1. Which parts are confirmed and should be preserved?
2. Which chapters are still incomplete?
3. Which states, buttons, or role rules are still unclear?
4. Are there any missing exception or linkage rules?

### Prototype, Screenshot, or Page Description

Use when the UI exists but the rules do not.

Ask for:

- entry point
- action meaning
- business rule behind key controls
- post-action system behavior

Recommended minimum set:

1. What business action does each key button represent?
2. Who can use each action?
3. What should happen after each action?
4. Are any actions limited by state or permission?

### Old Module, Existing System, or Change Request

Use when the new PRD is based on an old page or an existing workflow.

Ask for:

- current-state baseline
- intended change
- unchanged parts
- migration or compatibility considerations

Recommended minimum set:

1. What stays the same from the old feature?
2. What is changing in this version?
3. Are any old rules being removed or replaced?
4. Does the change affect upstream or downstream modules?

## Workflow-Heavy Question Pack

Use this when the requirement resembles ERP, MES, approval flow, order flow, document flow, or any operations-heavy process.

Prioritize questions in these categories:

### Roles

- Who initiates the process?
- Who processes each stage?
- Who approves, confirms, or closes it?
- Which actions are restricted by role?

### Main Flow

- What is the exact start condition?
- What is the step-by-step normal process?
- What is the completion condition?

### Exceptions

- Can the process be rejected, returned, withdrawn, cancelled, or reopened?
- What happens if only part of the process succeeds?
- What happens when a later step discovers an earlier error?

### State and Button Rules

- What states exist at the parent level and sub-flow level?
- What actions are visible in each state?
- Which actions should be disabled rather than hidden?
- Which actions create irreversible changes?

### Data and Writebacks

- Which fields change after each action?
- Which parent object or downstream object must be updated?
- What is the source of truth?
- Does the change trigger to-dos, notifications, or external synchronization?

## When to Stop Asking

Stop follow-up questions and generate the PRD when:

- the main business goal is clear
- the current scope is clear enough
- the main roles are known
- the happy path is understandable
- the most dangerous rule gaps have been surfaced

At that point, move remaining uncertainty into `待确认问题` instead of prolonging the interview.

## Output Reminder

After using this question bank, the generated result should still be returned in three parts:

1. `PRD正文`
2. `待确认问题`
3. `风险与依赖`

Use the questions only to improve the draft. Do not output the raw question bank unless the user explicitly asks for it.
