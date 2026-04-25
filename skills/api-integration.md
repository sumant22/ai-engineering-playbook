# API Integration Skill (v1.0)

## Objective
Integrate with APIs in a reliable, predictable, and maintainable way.

---

## Core Principle
Never assume API behavior. Always validate inputs, outputs, and failures.

---

## Process

### 1. Understand the API Contract
- Identify endpoint, method (GET, POST, etc.)
- Understand required parameters
- Review expected response structure
- Clarify success and error responses

If anything is unclear → ask before implementing

---

### 2. Validate Inputs Before Sending
- Ensure required fields are present
- Validate data types and formats
- Avoid sending unnecessary or null data

---

### 3. Handle the API Call
- Make the request using appropriate method
- Keep the call isolated (no mixing with UI or unrelated logic)

---

### 4. Validate the Response
Do not trust the response blindly.

Check for:
- Response status (success/failure)
- Required fields exist
- Data types are correct
- Unexpected/null values

---

### 5. Handle Errors Explicitly
Always handle:

- Network errors (timeout, no connection)
- API errors (4xx, 5xx)
- Invalid or incomplete responses

Do not ignore or silently fail.

---

### 6. Transform Data (if needed)
- Convert API response into usable format
- Avoid leaking raw API structure into other layers
- Keep transformation logic clear and minimal

---

### 7. Update System State / Output
- Pass validated and transformed data forward
- Ensure correct updates in UI, state, or response

---

## Rules

- Do not assume API always succeeds
- Do not skip error handling for real scenarios
- Do not mix API logic with UI or unrelated code
- Do not expose raw API responses directly without validation

---

## Common Mistakes

- Assuming response structure without checking
- Ignoring error cases
- Mixing API calls inside UI components
- Not validating null or missing fields
- Over-transforming data unnecessarily

---

## When to Ask for Clarification

- API contract is unclear or incomplete
- Response structure is inconsistent
- Error handling expectations are undefined

---

## Output Format

When integrating an API, always include:

1. API contract summary  
2. What was implemented  
3. How errors are handled  
4. What was validated  

---

## Example

**Scenario:** Fetch user data from API  

**Implementation:**
- Called GET /users endpoint  
- Validated response status  
- Checked required fields (id, name)  

**Error Handling:**
- Handled network failure  
- Handled empty response  

**Result:**
- Passed clean, validated data to the next layer  
