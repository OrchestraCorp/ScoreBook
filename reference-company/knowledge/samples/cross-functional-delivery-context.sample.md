---
title: Cross-functional delivery context — Northstar onboarding pilot
status: reference-default-sample
classification: internal
reference_type: fictional
fictional: true
policy_effect: none
date: 2026-10-19
stage_state: illustrative_only
---

# 示例：Northstar 入职引导试点任务上下文包

> 本例完全虚构，仅演示跨岗位协作记录方式。`northstar-*` 引用是假设的 Stage/Repo 对象，不代表真实员工、客户、项目或已生效政策。

## 1. 身份与边界

- `task_id`: `northstar-onboarding-001`
- `task_version`: `v0.3`
- `title`: 为新客户类型设计 14 天入职引导试点
- `responsible_role`: Customer Onboarding Lead（客户入职负责人）
- `current_owner`: 由 Stage 在实例化后填写；本样例不指定个人
- `collaborating_roles`: Product Operations；Customer Success Enablement；Information Security Reviewer
- `classification`: internal
- `source_stage_ref`: `stage://example/task/northstar-onboarding-001`
- `prepared_at`: `2026-10-19`
- `prepared_by`: Customer Onboarding Lead Agent（虚构身份）

## 2. 目标与验收

- `intent`: 在不扩大客户数据访问范围的前提下，验证一套可重复的 14 天入职引导路径。
- `in_scope`:
  - 建立引导里程碑、客户可见检查清单和内部交接点。
  - 用脱敏的模拟客户记录跑一次端到端演练。
  - 记录阻塞、所需岗位输入和复盘结论。
- `out_of_scope`:
  - 不改变正式客户合同、计费规则或生产权限。
  - 不导入真实客户个人数据。
- `acceptance_criteria`:
  1. 每个里程碑有责任岗位、输入、输出和升级路径。
  2. 模拟演练可以由另一名获授权成员按文档复现。
  3. 安全审阅确认示例数据和工具权限边界清晰。
- `acceptance_authority`: Customer Onboarding Lead；Information Security Reviewer 对数据边界单独确认
- `deadline_and_timezone`: `2026-10-30 17:00 Asia/Shanghai`（示例）
- `version_change_rule`: 范围、客户数据分类、验收条件或对外承诺变化时回到 Stage 创建新版本。

## 3. 已确认事实

| 事实 | 来源 | 核实时间 | 可信状态 |
|---|---|---|---|
| 需要同时覆盖运营、客户成功和安全检查 | `decision://example/northstar-scope-v1` | 2026-10-19 | confirmed（虚构） |
| 演练使用脱敏模拟数据 | `stage://example/task/northstar-onboarding-001/context` | 2026-10-19 | confirmed（虚构） |
| 当前尚无生产客户数据授权 | `stage://example/access/northstar-001` | 2026-10-19 | reported; needs-check in real adoption |

## 4. 已作决定与依据

| 决定 | 决策引用 | 批准岗位 | 生效/适用版本 |
|---|---|---|---|
| 先做模拟演练，再申请真实客户试点 | `decision://example/northstar-simulation-first` | Reference Operations Sponsor（岗位） | sample-v1; policy_effect:none |

## 5. 承诺、依赖与风险

- `current_commitments`:
  - Product Operations：提交里程碑草案（示例承诺，须由 Stage 重新确认）。
  - Customer Success Enablement：准备客户可见语言和 FAQ 草案。
  - Information Security Reviewer：检查数据分类、外部链接和工具范围。
- `dependencies`:
  - 需要确认模拟数据字段清单；责任岗位：Information Security Reviewer。
  - 需要确认引导文档的对外文案；责任岗位：Customer Success Enablement。
- `risks`:
  - 若文档误带入真实客户字段，立即停止演练并撤回共享链接。
  - 若里程碑与合同承诺冲突，升级至 Legal/Commercial Owner，不自行修改合同解释。
- `resource_limits`: 仅使用示例 Stage 空间和受限测试仓；本条不授予任何真实权限。
- `stop_conditions`: 出现未分类个人数据、未经批准的对外承诺或无法追溯的交付版本时暂停。

## 6. 产物与证据

- `expected_artifacts`:
  - 14 天引导流程草案。
  - 模拟演练记录和验收证据。
  - 一份可复用的客户入职知识条目。
- `artifact_refs`:
  - `repo://example/reference-company/knowledge/samples/northstar-onboarding-v1.md`
  - `stage://example/acceptance/northstar-001`
- `verification_plan`: 由 Customer Onboarding Lead 按检查表复现；安全审阅人核对数据分类。
- `rollback_or_recovery`: 删除模拟数据、撤回未发布文档、保留审计引用；若交接未完成，转由责任岗位重新分派。

## 7. 未决问题

| 问题 | 影响 | 核实责任岗位 | 最迟处理时间 | 当前状态 |
|---|---|---|---|---|
| 真实企业是否已有同名流程 | 可能重复建设 | Product Operations | 2026-10-22 | open（虚构） |
| 哪些里程碑需要客户签字 | 影响验收与对外承诺 | Customer Success Enablement | 2026-10-24 | open（虚构） |

## 8. 下一步

1. 在 Stage 中确认各岗位的实际承诺和容量。
2. 完成模拟演练并填入 `acceptance-evidence.template.md`。
3. Maestro 从验收证据提取可复用步骤，提出知识条目 MR。
