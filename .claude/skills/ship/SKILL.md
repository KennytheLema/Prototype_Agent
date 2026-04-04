---
name: ship
description: Full ship workflow — commits all changes, pushes to remote, and creates a pull request. Pass an optional description of what you're shipping.
argument-hint: "[optional description of what you're shipping]"
user-invocable: true
allowed-tools: Bash Read
---

You are shipping code. Complete the full workflow end to end.

What we're shipping: $ARGUMENTS

Steps:
1. Run `git status` to see what's changed
2. Run `git diff` to understand all changes
3. Stage everything: `git add -A` (warn if any secrets look staged)
4. Write a conventional commit message based on the changes (feat/fix/chore/etc.)
5. Commit the changes
6. Run `git push` (with `-u origin <branch>` if needed)
7. Create a PR with `gh pr create` using a clear title and a body with:
   - ## Summary (bullet points of what changed)
   - ## Test plan (checklist of how to verify)
8. Return the PR URL

If there's nothing to commit, just push and create the PR from existing commits.
Do not ask for confirmation at each step — complete the full workflow.
