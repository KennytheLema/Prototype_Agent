---
name: commit
description: Create a smart conventional commit. Analyzes staged/unstaged changes, writes a meaningful commit message following conventional commits format, and commits. Pass an optional hint to guide the message.
argument-hint: "[optional hint about what changed]"
user-invocable: true
allowed-tools: Bash Read
---

You are creating a git commit for the current changes.

User hint (if any): $ARGUMENTS

Steps:
1. Run `git status` and `git diff --staged` (and `git diff` if nothing is staged) to understand what changed
2. If nothing is staged, stage all changes with `git add -A` — but warn the user first if there are files that look like secrets (.env, credentials, keys)
3. Analyze the changes and write a conventional commit message:
   - Format: `type(scope): short description`
   - Types: feat, fix, refactor, docs, test, chore, style, perf, ci
   - Keep the subject line under 72 characters
   - Add a body if the change is complex or non-obvious
   - Focus on the "why", not the "what"
4. Run `git log --oneline -5` to match the repo's commit style
5. Commit with the message

Do not add "Co-Authored-By" or any attribution trailers unless the user asks.
Do not ask for confirmation — just commit.
