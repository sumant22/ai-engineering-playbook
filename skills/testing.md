# Testing Skill (v1.0)

## Objective
Ensure features work correctly, handle edge cases, and do not break existing behavior.

---

## Core Principle
Do not assume correctness — verify behavior through structured testing.

---

## Process

### 1. Identify What to Test
Focus on critical areas:

- UI behavior
- Data flow
- API responses
- User interactions
- Edge cases

---

### 2. Define Test Scenarios

For every feature, define:

#### Primary (Golden Path)
- Main expected behavior works correctly

#### Edge Cases
- Empty data
- Error responses
- Invalid inputs
- Loading states

#### Failure Cases
- API failure
- Network issues
- Unexpected/null data

---

### 3. UI Testing

Verify:

- All states are handled:
  - Loading
  - Empty
  - Error
  - Success
- UI updates when data changes
- No layout issues (overflow, misalignment)
- Responsive behavior (mobile, tablet, web)

---

### 4. API Testing

Verify:

- Correct request is sent
- Response is validated before use
- Error handling works correctly
- No crashes on invalid data

---

### 5. Data Flow Testing

Ensure:

- Data moves correctly from API → state → UI
- UI reflects updated data
- No stale or hardcoded values

---

### 6. Interaction Testing

Test:

- Button clicks
- Form inputs
- Navigation flows

Ensure expected behavior occurs after each action.

---

### 7. Regression Check

After changes:

- Verify related features are not broken
- Re-test critical flows

---

## Rules

- Do not rely only on visual checks
- Do not skip edge cases
- Do not assume API always succeeds
- Do not ignore error states

---

## Common Mistakes

- Testing only happy path
- Ignoring error/empty states
- Not testing responsiveness
- Breaking existing features unknowingly

---

## When to Ask for Clarification

- Expected behavior is unclear
- Edge cases are not defined
- API response behavior is inconsistent

---

## Output Format

When testing, include:

1. Test scenarios covered  
2. Edge cases tested  
3. Issues found (if any)  
4. What was verified  

---

## Example

**Feature:** Display list from API  

Tested:
- Loading → loader shown  
- Empty → “No data” message  
- Error → error UI  
- Success → list displayed  

API:
- Handled success + failure  

Result:
- Feature works across all states  
