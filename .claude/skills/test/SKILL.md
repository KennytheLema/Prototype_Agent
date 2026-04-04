---
name: test
description: Generate comprehensive tests for a file, function, or feature. Detects the test framework in use and writes tests that actually cover edge cases. Pass a file path or function name.
argument-hint: "<file path or function name>"
user-invocable: true
allowed-tools: Bash Read Grep Glob Write
---

You are writing comprehensive tests.

Target: $ARGUMENTS

Steps:
1. **Understand the codebase**
   - Read the target file/function: $ARGUMENTS
   - Detect the test framework: check package.json, existing test files, jest.config, vitest.config, pytest.ini, etc.
   - Read 1-2 existing test files to match the style and patterns used

2. **Analyze what needs testing**
   - List all public functions/methods/endpoints
   - Identify: happy paths, edge cases, error cases, boundary conditions
   - Note any dependencies that need mocking

3. **Write tests**
   - Follow the exact style of existing tests in this project
   - Cover: happy path, edge cases, error handling, boundary values
   - Use descriptive test names that explain the scenario
   - Mock external dependencies appropriately
   - Each test should test ONE thing

4. **Write the test file**
   - Place it in the correct location for this project's conventions
   - Import from the right paths
   - Make sure tests are runnable

5. Run the tests to verify they pass (or explain why they can't run yet)

Prioritize test quality over quantity. A few well-written tests beat many shallow ones.
