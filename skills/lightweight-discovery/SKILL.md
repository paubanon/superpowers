---
name: lightweight-discovery
description: Use when a task needs some design judgment or tradeoff analysis but does not justify the full brainstorming spec workflow.
---

# Lightweight Discovery

Use this skill for Tier 1 discovery work: tasks that need brief structured thinking, but not a full design ceremony.

**Core principle:** Use the smallest amount of discovery process that still produces a sound recommendation and a clear implementation route.

## When to Use

Use this skill when the task involves some ambiguity, tradeoff, or design judgment, but the scope is still limited.

- isolated behavior changes
- small feature additions
- workflow or instruction changes
- limited-scope UX or copy changes
- tasks that need a short recommendation before implementation

Do not use this for trivial, already-concrete work. Do not use this for work that is still open-ended enough to need a durable spec before implementation.

## Core Workflow

1. Do a short context scan.
2. Ask at most 1-2 clarifying questions unless ambiguity remains high.
3. Propose 2 options with brief tradeoffs.
4. Recommend one option.
5. Explain why that option is the best fit.
6. Choose the implementation route.
7. List escalation triggers.

## Hard Limits

This skill should stay lightweight.

- No mandatory design doc.
- No mandatory git commit before implementation.
- No visual companion by default.
- No long checklist.
- No decomposition unless the scope is obviously too large.
- No more than 2 clarifying questions before giving a recommendation unless the user wants deeper exploration.

## Output Contract

Every run must end with these sections.

### Understanding

One short paragraph that restates the task, constraints, and success criteria.

### Options

#### Option A

1-2 lines of tradeoff.

#### Option B

1-2 lines of tradeoff.

### Recommendation

- Recommended option: <Option A or Option B>
- Why: <why this is the smallest safe fit and why heavier process is not needed yet>
- Implementation route: <Implement now | Implement with short brief | Escalate to full planning>
- Escalation triggers: <conditions that force Tier 2 or full planning>

The `Why` field is mandatory.

### Next Step

End with exactly one of these next-step labels:

- `Implement now`
- `Implement with short brief`
- `Escalate to full planning`

## Implementation Routes

### Implement now

Use when the change is local, concrete, and small enough to execute directly after discovery.

### Implement with short brief

Use when the task is not trivial, but a full implementation plan would be overkill.

The short execution brief must include:

- `Goal`
- `Scope` with included and excluded work
- `Likely files`
- `Execution steps` with 3-5 concrete steps
- `Verification`
- `Stop and escalate if`

### Escalate to full planning

Use when the work becomes multi-step, cross-cutting but already concrete, or worth durable planning.

Route to:

1. `writing-plans`
2. `lightweight-plan-execution` for most resulting plans

## Escalation Triggers

Escalate to full `brainstorming` only when the work is still ambiguous enough to need Tier 2 discovery.

- the user is still exploring product direction after 2 questions
- there are major UX or architecture tradeoffs that are not yet resolved
- the work needs a durable spec before implementation can be planned safely
- discovery expands the scope and the new scope is still open-ended rather than merely larger
