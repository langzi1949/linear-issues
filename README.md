# Playground

This workspace stores planning and execution assets for multiple personal projects.

## Projects
### Project Example
```
在projects目录下进行项目的创建。比如
- `projects/ai-agent-learning-copilot-demo`: 15-day AI agent demo project with Linear planning assets
- `projects/english-file-beginner-a1-30-day`: 30-day English learning plan with Linear import CSV
- `projects/ai-agents-langgraph-mcp-rag-14-day`: 14-day AI Agent learning and demo project with Linear import CSV
```

## 目的
所有的目的都是为了创建Linear的一个sprint或者cycle，为的是能够自我约束，以项目管理的方式进行学习。

## 你的职责
1. 需要在对应的项目中创建几个文件
- 创建一个csv文件，用于导入Linear的project等信息
- csv包含的header/column信息有：Title、Description、Priority、Assignee、Labels、Estimate
- 输出不仅是csv文件本身，还要有可执行的issue结构
- 任务拆分优先按“天”组织，确保每条issue可以在当天闭环完成

2. 需要理解Linear需要哪些信息，其中Assignee赋值永远是:chenzehao

## 任务拆分原则
- 先确定周期、日投入时长、主教材、辅助材料和最终目标，再开始拆任务
- 主线任务按教材节奏拆分；如果教材天然按章节或单元组织，优先按固定节奏切成daily issue
- 复习、整合、专项训练等内容不要堆到最后，应该按固定周期穿插到主线任务中
- 每条任务必须同时包含输入和输出，不能只有阅读、听音频或看视频
- 输出任务优先口语，并量化到句子数、录音时长、复述次数等可以验收的动作
- 辅助材料只定义学习动作和验收标准，不强制绑定具体素材编号；例如可以要求完成精听、跟读、复述，但不指定具体哪一期音频
- 如果主教材和辅助材料在同一天都很重，优先拆成两条独立issue，而不是塞进同一条任务里
- 拆分粒度以“当天能否闭环”为准；如果当天无法完成学习、输出和验收，说明任务仍然过大
- 当项目适合使用Linear管理时，默认一条issue对应一个可独立完成的日任务

## Linear Issue 要求
- CSV固定列为：`Title`、`Description`、`Priority`、`Assignee`、`Labels`、`Estimate`
- `Assignee` 默认固定为 `chenzehao`
- `Title` 使用统一命名方式，能直接看出任务发生在哪一天以及对应哪一段学习内容
- `Description` 必须符合 `SMART`
- `Description` 必须写清：
  - 当天学习范围
  - 当天必须完成的动作
  - 量化标准
  - 完成判定
- 每条issue必须同时包含：
  - 主教材任务
  - 辅助材料任务
  - 输出任务
  - 验收标准
- 如果主教材任务和辅助材料任务被拆成两条issue，则每条issue都必须有自己的输出任务和完成标准
- 禁止使用“熟悉本章内容”“提高听力”“掌握表达”这类不可验收的表述
- 应改写为可验证动作，例如“口头造句不少于10句”“录制1段2-3分钟音频”“完成1次无稿复述”
- 如果任务是学习项目，优先让Description覆盖单日闭环，不把跨多天的执行细节压缩到一条issue里

## AI Contribution
- This repository allows AI-assisted planning, writing, task splitting, CSV generation, and documentation drafting.
- AI is used as a productivity tool, not as the final authority on correctness.
- Final responsibility for scope, acceptance criteria, commits, and pushes remains with the repository owner.
- When AI materially contributes to a change, prefer making that visible in commit messages, PR descriptions, or project notes.
- Recommended wording for transparent attribution:
  - `AI-assisted with Codex`
  - `AI-assisted with Claude Code`
  - `AI-assisted planning and drafting`
- Do not claim AI participation if the change was fully authored or materially rewritten by hand after the initial draft.

## Commit Message Convention
- Use short, imperative commit subjects.
- Prefer the format: `<type>: <summary>`.
- Recommended commit types:
  - `feat`: new project assets, new plans, new CSV files
  - `docs`: README updates, notes, planning rules, explanations
  - `refactor`: reorganizing existing content without changing intent
  - `fix`: correcting task definitions, labels, estimates, naming, or formatting mistakes
  - `chore`: repository maintenance or non-content updates
- If AI materially helped with the change, append a transparent suffix in the subject or body.
- Recommended subject patterns:
  - `docs: update workspace rules (AI-assisted with Codex)`
  - `feat: add AI agent learning Linear plan (AI-assisted with Codex)`
  - `fix: rebalance estimates in English learning CSV`
- Keep the subject line focused on the repository change, not the tool.
- If more detail is needed, use the commit body for:
  - what changed
  - why it changed
  - whether AI was used for planning, drafting, or restructuring


## Conventions
- Keep the top-level `README.md` as the workspace index
- Put each project's detailed files into its own descriptive directory under `projects/`
- Use the top-level `README.md` to store reusable task-splitting and Linear issue rules; keep project-specific execution files under `projects/`
