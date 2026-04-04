---
name: job-search
description: Search for job opportunities matching your profile, values, and preferences. Returns curated results with ethical company signals. Pass a role title and optional location/modality/values keywords.
argument-hint: "<role title> [location] [optional: remote|hybrid|onsite] [optional: values keywords]"
user-invocable: true
allowed-tools: Read Glob WebSearch
---

You are conducting a targeted, values-aware job search on behalf of the user.

Search request: $ARGUMENTS

Steps:
1. **Parse the request**
   - Extract: role title, location (default: remote), work modality, any values or industry constraints
   - Read ~/.career/profile.json if it exists to enrich the search with the user's stated values, must-haves, and deal-breakers
   - If profile.json is absent, note that a richer search is possible after running /profile-setup

2. **Construct search queries**
   - Build 2-3 distinct search queries combining role + location + any ethical/values keywords the user or their profile specifies
   - Include queries targeting job boards known for mission-driven roles: LinkedIn, Idealist, WorkForGood, Wellfound (for startups), ClimateBase (for climate), Tech Jobs for Good, and standard boards (Indeed, Greenhouse-hosted listings)
   - If the user's profile lists deal-breaker industries, note that filter will be applied

3. **Execute searches**
   - Run WebSearch for each query
   - Collect up to 20 raw results before filtering

4. **Filter and score results**
   - Remove results from any deal-breaker industries in the user's profile
   - Score remaining results on a simple rubric:
     - Role fit (title, seniority, responsibilities): 0-3
     - Location/modality match: 0-2
     - Values signal (B-Corp status, non-profit, stated mission, employee reviews mentioning culture): 0-3
     - Compensation transparency (salary listed vs. not listed): 0-2
   - Return the top 8 results sorted by score

5. **Present results**
   - For each result, output:
     - Company name, role title, location/modality
     - One-sentence description of what the company does
     - Salary range if listed, otherwise note "not disclosed"
     - Values signals found (B-Corp, employee-owned, mission-stated, etc.)
     - Direct application URL
   - Group results: Mission-aligned first, then General, then Speculative (high fit role, lower values signal)

6. **Log the search**
   - Append a search record to ~/.career/searches.log with: date, query, number of results, top 3 links

7. **Offer next steps**
   - Suggest: /evaluate-company <company name> for deeper ethical review
   - Suggest: /tailor-resume for any listing the user wants to pursue
   - Suggest: /application-tracker add to track any application they decide to submit
