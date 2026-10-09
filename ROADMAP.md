# Global Growth OS 路线图

> 本文件是整个 Global Growth OS 的阶段、里程碑和执行状态入口。单次活动与实验在 `experiments/` 中展开。

## 阶段 0：权威源与项目架构

- [x] 建立 Global Growth OS 概念与 v0.1 架构准源
- [x] 明确 Public Core、私有实例和公司机密边界
- [x] 将 `projects/global-growth-os/` 确立为整个 OS 的唯一项目目录
- [x] 合并重复的 `proj-1788924797868-czj6i7` 本地项目入口
- [x] 将 AWW'26 公测降为 OS 下的一次实验
- [x] 2026-10-09 核验公开 GitHub 结构、提交和发布状态

## 阶段 1：runtime-v0.1 Manual Runtime

- [ ] 建立最小 Kernel：产品价值、目标用户、North Star、约束与运行原则
- [ ] 建立 Strategy Card 与 Organization Card
- [ ] 定义 Demand、Mission、Evidence、Capability、Run、Artifact、Feedback 的最小字段
- [ ] 建立 Demand Intake 与优先级入口
- [ ] 建立 Capability Registry
- [ ] 建立 Mission 模板、状态链和人工检查点
- [ ] 建立 Run Log、Artifact 验收和 Evaluation 模板
- [ ] 完整运行至少一个真实 Mission，并保留反馈回流记录

## 阶段 2：Public Core 内容与发布治理

- [x] 对齐通用架构的公开边界与 `ChenJinCloud/global-growth-os` 声明
- [x] 明确公开知识、能力包、案例与贡献要求
- [x] 定义版本范围与交付状态；见[版本定义](public-core/VERSIONING.md)
- [ ] 为每个能力包补齐来源、适用范围、验证状态和失效条件
- [ ] 建立 chenjin.io、GitHub 与飞书各自的职责和发布链路
- [ ] 完成来源、隐私和公司边界审核
- [x] 2026-09-23 开放公开知识内容首版 content-v0.1；见[版本定义](public-core/VERSIONING.md)
- [x] 建立[飞书资源索引](public-core/content-index.md)
- [ ] 完成逐篇正文发布映射与持续同步机制

## 阶段 3：真实实验与反馈

- [ ] 完成 [`AWW'26 首发与 9/24 公测`](experiments/aww26-launch/project.md)
- [ ] 将真实问题转换为结构化 Demand 和 Mission
- [ ] 记录现场运行、人工修改、失败与反例
- [ ] 将有效反馈进入 v0.2，而不是直接升级成最佳实践

### 已收集反馈

#### F-001：Growth OS 需求征集（已脱敏）

来源：`Growth OS · 需求征集表单`，1 条有效提交。

- 画像：前出海 0→1，现半自由职业 + AI 使用
- 阶段：0→1，还没跑起来
- 希望 Growth OS 提供：分析、筛选、复用、提炼
- 当前卡点：不同 AI 生态磨合调用
- 希望深挖：介绍一个希望大家都学会的 AI 使用场景；未来阶段关注使用 AI 的方向或需要解决的问题
- [ ] 将该反馈转换为结构化 Demand，并设计一个可验证的 Mission
- [ ] 用一次真实运行验证“分析—筛选—复用—提炼”链路是否能降低 AI 生态磨合成本

## 阶段 4：Repeatable Runtime

- [ ] 从多次 Mission 中识别稳定、可复用的运行模式
- [ ] 将重复选择与路由升级为 Playbook、Skill 或轻量自动化
- [ ] 建立能力回归测试、弃用和替代机制
- [ ] 建立可恢复的状态、日志和定期评估节奏

## 后续阶段

只有 Manual Runtime 被真实运行并证明有用后，才评估 Composable Runtime、自动编排或产品化 Runtime；不以功能数量替代有效性证明。
