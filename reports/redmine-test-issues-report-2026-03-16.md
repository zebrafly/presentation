#!/usr/bin/env markdown
# Redmine 项目任务分析报告（test）

- 生成时间：2026-03-16（Asia/Shanghai）
- 项目：test（`project_id=1`）
- 数据来源：Redmine `GET /issues.json?project_id=1&status_id=*`（共 12 条）
- 统计口径：
  - 总体进度：按 `done_ratio` 的算术平均值作为“完成度（%）”
  - 逾期：`due_date` 早于 2026-03-16 且状态未关闭（`status.is_closed=false`）；`due_date` 为空不计为逾期，但计入“无截止日期风险”

## 1. 总览（摘要）

| 指标 | 数值 |
| --- | ---: |
| Issues 总数 | 12 |
| 已关闭（Closed） | 0（0.0%） |
| 平均完成度（done_ratio） | 0.0% |
| 有截止日期（due_date 非空） | 0（0.0%） |
| 逾期任务 | 0 |
| 未指派（assigned_to 为空） | 1（8.3%） |

结论：当前项目任务全部处于 **New** 且 `done_ratio=0`，并且 **100% 缺少截止日期**，导致无法进行基于交付时间的风险管理与排期跟踪。

## 2. 状态分布（Status）

| 状态 | 数量 | 占比 |
| --- | ---: | ---: |
| New | 12 | 100.0% |

## 3. 总体进度（Progress）

- 平均完成度：0.0%
- 已关闭占比：0.0%

建议：若团队流程允许，尽快将可执行任务推进到 In Progress/Resolved，并对关键任务补齐 `done_ratio`（或通过子任务/版本里程碑体现真实进度）。

## 4. 成员任务情况（Assigned To）

| 成员 | 数量 | 其中 New | 已关闭 | 平均完成度 |
| --- | ---: | ---: | ---: | ---: |
| John Smith | 11 | 11 | 0 | 0.0% |
| 未指派 | 1 | 1 | 0 | 0.0% |

观察：
- 任务高度集中在单一成员（John Smith），存在单点风险与吞吐瓶颈风险。
- 存在未指派任务 1 条，建议尽快明确责任人（避免遗漏）。

## 5. 逾期与排期风险（Overdue & Scheduling）

### 5.1 逾期任务

本次数据中 `due_date` 全部为空，因此逾期任务数为 0；但这意味着当前无法基于截止日期识别进度风险。

### 5.2 无截止日期任务（高风险）

- 无截止日期：12 / 12（100.0%）

建议：
- 至少为高优先级任务设置 `due_date`，并建立每周滚动计划（例如每周一更新当周截止日期与优先级）。

## 6. 优先级与类型分布（Priority & Tracker）

- 优先级：High = 12（100.0%）
- Tracker：Bug = 12（100.0%）

提示：若长期“全是 High”，优先级体系会失效；建议结合业务影响/紧急程度，合理下调非关键事项到 Normal/Low，并用版本/里程碑管理交付节奏。

## 7. 明细清单（Issues）

| ID | 标题 | 状态 | 优先级 | 指派给 | 完成度 | 开始日期 | 截止日期 |
| ---: | --- | --- | --- | --- | ---: | --- | --- |
| 15 | very urgent issue | New | High | John Smith | 0 | 2026-03-16 | - |
| 11 | Homepage not loading on mobile devices #10 | New | High | John Smith | 0 | 2026-03-16 | - |
| 10 | Homepage not loading on mobile devices #9 | New | High | John Smith | 0 | 2026-03-16 | - |
| 9 | Homepage not loading on mobile devices #8 | New | High | John Smith | 0 | 2026-03-16 | - |
| 8 | Homepage not loading on mobile devices #7 | New | High | John Smith | 0 | 2026-03-16 | - |
| 7 | Homepage not loading on mobile devices #6 | New | High | John Smith | 0 | 2026-03-16 | - |
| 6 | Homepage not loading on mobile devices #5 | New | High | John Smith | 0 | 2026-03-16 | - |
| 5 | Homepage not loading on mobile devices #4 | New | High | John Smith | 0 | 2026-03-16 | - |
| 4 | Homepage not loading on mobile devices #3 | New | High | John Smith | 0 | 2026-03-16 | - |
| 3 | Homepage not loading on mobile devices #2 | New | High | John Smith | 0 | 2026-03-16 | - |
| 2 | Homepage not loading on mobile devices #1 | New | High | John Smith | 0 | 2026-03-16 | - |
| 1 | Homepage not loading on mobile devices | New | High | - | 0 | 2026-03-16 | - |
