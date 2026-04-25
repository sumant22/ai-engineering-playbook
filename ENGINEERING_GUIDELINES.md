# Engineering Guidelines (v1.0)

These guidelines define how code should be written, modified, and reviewed when working with LLMs or in collaborative environments.

**Principle:** Prioritize clarity, simplicity, and correctness over speed.

---

## 1. Think Before Coding

Do not assume. Make uncertainty explicit.

- State assumptions before implementing.
- If multiple interpretations exist, present them instead of choosing silently.
- Ask clarifying questions when requirements are unclear.
- Call out tradeoffs (e.g., simplicity vs flexibility).
- If a simpler approach exists, propose it before coding.
- If something is unclear, stop and ask.

---

## 2. Simplicity First

Solve the problem with the least code necessary.

- Do not add features beyond the request.
- Avoid premature abstractions, especially for single-use logic.
- Do not introduce speculative flexibility or configuration.
- Avoid handling unrealistic or impossible scenarios.
- Continuously ask: "Can this be simpler?"

---

## 3. Surgical Changes

Make minimal, targeted modifications.

- Only change what is required for the task.
- Do not refactor unrelated code.
- Match the existing code style and structure.
- Do not fix adjacent issues unless explicitly asked.
- Remove unused code introduced by your changes.
- If unrelated dead code exists, mention it but do not remove it.

**Test:** Every changed line should directly relate to the task.

---

## 4. Goal-Driven Execution

Work toward clear, verifiable outcomes.

Convert vague tasks into concrete checks:

- "Fix bug" → Reproduce → Fix → Verify  
- "Add validation" → Define invalid cases → Verify behavior  
- "Refactor" → Ensure behavior remains unchanged  

For multi-step tasks:  
Implement → verify → adjust → re-verify → final check  

Avoid vague success criteria like "it works."

**"Done" for UI means:**
- The main flow works (golden path)
- Edge cases are handled (empty, loading, error)
- No nearby functionality is broken
- Passing type checks is not enough — behavior must be verified

---

## 5. Communicate While Coding

Be explicit about reasoning and concerns.

- Explain why a particular approach was chosen.
- Surface uncertainties or risks early.
- Do not silently resolve unclear requirements.
- Keep communication concise but meaningful.

---

## 6. Follow Codebase Style — With Judgment

Follow existing patterns, but do not blindly copy poor ones.

- Default: follow the existing code style, patterns, and architecture.
- Maintain consistency with surrounding code, even if it’s not your preference.
- Write code that is easy to read, understand, and modify.

**However, if the existing approach is clearly problematic (performance, security, maintainability):**
- Do not blindly follow it.
- Call it out explicitly.
- Suggest a better alternative with a brief reason.

- Do not design for hypothetical future requirements.
- Do not add abstraction layers unless clearly needed.
- Optimize for readability and maintainability.

**Rule of thumb:**
- Minor imperfection → follow existing style  
- Clear technical issue → suggest improvement before implementing  

---

## Summary

These guidelines are effective when:

- Changes are small and focused  
- Code remains simple and readable  
- Unnecessary abstractions are avoided  
- Assumptions are clearly stated  
- Behavior is verified, not just written  
