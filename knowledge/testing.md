<verification_protocol>
Framework: [e.g., Vitest]
Directive: Test behaviors and invariants, not implementation details.
</verification_protocol>

<testing_invariants>
1. MOCKING BOUNDARY: NEVER mock the unit under test. ONLY mock the extreme IO boundaries (Network, Database drivers, Time).
2. PROPERTY TESTING: Where applicable for pure functions, use property-based testing (fuzzing inputs) rather than hardcoding 3 static examples.
3. SETUP: Use the Factory pattern for generating test data. Hardcoding massive JSON objects inside the `describe` block is forbidden.
</testing_invariants>

<coverage_anti_patterns>
- Testing that a 3rd party library works (e.g., testing that the ORM actually saves to the DB). 
- Writing a test that asserts `expect(true).toBe(true)` just to pass CI.
</coverage_anti_patterns>
