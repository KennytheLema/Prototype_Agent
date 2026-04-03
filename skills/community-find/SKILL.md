---
name: community-find
description: Discover communities of practice, professional groups, and online spaces aligned with your work and values. Pass your role or interest area and optional format preference.
argument-hint: "<role or interest area> [optional: format preference e.g. Slack|Discord|in-person|newsletter]"
user-invocable: true
allowed-tools: Read WebSearch Glob
---

You are helping the user discover professional communities that match their craft and values.

Interest area: $ARGUMENTS

Steps:
1. **Parse request and load profile**
   - Extract role/interest area and any format preference from $ARGUMENTS
   - Read ~/.career/profile.json for the user's location, remote preference, and any communities already listed under network.memberships (to avoid duplicates)

2. **Search for communities**
   Run targeted searches for:
   - "[interest area] Slack community professionals"
   - "[interest area] Discord server practitioners"
   - "[interest area] newsletter community 2024 2025"
   - "[interest area] conference annual community"
   - "[interest area] open source community contribute"
   - For mission-driven interests also search: "[interest area] social impact community network"

3. **Filter for quality signals**
   For each community found, look for:
   - Active moderation (mentioned code of conduct, reported active community management)
   - Size and activity signals (member count, recent posts if visible, last update)
   - Cost and accessibility (free vs. paid, application vs. open join)
   - Values alignment signals (DEI statements, safe space policies, anti-harassment stance)

4. **Categorize results**
   Group communities into:
   - **Tier 1 — High signal**: Active, well-moderated, directly relevant, free or low-cost
   - **Tier 2 — Worth exploring**: Relevant but harder to assess activity level
   - **Tier 3 — Adjacent**: Broader communities where the user's niche is represented

5. **Present results**
   For each community:
   - Name, platform/format, estimated size
   - What it's for in one sentence
   - How to join (URL, application process, invite requirement)
   - Why it's relevant to this user specifically
   - Notable signals (e.g., "has a dedicated #job-board channel", "hosts monthly virtual meetups")

6. **Suggest onboarding strategy**
   - Which community to join first and why
   - What to post as an introduction (template, honest and specific)
   - How to be a genuine contributor before asking for anything (lurk, help, then ask)

7. **Log new communities**
   - Ask the user which they plan to join and update ~/.career/profile.json under network.memberships
