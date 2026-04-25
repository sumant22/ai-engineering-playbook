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

### 1. Understand Requirements
- Identify feature goal
- Clarify UI, API, and interactions
- Ask questions if anything is unclear

---

### 2. Define Structure
- Break feature into:
  - UI layer
  - Data/API layer
  - State/data flow

Keep design simple and predictable.

---

### 3. Build UI (flutter-ui skill)
- Structure layout first
- Handle all states:
  - Loading
  - Empty
  - Error
  - Success
- Ensure responsiveness (mobile/tablet/web)

---

### 4. Integrate API (api-integration skill)
- Validate API contract
- Handle errors (network, response)
- Transform data before passing to UI

---

### 5. Connect Data Flow
- Ensure UI updates based on state
- Avoid hardcoded values
- Keep logic outside UI

---

### 6. Verify Behavior
- Test all UI states
- Validate API success and failure
- Check responsiveness across screen sizes

---

### 7. Fix Issues (bug-fixing skill)
- Identify root cause
- Apply minimal fix
- Verify no regressions

---

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
