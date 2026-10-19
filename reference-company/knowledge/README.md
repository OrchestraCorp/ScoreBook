# 参考公司知识目录

ScoreBook 只保存经过确认、可交接、可复用的组织知识：SOP、Skill、案例、检查表、决策原则和模板。这里的 `reference-company/` 是默认参考公司骨架；本目录内容用于说明推荐结构，默认 `policy_effect: none`，不能直接当作企业已生效政策。

## 权威边界

- **Stage**：当前任务、认领、承诺、容量、授权、运行事件、实际可见范围和生效回执的权威来源。
- **ScoreBook**：模板、静态示例、正式知识候选与已发布知识、来源、版本和历史引用。
- **Maestro**：在授权范围内整理、去重、补来源、提出知识变更和提交审阅；不自动批准或生效。
- **Virtuoso**：在岗位授权上下文中使用知识并提交复用反馈。

## 模板

`templates/` 里的模板都包含谁填写、何时使用、证据要求、权限边界和未决点：

- [任务上下文包](templates/task-context.template.md)：让获授权的员工或 Agent 接手任务。
- [岗位/任务交接清单](templates/handover-checklist.template.md)：缺席、轮换、临时接管和 Agent 更换。
- [知识条目](templates/knowledge-entry.template.md)：把可复用经验整理成可验证知识。
- [跨岗位协作请求](templates/collaboration-request.template.md)：请求输入、评审、执行、验收或解除阻塞。
- [协作结果验收证据](templates/acceptance-evidence.template.md)：逐条证明交付是否满足条件。
- [决策记录](templates/decision-record.template.md)：保存影响规则、资源、边界或长期记忆的决定。

## 虚构参考样例

`samples/` 里的文件均标记 `fictional: true`、`reference_type: fictional`、`policy_effect: none`、`date: 2026-10-19`。它们演示填法，不代表真实员工、客户、组织、承诺、授权或已生效政策：

- [跨岗位交付上下文](samples/cross-functional-delivery-context.sample.md)：客户入职试点的目标、依赖、风险、证据和未知项。
- [跨岗位协作请求](samples/cross-functional-collaboration-request.sample.md)：安全审阅请求的范围、最小数据边界和未形成承诺的状态。
- [知识沉淀样例](samples/knowledge-capture-support-triage.sample.md)：将模拟支持分流结果整理成待审阅 SOP。
- [岗位交接样例](samples/role-handover-internal-service.sample.md)：内部服务负责人缺席时的最小接管上下文和授权边界。

## 使用规则

每项知识应记录：来源任务或决定、适用范围、数据分类、责任岗位、版本、复核时间和验证方式。工作过程不自动成为知识；Maestro 可以提出整理，责任岗位或指定审阅人确认后发布。

知识条目中的引用是来源索引，不是访问授权。来自受限资料的摘要仍须遵守披露边界；不要在模板或样例中写入凭据、真实个人/客户数据、合同原文、薪酬或财务细节。
