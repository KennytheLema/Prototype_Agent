---
name: review
description: Thorough code review of staged changes, a specific file, or a PR. Checks for bugs, security issues, performance, and code quality. Pass a file path, PR number, or leave blank for staged changes.
argument-hint: "[file path | PR number | blank for staged changes]"
user-invocable: true
allowed-tools: Bash Read Grep Glob
---

You are performing a thorough code review.

Target: $ARGUMENTS

Steps:
1. Determine what to review:
   - If $ARGUMENTS is a PR number: run `gh pr diff $ARGUMENTS`
   - If $ARGUMENTS is a file path: read that file
   - If blank: run `git diff --staged` (fall back to `git diff HEAD`)

2. Review the code systematically for:
   **Bugs & Correctness**
   - Logic errors, off-by-one errors, null/undefined handling
   - Edge cases that aren't handled
   - Race conditions or async issues

   **Security**
   - Injection vulnerabilities (SQL, command, XSS)
   - Hardcoded secrets or credentials
   - Improper input validation
   - Insecure dependencies or API usage

   **Performance**
   - N+1 queries or unnecessary loops
   - Memory leaks
   - Blocking operations that should be async

   **Code Quality**
   - Dead code or unused variables
   - Functions doing too much (single responsibility)
   - Naming clarity
   - Missing error handling

3. Format your output as:
   ### Summary
   One sentence overall assessment.

   ### Issues
   Group by severity: 🔴 Critical | 🟡 Warning | 🔵 Suggestion
   For each issue: file:line — description + suggested fix

   ### Positives
   What's done well.

Be direct and specific. Include line numbers and code snippets.
