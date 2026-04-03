---
name: cover-letter
description: Write an authentic, specific cover letter for a job application. Connects your real story to the company's mission. Pass company name, role, and optionally a specific angle or story.
argument-hint: "<company name> <role title> [optional: angle or specific story to highlight]"
user-invocable: true
allowed-tools: Read Glob WebSearch
---

You are writing a cover letter that is honest, specific, and human — not a template.

Target: $ARGUMENTS

Steps:
1. **Load context**
   - Read ~/.career/profile.json for the user's values, career narrative, and authentic voice preferences
   - Read ~/.career/applications/<company-slug>*/resume.md if a tailored resume exists for this company (to maintain consistency)
   - Read ~/.career/evaluations/<company-slug>*.md if a company evaluation exists (to incorporate genuine values alignment)

2. **Research the company's mission and recent news**
   - Search "[company name] mission vision recent news 2024 2025"
   - Find one specific, recent, concrete thing about the company to reference — a product launch, a published article by their team, a policy they adopted, a community initiative
   - This specificity signal separates authentic letters from templates

3. **Identify the authentic hook**
   - What is the genuine intersection of the user's story and this company's work?
   - If the user provided a specific angle ($ARGUMENTS includes one), use that
   - Otherwise, derive the strongest honest hook from the profile and research
   - RULE: If there is no genuine connection, say so and ask the user whether they still want to proceed

4. **Draft the letter structure**
   - Opening (2-3 sentences): Specific hook — why this company, why this role, why now. No generic opener.
   - Body paragraph 1 (3-4 sentences): The strongest relevant experience, told as a brief story with a concrete outcome
   - Body paragraph 2 (3-4 sentences): A second dimension — values alignment, or a skill/project that complements paragraph 1
   - Closing (2-3 sentences): What you'd bring, an invitation to discuss, confident but not sycophantic

5. **Write the letter**
   - Target 300-400 words — respects the reader's time
   - Match the tone to the company culture (formal for traditional institutions, conversational for startups)
   - First-person, active voice
   - No hollow phrases: "I am passionate about", "I am a team player", "I think outside the box"
   - Yes: specific reference, honest reason, concrete and respectful claim

6. **Flag authenticity check**
   - After the letter, note: any claims in the letter that depend on resume items the user should be prepared to elaborate on in detail
   - If the user's genuine enthusiasm for this role seems low based on their profile, note that — a lukewarm cover letter often shows, and it may be worth reconsidering the application

7. **Save**
   - Suggest saving to ~/.career/applications/<company-slug>-<date>/cover-letter.md
