# State Management Decision Guide

> Consistency with the existing codebase is more important than theoretical best practices.

This guide is used ONLY when:
- No clear pattern exists in the codebase
- OR the current pattern is not suitable

---

## Default Behavior (No Existing Pattern)

If this is a new feature with no prior reference:

- Start with the simplest valid approach
- Avoid introducing complex state management unless clearly required
- Prefer local state first, then scale if needed

---

## Step 1: Is data coming from an external source?
(API, database, websocket)

- Yes → Use BLoC / Controller / Service layer
- No → Go to Step 2

---

## Step 2: Is the state shared across multiple widgets or screens?

- Yes → Use BLoC / Controller
- No → Go to Step 3

---

## Step 3: Is this simple UI state?
(search filter, toggle, input field, local interaction)

- Yes → Use local state:
  - setState
  - ValueNotifier
  - ValueListenableBuilder
- No → Go to Step 4

---

## Step 4: Is the logic complex or expected to grow?

- Yes → Consider structured state management (e.g., BLoC)
- No → Keep it simple (local state)

---

## When to Change Existing Pattern

Only change the current pattern if:

- There are performance issues
- Code is difficult to maintain or extend
- The same feature uses inconsistent approaches

---

## Important Rules

- Do NOT default to BLoC
- Prefer the simplest solution first
- Follow existing codebase patterns when available
- Optimize for readability and maintainability
