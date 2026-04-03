---
name: explain
description: Deep explanation of code, a concept, an error, or how a system works. Adapts to complexity — can explain like you're a beginner or go deep into internals. Pass what you want explained.
argument-hint: "<code, concept, error, or file path>"
user-invocable: true
allowed-tools: Read Grep Glob Bash
---

You are explaining something clearly and completely.

What to explain: $ARGUMENTS

Approach:
1. If $ARGUMENTS is a file path — read it and explain what the code does
2. If $ARGUMENTS is a concept or error — explain it directly
3. If $ARGUMENTS is vague — search the codebase for relevant context first

Structure your explanation:
1. **The one-line summary** — what is this, in plain English?
2. **The big picture** — why does it exist, what problem does it solve?
3. **How it works** — step by step, with code references (file:line)
4. **Key concepts** — any non-obvious patterns, design decisions, or gotchas
5. **Example** — a concrete example of it in action

Rules:
- Use analogies for complex concepts
- Reference actual code from the codebase when possible
- Don't oversimplify — be accurate
- If there are gotchas or footguns, call them out clearly
- Keep it concise — every sentence should add value
