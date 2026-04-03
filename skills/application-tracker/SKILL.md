---
name: application-tracker
description: Track job applications, follow-up dates, interview stages, and outcomes in a local log. Add entries, update status, view dashboard, or get reminders for overdue follow-ups.
argument-hint: "[add <company> <role> | update <company> <stage> | status | remind]"
user-invocable: true
allowed-tools: Read Glob Bash
---

You are managing the user's job application tracker — their single source of truth for where they've applied, what stage each is at, and what actions are needed.

Command: $ARGUMENTS

Steps:
1. **Parse the command**
   - "add <company> <role>": Add a new application entry
   - "update <company> <stage>": Update an existing application's stage
   - "status": Display the full dashboard
   - "remind": List applications that need follow-up action based on dates
   - No argument: Default to "status"

2. **Load the tracker**
   - Read ~/.career/tracker.json (or create a blank structure if it does not exist)
   - Structure: { "applications": [ { "company", "role", "date_applied", "stage", "source_url", "follow_up_date", "notes", "outcome" } ] }

3. **For "add" command**
   - Create new entry with company, role, today's date, status: "Applied"
   - Set next follow-up date to 7 days from now
   - Ask user for the source URL if not provided
   - Save updated tracker

4. **For "update" command**
   - Find the matching application by company name
   - Update stage to one of: Applied | Phone Screen | Technical | Behavioral | Final | Offer | Rejected | Withdrawn | Accepted
   - Update follow-up date based on stage (Phone Screen: +5 days, Interview stages: +3 days, Offer: +2 days)
   - Add optional notes if the user provides context
   - Save updated tracker

5. **For "status" command**
   Display a dashboard grouped by stage:
   - Active applications by stage (with company, role, days since applied)
   - Applications with overdue follow-ups highlighted
   - Conversion funnel: Applied -> Screen -> Interview -> Offer (with counts and %)
   - Total active, total completed, total rejected

6. **For "remind" command**
   - List all applications where follow_up_date is today or earlier
   - For each: suggest the specific next action (send follow-up email, prepare for interview, make decision on offer)
   - Prioritize by urgency

7. **Quality over quantity check**
   - If user has >25 active applications, gently note that response rates and follow-through quality tend to decline at high volume
   - Suggest focusing energy on the top 10-15 strongest fits rather than spray-and-pray
   - This is advice, not a block — the user decides
