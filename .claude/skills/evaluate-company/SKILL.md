---
name: evaluate-company
description: Deep ethical evaluation of a company before applying — culture, values alignment, red flags, and deal-breakers. Pass a company name and optionally a role.
argument-hint: "<company name> [optional: role you're applying for]"
user-invocable: true
allowed-tools: Read WebSearch Glob
---

You are conducting an independent ethical and cultural due-diligence review of a company.

Target: $ARGUMENTS

Steps:
1. **Parse target**
   - Extract company name and role (if provided)
   - Read ~/.career/profile.json to load the user's stated values, ethical priorities, and deal-breakers

2. **Gather public information**
   - Search for: "[company name] employee reviews Glassdoor", "[company name] culture layoffs news", "[company name] B-Corp certification", "[company name] DEI report", "[company name] environmental impact", "[company name] executive pay ratio"
   - Also search: "[company name] controversy lawsuit settlement" to surface legal/ethical history
   - If the role is provided, search: "[company name] [role] interview experience"

3. **Evaluate on the Ethical Career Rubric**
   Rate each dimension 1-5 (1=red flag, 5=strong positive), with a one-sentence rationale:
   - **Mission clarity**: Does the company have a stated mission beyond profit? Is it credible?
   - **Labor practices**: Layoff history, union stance, contractor vs. FTE ratio, pay equity signals
   - **Environmental record**: Carbon commitments, industry sector impact, greenwashing signals
   - **Governance**: Founder control vs. board independence, B-Corp or benefit corporation status
   - **DEI in practice**: Leadership diversity data, public pay gap report, ERG presence
   - **Transparency**: Salary ranges posted, financial transparency, public benefit reports
   - **Culture signals**: Glassdoor rating trend (improving or declining), common praise/complaints

4. **Flag deal-breakers**
   - Cross-reference the user's deal-breakers from their profile against findings
   - If any deal-breaker is triggered, surface it prominently at the top of the report
   - Be explicit: "This company operates in [industry X], which you have listed as a deal-breaker"

5. **Summarize verdict**
   - Overall Ethical Score: X/35 (sum of seven rubric dimensions)
   - Verdict label: Strong Alignment | Moderate Alignment | Proceed with Caution | Not Recommended
   - Three things the user should ask in interviews to probe the weaker areas
   - One key risk to be aware of even if proceeding

6. **Save the evaluation**
   - Write a summary record to ~/.career/evaluations/<company-slug>-<date>.md

Be honest and evidence-based. Do not give companies benefit of the doubt without evidence. Do not penalize for imperfection — penalize for dishonesty or demonstrated harm.
