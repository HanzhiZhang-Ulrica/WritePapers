# WritePapers

按当前研究与稿件进展，分阶段完成研究定位、全文规划、起草、修改、检查和投稿准备。

Agent 先判断当前任务与已有成果，再选择对应 skill。每个阶段都有交付内容和完成标准；完整论文由这些阶段连续推进。

## 独立画图部分

[画图目录](figures/README.md) · [工具](figures/tools.md) · [配色与实例](figures/palettes.md)

绘图工具和配色单独维护，需要作图时从此处进入，不加入下方的论文正文写作阶段流程。

## Agent 从这里开始

1. 接收用户当前要求。最小输入是代码仓库与目标会议及年份；已有草稿、结果、研究日志和批注一并使用。用户可以只要求修改某段或检查某类问题，不必提供阶段编号。
2. 读取最新材料，确定当前生效的版本、已完成的工作、正在运行的实验，以及作者已接受或拒绝的选择。以实际产物和来源判断进展。
3. 用下方阶段表检查哪些完成标准已经满足。保留这些成果，从当前任务涉及的未完成工作进入；进展不清楚时使用 [write-papers](skills/write-papers/SKILL.md) 判断入口。
4. 读取 [共同要求](skills/write-papers/references/common-rules.md)，选择对应阶段 skill 和规则文件。只读取当前任务需要的部分。
5. 完成当前阶段的具体产物，核对完成标准，更新进展与待核对事项，再决定下一步。已有正文的局部修改保护未受影响的已确认内容。

**全流程任务持续推进到完整初稿，并按任务范围继续修改、终检与终稿准备。** 阶段之间允许交叉：会议调研与代码阅读可以同时进行；实验尚在运行时，Method、Related Work 和 Appendix 中已确认的内容可以继续写。

只有出现会根本改变研究定位、方法真实性或主要结果的关键问题时，才集中请作者判断。已有配置和结果应先从材料中寻找。

## 接受输入并记录当前进展

新项目的最小输入：

```text
Repository: [GitHub URL / Branch / Commit / ZIP]
Target Conference: [会议名称 + 年份]
```

继续已有项目时，可以额外提供当前稿件、结果、批注或简单进度说明。缺少这些说明时，agent 从已有材料中判断；以下记录由 agent 整理，不要求用户逐项填写。

| 当前状态 | 应确定的内容 |
| --- | --- |
| 当前任务 | 全流程、指定章节、局部修改、专项检查、终稿检查或审稿回应 |
| 研究版本 | 当前 branch、commit、方法配置及稿件版本；历史路径与当前路径的区别 |
| 投稿目标 | 会议、年份、投稿类型、官方要求及实际截止日期 |
| 已有产物 | 会议调研、方法事实、结果来源、最近邻比较、研究主线、证据关系、Blueprint、草稿和 PDF |
| 已确认选择 | 研究范围、命名、贡献、术语、作者已接受及拒绝的建议 |
| 实验状态 | 已完成并核对、等待验证、正在运行、尚未运行或当前无法获得 |
| 排版状态 | 正文是否锁定页数，图表是否确定，是否已有待提交的实际 PDF |
| 当前阶段 | 阶段编号、判断依据、已满足的完成标准、待核对或等待数据的部分 |
| 下一步 | 选择的 skill、当前需要的规则、下一项具体交付和验收条件 |

状态可先在对话中维护。交付时说明当前完成了什么、还缺什么及下一步，不把尚未核对的事项记录为已完成。

## 从用户当前任务选择入口

| 用户输入或当前材料 | 入口 | 从哪里开始 |
| --- | --- | --- |
| 只给仓库与会议，尚无论文定位 | [paper-research](skills/paper-research/SKILL.md) | Phase 0：确认版本和作者要求，再建立事实与证据 |
| 已有代码与实验，但主要问题、insight 或最近邻区别尚未确定 | [paper-research](skills/paper-research/SKILL.md) | Phase 3–6 中尚未满足的部分，保留已核对事实 |
| 主线已确认，准备写全文；或实验仍在运行 | [paper-draft](skills/paper-draft/SKILL.md) | Phase 7–11：规划并起草有依据的正文，缺失结果保留准确位置 |
| 明确要求只写 Introduction、Method、Appendix 等部分 | [paper-draft](skills/paper-draft/SKILL.md) | Phase 10 或 11：使用已确认研究设计和对应章节规则 |
| 已有完整稿，希望系统审阅和修改 | [paper-revise](skills/paper-revise/SKILL.md) | Phase 13：按六轮顺序审阅，再做必要替换 |
| 指定一句、一个 caption、减少 6 词或处理明确批注 | [paper-revise](skills/paper-revise/SKILL.md) | Phase 14：打开当前原文，控制修改幅度并处理必要联动 |
| 只检查引用、LaTeX、图表、实际 PDF 或匿名要求 | [paper-audit](skills/paper-audit/SKILL.md) | Phase 12/15：检查指定范围，报告实际覆盖的层次 |
| 正文与附录已整合，准备投稿 | [paper-audit](skills/paper-audit/SKILL.md) | Phase 15–16：全文审计、唯一终稿和实验来源冻结 |
| 已收到 reviewer 问题，需要定位证据或写 Rebuttal | [paper-audit](skills/paper-audit/SKILL.md) | Phase 16 的审稿问题与回应规则 |
| 需要按截止日期调整工作顺序 | [paper-audit](skills/paper-audit/SKILL.md) | Phase 17：结合当前进展倒排时间 |
| 用户只说“继续”，或无法确定当前进度 | [write-papers](skills/write-papers/SKILL.md) | 读取最新材料与上次状态，再选择未完成的阶段 |

指定只做文字写作时，依据已确认研究设计推进正文。局部修改与专项检查按用户指定范围进行。关键研究事实出现新冲突时，定位冲突及其影响，再处理相关阶段。

## 完整阶段表与完成标准

Phase 0–16 覆盖研究写作到终稿准备。Phase 17 可在任何阶段用于时间管理；Phase 18 是新项目或续写的输入入口。

| Phase | 当前任务 | Skill | 交付与进入下一阶段的条件 |
| --- | --- | --- | --- |
| 0 | 项目启动与版本确认 | [paper-research](skills/paper-research/SKILL.md) | 明确当前研究版本、目标会议和作者已确定的选择 |
| 1 | 会议、年份、领域及样例调研 | [paper-research](skills/paper-research/SKILL.md) | 确定投稿分类、目标读者、研究质量要求、近邻情况及篇幅格式 |
| 2 | 阅读当前生效代码 | [paper-research](skills/paper-research/SKILL.md) | 能解释算法、数据与执行流程，并追溯到实现和配置 |
| 3 | 结果与实验协议 | [paper-research](skills/paper-research/SKILL.md) | 进入论文的关键数字有来源、单位、比较条件、方法版本及状态 |
| 4 | 相关工作与 novelty | [paper-research](skills/paper-research/SKILL.md) | 以具体行为和技术关系说明最近邻区别及实质增量 |
| 5 | Problem、Gap、Insight、Difficulties、Contributions | [paper-research](skills/paper-research/SKILL.md) | 形成一条研究主线，关键关系能够用普通语言说明且有真实逻辑 |
| 6 | Contribution–Experiment 闭环 | [paper-research](skills/paper-research/SKILL.md) | 每项贡献有对应机制与证据，每组核心实验有明确职责 |
| 7 | 全文 Blueprint | [paper-draft](skills/paper-draft/SKILL.md) | 各节和各段的主题、必要内容、公式、引用、图表及附录指向明确 |
| 8 | 图表的论证职责 | [paper-draft](skills/paper-draft/SKILL.md) | 确认图表研究问题、真实来源与正文位置；已确定图表有对应 caption |
| 9 | 第一版全文 | [paper-draft](skills/paper-draft/SKILL.md) | 形成可以从头到尾阅读的连贯初稿，已有材料全部用于相应正文 |
| 10 | 各节精写 | [paper-draft](skills/paper-draft/SKILL.md) | 各节职责完整、整体故事顺畅、必要内容能够独立理解 |
| 11 | Appendix | [paper-draft](skills/paper-draft/SKILL.md) | 方法细节、推导、控制定义、协议及完整结果可查，正文指向有效 |
| 12 | Bibliography、术语与 LaTeX | [paper-draft](skills/paper-draft/SKILL.md) / [paper-audit](skills/paper-audit/SKILL.md) | 引用与编号明确对应、元数据正确、术语稳定；写作时整合，检查时审计 |
| 13 | 六轮系统性修改 | [paper-revise](skills/paper-revise/SKILL.md) | 依次处理科学性、研究故事、读者理解、文风、图表引用与模拟审阅，剩余问题分类明确 |
| 14 | 精准替换与批注管理 | [paper-revise](skills/paper-revise/SKILL.md) | 准确位置、原文、修改后和原因可直接使用；保留已确认内容与状态 |
| 15 | 全文最终审计 | [paper-audit](skills/paper-audit/SKILL.md) | 对源码、科学一致性、实际 PDF 和提交合规分别给出检查结论 |
| 16 | 终稿冻结与审稿准备 | [paper-audit](skills/paper-audit/SKILL.md) | 唯一最终版本、关键实验来源和 reviewer 问题对应位置可追溯 |
| 17 | 倒排时间与阶段验收 | [paper-audit](skills/paper-audit/SKILL.md) | 计划对应实际截止日期和当前实验进度，已满足完成标准的阶段继续推进 |
| 18 | 启动或继续下一篇论文 | [write-papers](skills/write-papers/SKILL.md) | 接收最小输入或当前状态，回到适合的阶段 |

## 阶段之间怎样继续

- 全流程任务完成当前阶段后继续下一项必要工作。局部任务完成指定范围，并同步处理必要的跨节一致性。
- 已完成阶段依据最新材料与作者确认保留；不因另一个位置需要缩短而重新改写已接受的段落。
- 实验状态与写作状态分别记录。等待结果时，可以完成已有依据的正文和协议；关键主张仍缺证据时保留待核对状态，不能标记终稿审计完成。
- 图尚未确定时，保留图环境、标签和中性图注占位；图表规划不提前规定面板、布局或图中结论。
- 修改定位问题后，给准确位置、当前原文、修改后和原因。已锁定正文优先等长或更短替换，详细补充进入 Appendix。
- 审计分别记录源码检查、科学性核对、PDF 逐页检查和程序执行验证的实际范围。检查一层完成，不代表其他层已通过。
- 作者已确认或拒绝的要求持续有效。只有新的实质性证据或必要的跨节冲突，才重新处理相关选择。

## Skill 与规则的分工

README 维护阶段选择与完成标准；各 skill 维护当前任务入口。写作规则集中在下列文件中，共同规则只保留一份。

| 规则文件 | 内容 |
| --- | --- |
| [共同要求](skills/write-papers/references/common-rules.md) | 研究问题与洞察、逻辑、对象、机制、语言、引用、范围与最新作者决定 |
| [研究定位与证据](skills/write-papers/references/research-and-evidence.md) | 会议、代码、结果、版本状态、最近邻、候选 framing 与证据关系 |
| [全文规划与完整起草](skills/write-papers/references/drafting-plan.md) | Blueprint、图表职责、写作顺序、完整初稿与 Appendix 补齐 |
| [各节写作](skills/write-papers/references/paper-sections.md) | Title、Abstract、Introduction、Related Work、Method、Experiments、Appendix、Conclusion |
| [逐句修改与表达](skills/write-papers/references/revision-and-style.md) | 精确替换、修改幅度、术语格式、六轮审阅、问题分类及批注状态 |
| [成稿与投稿检查](skills/write-papers/references/final-checks.md) | 引用、实验、语法、图表、指标、PDF、文件清理与四层审计 |
| [终稿冻结、审稿回应与时间安排](skills/write-papers/references/submission-and-response.md) | 唯一终稿、实验来源、审稿问题、Rebuttal 与倒排时间 |
| [原始材料与规则来源](skills/write-papers/references/source-map.md) | 原文存档、逐项出处与本轮归并处理 |

## 可直接提供给 Agent 的输入

```text
请按本仓库 README 判断当前论文进展，选择对应阶段 skill，完成当前任务并更新进展。

Repository: [URL / branch / commit / ZIP]
Target Conference: [会议名称 + 年份]

Current Materials（如已有）: [稿件 / 结果 / 批注 / 上次进度]
Task: [从头推进全文 / 继续当前阶段 / 写指定章节 / 局部修改 / 指定检查 / 投稿准备 / Rebuttal]
Confirmed Decisions（如已有）: [已确认范围、术语、贡献、排版或拒绝的建议]

请先读取最新材料，说明当前阶段、判断依据与本次交付。
全流程任务持续推进已有依据的部分；局部任务保护未受影响的已确认内容。
```

## 原始流程、检查清单与外部参考

阶段导航依据 [完整流程原文](skills/write-papers/references/sources/full-paper-workflow.md)，新增或进一步强调的要求已归入对应规则，重复内容不再整段复制。

[Computer Science Paper Pre-Submission Checklist](skills/write-papers/references/sources/cs-paper-pre-submission-checklist.pdf) 已归入终检规范，逐项对应保留在规则来源表。

[外部写作方法参考目录](references/writing-methods.md) 仅供需要时专门查找写作方法，不直接融合进现有 skills 的描述或规则。
