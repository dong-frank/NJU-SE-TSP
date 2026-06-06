# Project Instructions for AI Assistants

## Context

This workspace is for the Software Quality and Management course assignment.
The assignment asks the team to role-play a software development team using the
TSP (Team Software Process) launch meeting approach, then produce a project
planning proposal for an LLM code-completion evaluation platform.

The team has 4 members. Use the 4-person-team requirement consistently:

- Platform launch cycle: 2 weeks.
- Proposal preparation time: 3 days.
- Phase 1 deadline: 2026-06-12.
- Phase 2 deadline: 2026-06-19.

Do not change the 2-week launch cycle to 3 weeks. The 3-week note only applies
to 3-person teams, and this team has 4 members.

## Important Assignment Interpretation

The assignment is not primarily asking the team to actually develop the
platform. The key task is to build and demonstrate a credible TSP-style team
startup process, including team formation, role allocation, launch meetings,
planning, quality strategy, risk handling, and team commitment.

For TSP theory and courseware-aligned interpretation, read
`TSP理论知识参考.md`. It summarizes pages 25-55 of
`软件质量与管理.第三讲.pdf` and should be treated as the local reference when
creating the proposal, PPT, meeting records, or Phase 2 answer material.

For the FIM platform requirements, read `FIM需求沉淀.md` first. It summarizes
the requirement package under `FIM评测平台需求/` into project goals, scope,
functional and non-functional requirements, MVP implications, TSP meeting
inputs, risks, and Phase 2 evidence.

When the user provides TSP meeting records and asks to advance the assignment,
use the project-local skill at `skills/advance-tsp-meetings/SKILL.md`. It
converts meeting notes into meeting outputs, proposal updates, gaps, next
actions, and Phase 2 evidence.

The final score is based on answers to Phase 2 questions. However, every Phase
2 answer must come only from the Phase 1 project planning proposal. No new
content may be added in Phase 2. Therefore, treat the Phase 1 proposal as the
single evidence base for later answers.

When helping with this assignment, optimize the proposal for answerability:
make it complete, self-consistent, and easy to cite during Phase 2. The proposal
should contain enough material to answer likely questions about scope, schedule,
roles, process, estimates, quality, risks, trade-offs, and team commitments.

The teacher mentioned that the proposal may be in PPT form, but the essential
deliverable is the project planning proposal itself. The format can be adjusted
as needed, but the content must work as the Phase 2 evidence base.

## TSP Role Model

All 4 team members are developers. Each member may also take one or more TSP
management roles.

Typical TSP roles to represent:

- Project Leader: coordinates the team, protects commitments, and handles
  overall project direction.
- Planning Manager: organizes Meeting 4 and Meeting 6. The plan is developed
  through team discussion; the planning manager facilitates the plan rather than
  deciding it alone.
- Development Manager: usually leads the development strategy in Meeting 3 and
  guides team estimation in Meeting 4.
- Quality Manager: focuses on preventing defects through review and process
  control, not merely finding defects through testing. Warns the project leader
  about quality issues and hosts Meeting 5.
- Process Manager: emphasizes that process quality determines result quality.
  Leads process definition in Meeting 3.
- Support Manager: ensures the team has suitable tools, environment, templates,
  repositories, communication channels, and supporting materials. Does not own a
  specific meeting, but supports every meeting.

Because the team has only 4 people, combine roles sensibly while keeping all
role responsibilities visible.

## Suggested Launch Meeting Structure

Use the assignment-specific TSP launch meeting storyline as the main organizing
logic when creating or revising the proposal. Although the courseware shows a
complete 10-meeting TSP Launch, this assignment removes the final 3 meetings;
use Meetings 1-7 as the proposal structure.

- Meetings 1-2: understand goals, establish team objectives, define success
  criteria, and assign roles.
- Meeting 3: define development strategy and team process. Development Manager
  leads the development strategy; Process Manager leads process definition.
- Meeting 4: develop the project plan. Planning Manager facilitates the plan;
  Development Manager guides estimation; the whole team discusses and commits.
- Meeting 5: develop the quality plan. Quality Manager leads review strategy,
  defect prevention, quality metrics, and quality warnings.
- Meeting 6: balance the plan. Planning Manager facilitates trade-off decisions,
  risk adjustment, schedule balancing, and final team commitment.
- Meeting 7: assess risks. The team asks "what if" questions, records major
  risks, assigns owners, and defines mitigation and contingency actions.

The proposal should make clear that the plan is the team's shared commitment,
not the unilateral decision of a single role.

## Content Priorities

When producing or improving the proposal, include:

- project background and expert-facing value proposition;
- team goals and product goals;
- 4-person role allocation and responsibility matrix;
- TSP launch meeting agenda, decisions, and outputs;
- scope and non-scope;
- development strategy for a 2-week MVP;
- process definition and collaboration workflow;
- task decomposition and schedule;
- estimation method and assumptions;
- quality plan based on reviews, inspections, process checks, and testing;
- risk list with mitigation and contingency;
- support plan for tools, environment, documents, and communication;
- acceptance criteria and delivery commitment;
- a Phase 2 answerability index, if useful.

Avoid over-focusing on real implementation details at the expense of TSP team
formation and process discipline. Technical details should support planning,
estimation, quality, and risk arguments.

## Repository Reading Boundaries

The `FIM评测平台需求/` directory contains platform requirement material. Only read
or analyze it when the user explicitly asks to work with those requirements.
Until then, do not inspect that directory.
