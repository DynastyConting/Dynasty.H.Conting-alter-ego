# 变更记录

## 2026-09-13：V-009 七步法第四步资源与韧性域重构

- Archive ID：`KNOW-2026-09-13-V009`；Outcome Type=REPAIR（修复）；不形成020；正式进度仍019；
- Search Domain 07 从 Resource, Capacity, Allocation & Resilience（资源、容量、分配与韧性）重构并暂时冻结为 Resource & Resilience（资源与韧性）；
- Resource（资源）只问外部环境中当前任务所需资源是否存在可调用的可用存量／供给源；不以 Domain 01 已覆盖的质量审查在本域重审；机械检查句：就当前任务所需的资源类型，外部环境是否存在可调用的可用供给源／存量？四值 NORMAL / ABNORMAL / UNKNOWN / N/A；
- Resilience（韧性）问主供给受扰时，靠储备／冗余／备援／松弛／替代供给是否仍能维持当前任务所需；收窄为资源侧缓冲／备援抗扰动，非整系统恢复；例：主源断只剩半瓶撑 → 01当前流入可能NORMAL，Resilience可ABNORMAL；
- Capacity 记分流不武断删除：外部容器容量 → Resource；通道／管道容量 → Domain 01 Rate；对象自身内部容积 → Domain 03 Design Adequacy；
- Allocation（分配有无）分流至 Domain 01 Place、Domain 04 Omission、Domain 02 Activation State；公平／合理残留挂起（可能 Domain 11）；
- 余量并入 Resilience；恢复资源留给 Domain 09；瓶颈／争用不塞入本域；
- 当前纵向进度：01—03 Frozen；04主体成立未最终冻结；原05拆除且Time/Space挂起；06 Interface & Dependency主体完成；07 暂时冻结 Resource & Resilience；下一纵向位置 Domain 08 Information, Measurement & Model。

## 2026-09-04：V-008 七步法第四步接口与依赖域重构

- Archive ID：`KNOW-2026-09-04-V008`；Outcome Type=REPAIR（修复）；不形成020；
- Search Domain 06 从 Interface, Dependency & Propagation（接口、依赖与传播）收窄为 Interface & Dependency（接口与依赖）；
- Interface（接口）主体保留 Physical Compatibility（物理兼容性）与 Interface Contract Compatibility（接口契约兼容性）；后者统一承载电气／信号、协议／版本、握手、数据格式／字段／语义等非机械契约，但不把电气概念与协议概念混同；
- Functional Compatibility（功能兼容性）删除：能力不足回 Domain 02 Task Capability；方案本身不足以支撑需求回 Domain 03 Design Adequacy；仅双方能力成立但接口／契约不相容时归 Domain 06；
- Dependency（依赖）不重复建立新理论，Domain 06仅保留扫描入口；命中 Failure Independence（失效独立性）、Shared Dependency（共享依赖）、Coupling Mechanism（耦合机制）等问题后调用R-004既有结构；
- Propagation / Cascade（传播／级联）从Domain 06摘出挂起，保持PARKED / UNRESOLVED，后续在横向Causal Role / Causal Mechanism或剩余搜索域中重审；
- 新增仿生边界：七步法可继续作为Biomimetic / Bio-inspired（仿生／生物启发）系统，但仿的是可复用认知功能，不把用户个人习惯性排故顺序机械复制为机器规则；
- 当前纵向进度：01—03 Frozen；04主体成立未最终冻结；原05拆除且Time/Space挂起；06主体完成；下一纵向位置Domain 07。

## 2026-09-03：V-007 七步法第四步时间摘出与归因骨架澄清

- Archive ID：`KNOW-2026-09-03-V007`；Outcome Type=REPAIR（修复）；不形成020；
- Domain 04继续维持主体骨架成立但未最终冻结；Procedure Deviation 与 Omission / Execution Error 仍待收边；
- 原Domain 05 Spatiotemporal Coordination（时空协调）继续不整体接受；Time（时间）因与Domain 01 Timing高度重叠，从一级Search Domain位置摘出并与Space一并挂起；
- 第四步整体结构明确为 Outcome / Explanandum（结果／待解释项）→纵向Search Domain Axis生成候选→横向Orthogonal Dimensions描述／限定／审计；
- Output（输出）通常属于待解释结果，不再作为独立一级Search Domain；
- Domain 06保持UNRESOLVED / PENDING，课堂提出的Interface Mismatch / Dependency Failure / Interaction or Coupling / Shared Dependency / Propagation角色化等均只保留为Candidate Decomposition，不冻结；
- 挂起池记录Time、Space、Degradation / Fatigue，下一优先位置Domain 06。

## 2026-09-02：V-006 七步法第四步执行域与时空域拆分

- Archive ID：`KNOW-2026-09-02-V006`；Outcome Type=REPAIR（修复）；不形成020；
- Search Domain 04 Execution & Process（执行与流程）形成可用主体骨架：Omission、Incorrect Action / Execution Error、Procedure Deviation、Method–Task Misfit；
- Domain 04尚未最终冻结，Procedure Deviation与Omission / Execution Error仍存在待收窄交叠；
- 原Search Domain 05 Spatiotemporal Coordination（时空协调）不再整体接受；Space（空间）摘出挂起；Time（时间）暂留Pending；
- Domain 01 Timing已覆盖过早／过晚／顺序／频率／间隔／持续时间／同步，因此Time若保留为独立域必须证明额外的稳定因果机制；
- 延续“分类位置错误可先摘出、后安置”原则；Degradation / Fatigue继续等待Domain 10重审；
- Interface Contract完整审表继续Deferred。

## 2026-09-01：V-005 七步法第四步前三搜索域重构

- Archive ID：`KNOW-2026-09-01-V005`；Outcome Type=REPAIR（修复）；不形成020；
- 第四步 Attribution（归因）进一步收窄为“输入 Problem Representation（问题表征），输出 Candidate Direction（候选探索方向）”，不直接生成最终原因或具体行动；
- 全域统一审查状态为 NORMAL / ABNORMAL / UNKNOWN / NOT APPLICABLE；ABNORMAL 不编码严重程度；
- Search Domain 01 重构为 Input & Exposure（输入与暴露），使用 Normal Input Audit（正常输入审查）八项 + Exposure Audit（暴露审查）双遍扫描；
- Search Domain 02 重构为 State, Integrity & Task Capability（运行状态、完整性与任务胜任能力）；Degradation（退化）与 Fatigue（疲劳）从 Integrity（完整性）中摘出；
- Search Domain 03 重构为 Requirements, Design & Trade-offs（要求、设计与固有权衡），分别使用 Requirement Coherence（要求一致性）、Design Adequacy（设计适当性）、Inherent Trade-off（固有权衡）；
- 固有权衡改以当前结构下多个评价维度的稳定条件性 Coupling（耦合）与可行边界定义，不再使用“有得必有失”式绝对表述；
- 明确 Information Provenance（信息来源/信息溯源）≠ Input Source（输入来源）、Current State（当前状态）≠ Operational State（运行状态）、Subjective Exchange Willingness（主观交换意愿）≠ Constraints（客观约束）≠ Inherent Trade-off（固有权衡）；
- Search Domain 01—03 主体结构暂时冻结，04—12 继续作为待重构候选；`通用归因候选生成标准_V0.2.md` 文件名暂不升级，避免把局部修订冒充整套工具完成。

## 2026-08-27：U-003 信息五问边界增强

- 保持“五问”结构不变，不新增 U 编号、R 节点或正式污染编号；
- 第二问补入 Data-Generating Process（数据生成过程），要求检查信息在何种测量、筛选、规则或干预条件下生成；
- 第五问新增双向效果审计：Backward Evidential Effect（向后证据效应，工具内部标签）与 Forward Propagation（向前传播）；
- 明确“存在向后证据关系 ≠ 获得独立验证”；
- 若原判断、模型或规则参与制造后续结果，需检查 Evidential Dependence（证据依赖）与循环验证风险；
- 增强 U-003 与 003《可识别性》、019《牛鞭效应》及 R-004 的接口。

## 2026-08-24：副躯体架构重构

- 项目正式名改为《周承续的副躯体》；
- 原《七步五项法》仓库升级为更大的副躯体系统；
- 七步法被重新定位为稳定主干；
- “原始样本”改为“事实采样”；
- “分类”改为“结构化”；
- 状态 / 条件 / 资源 / 约束 / 轨迹独立为结构化原生工具；
- 下一动作五项、信息三项、余地四项独立为原生工具；
- U-003 信息五问、U-004 灰值判断独立为跨步骤工具；
- 新增通用归因候选生成标准 V0.2；
- 新增安全与审结层架构草案；
- 新增副躯体网络图与调用数据流；
- 保留 V-002 作为历史版本。
