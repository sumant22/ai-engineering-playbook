# Bug Fixing Skill (v1.0)

## Objective
Fix issues by identifying and resolving the root cause — not by patching symptoms.

---

## Core Principle
Never fix a bug you don’t fully understand.

---

## Process

### 1. Reproduce the Issue
- Confirm the bug exists
- Identify exact steps to reproduce
- If not reproducible → stop and ask for more details

---

### 2. Define Expected vs Actual Behavior
- What should happen?
- What is actually happening?

---

### 3. Narrow Down the Scope
Identify where the issue originates. Common areas include:

- Input (user input, request data, events)
- Processing (business logic, conditions, calculations)
- Data flow (state handling, data transformation, mapping)
- External systems (API, database, third-party services)
- Output (UI rendering, response generation)

Focus on tracing the flow from input → processing → output.

> Note: Adapt these categories based on your domain (e.g., frontend, backend, mobile, etc.).

---

### 4. Identify Root Cause
Trace the issue instead of guessing.

Check for:
- Incorrect conditions or logic
- Null / undefined values
- State/data not updating correctly
- Async timing issues
- Incorrect data mapping

---

### 5. Implement Minimal Fix
- Fix only the root cause
- Avoid rewriting unrelated code
- Do not introduce new abstractions unless necessary

---

### 6. Verify the Fix
- Re-test the original scenario
- Check related flows
- Ensure no regressions are introduced

---

## Rules

- Do not guess fixes
- Do not apply trial-and-error patches
- Do not fix multiple issues at once
- Do not refactor unrelated code

---

## Common Mistakes

- Fixing symptoms instead of root cause
- Skipping reproduction step
- Ignoring edge cases
- Breaking nearby functionality

---

## When to Ask for Clarification

- Issue cannot be reproduced
- Expected behavior is unclear
- Multiple possible root causes exist

---

## Output Format

When fixing a bug, always include:

1. Root cause  
2. What was changed  
3. Why this fix works  
4. What was verified  

---

## Example

**Issue:** Button does not update UI after API call  

**Root Cause:** Data flow was not updated after successful response  

**Fix:** Ensured updated data is passed to the output layer  

**Verification:**
- UI updates correctly after action  
- No impact on other flows  
