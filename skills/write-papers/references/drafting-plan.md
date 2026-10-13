# 全文规划与完整起草

图表未确定时的处理、研究范围与已确认主线，遵守共同要求。

## 段落级 Blueprint

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

对每个新概念，确定：

1. 第一次出现在哪里？
2. 此时读者是否已经具备理解它的知识？
3. 是否需要先给普通语言解释？
4. 什么时候才需要数学定义？
5. 哪个位置进一步解释实现？
6. 是否有必要在 Figure caption 中重复？
7. Appendix 应当补充哪些精确定义？

对每段问三个问题：

信息是否太多？ 如果同时出现十个新对象、三个公式、若干实现细节，需要重新拆分。

信息是否重复？ 如果只是换词重复此前解释，应当删除或合并。

解释是否足够？ 如果删到读者需要猜测公式作用、符号含义或设计原因，就压缩过度。

篇幅分配应该包含图表占用。 一张大表可能占据半页以上，不能只按照英文词数规划。

## 图表职责与消融计划

每张图表都拥有明确的研究问题、真实数据来源、内容设计、caption 和正文引用位置。

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

如果两个表重复支持相同的认识，保留正文中信息更强、更容易理解的一个，另一张进入 Appendix。

## 第一版全文的写作顺序

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

## 完整初稿与缺失结果

只要仓库和实验资料足够，就直接写出完整正文。

不要交付：

- 只有 Section 标题的框架。
- 充满 TODO 的半成品。
- 只有 Introduction 而其他部分空白。
- 一组看似完善但没有形成连续正文的 bullets。
- 与真实代码无关的通用 Method 模板。

尚无数据的位置可以暂时保留占位，但已有的数据应当被实际读取和使用。

完整初稿出现以后，马上检查：

- Abstract 和 Introduction 是否描述同一问题。
- Contributions 是否在 Method 中逐项得到回应。
- Method 中的技术机制是否在实验中有对应证据。
- 实验结果是否支持 Introduction 的主张。
- Conclusion 是否超出实际结果范围。
- Appendix 是否包含正文承诺的详细内容。

第一版已经是一篇可以从头到尾阅读的完整论文，而不只是各章节内容的集合。

## Appendix 的补齐与定位

Appendix 的目的既包括详细复现，也包括为正文提供更深入的机制与结果解释。

不需要为每种内容都创建一个 Section，但以下类别应当有清楚位置。

### Design Rationale

解释为什么采用某个重要的设计选择。

需要区分：

- 数值质量方面的理由。
- 计算和访存方面的理由。
- 工程适配方面的理由。
- 实际消融支持的理由。

### Experimental Protocols

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

默认配置和特殊实验明确区分。 例如默认 calibration 和 calibration-size robustness 可能使用不同的采样记录。

所有 Appendix pointers 真实有效。 正文承诺在某个 Appendix 解释的内容，确实应该出现在那个位置。
