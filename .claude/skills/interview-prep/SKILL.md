---
name: interview-prep
description: Generate tailored interview preparation — likely questions, STAR story mapping, company-specific research, and questions to ask. Pass company name, role, and optional interview stage.
argument-hint: "<company name> <role title> [optional: stage e.g. technical|behavioral|final]"
user-invocable: true
allowed-tools: Read Glob WebSearch
---

You are preparing the user for a job interview — comprehensively and specifically.

Interview target: $ARGUMENTS

Steps:
1. **Load context**
   - Read ~/.career/profile.json for the user's experience, strengths, and values
   - Read ~/.career/applications/<company-slug>*/resume.md and cover-letter.md if they exist
   - Read ~/.career/evaluations/<company-slug>*.md for company culture signals
   - Determine interview stage from $ARGUMENTS (default: behavioral if not specified)

2. **Research the role and company**
   - Search "[company name] [role] interview questions", "[company name] interview process Glassdoor", "[company name] engineering/product/design culture"
   - Note any reported quirks: take-home assignments, case studies, specific frameworks they favor

3. **Generate likely questions by category**
   Produce 5-7 questions per relevant category:
   - **Role-specific technical/craft questions**: Based on the job description and role type
   - **Behavioral questions**: STAR-format questions drawn from common patterns for this role level
   - **Culture/values questions**: Questions they're likely to ask given the company's stated values
   - **Situational questions**: "What would you do if..." scenarios relevant to the role's challenges

4. **Map STAR stories from the user's experience**
   - For each behavioral question category (conflict, failure, leadership, collaboration, ambiguity), identify the best experience from the user's resume/profile to use
   - Draft a 3-sentence STAR outline for each: Situation + Task, Action (specific), Result (quantified if possible)
   - Flag any category where the user's experience is thin — better to know now than be caught unprepared

5. **Generate questions the user should ask**
   - 3 questions about the team/role (show genuine curiosity)
   - 2 questions that probe the company's values claims (based on evaluation findings)
   - 1 question about growth and success metrics for this role
   - Flag which questions are also intelligence-gathering for the user's own decision-making

6. **Compile a one-page prep brief**
   - Company in three sentences (what they do, business model, current stage)
   - The role's core success metric in this user's interpretation
   - Three things to emphasize throughout the interview
   - One thing to be careful about (based on profile gaps or evaluation red flags)

7. **Save**
   - Write to ~/.career/applications/<company-slug>-<date>/interview-prep.md
