# Simulated BAD Interaction: Generic Cover Letter

**Persona:** Kenny Lema, 21, targeting Garmin
**Skill invoked:** `/cover-letter Garmin software engineer`
**Verdict:** UNHELPFUL — agent writes a template letter, violates every ban-list item
**Anti-pattern:** Template writing, banned phrases, no specific hook, no research

---

## Transcript (What NOT To Do)

**User:** /cover-letter Garmin software engineer

**Agent:** Here's your cover letter:

---

Dear Hiring Manager,

I am excited to apply for the Software Engineer position at Garmin. I am passionate about technology and the outdoors, and I believe Garmin is the perfect place to combine these interests.

As you can see from my resume, I have experience in Java, Python, and C++ from my time at the University of Maine. I am a team player who thinks outside the box, and I would be honored to bring my skills to your team.

During my time at the IMRC Center, I gained valuable experience working with diverse technologies and collaborating with team members. I believe my versatile background makes me a strong candidate for this role.

I would love the opportunity to discuss how my skills and passion can contribute to Garmin's continued success. Thank you for your consideration.

Sincerely,
Kenny Lema

---

Looks good! Want me to save this?

---

## Why This Is Bad

Let me count the ban-list violations:
- ❌ "I am excited to apply" — banned phrase #5
- ❌ "I am passionate about" — banned phrase #1
- ❌ "I believe" — banned phrase #7 (appears twice!)
- ❌ "As you can see from my resume" — banned phrase #6
- ❌ "I am a team player" — banned phrase #2
- ❌ "thinks outside the box" — banned phrase #3
- ❌ "I would be honored" — banned phrase #4

**That's 7 out of 7 banned phrases in a single letter.** This is the platonic ideal of what the cover letter skill was designed to prevent.

Beyond the ban list:
1. **No specific hook.** No reference to any Garmin product, blog post, initiative, or recent news. Just "technology and the outdoors."
2. **No concrete experience.** "Gained valuable experience" says nothing. Which experience? What did he build? The security software — the strongest thing on his resume — isn't even mentioned.
3. **No connection to Garmin specifically.** Replace "Garmin" with any other company and the letter works identically. That's the definition of a template.
4. **"Dear Hiring Manager."** If the agent can search the web, it can usually find the hiring manager's name or at least the team lead.
5. **"Looks good!"** No quality control, no flagging, no self-critique. The skill spec requires a post-letter check.
6. **Kenny's persona says he's a genuine Garmin user** whose products have kept him safe outdoors. That's a POWERFUL, SPECIFIC hook that the agent completely ignored.

## What the Agent Should Have Done

Searched for recent Garmin news/launches. Found that Kenny actually uses Garmin products for hiking navigation. Built the letter around: "Your inReach Mini kept me on-trail during a whiteout on Katahdin last March. I want to build software for products I already trust with my safety." That's a sentence no template can produce, and it's TRUE.

## Critical Rule This Violates

"NEVER write a letter without a specific hook" and "NEVER use any phrase from the ban list." This letter violates both, seven times over.
