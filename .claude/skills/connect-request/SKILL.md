---
name: connect-request
description: Draft a genuine, non-transactional outreach message to someone you want to connect with for career, collaboration, or learning purposes. Pass the person's name and context.
argument-hint: "<person's name and context> [optional: reason for reaching out]"
user-invocable: true
allowed-tools: Read WebSearch Glob
---

You are drafting a connection request or outreach message — genuine, specific, and respectful of the recipient's time.

Recipient and context: $ARGUMENTS

Steps:
1. **Understand the intent**
   - Parse who the person is and why the user wants to connect
   - Read ~/.career/profile.json for the user's current context (job searching, pivoting, starting something, etc.)
   - Identify: Is this a cold outreach or warm connection? Is there a mutual connection or shared context?

2. **Research the recipient**
   - Search "[person name] [company/context]" to find their public profile, work, writing, or talks
   - Look for a specific, genuine hook: a post they wrote, a project they shipped, a talk they gave, a shared experience or community
   - If no genuine hook can be found, flag this — outreach without a real reason is spam

3. **Apply the Genuine Connection Test**
   Before drafting, answer:
   - What specifically about this person's work is the user genuinely interested in or inspired by?
   - What does the user offer in this exchange — even if just a genuine perspective or question?
   - Is this an ask (informational interview, intro, feedback) or a give (sharing relevant info, collaborating)?
   - If it's purely an ask, is it a reasonable one given the relationship (or lack thereof)?

4. **Draft the message**
   - Length: 3-5 sentences for LinkedIn/email — not longer
   - Structure: Specific hook -> honest context for reaching out -> clear, small ask OR genuine offer
   - Tone: Peer-to-peer, not flattering or subservient
   - No: "I'd love to pick your brain", "I'm a huge fan", generic compliments
   - Yes: Specific reference, honest reason, concrete and respectful ask

5. **Version for platform**
   - LinkedIn: 300 characters for connection request note (ultra-short version) + 500-word follow-up message
   - Email: Full message with subject line
   - Twitter/X or other: Adapted tone and length

6. **Flag ethical considerations**
   - If the user's stated goal involves asking for a referral before establishing any genuine connection, flag this as likely to backfire and suggest a more relationship-first approach
   - If the user wants to misrepresent their background in the message, refuse and explain why it damages long-term reputation
   - If the user just joined a community and wants to immediately ask a member for favors, suggest establishing genuine presence first

7. **Offer a cadence note**
   - If no response in 1 week: one respectful follow-up is appropriate
   - If no response after follow-up: move on — do not send further messages
