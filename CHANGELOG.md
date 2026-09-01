# 变更记录

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
