# 从零开始完成一篇高质量学术论文：完整研究、规划、写作、修改与投稿流程

基于 AlignQuant 整个研究定位、论文规划、完整起草、反复修改、Appendix 补充、文献调查与投稿审计过程整理

这是一套可以直接复用到下一篇论文的 End-to-End Paper Writing SOP。目标是以后只需要输入：

代码仓库 + 目标会议及年份

写作者就能主动完成代码理解、会议调研、研究定位、论文结构规划、完整写作、实验结果分析、Appendix、逐轮修改和终稿检查。

这次把整个流程直接放在对话中，不创建任何文件。其中涉及的工作表、证据账本和写作计划，也都可以先在对话中完成。

# 第一部分：总目标、执行原则与工作流程

## 1. 最终希望达到什么效果

一篇优秀论文最终需要让读者明白六件事：

1. Problem： 正在解决什么重要而具体的问题？
2. Research Gap： 哪个真实约束使这个问题值得继续研究？
3. Insight： 作者抓住了什么关键现象、关系或设计原则？
4. Method： 为什么当前方法能够利用这个 insight 解决问题？
5. Evidence： 哪些实验或理论结果支持这些主张？
6. Knowledge： 读者完成阅读后获得了什么可以迁移到其他研究中的认识？

全文的 Abstract、Introduction、Related Work、Method、Experiments、Appendix 和 Conclusion，都为这六个问题服务。

其中最重要的原则是：

论文不能只是介绍作者做过什么，还需要解释这些工作为什么值得做、为什么这样设计，以及读者由此学到了什么。

代码可能包含多个算法、优化组件和执行路径。论文需要从中找到一条真正有价值的研究主线，而不是按照代码开发顺序罗列组件。

## 2. 必须长期遵守的写作原则

| 原则                | 具体执行要求                 |
| ----------------- | ---------------------- |
| 研究判断先于写作          | 先确认工作真正的价值，再决定如何表达     |
| 证据先于主张            | 重要 claim 对应代码、公式、实验或理论 |
| Research Gap 必须真实 | 解释实际需求、结构性困难与其后果       |
| 一篇论文一个核心认识        | 多项贡献共同服务于清晰的主要研究问题     |
| 作者承担解释成本          | 新概念出现时，读者已经知道为什么需要它    |
| 正向展示研究价值          | 使用具体设计和结果，减少防御性措辞      |
| 具体而不琐碎            | 保留必要机制，低层实现放 Appendix  |
| 减少自造术语            | 使用领域熟悉的名称，确保一词一义       |
| 科学结论有范围           | 明确模型、任务、硬件、指标与比较对象     |
| 保护已确认内容           | 作者已经接受的选择稳定保留          |
| 从头到尾完成            | 不停在提纲、占位框架或孤立的小节       |
| 修改要有原因            | 每次修改解决可辨认的事实、逻辑或表达问题   |

这里特别区分写作策略和研究诚信。

论文应当围绕真实优势组织叙事，减少主动自我辩护和无意义的缺点罗列；同时保留支撑结论所必需的实验条件、重要取舍与会议要求的披露。两者完全可以兼顾。

## 3. 所有阶段的完整导航

| 阶段 | 任务                         | 最终成果                                   |
| -- | -------------------------- | -------------------------------------- |
| 0  | 启动研究写作任务                   | 当前研究范围和作者要求                            |
| 1  | 调查目标会议与年份                  | 会议偏好、track、篇幅、证据要求                     |
| 2  | 完整阅读代码仓库                   | 方法事实、算法和执行流程                           |
| 3  | 审查实验和结果                    | 数据、配置及可信结果账本                           |
| 4  | 阅读相关工作                     | 技术谱系、最近邻、区别                            |
| 5  | 构建 Framing 与 Contributions | Research question、insight、difficulties |
| 6  | 建立 Claim–Evidence 关系       | 每项贡献和结果对应                              |
| 7  | 制定逐页、逐段、逐句计划               | 完整论文 Blueprint                         |
| 8  | 规划 Figures 和 Tables        | 图表职责、来源、位置                             |
| 9  | 完成第一版全文                    | 连贯的论文初稿                                |
| 10 | 逐节精写                       | Abstract 到 Conclusion 的完整正文            |
| 11 | 撰写 Appendix                | 推导、执行、实验协议及完整结果                        |
| 12 | 整理文献与 LaTeX                | 引用、符号、术语和格式统一                          |
| 13 | 六轮系统性修改                    | 科学性、结构、可读性和文风                          |
| 14 | 逐项精准替换                     | 原文、修改后、原因和修改状态                         |
| 15 | 全文最终审计                     | Ref、typos、内容、图表、排版                     |
| 16 | 投稿前冻结与准备                   | 终稿及可追溯的实验依据                            |
| 17 | 时间管理与阶段验收                  | 每个阶段的完成标准                              |
| 18 | 下一篇论文直接复用                  | 最小输入与完整执行 Prompt                       |

这些阶段是一套连续流程，实际工作允许交叉进行。例如研究定位会随着相关工作调查而更新，实验继续运行时也可以先完成 Method 和 Appendix 的协议部分。

默认直接推进到完整初稿。 只有出现会根本改变研究定位、方法真实性或主要结果的关键问题时，才集中请作者判断。

# 第二部分：开始写之前，先真正理解研究

## Phase 0：项目启动与输入确认

### Step 0.1：接收最小输入

```
Repository: [GitHub URL / Branch / Commit / ZIP]
Target Conference: [Conference + Year]
```

如果用户另外提供论文草稿、实验结果、研究日志或写作约束，一并作为当前项目材料。

### Step 0.2：确定当前生效的研究版本

先明确：

- 当前代码的主方法是什么？
- 是否存在旧版实现、已废弃方法或历史实验？
- 当前论文对应哪个 branch、commit 或方法配置？
- 哪些实验已经完成，哪些正在运行？
- 是否已有被作者确认的研究问题、命名和贡献？
- 是否有此前明确拒绝的写法或设计解释？

不能因为 README 排在仓库最上面，就将其中的历史描述直接当作当前论文的方法。

应当沿着实际的运行入口、配置和保存结果，确认当前生效的研究路径。

### Step 0.3：建立信息来源优先级

不同信息应采用对应的事实来源：

| 信息               | 优先依据            |
| ---------------- | --------------- |
| 当前论文希望表达的主张与研究范围 | 最新稿件和作者最新决定     |
| 算法实际执行了什么        | 当前生效代码与配置       |
| 最终数值及其评价口径       | 最终实验结果和对应运行记录   |
| 投稿要求             | 目标会议当年的官方资料     |
| 已有工作的机制          | 原论文、官方实现和正式发表信息 |
| 历史背景             | 旧日志、旧计划、早期讨论    |

发现不一致时，先辨别版本和范围，再决定如何处理。

### Step 0.4：整理已经确认的写作要求

例如：

- 是否禁止特定句式或术语？
- 是否偏好五段式 Introduction？
- 方法是否已经冻结？
- 是否要求缩写第一次出现时展开？
- 正文页数是否已经锁定？
- 是否必须使用给定论文作为文风参照？
- 是否要求修改前后分别使用 code fence？

这些约束必须持续有效。作者已经拒绝的建议进入“已拒绝”状态，除非出现新的实质性证据，否则不再重新推荐。

### Phase 0 完成标准

能够准确回答：

> 这次要写的是哪一个当前研究版本，面向哪一个会议，作者已经确定了哪些选择？

满足后进入会议调研与代码阅读。

## Phase 1：目标会议、年份、领域偏好与写作样例调查

### Step 1.1：检查当年官方要求

必须查看目标会议的：

- Call for Papers。
- Author Guidelines。
- Reviewer Guidelines。
- LaTeX 官方模板。
- Track、Primary Area、Subject Area、Keywords 等实际投稿字段。
- 正文页数、参考文献、Appendix 和 Supplementary 的规则。
- 匿名与公开代码要求。
- AI Use、Ethics、Reproducibility 等政策。
- 截稿时间及时区。

使用指定年份的规则，避免把上一年的要求套用到当前年份。

### Step 1.2：确定最合适的投稿分类

先根据代码判断研究贡献属于什么类型：

- 新算法与优化规则。
- 新模型结构或表示。
- 系统、软件、硬件与实际执行。
- 数据集或 Benchmark。
- 模型行为与评价。
- 理论分析。
- 应用研究。

然后判断论文的最主要学术贡献由哪个类别的读者最容易正确评价。

例如，一个项目包含优化算法，也包含 CUDA kernel。如果主要增量在表示与实际执行的共同设计，写作就应该让评审看到这项系统层面的知识和证据，而不是因为包含一个优化公式，就将其包装成优化理论论文。

### Step 1.3：阅读近两年相似论文

建议初始阅读量：

| 类型        | 数量  | 目的            |
| --------- | --- | ------------- |
| 技术最近邻论文   | 4–6 | 判断实质区别        |
| 同会议同类型论文  | 4–6 | 学习会议中的证据与组织方式 |
| 特别清楚的写作范例 | 2–3 | 学习段落职责、语言与图表  |
| 公开审稿记录    | 2–4 | 了解实际关注的问题     |

这些是起始阅读预算。真正重要的是覆盖最接近的工作，而非完成固定数量。

每篇论文都应检查：

1. 标题怎样表达研究对象和贡献？
2. Abstract 第一句从哪里开始？
3. Research Gap 具体是什么？
4. Introduction 有多少段，每段承担什么？
5. Figure 1 展示结构、观察还是实验结果？
6. Method 先介绍总体框架还是按组件推进？
7. 最核心的公式承担什么作用？
8. Experiments 最先展示什么？
9. 哪些实验支持真正的新设计？
10. 哪些细节放进 Appendix？
11. Conclusion 带给读者什么认识？
12. 如果审稿可公开，审稿人对什么证据提出了具体问题？

### Step 1.4：建立研究论文对比表

| Paper  | 核心问题 | 主要机制 | 研究认识 | 关键实验 | 值得学习的写作技巧 |
| ------ | ---- | ---- | ---- | ---- | --------- |
| 最近邻 A  | 实际问题 | 真实方法 | 新增能力 | 主要证据 | 问题引出方式    |
| 最近邻 B  | 实际问题 | 真实方法 | 新增能力 | 主要证据 | Method 组织 |
| 同会范例 C | 实际问题 | 真实方法 | 新增能力 | 主要证据 | 图表与实验     |
| 同会范例 D | 实际问题 | 真实方法 | 新增能力 | 主要证据 | 叙事节奏      |

学习的是信息选择、研究判断、逻辑顺序和表达风格。技术事实和结论必须属于当前研究本身。

### Step 1.5：吸收写作技巧

优先应用我们此前确定有效的原则：

- Nanda：论文要让读者记住少数真正有价值的研究认识。
- Farquhar：先减少低价值内容，再精简句子。
- Gopen 与 Swan：信息出现顺序应符合读者已有认知。
- Mensh 与 Kording：整体文章、章节和段落各有明确职责。
- Levin 与 Redell：系统实现工作量与研究贡献分开。
- Irene Zhang：明确使用场景，整体性能和设计消融承担不同证据职责。
- 小说与剧本：建立具体场景、真实冲突和持续的信息推进。
- Deslop / Humanizer：清理机械语言结构与空泛概括。

这些技巧需要融入最终文章，而不是照搬某份 skill 的固定句数、强制段尾或句式模板。

### Phase 1 完成标准

必须确定：

投稿分类、目标读者、会议真正关注的研究质量、近邻研究情况、篇幅与格式规则。

## Phase 2：完整阅读代码仓库

这一阶段决定论文在技术上是否可信。

### Step 2.1：建立完整仓库地图

先扫描：

- 核心源码目录。
- 运行入口。
- 算法与模型实现。
- 数据处理。
- Calibration 或 Training。
- 推理或执行代码。
- CUDA/Triton/CPP kernel。
- 配置文件与 Model Presets。
- 实验脚本。
- 测试。
- 日志和结果。
- 绘图代码。
- README、设计文档、历史记录。

先确定哪些路径与当前方法有关，再追踪执行流程。

### Step 2.2：按运行顺序阅读核心算法

对于每个重要函数，理解：

1. 输入是什么？
2. 输入形状与数值类型是什么？
3. 进行了哪些转换？
4. 方法在这里作出了什么决策？
5. 依据哪些数值、统计量或约束？
6. 输出了什么？
7. 输出会交给哪个步骤？
8. 该操作为什么对研究目标重要？

直到能够用普通语言完整描述：

Input → Transformation → Decision → Representation → Computation → Output。

对非系统研究，这条链条可以替换为对应的训练、生成、选择或求解过程。

### Step 2.3：区分不同实现状态

不要把仓库所有代码都当成当前方法。

| 状态         | 含义             |
| ---------- | -------------- |
| 当前主路径      | 论文实际采用的实现      |
| Optional   | 可选功能，须确认实际是否启用 |
| Ablation   | 只用于消融          |
| Diagnostic | 只用于调试或分析       |
| Legacy     | 历史方法           |
| Planned    | 文档提出但尚未完成      |
| Unverified | 存在代码，但尚不能确认行为  |

只有确认生效的路径，才能进入 Method 的技术事实。

### Step 2.4：深入理解数学机制

确定：

- 主要输入、输出与决策变量。
- 损失函数或目标。
- 优化约束与预算。
- 局部计算与全局计算之间的关系。
- 近似、估计与实际量的区别。
- 推理或训练过程中哪些量保持不变。
- 是否存在多阶段聚合。
- 数值变换能否恢复到原始坐标或输出。
- 理论推导有哪些必要条件。

不要为写论文重新发明符号。 首选领域熟悉的变量，保持一个符号代表一个明确对象。

### Step 2.5：阅读存储、数据流和实际执行

尤其对系统或高效推理研究：

- 哪些数据持久保存？
- 哪些数据在当前调用中临时创建？
- 压缩表示与计算表示分别是什么？
- 数据转换发生在 CPU、GPU memory、shared memory 还是 registers？
- 哪些 kernel 实际执行？
- 不同 batch、sequence length、hardware 触发哪些路径？
- 哪些输入可复用？
- 哪些中间结果可复用？
- Scale、metadata、padding 与输出重构如何处理？
- 完整运行时间是否包括在线准备与转换？

需要区分：

Logical unit、Storage unit、Kernel unit、Instruction unit。

这些概念可能相关，但不能未经实现验证就当成同一个单位。

### Step 2.6：建立方法事实卡

对每个主要组件整理：

```
Component:
Purpose:
Input:
Output:
Shape / Dtype:
Main operation:
Decision rule:
Scope:
Execution stage:
Persistent or temporary state:
Hardware or workload conditions:
Source code location:
Configuration:
Associated experiments:
Scientific contribution:
```

### Step 2.7：用代码回答研究问题

代码阅读结束后，尝试不用代码函数名解释：

> 这项方法改变了什么决策或计算关系？为什么这样改变？它实际产生了什么能力？

如果只能用模块列表回答，说明研究理解还没有完成。

### Phase 2 完成标准

读者提出“这个值怎么算”“这个结构如何存储”“两个阶段如何共享”之类问题时，能够准确解释，并追溯到代码。

## Phase 3：阅读实验结果、检查协议与建立证据账本

### Step 3.1：盘点实验资产

从所有实验脚本、配置、日志、CSV、JSON、绘图文件和已有表格中，寻找：

- Main quality。
- Main efficiency。
- External baselines。
- Internal structural controls。
- Scoring/algorithm ablations。
- Runtime ablations。
- 不同模型、长度、硬件的结果。
- 稳定性、随机种子和统计量。
- 内存、存储、能耗与峰值。
- 已完成但尚未写进论文的分析。

### Step 3.2：明确每组实验的具体配置

每个结果至少记录：

```
Experiment ID:
Result file:
Model / Revision:
Tokenizer:
Method / Configuration:
Dataset / Split:
Evaluation task:
Metric and direction:
Shot count / Prompt format:
Hardware:
Runtime backend:
CUDA Graph:
Attention backend:
KV-cache configuration:
Batch size:
Prompt length:
Generated length:
Warmup / Repetitions:
Timing boundary:
Memory or energy accounting:
Result:
Status:
```

在用户已经确认跨方法条件匹配、同一 evaluator 和同一 metric field 时，应将这些记录为已确认事实，写入协议即可。

### Step 3.3：处理各种容易混淆的指标

重点区分：

- Perplexity 的绝对值、变化量和相对变化。
- Accuracy 与 normalized accuracy。
- TTFT、TPOT、吞吐和整次请求延迟。
- Kernel-only latency 与 End-to-end latency。
- Nominal bits per weight 与实际 packed BPW。
- Serialized model size、resident memory 与 peak memory。
- 在线运行时成本与离线构造成本。
- 长度等级与 tokenizer 实际 token 长度。
- 单模型跨硬件与多模型单硬件。
- 默认实验与 calibration robustness 等特殊配置。

### Step 3.4：计算结果时固定比较条件

任何性能或质量比较都应明确：

Model + Method + Dataset/Workload + Hardware + Metric + Baseline。

例如，不能把不同 runtime 的同名位宽配置当作完全相同的实验。

也不能拿两个不同 ablation 的倍率直接相减，并据此推断某个组件的独立贡献。

### Step 3.5：建立证据账本

| Claim  | Model | Baseline | Metric | Workload | Result | Evidence |
| ------ | ----- | -------- | ------ | -------- | ------ | -------- |
| 主效果    | 对应模型  | 对应参照     | 主指标    | 固定条件     | 实际数值   | 结果文件     |
| 局部设计有效 | 对应模型  | 结构控制     | 质量指标   | 同预算      | 实际数值   | 消融       |
| 系统设计有效 | 对应模型  | 运行时控制    | 时间/内存  | 同配置      | 实际数值   | 系统消融     |
| 扩展能力   | 多个模型  | 对应参照     | 对应指标   | 扩展条件     | 实际数值   | 扩展结果     |

### Step 3.6：按完成状态处理实验

| 状态         | 写作处理           |
| ---------- | -------------- |
| 已完成并核对     | 直接用于论文         |
| 已完成、等待最终验证 | 在内部标记核对事项      |
| 正在运行       | 留出结果和分析位置      |
| 已设计尚未运行    | 根据主张的重要性决定是否需要 |
| 当前无法获得     | 不填造数字，也不声称已经完成 |

### Phase 3 完成标准

所有进入论文的关键数值，都有确定的来源、单位、比较条件和对应方法版本。

## Phase 4：相关工作调研和 Novelty 判断

### Step 4.1：先判断技术谱系

根据当前方法的本质分类，例如：

- 决策粒度。
- 优化或评分依据。
- 模型训练、离线校准、在线适配。
- 数据表示与压缩。
- GPU execution。
- 存储与缓存。
- 任务相关的能力保持。
- 系统与算法协同设计。

根据这些维度寻找最接近的论文，而不是只按照标题关键词搜索。

### Step 4.2：对最近邻逐项比较

| 比较维度                  | Prior Work | Current Method |
| --------------------- | ---------- | -------------- |
| Research objective    | 对方的实际目标    | 本文目标           |
| Decision unit         | 对方的选择单位    | 当前选择单位         |
| Sensitivity/criterion | 对方的依据      | 本文依据           |
| Representation        | 对方保存什么     | 本文保存什么         |
| Execution             | 对方怎样计算     | 本文怎样计算         |
| Budget/constraint     | 对方约束什么     | 本文约束什么         |
| Evaluation            | 对方证据范围     | 本文证据范围         |
| Main distinction      | 两者实际不同的行为  | 不同如何产生价值       |

### Step 4.3：排除错误的首次性主张

某项组件可能已经存在于先前研究中。

例如已经使用过的：

- Fisher weighting。
- Local candidate substitution。
- Hardware-aligned blocks。
- Mixed precision。
- Model-wide allocation。
- Quantization-aware execution。

这些概念本身不能自动成为当前论文的 novelty。

真正的新意可能在于：

它们围绕一个尚未解决好的研究目标，形成了怎样具体的新决策关系、表示关系或执行关系。

### Step 4.4：将 Distinction 写成具体行为

避免只写：

> Our method is more flexible and hardware friendly.

需要说清：

- 哪个对象可以独立选择？
- 哪些对象共享选择？
- 什么时候决定？
- 决策结果怎样表示？
- 执行时怎样读取？
- 哪些实际能力因此改变？

### Phase 4 完成标准

能够不依靠“首次提出”“尚未探索”等笼统句子，清楚说明当前工作相对于最接近研究的具体增量。

## Phase 5：构建研究问题、Research Gap、Insight 与 Contributions

这是整篇论文最关键的决策阶段。

### Step 5.1：先提出两三个候选 Framing

对每个候选填写：

```
Application setting:
Important objective:
What creates the difficulty:
Observed phenomenon:
Core insight:
Key design:
Main expected benefit:
Existing evidence:
Closest prior work:
```

比较这些候选：

- 哪个问题真正重要？
- 哪个有最强实验支持？
- 哪个最符合当前实际实现？
- 哪个具有可辨识的学术增量？
- 哪个最容易让目标会议的读者理解？
- 哪个能够连接现有多个技术组件？

然后选择一条主要主线，而不是同时使用几个互相竞争的故事。

### Step 5.2：写出 Research Gap

构建过程是：

实际目标 → 已有设计方式 → 具体结构约束 → 对目标的影响 → 新设计机会。

好的 Research Gap 让读者自然产生：

> 原来这里确实存在一个值得解决的问题。

它需要真实困难和后果。单纯指出“其他工作没用过我们这种组合”，仍然不足以解释研究的必要性。

### Step 5.3：形成核心 Insight

Insight 应当是一项能被普通语言表达的研究认识。

不要只把它写成：

- 我们使用一种新模块。
- 我们设计一个评分函数。
- 我们实现两种 kernel。
- 我们选择新的参数。

要再问：

为什么这些选择使原来受到约束的能力能够实现？

### Step 5.4：确定 Difficulties

通常先考虑两个到三个主要 difficulties。

每项包含：

1. 困难产生于哪个实际条件？
2. 为什么会影响研究目标？
3. 解决它需要什么能力？
4. 本文哪项技术具体处理这个困难？
5. 哪项证据表明问题得到处理？

这些 difficulties 最好相互联系，最终共同引出完整方法。

### Step 5.5：确定 Contributions

通常优先使用两到四项，职责清楚且互不重复。

可以从下列层次选择：

- 核心设计或表示。
- 决策与优化规则。
- 数值或计算机制。
- 实际系统实现。
- 独立有价值的理论或实证发现。
- 数据或评测资源。

对每项写：

```
Contribution:
What is introduced:
What capability it provides:
Why it matters:
Method section:
Supporting experiment:
```

### Step 5.6：确定统一术语

对每个核心概念固定名称。

优先使用领域常见词语，避免凭空增加：

`contract`、`artifact`、`native`、`risk`、`frontier` 等抽象包装。

这些词在确有准确技术含义时可以使用；本次 AlignQuant 后期的教训是，反复制造抽象名称容易遮盖真正具体的设计。

### Phase 5 完成标准

完成一页内部研究定位，能够说明：

Problem → Gap → Insight → Difficulties → Method → Contributions → Results。

其中每个箭头都有真实逻辑。

## Phase 6：建立 Contribution–Experiment 闭环

### Step 6.1：逐项建立支持关系

| Contribution | Method | Primary evidence | Control         | Expected conclusion |
| ------------ | ------ | ---------------- | --------------- | ------------------- |
| C1           | 对应机制   | 主效果              | 对应结构对照          | 该设计产生何种能力           |
| C2           | 对应决策规则 | 质量或功能实验          | 评分/决策消融         | 决策为什么有效             |
| C3           | 对应执行实现 | 完整运行实验           | Runtime control | 实现如何产生收益            |

### Step 6.2：把实验分成不同职责

Main Results 说明完整方法在目标任务中能做什么。

Structural Ablations 检查设计对象或空间自由度的作用。

Scoring/Algorithm Ablations 检查某项算法选择的独立贡献。

Runtime Ablations 检查固定模型之后执行设计的影响。

Robustness 检查校准、输入或参数变化下的实际行为。

Scaling 检查长度、batch、规模或硬件变化下的表现。

### Step 6.3：确定正文实验的呈现顺序

效率是核心贡献的论文，可以优先：

End-to-end Efficiency → Model Quality → Challenging Tasks → Allocation/Runtime Evidence。

模型质量是主贡献的论文，可以优先：

Main Quality → Key Mechanism → Extended Settings → Efficiency/Cost。

### Step 6.4：避免无效实验堆积

每张图、每个表都必须回答：

> 这个结果支持哪项 claim？读者从这里获得什么新的理解？

如果两个表重复支持相同的认识，保留正文中信息更强、更容易理解的一个，另一张进入 Appendix。

### Step 6.5：检查结果的支持范围

要区分：

- 完整方法优于 baseline。
- 某个结构选择优于对照。
- 某个评分机制比替代评分有效。
- 某项执行优化减少了时间。
- 多种组件组合后表现良好。

不同问题需要不同对照。

### Phase 6 完成标准

每项贡献有对应证据，每组核心实验有明确作用，全文结论能够从这些证据中得到。

# 第三部分：正式写作前，完成全文结构设计

## Phase 7：制定逐页、逐节、逐段、逐句的写作计划

这一阶段先决定每部分应该让读者理解什么，再决定写多少字。

不要一开始就打开空白 LaTeX 文档，按照标准章节名称随意填写。那样很容易产生篇幅失衡、重复解释以及前后研究定位不一致的问题。

### Step 7.1：根据会议确定正文篇幅

先确认当年官方规定：

- 正文最大页数。
- 参考文献是否计入。
- Appendix 是否单独提交。
- 单栏还是双栏。
- 正文字号、图表和标题格式。
- 必需声明的位置。
- 补充材料的要求。

然后根据论文类型初步分配正文空间。

对于类似 AlignQuant 的方法与系统共同设计、以经验结果为主要证据的论文，可从以下比例开始：

| Section      | 初始篇幅比例 | 主要职责          |
| ------------ | ------ | ------------- |
| Abstract     | 约 5%   | 问题、方法、主要结果、认识 |
| Introduction | 约 15%  | 建立研究动机与完整主线   |
| Related Work | 约 8%   | 说明研究位置与区别     |
| Method       | 约 30%  | 解释核心算法、表示和执行  |
| Experiments  | 约 39%  | 提供决定性证据       |
| Conclusion   | 约 3%   | 回答问题与提炼启发     |

这只是初始规划。理论论文、数据集论文、模型结构论文和系统论文应当分别调整。

篇幅分配应该包含图表占用。 一张大表可能占据半页以上，不能只按照英文词数规划。

### Step 7.2：先为每个 Section 定义职责

在写作前，用一句话规定每节的目标。

| Section      | 读者阅读后应该知道什么           |
| ------------ | --------------------- |
| Abstract     | 这项研究为什么值得看，主要方法和结果是什么 |
| Introduction | 研究问题为何重要，困难在哪里，本文怎样解决 |
| Related Work | 当前方法在领域中的位置，与最近邻有什么区别 |
| Method       | 方法如何运作，每项设计为什么需要      |
| Experiments  | 哪些证据支持方法及其学术价值        |
| Conclusion   | 最终得到什么研究认识            |
| Appendix     | 怎样查阅完整方法、协议、推导与结果     |

### Step 7.3：确定每段承担的工作

建议在开始写之前，先形成这样的段落计划：

```
Section:
Paragraph:
Target length:

这一段的主要目标：
读者此前已经知道什么：
这一段需要新增什么认识：

Sentence 1:
Sentence 2:
Sentence 3:
Sentence 4:
Sentence 5:

对应的 Figure/Table：
需要引用的相关工作：
需要引入的数学对象：
应该放到 Appendix 的细节：
下一段怎样承接：
```

每段的职责应当不同。

例如，一段负责介绍研究需求，下一段负责建立已有设计之间的关系，第三段引出新 insight。不能三个段落都换着语言重复“我们的设计兼顾质量和效率”。

### Step 7.4：规划信息首次出现的位置

对每个新概念，确定：

1. 第一次出现在哪里？
2. 此时读者是否已经具备理解它的知识？
3. 是否需要先给普通语言解释？
4. 什么时候才需要数学定义？
5. 哪个位置进一步解释实现？
6. 是否有必要在 Figure caption 中重复？
7. Appendix 应当补充哪些精确定义？

例如，Introduction 可以先介绍“两个推理阶段使用同一份模型”，再引出联合校准的必要性。

如果一开始直接出现 `joint prefill/decode calibration`，但读者尚未理解为什么两个阶段需要共同决定权重精度，就增加了理解负担。

### Step 7.5：检查信息密度

对每段问三个问题：

信息是否太多？ 如果同时出现十个新对象、三个公式、若干实现细节，需要重新拆分。

信息是否重复？ 如果只是换词重复此前解释，应当删除或合并。

解释是否足够？ 如果删到读者需要猜测公式作用、符号含义或设计原因，就压缩过度。

### Phase 7 完成标准

正式写作前，应该已经有一份从 Abstract 到 Conclusion 的段落级 Blueprint。

每段的主题、必要内容、公式、图表、实验和 Appendix 指向都明确。

## Phase 8：先规划 Figure 和 Table，再写对应段落

图表应该成为论文论证的一部分。

### Step 8.1：设计 Figure 1

Figure 1 的核心任务是让读者看见：

研究问题为什么值得解决，或者本文发现了什么值得解释的规律。

可以选择以下形式：

- 真实实验观察。
- 性能或质量与某个设计变量之间的关系。
- 研究对象内部的分布规律。
- 一项影响设计选择的现象。
- 概念示意与实际结果组合。
- 不同结构选择的示意比较。

不要求 Figure 1 必须比较别人的方法。

如果已有实验结果能很好地展示研究需要，直接展示结果可能更有说服力。

### Step 8.2：设计 Figure 2，即方法总图

建议沿一个稳定对象解释完整方法：

Input → Preparation → Decision → Selected Representation → Execution → Output。

检查：

- 每个箭头表示真实的数据或决策关系。
- 离线和在线阶段区分清楚。
- 关键变量名称与正文一致。
- 不同计算分支实际怎样汇合。
- 对共享状态的表示符合代码。
- 图中步骤与 Method 顺序一致。
- 关键设计突出，普通实现操作适度弱化。

总图应当让读者更容易理解 Method，不能把代码仓库里的所有函数都画成同级模块。

### Step 8.3：设计辅助机制图

只在能增加独立信息时加入。

例如：

- Data Movement。
- Memory Layout。
- Kernel Execution。
- Routing/Allocation Map。
- Numerical Perturbation。
- Sensitivity Distribution。
- Model Architecture。
- Error Behavior。

如果总体方法图已经解释充分，辅助图可以放 Appendix。

### Step 8.4：优先设计 Main Results

主结果表必须让人直接看到：

- 对应模型。
- 方法和 baseline。
- Metric 与方向。
- 单位。
- 最重要的数值。
- 明确的比较条件。
- 是否采用相同预算、资源或运行设置。

正文图表强调最强而有代表性的结果。完整模型、任务、长度或硬件矩阵可以放进 Appendix。

### Step 8.5：设计 Ablation Figures

每个消融都明确：

```
Hypothesis:
Changed factor:
Fixed factors:
Metric:
Expected observation:
Scientific conclusion:
```

一个图表尽量回答一个主要研究问题。

### Step 8.6：先写 Caption 草稿

图注需要具备独立阅读能力。

应当包含：

- 这是什么图。
- 各坐标或 panel 表示什么。
- 使用哪个模型、任务或硬件。
- 指标如何解释。
- 哪个方向更好。
- 必要的对照或参考值。

例如，`generation throughput` 和 `generation-throughput speedup relative to BF16` 是不同指标，不能混用。

### Step 8.7：检查最终视觉效果

不要只看绘图代码或 PDF 文件路径。

需要实际查看：

- 图内字体是否足够大。
- 多 panel 图是否易读。
- Figure 1 能否在正常页面大小下阅读。
- 图例是否遮挡数据。
- 色彩是否区分清楚。
- 轴名与 caption 是否一致。
- 示意图是否与真实实现一致。
- 表格加粗、颜色和箭头是否正确。

### Phase 8 完成标准

每张图表都拥有明确的研究问题、真实数据来源、内容设计、caption 和正文引用位置。

# 第四部分：开始写完整论文

## Phase 9：完成第一版全文

### Step 9.1：先建立实际投稿结构

在真正需要生成论文工程时，使用目标会议的官方模板。

确认：

- 主 LaTeX 入口。
- 会议 style 和必要宏文件。
- Bibliography。
- Figures。
- Appendix。
- 作者匿名模式。
- References 样式。
- 必要声明。

当前只整理流程，因此不创建这些文件。

### Step 9.2：推荐的写作顺序

| 顺序 | 写作内容               | 为什么            |
| -- | ------------------ | -------------- |
| 1  | Method             | 技术事实最确定        |
| 2  | Experimental Setup | 固定比较条件         |
| 3  | Main Experiments   | 明确实际支持什么       |
| 4  | Appendix           | 固定技术细节和结果口径    |
| 5  | Related Work       | 此时能够准确确定方法区别   |
| 6  | Introduction       | 由已确定的方法和证据形成主线 |
| 7  | Abstract           | 最后压缩为准确的整体叙事   |
| 8  | Conclusion         | 用已有证据回答研究问题    |

可以在正式写作最初先写一个工作版 Abstract，帮助检查故事是否清楚。

但最终 Abstract 应在 Method 和实验已经稳定后定稿。

### Step 9.3：完成整个 Section，再进行跨节修改

例如写 Method 时：

1. 先完成 Overview。
2. 完成所有核心 Subsections。
3. 补齐必须的公式。
4. 完成图表引用。
5. 检查符号一致。
6. 对应 Appendix 的位置。
7. 将整个 Method 从头读到尾。
8. 修正本节内部的重复和衔接。

随后进入 Experiments。

不要每写一句就重新审查整篇研究定位，否则容易导致大量低效率迭代。

### Step 9.4：已完成内容直接写完整

只要仓库和实验资料足够，就直接写出完整正文。

不要交付：

- 只有 Section 标题的框架。
- 充满 TODO 的半成品。
- 只有 Introduction 而其他部分空白。
- 一组看似完善但没有形成连续正文的 bullets。
- 与真实代码无关的通用 Method 模板。

尚无数据的位置可以暂时保留占位，但已有的数据应当被实际读取和使用。

### Step 9.5：完成第一轮全文一致性检查

完整初稿出现以后，马上检查：

- Abstract 和 Introduction 是否描述同一问题。
- Contributions 是否在 Method 中逐项得到回应。
- Method 中的技术机制是否在实验中有对应证据。
- 实验结果是否支持 Introduction 的主张。
- Conclusion 是否超出实际结果范围。
- Appendix 是否包含正文承诺的详细内容。

### Phase 9 完成标准

第一版已经是一篇可以从头到尾阅读的完整论文，而不只是各章节内容的集合。

# 第五部分：每个 Section 的具体写作方法

## Phase 10：逐节精写

### 10.1 Title

#### 目标

读者看到标题就知道：

研究对象 + 主要技术特点 + 应用或目标。

#### 详细步骤

1. 识别论文最主要的研究对象。
2. 确定最值得强调的具体设计。
3. 判断标题是否需要方法名。
4. 判断任务或应用是否应该直接出现。
5. 删除泛化但没有具体意义的修饰词。
6. 查询是否已有相同或过于相近的方法名称。
7. 检查标题是否与 Abstract 的主要贡献一致。

例如，`Unified`、`Native`、`Efficient` 可以使用，但需要有具体技术含义；不要连续堆叠。

建议先生成三到五个候选，再选择一个作为全文固定名称。

### 10.2 Abstract

#### 推荐长度

默认一段，8–10 句，约 180–230 个英文词，根据会议要求调整。

#### 推荐职责

| 句子 | 功能              | 读者应得到的信息         |
| -- | --------------- | ---------------- |
| A1 | 引出实际问题          | 研究什么、为什么重要       |
| A2 | 解释结构性困难         | 现有关系如何限制目标       |
| A3 | 提出方法            | 方法身份和关键解法        |
| A4 | 解释主要 insight    | 设计提供什么能力         |
| A5 | 第一机制            | 如何决定或估计          |
| A6 | 第二机制            | 如何满足其他要求         |
| A7 | 表示与执行           | 方法怎样成为实际可用的系统或模型 |
| A8 | Main Results    | 最有说服力的结果         |
| A9 | General Insight | 读者应该记住什么         |

#### 具体写作要求

第一句直接进入具体领域问题。

不要用几句话讨论 AI 的发展、LLM 的普及或技术的重要性，除非这些事实确实构成研究问题。

第二句应当指出有实际后果的困难。

方法出现以后，立即说明它最重要的设计变化，而不是一连串细节操作。

具体数字与精度配置只在必要位置出现。一个参数反复出现，会让读者把参数本身误认为研究贡献。

Method 中可以详细解释 INT4、INT8、激活位宽、尺度及其他设置。Abstract 更重要的是说明这些设计满足了什么共同要求。

#### 结果句怎么写

通常包含：

方法 + 最主要的指标 + baseline + 结果 + 必要范围。

例如：

```
Across the evaluated models, \modelname improves generation efficiency while preserving predictive quality under the tested storage budget.
```

如果加入具体数字，必须明确比较对象与指标。

尤其注意：

- Perplexity 越低通常越好。
- PPL difference 与 PPL percentage difference 不同。
- TPOT speedup 与 throughput ratio 不同。
- 仅测过某几个硬件，不应写成所有硬件。
- 最大值对应某个具体设置。

#### 最后一句怎么写

不要再次压缩整个方法流程。

应提炼：

> 这些结果说明了怎样的设计关系，能对领域内其他工作产生什么启发？

### 10.3 Introduction

建议先按照五段规划，再自然写成连贯正文。

#### Paragraph 1：重要问题与研究目标

推荐 4–5 句。

- S1：说明具体场景以及实际需求。
- S2：介绍当前相关技术为何重要。
- S3：说明常见解决路线。
- S4：引入更细的需求或自由度。
- S5：明确它与实际目标之间的冲突。

这段读完，读者应当知道：

为什么这个问题值得研究。

#### Paragraph 2：相关工作与核心 Research Question

推荐 5–6 句。

- S1：引出 Figure 1 或重要观察。
- S2：介绍第一类相关设计。
- S3：介绍第二类相关设计。
- S4：介绍系统或其他相关设计。
- S5：说明这些设计需要协调什么具体要求。
- S6：提出核心 Research Question。

注意已有方法的描述要准确。

这里默认按方法类别组织，不必把一长串论文逐个点名。

这段读完，读者应当理解：

为什么需要研究当前提出的问题。

#### Paragraph 3：Inspiration、Insight 与 Difficulties

推荐 5–7 句。

- S1：直接给出关键 Insight。
- S2：解释它带来的实际能力。
- S3：提供一项真实观察或研究发现。
- S4：说明将该 insight 落实还需要满足什么条件。
- S5：第一个 Difficulty。
- S6：第二个 Difficulty。
- S7：必要时解释两个 Difficulties 的关联。

这一段非常重要。

Insight 应当先于复杂 Method。

通过真实观察让读者看到为什么想到这个设计，再解释实际实现还面临哪些挑战。

困难要来自研究问题，而不是把每个实现模块硬说成一个挑战。

#### Paragraph 4：Method Overview

推荐 4–5 句。

- S1：方法名称、方法类型、整体目标。
- S2：如何回应第一个 Difficulty。
- S3：如何回应第二个 Difficulty。
- S4：设计如何形成完整模型或系统。
- S5：必要时说明某个关键执行关系。

这里讲清楚总体思路即可。

详细公式、scale search、kernel 参数、indexing 等留给 Method 和 Appendix。

#### Paragraph 5：Main Results 与意义

推荐 2–3 句。

- S1：最强主要结果。
- S2：质量、资源、扩展范围的互补证据。
- S3：这些证据支持什么研究认识。

避免结果段只列“我们做了哪些 Benchmark”。

#### Contributions

默认两到四项，每项一至两句。

每项应具有平行职责，例如：

| Contribution | 回答的问题               |
| ------------ | ------------------- |
| C1           | 引入了什么核心设计或结构？       |
| C2           | 通过什么机制完成关键决策？       |
| C3           | 如何将设计实现成具有实际能力的系统？  |
| C4，可选        | 是否提供独立重要的理论、资源或新发现？ |

Contributions 应与 Method 和 Experiments 对应。

### 10.4 Related Work

#### 推荐长度

三到四个主题段，每段约四到六句。

#### 第一阶段：确定分类

分类应当来自当前研究的真实技术维度，而不是按照随意的时间线逐篇介绍。

例如：

- Algorithmic Allocation。
- Numerical Representation。
- GPU Execution。
- Training or Calibration。
- Application-specific Methods。

#### 第二阶段：为每段确定写作顺序

推荐：

研究方向 → 代表性设计 → 主要选择 → 更具体的相邻方向 → 与当前问题的关系。

#### 第三阶段：写出真正区别

不要反复使用：

```
A improves X but introduces Y.
B improves X but suffers from Z.
C improves X but remains limited by W.
```

这种结构容易让 Related Work 看起来像为了证明本文优越而预先设置的批评。

应当直接解释各方法使用什么决策单位、表示或计算机制。

#### 第四阶段：控制引用密度

引用需要足够覆盖当前最相关的领域工作。

但引用越多并不意味着 Related Work 越好。

每项引用应当准确支持所在句子，而不是把十几个引用机械堆在一条过于宽泛的分类后面。

#### 第五阶段：检查与 Introduction 的分工

Introduction 通过必要文献建立问题。

Related Work 更完整地定位相关方法及本文区别。

两节可以共享重要引用，但不要共享整段同义内容。

### 10.5 Method

Method 是研究事实最集中的部分。

#### Method Opening

通常三到五句：

1. 当前方法处理的对象。
2. 整体设计原则。
3. 输入与输出。
4. 最重要的决策或计算阶段。
5. Figure 2 展示完整过程。

#### 每个 Subsection 的内部顺序

Objective → Definitions → Mechanism → Explanation → Output。

具体展开如下。

第一步：解释本节目的。

读者应该知道这一步为什么存在。

第二步：定义必要对象。

优先使用领域常见符号，例如 \\(X,W,Y\\)。只有数学上确实需要区分的对象才引入新变量。

第三步：介绍机制。

说明从输入到输出的操作关系。

第四步：必要时给出公式。

公式前应当说明它将计算什么。

公式后解释每个关键项在当前研究中的意义。

第五步：说明机制的实际作用。

例如它怎样决定后面的选择，或怎样改善数据表示和计算。

第六步：连接下一节。

说明当前步骤的产物如何被后续使用。

#### Method 中公式的取舍

正文保留：

- 核心决策。
- 关键变换。
- 真正使用的评分。
- 优化目标。
- 必要的约束与重要性质。

Appendix 保留：

- 完整推导。
- Scale 搜索。
- 数值边界。
- 证明细节。
- Indexing。
- Tie handling。
- Padding。
- 具体 kernel geometry。

#### 关于符号

此前我们反复遇到一个问题：为了写得形式化，不断新增 \\(U,V,R,S,z,b\\) 等符号，会让读者需要跳回前面查找。

以后只要自然语言清楚、符号并非后续推导必需，就优先使用普通语言。

数学复杂度应当由研究本身决定。

#### 关于系统执行

每段说明：

Workload → Execution Design → Data Movement → Result。

例如：

- 一个阶段为什么能够复用权重？
- 另一个阶段为什么需要另一种并行组织？
- 数据什么时候被压缩？
- 什么时候被读取？
- 哪一步扩展或重构？
- 使用了哪种实际算术路径？

不能把代码中普通的格式转换包装成新的数学贡献。

#### 关于粗体

已有：

```
\paragraph{Decode parallelism.}
```

就不再在段首添加一个同级的粗体伪标题。

正文每段最多突出少量真正值得记住的设计机制或结论。

### 10.6 Experiments

#### Experimental Setup

简洁说明：

1. 研究评价目标。
2. Models。
3. Datasets 与 Metrics。
4. 默认 Configuration。
5. External Baselines。
6. Internal Controls。
7. Hardware。
8. Measurement。
9. Appendix protocol 指向。

正文重点解释实验设计。

例如“为什么测试长上下文”“为什么使用结构控制”是值得说明的。

具体 seed、metric key、版本、采样参数、完整计时协议通常适合 Appendix。

#### 主结果分析

每段可以按：

Evaluation Goal → Observed Trend → Comparison → Interpretation → Insight。

例如：

1. 为什么评价当前任务？
2. 哪个现象最值得注意？
3. 与哪个 baseline 相比？
4. 哪些数字支持观察？
5. 这一结果与方法哪个设计有关？
6. 读者从结果中学到什么？

#### 控制实验

每个 Ablation 应说明：

- 改变哪个因素。
- 其他条件怎样保持。
- 为什么选择这个对照。
- 结果如何变化。
- 它支持哪个机制。

如果数据只是观察性关系，解释也应保持观察性。

#### 实验叙事需要层层推进

例如一篇质量与效率共同重要的论文，可以组织：

基本质量 → 高难度任务 → 局部选择价值 → 运行效率 → 扩展范围。

如果效率是论文最强卖点，也可以把效率放在前面。

顺序由主要研究价值决定。

#### 具体结果句的要求

每个结果至少明确：

模型、指标、对照、条件、结果。

不需要每句话都重复所有配置；前文已经建立的上下文可以正常继承。

#### Appendix 实验分析

Appendix 中的实验也必须解释趋势和设计意义。

不能因为它放在附录，就只放一张大表而完全不分析。

但正文不需要重新讨论附录每一行。

### 10.7 Conclusion

建议一个段落，三到四句。

- 第一句回答全文研究问题。
- 第二句总结主要设计怎样实现相关能力。
- 第三句概括有证据的结果及其意义。
- 最后一句提炼可迁移的认识。

未来工作只有在自然衔接时才需要提。

避免机械重复 Abstract，也避免把所有贡献重新列举一次。

### Phase 10 完成标准

每个 Section 都具备完整职责，整体故事顺畅，并且能够独立解释其必要内容。

# 第六部分：Appendix、引用与可复现性

## Phase 11：设计和撰写完整 Appendix

Appendix 的目的既包括详细复现，也包括为正文提供更深入的机制与结果解释。

不需要为每种内容都创建一个 Section，但以下类别应当有清楚位置。

### A. Notation and Reading Guide

包含：

- 核心符号。
- 数学对象。
- 维度。
- 符号之间的关系。
- Appendix 导航。

符号表便于查阅，不能替代正文的首次解释。

### B. Numerical / Algorithmic Construction

包含：

- 具体数值构造。
- 候选生成。
- 参数、搜索范围。
- 数据转换。
- 数值精度。
- 边界处理。
- 实际实现中的特殊条件。

### C. Calibration / Training Details

包含：

- 数据集来源。
- 数据划分。
- 采样规则。
- 样本构造。
- 模型状态。
- 损失。
- 梯度。
- 观测位置。
- 阶段差异。
- 随机种子或确定性规则。

### D. Mathematical Derivations

包含：

- 正文公式的详细推导。
- 关键等价性。
- 优化条件。
- 定理或性质。
- 证明所需假设。
- 端点和 tie handling。

证明只能支持其真正证明的数学对象。

例如，一个固定评分的排序规则成立，不等于整个神经网络真实 loss 的全局最优性得到证明。

### E. Representation and Execution

适合系统研究：

- Memory layout。
- Serialized representation。
- Metadata。
- Indexing。
- Kernel geometry。
- Data movement。
- Thread/block mapping。
- Scheduling。
- Temporary buffer。
- Resource accounting。

### F. Design Rationale

解释为什么采用某个重要的设计选择。

需要区分：

- 数值质量方面的理由。
- 计算和访存方面的理由。
- 工程适配方面的理由。
- 实际消融支持的理由。

### G. Experimental Protocols

这是保证实验可解释和可复现的重要部分。

至少整理：

- 精确模型版本。
- Dataset 与 split。
- Benchmark 任务及指标字段。
- Prompt/shot 设置。
- Calibration。
- Baseline backend。
- 关键共享 runtime 条件。
- Batch 与 sequence length。
- Warmup 和 repetitions。
- 统计方法。
- 存储与能耗定义。
- Random seed。
- 不同实验组之间的实际区别。

### H. Additional Results and Analysis

包含：

- 其他模型。
- 其他任务。
- 更长的上下文。
- 不同硬件。
- 完整消融。
- 参数与数据量变化。
- 稳定性。
- 内存和效率变化。
- 局部行为分析。

每个结果属于哪个小节，就在该小节进行相应解释。

### Appendix 专项检查

尤其注意四个问题。

第一，正文用到的 control 都已定义。 `Output-row`、`Red.-col`、`Proj./layer` 和 `Random` 这种表头，需要解释真实选择范围和约束。

第二，默认配置和特殊实验明确区分。 例如默认 calibration 和 calibration-size robustness 可能使用不同的采样记录。

第三，协议与已确认设置一致。 如果作者已经确认所有方法共享 evaluator、metric field 和关键 runtime 条件，用标准协议语言清楚说明即可。

第四，所有 Appendix pointers 真实有效。 正文承诺在某个 Appendix 解释的内容，确实应该出现在那个位置。

### Phase 11 完成标准

读者可以通过 Appendix 还原研究方法、理解所有控制实验及完整结果，不需要反复询问作者“这张表到底代表什么”。

## Phase 12：Bibliography、术语和 LaTeX 一致性

### Step 12.1：所有引用都建立在真实文献上

检查：

- Title。
- Authors。
- Publication year。
- Venue。
- Pages。
- DOI。
- arXiv ID。
- 正式版本与预印本区别。

不要随意编造 BibTeX key 对应的元数据。

### Step 12.2：区分引用的学术职责

不同 citation 可能用于：

- 介绍研究背景。
- 支持某个已有方法的设计。
- 说明使用某项技术。
- 介绍 Benchmark。
- 引用数据集。
- 解释某个硬件或算法基础。
- 对比最近邻工作。

不能仅因为标题相关，就把引用放在一条无法支持的宽泛陈述后。

### Step 12.3：建立术语表

固定：

```
Concept:
Preferred English Term:
First Definition:
Symbol:
Related Terms:
Disallowed Alternatives:
```

避免同一对象反复被称为 `policy`、`state`、`map`、`artifact`，让读者误以为这些是不同对象。

### Step 12.4：检查 LaTeX 宏与交叉引用

必须核查：

- `\label`。
- `\ref`。
- `\eqref`。
- `\citep`。
- Figure/Table caption。
- 宏命令。
- `\begin` / `\end`。
- 表格列数。
- 公式编号。
- Bibliography style。

特别注意目标模板可能重新定义 `\eqref` 等常见命令。

先查看实际定义，再决定怎样修正。

### Phase 12 完成标准

所有引用和编号均有明确对应，文献元数据正确，全文术语稳定。

# 第七部分：写完以后，如何科学地修改

## Phase 13：六轮系统性修改

修改顺序必须从研究与结构开始，最后才是遣词造句。

如果论文的 gap、contributions 或实验归因仍然有问题，先做同义词替换只会浪费大量时间。

## Round 1：Scientific Validity

逐项检查：

- 论文描述与代码实现一致吗？
- 当前方法与历史实现区分了吗？
- 评分、优化与真实输出的关系准确吗？
- 数学公式与对应文字一致吗？
- 离线、在线、训练、校准与推理阶段清楚吗？
- 系统实际运行路径完整吗？
- 报告的最高结果有正确适用范围吗？
- 所有数字与最终结果一致吗？

### 完成标准

论文没有实质性技术错误、跨配置混用或 unsupported claims。

## Round 2：Research Story

从头阅读：

Abstract → Introduction → Contributions → Method → Experiments → Conclusion。

检查：

- 是否始终围绕同一个研究问题？
- Research Gap 是否真实？
- Difficulty 是否从 Gap 自然产生？
- 每项机制是否回应某项 Difficulty？
- 每项 Contribution 是否有区别？
- 实验是否支持相应机制？
- Conclusion 是否回答最初问题？
- 读者能否说出整篇论文的主要认识？

### 完成标准

能够不用方法名和模块列表，用一段普通语言讲清全文研究故事。

## Round 3：Reader-First Clarity

逐段检查：

1. 段落第一句是否有明确作用？
2. 新名词出现时有没有上下文？
3. 有没有隐含但尚未解释的前提？
4. 代词是否能明确指向对应对象？
5. 是否同时出现太多新概念？
6. 公式前有没有目的说明？
7. 公式后有没有直观解释？
8. 为什么做这一步是否清楚？
9. 段尾增加了什么认识？
10. 删除某句是否会失去必要信息？

这里落实“不让读者承担不必要的理解成本”。

### 完成标准

熟悉相邻领域但尚未阅读该仓库的读者，能够顺着正文理解核心设计。

## Round 4：Writing Style / De-AI

这一轮重点检查语言。

### 1. 禁止否定式包装

例如：

```
not A but B
not only A but also B
rather than
instead of
```

尽量改成正向陈述实际设计及作用。

必要的科学否定、数学否定和准确约束保留。

### 2. 禁止句中插入破折号

例如使用 em dash 插入额外解释，应改为：

- 单独句子。
- 明确从句。
- 简洁括号。

正常技术复合词中的连字符保留。

### 3. 减少 AI 式造词

优先具体对象和动作。

例如：

| 抽象用语                     | 更具体的表达       |
| ------------------------ | ------------ |
| Native contract          | 实际共享的表示或决策单位 |
| Immutable artifact       | 实际保存的模型或数据结构 |
| Risk landscape           | 评分或敏感性分布     |
| Operationally meaningful | 对应的可测量作用     |
| Unified execution        | 实际共用的算术或数据路径 |

这些替换需要根据研究事实判断，不是禁止专业术语。

### 4. 控制名词堆叠

连续使用多个形容词或复合名词时，读者必须解码它们之间的关系。

例如一个很长的技术命名，可以拆成：

对象是什么 → 怎样使用 → 为什么需要。

### 5. 自然使用主语

避免连续：

```
We first ...
We then ...
We further ...
We finally ...
```

可以让真实技术对象作为主语。

例如：

```
Calibration produces the scores.
The resulting ranking determines the selected precision.
The packed model stores the selected values.
```

这些句子沿一个对象自然推进，不需要机械连接词。

### 6. 处理重复总结

尤其搜索：

```
Together, these results ...
This demonstrates ...
This highlights ...
This underscores ...
```

它们不是绝对禁止的词组，但不能作为每段的固定收尾。

需要有新的结果解释或实际研究认识。

### 7. 保留有价值的转折

`However` 在真实逻辑转折中非常有用。

例如准确率需求与部署执行之间存在实际冲突时，可以自然使用。

问题不在于某个连接词，而在于整篇论文是不是反复复制同一种句法结构。

### 完成标准

专业、准确、正式、自然，读者能够快速理解句子真正传递的技术信息。

## Round 5：Figures、Tables、References 和版面

重点检查：

- Figure 1 是否突出主要研究认识。
- Figure 2 是否与实际方法一致。
- 图内标签与 caption 一致。
- 图例足够清楚。
- 字体正常阅读时可辨认。
- Table 中数据与说明一致。
- 最优值加粗是否正确。
- 颜色对应指标方向。
- 所有主表在正文被引用。
- Appendix Tables 没有严重跨节漂移。
- 所有 citation keys 都存在。
- 所有 labels 正确。
- 模型名称和 Benchmark 大小写统一。
- 论文符合目标会议格式。

### 完成标准

内容与视觉一致，图表可独立理解，LaTeX 编译结果符合提交要求。

## Round 6：模拟 Reviewer 审查

只关注真正影响论文科学价值的问题。

重点提问：

1. 研究问题是否具有学术意义？
2. Novelty 相对于最近邻是否成立？
3. 方法是否清楚？
4. 核心机制是否有直接证据？
5. 实验比较是否准确且可解释？
6. 系统收益是否具有明确范围？
7. 最主要结论是否由数据支持？
8. 论文给领域带来了什么有价值的认识？

将疑问分类：

| 状态                  | 处理             |
| ------------------- | -------------- |
| Factual Error       | 立即修复           |
| Unsupported Claim   | 调整范围或补证据       |
| Missing Explanation | 增加必要解释         |
| Missing Ablation    | 判断是否影响核心 claim |
| Presentation Issue  | 修改文字或图表        |
| Already Addressed   | 给出已有位置，不重复改    |
| Author Confirmed    | 记录已确认条件        |
| Rejected Suggestion | 保持作者已经确定的选择    |

模拟 reviewer 的判断只是审查工具，不直接等同于真实接收概率。

### Phase 13 完成标准

六轮修改后，剩余问题有明确分类，不再反复出现同一批无效建议。

# 第八部分：逐句修改与作者反馈管理

## Phase 14：精准修改协议

### Step 14.1：只以当前稿件作为原文

每次修改前必须打开最新版本。

不能使用两三轮以前的旧句子冒充当前原文。

### Step 14.2：修改前解释问题

对每个位置说明：

- 为什么需要修改？
- 影响读者理解还是技术准确性？
- 是否与其他章节冲突？
- 修改是否会影响图表或符号？
- 是否可以通过 Appendix 解决？

### Step 14.3：固定输出格式

位置： Section、段落和原文所在位置。

原文

```
The original sentence from the current manuscript.
```

修改后

```
The revised sentence ready to replace the original sentence.
```

修改原因：

解释具体改善点。

原文与修改后必须使用两个独立 code fence。

### Step 14.4：对全文联动进行检查

修改一个术语时，检查：

- Abstract。
- Introduction。
- Method。
- Figure captions。
- Tables。
- Appendix。
- Conclusion。

一个关键概念在全文应当表达同一含义。

### Step 14.5：已经确认的内容保持稳定

建立以下状态：

| 状态           | 含义         |
| ------------ | ---------- |
| Accepted     | 作者确认采用     |
| Applied      | 已实际修改      |
| Rejected     | 作者明确拒绝     |
| Deferred     | 延后处理       |
| Data Pending | 等待最终实验     |
| Verified     | 已通过代码或协议确认 |

后续建议必须遵守这些状态。

### Step 14.6：正文排版锁定模式

当正文已经达到目标页数、排版刚好时：

1. 默认不增加正文篇幅。
2. 优先等长或更短替换。
3. 删除真实冗余后才考虑加入新解释。
4. 配置、seed、控制定义等优先放 Appendix。
5. 避免大规模重构已经稳定的 Section。
6. 保留当前合理的图表布局。
7. 修改后重新查看实际 PDF。

如果某项关键内容确实必须进入正文，应当说明原因和需要调整的空间。

### Step 14.7：如何处理多模型提出的修改建议

把不同意见分为：

- 共同指出的实质问题。
- 真正存在分歧的研究判断。
- 纯粹措辞偏好。
- 新发现的有用写作技巧。
- 依据错误版本得出的建议。

对于重要 framing 变化，由作者决定是否采用。

此前已拒绝的全面重写，不能因为另一个模型再次提出就自动恢复。

### Phase 14 完成标准

用户能够逐项替换文本，知道每个修改解决什么问题，而且后续不会再为相同问题重复解释和拒绝。

# 第九部分：全文最终审计

## Phase 15：三层内容检查加投稿合规检查

### 第一层：LaTeX Source Audit

检查：

- 所有 `\label` 是否唯一。
- 所有 `\ref` 是否有效。
- 所有 `\eqref` 是否符合当前宏定义。
- 所有 citation keys 是否存在。
- 是否有未使用的主要 Figure/Table label。
- `\begin` 和 `\end` 是否匹配。
- 表格列数与 `&` 数量是否一致。
- 图表 caption 与 label 是否放在正确位置。
- 是否有残留 TODO 和错误占位。
- 正文、Appendix 和 References 是否完整。

### 第二层：Scientific Consistency Audit

逐项检查：

Method 与代码

- 当前实际执行路径是否一致？
- 算法步骤是否准确？
- 所有公式是否有正确解释？
- 存储与计算格式是否混淆？
- 逻辑划分与硬件执行单位是否区分？

Experiments 与结果

- 各方法比较条件是否准确？
- 指标方向是否正确？
- 模型及硬件范围是否正确？
- 质量和效率是否对应同一模型配置？
- 各组 control 是否有定义？
- 结果分析是否超出实际证据？

Claims 与全文

- Abstract 的主张是否全部有依据？
- Introduction 中的 Gap 是否由实际设计关系支持？
- Contributions 是否分别有机制与证据？
- Conclusion 是否与 Abstract 对应？
- 有没有同一个词在不同 Section 表示不同对象？

### 第三层：PDF Visual Audit

必须打开实际 PDF，逐页查看。

重点包括：

- 标题页。
- Abstract 换行。
- Figure/Table 是否遮挡。
- Equation 是否超出边界。
- 图表字号。
- 页眉页脚。
- Figure 引用位置。
- 表格跨页。
- Appendix float 顺序。
- References 格式。
- 页面总数。

源码没有报错，不等于排版没有问题。

### 第四层：Submission Compliance Audit

核对：

- 会议与年份正确。
- 页面限制符合要求。
- 模板使用正确。
- 作者匿名。
- 代码链接符合匿名规则。
- 需要的声明准确填写。
- 参考文献和附录位置正确。
- Supplementary 格式正确。
- 投稿截止时间准确。

### Phase 15 完成标准

能够明确给出：

内容完整性、科学一致性、typos、references、图表、PDF 和会议格式的检查结论。

# 第十部分：冻结、提交与 Rebuttal 准备

## Phase 16：投稿前冻结

### Step 16.1：确定唯一最终版本

确保所有作者使用同一份当前稿件。

不允许同时存在几个都被称为 final 的版本，而修改没有同步。

### Step 16.2：固定关键实验来源

对每个重要数字保存对应信息：

- Model revision。
- Method configuration。
- Baseline。
- Dataset。
- Metric。
- Hardware。
- Workload。
- Result。
- Source。
- Statistical procedure。

这样收到 reviewer 的问题后，可以迅速找到原始依据。

### Step 16.3：提前整理关键 Reviewer Questions

按照主题分类：

- Novelty。
- Research Gap。
- Algorithm。
- Numerical behavior。
- Comparison fairness。
- Evaluation consistency。
- Efficiency。
- Runtime attribution。
- Generalization。
- Reproducibility。

每个问题对应已有正文、Appendix 或实验结果的位置。

### Step 16.4：Rebuttal 的基本原则

- 准确回答 reviewer 的具体问题。
- 首先提供已有证据。
- 相关实验有必要时再补充。
- 新实验的结论限定到真实结果范围。
- 保持原论文 claim 与回应一致。
- 重要事实问题不能靠措辞回避。
- 避免用冗长的自我辩护稀释主要证据。
- 所有报告的结果必须真实，遵守会议修改和披露规则。

### Phase 16 完成标准

论文及实验来源可以追溯；收到审稿意见时，能够快速定位相关证据。

# 第十一部分：如何安排时间并减少返工

## Phase 17：倒排时间计划

下面是一个完整论文写作周期的参考安排，应根据实际截止日期和当前实验进度调整。

| 距投稿时间    | 工作重点                                         | 完成标准            |
| -------- | -------------------------------------------- | --------------- |
| 4 周或更早   | 会议、代码、实验和最近邻调研                               | 核心事实清楚          |
| 3 周      | Framing、contributions、证据关系、图表规划              | 全文 Blueprint 确定 |
| 2–3 周    | Method、Experiments、Appendix 完整起草             | 第一版正文完整         |
| 1–2 周    | Intro、Related Work、Abstract、Conclusion，合作者反馈 | 主线稳定            |
| 最后 7 天   | 科学性、可读性、图表、References、Appendix               | 进入局部修改          |
| 最后 2–3 天 | 全文审计、PDF 排版、投稿要求                             | 终稿准备完成          |
| 提交前      | 最终编译与提交状态核对                                  | 唯一最终版本          |

### 哪些工作可以并行？

会议调研和代码审计可以同时推进。

实验正在运行时，Method、Related Work 和 Appendix 中已确认的内容可以继续写。

图表制作与实验结果核对可以相互配合。

### 哪些工作应当有先后顺序？

Novely 判断需要了解最近邻工作。

Introduction 的最终 framing需要准确理解 Method 和结果。

Abstract 的最终数值需要来自最终实验。

Final Audit应当在全文整合之后执行。

### 每个阶段都需要设置完成标准

如果某阶段已经满足条件，就进入下一阶段。

不能因为仍然存在一些可以继续润色的句子，就无限停留在当前 Section。

# 第十二部分：完整写作的验收清单

这是最后检查整篇论文是否达到目标时使用的清单。

终稿验收进度

0/25

研究问题与定位

实际研究问题明确且重要

Research gap 有真实约束与实际后果

核心 insight 可以用普通语言解释

与最近邻的区别有具体技术依据

每项 contribution 有独立职责

Method

当前生效代码路径已核对

核心机制和数据流完整

符号数量经过控制

必要公式均有作用解释

方法与 Appendix 技术定义一致

Experiments

主结果有准确的比较条件

每个核心 claim 对应证据

结构与评分消融各有明确作用

运行时归因与比较对象一致

扩展实验能够说明适用范围

写作与读者理解

摘要能独立表达整项研究

引言各段都有信息推进

Related Work 分类真实且没有模板式批评

正文避免防御式、否定式包装和插入破折号

结论给出可迁移的研究认识

Appendix 与提交

所有控制实验都有定义

实验协议和引用完整

引用编号与术语一致

实际 PDF 逐页检查

满足会议当年的提交政策

重置检查

# 第十三部分：下一篇论文直接使用的完整 Prompt

## Phase 18：最小输入、全流程自动推进

只需将实际仓库与会议名称填进去。

复制以下完整写作指令

&#x20;复制

下方是精简执行版，适合每次启动一个新项目。

```
请根据我提供的代码仓库和目标会议，完成从研究理解到完整投稿论文的全部工作。

Repository: [URL / branch / commit / ZIP]
Target Conference: [会议名称 + 年份]

要求：

1. 先核查会议当年的官方规则、投稿类别、审稿标准、模板与篇幅限制。阅读最近两年最相关的论文，学习其研究定位、叙事、图表和证据组织。

2. 完整阅读当前仓库的实际执行路径、算法、数据、配置、系统实现、实验脚本和结果。区分当前方法、历史方法、消融和计划功能。

3. 客观判断学术价值。识别真正重要的 Problem、Research Gap、核心 Insight、Difficulties、Novelty、Distinctions 和 Contributions。不要从现成的模块名称倒推研究价值。

4. 建立 Claim–Mechanism–Evidence Map。所有重要主张都对应真实方法和结果。明确模型、任务、硬件、指标、baseline、预算及比较条件。

5. 制定全文详细计划。明确每个 Section、每段和关键句子的职责，分配正文与 Appendix 的内容，确定 Figure/Table 的研究问题及出现位置。

6. 完整起草论文，包括 Abstract、Introduction、Related Work、Method、Experiments、Conclusion、Appendix 和 References。不在提纲或零散段落阶段停止。

7. 正文以读者理解为中心，先解释对象和研究需求，再介绍机制与公式。减少多余符号和自造术语，保持领域常用名称与专业性。

8. 写作正向、直接、自然。避免 not…but、rather than、not only 等否定式包装以及句中插入破折号；减少空泛名词、AI式机械衔接和重复总结。

9. 实验部分包含研究问题、具体趋势、代表性比较、设计解释与得到的认识。结果与主张对应，消融与归因严格一致，Appendix 保留完整协议和详细分析。

10. 完整稿之后，依次完成科学性、研究故事、读者理解、语言、图表与引用、模拟审稿六轮检查。

11. 修改时遵守已确定的作者偏好。每项改动给出准确位置、原文独立 code fence、修改后独立 code fence 和原因。正文页数已锁定时不增加正文篇幅，详细补充优先进入 Appendix。

12. 最终检查全文一致性、技术正确性、参考文献、图表、实验数据、typos、LaTeX 和会议投稿要求。

直接推进完整工作，只有遇到真正影响研究定位或事实准确性的必要缺失信息时，才集中询问。
```

# 最后的总验收：六个问题

在提交之前，将整篇论文重新当作第一次阅读，回答：

1. Why： 为什么研究这个问题？
2. What： 本文真正改变了什么？
3. How： 它通过怎样的具体机制实现？
4. Difference： 与最接近工作之间的实质区别是什么？
5. Evidence： 哪些证据支持主要结果和机制？
6. Knowledge： 读者学到了什么能够迁移到其他研究中的认识？

如果前五个问题能够被清楚回答，而第六个问题只能回答“我们的方法效果很好”，就需要重新思考论文最值得强调的 insight。

最终目标是一篇研究问题明确、增量具体、机制易懂、证据完整、文风自然、能让读者获得新认识的论文。 写作流程中的每一步，都应当帮助达到这个目标。