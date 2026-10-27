<p align="center">
  <img src="assets/brand/scorebook.png" width="144" height="144" alt="ScoreBook logo">
</p>

# ScoreBook

English | [中文](README.zh.md)

**A score for enterprise collaboration: versioned organizational handbooks, role contracts, and formal knowledge.**

ScoreBook is OrchestraCorp's repository of organizational knowledge and governance templates (Mind Repo). It provides a reference company structure that teams can read, review, and adapt, keeping working rules, responsibilities, knowledge, and decisions in traceable Git history.

This project uses the [MIT License](LICENSE), which permits commercial use, modification, and redistribution. Companies can use these templates to maintain their own private knowledge repositories.

[Reference handbook](reference-company/operating-handbook/README.md) · [Getting started](#getting-started) · [Architecture](architecture.md) · [Planned development](docs/repository-lifecycle-design.md)

The reference handbook, templates, and supporting documentation are currently primarily in Chinese.

## The four OrchestraCorp modules

| Project | Responsibility |
| --- | --- |
| **[ScoreBook](https://github.com/OrchestraCorp/ScoreBook)** | Versioned organizational handbooks, role contracts, formal knowledge, and decisions. |
| [Stage](https://github.com/OrchestraCorp/Stage) | The enterprise backend for identity, assignments, permissions, and controlled business operations. |
| [Maestro](https://github.com/OrchestraCorp/Maestro) | The organizational collaboration and administration interface, supporting understanding, organization, proposals, and coordination under human supervision. |
| [Virtuoso](https://github.com/OrchestraCorp/Virtuoso) | The employee workspace, helping people and agents carry out specific work. |

These responsibilities describe the product direction. Automated publishing, loading, and acknowledgment between ScoreBook and Stage are not yet implemented. The documents and YAML templates are available to use now, without running an application service.

## What is included

| Content | Entry point and status |
| --- | --- |
| An 11-chapter operating handbook | The [reference handbook](reference-company/operating-handbook/README.md) covers organization, work, knowledge, decisions, people, customers, assets, and risk. It is currently an initial reference draft. |
| 10 department structures | The [department directory](reference-company/departments/) includes responsibilities, roles, collaboration interfaces, and knowledge entry points. |
| 3 role contracts | The [role contracts](reference-company/organization/role-contracts/) define responsibilities for cross-department work, knowledge maintenance, and internal services. |
| 6 record templates | The [template directory](reference-company/knowledge/templates/) covers work context, collaboration requests, handoffs, acceptance evidence, knowledge, and decisions. |
| 4 fictional examples | The [sample directory](reference-company/knowledge/samples/) illustrates collaboration, delivery, handoffs, and knowledge organization. |
| Governance and versioning structure | Templates and directories for [governance](reference-company/governance/), [organization](reference-company/organization/), [decisions](reference-company/decisions/), and [archives](reference-company/archives/). |

The content still needs consistency review and validation for each company's needs. Reference chapters and examples do not automatically become effective company policies. Schema validation, automated setup, template upgrade tools, and Stage synchronization remain to be built.

<a id="开始采用"></a>

## Getting started

1. **Read and select a baseline.** Start with the [reference company overview](reference-company/README.md) and [operating handbook](reference-company/operating-handbook/README.md). Record the ScoreBook Git commit you use, and identify the organizational rules and role responsibilities you need to adapt.
2. **Create your own private repository.** Copy the complete contents of `reference-company/` into a new private trial repository, preserving internal paths, `LICENSE`, `AGENT.md`, and `AGENTS.md`. The copied root `AGENT.md` is Maestro's entry point for the company instance. The outer product repository and `examples/` are not required to operate that instance.
3. **Establish responsibilities and access before adopting it.** Assign content owners and reviewers, classify information, and configure repository permissions for the intended readers before adding company data. Review which rules to adopt and how they take effect. For runtime configuration, separately verify Stage integration and what Stage actually loads.

Content intended for different audiences should live in separate repositories with appropriate access restrictions. Directory names and classification labels do not enforce permissions: a `locked/` directory in a repository everyone can read does not protect its contents.

The planned setup tool will initially target company-hosted GitLab. It is intended to create company-wide, departmental, and restricted repositories according to permissions, with authorization checks, upgrades, and knowledge evolution. See the [repository lifecycle design](docs/repository-lifecycle-design.md) for the proposed contracts and implementation status.

## Repository layout and authority boundaries

```text
ScoreBook/                   Open-source product template repository
├── README.md                English overview (default)
├── README.zh.md             Chinese overview
├── LICENSE                  MIT License
├── AGENT.md / AGENTS.md      Template maintenance instructions
├── architecture.md          Content structure and responsibilities
├── assets/brand/            Product logo
├── docs/                    Repository setup, authorization, and evolution designs
├── examples/                External references and source record formats
└── reference-company/       Standalone reference company structure
    ├── AGENT.md / AGENTS.md  Company instance entry point
    ├── LICENSE              Retain when copying the company structure
    ├── operating-handbook/  Organizational operating handbook
    ├── governance/          Governance, authorization, and classification templates
    ├── organization/        Organizational model, roles, and decision rights
    ├── departments/         Department responsibilities and interfaces
    ├── cross-functional/    Cross-department collaboration methods
    ├── knowledge/           Formal knowledge, record templates, and examples
    ├── agents/              Agent capability and registration templates
    ├── decisions/           Formal decisions
    ├── repositories/        System and repository indexes
    └── archives/            Historical archive indexes
```

ScoreBook stores long-lived, reviewable versions of rules and knowledge. Stage manages live tasks, assignments, permissions, and runtime state. Private employee conversations, credentials, and business source material without authorization to publish must not enter the public product templates.

People and Maestro may organize content, prepare changes, and review proposals within their authorization. Commits, approvals, merges, and runtime activation must be verified separately. A Git merge does not mean Stage has loaded the change, and it does not grant an agent additional execution permissions.

## Documentation and contributions

- [Architecture](architecture.md): directory purposes, content authority, repository separation by access level, and remaining gaps.
- [Repository lifecycle design](docs/repository-lifecycle-design.md): company setup, Git collaboration, template upgrades, and knowledge evolution.
- [Handbook writing plan](reference-company/operating-handbook/writing-plan.md): the scope and writing requirements of the reference handbook.
- [Template maintenance instructions](AGENT.md): requirements for sources, ownership, classification, versioning, and review.
- [External reference guide](examples/README.md): how to record sources and licenses.

Contributions through [Issues](https://github.com/OrchestraCorp/ScoreBook/issues) or pull requests are welcome: improve templates, correct documentation, or add reusable fictional examples. Before contributing company experience, remove real personal and customer information, credentials, and restricted material, and verify the rights and sources for your contribution.

## License

ScoreBook's product templates are licensed under [MIT](LICENSE). Copies of the templates or substantial portions must retain the copyright and license notices. When copying the full reference company, retain its [LICENSE](reference-company/LICENSE) as well.

Company instances and customizations may remain private. Adopting these templates does not require publishing company policies or business information. Rights to company-authored additions belong to their respective rights holders; external reference material remains subject to its stated license.
