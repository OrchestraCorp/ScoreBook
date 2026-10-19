---
title: Collaboration Request Template
status: template
classification: internal
reference_type: reference-default
policy_effect: none
fictional: false
date: 2026-10-19
---

# 跨岗位协作请求

用于岗位、员工 Agent 或公司 Agent 向责任岗位发起结构化请求。请求不是承诺；接收岗位在 Stage 中接受后才形成承诺。

## 使用说明

- **谁填写**：请求方岗位或其 Agent；请求方对目标和上下文负责。
- **何时用**：需要其他岗位输入、评审、交付、验收或解除阻塞时。
- **证据要求**：关联任务上下文包、目标版本、已有决定和所需产物。
- **权限要求**：只共享完成请求所需的最小信息；请求方不能借请求自动获得接收岗位权限。
- **未决点**：接收岗位可提出范围、期限、资源或风险问题；双方未确认前不写成承诺。

## 请求内容

- `request_id`：
- `task_id` / `task_version`：
- `requesting_role`：
- `receiving_role`：
- `request_type`：input / review / execution / acceptance / unblock
- `intent`：
- `requested_output`：
- `desired_by`：
- `priority_reason`：
- `shared_context_refs`：
- `classification`：

## 边界与响应

- `in_scope`：
- `out_of_scope`：
- `required_capability`：
- `data_or_tool_boundary`：
- `response_options`：accept / propose_change / decline / escalate
- `acceptance_criteria`：
- `idempotency_key`：

## 结果记录

- `stage_request_ref`：
- `accepted_commitment_ref`：
- `decline_or_change_reason`：
- `next_action`：
- `unknowns`：

> 临时跨岗执行仍需有权人员确认和电子签名；本请求模板不能替代授权记录。
