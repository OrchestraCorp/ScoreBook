---
title: Task Context Package Template
status: template
classification: internal
reference_type: reference-default
policy_effect: none
fictional: false
date: 2026-10-19
---

# 任务上下文包

这份上下文包用于让获授权的员工或 Agent 接手一项工作，而不需要重读全部会话。它是 ScoreBook 的静态模板；实时任务、承诺、状态和权限由 Stage 管理。

## 使用说明

- **谁填写**：任务负责人或其 Agent 起草；责任岗位在交接、验收或重大变更时核对。
- **何时填写**：任务发布时建立；目标、验收、责任人、范围或关键依赖变化时更新；提交验收前必须刷新。
- **证据要求**：每个关键事实链接 Stage 对象、批准决定、Repo 版本、外部业务记录或明确的“待核实”项。
- **权限要求**：只写接收人有权查看的最小必要上下文；敏感原文用受限引用，不在此复制凭据、合同、健康或薪酬资料。
- **未决点**：不能用推断代替事实；无法确认的字段写入 `unknowns` 并指定核实责任。

## 1. 身份与边界

- `task_id`：
- `task_version`：
- `title`：
- `responsible_role`：
- `current_owner`：由 Stage 运行记录填写；本模板不写真实人名
- `collaborating_roles`：
- `classification`：public / internal / restricted / highly-restricted
- `source_stage_ref`：
- `prepared_at`：
- `prepared_by`：岗位或 Agent 身份，不写未经授权的个人识别信息

## 2. 目标与验收

- `intent`：要改变什么，为什么现在做？
- `in_scope`：
- `out_of_scope`：
- `acceptance_criteria`：
  1.
  2.
- `acceptance_authority`：负责确认结果的岗位
- `deadline_and_timezone`：
- `version_change_rule`：目标、验收、截止时间、奖励约定或数据范围变化时，生成新版本并重新确认。

## 3. 已确认事实

| 事实 | 来源 | 核实时间 | 可信状态 |
|---|---|---|---|
|  | Stage / Repo / 业务系统引用 |  | confirmed / reported / needs-check |

## 4. 已作决定与依据

| 决定 | 决策引用 | 批准岗位 | 生效/适用版本 |
|---|---|---|---|
|  | `decision_id` 或 MR |  |  |

## 5. 承诺、依赖与风险

- `current_commitments`：当前已被 Stage 确认的承诺、交付人和期限
- `dependencies`：前置输入、责任岗位、期望时间、解除条件
- `risks`：发生条件、影响、缓解动作、升级时间
- `resource_limits`：预算、容量、工具或数据范围限制（引用规则，不在此自行授予权限）
- `stop_conditions`：出现哪些情况必须暂停并升级

## 6. 产物与证据

- `expected_artifacts`：
- `artifact_refs`：Repo 路径、MR、外部系统对象或 Stage 附件引用
- `verification_plan`：谁按什么检查，结果写在哪里
- `rollback_or_recovery`：失败时如何撤回、重试或交接

## 7. 未决问题

| 问题 | 影响 | 核实责任岗位 | 最迟处理时间 | 当前状态 |
|---|---|---|---|---|
|  |  |  |  | open |

## 8. 下一步

1.
2.

> 本文件只提供上下文结构。Stage 才是任务当前状态、认领、容量、授权和运行事件的权威来源。
