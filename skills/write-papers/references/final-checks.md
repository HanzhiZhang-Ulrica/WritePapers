# 成稿与投稿检查

## 标题、相关工作与独立阅读

- [ ] Title is specific and matches the actual contribution.
- [ ] Related work covers the most relevant prior methods, datasets, and benchmarks.
- [ ] Symbols, assumptions, and terminology are defined before use.
- [ ] Read the title, abstract, section headings, and captions as a standalone summary.

## 引用检查

**技术检查：** citation key 存在、label 唯一、引用目标有效。

**语义检查：** 引用内容确实支持当前句子，附录指向确实包含所承诺的细节，图表比较与文字相符。

BibTeX 的作者、标题、年份、venue、页码和正式版本要核实。不要凭论文年份构造 volume，也不要自动认定不熟悉的新论文 metadata 有误。

## 实验与技术可靠性

- [ ] Baselines are strong, current, and fairly implemented.
- [ ] Key implementation details, datasets, splits, and hyperparameters are documented.
- [ ] At least one ablation or sensitivity analysis supports the main claims.

## 指标、比较条件与证据边界

PPL、误差、延迟和能耗通常是越低越好；准确率和吞吐通常是越高越好。具体方向以指标定义为准。

`within` 更适合表达一个上界；差值范围使用 `differences of ...`。不能为强调质量保持而把实际上升写成 PPL improvement。

重点检查：

**TPOT speedup 与 throughput ratio；微算子与完整请求；名义位宽与 packed bytes；权重存储与常驻内存；基准长度等级与实际 token 数；单模型多硬件与多模型单硬件。**

一个最高数值要能追溯到明确的比较对象。

- 图内公式、正文公式、算法和实现是否使用同一输入输出约定

- 比较对象、运行范围、指标和 workload 不可混写

- 图上究竟是绝对数值、差值、比值还是归一化倍率

- benchmark 的标称等级与实际执行范围是否分开说明

- 整体效果、评分机制、表示设计和 runtime 收益是否有对应的独立证据

## 语法、拼写与一致性

- [ ] Terminology, notation, capitalization, tense, and voice are consistent.
- [ ] Check spelling, typos, punctuation, commas, articles, and subject-verb agreement.
- [ ] Remove contractions, colloquial phrases, and unsupported adjectives.

## 图表与视觉编码

图注至少让读者理解对象、坐标、比较范围、指标方向和必要条件。复杂 panel 需要说明行、列和 panel 内横轴分别代表什么。

- [ ] Every figure, table, and equation is referenced and explained in the text.

详细分析与对应图表放在同一部分。

对 caption 的修改不仅检查文字信息，还要检查视觉编码有没有被原样保留。

对图表的检查既包括数值，也包括坐标轴、图例、颜色、单位、归一化定义、统计口径与图注。

- [ ] Captions state the takeaway, not only what is shown.
- [ ] Axes, units, legends, and fonts are readable in grayscale and when printed.

## 最终 PDF 与验证范围

- 最终检查必须覆盖真正上传的 PDF

- 公式、坐标轴、caption、图内文字、浮动顺序、参考文献和实际页数

- 应明确区分源码检查、PDF 渲染检查和程序执行验证

- 必须查看最终 PDF，而不能把 LaTeX 编译成功当作最终完成

- [ ] The uploaded PDF opens correctly; links, fonts, metadata, and supplement files are checked.
- [ ] After checking every item, open the exact uploaded PDF once more and verify it matches what you intended to submit.

## 提交文件清理

- [ ] Remove TODO/FIXME notes, tracked changes, comments, and debug text.

## 投稿声明与表单

- [ ] Limitations, failure cases, and ethics/societal impact are addressed if required.

- 投稿政策要落实到具体声明和表单

- 强制 Section、可选 Section、必填表单、声明证据的区别

- 表单问题必须按照原问题的实际语义判断

- 不能把“未写进论文”和“没有完成”混为一谈

- 每项声明究竟在哪里完成，如何通过原文和证据验证

## 双重可读性与逐句检查

论文首先应当让人类读者能够连续理解问题、方法和结论，同时保证结构化评审能够准确提取研究问题、贡献、公式含义、比较条件和支持证据。

主张、证据和适用范围应在局部保持清楚对应。

交付前主动逐句检查“这是谁、为什么此时出现、与谁比较、具体收益是什么、与上一句如何连接、是否推进了新的理解”，把问题解决在正文里，而不是只在分析中解释正确、成稿继续重复同样的错误。

不能仅评价文本是否漂亮，还应当分别检查 novelty、soundness、experimental fairness、reproducibility 和 contribution boundaries。

写作能帮助审稿人理解已有证据，但不能通过改变措辞代替缺失的技术证明。

## 最后五分钟检索

- [ ] TODO / FIXME / XXX / ??
- [ ] doubled words and duplicate spaces
- [ ] missing words
- [ ] self-identifying names, links, or metadata
- [ ] missing citations, broken references, and numbering mismatches

## 最终验收：六个问题

**问题是什么，为什么值得解决？**

**困难来自哪个具体关系？**

**本文改变了什么，这个改变为什么有效？**

**与最接近的已有设计相比，实质增量在哪里？**

**哪些证据支持效果、机制和适用范围？**

**读完之后，我在设计或理解同类方法时，可以采用什么新的判断？**
