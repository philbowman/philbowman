**Software engineer who actually understands accounting.** I build the internal financial systems at an electrical contractor: billing, job costing, and GL-tied reporting over an MS SQL ERP, plus LLM tooling that is allowed to say "I don't know."

## Live demos, no login

### [Construction financials →](https://job-dashboard-demo.pkbowman.com)

Progress billing, AR aging and DSO, job costing and cost-to-complete, lien waiver tracking, and a natural-language query layer over the financials. That layer runs on Anthropic tool use with JSON-schema-constrained tools rather than free-form generation, and validates the SQL against an AST before anything executes, because over financial data a confidently wrong answer is worse than no answer. Someone downstream acts on it.

### [Workforce and timesheets →](https://employee-dashboard-demo.pkbowman.com)

Weekly timesheet review with automated violation detection: overtime distribution, short days, sub-40-hour weeks, each with a suggested correction rather than just a flag. Extends into employee lifecycle, device management across Intune and Entra, and license tracking, because onboarding a field employee is a payroll problem and an IT problem at the same time.

Both codebases are private. They carry our ERP schema and our business logic, so the demos run on separate backends with no production data and are the whole public version of the work.

`Python` · `Flask` · `MS SQL Server` · `SQLAlchemy` · `Docker` · `AWS` · `Anthropic tool use`

## The pinned repositories are from before this

Eight years teaching high school computer science, 2016 to 2024.

[**headsup3**](https://github.com/philbowman/headsup3) is a containerized calendar-sync service that replaced printed daily schedules at a 1,000-student school and ran in production for four years.

[**ZrRobot**](https://github.com/philbowman/ZrRobot) is the largest: a Flask grading platform over Google Classroom and PowerSchool, whose rubric engine nests rubrics inside one another, so an assignment grade, a unit grade, and a course grade all run through the same scoring code. The four grading categories are packed into the decimal places of a single integer, which is how a standards-based rubric survives a round trip through a gradebook that stores one number per submission.

---

[pkbowman.com](https://pkbowman.com) · [LinkedIn](https://www.linkedin.com/in/philipkbowman)
