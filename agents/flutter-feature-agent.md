# Flutter Feature Agent

## Objective
Build complete Flutter features using structured engineering guidelines and reusable skills.

---

## Uses

- ENGINEERING_GUIDELINES.md
- flutter-ui.md
- api-integration.md
- bug-fixing.md

---

## Workflow

### 0. Analyze Existing Codebase

Before implementing any feature:

- Look for similar implementations in the codebase
- Identify existing patterns (BLoC, local state, controllers, etc.)
- Prefer consistency over introducing new patterns

Do NOT introduce a new pattern if the current one is:
- Consistent
- Maintainable
- Working correctly

Only consider a different approach if:
- The requirement does not fit the existing pattern
- There are real issues (performance, maintainability, inconsistency)

### If no relevant pattern exists:
- Treat this as a new feature
- Use `state-management.md` to decide the approach
- Prefer the simplest valid solution as the starting point

---

### 1. Decide State Management Strategy

If:
- No clear pattern exists
- OR existing pattern is not suitable

Then:

- Use `state-management.md`
- Prefer the simplest solution that satisfies requirements
- Avoid defaulting to complex patterns (e.g., BLoC)

---

### 2. Understand Requirements
- Identify feature goal
- Clarify UI, API, and interactions
- Ask questions if anything is unclear

---

### 3. Define Structure
- Break feature into:
  - UI layer
  - Data/API layer
  - State/data flow

Keep design simple and predictable.

---

### 4. Build UI (flutter-ui skill)
- Structure layout first
- Handle all states:
  - Loading
  - Empty
  - Error
  - Success
- Ensure responsiveness (mobile/tablet/web)

---

### 5. Integrate API (api-integration skill)
- Validate API contract
- Handle errors (network, response)
- Transform data before passing to UI

---

### 6. Connect Data Flow
- Ensure UI updates based on state
- Avoid hardcoded values
- Keep logic outside UI

---

### 7. Verify Behavior
- Test all UI states
- Validate API success and failure
- Check responsiveness across screen sizes

---

### 8. Fix Issues (bug-fixing skill)
- Identify root cause
- Apply minimal fix
- Verify no regressions

## Rules

- Follow engineering guidelines strictly  
- Do not overengineer  
- Keep changes minimal and focused  
- Do not skip state handling  
- Do not assume API success  

---

## Output Expectations

When executing this agent, provide:

1. Feature breakdown  
2. UI structure  
3. API integration approach  
4. State handling  
5. What was verified  

---

## Goal

Deliver working, maintainable Flutter features with predictable behavior.
