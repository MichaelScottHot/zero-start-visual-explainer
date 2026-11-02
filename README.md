<div align="center">

# 🧭 Zero-Start Visual Explainer

### 从“我没学过”开始，把陌生问题讲到能用。
### Start from zero, follow the steps, and learn how to use what you understand.

![类型 / Type](https://img.shields.io/badge/TYPE-AI%20Skill-7257d5?style=flat-square)
![主题 / Topics](https://img.shields.io/badge/TOPICS-AI%20%2F%20Logic%20%2F%20Tools-3478c8?style=flat-square)
![方法 / Method](https://img.shields.io/badge/METHOD-Step--by--step-159578?style=flat-square)
![语言 / Languages](https://img.shields.io/badge/LANG-中文%20%2F%20English-64748B?style=flat-square)

[查看 Skill 文件 / View the Skill](SKILL.md)

</div>

---

## 目录 / Contents

[它解决什么 / Why it helps](#why-it-helps) · [讲解路径 / How it explains](#how-it-explains) · [使用案例 / Example](#example) · [适合的问题 / Good for](#good-for) · [如何使用 / How to use](#how-to-use) · [文件说明 / Files](#files) · [边界与质量 / Boundaries](#boundaries)

<a id="why-it-helps"></a>
## 它解决什么 / Why it helps

很多解释直接给出结论，却默认读者已经认识一堆术语；有些回答把推理压成几句口诀，让人知道“要做什么”，却不知道每一步为什么成立。

Many explanations jump to the answer and assume you already know the jargon. Others compress the reasoning into a few tips, telling you what to do without showing why each step works.

**Zero-Start Visual Explainer** 从当前问题真正需要的前置知识开始，解释新术语，补全关键推理，并用具体例子展示知识如何用起来。

**Zero-Start Visual Explainer** starts with only the background needed for your question. It explains new terms, fills in the reasoning, and uses a worked example to show how the idea applies.

<a id="how-it-explains"></a>
## 讲解路径 / How it explains

**问题与已知 → 必要前置 → 每一步的理由 → 具体例子 → 可带走的结论**

**Question and givens → needed background → reasons for each step → worked example → takeaway**

| 你提出的问题 / Your question | 讲解会补上的内容 / What the explanation covers |
| --- | --- |
| AI 或陌生概念 / An AI or unfamiliar concept | 日常问题、概念定义、组成关系、运行过程与边界 / Familiar need, plain definition, parts, how it works, and its limits |
| 逻辑或数学题 / A logic or math problem | 已知条件、每一步推导的理由、结果核对 / Givens, the reason for each deduction, and a consistency check |
| 工具或工作流 / A tool or workflow | 前提、实际输入、操作决策、产出与异常处理 / Prerequisites, real input, decisions, output, and failure handling |
| 岗位或协作方式 / A role or collaboration process | 每个人接收、决定、交付和验收什么 / What each person receives, decides, hands off, and checks |
| 研究或复杂判断 / Research or a complex judgment | 证据、推论、不确定性和实际影响 / Evidence, inference, uncertainty, and practical implications |

<a id="example"></a>
## 使用案例 / Example

**问题 / Question**

> 复利为什么会越滚越快？  
> Why does compound interest grow faster over time?

**从一个明确的假设开始 / Start with a stated assumption**

假设本金是 ¥1,000，年利率为 10%，不再追加资金。以下只是用来解释数学关系的假设数字，不是收益预测或投资建议。

Assume a starting balance of ¥1,000, a 10% annual rate, and no additional deposits. These figures illustrate the math; they are not a return forecast or investment advice.

| 年份 / Year | 年初金额 / Starting balance | 当年利息 / Interest earned | 年末金额 / Ending balance |
| --- | ---: | ---: | ---: |
| 第 0 年 / Year 0 | — | — | ¥1,000 |
| 第 1 年 / Year 1 | ¥1,000 | ¥100 | ¥1,100 |
| 第 2 年 / Year 2 | ¥1,100 | ¥110 | ¥1,210 |

第一年赚到的 ¥100 留在账户里，所以第二年的 10% 是按 ¥1,100 计算，得到 ¥110。第二年因此比第一年多赚 ¥10。若按单利计算，两年都只按原始的 ¥1,000 计算，期末会是 ¥1,200。

The first year's ¥100 stays in the balance. The next 10% is calculated on ¥1,100, so the second year's interest is ¥110—¥10 more than the first year. With simple interest, both years use the original ¥1,000, leaving ¥1,200 after two years.

**关键差别 / The key difference:** 复利会把已产生的利息也算进下一轮的计算基础。  
With compound interest, previously earned interest is included in the next calculation.

<a id="good-for"></a>
## 适合的问题 / Good for

- 从零理解 AI、产品、科学或其他陌生概念。  
  Learn an unfamiliar topic such as AI, product, or science from the ground up.
- 比较方案，弄清它们分别适合什么情况。  
  Compare options and understand when each one fits.
- 跟着完整步骤解一道逻辑题或数学题。  
  Follow the complete reasoning for a logic or math problem.
- 看懂研究、工具、岗位或工作流程。  
  Understand research, tools, roles, or workflows.
- 重新解释一段太抽象、跳步太多或术语太密的内容。  
  Rework an explanation that feels too abstract, skips steps, or uses too much jargon.

<a id="how-to-use"></a>
## 如何使用 / How to use

在支持 Skill 的 AI 工具中启用仓库里的 Skill，然后给出你想理解的问题。  
Enable the Skill from this repository in an AI tool that supports Skills, then provide the question you want to understand.

~~~text
请用 $zero-start-visual-explainer 从零解释复利。
先解释必要概念，逐步说明每一步为什么成立，
再用一组明确标为假设的数据演示，并检查结论。

Use $zero-start-visual-explainer to explain compound interest from zero.
Explain the prerequisites and why each step follows.
Show one worked example with clearly labeled hypothetical numbers,
then check the result.
~~~

对于需要详细推理的主题，如果当前 AI 环境支持阅读界面，它会按 Skill 规范组织完整讲解；纯文本环境则保留清晰步骤和结构。

For topics that need detailed reasoning, the Skill uses its specified reading layout when the AI environment supports it. In a text-only environment, it keeps the steps and structure clear.

<a id="files"></a>
## 文件说明 / Files

| 文件 / File | 用途 / Purpose |
| --- | --- |
| [SKILL.md](SKILL.md) | 讲解流程、视觉呈现规范和质量检查 / Explanation workflow, visual presentation rules, and quality checks |
| [references/presentation.md](references/presentation.md) | 已确认的阅读界面结构和版式 / Approved reading layout and structure |
| [assets/explainer.css](assets/explainer.css) | 浅色阅读界面的样式表 / Styles for the light reading interface |
| [agents/openai.yaml](agents/openai.yaml) | Skill 名称、简介与默认提示 / Skill name, description, and default prompt |
| [assets/icon.svg](assets/icon.svg) | Skill 图标 / Skill icon |

<a id="boundaries"></a>
## 边界与质量 / Boundaries

- “从零开始”是补足当前问题需要的前置知识，不代表每个问题都要变成长篇课程。  
  “From zero” means adding the background this question needs; it does not mean turning every answer into a long lesson.
- 示例、假设、来源事实和推论会区分；依赖来源或时效的信息需要核实。  
  Examples, assumptions, source-based facts, and inferences are kept distinct; time-sensitive or source-dependent claims need verification.
- 视觉排版取决于当前 AI 环境是否支持；纯文本环境不会假称有可点击界面。  
  Visual layouts depend on the AI environment; text-only environments are not described as having interactive features.
- 讲解和理解检查支持学习，但不证明读者已经掌握或长期记住。  
  An explanation and a comprehension check support learning; they do not prove mastery or long-term retention.
- 本仓库当前没有指定开源许可证；公开可见不等于已授权复制、修改或再发布。  
  This repository currently has no specified open-source license. Public visibility does not grant permission to copy, modify, or redistribute it.

