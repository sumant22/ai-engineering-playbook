# Flutter UI Skill (v1.0)

## Objective
Build responsive, maintainable, and predictable UI across mobile, tablet, web, and desktop.

---

## Core Principle
UI should be simple, data-driven, and adaptable to different screen sizes without breaking layout or behavior.

---

## Process

### 1. Understand Layout Requirements
- Identify screen type (list, form, dashboard, detail)
- Define required states (loading, empty, error, success)
- Identify target platforms:
  - Mobile
  - Tablet
  - Web/Desktop

Do not start coding until layout and platforms are clear.

---

### 2. Structure Before Styling
- Break UI into logical sections:
  - Header
  - Content
  - Actions
- Keep widget tree shallow and readable
- Avoid deeply nested layouts

---

### 3. Handle UI States Explicitly

Every screen must handle:

- Loading → show loader  
- Empty → show message  
- Error → show error UI  
- Success → show content  

Do not assume data is always available.

---

### 4. Data-Driven UI

- UI must reflect actual state/data
- Avoid hardcoded values
- Ensure UI updates when state changes

---

### 5. Keep Logic Out of UI

- Avoid complex logic inside widgets
- Move logic to BLoC / controller / service layer
- UI should focus on rendering

Exception:
Simple UI conditions (visibility, toggles)

---

### 6. Responsive Design Strategy

Design should adapt based on screen size:

#### Mobile
- Single column layout
- Vertical scrolling
- Compact spacing

#### Tablet
- Wider layout
- Optional 2-column sections

#### Web / Desktop
- Multi-column layout
- Apply max-width constraints
- Center content to avoid stretched UI

---

### 7. Layout Rules for Responsiveness

- Avoid fixed widths/heights unless required
- Use flexible widgets (Expanded, Flexible)
- Apply constraints instead of hard values
- Prevent overflow issues

Common approach:
- Use screen width to adjust layout
- Switch layout structure when needed

---

### 8. Component Strategy

- Extract widget if reused OR improves clarity
- Avoid unnecessary abstraction

Rule:
- Single use → keep inline  
- Reused → extract  

---

### 9. Prevent Common UI Issues

Watch for:
- Overflow errors
- Unbounded height/width
- Incorrect scroll behavior
- UI not updating after state change

---

### 10. Verify Across Devices

Test on:
- Mobile (small screen)
- Tablet (medium screen)
- Web/Desktop (large screen)

Check:
- Layout consistency
- No overflow
- Proper spacing
- Correct behavior

---

## Rules

- Do not build UI without handling states
- Do not hardcode layout values blindly
- Do not mix business logic inside UI
- Do not assume one screen size

---

## Common Mistakes

- Designing only for mobile
- Ignoring tablet/web layouts
- Using fixed sizes causing overflow
- UI not adapting to screen changes

---

## When to Ask for Clarification

- Target platform is not defined
- Responsive behavior is unclear
- Layout requirements are ambiguous

---

## Output Format

When building UI, include:

1. Layout structure  
2. Responsive strategy (mobile/tablet/web)  
3. State handling  
4. Data flow  
5. What was verified  

---

## Example

**Scenario:** Display list of items  

Handled:
- Mobile → single column list  
- Tablet → wider layout  
- Web → centered layout with max width  

States:
- Loading → loader  
- Empty → message  
- Error → error UI  
- Success → list  

Result:
- UI adapts correctly across all screen sizes  
