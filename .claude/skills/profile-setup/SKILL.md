---
name: profile-setup
description: Set up or update your Ethical Career Agent profile — career history, values, preferences, deal-breakers, and goals. Foundation for all other career skills. Pass an optional section to update.
argument-hint: "[optional: update section e.g. values|experience|goals|network|projects]"
user-invocable: true
allowed-tools: Read Glob
---

You are setting up or updating the user's Ethical Career Agent profile — the foundation that powers every other career skill.

Section to update (if any): $ARGUMENTS

Steps:
1. **Check existing profile**
   - Try to read ~/.career/profile.json
   - If it exists: determine which section to update based on $ARGUMENTS, or do a full review if no section specified
   - If it does not exist: run full setup from scratch

2. **Collect career history**
   Ask the user (or prompt them to paste):
   - Current role and company (or most recent if between jobs)
   - Years of experience and primary craft/discipline
   - 3-5 previous roles with company, title, and what they built or delivered
   - Key skills (technical and interpersonal)
   - Industries worked in

3. **Collect values and ethical priorities**
   Ask the user to describe:
   - Top 3 work values (e.g., autonomy, impact, learning, stability, compensation, mission)
   - Industries or company types they are EXCITED to work in
   - Hard deal-breakers: industries, business models, or practices they will not support (e.g., surveillance tech, fossil fuels, predatory lending, weapons, gambling)
   - Ethical priorities ranked: environmental impact, labor practices, DEI, governance, transparency, community impact

4. **Collect job search preferences**
   - Target roles (titles, seniority levels)
   - Location and modality preferences (remote/hybrid/onsite, cities, countries)
   - Compensation minimum (and whether they want to target above-band)
   - Timeline (actively searching, passively open, just exploring)
   - Preferred company stage (startup, growth, enterprise, nonprofit, government, cooperative)
   - Must-haves vs. nice-to-haves

5. **Collect network and community context**
   - Communities they already belong to (Slack groups, Discord servers, meetups, professional orgs)
   - 3-5 people in their network they trust for career advice
   - Whether they are open to introductions and at what frequency

6. **Collect side project and startup interests**
   - Any active side projects
   - Problem areas they want to work on beyond day jobs
   - Whether they are open to co-founding opportunities
   - Available hours per week for side projects

7. **Build the career narrative**
   - Help the user articulate a one-liner describing their career arc
   - Identify the through-line connecting their roles and interests
   - What they are known for in their field

8. **Confirm and save**
   - Display the complete profile in readable format for the user to review
   - Confirm accuracy before saving to ~/.career/profile.json
   - Note which skills become more powerful with this profile in place

This profile is private — it stays on the user's local machine. Do not send it anywhere or reference it outside of career-related skill invocations.
