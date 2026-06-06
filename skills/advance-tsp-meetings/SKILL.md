---
name: advance-tsp-meetings
description: Use when the user provides TSP launch meeting notes, asks how to advance a Software Quality course project proposal from meeting records, or needs meeting outputs converted into proposal sections, gaps, next actions, and Phase 2 answer evidence for a 4-person TSP assignment.
---

# Advance TSP Meetings

## Overview

将用户提供的 TSP 启动会议记录转化为可推进的作业材料：会议纪要、会议产物、项目策划书更新块、缺口检查、下一步行动和阶段二答题证据。这个 skill 面向“软件质量与管理”课程作业，核心是构建和磨合团队，而不是真正推进代码开发。

## Before Processing

在本项目中使用时，先遵守根目录 `AGENTS.md`。如需理论依据，读取 `TSP理论知识参考.md`。不要读取 `FIM评测平台需求/`，除非用户明确要求。

本次作业采用 TSP Launch 的前 7 次会议，去掉最后 3 次：

| 会议 | 作业主题 | 主要产物 |
| --- | --- | --- |
| Meeting 1 | 产品目标和业务目标 | 产品目标、业务目标、成功标准 |
| Meeting 2 | 角色分配和小组目标 | 角色分配、职责矩阵、团队目标 |
| Meeting 3 | 开发流程定义与策略选择 | 过程定义、迭代策略、组件获取策略 |
| Meeting 4 | 整体计划 | WBS、交付物清单、规模/工作量估算、总体计划 |
| Meeting 5 | 质量计划 | 评审机制、质量指标、测试策略、质量资源投入 |
| Meeting 6 | 个人计划和计划平衡 | 个人任务、负载平衡、关键路径、团队承诺 |
| Meeting 7 | 风险评估 | 风险清单、触发条件、应对措施、责任人 |

## Processing Workflow

When the user provides meeting notes, process them in this order:

1. Identify the meeting number.
   - If the user states it, use that.
   - If not, infer from content and state confidence.
   - If multiple meetings are mixed, split them by likely meeting.

2. Extract raw decisions and facts.
   - Preserve concrete names, dates, constraints, numbers, and role assignments.
   - Distinguish decisions from discussion, questions, assumptions, and unresolved issues.
   - Do not invent missing decisions. Mark missing items as gaps.

3. Convert notes into TSP meeting outputs.
   - Produce the artifact expected from that meeting, such as goals, role matrix, process, WBS, quality plan, personal plan, or risk table.
   - If notes are thin, provide a "补充建议" section with candidate content clearly labeled as suggested, not already decided.

4. Update the proposal draft conceptually.
   - Output a "可放入项目策划书的内容" section.
   - Write in formal proposal style, not chatty meeting-note style.
   - Keep it usable as the Phase 1 evidence base for Phase 2 answers.

5. Generate advancement actions.
   - Since the assignment does not require actual development, advance documents and decisions instead of code.
   - List concrete next actions: what to confirm, what table to fill, what section to update, what the next meeting should resolve.

6. Maintain Phase 2 answerability.
   - Add an evidence index: what future Phase 2 question this meeting helps answer, and where the answer should live in the proposal.

If the user asks to edit files, update the relevant project file directly. If no target file exists, ask before creating a new formal deliverable. For ordinary meeting-note processing, reply with structured output instead of creating files automatically.

## Output Format

Use this structure unless the user asks for a different format:

```markdown
## 会议判断
- 对应会议：
- 判断依据：
- 记录完整度：

## 整理后的会议记录
- 会议目标：
- 关键讨论：
- 已形成决策：
- 未决问题：

## 本次会议产物
[根据会议类型输出对应表格或清单]

## 可放入项目策划书的内容
[正式写作版本，可直接改写进策划书]

## 缺口与补充建议
- 必须补齐：
- 建议增强：
- 不应新增到阶段二、需在阶段一预埋：

## 下一步推进
- 会后行动：
- 下一次会议要解决：
- 策划书需更新章节：

## 阶段二答题证据索引
| 未来可能问题 | 本次会议提供的依据 | 策划书建议位置 |
| --- | --- | --- |
```

## Meeting-Specific Guidance

### Meeting 1: 产品目标和业务目标

Focus on "what to build" and "how good is good enough." Separate:

- 产品目标：平台功能范围。
- 业务目标：两周上线、专家认可、可复现、可比较、可用于课程场景。
- 成功标准：可验收、可度量、能支撑答辩。

### Meeting 2: 角色分配和小组目标

Ensure all 4 members are developers and also carry TSP roles. Prefer a responsibility matrix over a bare role list. Check whether team goals conflict with school/expert goals.

### Meeting 3: 开发流程定义与策略选择

Make the process practical for a 2-week MVP. Capture iterations, process steps, component sources, reuse/self-build choices, and collaboration standards. Development Manager leads strategy; Process Manager leads process definition.

### Meeting 4: 整体计划

Convert notes into WBS, deliverables, size assumptions, effort estimates, resource sufficiency, and schedule. Make clear that the Planning Manager facilitates the plan and the team discusses it together.

### Meeting 5: 质量计划

Emphasize reviews and defect prevention before testing. Include requirement review, design review, code/config review, test review, quality metrics, review records, and Quality Manager warnings.

### Meeting 6: 个人计划和计划平衡

Map tasks to people, identify overload, adjust scope or sequencing, and state the final team commitment. The goal is the earliest credible completion time, not the most optimistic date.

### Meeting 7: 风险评估

Use "what if" thinking. For each risk, record trigger, impact, mitigation, contingency, and owner. Cover requirement, schedule, technical, quality, personnel, and support risks.

## Guardrails

- Do not treat meeting notes as final truth when they are incomplete.
- Do not create Phase 2 answers from new content that was not pre-planned for Phase 1.
- Do not over-focus on implementation details; use technical content to support TSP planning, estimation, quality, and risk.
- Do not include Meeting 8-10 as formal assignment meetings unless the user explicitly changes the assignment structure.
- Prefer concise, usable artifacts over long theoretical explanation.
