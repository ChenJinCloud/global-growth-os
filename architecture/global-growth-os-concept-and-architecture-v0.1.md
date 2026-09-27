# Global Growth OS：概念、系统架构与 v0.1 边界

> 状态：工作准源（Working Source of Truth）  
> 版本：v0.1  
> 日期：2026-09-11  
> 最后更新：2026-09-11（整合增长组织系统与中台化参考）  
> 适用范围：Global Growth OS 的长期概念、公开系统架构、个人网站定位与当前最小实现  
> 不代表：已经完成的产品、已经验证的商业模式、对外承诺或公司内部系统

## 0. 这份文档解决什么问题

这份文档完整记录陈今目前对 Global Growth OS 的核心想法，并将已经明确的个人意图、基于 Agent Infra 的系统设计建议，以及仍待验证的产品假设分开保存。

此前对 Growth OS 的描述容易滑向三个不准确的方向：把它理解成内容知识库，把 Skill 当成系统本体，或把陈今理解成需要亲自开发所有组件的人。本文修正这些偏差，并作为后续网站、GitHub 仓库、飞书知识库、公开活动和版本规划共同引用的概念准源。

文中使用三种状态：

- **已确认意图**：来自陈今在当前讨论中的明确表达。
- **架构建议**：根据 Agent、Agent Infra 和操作系统思想给出的当前设计，仍可迭代。
- **待验证假设**：需要通过真实使用、访谈、运行记录或商业结果验证，不能提前写成事实。

---

## 1. 一句话定义

### 已确认意图

**Global Growth OS 是面向全球增长的领域基础设施。它希望像 InsForge 和 Atoms 为产品与开发提供底层能力一样，把产品价值、战略、组织、数据、知识和可复用能力组织成一套可被人和 Agents 共同使用、组合、运行和持续改进的增长系统。**

它不要求陈今从零开发全部组件。系统应优先发现、筛选和复用全球已有的知识、方法、工具、服务与 Agent 能力；陈今负责判断、验证、组合、优化和维护，只在关键缺口没有合适方案时进行构建。

当前阶段不需要开发复杂产品。知识库与 Skills 足以成为 v0.1 的主要载体，但它们必须运行在一套完整的 OS 逻辑中，而不能被误认为 OS 的全部。

### 对外简版

> Global Growth OS 将产品目标、全球增长知识、信源、数据、方法、工具和真实经验，组织成可被团队与 Agents 共同运行、验证和持续改进的基础能力。

### 技术简版

> A composable operating layer for global growth, connecting product value, strategy, organization, context, capabilities, workflows, evidence and human judgment.

---

## 2. 为什么是 OS，而不只是知识库、工具箱或 Agent

知识库解决“系统知道什么”；Skill 解决“系统会做什么”；工具和服务解决“系统可以调用什么”；Agent 解决“谁能在一定授权下自主规划和行动”。OS 要解决的是更上层的问题：这些元素如何在统一的对象模型、状态、权限和反馈机制下共同运行。

因此：

| 元素 | 在 Global Growth OS 中的角色 | 为什么不是 OS 本身 |
|---|---|---|
| 知识库 | Context 与长期知识层 | 只有内容，没有任务状态、编排和执行闭环 |
| Skill | 可复用的能力包或标准操作单元 | 只是众多能力类型中的一种 |
| Prompt / Playbook | 指令、判断框架或流程模板 | 本身不知道何时调用、如何组合和怎样验收 |
| Tool / SaaS | 外部执行能力 | 不掌握完整目标、上下文和系统状态 |
| Agent | 可自主规划和调用能力的执行者 | 仍需要数据、工具、权限、运行时和评估环境 |
| 网站 | 公开入口与交互界面 | 不是系统的权威数据、运行时或全部状态 |
| GitHub | 版本、组件和开放协作界面 | 不等于实际业务运行 |
| 飞书知识库 | 低门槛查询、协作和反馈界面 | 不应成为唯一系统结构或权威边界 |

一个高质量 OS 必须同时具有“可以被使用的能力”和“让能力围绕正确目标可靠运行的控制结构”。Skills 属于能力层；产品价值、北极星、战略、组织、资源、领域模型、状态、编排、权限、评估和反馈共同构成更完整的系统。

---

## 3. Agent Infra 与增长组织系统的双重映射

以下不是要求立刻开发对应软件，而是用成熟 Agent 系统的组成方式检查 Global Growth OS 是否具备完整逻辑。

| 操作系统 / Agent Infra 概念 | Global Growth OS 对应要素 |
|---|---|
| Kernel | 产品价值、North Star、增长领域模型、基本规则和统一运行闭环 |
| Filesystem / Resources | 信源、知识、案例、证据、方法与历史产出 |
| Memory | 当前目标、用户背景、历史决策、实验状态与反馈 |
| Processes | 正在运行的市场研究、定位、Launch、渠道、内容、合作或复盘任务 |
| Applications | Skills、Playbooks、模板、Agents、工具和服务 |
| Scheduler / Orchestrator | 根据目标、阶段、优先级、成本和权限选择下一步与所需能力 |
| Drivers / Adapters | 与搜索、飞书、Notion、CRM、数据分析、广告和内容平台等系统的连接 |
| Permissions | 公开、个人私有、公司内部、可读取、可写入、可自动执行和需人工批准的边界 |
| Runtime State | 任务当前阶段、Owner、等待项、检查点、错误、恢复位置和下一步 |
| Artifacts | 研究简报、ICP、策略、计划、内容、名单、实验、看板和复盘等真实交付物 |
| Logs / Traces | 一次运行使用了什么来源、调用了什么能力、做出什么判断、发生什么失败 |
| Evaluation | 输出质量、事实准确性、过程效率、业务结果、反例和回归测试 |
| Interface | 个人网站、飞书知识库、GitHub，以及未来可能开放的 Agent 接口 |

Agent Infra 给 Global Growth OS 的关键启发不是“做一个 Agent”，而是：能力需要被发现，任务需要有生命周期，运行需要保存状态，输出需要成为可追踪的 Artifact，高风险行动需要人类控制，系统必须能够观察、评估、恢复和迭代。

### 3.1 从字节 UG 增长系统叙述中提取的架构参考

2026-09-11，陈今提供了一段关于字节 UG 增长系统的经验性叙述。本文将它作为系统设计参考，而不是对字节内部现状、历史成绩或行业比较的独立事实核查。值得吸收的是其中稳定的系统结构，而不是“行业第一”、大预算文化、对其他公司的评价，或 Push、红包、抖音头条互导等特定公司的具体能力清单。

这段材料可以抽象成六层：

| 原材料中的概念 | 可复用的系统抽象 | Global Growth OS 中的位置 |
|---|---|---|
| OKR、结果导向、高目标、长期主义 | Operating Kernel | 产品价值、北极星、目标原则、决策标准与长期边界 |
| 跨部门协作、增长人才培养、预算授权 | Organization & Governance | 角色、Owner、决策权、资源、审批、协作和能力培养 |
| 增长 BP 深入产品，多周期策略 | Strategy Control Plane | 阶段判断、战略组合、优先级、资源配置和时间尺度 |
| 数据基建、指标、AB、监控、ROI | Evidence & Evaluation Plane | 数据源、指标树、实验、归因、监控和效果评估 |
| Push、裂变、Affiliate、SEO、投放等中台能力 | Capability Platform | 可注册、组合、替换和复用的知识、Skills、工具、Agents、人和服务 |
| 产品价值 × 数据反馈 × 组织执行 | Runtime Loop | 从价值假设到行动、反馈、决策和持续迭代的运行闭环 |

这个抽象补充了单纯 Agent Infra 视角容易忽略的部分：增长不是只靠模型、工具和 Runtime 运行的技术任务，它还是一个组织系统。产品价值、战略选择、Owner、预算、跨职能协作和长期责任必须进入架构，不能留在 OS 外部作为默认前提。

### 3.2 增长系统的最小内核

Global Growth OS 不应把自动化程度当成增长质量本身。它的最小内核可以表达为：

```text
Product Value × Evidence Quality × Execution Capacity
= Sustainable Growth
```

- **Product Value**：产品是否为特定用户创造了真实价值，实际体验是否支持增长承诺。
- **Evidence Quality**：系统能否及时、准确地看到用户行为、业务结果、因果边界和反例。
- **Execution Capacity**：组织中的人、Agents、工具、预算和协作机制能否持续把判断变成行动。

AI 可以提升研究、分析、编排和执行效率，但不能替代产品价值，也不能把只有新增、没有留存的短期波峰自动解释为可持续增长。

---

## 4. 核心目标与非目标

### 核心目标

Global Growth OS 希望降低人和 Agents 完成高质量全球增长工作的重复成本，使他们不必每次从零搜索、理解、判断、选择工具和重建流程。系统最终应支持以下闭环：

```text
Sense      获取市场、用户、竞品、渠道和业务信号
  ↓
Understand 将新信号与已有知识、上下文和历史状态连接
  ↓
Decide     明确目标、约束、优先级、假设和验收标准
  ↓
Compose    选择并组合知识、Skills、Agents、工具、服务和人
  ↓
Execute    运行任务并生成真实交付物
  ↓
Measure    记录质量、效率、业务指标、人工修改和失败
  ↓
Learn      更新知识、状态、选择规则、能力组件和系统版本
```

### 当前非目标

- 不从零发明一套封闭的全球增长方法论。
- 不要求所有知识、工具、Skill 或 Agent 都由陈今原创。
- 不把“开发了多少工具”作为系统价值的主要证明。
- 不在 v0.1 开发复杂 SaaS、Agent 平台、工作流编辑器、账号系统或 Skill 商店。
- 不把公司内部数据、策略、凭证和执行资产直接公开。
- 不承诺 Agent 可以替代所有增长判断、关系工作和最终责任。
- 不把内容发布量、知识条目数或 Skill 数量等同于系统已经有效。

---

## 5. 设计原则

### 5.1 复用优先，构建补缺

默认顺序是：发现现有方案、检查来源与适用条件、真实测试、适配组合、持续优化，最后才是自主构建。构建的理由应是存在明确且重复的能力缺口，而不是为了证明原创或技术能力。

### 5.2 从 1 到 10，而不是重复从 0 到 1

Global Growth OS 的主要价值在于提高已有知识和能力的可发现性、可组合性、可靠性和复用率。它可以收录从 0 到 1 的入门支持，但系统自身的资源配置应优先投入到验证、整合、标准化和规模化复用。

### 5.3 增长与开发是两种纵深能力，不是两个互斥赛道

Coding 不是 Global Growth OS 唯一服务的行业。陈今同时深入增长与开发，是为了既理解增长问题，也理解如何通过数据、软件、AI Coding、Agents 和自动化把方案落地。开发能力是系统构建与连接能力，不能被误写成“只服务 Coding Agents 产品”。

### 5.4 真实任务优先于内容分类

系统的基本入口应是一个真实 Growth Mission，而不是一篇文章、一个工具或一个 Skill。知识和能力只有在真实目标、上下文、约束和验收标准中被组合运行，才能证明价值。

### 5.5 人类判断是一等组件

全球增长包含定位、创意、关系、品牌、风险和资源选择，不能把人工判断视为临时补丁。系统必须明确哪些步骤可以自动化、哪些需要人工审核、哪些必须由人负责，以及人与 Agent 如何交接。

### 5.6 来源、边界和失败必须可见

每个重要结论和能力都应尽可能说明来源、更新时间、适用场景、验证状态和失效条件。Growth OS 当前提出的“真卡点、真跑通、真交付、真边界”可以继续作为公开质量原则。

### 5.7 逻辑完整，产品克制

v0.1 可以由 Markdown、GitHub、飞书、现有 SaaS 和人工编排运行，但不能缺少对象、状态、输入输出、权限、评估和回流的定义。当前可以没有自动化 Runtime，但不能没有 Runtime 逻辑。

### 5.8 Public Core 与 Private Instance 分离

公开系统只包含经过审核、可复用、可公开的领域结构、知识、能力、案例和测试结果。个人私密信息、公司专属事实、凭证、未公开策略、客户状态和真实执行权限留在私有实例。公开 Core 可以被不同用户或团队实例化，但不反向吸收未经授权的私有事实。

### 5.9 产品价值先于增长动作

增长系统必须连接产品本身，而不能退化成市场传播和渠道执行系统。每个重要 Mission 都应说明产品当前为谁解决什么问题、价值是否已经得到什么程度的验证，以及增长动作是在放大真实价值、验证价值，还是试图用传播替代尚未成立的产品体验。

### 5.10 组织与资源是一等系统组件

高质量增长依赖明确的 Owner、决策权、跨职能协作、预算和执行节奏。Global Growth OS 不能假设“给出正确建议后组织自然会执行”，而应记录谁负责、谁批准、谁提供数据、谁承担风险、资源是否可用，以及任务被阻塞时如何升级和恢复。

### 5.11 系统吸收复杂度，用户先得到价值

完整架构用于让系统可靠，不用于要求用户先理解系统。任何公开入口都应从用户正在完成的工作出发，用最多三步让用户看到第一个有用结果，再按需展开来源、能力、运行和治理细节。若一个概念只对维护者有用，就留在后台；若一个页面不能推动用户更快得到结果，就不应占据主路径。

---

## 6. Global Growth OS 的系统层级

### 6.1 Operating Kernel：产品价值、北极星与原则

Kernel 定义系统为什么运行、什么结果值得追求，以及增长活动不能突破什么边界。它至少包括：

- 产品为谁创造什么价值；
- 当前产品与市场阶段；
- 北极星指标与约束指标；
- 短期效率与长期价值冲突时的选择原则；
- 对用户、品牌、数据、隐私和渠道实践的底线；
- 事实、推断、假设和宣传表达的证据标准。

文化在这里不作为口号集合，而作为可以影响决策的运行原则。例如“数据结果导向”只有在它能改变指标定义、实验门槛和停止条件时，才是 OS 的一部分。

### 6.2 Domain Model：领域模型

领域模型定义系统认识什么，以及不同对象如何发生关系。建议的首批核心对象如下；这是架构建议，不代表字段已经定稿。

| 对象 | 作用 |
|---|---|
| Actor | 人、团队、Agent、服务商或合作方 |
| Product | 被增长的产品及其阶段、价值主张和约束 |
| Market | 国家、区域、语言、行业或细分市场 |
| Segment / ICP | 目标用户、买家、使用者及筛选条件 |
| Problem / Demand | 来自用户、团队或市场、尚待澄清和排序的真实增长问题 |
| Source | 信息从哪里获得 |
| Signal | 新出现的市场、用户、竞品、渠道或业务变化 |
| Evidence | 支持或反驳判断的可追踪材料 |
| Goal / Metric | 想实现的结果、基线和衡量方式 |
| Strategy | 在特定周期、约束和证据下选择的增长方向与打法组合 |
| Portfolio | 多个 Strategy、Mission 和 Experiment 的优先级、资源与依赖关系 |
| Hypothesis | 尚未得到充分验证的判断 |
| Decision | 在特定证据和约束下做出的选择 |
| Channel | 内容、社区、搜索、广告、合作等分发与获客路径 |
| Experiment | 验证某个假设的有边界行动 |
| Mission | 一次具有目标、上下文、状态和验收标准的增长任务 |
| Capability | Skill、方法、工具、Agent、人或服务所提供的能力 |
| Run | 某个 Mission 的一次实际运行 |
| Artifact | 运行产生的可检查交付物 |
| Feedback | 对输出、过程和业务结果的评价、修改或反例 |

核心关系示例：一个 Mission 服务于某个 Product 和 Goal；引用一组 Evidence；选择若干 Capabilities；产生一个或多个 Artifacts；运行结果形成 Feedback；Feedback 再更新 Hypothesis、Decision、Capability 或知识状态。

### 6.3 Strategy Control Plane：战略与组合管理

Strategy Control Plane 位于单个 Mission 之上，负责将产品价值、长期目标和当前证据转换为阶段性选择。它需要回答：在哪个市场和用户上竞争、当前最重要的问题是什么、哪些增长路径值得投入、不同 Mission 如何排序、资源如何分配，以及何时继续、扩大、暂停或停止。

建议同时保留三个时间尺度，但不要求每个项目都机械填写：

- **近期运行周期**：未来数周或一个实验周期要验证什么。
- **阶段策略周期**：未来一个季度或当前产品阶段要建立什么能力和结果。
- **长期方向周期**：未来一年及以上希望积累什么市场位置、数据、品牌、渠道和系统能力。

Strategy Portfolio 管理多个 Mission 之间的关系：共同服务哪个 North Star，各自消耗多少预算和注意力，有什么依赖、冲突和机会成本。它避免系统把每个真实问题都自动升级成任务，也避免局部优化偏离产品长期价值。

```text
Product Value + North Star
          ↓
Strategy Portfolio
          ↓
Growth Missions and Experiments
          ↓
Runs, Artifacts and Evidence
```

### 6.4 Organization Operating Model：组织与协作

Global Growth OS 是社会—技术系统。组织层至少需要表达：

- 谁是业务一号位和最终结果责任人；
- Product、Growth、Content、Sales、Data、Engineering 等角色如何协作；
- 哪些决策由单一 Owner 做出，哪些需要跨职能确认；
- 人、Agent、工具和外部服务商分别承担什么；
- 预算、时间、数据权限和执行资源由谁提供；
- 哪些能力应在组织内长期培养，哪些适合外部采购或临时组合；
- 阻塞、分歧、风险和失败如何被发现、升级、恢复和复盘。

Public Core 可以提供角色模板、协作协议、决策记录和任务契约，但不能替具体团队决定组织结构。每个 Team Instance 必须带入自己的 Owner、资源、权限和责任链。

### 6.5 Source、Knowledge、Context 与 Memory

这一层不仅保存文章和资料，还要让人和 Agent 判断信息是否可信、是否新鲜、是否适用于当前问题。重要内容至少需要记录来源、作者或机构、获取时间、覆盖范围、事实/观点/推断类型、适用场景、访问权限和被哪些判断引用。

四者应区分：

- **Source** 是原始来源或可追踪入口。
- **Knowledge** 是经过结构化、去重、关联和边界说明的可复用认知。
- **Context** 是为某个 Mission 临时选择的相关信息组合。
- **Memory** 是跨一次或多次运行需要保留的状态、决策、反馈和历史。

每个 Team Instance 还需要一份可复用的 **Growth Context Pack**，避免每个 Skill、Agent 或服务重复询问背景。它至少应覆盖：产品及阶段、用户与买家、市场和语言、价值主张、竞品、品牌约束、当前目标与指标、已有渠道与资产、数据入口、预算和人力、权限、已知事实、关键假设、历史决策与当前阻塞。Mission Context 是从 Team Context Pack、公共知识和本次任务材料中按需组装出的最小上下文，不应把整个知识库无差别塞给模型。

### 6.6 Capability Platform：能力中台与注册表

Skill 只是 Capability Registry 中的一种能力。注册表还应容纳：

- 数据源和搜索能力；
- 方法、标准和 Playbook；
- Skills、Prompts 和工作流；
- 模型与 Agents；
- SaaS、API、CLI、MCP 或其他工具；
- 人类专家、执行者、服务商和合作网络；
- 可复用模板、数据结构与评估器。

每项能力应逐步具备统一描述：能力 ID、版本、Owner、解决的问题、触发条件、所需 Context、输入与输出契约、安装或调用方式、兼容的人和 Agent 客户端、前置条件、依赖、成本、权限与执行风险、人工判断点、来源、最近验证时间、评估方法、适用范围、失败条件和替代方案。

能力的“来源”和“成熟度”不应混成一个标签：

| 维度 | 建议状态 |
|---|---|
| 来源 | External / Adapted / Original |
| 成熟度 | Discovered / Reviewed / Tested / Operational / Deprecated |

外部能力完全可能比原创能力更成熟；原创也不等于已经验证。

能力中台化的价值不在于拥有一张越来越长的工具清单，而在于通用能力可以被不同 Strategy 和 Mission 重复使用、替换和组合。SEO、内容、广告、Affiliate、Referral、Influencer、用户分群、归因和实验等都是可能的能力域，不是每个 Global Growth OS 实例都必须具备的固定模块。

### 6.7 Mission、Workflow 与 Orchestration

OS 的主要运行单元建议定义为 **Growth Mission**。它代表一个有目标、有上下文、有状态、会产生交付物的真实增长任务，而不是一条内容或一次无边界对话。

一个 Mission 至少需要：

- 问题与期望结果；
- Product、Market、ICP 等必要上下文；
- 当前基线、约束、Owner 和截止时间；
- 事实、假设与未知项；
- 成功标准和所需证据；
- 被选中的知识与能力；
- 工作步骤、依赖和人工检查点；
- 当前状态、等待项和恢复位置；
- 最终 Artifacts；
- 运行后反馈和复盘。

建议的最小状态链：

```text
Captured → Qualified → Context Ready → Planned → Running
→ Waiting / Human Review → Completed / Failed / Stopped
→ Evaluated → Harvested
```

编排可以先由陈今或参与者人工完成。未来只有在同一种选择和路由反复发生时，才值得把它自动化成 Orchestrator。

### 6.8 Runtime、State 与 Artifact

Runtime 负责让 Mission 从输入走到结果。高质量运行不只是“Agent 给出一段答案”，而是能保存任务状态、处理等待与失败、允许人工介入、从检查点恢复，并产出明确 Artifact。

Artifact 是系统的真实价值载体，例如：带信源的市场简报、ICP 假设、渠道优先级、Launch 计划、内容资产、合作名单、实验方案、数据看板或复盘。对话文本可以是过程，但不应默认被视为最终交付。

### 6.9 Governance：权限、责任与边界

每一类资源和行动至少要回答：谁可以看、谁可以修改、谁可以执行、谁对结果负责、是否需要审批、能否公开、能否被模型提供商处理、能否进入训练或评估材料。

建议的最低数据边界：

- **Public**：允许公开和复用的知识、组件、案例与结果。
- **Private Personal**：个人上下文、未公开判断、关系和本地状态。
- **Company Confidential**：公司数据、策略、凭证、客户和内部执行资产。
- **Restricted Action**：涉及发布、付款、授权、删除、外联或生产写入的行动。

InsForge 可以作为陈今真实实践和能力证明，但 InsForge 内部数据不进入公开 Global Growth OS。

### 6.10 Evidence Plane：数据、实验、监控与评估

Evidence Plane 让增长从模糊经验变成可观察、可质疑、可迭代的实践。每次重要 Run 应逐步留下可审计记录：输入、来源、选用能力、关键判断、人工修改、耗时与成本、输出、错误、业务结果和后续反馈。

每个重要 Mission 至少应说明：想改变什么、当前基线是什么、数据从哪里获得、多久检查一次、什么结果意味着成功、什么情况下停止，以及哪些变化不能合理归因于本次行动。AB 测试、监控和 ROI 是这一原则在不同成熟阶段的具体实现，不要求所有 v0.1 Mission 都具备企业级数据设施。

评估至少包含四类：

- **事实质量**：来源是否可靠，结论是否有证据，是否过期或越界。
- **交付质量**：Artifact 是否完整、可读、可执行、符合格式要求。
- **运行质量**：耗时、人工步骤、返工、失败与恢复能力。
- **业务质量**：是否改善真实增长结果；若无法归因，应明确只验证过程价值。

失败案例、反例和人工修改应成为系统资产。系统是否能从运行中变得更可靠，比一次 Demo 是否流畅更重要。

### 6.11 Learning、Feedback 与 Contribution

活动和社区不是独立于 OS 的内容运营层，而是系统的输入、测试和学习机制。参与者带来真实问题、语言、约束、反例和结果；系统返回知识、能力组合和 Artifact；双方共同判断哪些内容应进入下一版本。

贡献不只包括提交 Skill，也可以是：新增信源、修正事实、补充适用边界、提供失败案例、验证一个工作流、贡献模板、提出新 Mission 或报告业务结果。

跨场景学习不能把单次成功直接升级为“最佳实践”。进入 Public Core 的案例应尽可能保留产品阶段、市场、用户、资源、指标、外部变量、适用条件和不可复制部分。只有经过抽象、边界说明和再次验证的内容，才逐步升级为更稳定的 Pattern、Playbook 或 Capability。

### 6.12 Public Core 与 Team Instance

字节式内部增长系统可以直接控制产品、组织、预算、数据和执行，而公开的 Global Growth OS 无法也不应替每家公司控制这些资源。因此完整系统需要区分公共内核与具体实例。

**Public Core** 由陈今与贡献者公开维护，可能包括：领域模型、运行原则、公开信源与知识、Strategy 和 Mission 契约、Capability Registry、Skills、Playbooks、评估标准、案例边界、贡献和版本规则。

**Team Instance** 由具体团队提供，包含：产品价值、North Star、真实 ICP、内部数据、组织角色、决策权、预算、当前策略、任务状态、凭证、权限和业务结果。

```text
Global Growth OS Public Core
        +
Company / Team Context
        +
Data, People, Resources and Permissions
        =
A Running Growth System Instance
```

这使 Global Growth OS 更接近 Infra：它不替每家公司经营业务，而是提供可以被实例化的结构和通用能力。私有实例的经验只有经过授权、脱敏、抽象、边界检查和重新验证后，才能回流 Public Core。

### 6.13 Demand Intake：需求进入与优先级

“反馈入口”还不够。高质量 OS 需要把外部提问、团队卡点、市场信号和执行阻塞变成一组可管理的 Demand，而不是直接变成文章或 Skill。每条 Demand 至少应记录提出者角色、原始表达、目标结果、频率、紧迫度、影响范围、当前替代方案、愿意投入的资源、所需证据和是否适合公开。

Demand 需要经过 Captured → Clarified → Qualified → Prioritized → Routed 的最小流程，再决定它进入一次 Mission、一个 Deep Dive、一个现有能力、一项新能力建设，还是暂不处理。这样，需求征集表单才是 OS 的 intake，而不只是活动报名表。

### 6.14 Knowledge Lifecycle：从信号到可复用能力

Web.Cafe 展示了“群聊材料—每日整理—经验—教程—问答—产品”的内容加工链。Global Growth OS 需要把它进一步升级为有证据门槛的知识与能力生命周期：

```text
Signal / Raw Input
→ Source Record
→ Claim + Evidence
→ Insight
→ Pattern / Playbook
→ Capability
→ Mission Run
→ Case + Evaluation
→ Revision / Deprecation
```

不是每条素材都应进入下一阶段。编辑选择、去重、适用边界、事实核验、真实运行和版本复审共同决定它能否升级。对话精华、短经验和长教程可以是不同阅读视图，但不能替代背后的来源、证据和版本关系。

### 6.15 Discovery、Packaging 与 Routing

系统需要同时支持三种发现路径：按“我需要完成什么”从 Mission / Problem 进入；按“系统有什么能力”从 Capability 进入；按“最近出现了什么变化”从 Signal / Update 进入。标签、分类、搜索、精选、最新和相关内容是发现界面，不是领域模型本身。

能力数量增加后，统一包装比目录数量更重要。一个可被复用的能力包应让人和 Agent 看懂它何时触发、需要什么上下文、会产出什么、如何安装或调用、兼容哪些客户端、是否会执行外部动作、如何验证、何时不适用。路由优先依据任务适配、证据、成本、风险和当前 Context，而不是热度或是否原创。

### 6.16 Trust、Proof 与 Reputation

公开系统需要区分两类信任：一类是 **Editorial Trust**，表示内容或能力经过来源检查、人工评审和适用边界说明；另一类是 **Field Proof**，表示它在具体 Team Instance 和 Mission 中被真实运行，并留下结果、失败、人工修改和评价。浏览量、点赞、收藏和作者声誉可以辅助发现，但不能代替有效性证据。

每个 Case 应尽可能回链到 Mission、Context 摘要、使用的能力、Artifact、指标和限制；每个能力则应显示来源、Owner、版本、验证状态、最后复审时间和已知失败。贡献者声誉应建立在可追踪贡献与验证上，而不是只建立在发帖数量上。

### 6.17 Adoption、First Run 与 Handoff

Alignify 的“先一起跑第一圈，再交给团队”揭示了知识库与真实采用之间常被忽略的实施层。Global Growth OS 不应假设用户读完 Playbook 或安装 Skill 就会形成运行系统，而应提供最小采用链：

```text
Diagnose
→ Configure Growth Context Pack
→ Select One Mission
→ Run Together
→ Review Evidence
→ Hand Off Ownership
→ Recurring Check-in / Re-entry
```

这一层可以由陈今、合作伙伴、社区贡献者或未来的 Agent 承担。其目标不是永久代运营，而是帮助团队完成首轮实例化、学会判断和接管运行。是否采用咨询、固定范围项目、工作坊或自助模板是商业模式选择，不改变该系统职责。

---

## 7. 现有四层内容如何进入完整 OS

当前公开介绍中的“岗位与常识、Deep Dive 与信源、Growth Toolkit、活动与反馈”可以保留，但它们应被理解为 OS 的公开内容视图，而不是完整系统架构。

| 现有层 | 在完整 OS 中的位置 |
|---|---|
| 岗位与常识 | 人类用户的 Onboarding 与基础 Knowledge |
| Deep Dive 方法论与信源 | Source、Evidence、Knowledge 与 Context |
| Growth Toolkit | Capability Registry 的公开部分，包括 Skills、Playbooks、工具和模板 |
| 活动与反馈 | Mission 获取、真实测试、Evaluation、Feedback 与 Contribution |

这四层之外，OS 还需要产品价值与 North Star、Strategy Portfolio、组织与资源、领域模型、任务状态、能力选择、编排逻辑、输入输出契约、权限边界、运行记录和评估机制。它们可以暂时不做成软件功能，但必须在内容结构和运行方式中存在。

---

## 8. v0.1：不用复杂产品也能成立的最小实现

### 8.1 v0.1 的目标

v0.1 不证明 Global Growth OS 已经完整，也不证明商业模式成立。它只需要证明：一个真实增长问题能够进入系统，系统能调取相关上下文，组合已有与自建能力，产生可用 Artifact，保留运行证据，并让反馈进入下一版本。

### 8.2 v0.1 的必要组成

1. **最小 Kernel**：记录产品价值、目标用户、North Star、约束指标和运行原则。
2. **最小领域模型**：先定义 Product、Problem / Demand、Goal、Strategy、Mission、Source、Evidence、Capability、Run、Artifact 和 Feedback 等核心对象。
3. **Strategy Card**：说明当前阶段最重要的问题、策略选择、时间尺度和 Mission 优先级；不急于建设复杂 Portfolio 软件。
4. **Organization Card**：记录 Owner、协作者、决策权、人工审批点、预算和关键资源。
5. **结构化知识库**：内容带来源、日期、适用范围、证据类型和引用关系。
6. **能力注册表**：不仅登记 Skills，也登记外部工具、方法、Agents、模板、人和服务。
7. **Mission 模板**：统一记录目标、上下文、约束、Owner、成功标准和当前状态。
8. **人工编排流程**：由人根据 Strategy 和 Mission 选择知识与能力，不急于开发自动路由。
9. **Run Log**：记录一次任务实际如何运行、哪里失败、哪里人工修改。
10. **Artifact 与评估**：输出必须可检查，并至少经过一次人类评价或真实使用。
11. **反馈入口**：让问题、反例、结果和贡献能够进入后续版本。
12. **公开与私有边界**：所有公开资产先经过来源、隐私和公司边界检查。

### 8.3 三个公开载体的分工

| 载体 | v0.1 职责 | 不承担什么 |
|---|---|---|
| chenjin.io | 解释系统、按问题导航、展示 Mission、能力、案例、版本与参与入口 | 不承担完整 Runtime 或全部知识存储 |
| GitHub | 公开 Core、版本、Skills、结构化组件、Issue 和贡献记录 | 不保存私密业务状态和凭证 |
| 飞书知识库 | 阅读、提问、协作、活动使用和低门槛反馈 | 不单独定义系统架构和权威边界 |

私有的 `/Users/jinchen/01-global-growth-system/projects/global-growth-os` 是整个 Global Growth OS 的本地项目权威目录；`01-global-growth-system` 仍是包含公司项目、合作和活动在内的更大增长领域工作区。公开 Global Growth OS 是从私有项目中经过审核和脱敏形成的 Public Core，不应把整个私有目录直接发布。

### 8.4 v0.1 暂不建设

- 自建登录和账户体系；
- 自建向量数据库或通用 RAG 平台；
- 可视化工作流编辑器；
- 自建多 Agent Runtime；
- Skill Marketplace；
- 全自动任务路由和长期自治；
- 为追求完整而批量生产未经真实需求验证的 Skills；
- 将活动、内容、社区、咨询和软件同时扩张成多个产品线。

如果现有工具已经能承担存储、检索、执行或协作，就先使用现有工具。只有重复运行暴露出稳定瓶颈后，才评估是否开发专用产品。

### 8.5 参考产品补全后的实现优先级

参考 Web.Cafe 与 Alignify 后，v0.1 对用户可见的部分只保留三件事：

1. **说出问题**：用户用自己的语言描述一个正在面对的全球增长问题。
2. **得到 First Move**：系统返回一个可以立即判断和执行的下一步，而不是先要求用户学习整套 OS。
3. **拿走结果**：用户获得一个可使用的 Artifact，并知道下一步可以自己运行、与陈今一起运行，或进入相关案例与资源。

内部仍可使用 Growth Context Pack、Demand Registry、Knowledge Promotion Rules、Capability Package Card 和 First-run / Handoff Template，但这些是系统实现，不是首页需要教育用户的概念。

积分、付费问答、会员、广告竞价、产品商店、贡献者排行榜和 Skill Marketplace 都不属于 v0.1。先证明“一个真实问题能够迅速得到有用结果”，再讨论供需、激励和交易机制。

---

## 9. 个人网站：把完整 OS 隐藏在一条极简路径后面

### 9.1 网站只有一个用户任务

chenjin.io 的首页不负责向用户解释完整的 Global Growth OS。它只负责一件事：**把访客正在面对的一个全球增长问题，变成一个可信、可执行的 First Move。**

用户不需要先理解 Kernel、Context、Mission、Capability、Runtime 或 Evidence。那些是系统为了把结果做对而使用的后台结构，不是用户开始使用它的前置知识。

与泛函网站真正值得类比的不是页面数量，而是单一动作闭环：对方可能是“找到合适职位并申请”，chenjin.io 应是“说出增长问题并得到第一个有用结果”。

### 9.2 唯一的 Aha Moment

```text
我有一个模糊的增长问题
        ↓
系统理解我的具体处境
        ↓
我得到一个有依据、现在就能执行的下一步
        ↓
我还能把这一步继续变成可复用的工作流
```

用户的 Aha Moment 不是“这里有很多增长知识和 Skills”，而是：

> **它真的理解了我的问题，并把我原本需要四处搜索、拼接和判断的东西，变成了一个可以马上使用的结果。**

第一次交互只需要输入一个问题。系统返回一张极短的 **First Move Card**：

- 你现在真正要解决的问题；
- 一个最值得先做的动作；
- 为什么，依据是什么；
- 你会拿到的第一个交付物；
- 下一步：直接使用、查看相似案例，或邀请陈今一起跑第一轮。

### 9.3 首页只保留五个区块

```text
1. 一句话价值 + 问题输入框
2. 三个真实问题示例
3. 一张 First Move Card 示例
4. 两到三个有边界的真实案例
5. 陈今是谁 + 一个次要行动入口
```

顶部导航最多保留 **Cases、Library、About**。Global Growth OS 的完整定义、Build Log、贡献规则、Skills、工具与技术说明放在二级页面或页脚，不与主路径竞争注意力。

### 9.4 对用户说人话，对系统保留结构

| 系统内部 | 用户看到 |
|---|---|
| Demand Intake | 说说你现在卡在哪里 |
| Growth Context Pack | 回答少量必要问题 |
| Mission + Capability Routing | 这是最适合你的第一步 |
| Artifact + Evidence | 这是可直接使用的结果和依据 |
| Run + Feedback | 试一下，告诉我是否真的有用 |

只有当用户想深入、复用或贡献时，才逐步展开 Research、Playbooks、Skills、Tools、Cases 和 Build Log。复杂度由系统承担，不转嫁给用户。

### 9.5 参考网站的极简抽象

[Web.Cafe](https://new.web.cafe/) 值得借鉴的是让真实问题持续进入、被编辑和沉淀；[Alignify](https://alignify.co/) 值得借鉴的是把研究包装成按工作目标可用的能力，并帮助用户跑完第一圈。chenjin.io 不复制它们的栏目规模、内容数量、积分、商店或 Skill 数量，只保留共同的底层逻辑：**问题进来，价值尽快出现，结果留下来并变得可复用。**

InsForge 增长负责人的经历只作为“为什么可以信任陈今”的一条证据放在 Cases 或 About；首页优先建立陈今长期处在“全球增长 × 开发 / Agents”的位置，以及她能够筛选、验证、组合和优化现有能力，而不是把公司职位作为主身份。

---

## 10. 陈今在 Global Growth OS 中的角色

陈今不是全部知识、方法和工具的原创者，也不需要成为所有增长环节的唯一专家或执行者。她当前更准确的责任是：

- 提出和维护系统的核心定义与质量原则；
- 持续深入全球增长与开发两个领域；
- 发现、筛选和连接高质量来源与能力；
- 判断哪些组件适合什么场景；
- 在真实任务中测试、适配和优化；
- 使用 AI Coding 或协作者补齐关键缺口；
- 明确人工判断、权限、来源和失效边界；
- 让运行结果、反例和贡献持续回到系统。

因此，“Builder”只能表达她会把系统做出来的一面，不能被理解为所有组件都必须亲自开发。更完整的角色接近 **Founder / Architect / Curator / Operator of Global Growth OS**。最终对外称谓仍待品牌表达验证。

Coding Agents 也不是唯一服务赛道。Coding 和开发能力代表陈今能够理解并操作技术系统，用 AI Coding、Agents 和自动化把增长判断转化为可运行结构。Global Growth OS 可以从 AI、Developer Tool、Agent Infra 和技术型产品开始验证，但长期领域仍是全球增长。

---

## 11. 用户、参与者与商业 ICP 的关系

Global Growth OS 可以服务不同层级的人，但不能让所有层级同时决定 v0.1 的产品设计。

| 角色 | 可能需要什么 | 与 OS 的关系 |
|---|---|---|
| 入门者 | 岗位地图、常识、信源与第一次产出 | Onboarding 与公开知识用户 |
| 增长实践者 | 方法、工具、Skills、复盘和效率提升 | 高频使用者与反馈贡献者 |
| Founder / Growth Lead / PMM | 围绕真实业务目标完成 Mission | 高价值验证者与潜在买家 |
| Agent / AI 工具 | 结构化 Context、能力描述、权限和评估 | 机器使用者或执行组件 |
| 专家、服务商和贡献者 | 分享信源、能力、案例和边界 | Capability 与 Evidence 贡献者 |

基于现有微信归档形成的 ICP 结论只能作为当前验证假设：已有产品和真实增长动作、但缺少可持续 Growth Ops 系统的全球 AI、Developer Tool、Agent Infra 或技术型 SaaS 小团队，可能是最值得优先验证的企业用户。该结论尚未完成付费和市场验证，不应限制 Global Growth OS 的长期概念边界。

---

## 12. v0.1 的最低验收标准

Global Growth OS v0.1 是否成立，不以页面数量、文章数量或 Skill 数量判断。最低应满足：

1. 至少一个真实 Growth Mission 被完整记录，而不是只有抽象 Demo。
2. Mission 明确关联产品价值、North Star 或阶段目标，不能只追求流量动作。
3. 当前 Strategy、Mission 优先级、Owner、资源与人工决策点清楚可见。
4. Mission 能关联来源、证据、上下文、能力、状态和成功标准。
5. 系统优先复用外部能力，并清楚记录来源、适配和人工判断。
6. 至少产生一个可检查、可带走、可继续使用的 Artifact。
7. 运行过程可以看见关键步骤、人工修改、失败和边界。
8. 至少记录一个过程、交付或业务评价；无法归因时不得把过程改善写成业务增长。
9. 反馈能够进入知识、能力、选择规则或下一版本 Roadmap。
10. 另一位用户或 Agent 能依据现有结构复现核心过程，而不完全依赖陈今口头解释。
11. 公开内容通过来源、隐私、公司边界和发布检查。

现有 AWW'26 公测夜的数量目标和日期计划由 `projects/global-growth-os/experiments/aww26-launch/project.md` 管理；它们是一次发布实验的验收标准，不等于 Global Growth OS 长期系统的全部验收标准。

---

## 13. 版本演进原则

### v0.1：Manual Runtime

使用最小 Kernel、Strategy Card、Organization Card、结构化知识库、少量 Skills、现成工具、Mission 模板、人工编排和反馈记录跑通一个闭环。网站、GitHub 和飞书只是不同入口。

### v0.2：Repeatable Runtime

在多次真实运行后，统一高频对象、状态、能力接口和评估方法；将重复选择沉淀为 Playbooks，将重复执行沉淀为 Skills 或自动化。

### v0.3：Composable Runtime

当能力数量和使用场景足够多时，增强能力发现、上下文组装、版本依赖、权限控制和跨工具适配，使不同人和 Agents 能稳定组合使用。

### 更后阶段：Productized Runtime

只有在手工与现有工具无法承受真实使用量、状态复杂度或协作需求时，才考虑开发专用 Runtime、Agent 接口、工作台或商业产品。是否走到这一步属于未来决策，不是当前承诺。

---

## 14. 仍待确认和验证的问题

1. Global Growth OS 的首个核心用户究竟是增长实践者、Founder / Growth Lead，还是同时允许两条入口但只优化其中一条？
2. 首个最值得反复运行的 Growth Mission 是市场情报、ICP、Launch、内容分发、Influencer、合作伙伴还是数据复盘？
3. “Global Growth OS”是长期公开品牌、产品名，还是当前阶段的工作名称？
4. Public Core 的权威仓库、许可证、贡献协议和版本策略是什么？
5. 飞书知识库与 GitHub 哪一个保存公开知识的权威版本，如何避免双向漂移？
6. Skill 采用哪一种开放格式，是否需要兼容不同 Agent 平台？
7. 哪些能力只能提供判断和建议，哪些可以连接外部系统执行动作？
8. 商业化更适合围绕 Mission、实施 Sprint、托管实例、会员访问还是其他形态？
9. 哪些运行指标能够真正证明 OS 比普通内容库或工具清单更有价值？
10. 个人网站应突出“陈今”还是“Global Growth OS”，两者如何共享信任而不互相覆盖？
11. Strategy Portfolio 和 Organization Card 在 v0.1 中需要多细，才能支持决策又不制造维护负担？
12. Public Core 应如何验证来自不同 Team Instance 的经验，避免把单个公司的成功条件误写成通用最佳实践？

这些问题进入真实验证，不在概念文档中提前封闭。

---

## 15. 相关材料与研究依据

### 本地相关材料

- `project.md`：私有全球化增长系统的范围与边界。
- `ROADMAP.md`：私有系统的阶段计划与里程碑。
- `projects/global-growth-os/project.md`：整个 Global Growth OS 的项目范围、当前状态与权威关系。
- `projects/global-growth-os/experiments/aww26-launch/project.md`：AWW'26 公开实验、活动与当次数量目标。
- `/Users/jinchen/Documents/ChatGPT/02-personal-ip-system/2026-08-31-微信双账号问题解决与未来产出地图.md`：基于双账号本地归档形成的能力与未来方向地图。
- `/Users/jinchen/Documents/Codex/2026-08-19/chatgpt/wechat-group-icp-analysis-2026-09-04.md`：基于群聊归档形成的商业 ICP 假设。
- 2026-09-11 用户提供的“字节 UG 增长系统”经验性叙述：用于抽象 Operating Kernel、Organization、Strategy Control Plane、Evidence Plane、Capability Platform 和 Runtime Loop；未作为对字节内部事实或行业优劣的独立核验来源。

### Agent / Agent Infra 一手参考

- [Anthropic：Building Effective AI Agents](https://www.anthropic.com/engineering/building-effective-agents)：区分 workflow 与 agent，并将 retrieval、tools、memory 视为增强模型的基础组件。
- [Model Context Protocol Architecture](https://modelcontextprotocol.io/specification/2025-06-18/architecture)：说明 host、client、server、能力协商、安全边界和 context 聚合。
- [MCP Server Primitives](https://modelcontextprotocol.io/specification/2025-06-18/server/index)：区分 resources、prompts 与 tools 的控制关系。
- [OpenAI Agents SDK：Agents](https://openai.github.io/openai-agents-python/agents/)：涵盖 instructions、tools、handoffs、sessions、guardrails 和 orchestration。
- [OpenAI Agents SDK：Tracing](https://openai.github.io/openai-agents-python/tracing/)：记录模型生成、工具调用、handoff、guardrail 和自定义事件。
- [LangGraph：Persistence](https://docs.langchain.com/oss/python/langgraph/persistence)：说明 checkpoint、持久状态、恢复、human-in-the-loop 和容错。
- [A2A Protocol：Core Concepts](https://a2a-protocol.org/latest/topics/key-concepts/)：定义能力发现、Task 生命周期、Message、Artifact、Context 和 Agent 间协作。

### 产品化与信息架构参考

- [Web.Cafe](https://new.web.cafe/)：参考其内容颗粒度、编辑精选、问答入口、贡献角色、发现机制与社区激励；其交易和流量数据仅视为网站自述与界面观察，不作为已独立验证的商业证据。
- [Alignify](https://alignify.co/) 及其 [Skills](https://alignify.co/skills)、[Services](https://alignify.co/services)、[AI Tools](https://alignify.co/tools) 与 [Growth Strategy](https://alignify.co/marketing) 页面：参考共享项目 Context、版本化能力包、按任务路由、首轮实施与交接、案例证明和内容—能力—服务闭环；其客户数、案例指标与效果主张未在本文中独立核验。

---

## 16. 当前结论

Global Growth OS 不是一套由陈今亲自生产全部内容和代码的增长产品，也不是知识库、Skills、网站或活动的简单集合。它是一套可实例化的社会—技术型全球增长基础设施：以产品价值和 North Star 为内核，以战略、组织、资源和治理为控制层，以数据、实验和评估为证据层，以可组合的知识、工具、人和 Agent 能力为中台，持续运行并改进真实增长任务。

v0.1 的正确策略是：保留完整 OS 逻辑，使用最低复杂度的实现。知识库与 Skills 可以是首批核心组件，Strategy Card 和 Organization Card 可以承载控制信息，人工可以承担编排，GitHub 和飞书可以承担版本与协作，个人网站可以承担公开入口；但系统必须从第一次真实 Mission 开始记录产品价值、目标、Owner、资源、状态、证据、能力选择、Artifact、评价和回流。

最重要的判断不是“我们还需要开发什么产品”，而是：

> **这套结构能否让一个团队围绕真实产品价值完成全球增长任务，不再从零开始，并在每次运行后获得更好的判断、更强的执行能力和更可靠的可复用系统。**
