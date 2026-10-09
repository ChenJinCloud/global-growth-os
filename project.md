# 项目：Global Growth OS

> 状态：content-v0.1 已开放；runtime-v0.1 Manual Runtime 建设中\
> 更新：2026-10-09\
> 公开仓库：[ChenJinCloud/global-growth-os](https://github.com/ChenJinCloud/global-growth-os)；[飞书知识库](https://my.feishu.cn/wiki/Kg2qw1cJCiYOOMkPFVocqbZXn9f)

## 项目定位

Global Growth OS 是面向全球增长的领域基础设施。它把产品价值、战略、组织、信源、知识、数据、方法、工具、Agents、人类判断、运行状态和反馈组织成一套可被人和 Agents 共同使用、组合、验证和持续改进的增长系统。

本目录代表整个 Global Growth OS，而不是某一次活动、某一个知识库或某一组 Skills。活动、内容、工具和公开发布都是 OS 的组成部分或验证方式。

## 与 01-global-growth-system 的关系

- `01-global-growth-system` 是陈今全部全球化增长工作的私有领域工作区，还包含 InsForge、DeepWisdom、合作与活动等其他项目。
- `projects/global-growth-os/` 是 Global Growth OS 这一独立系统/产品方向的完整项目权威目录。
- 公司内部事实和执行资产仍留在对应公司项目与正式工作仓库，不因为被用于验证 OS 而自动进入 Public Core。

## 最小运行内核

```text
Product Value × Evidence Quality × Execution Capacity
                         ↓
Sense → Understand → Decide → Compose → Execute → Measure → Learn
                         ↓
Mission → Run → Artifact → Evaluation → Feedback
```

系统价值不以文档、内容或 Skill 数量衡量，而以真实 Growth Mission 是否能够获得正确上下文、组合合适能力、产生可用交付、保留证据并完成反馈回流衡量。

## 系统组成

1. **Operating Kernel**：产品价值、North Star、原则和边界。
2. **Domain Model**：Product、Demand、Goal、Strategy、Mission、Evidence、Capability、Run、Artifact、Feedback 等核心对象。
3. **Strategy & Organization**：阶段选择、优先级、Owner、资源和审批关系。
4. **Knowledge & Context**：信源、证据、知识、Context Pack 和 Memory。
5. **Capability Platform**：方法、Skills、Agents、工具、模板、人和服务的注册与组合。
6. **Runtime**：Mission 状态、工作流、人工检查点、运行记录和恢复机制。
7. **Evidence & Evaluation**：事实、交付、运行和业务结果评估。
8. **Public Core & Private Instance**：公开可复用的核心与具体团队的私有运行实例。

## 当前状态

### 已落盘

- [现行公开边界](public-core/decisions/2026-10-09-public-boundary-and-version-policy.md)：公开通用架构和经审核的可复用内容，团队运行实例保留私有；
- [版本与交付定义](public-core/VERSIONING.md)：content-v0.1 是知识内容首版，runtime-v0.1 尚未验收；
- [飞书资源索引](public-core/content-index.md)：关联公开入口与正文；
- 完整概念架构与 v0.1 边界；
- Public Core 的初始 GitHub 建设记录；
- AWW'26 Build in Public 与公测实验材料；
- Public Core、私有实例和公司机密之间的基本边界；
- 重复本地项目入口的合并与归档。

### 尚未完成

- 可操作的 Kernel、Strategy Card 和 Organization Card；
- Demand、Mission、Capability、Run、Artifact、Evaluation 的统一模板或注册表；
- 至少一个按完整对象和状态链运行、复盘并回流的真实 Mission；
- 本地私有项目、GitHub、chenjin.io 和飞书之间经过验证的发布与同步关系；
- runtime-v0.1 的正式验收和发布记录。

## 权威文件

- 项目当前状态与范围：本文件；
- 阶段和里程碑：[`ROADMAP.md`](ROADMAP.md)；
- 概念和架构：[`architecture/global-growth-os-concept-and-architecture-v0.1.md`](architecture/global-growth-os-concept-and-architecture-v0.1.md)；
- Public Core：[`public-core/README.md`](public-core/README.md)；
- 单次验证：`experiments/<experiment>/project.md`；
- 历史记录：`archive/` 与 `public-core/history/`。

## 当前实验

- [`AWW'26 首发与 9/24 公测`](experiments/aww26-launch/project.md)：通过真实需求采集、公开建造、现场使用和反馈，验证 OS v0.1 能否从问题走到可带走的 Artifact。

## 非目标

- 不把活动本身等同于 OS；
- 不把知识库、网站、GitHub、飞书或 Skill 单独称为 OS；
- 不为了显得完整而自建账户、向量数据库、多 Agent Runtime 或 Marketplace；
- 不将未经授权的公司内部事实、数据、策略和凭证放入公开 Core；
- 不把计划、历史报告或 Demo 写成已经验证的业务结果。

