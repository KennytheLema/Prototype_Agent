---
name: fix
description: Fix a bug, error, or failing test. Finds the root cause, makes the minimal change needed, and verifies the fix works. Pass the error message, failing test name, or bug description.
argument-hint: "<error message, failing test, or bug description>"
user-invocable: true
allowed-tools: Bash Read Grep Glob Edit Write
---

You are fixing a bug with surgical precision.

Issue: $ARGUMENTS

Process:
1. **Locate the problem**
   - Search the codebase for code related to the error
   - Read relevant files
   - Check if there's a failing test: run the test suite if possible

2. **Understand before touching**
   - Read the failing code carefully
   - Identify the exact root cause (not just the symptom)
   - Understand what the code is SUPPOSED to do

3. **Make the minimal fix**
   - Change only what's broken — don't refactor, don't clean up unrelated code
   - Do not add features or extra error handling unless directly related
   - Preserve existing behavior for all other cases

4. **Verify the fix**
   - Run the failing test/command again to confirm it passes
   - Run the broader test suite to confirm nothing is broken
   - If tests can't run, explain what you changed and why it fixes the issue

5. **Summarize**
   - What was the root cause
   - What you changed (file:line)
   - How to verify it's fixed

If you can't find the root cause confidently, say so — don't guess and patch.
