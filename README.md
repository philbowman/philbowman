**Software engineer who actually understands accounting, and taught for eleven years before that.** I build the internal financial systems at a 100-person electrical contractor: billing, job costing, and GL-tied reporting over an MS SQL ERP, plus LLM tooling that is allowed to say "I don't know."

## Live demos running production code, separate environment, fake data, no login

### [Job Dashboard](https://job-dashboard-demo.pkbowman.com) (Construction financials)

Progress billing, AR aging and DSO, job costing and cost-to-complete, lien waiver tracking, and a natural-language query layer over the financials. That layer runs on Anthropic tool use with JSON-schema-constrained tools rather than free-form generation, and validates the SQL against an AST before anything executes, because over financial data a confidently wrong answer is worse than no answer. Someone downstream acts on it.

### [Employee Dashboard](https://employee-dashboard-demo.pkbowman.com) (Workforce, identity, and devices)

Two halves of one problem: who works here, and what they still have access to.

**Payroll.** Weekly timesheet review with automated violation detection across crews: overtime distribution, short days, sub-40-hour weeks, each carrying a suggested correction rather than just a flag.

**Identity and security.** Entra reconciled against the payroll system, surfacing terminated employees still holding paid licenses, active employees with no MFA registered, stale accounts, and service accounts nobody owns. Onboarding and offboarding tracked as task sets covering provisioning, backup configuration, and device recovery, where the case that matters is the offboarding step still open three years later.

**Inventory.** Laptops, phones, lines, and spares with assignment, location, verification age, and Intune compliance posture.

The demos run production code in their own environment with fake data. The application codebases stay private.

`Python` · `Flask` · `MS SQL Server (pymssql)` · `SQL` · `sqlglot` · `PostgreSQL` · `Docker` · `AWS` · `Anthropic tool use`

## The pinned repositories are from before this

Eleven years teaching high school Computer Science, Design Technology, and English Language Arts, 2013 to 2024, at the American Community School of Amman and the American School of Kuwait.

[**headsup3**](https://github.com/philbowman/headsup3) is a containerized calendar-sync service. It merged nine conflicting schedules, with variants for division, weekday and exceptions, into authoritative Google Calendar events, replacing printed daily schedules for roughly 550 students and teachers across the middle and high school. It ran in production for four years across two rebuilds. The scheduling data comes out of PowerSchool's Oracle schema through custom PowerQueries written for the purpose, one of which joins seven tables to answer where a section meets and when.

`Python` · `SQL (custom PowerSchool PowerQueries, Oracle)` · `Google REST APIs` · `Docker` · `AWS EC2` · `pandas` · `httpx`

[**ZrRobot**](https://github.com/philbowman/ZrRobot) is the largest: a Flask grading platform over check50, Google Classroom, and PowerSchool, whose rubric engine nests rubrics inside one another, so an assignment grade, a unit grade, and a course grade all run through the same scoring code. The four grading categories are packed into the decimal places of a single integer, which is how a standards-based rubric survives a round trip through a gradebook that stores one number per submission.

`Python` · `Flask` · `SQLAlchemy` · `Alembic` · `SQL`

[**multi-puller**](https://github.com/philbowman/multi-puller) is a CLI tool for bulk-cloning student repositories and indexing them into a navigable HTML review page.

---

[pkbowman.com](https://pkbowman.com) · [LinkedIn](https://www.linkedin.com/in/philipkbowman)
