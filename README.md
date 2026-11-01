<div align="center">

# 🧭 Zero-Start Visual Explainer

### 从“我没学过”开始，把陌生问题讲到能用。

Explain unfamiliar ideas from zero, with the steps and examples needed to use them.

![Type](https://img.shields.io/badge/type-AI%20Skill-7257d5)
![Input](https://img.shields.io/badge/input-question%20%2F%20problem-3478c8)
![Output](https://img.shields.io/badge/output-reasoning%20%2B%20example-159578)

[它解决什么](#它解决什么) · [怎么讲清楚](#怎么讲清楚) · [适合的问题](#适合的问题) · [示例](#示例) · [怎么使用](#怎么使用) · [边界与质量](#边界与质量)

</div>

---

## 一句话介绍

Zero-Start Visual Explainer 从读者还不熟悉的地方开始，补上必要的前置知识，一步步解释“发生了什么、为什么这一步成立、最后怎样用到实际问题里”。适合 AI 概念、工具、岗位、研究、数学和逻辑推理等主题。

**先给核心结论 → 补上必要前置 → 展开推理 → 用具体例子走一遍 → 带走一个结论**

## 它解决什么

很多解释看起来有答案，却默认读者已经认识一堆术语；也有些回答把结论压成几句口诀，让人知道“要做什么”，却不知道每一步为什么成立。

这个 Skill 会把缺失的台阶补出来：新术语先用大白话解释，关键推理不跳步，抽象概念尽量配一个从输入到结果的具体例子。在当前环境支持视觉呈现时，它会把完整讲解放进清晰的阅读界面；不支持时，则用结构清楚的文字和图表说明。

| | 快速结论式回答 | Zero-Start Visual Explainer |
| --- | --- | --- |
| 面向读者 | 默认读者知道背景 | 从必要的前置知识开始 |
| 讲解方式 | 给结论或一串术语 | 展示事实、推理步骤和每一步的理由 |
| 例子作用 | 作为补充 | 用具体输入、判断和结果走完机制 |
| 适合目标 | 快速查一个事实 | 真正弄懂、比较或照着完成一件事 |

## 怎么讲清楚

1. **先确定问题边界。** 要讲一个概念、一道题、一个工具流程，还是几者结合。
2. **找出缺的第一块知识。** 从读者第一次可能卡住的术语或步骤开始解释。
3. **把推理连起来。** 展示输入或已知事实，说明中间的判断，再给出结果。
4. **走一个具体例子。** 让读者看见同一套思路如何用于一个实际情境。
5. **检查是否真的讲通。** 用一句简短的问题，让读者试着把概念用到相邻情境。

## 适合的问题

| 主题 | 读者会看到什么 |
| --- | --- |
| AI 或陌生概念 | 日常问题、概念定义、组成关系、运行过程与边界 |
| 逻辑或数学题 | 已知条件、每一步推导的理由、结果核对 |
| 工具或工作流 | 使用前提、实际输入、操作决策、产出与异常处理 |
| 岗位或协作方式 | 每个角色接收什么、决定什么、交付什么、怎样验收 |
| 研究或复杂判断 | 问题、证据、推论、不确定性与实际影响 |

## 示例：从零理解复利

**问题：**“复利为什么会越滚越快？”

**讲解路径**：先说明本金和利息是什么，再演示“下一轮的利息也会产生利息”。之后用一笔假设金额和一个明确注明的假设利率，逐年算出本金如何变化；最后对比单利，指出结果依赖利率、时间和是否持续投入。

这个示例说明讲解方法，不构成投资建议；数字也应标为假设，不能当成收益预测。

## 怎么使用

把仓库下载并放入你的 AI 工具支持的 Skill 目录，然后描述你想学的内容，以及你希望解释到什么程度。

可以这样提问：

```text
Use zero-start-visual-explainer to explain compound interest from zero.
Show the prerequisites, each step in the reasoning, and one worked example.
Use an easy-to-read visual layout when available, then ask one short
question that helps me apply the idea.
```

适合学习陌生概念、比较方案、跟着推导一道题、理解研究与工作流程，或在解释太抽象、跳步太多时重新讲一遍。

## 边界与质量

- “从零开始”指补足当前问题需要的前置，不代表每个回答都要拉成长篇课程。
- 示例、假设、来源事实和推论会区分；时效性或依赖来源的内容需要核实。
- 视觉排版取决于当前 AI 环境是否支持对应的呈现能力；纯文本环境会保留清晰的步骤和结构，不会假称有可点击界面。
- 讲解和理解检查帮助读者学习，不代表已经证明读者掌握或能长期记住。
- 本仓库当前没有指定开源许可证；公开可见不等于已授权复制、修改或再发布。

## 仓库内容

| 文件 | 用途 |
| --- | --- |
| [`SKILL.md`](SKILL.md) | 从零讲解的流程、视觉呈现规范和质量检查 |
| [`references/presentation.md`](references/presentation.md) | 已确认的阅读界面结构和版式规范 |
| [`assets/explainer.css`](assets/explainer.css) | 浅色阅读界面的样式表 |
| [`agents/openai.yaml`](agents/openai.yaml) | Skill 名称、简介与默认提示 |
| [`assets/icon.svg`](assets/icon.svg) | Skill 图标 |

---

For the full instructions, see [`SKILL.md`](SKILL.md). The goal is not just a shorter answer; it is an explanation a reader can follow and apply.
