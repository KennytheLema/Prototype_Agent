---
name: find-collaborators
description: Find potential co-founders, collaborators, or contributors for a side project, startup, or nonprofit — from communities, networks, and public directories. Pass project brief or skills needed.
argument-hint: "<project brief or skills needed> [optional: community or network to search within]"
user-invocable: true
allowed-tools: Read WebSearch Glob
---

You are helping the user find genuine collaborators for a project — people who are a real fit, not just warm bodies.

Project and skills needed: $ARGUMENTS

Steps:
1. **Load project context**
   - Read ~/.career/projects/<most-recent>-brief.md if a project brief exists
   - If $ARGUMENTS contains a brief or skills description, parse it directly
   - Read ~/.career/profile.json for the user's existing network and community memberships

2. **Define the ideal collaborator profile**
   - Synthesize: what skills are specifically needed, what values alignment matters for this project, what time commitment is realistic, what stage of involvement (co-founder, advisor, contributor, volunteer)?
   - Be specific: "a backend engineer with Python experience who cares about climate" is more useful than "a technical co-founder"

3. **Search for candidates in directories and communities**
   - Search the communities in the user's profile (network.memberships) for relevant public directories or job boards
   - Search: "[community name] member directory", "co-founder matching [interest area]", "[skill] + [values keyword] open to collaborations"
   - Check relevant platforms: YC co-founder matching, Idealist volunteers, Wellfound startup jobs, GitHub for open source contributors, relevant Slack communities

4. **Generate a shortlist**
   - Present 5-8 candidate profiles or sources (not specific people's private details — focus on public profiles, community roles, or platform-level sources)
   - For each: Where to find them, what makes them potentially relevant, how to reach out authentically

5. **Draft outreach approach**
   - Do NOT mass-message people with a template
   - For each candidate source, suggest a personalized hook based on their public work
   - Suggest a "project brief share" format: a short, honest description of the project that a potential collaborator can evaluate fairly before committing any time

6. **Suggest venues for organic discovery**
   - Which communities to post a "looking for collaborators" post in
   - Draft a genuine "looking for collaborators" post: specific problem, honest scope, skills sought, what you bring, how to respond
   - Note: post in communities where you've been a genuine participant first

7. **Log outreach**
   - Track contacts made in ~/.career/projects/<project-slug>-collaborators.md
