**Software engineer who actually understands accounting.** I build the internal financial systems at an electrical contractor: billing, job costing, and GL-tied reporting over an MS SQL ERP, plus LLM tooling that is allowed to say "I don't know."

## Live demos, no login

### [Construction financials →](https://job-dashboard-demo.pkbowman.com)

Progress billing, AR aging and DSO, job costing and cost-to-complete, lien waiver tracking, and a natural-language query layer over the financials. That layer runs on Anthropic tool use with JSON-schema-constrained tools rather than free-form generation, and validates the SQL against an AST before anything executes, because over financial data a confidently wrong answer is worse than no answer. Someone downstream acts on it.

### [Workforce, identity, and devices →](https://employee-dashboard-demo.pkbowman.com)

Two halves of one problem: who works here, and what they still have access to.

**Payroll.** Weekly timesheet review with automated violation detection across crews: overtime distribution, short days, sub-40-hour weeks, each carrying a suggested correction rather than just a flag.

**Identity and security.** Entra reconciled against the payroll system, surfacing terminated employees still holding paid licenses, active employees with no MFA registered, stale accounts, and service accounts nobody owns. Onboarding and offboarding tracked as task sets covering provisioning, backup configuration, and device recovery, where the case that matters is the offboarding step still open three years later.

**Inventory.** Laptops, phones, lines, and spares with assignment, location, verification age, and Intune compliance posture.

Both codebases are private. They carry our ERP schema and our business logic, so the demos run on separate backends with no production data and are the whole public version of the work.

`Python` · `Flask` · `MS SQL Server` · `SQLAlchemy` · `Docker` · `AWS` · `Anthropic tool use`

## The pinned repositories are from before this

Eight years teaching high school computer science, 2016 to 2024.

[**headsup3**](https://github.com/philbowman/headsup3) is a containerized calendar-sync service that replaced printed daily schedules at a 1,000-student school and ran in production for four years.

[**ZrRobot**](https://github.com/philbowman/ZrRobot) is the largest: a Flask grading platform over Google Classroom and PowerSchool, whose rubric engine nests rubrics inside one another, so an assignment grade, a unit grade, and a course grade all run through the same scoring code. The four grading categories are packed into the decimal places of a single integer, which is how a standards-based rubric survives a round trip through a gradebook that stores one number per submission.

---

[pkbowman.com](https://pkbowman.com) · [LinkedIn](https://www.linkedin.com/in/philipkbowman)
