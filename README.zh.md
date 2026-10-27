<p align="center">
  <img src="assets/brand/scorebook.png" width="144" height="144" alt="ScoreBook logo">
</p>

# ScoreBook

[English](README.md) | 中文

**用版本化的组织手册、岗位契约与正式知识，为企业协作写好乐谱。**

ScoreBook 是 OrchestraCorp 的组织知识与治理模板仓（Mind Repo）。它提供一套可阅读、审阅和修改的参考公司骨架，帮助企业把工作规则、责任边界、知识和决策保存在可追溯的 Git 历史中。

本项目采用 [MIT 许可证](LICENSE)，允许商业使用、修改和再分发。企业可以基于模板维护自己的私有知识仓库。

[参考公司手册](reference-company/operating-handbook/README.md) · [开始采用](#开始采用) · [架构设计](architecture.md) · [后续建设](docs/repository-lifecycle-design.md)

## OrchestraCorp 四个模块

| 项目 | 分工 |
| --- | --- |
| **[ScoreBook](https://github.com/OrchestraCorp/ScoreBook)** | 组织手册、岗位契约、正式知识与决定的版本依据。 |
| [Stage](https://github.com/OrchestraCorp/Stage) | 企业后端，负责身份、任职、权限与受控业务操作。 |
| [Maestro](https://github.com/OrchestraCorp/Maestro) | 组织协作与管理入口，支持人员监督下的理解、整理、提案和协调。 |
| [Virtuoso](https://github.com/OrchestraCorp/Virtuoso) | 面向员工的工作入口，支持人员与 Agent 完成具体工作。 |

这些分工描述产品方向；ScoreBook 与 Stage 的自动发布、加载和回执链路尚未实现。当前可以直接采用的是文档与 YAML 模板，无需启动应用服务。

## 当前包含什么

| 内容 | 入口与状态 |
| --- | --- |
| 11 章组织操作手册 | [参考正文](reference-company/operating-handbook/README.md)，覆盖组织、工作、知识、决策、人员、客户、资产与风险等主题；当前为参考初稿。 |
| 10 个部门骨架 | [部门目录](reference-company/departments/)，包含职责、岗位、协作接口和知识入口。 |
| 3 份岗位契约 | [岗位契约](reference-company/organization/role-contracts/)，明确跨部门任务、知识维护和内部服务责任。 |
| 6 份记录模板 | [模板目录](reference-company/knowledge/templates/)，覆盖工作上下文、协作请求、交接、验收证据、知识和决定。 |
| 4 份虚构样例 | [样例目录](reference-company/knowledge/samples/)，演示协作、交付、交接和知识整理。 |
| 治理与版本管理骨架 | [治理](reference-company/governance/)、[组织](reference-company/organization/)、[决定](reference-company/decisions/)与[归档](reference-company/archives/)。 |

内容仍需一致性审阅和企业适用性确认。参考章节和样例不自动成为任何企业的生效制度。Schema 校验、自动实例化、模板升级工具及 Stage 同步程序仍待建设。

## 开始采用

1. **阅读并选择基线。** 从[参考公司入口](reference-company/README.md)和[组织操作手册](reference-company/operating-handbook/README.md)开始，记录所用的 ScoreBook Git 提交，确定需要调整的组织规则与岗位责任。
2. **建立自己的私有仓库。** 将 `reference-company/` 内的完整内容复制到新的私有试用仓，保留内部路径、`LICENSE`、`AGENT.md` 和 `AGENTS.md`。复制后的根 `AGENT.md` 是企业实例的 Maestro 入口；外层产品仓和 `examples/` 不属于企业运行必需内容。
3. **明确责任和权限后再采用。** 指定内容责任人、审阅人和信息分类，按实际读者设置仓库权限，再填入企业资料。通过审阅明确采用哪些规则及其生效方式；涉及运行配置时，另行核验 Stage 的接入和实际加载结果。

有不同读者范围的内容应拆到不同受限仓库。目录名称和分类标签不能代替权限：在全员可读的仓库里建立 `locked/` 目录，并不能保护其中的资料。

拟建初始化工具将优先支持企业自托管 GitLab，按权限生成公司共享、部门和受限仓库，并支持授权核验、升级和知识演进。具体合同与实施进度见[仓库生命周期设计](docs/repository-lifecycle-design.md)。

## 目录与权威边界

```text
ScoreBook/                   开源产品模板仓
├── README.md                英文介绍（默认）
├── README.zh.md             中文介绍
├── LICENSE                  MIT 许可证
├── AGENT.md / AGENTS.md     模板维护指令
├── architecture.md          内容结构与职责设计
├── assets/brand/            产品 Logo
├── docs/                    仓库初始化、授权与演进设计
├── examples/                外部参考入口与来源记录格式
└── reference-company/       可独立复制的参考公司骨架
    ├── AGENT.md / AGENTS.md 企业实例入口
    ├── LICENSE              独立复制时保留
    ├── operating-handbook/  组织操作手册
    ├── governance/          治理、授权与信息分类模板
    ├── organization/        组织模型、岗位与决策权
    ├── departments/         部门职责与接口
    ├── cross-functional/    跨部门协作方法
    ├── knowledge/           正式知识、记录模板与样例
    ├── agents/              Agent 能力与注册模板
    ├── decisions/           正式决定
    ├── repositories/        系统与仓库索引
    └── archives/            历史归档索引
```

ScoreBook 保存长期、可审阅的规则与知识版本。Stage 的实时任务、任职、权限和运行状态由 Stage 管理；员工私人会话、凭据以及未经授权的业务原文不应进入公开产品模板。

人员与 Maestro 可以按授权整理内容、准备变更和审阅提案。提交、批准、合并和运行生效分别核验；Git 合并不代表 Stage 已加载，也不授予 Agent 额外执行权限。

## 文档与贡献

- [架构设计](architecture.md)：目录功能、内容权威、权限分仓与后续缺口。
- [仓库生命周期设计](docs/repository-lifecycle-design.md)：企业初始化、Git 协作、模板升级与知识演进方向。
- [手册编写纲要](reference-company/operating-handbook/writing-plan.md)：参考手册的范围和编写要求。
- [模板维护指令](AGENT.md)：来源、责任、分类、版本和审阅约束。
- [外部参考说明](examples/README.md)：来源和许可的记录要求。

欢迎通过 [Issues](https://github.com/OrchestraCorp/ScoreBook/issues) 或 Pull Request 改进模板、修正文档和补充可复用的虚构样例。贡献企业经验前请去除真实人员、客户、凭据及受限资料，并确认所提供内容的授权和来源。

## 许可证

ScoreBook 产品模板采用 [MIT](LICENSE)。复制本模板或其实质部分时须保留版权及许可声明；完整复制参考公司时，应一并保留其 [LICENSE](reference-company/LICENSE)。

企业实例及其定制内容可以保持私有，采用模板不要求公开企业制度或业务资料。企业新增内容的权利由其权利人决定；外部参考材料仍遵守各自注明的许可证。
