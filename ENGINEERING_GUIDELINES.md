# Engineering Guidelines (v1.2)

These guidelines define how problems should be understood, approached, and solved when building software with or without LLMs.

**Principle:** Favor clarity, simplicity, and correctness over speed.

---

## 1. Deliberate Before Implementation

Do not assume. Make uncertainty explicit.

- State assumptions before writing code  
- If multiple interpretations exist, present them clearly  
- Ask questions when requirements are unclear  
- Call out tradeoffs (e.g., simplicity vs flexibility)  
- If a simpler approach exists, propose it first  
- If something is unclear, stop and clarify  

---

## 2. Prefer Minimal Solutions

Solve the problem with the least necessary complexity.

- Do not add features beyond the request  
- Avoid premature abstractions, especially for single-use logic  
- Do not introduce speculative flexibility or configuration  
- Avoid handling unrealistic scenarios  
- Continuously ask: “Can this be simpler?”  

---

## 3. Make Targeted Changes

Modify only what is required to achieve the goal.

- Do not refactor unrelated code  
- Do not “clean up” adjacent areas without instruction  
- Match the existing structure and style  
- Remove only the unused code introduced by your changes  
- If unrelated issues are found, mention them but do not fix  

**Test:** Every change should directly support the task.

---

## 4. Work Toward Verifiable Outcomes

Define success in concrete, testable terms.

Transform vague tasks into checks:

- “Fix bug” → Reproduce → Fix → Verify  
- “Add validation” → Define invalid cases → Verify behavior  
- “Refactor” → Ensure behavior remains unchanged  

Execution loop:
Implement → Verify → Adjust → Re-verify → Final check  

Avoid vague success criteria like “it works.”

**UI is considered complete when:**
- Main flow works (golden path)  
- Loading, empty, and error states are handled  
- No nearby functionality is broken  
- Behavior is verified, not just types  

---

## 5. Communicate Decisions Clearly

Make reasoning visible.

- Explain why a particular approach was chosen  
- Surface risks or uncertainties early  
- Do not silently resolve unclear requirements  
- Keep communication concise and meaningful  

---

## 6. Follow Existing Patterns — With Judgment

Maintain consistency, but do not blindly copy poor practices.

- Follow the existing code style, patterns, and architecture  
- Keep code easy to read, understand, and modify  

**If the existing approach is clearly problematic (performance, security, maintainability):**
- Call it out explicitly  
- Suggest a better alternative with a brief reason  

Avoid:
- Designing for hypothetical future needs  
- Adding unnecessary abstraction layers  

**Rule of thumb:**
- Minor imperfection → follow existing style  
- Clear technical issue → suggest improvement before implementing  

---

### 7. When No Clear Pattern Exists

If there is no similar implementation in the codebase:

- Start with the simplest valid solution  
- Prefer local and minimal state management first  
- Introduce structured patterns (e.g., BLoC) only when clearly required  

Avoid introducing complexity without a concrete need.

## Summary

These guidelines are effective when:

- Changes are small and focused  
- Code remains simple and readable  
- Unnecessary abstractions are avoided  
- Assumptions are clearly stated  
- Behavior is verified, not assumed  
