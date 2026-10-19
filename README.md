# ScoreBook

ScoreBook 是 OrchestraCorp 的 **Mind Repo**，用乐谱指代组织运行所依赖的规则、知识和正式产物。

[架构设计](architecture.md)说明[当前目录树与功能设计](architecture.md#三当前目录树与功能设计)、模板与企业实例、权威范围、权限分仓，以及 Maestro 和 Stage 的协作方式。

[参考公司手册](reference-company/operating-handbook/README.md)提供完整参考组织的手册入口；[参考公司骨架](reference-company/)包含默认部门、岗位和跨部门协作入口。

[仓库初始化、授权与持续演进设计](docs/repository-lifecycle-design.md)记录下一阶段能力：以企业自托管 GitLab 为首版，生成公司共享仓和按读者分离的部门/受限仓，支持权限核验、Git 协作、模板升级与知识演进。该方向已于 2026-10-19 确认；具体接口与实施细节继续细化，相关工具尚未实现。

当前产品模板由独立 Git 仓库管理，主分支为 `main`，`origin` 指向 GitHub 私有仓库 `OrchestraCorp/ScoreBook`；`reference-company/` 作为模板内容由本仓库管理，企业实例仍按 GitLab 多仓方案另行建仓。

## 产品仓与企业入口

```text
ScoreBook/                   产品模板仓
├── AGENT.md                 模板维护指令
├── AGENTS.md                模板维护兼容入口
├── README.md
├── architecture.md
├── docs/                    初始化、授权与演进设计
├── examples/                外部知识和模板参考
└── reference-company/       可独立复制的公司 Repo 骨架
    ├── AGENT.md             公司 Maestro 入口
    ├── AGENTS.md
    ├── operating-handbook/
    ├── governance/
    ├── organization/
    ├── agents/
    ├── knowledge/
    ├── decisions/
    ├── repositories/
    ├── archives/
    ├── departments/
    └── cross-functional/
```

企业取 `reference-company/` 内的完整内容建立自己的私有 Repo，以其中的 `AGENT.md` 为 Maestro 入口。产品仓根目录只用于维护模板，不作为企业运行上下文，也不随企业实例运行持续读取。

上述复制方式适用于当前内容采用。拟建初始化工具会按企业蓝图将同一内容源生成到多个独立仓库，并重写入口和引用；不会把所有部门原文先放进共享仓，再把搬目录视为权限隔离。

## 默认组织操作手册

ScoreBook 将提供一套有明确默认选择、可以直接审阅和采用的参考组织手册，企业从完整基线开始调整。它不只是一组空白表格，也不绑定某批人员或固定部门。

截至 2026-10-19，已保存[编写纲要](reference-company/operating-handbook/writing-plan.md)和 [11 章参考初稿](reference-company/operating-handbook/README.md)，并建立 10 个部门骨架、3 份岗位契约、6 份记录模板及 4 份虚构样例。内容仍需一致性审阅和企业适用性确认；章节主张和示例不自动成为任何企业的生效制度。

当前仓库内容是文档与 YAML 模板，尚无 schema 校验、自动实例化、发布或 Stage 同步程序。各目录已有内容、功能边界与待决问题见[架构设计](architecture.md)。

## 公司 Repo 保存什么

- 治理原则、权限与信息分类规则。
- 岗位契约、Agent 能力定义和协议 schema。
- 经确认的知识、SOP、Skill、案例和模板。
- 正式决策、变更历史和归档索引。
- 真实代码仓、连接器和交付物索引。

## 不作为公司 Repo 的实时事实源

- Stage 的高频任务、认领、运行队列和实时状态。
- Virtuoso 的私人会话或不可交接的个人记忆。
- 未经授权的个人信息、凭据、合同金额和财务原文。
- 具体公司的真实人员和业务记录，除非在实例化后的受限仓中维护。

ScoreBook 是长期事实与版本依据；它不是实时队列，也不自动决定制度何时生效。规则生效由 Stage 读取指定版本并记录。

根目录是产品模板和参考资料；真正给企业使用的 ScoreBook 应从 `reference-company/` 实例化，并按企业权限拆分仓库。不应把受限内容仅放进一个所有人可读取仓库中的 `locked/` 目录。
