---
title: Acceptance Evidence Template
status: template
classification: internal
reference_type: reference-default
policy_effect: none
fictional: false
date: 2026-10-19
---

# 协作结果验收证据

用于证明一次交付是否满足已确认的目标和验收条件。验收证据不等于主观“看起来完成”。

## 使用说明

- **谁填写**：交付岗位准备证据；独立验收岗位或责任岗位按既定标准核对。
- **何时用**：提交交付、申请关闭任务、变更影响范围或复核争议时。
- **证据要求**：引用可复核的文件版本、测试结果、业务对象、回执或观察记录；区分事实和解释。
- **权限要求**：只披露验收所需字段；敏感证据以受限引用表示。
- **未决点**：无法验证的条件必须标记 partial / blocked，不得默认通过。

## 交付身份

- `task_id`：
- `commitment_id`：
- `delivery_version`：
- `delivering_role`：
- `acceptance_role`：
- `stage_ref`：
- `submitted_at`：

## 条件核对

| 验收条件 | 证据引用 | 结果 | 核验人/岗位 | 核验时间 |
|---|---|---|---|---|
|  |  | pass / fail / partial / blocked |  |  |

## 质量与风险

- 已知偏差：
- 未完成事项：
- 安全/数据分类检查：
- 回滚或补救方案：
- 后续观察窗口：

## 结论

- `acceptance_result`：accepted / accepted_with_followup / rejected / blocked
- `decision_or_policy_ref`：
- `reason`：
- `follow_up_task_refs`：
- `dispute_or_appeal_path`：

> 任务关闭、奖励计量或知识发布使用哪一版本，必须由 Stage 记录并引用这份验收证据。
