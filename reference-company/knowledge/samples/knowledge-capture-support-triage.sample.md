---
title: Knowledge entry — support escalation triage pattern
status: reference-default-sample
classification: internal
reference_type: fictional
fictional: true
policy_effect: none
date: 2026-10-19
stage_state: illustrative_only
---

# 示例：支持升级分流方法

> 本例演示将跨岗位工作结果沉淀为知识。它不是企业政策、服务承诺或现实客户案例。

## 1. 元数据

- `knowledge_id`: `knowledge.example.support-triage.v1`
- `title`: 支持请求的三层升级分流
- `knowledge_type`: SOP
- `status`: draft（示例，未发布）
- `classification`: internal
- `owner_role`: Customer Support Operations Owner
- `reviewer_role`: Customer Success Lead
- `version`: `v1.0-example`
- `effective_from`: 不适用；`policy_effect:none`
- `review_due`: `2026-11-19`（示例）

## 2. 结论或方法

- `summary`: 先判断影响范围和可逆性，再将支持事项分为自助处理、责任岗位协作或需要经营者决策的事项。
- `when_to_use`: 新支持请求出现、已有承诺可能延期、或同类问题重复发生时。
- `when_not_to_use`: 需要即时安全止损、法律响应或真实客户合同解释时，直接走相应责任岗位的升级路径。
- `preconditions`: 有基本请求上下文、影响对象、来源和当前承诺引用。
- `steps`:
  1. 记录请求事实、来源和数据分类，不把猜测写成事实。
  2. 判断是否能在既有岗位权限、SOP 和承诺内完成。
  3. 若需其他岗位输入，创建结构化协作请求；未形成承诺前不对外承诺时限。
  4. 若可能影响安全、合同、付款或重大客户承诺，暂停并升级。
  5. 关闭后记录验收证据；重复出现的问题才进入知识整理候选。
- `expected_output`: 分流结果、责任岗位、下一个动作、证据引用和未知项。
- `failure_signals`: 无法确认责任岗位、请求包含未分类敏感信息、或同一事项被多个 Agent 重复处理。
- `escalation`: 先到对应责任岗位；跨岗冲突由任务主责协调；重大风险由指定经营/安全/法务岗位接管。

## 3. 来源与验证

| 来源类型 | 引用 | 说明 | 核实时间 |
|---|---|---|---|
| 示例任务 | `stage://example/task/support-triage-014` | 虚构的三次模拟请求汇总 | 2026-10-19 |
| 示例决定 | `decision://example/support-triage-simulation` | 仅说明采用模拟验证，不是生效政策 | 2026-10-19 |
| 示例交付 | `repo://example/reference-company/knowledge/samples/support-triage-runbook.md` | 虚构文档版本 | 2026-10-19 |

- `validation_method`: 用三条脱敏模拟请求逐条复现，检查是否能从请求到验收证据回溯。
- `validation_result`: partial（示例；仍需企业实例复核）
- `limitations`: 未覆盖行业监管、客户合同和多语言支持。

## 4. 披露与复用

- 可见范围：参考公司的内部知识维护岗位和支持相关岗位。
- 可被哪些岗位/Agent 检索：Customer Support Operations、Customer Success、Maestro；实例化后由 Stage 按策略过滤。
- 需要脱敏的字段：客户名称、联系方式、合同号、内部安全细节。
- 可否复制到外部材料：不可直接复制；需另行审阅。
- 复用反馈入口：`stage://example/knowledge-feedback/support-triage`

## 5. 未决问题和维护

- `unknowns`: 企业是否需要把法务、隐私或监管事件单独分流。
- `open_questions`: 响应时间和轮值如何由企业业务确定？
- `supersedes`: none
- `maintenance_trigger`: 规则、支持工具、数据分类或升级失败率发生变化时重新审阅。
