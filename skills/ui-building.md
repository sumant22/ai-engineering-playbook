# UI Building Skill (v1.0)

## Objective
Build user interfaces that are clear, functional, and easy to maintain.

---

## Core Principle
UI should prioritize clarity, usability, and correctness over visual complexity.

---

## Process

### 1. Understand Requirements
- Identify what needs to be displayed
- Understand user interactions
- Clarify states (loading, empty, error, success)

If unclear → ask before building

---

### 2. Structure the UI
Break UI into logical sections:
- Header / title
- Content area
- Actions (buttons, inputs)
- Feedback (messages, loaders)

Keep structure simple and predictable.

---

### 3. Handle UI States Explicitly
Every UI should account for:

- Loading state  
- Empty state  
- Error state  
- Success state  

Do not assume data is always available.

---

### 4. Keep Components Focused
- Each component should have a single responsibility
- Avoid large, complex components
- Extract only when reuse is clear

---

### 5. Connect Data Properly
- Ensure UI reflects actual data/state
- Avoid hardcoded or stale values
- Update UI when data changes

---

### 6. Keep Logic Out of UI (as much as possible)
- Avoid complex logic inside UI components
- Move processing to appropriate layers when needed

---

### 7. Validate Behavior
- Check interactions (clicks, inputs)
- Verify correct rendering across states
- Ensure no broken or inconsistent UI behavior

---

## Rules

- Do not build UI without handling states
- Do not over-componentize unnecessarily
- Do not mix heavy logic inside UI
- Do not assume ideal data conditions

---

## Common Mistakes

- Ignoring loading or error states
- Creating overly complex components
- Hardcoding values instead of using data
- UI not updating after data change

---

## When to Ask for Clarification

- UI behavior is unclear
- Missing state definitions
- Interaction flow is ambiguous

---

## Output Format

When building UI, include:

1. Structure explanation  
2. States handled  
3. Data flow description  
4. What was verified  

---

## Example

**Scenario:** Display list of items  

**Handled:**
- Loading → show loader  
- Empty → show message  
- Error → show error state  
- Success → show list  

**Result:**
- UI behaves correctly in all states  
