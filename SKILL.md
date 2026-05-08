---
name: linear-learning-projects
description: Use this skill when working in this repository to create or update project-based learning plans that are exported as Linear import CSV files. Apply it for new study projects, issue splitting, SMART task writing, review-cycle insertion, label and estimate assignment, and project README generation under projects/.
---

# Linear Learning Projects

This repository is used to turn personal learning goals into executable `Linear` issue plans.

Use this skill when the task involves:
- creating a new learning project under `projects/`
- updating an existing learning plan
- generating or revising `linear_issues.csv`
- converting a topic, book, course, or demo goal into daily `Linear` issues
- inserting review or revise tasks into a learning cycle

## Repository Contract

For each project, create or maintain:
- `projects/<project-name>/README.md`
- `projects/<project-name>/linear_issues.csv`

Top-level rules live in:
- `/Users/chenzehao/Documents/Playground/README.md`

Read the top-level `README.md` first when:
- naming a new project
- deciding CSV columns
- choosing issue granularity
- deciding how to describe AI contribution or commit messages

## Required CSV Shape

The CSV columns are fixed:
- `Title`
- `Description`
- `Priority`
- `Assignee`
- `Labels`
- `Estimate`

Defaults:
- `Assignee` is always `chenzehao`
- `Description` must be `SMART`

## Workflow

1. Clarify the learning scope.
2. Lock the cycle length and daily time budget.
3. Identify:
   - primary material
   - supporting material
   - output form
   - demo or implementation goal
4. Split work into daily issues.
5. Insert explicit `review` or `revise` issues when consolidation matters.
6. Write `SMART` descriptions with measurable outputs and same-day acceptance criteria.
7. Create or update the project `README.md`.
8. Generate or revise `linear_issues.csv`.

## Issue Design Rules

- Prefer `daily issues` over vague phase-based tasks.
- Each issue must be completable in the same day.
- Each issue must include both `input` and `output`.
- If one day contains two heavy tracks, split them into separate issues.
- Use separate review issues instead of burying review inside normal study tasks.
- Supporting materials should usually be described by task type, not by forcing one exact asset or episode, unless the exact source matters.

## Description Rules

Each `Description` should make four things explicit:
- scope
- required actions
- measurable output
- completion criteria

Avoid vague wording such as:
- “熟悉本章内容”
- “提高听力”
- “掌握表达”

Prefer observable actions such as:
- “整理不少于10条关键点”
- “录制1段3分钟音频”
- “完成1次无稿复述”
- “输出1份demo设计文档”

## Labels and Estimates

Choose labels by work type, not by topic name alone.

Typical label patterns:
- learning projects: `*-learning`
- source material: `book-study`, `course-study`
- implementation: `demo`, `rag`, `agent-workflow`
- review tasks: `review`, `revise-check`

Use estimates comparatively inside the same project:
- lighter study task: smaller estimate
- review day: medium estimate
- implementation or synthesis day: larger estimate

Keep estimate logic consistent across the same project.

## Project README Pattern

Each project `README.md` should usually include:
- project scope
- time period
- primary source
- supporting source
- output expectations
- file list
- issue design summary

Keep it short. The project README is an execution index, not a textbook summary.

## AI Attribution

This repository allows AI-assisted planning and drafting.

If AI materially contributed, prefer transparent wording in commits or notes such as:
- `AI-assisted with Codex`
- `AI-assisted with Claude Code`

Do not overstate AI contribution if the final result was substantially rewritten by hand.
