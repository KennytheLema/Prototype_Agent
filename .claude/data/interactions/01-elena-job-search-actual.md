# Actual Interaction Log: Elena — Job Search (High School Student)

**Date:** 2026-04-05
**Persona:** Elena, high school student in Maine, Jackson Labs internship experience
**Skills invoked:** `/job-search`
**Verdict:** BENEFICIAL — agent behaved well overall

---

## Transcript Summary

**User:** "hey my name is elena and im a highschooler witht internship expecirece, and im lookign for a job help me find one"

**Agent:** Checked for a profile (none found). Mentioned `/profile-setup` as optional. Pushed back on the vague request — asked for role type, internship field, location, part-time vs full-time, and values.

**User:** "I was interning at Jackson Labs, A laboratory here in Maine. Im interested in animal biology and I want to conserve the environment."

**Agent:** Recognized Jackson Labs as a legitimate genomics institution. Updated the user profile. Proposed 3 specific search queries and asked one more clarifying question: summer job vs part-time vs internship.

**User:** "I want a summer job"

**Agent:** Ran 3 web searches. Scored results on a 10-point rubric (role fit, location, values signal, pay transparency). Presented 8 results in three tiers:
- **Strong Fits (7+):** Maine Audubon Coastal Birds Intern (9/10), Maine Audubon Program Intern (8/10), NECWA Marine Wildlife Intern (7/10)
- **Worth a Look (4-6):** Maine Appalachian Trail Club (6/10), National Conservation Crew (6/10), Maine Audubon Camp Educator (5/10)
- **Flagged (age/enrollment barriers):** Rockefeller Internship, Marine Mammals of Maine

Gave opinionated recommendation: "Go for #1 first." Offered chaining into `/evaluate-company`, `/tailor-resume`, `/cover-letter`.

---

## What Went Well

1. **Pushed back on vague request.** Didn't dump generic results for "find me a job." Asked clarifying questions first, which is what the skill spec requires.
2. **Adapted to the user's experience level.** Didn't assume professional vocabulary. Kept language casual and accessible for a high schooler.
3. **Scored and ranked results visibly.** Showed the rubric math so Elena can see WHY each result made the list — not just a wall of links.
4. **Flagged age/enrollment barriers.** Two great results (MMoME, Rockefeller) required college enrollment. Instead of hiding them, flagged them as "for next year" — useful framing.
5. **Had a clear opinion.** Recommended #1 and explained why. Acted like a friend, not a search engine.
6. **Offered chaining naturally.** Didn't just say "here's a list, good luck." Gave clear next steps.

## What Could Be Better

1. **Didn't fully confirm search strategy before running.** The skill spec says: "Tell the user what you're about to search... Anything I should add or skip?" The agent described queries but ran them without waiting for confirmation.
2. **Could have probed deeper on location constraints.** "Maine" is a big state. Bangor vs. Portland vs. Bar Harbor matters for a high schooler who probably can't relocate freely.
3. **Salary information was sparse.** Most results had "salary not disclosed" — agent noted this but could have added context like "seasonal conservation internships in Maine typically pay $12-18/hr" to set expectations.
