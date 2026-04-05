# User Data Schema — Ethical Career Agent

## Profile Schema (`~/.career/profile.json`)

```json
{
  "meta": {
    "created": "2025-01-15",
    "last_updated": "2025-03-20",
    "version": "1.0"
  },
  "identity": {
    "name": "string",
    "location": "string",
    "timezone": "string",
    "preferred_pronouns": "string (optional)"
  },
  "career_history": {
    "current_role": {
      "title": "string",
      "company": "string",
      "start_date": "YYYY-MM",
      "status": "active | ended",
      "end_date": "YYYY-MM or null"
    },
    "experience_years": "number",
    "primary_discipline": "string",
    "secondary_disciplines": ["string"],
    "prior_roles": [
      {
        "title": "string",
        "company": "string",
        "dates": "YYYY-MM to YYYY-MM",
        "key_deliverable": "string (one sentence)"
      }
    ],
    "industries_worked_in": ["string"],
    "skills": {
      "technical": ["string"],
      "interpersonal": ["string"],
      "tools_and_platforms": ["string"]
    }
  },
  "values": {
    "top_work_values": ["string (max 3)"],
    "ethical_priorities_ranked": [
      "environmental_impact",
      "labor_practices",
      "dei_in_practice",
      "governance",
      "transparency",
      "community_impact"
    ],
    "excited_industries": ["string"],
    "deal_breakers": {
      "industries": ["string"],
      "business_models": ["string"],
      "practices": ["string"]
    }
  },
  "job_search_preferences": {
    "target_roles": ["string"],
    "seniority_levels": ["string"],
    "location": {
      "modality": "remote | hybrid | onsite | flexible",
      "preferred_cities": ["string"],
      "willing_to_relocate": "boolean",
      "open_to_countries": ["string"]
    },
    "compensation": {
      "minimum_base_salary": "number",
      "currency": "USD",
      "target_above_band": "boolean"
    },
    "timeline": "active | passive | exploring | on_hold",
    "preferred_company_stage": ["startup", "growth", "enterprise", "nonprofit", "government", "cooperative"],
    "must_haves": ["string"],
    "nice_to_haves": ["string"]
  },
  "network": {
    "memberships": [
      {
        "name": "string",
        "platform": "string",
        "joined_date": "YYYY-MM",
        "activity_level": "active | lurking | inactive"
      }
    ],
    "trusted_advisors": ["string"],
    "open_to_introductions": "boolean",
    "intro_frequency_preference": "weekly | monthly | as_needed"
  },
  "side_projects": {
    "active_projects": [
      {
        "name": "string",
        "brief_path": "string",
        "stage": "idea | scoped | building | launched",
        "open_to_collaborators": "boolean"
      }
    ],
    "problem_areas_of_interest": ["string"],
    "open_to_cofounding": "boolean",
    "available_hours_per_week_for_projects": "number"
  },
  "career_narrative": {
    "one_liner": "string",
    "through_line": "string",
    "what_they_are_known_for": "string"
  }
}
```

---

## Example User Profile 1: Priya Sharma

**Context:** Senior PM at Oracle, 9 years experience, actively pivoting into climate tech.

```json
{
  "meta": { "created": "2025-01-15", "last_updated": "2025-03-20", "version": "1.0" },
  "identity": { "name": "Priya Sharma", "location": "Austin, TX", "timezone": "America/Chicago" },
  "career_history": {
    "current_role": { "title": "Senior Product Manager", "company": "Oracle", "start_date": "2021-03", "status": "active" },
    "experience_years": 9,
    "primary_discipline": "Product Management",
    "secondary_disciplines": ["Data Analytics", "UX Research"],
    "prior_roles": [
      { "title": "Product Manager", "company": "Indeed", "dates": "2018-06 to 2021-02", "key_deliverable": "Launched job alert personalization system, increasing click-through rates 34%" },
      { "title": "Associate PM", "company": "Yammer (Microsoft)", "dates": "2016-08 to 2018-05", "key_deliverable": "Led migration of Yammer mobile app to React Native across 3M users" }
    ],
    "industries_worked_in": ["Enterprise SaaS", "HR Tech", "Social Collaboration"],
    "skills": {
      "technical": ["SQL", "API design", "A/B testing", "data analytics"],
      "interpersonal": ["stakeholder alignment", "cross-functional leadership", "written communication"],
      "tools_and_platforms": ["JIRA", "Amplitude", "Figma", "Looker"]
    }
  },
  "values": {
    "top_work_values": ["impact", "autonomy", "learning"],
    "ethical_priorities_ranked": ["environmental_impact", "labor_practices", "dei_in_practice", "transparency", "governance", "community_impact"],
    "excited_industries": ["climate tech", "clean energy", "sustainable agriculture", "civic tech"],
    "deal_breakers": {
      "industries": ["fossil fuel extraction", "defense contractors", "tobacco"],
      "business_models": ["surveillance advertising", "dark patterns"],
      "practices": ["forced arbitration", "union busting"]
    }
  },
  "job_search_preferences": {
    "target_roles": ["Senior PM", "Principal PM", "Head of Product"],
    "seniority_levels": ["senior", "principal"],
    "location": { "modality": "hybrid", "preferred_cities": ["Austin, TX", "San Francisco, CA", "New York, NY"], "willing_to_relocate": false },
    "compensation": { "minimum_base_salary": 185000, "currency": "USD", "target_above_band": true },
    "timeline": "active",
    "preferred_company_stage": ["growth", "enterprise", "nonprofit"],
    "must_haves": ["Salary transparency in job posting", "Remote-friendly culture", "Mission-driven product"],
    "nice_to_haves": ["B-Corp certified", "Employee equity", "4-day work week option"]
  },
  "network": {
    "memberships": [
      { "name": "MCJ Collective", "platform": "Slack", "joined_date": "2024-06", "activity_level": "active" },
      { "name": "Women in Product", "platform": "Slack", "joined_date": "2022-01", "activity_level": "lurking" }
    ],
    "trusted_advisors": ["Raj Patel (former manager at Indeed)", "Sarah Chen (climate VC)"],
    "open_to_introductions": true,
    "intro_frequency_preference": "as_needed"
  },
  "side_projects": {
    "active_projects": [],
    "problem_areas_of_interest": ["Carbon transparency in consumer products", "Climate literacy tools"],
    "open_to_cofounding": false,
    "available_hours_per_week_for_projects": 5
  },
  "career_narrative": {
    "one_liner": "Product leader with 9 years building data-driven consumer and enterprise products, pivoting into climate tech to apply those skills where impact is measurable in tonnes of CO2.",
    "through_line": "Consistently drawn to products that connect large audiences with better decision-making — now focusing that on decisions that affect climate.",
    "what_they_are_known_for": "Turning ambiguous data problems into clear product features. Built Indeed's personalization engine from 0-1."
  }
}
```

---

## Example User Profile 2: Marcus Webb

**Context:** Backend engineer, laid off from Robinhood, 6 years experience, building civic tech side project, prioritizes community impact.

```json
{
  "meta": { "created": "2025-02-01", "last_updated": "2025-04-01", "version": "1.0" },
  "identity": { "name": "Marcus Webb", "location": "Atlanta, GA", "timezone": "America/New_York" },
  "career_history": {
    "current_role": { "title": "Software Engineer II", "company": "Robinhood", "start_date": "2022-05", "status": "ended", "end_date": "2024-11" },
    "experience_years": 6,
    "primary_discipline": "Software Engineering",
    "secondary_disciplines": ["Data Engineering", "DevOps"],
    "prior_roles": [
      { "title": "Software Engineer", "company": "Plaid", "dates": "2020-03 to 2022-04", "key_deliverable": "Built Plaid's fraud detection pipeline reducing false positives by 28%" },
      { "title": "Junior Software Engineer", "company": "Georgia Tech Research Institute", "dates": "2018-08 to 2020-02", "key_deliverable": "Developed public health data aggregation tools for CDC grant project" }
    ],
    "industries_worked_in": ["Fintech", "Financial Infrastructure", "Public Health Research"],
    "skills": {
      "technical": ["Python", "Go", "Kafka", "distributed systems", "data pipelines", "PostgreSQL"],
      "interpersonal": ["technical documentation", "mentoring junior engineers", "open source collaboration"],
      "tools_and_platforms": ["AWS", "dbt", "Airflow", "Terraform", "GitHub Actions"]
    }
  },
  "values": {
    "top_work_values": ["mission", "community", "stability"],
    "ethical_priorities_ranked": ["community_impact", "labor_practices", "dei_in_practice", "transparency", "governance", "environmental_impact"],
    "excited_industries": ["public health tech", "civic tech", "nonprofit tech", "financial inclusion", "education"],
    "deal_breakers": {
      "industries": ["predatory lending", "gambling", "crypto/web3"],
      "business_models": ["payday loans", "high-frequency trading", "MLM infrastructure"],
      "practices": ["excessive employee surveillance", "no remote work", "mandatory on-call without compensation"]
    }
  },
  "job_search_preferences": {
    "target_roles": ["Senior Software Engineer", "Staff Engineer", "Engineering Lead"],
    "seniority_levels": ["senior", "staff"],
    "location": { "modality": "remote", "preferred_cities": ["Atlanta, GA"], "willing_to_relocate": false, "open_to_countries": ["US"] },
    "compensation": { "minimum_base_salary": 160000, "currency": "USD", "target_above_band": false },
    "timeline": "active",
    "preferred_company_stage": ["nonprofit", "government", "cooperative", "growth"],
    "must_haves": ["Remote-first or fully remote", "Mission clearly tied to public benefit"],
    "nice_to_haves": ["Unionized or union-friendly", "Employee ownership", "Explicit DEI commitments with data"]
  },
  "network": {
    "memberships": [
      { "name": "Civic Tech Atlanta", "platform": "in-person + Slack", "joined_date": "2023-02", "activity_level": "active" },
      { "name": "Code for America Brigade", "platform": "in-person + GitHub", "joined_date": "2022-09", "activity_level": "active" },
      { "name": "Black in Tech ATL", "platform": "Slack", "joined_date": "2023-08", "activity_level": "active" }
    ],
    "trusted_advisors": ["Dr. Nia Robinson (Georgia Tech advisor)", "James Foster (Plaid engineering lead)"],
    "open_to_introductions": true,
    "intro_frequency_preference": "monthly"
  },
  "side_projects": {
    "active_projects": [
      { "name": "ATL Eviction Watch", "brief_path": "~/.career/projects/atl-eviction-watch-brief.md", "stage": "building", "open_to_collaborators": true }
    ],
    "problem_areas_of_interest": ["Eviction data transparency", "Housing justice tools", "Voter registration infrastructure"],
    "open_to_cofounding": true,
    "available_hours_per_week_for_projects": 15
  },
  "career_narrative": {
    "one_liner": "Backend engineer with 6 years building financial data infrastructure, now prioritizing roles where the technical systems I build directly serve underserved communities.",
    "through_line": "Started with public health data tools, detoured through fintech for the technical rigor, returning to public benefit work with much stronger systems-building skills.",
    "what_they_are_known_for": "Building reliable data pipelines at scale. Reducing Plaid's fraud false positives by 28% through better ML feature engineering."
  }
}
```

---

## Application Tracker Schema (`~/.career/tracker.json`)

```json
{
  "applications": [
    {
      "company": "string",
      "role": "string",
      "date_applied": "YYYY-MM-DD",
      "source_url": "string (URL)",
      "stage": "Applied | Phone Screen | Technical | Behavioral | Final | Offer | Rejected | Withdrawn | Accepted",
      "follow_up_date": "YYYY-MM-DD",
      "notes": "string (optional)",
      "outcome": "string (optional, filled when final)"
    }
  ]
}
```

---

## Interaction Examples

### Positive Interactions

**1. Honest gap acknowledgment saves user from a bad fit**

```
User: /tailor-resume [research engineer safety role at OpenAI]

Agent: The posting requires: PhD or equivalent research experience, published ML safety 
research, proficiency in JAX or PyTorch at research scale.

Your resume covers: solid Python/Kafka engineering, strong data pipelines. These are 
genuinely transferable skills.

What it does NOT cover — and I won't paper over this:
- No published research of any kind
- No ML framework experience at research scale
- No PhD or equivalent background

This isn't a fit gap I can close with better bullet points. Applying as-is risks damaging 
your credibility for future roles you ARE qualified for.

Options:
1. Target OpenAI's infrastructure or data engineering roles — strong fit
2. Build ML safety credibility through a 12-18 month learning path and side project
3. Search for roles at safety-focused organizations matching your actual background
```

**2. Community-first networking leads to warm introduction**

```
User: /connect-request "David Park, Head of Engineering at Watershed, posted in MCJ he's hiring"

Agent: Before drafting a referral ask — you joined MCJ 3 weeks ago and I don't see 
activity yet. A cold message from a new community member asking about roles will likely 
get lost.

Better path:
- Week 1-2: Respond to 2-3 of David's posts with substantive contributions
- Week 3: Send a brief message — "I've been contributing to MCJ and noticed your hiring 
  post. I'm a PM with climate-relevant experience — would a 20-min intro conversation 
  make sense?"

This takes 2 extra weeks but has 3-4x higher response rate than cold outreach.
```

**3. Surfacing values conflict before offer acceptance**

```
User: I got an offer from Palantir. $240k base. Help me negotiate?

Agent: I can help negotiate — but first, your profile lists "government surveillance 
technology" as a hard deal-breaker. Palantir's core revenue: ICE contracts, military 
targeting systems, predictive policing tools.

Ethical Score: 11/35 | Verdict: Not Recommended (deal-breaker triggered)

I'm not refusing to help — this is your decision. But I won't pretend the conflict 
doesn't exist. Consider: Is there a team that doesn't touch these contracts? What's your 
actual minimum? Do you have other offers in the $180-220k range at aligned companies?

I'll help negotiate if you proceed. I want the decision to be clear-eyed.
```

### Not Helpful / Problematic Interactions (and how the agent handles them)

**4. User asks to fabricate credentials**

```
User: /tailor-resume [Amazon staff engineer]
  Add bullet points about "informal leadership" — I didn't really lead but make it sound 
  like I did.

Agent: I won't add bullet points describing leadership you didn't have. Amazon's 
behavioral interviews deep-dive every resume claim — fabricated bullets fall apart in the 
room and get you rejected at late stages.

What I CAN do: find genuine leadership signals in your experience — mentoring, driving 
technical decisions, cross-team coordination, influencing without authority. These are 
real and worth surfacing honestly. Want to start there?
```

**5. Mass application spam request**

```
User: Generate tailored applications for 200 jobs in the next two weeks.

Agent: Your tracker shows 23 active applications you haven't followed up on. Several 
have passed their follow-up dates.

Response rates drop sharply above 40-50 applications because quality degrades. A genuine, 
specific application to 40 companies outperforms 200 generic ones.

Suggestion: Close out or follow up the 23 active ones, then run /job-search for 15 
genuinely well-matched opportunities. I'll tailor each to a high standard.
```

**6. Ghosting after accepting an offer**

```
User: I accepted Watershed's offer but got a better one from Stripe Climate. Draft an 
email to ghost Watershed.

Agent: I won't draft a ghosting strategy. Climate tech PM is a tiny community — 
Watershed and Stripe teams interact regularly, share investors, and attend the same 
conferences.

Ghosting after acceptance is one of the few things that gets people talked about 
negatively. It also burns a reference you might want in 5 years.

What to do: Call Watershed's recruiter today. Say you received an offer that represents 
a career inflection point you can't pass up. Apologize for the timing. Offer to stay 
available during their re-search.

Uncomfortable? Yes. But it preserves the relationship. Want me to help draft what to say?
```
