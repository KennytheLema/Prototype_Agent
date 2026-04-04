---
name: tailor-resume
description: Tailors your master resume to a specific job posting — highlighting relevant experience, keywords, and genuine fit. Does not fabricate or embellish. Pass a job posting URL or pasted description.
argument-hint: "<job posting URL or pasted job description>"
user-invocable: true
allowed-tools: Read WebSearch Glob
---

You are tailoring the user's resume for a specific job opportunity — with accuracy and honesty as non-negotiable constraints.

Job target: $ARGUMENTS

Steps:
1. **Load the user's master resume**
   - Read ~/.career/resume-master.md (or .txt/.json)
   - If it does not exist, ask the user to run /profile-setup first or paste their resume content directly
   - Read ~/.career/profile.json for career goals and tone preferences

2. **Gather the job description**
   - If $ARGUMENTS is a URL: use WebSearch to retrieve the job posting text
   - If $ARGUMENTS is pasted text: use it directly
   - Extract: required skills, preferred skills, responsibilities, cultural keywords, and any explicit values language

3. **Analyze fit gaps and strengths**
   - List required skills from the posting
   - For each required skill, identify which resume items demonstrate it (with specific evidence)
   - Note any required skills the user genuinely lacks — do NOT paper over them
   - Identify 2-3 "hidden strengths" — experiences in the resume that are relevant but not obvious from titles alone

4. **Reorder and emphasize, never fabricate**
   - Rewrite the summary/objective to speak directly to this role and company
   - Reorder bullet points within each role so the most relevant ones surface first
   - Incorporate exact keywords from the posting where they accurately reflect the user's experience
   - Add quantified impact numbers from the master resume where available
   - STRICT RULE: Do not add skills, roles, technologies, or achievements that do not appear in the master resume. Flag any genuine gap honestly.

5. **Write the tailored resume**
   - Output the full tailored resume in clean Markdown
   - Include a "Tailoring Notes" section at the bottom (for the user's eyes only, not to submit):
     - Which required skills are well-covered
     - Which required skills are absent — honest gaps to address in the cover letter or interview
     - Suggested talking points for interview

6. **Save the output**
   - Suggest saving to ~/.career/applications/<company-slug>-<date>/resume.md
