# Ethical Career Agent

An AI career agent built on [Claude Code](https://claude.ai/code) that helps people find meaningful work — with honesty, values alignment, and genuine human connection at the center.

## What It Does

11 skills that chain together into a full career pipeline:

| Skill | Command | What It Does |
|-------|---------|-------------|
| Profile Setup | `/profile-setup` | Build your career profile — values, deal-breakers, preferences |
| Job Search | `/job-search` | Curated, scored results with ethical company signals |
| Evaluate Company | `/evaluate-company` | 7-dimension ethical rubric (35-point scale) |
| Tailor Resume | `/tailor-resume` | Honest tailoring — highlights real fit, flags real gaps |
| Cover Letter | `/cover-letter` | Specific, authentic letters (refuses to write generic ones) |
| Interview Prep | `/interview-prep` | STAR stories, company research, questions to ask back |
| Application Tracker | `/application-tracker` | Track stages, follow-ups, and conversion |
| Community Find | `/community-find` | Discover communities aligned with your craft and values |
| Connect Request | `/connect-request` | Genuine outreach (enforces the Genuine Connection Test) |
| Side Project Scope | `/side-project-scope` | Scope ideas into weekend, quarterly, or full venture |
| Find Collaborators | `/find-collaborators` | Find co-founders from communities and directories |

## What Makes It Different

**It has opinions.** Job search results are scored and ranked, not dumped as a list. Company evaluations flag real concerns. Cover letters are refused when there's no genuine connection to build on.

**It refuses to help you lie.** Won't fabricate resume credentials, generate mass-application spam, or draft dishonest outreach. Surfaces gaps honestly so you can address them — in the cover letter, in the interview, or by finding a better-matched role.

**It centers values.** Your deal-breakers are first-class filters. If a company triggers one, the agent leads with that — before any other analysis.

## How It Works

Built as a Claude Code agent with custom skills, hooks, and test personas:

```
.claude/
├── agents/ethical-career-agent.md    # Unified agent definition
├── skills/                           # 11 skill definitions
├── data/
│   ├── personas/                     # 6 test personas for validation
│   └── interactions/                 # 11 example interactions (good + bad)
├── docs/                             # Architecture docs and data schema
└── settings.json                     # Hooks and permissions
```

User data stays local at `~/.career/`. Nothing is sent externally.

## Design Process

The interaction logs in [.claude/data/interactions/](.claude/data/interactions/) document both **beneficial** and **unhelpful** agent behaviors. The unhelpful examples — preachy lecturing, dismissive shaming, resume fabrication, uncritical cheerleading — directly informed the Critical Rules in every skill definition.

## Test Personas

6 personas with detailed backstories, emotional triggers, and success criteria:
- **Kenny Lema** — 21, CS senior, wants varied work at mission-driven outdoor tech
- **Priya Sharma** — 29, data scientist pivoting to climate tech
- **Marcus Webb** — 28, backend engineer, civic tech, laid off
- **Diana Chen** — 34, data engineer leaving oil & gas for clean energy
- **Elena Vasquez** — 42, warehouse worker exploring career change
- **James Okafor** — 38, nonprofit director exploring private sector

## Getting Started

1. Clone this repo
2. Open in VS Code with the Claude Code extension
3. Run `/profile-setup` to build your career profile
4. Run `/job-search [role]` to start searching

## Built With

[Claude Code](https://claude.ai/code) — Anthropic's CLI and IDE extension for Claude.
