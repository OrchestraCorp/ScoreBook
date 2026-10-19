---
title: Collaboration request — Northstar security review
status: reference-default-sample
classification: internal
reference_type: fictional
fictional: true
policy_effect: none
date: 2026-10-19
stage_state: illustrative_only
---

# 示例：跨岗位安全审阅请求

> 本例演示 `collaboration-request.template.md` 的填法。所有对象、岗位和时间均为虚构；请求不会自动授予权限，也不代表真实承诺。

## 请求内容

- `request_id`: `northstar-security-review-001`
- `task_id` / `task_version`: `northstar-onboarding-001 / v0.3`
- `requesting_role`: Customer Onboarding Lead
- `receiving_role`: Information Security Reviewer
- `request_type`: review
- `intent`: 核对模拟客户数据字段和外部共享链接是否满足试点边界。
- `requested_output`: 一份字段级分类结果、阻塞项和是否可进入模拟演练的结论。
- `desired_by`: `2026-10-24 12:00 Asia/Shanghai`（示例）
- `priority_reason`: 模拟演练必须先通过数据边界检查。
- `shared_context_refs`:
  - `stage://example/task/northstar-onboarding-001/context`
  - `repo://example/reference-company/knowledge/samples/northstar-onboarding-v1.md`
- `classification`: internal

## 边界与响应

- `in_scope`: 字段分类、链接权限、示例数据是否包含可识别个人信息。
- `out_of_scope`: 批准生产权限、修改合同、批准真实客户导入。
- `required_capability`: information-classification、security-review
- `data_or_tool_boundary`: 仅读取模拟数据字典和候选文档；不得读取真实客户空间。
- `response_options`: accept / propose_change / decline / escalate
- `acceptance_criteria`:
  1. 每个字段有分类或明确待核实标记。
  2. 所有外链有责任岗位和最小读权限说明。
  3. 未满足条件时给出补救动作。
- `idempotency_key`: `northstar-security-review-001-v03`

## 结果记录

- `stage_request_ref`: `stage://example/request/northstar-security-review-001`
- `accepted_commitment_ref`: 待 Stage 形成（本样例不虚构承诺）
- `decline_or_change_reason`: 未发生；如超出审阅范围，接收岗位应提出范围变更而非默默执行。
- `next_action`: 安全审阅岗位确认是否接受；若需临时跨岗执行，由有权人员另行签署。
- `unknowns`: 实例化企业的真实分类法和保留期限尚未配置。
