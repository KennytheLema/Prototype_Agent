---
name: side-project-scope
description: Help scope a side project, startup idea, or nonprofit concept — clarify the problem, identify collaborators needed, and create a lightweight project brief. Pass your idea or problem statement.
argument-hint: "<project idea or problem statement>"
user-invocable: true
allowed-tools: Read Glob WebSearch
---

You are helping the user turn a vague idea into a scoped, actionable project brief.

Idea: $ARGUMENTS

Steps:
1. **Clarify the problem being solved**
   - Restate the idea as a problem statement: "Who has [problem X] and why does it matter?"
   - Ask the user (or infer from the idea) to confirm: Is this a personal itch, a community need, or an observed market gap?
   - Read ~/.career/profile.json to understand the user's skills, values, and available time/resources

2. **Research the space**
   - Search for existing solutions: "[idea keywords] existing app tool platform nonprofit"
   - Search for adjacent communities: "[idea keywords] community subreddit forum"
   - Note what exists and where the gap genuinely is — do not scope a project that is a close clone of something well-established without a clear differentiation

3. **Define scope layers**
   Present three scope options:
   - **Smallest viable version (weekend project)**: What could one person build/do in 2 days to test the core assumption?
   - **Small team project (1-3 months)**: What would justify forming a small team and running for a quarter?
   - **Full venture (6+ months)**: What does the full version look like if the core assumption proves true?

4. **Identify the riskiest assumption**
   - State the single most important unproven assumption in this idea
   - Suggest the cheapest possible test of that assumption (survey, landing page, one conversation with a potential user)
   - Do not encourage building before validating

5. **Map skills needed**
   - List the distinct skills/roles needed at each scope level
   - Cross-reference with the user's own skills (from profile)
   - Identify the 1-2 collaborator types most critical to find

6. **Generate a lightweight project brief**
   Output a structured brief:
   - Problem statement (2 sentences)
   - Target user and their pain (2 sentences)
   - Proposed solution (2 sentences)
   - Smallest test (1 sentence)
   - Skills gap: what collaborators are needed
   - Success metric for the next 30 days

7. **Save and suggest next steps**
   - Save to ~/.career/projects/<project-slug>-brief.md
   - Suggest running /find-collaborators with the skills gap to find potential co-founders or contributors
   - If a nonprofit: note any legal incorporation considerations to research
