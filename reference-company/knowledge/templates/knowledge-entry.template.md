---
title: Knowledge Entry Template
status: template
classification: internal
reference_type: reference-default
policy_effect: none
fictional: false
date: 2026-10-19
---

# 知识条目

用于将可复用的案例、SOP、Skill、检查表或决策原则整理为组织知识。原始任务、聊天和运行事件不自动成为知识。

## 使用说明

- **谁填写**：Maestro 或领域知识维护责任人起草；责任岗位和指定审阅人确认。
- **何时用**：某次工作已产生可复用方法、稳定结论或明确的失败教训时；复用前检查适用范围和复核日期。
- **证据要求**：列出来源任务、决定、产物版本、验证记录和已知局限。
- **权限要求**：选择最小披露范围；从受限来源提炼出的摘要不能泄露原文中的敏感字段。
- **未决点**：将推测、争议和需要进一步验证的内容单独标注，不写进“已确认方法”。

## 1. 元数据

- `knowledge_id`：
- `title`：
- `knowledge_type`：SOP / skill / case / checklist / principle
- `status`：draft / reviewed / published / superseded
- `classification`：public / internal / restricted / highly-restricted
- `owner_role`：
- `reviewer_role`：
- `version`：
- `effective_from`：
- `review_due`：
- `policy_effect`：none（模板默认）；正式企业采用时另按发布记录填写

## 2. 结论或方法

- `summary`：
- `when_to_use`：
- `when_not_to_use`：
- `preconditions`：
- `steps`：
  1.
  2.
- `expected_output`：
- `failure_signals`：
- `escalation`：

## 3. 来源与验证

| 来源类型 | 引用 | 说明 | 核实时间 |
|---|---|---|---|
| 任务 / 决定 / Repo / 业务系统 |  |  |  |

- `validation_method`：
- `validation_result`：confirmed / partial / needs-retest
- `limitations`：

## 4. 披露与复用

- 可见范围：
- 可被哪些岗位/Agent 检索：
- 需要脱敏的字段：
- 可否复制到外部材料：需另行确认 / 不可
- 复用反馈入口：Stage knowledge feedback 事件

## 5. 未决问题和维护

- `unknowns`：
- `open_questions`：
- `supersedes`：
- `maintenance_trigger`：规则变化、工具变化、失败率上升或 review_due 到期

> 知识条目的发布是 ScoreBook 的版本事件；Stage 是否已加载、哪些岗位实际可见，必须以 Stage 回执为准。
