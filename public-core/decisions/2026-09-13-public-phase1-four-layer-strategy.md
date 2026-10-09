# 决策备忘：公开第一阶段以四层内容架构为准

> 状态：历史策略；2026-10-09 已由[公开边界与版本决策](2026-10-09-public-boundary-and-version-policy.md)替代\
> 日期：2026-09-13  
> 范围：Public Core 对外公示策略；不改变本地完整 OS 工作准源  
> 相关：`ChenJinCloud/global-growth-os`、本地 `architecture/`、`project.md`、`ROADMAP.md`

## 决定

1. **本地**继续保留完整 Global Growth OS 设计（Kernel、Domain Model、Mission、Capability、Runtime、Evidence 等）作为工作准源与长期架构。
2. **对外公示第一阶段**以「四层内容架构」为准，初期**只输出**这四层，不把完整 OS 架构提前写进公开叙事。
3. 公开 GitHub（`ChenJinCloud/global-growth-os`）的对齐方式：在现有四层框架内填真内容、修正过期信息；**不**把公开 README / 目录改写成完整 OS 叙事。

## 四层（公开 Phase 1 产出边界）

| 层 | 公开名称 | 初期可产出 |
|---|---|---|
| 1 | 岗位与常识（Foundation） | 岗位、工具平台、基础常识 |
| 2 | 方法论与信源（Methodology） | 调研方法、信源、深挖模板 |
| 3 | Growth Toolkit | 可复用模板、脚本、工作流 |
| 4 | 反馈与社区（Feedback） | 需求/反馈入口、活动与迭代记录 |

完整 OS 对象（Mission 状态链、Strategy Card、Organization Card、Capability Registry 等）可继续在本地建设，但**不作为第一阶段对外公示内容**。

## 与既有权威文件的关系

- 本地架构准源仍是 `architecture/global-growth-os-concept-and-architecture-v0.1.md`（含：四层是公开内容视图，不是完整系统本身）。
- 本备忘约束的是**对外发布节奏与公开仓库叙事**，不废止本地架构，也不要求删除或改写本地完整设计。
- 公开仓库当前线上状态（截至 2026-09-13 核验）：`main` @ `4ec2c3c`（2026-09-09），四层骨架已建、内容多为空 README；后续填肉与信息修正以本策略为准。

## 公开仓库执行含义

- **做**：按四层补内容；修正过期公开信息（例如活动地点/时间与本地 AWW'26 实验对齐：杭州，2026-09-24）。
- **不做**：把公开首页改成完整 OS 层级图；把本地 Kernel / Runtime 等未脱敏设计直接推上公开仓库。
- 个人 IP / 内容侧若需 Public Core 素材，第一阶段按上述四层供给，不以完整架构文档为对外素材源。

## 非目标

- 不把「暂不公示完整 OS」解释为「本地架构作废」。
- 不把四层内容数量等同于 OS v0.1 已验收。
- 不将公司执行资产（如 InsForge 内部数据）因本策略进入公开四层。

## 后续触发重审的条件

- 至少一个真实公开 Mission / 活动反馈证明需要对外解释 OS 控制层；或
- Public Core v0.1 正式发布前需要调整公开叙事；或
- 陈今明确决定升级公开品牌从「四层内容」到「可实例化 OS」。
