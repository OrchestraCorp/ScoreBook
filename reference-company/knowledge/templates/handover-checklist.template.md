---
title: Role Handover Checklist Template
status: template
classification: internal
reference_type: reference-default
policy_effect: none
fictional: false
date: 2026-10-19
---

# 岗位/任务交接清单

用于人员缺席、岗位轮换、临时接管、离职交接或 Agent 更换。它描述交接所需信息，不代表任何人已经获得 Stage 权限。

## 使用说明

- **谁填写**：当前责任岗位或其授权 Agent 先填；接任岗位逐项核对并在 Stage 中确认接管。
- **何时用**：计划性离岗至少在交接窗口开始时建立；紧急接管先记录最低安全上下文，随后补齐。
- **证据要求**：每项使用 Stage 任务/承诺引用、Repo 版本、决定记录、业务系统对象或明确的缺失标记。
- **权限要求**：交接人只转移必要工作上下文；权限转移由 Stage 授权流程单独处理，不能用清单代替签署。
- **未决点**：未验证的事实必须列入风险和待办；接任人不能默认为同意所有承诺。

## 1. 交接范围

- `handover_id`：
- `subject_type`：role / task / service / agent
- `subject_id`：
- `from_role`：
- `to_role`：
- `effective_window`：
- `classification`：
- `stage_ref`：
- `prepared_at`：

## 2. 必须交接的事实

- 当前目标与验收标准：
- 已确认承诺、截止时间和优先级：
- 当前阻塞、依赖和风险：
- 最近一次核实时间：
- 当前生效的规则/策略版本：
- 关键外部联系或业务对象引用：

## 3. 产物和工作区

| 项目 | 位置/引用 | 版本 | 接任人已核对 |
|---|---|---|---|
|  |  |  | yes / no / blocked |

## 4. 权限与安全边界

- 接任岗位所需的最小数据范围：
- 需要新增、撤销或限时授权的动作：由 Stage 提交授权申请，不在此直接批准
- 凭据/密钥处理：不得写入本文；通过公司密钥系统轮换或撤销
- 需要通知的审计/安全岗位：

## 5. 待办与未决事项

| 事项 | 优先级 | 下一动作 | 责任岗位 | 截止 | 核实证据 |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## 6. 接管确认

- `handover_status`：draft / reviewed / accepted / blocked / superseded
- 交接人核对：
- 接任岗位核对：
- 责任岗位确认：
- Stage 接管事件引用：
- 未解决分歧：

> 接管完成的含义是上下文和责任边界被确认；它不自动改变组织任职、数据权限或审批权。
