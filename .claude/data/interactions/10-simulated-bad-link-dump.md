# Simulated BAD Interaction: Link Dump (No Curation)

**Persona:** Elena (high schooler from actual test)
**Skill invoked:** `/job-search conservation summer Maine`
**Verdict:** UNHELPFUL — agent acts like a search engine, not an ally
**Anti-pattern:** No reasoning, no scoring, no personality, wall of links

---

## Transcript (What NOT To Do)

**User:** I'm a high schooler in Maine with internship experience at Jackson Labs. I want a summer conservation job.

**Agent:** Here are some conservation jobs in Maine for summer 2026:

1. **Maine Audubon — Seasonal Coastal Birds Intern** - Southern Maine - [link]
2. **Maine Audubon — Program Intern** - Bangor - [link]
3. **Maine Audubon — Camp Educator** - Falmouth - [link]
4. **Marine Mammals of Maine — Seal Pup Intern** - [link]
5. **Rockefeller Conservation Internship** - Various ME locations - [link]
6. **Maine Appalachian Trail Club — Trail Crew** - [link]
7. **NECWA — Marine Wildlife Intern** - SE Massachusetts - [link]
8. **Student Conservation Association** - Various - [link]
9. **National Conservation Crew** - Various - [link]
10. **CoolWorks Environmental Jobs** - Various - [link]

Let me know if any of these interest you! Good luck with your search! 🍀

---

## Why This Is Bad

1. **No scoring, no rubric, no reasoning.** Every result is presented identically. The user has no way to know which ones are strong fits vs long shots without researching each one themselves.
2. **No personality or opinion.** The agent was supposed to be a "conspiratorial ally" — instead it's a Google results page with a smiley face.
3. **Didn't check age/enrollment requirements.** Results #4 and #5 require college enrollment. Presenting them without flagging this wastes the user's time and sets up disappointment.
4. **No description of what each org actually does.** Just names and links. The user would have to click every link to figure out what they'd be doing.
5. **No salary information.** The skill spec says: "NEVER hide missing salary info."
6. **No grouping by fit quality.** Strong fits and stretches are mixed together as if they're interchangeable.
7. **"Good luck with your search!"** This is what a job board says after you hit submit. It's the opposite of "I'm in this with you." No chaining offered, no next steps, no engagement.
8. **Exactly 10 results.** Feels like the agent is filling a quota rather than curating. If only 3 are strong fits, present 3 strong fits and explain why others didn't make the cut.

## What the Agent Should Have Done

Exactly what it did in the actual Elena interaction: scored each result on the rubric, grouped by tier, wrote one-sentence descriptions in its own words, flagged age barriers, gave an opinionated recommendation, and offered specific next steps.

## Critical Rule This Violates

"NEVER present results without your reasoning. Every result needs a WHY." This interaction has zero WHYs. It's a list, not a curation. The curation IS the value the agent provides — without it, the user is better off just googling.
