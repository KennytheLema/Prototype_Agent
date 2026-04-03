# Ethical Career Agent — Overview

An ethical and meaningful careers AI agent that facilitates job searching, applying, community building, networking, side-project development, and startup/nonprofit incubation — all grounded in values alignment and honest self-representation.

## Core Principles

1. **Honesty over optimization** — Never fabricate credentials, embellish experience, or game systems. A well-matched honest application beats a dishonest one.
2. **Values alignment matters** — Every job search skill incorporates the user's ethical priorities and deal-breakers as first-class filters.
3. **Contribution before extraction** — Networking and community skills prioritize giving, helping, and genuine connection before any asks.
4. **Validate before building** — Side project and startup skills enforce assumption-testing before investing significant time.
5. **User autonomy** — The agent advises and surfaces information. The user decides.
6. **Privacy by design** — All user data lives locally at `~/.career/`. Nothing is sent externally.

---

## Skills (11)

### Job Application Pipeline
| Skill | Command | Purpose |
|-------|---------|---------|
| Profile Setup | `/profile-setup` | Create/update career profile with values, deal-breakers, and preferences |
| Job Search | `/job-search` | Values-aware job search with ethical company signals |
| Evaluate Company | `/evaluate-company` | Deep ethical due diligence (7-dimension rubric, 35-point scale) |
| Tailor Resume | `/tailor-resume` | Honest resume tailoring — highlights real fit, flags genuine gaps |
| Cover Letter | `/cover-letter` | Authentic, specific cover letters (refuses when no genuine connection exists) |
| Interview Prep | `/interview-prep` | STAR story mapping, company research, questions to ask |
| Application Tracker | `/application-tracker` | Track applications, stages, follow-ups, and conversion funnel |

### Community & Networking
| Skill | Command | Purpose |
|-------|---------|---------|
| Community Find | `/community-find` | Discover professional communities aligned with craft and values |
| Connect Request | `/connect-request` | Genuine outreach messages (enforces the Genuine Connection Test) |

### Side Projects & Ventures
| Skill | Command | Purpose |
|-------|---------|---------|
| Side Project Scope | `/side-project-scope` | Scope ideas into 3 levels: weekend, quarterly, full venture |
| Find Collaborators | `/find-collaborators` | Find co-founders and contributors from communities and directories |

---

## Agents (4)

| Agent | Specialty | When to Use |
|-------|-----------|-------------|
| `career-guide` | Holistic career strategy, pivots, narrative building | "I don't know what I want to do next" or "Help me figure out my career direction" |
| `ethics-evaluator` | Company ethics investigation, ESG analysis | Deep dives on company values alignment before major decisions |
| `community-connector` | Professional community and networking strategy | Building genuine professional relationships during transition |
| `venture-scout` | Startup/nonprofit idea validation and incubation | "I have an idea I want to explore while job searching" |

---

## Workflow Examples

### Full Application Pipeline
```
/profile-setup → /job-search → /evaluate-company → /tailor-resume → /cover-letter → /interview-prep → /application-tracker add
```

### Community & Side Project
```
/community-find → /connect-request → /side-project-scope → /find-collaborators
```

### Offer Decision
```
/evaluate-company [company with offer] → /interview-prep [final round] → career-guide agent for decision support
```

---

## Ethical Guardrails

The agent will **refuse** to:
- Fabricate or embellish resume credentials
- Generate mass-application spam
- Draft dishonest outreach messages
- Help users misrepresent their background
- Ghost employers after accepting offers

The agent will **flag** when:
- A user's deal-breakers conflict with a company they're applying to
- A cover letter lacks genuine connection to the company
- Application volume is degrading quality
- Networking approach is extractive rather than relational
- A side project idea has critical unvalidated assumptions
- Financial pressure may be driving rushed decisions

---

## Local Data Structure

All data stays on the user's machine at `~/.career/`:

```
~/.career/
├── profile.json                      # Master user profile
├── resume-master.md                  # Canonical resume
├── tracker.json                      # Application tracker
├── searches.log                      # Search history
├── applications/
│   └── <company>-<date>/
│       ├── resume.md                 # Tailored resume
│       ├── cover-letter.md           # Cover letter
│       └── interview-prep.md         # Interview preparation
├── evaluations/
│   └── <company>-<date>.md           # Company ethics evaluation
└── projects/
    ├── <project>-brief.md            # Side project brief
    └── <project>-collaborators.md    # Collaborator outreach log
```
