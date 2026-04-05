# Interaction Logs

Example interactions — both beneficial and unhelpful — that define the boundary of acceptable agent behavior.

## Index

### Actual (from real testing sessions)
| # | File | Persona | Skill | Verdict |
|---|-------|---------|-------|---------|
| 01 | `01-elena-job-search-actual.md` | Elena (high schooler) | `/job-search` | BENEFICIAL |

### Simulated — Beneficial
| # | File | Persona | Skill | What It Demonstrates |
|---|-------|---------|-------|----------------------|
| 02 | `02-simulated-good-kenny-profile-setup.md` | Kenny | `/profile-setup` | Collaborative tone, correcting self-deprecation without lecturing |
| 03 | `03-simulated-good-evaluate-company.md` | Diana | `/evaluate-company` | Honest scoring, no sugarcoating, actionable interview questions |
| 04 | `04-simulated-good-connect-request-refusal.md` | Marcus | `/connect-request` | Correctly refusing to write spam, redirecting constructively |

### Simulated — Unhelpful (Anti-patterns)
| # | File | Anti-Pattern | Why It Matters |
|---|-------|-------------|----------------|
| 05 | `05-simulated-bad-preachy-lecturing.md` | Moralizing / lecturing | Blocks the user's goal with unsolicited philosophy |
| 06 | `06-simulated-bad-dismissive-shaming.md` | Class bias / gatekeeping | Prejudges user fitness based on job title, not skills |
| 07 | `07-simulated-bad-unsolicited-advice.md` | Scope creep / advice overload | Delivers 5 opinions before doing the requested task |
| 08 | `08-simulated-bad-fake-enthusiasm.md` | Uncritical cheerleading | Sugarcoats a controversial company, ignores deal-breakers |
| 09 | `09-simulated-bad-resume-fabrication.md` | Fabricating credentials | Inflates resume with fake skills, sets user up for interview failure |
| 10 | `10-simulated-bad-link-dump.md` | No curation / search engine mode | Dumps links without reasoning, scoring, or personality |
| 11 | `11-simulated-bad-cover-letter-generic.md` | Template writing / banned phrases | Hits 7/7 banned phrases, zero specificity, ignores user's real story |

## How These Informed Critical Rules

Each unhelpful example maps directly to a Critical Rule in the skill definitions:

- **Preachy lecturing** → "Conspiratorial ally, not job board algorithm" (tone directive in every skill)
- **Dismissive shaming** → Never pre-judge fitness; show data and let user decide
- **Unsolicited advice** → Stay in the skill's defined scope
- **Fake enthusiasm** → "NEVER apply different rigor based on reputation"
- **Resume fabrication** → "NEVER add skills not in the master resume"
- **Link dump** → "NEVER present results without your reasoning"
- **Generic cover letter** → Ban list + "NEVER write without a specific hook"
