# Linear Learning Projects

This repository is a workspace for building personal learning projects as executable `Linear` issue plans.

The core idea is simple:
- choose one learning topic
- define a fixed cycle
- split the work into daily issues
- export the plan as a CSV that can be imported into `Linear`

## Repository Structure
- `projects/`: one directory per learning project
- top-level `README.md`: shared rules, templates, and working conventions

Current project examples:
- `projects/english-file-beginner-a1-30-day`: 30-day English learning plan with Linear import CSV
- `projects/ai-agents-langgraph-mcp-rag-14-day`: AI Agent learning and RAG demo plan with Linear import CSV

## Goal
The purpose of this repository is to turn learning into a project-managed workflow.

Instead of keeping goals vague, each topic should be converted into:
- a bounded time period
- a concrete set of daily issues
- measurable outputs
- explicit review points

## Standard Output
Each project should usually contain:
- a project-level `README.md`
- a `MILESTONES.md` file that defines project milestones
- a `linear_issues.csv` file for import into `Linear`

The CSV columns are fixed:
- `Title`
- `Description`
- `Priority`
- `Assignee`
- `Labels`
- `Estimate`

Default rule:
- `Assignee` is always `chenzehao`

## Task Splitting Rules
- Lock the cycle length, daily study time, primary material, supporting material, and target outcome before splitting work.
- Define project milestones before writing issues or CSV rows.
- Default to `daily issues`, not broad weekly buckets.
- Each issue should be completable within the same day.
- Each issue must include both `input` and `output`; reading or listening alone is not enough.
- Output should be measurable, for example:
  - number of sentences
  - recording length
  - review notes
  - demo artifacts
  - test questions
- If review is important, create explicit `review` or `revise` issues instead of hiding review inside normal study tasks.
- If one day contains two heavy tracks, such as primary material plus supporting practice, prefer splitting them into separate issues.
- Supporting materials should be defined by task type and acceptance criteria, not by forcing one exact source item unless the source itself matters.

## Milestone Rules
- Each project must have a `MILESTONES.md` file.
- `MILESTONES.md` defines the milestone list that the CSV will use.
- Each milestone must include:
  - `Title`
  - `Description`
- Create milestones before generating `linear_issues.csv`.
- Each issue must belong to exactly one milestone.
- Put milestone ownership in `Labels`, not in free-form topic or task-type tags.

## Linear Issue Rules
- `Title` should make the day and task scope obvious.
- `Description` must follow `SMART`.
- `Labels` is not a free-form tag collection in this repository.
- `Labels` must contain exactly one value.
- That value must exactly match one milestone `Title` from the project's `MILESTONES.md`.
- Each `Description` must state:
  - task scope
  - required actions
  - measurable output
  - completion criteria
- Avoid non-verifiable wording such as:
  - “熟悉本章内容”
  - “提高听力”
  - “掌握表达”
- Rewrite those into observable actions such as:
  - “口头造句不少于10句”
  - “录制1段2-3分钟音频”
  - “完成1次无稿复述”

## AI Contribution
- This repository allows AI-assisted planning, writing, task splitting, CSV generation, and documentation drafting.
- AI is a productivity tool, not the final authority on correctness.
- Final responsibility for scope, acceptance criteria, commits, and pushes remains with the repository owner.
- When AI materially contributes to a change, prefer making that visible in commit messages, PR descriptions, or project notes.

Recommended attribution wording:
- `AI-assisted with Codex`
- `AI-assisted with Claude Code`
- `AI-assisted planning and drafting`

Do not claim AI contribution if the final result was fully rewritten by hand and the AI draft no longer materially shaped the outcome.

## Commit Message Convention
- Use short, imperative commit subjects.
- Preferred format: `<type>: <summary>`

Recommended types:
- `feat`: new project assets, new plans, new CSV files
- `docs`: README updates, notes, planning rules, explanations
- `refactor`: restructuring existing content without changing intent
- `fix`: correcting task definitions, labels, estimates, naming, or formatting mistakes
- `chore`: repository maintenance or non-content updates

If AI materially helped, add transparent attribution in the subject or body.

Recommended examples:
- `feat: add AI agent learning Linear plan (AI-assisted with Codex)`
- `docs: update workspace rules (AI-assisted with Codex)`
- `fix: rebalance estimates in English learning CSV`

## Working Convention
- Keep the top-level `README.md` focused on reusable rules and repository entry guidance.
- Keep project-specific details inside each project directory under `projects/`.
- When a project evolves, update that project's local `README.md`, `MILESTONES.md`, and `linear_issues.csv` instead of overloading the top-level README.
