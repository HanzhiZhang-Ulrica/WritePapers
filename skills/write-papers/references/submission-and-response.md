# 终稿冻结、审稿回应与时间安排

## 唯一最终版本

确保所有作者使用同一份当前稿件。

不允许同时存在几个都被称为 final 的版本，而修改没有同步。

## 关键数字与审稿问题的来源

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

## Rebuttal

- 准确回答 reviewer 的具体问题。
- 首先提供已有证据。
- 相关实验有必要时再补充。
- 新实验的结论限定到真实结果范围。
- 保持原论文 claim 与回应一致。
- 重要事实问题不能靠措辞回避。
- 避免用冗长的自我辩护稀释主要证据。
- 所有报告的结果必须真实，遵守会议修改和披露规则。

## 倒排时间与阶段验收

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

Novelty 判断需要了解最近邻工作。

Introduction 的最终 framing需要准确理解 Method 和结果。

Abstract 的最终数值需要来自最终实验。

Final Audit应当在全文整合之后执行。

### 每个阶段都需要设置完成标准

如果某阶段已经满足条件，就进入下一阶段。

不能因为仍然存在一些可以继续润色的句子，就无限停留在当前 Section。
