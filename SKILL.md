---
name: zero-start-visual-explainer
description: Explain unfamiliar AI concepts, logic or math problems, research, tools, skills, roles, and workflows from zero subject knowledge. Use when the user asks to understand, learn, compare, see a visual explanation, follow a worked solution, or says an explanation is abstract, crowded, shallow, or skips steps. For substantive teaching, render the whole explanation in the approved white rounded, pale-blue visual reading interface when a renderer is available; preserve full reasoning, meaningful interaction when useful, and one understanding check. Do not impose the full structure on casual chat or a simple factual lookup.
---

# Zero-Start Visual Explainer

Help an adult reader understand what something is, why it works, and how to use the explanation. Assume no prior knowledge of this subject. Respect demonstrated knowledge and the requested scope. Never infer intelligence or capability from ADHD or a preference for visual explanations.

## Workflow

1. **Identify the question.** Determine whether the task concerns a concept, a reasoning problem, a tool/workflow, research, or several of these. Set the boundaries of the answer before expanding it.
2. **Check essential inputs.** Ask at most 1–3 focused questions when missing facts or constraints materially change the answer. Continue independent work. State a reasonable, low-risk assumption when it allows progress; never invent source material or product behavior. Do not repeat questions already answered.
3. **Trace prerequisites.** Work backward from the first unfamiliar step to everyday knowledge. Explain the smallest sufficient prerequisite chain in dependency order. Explain a necessary new term in ordinary language at first use, before relying on it to explain another term.
4. **Open with a prominent central claim and short map.** Give one or two sentences answering the question, then show the 3–5 dimensions the explanation will cover. Use descriptive labels that match the content. For a deduction puzzle, highlight the goal or method first and reserve the final answer until after the derivation.
5. **Explain the mechanism.** Show known facts or input → action/inference → result, and state why each consequential transition holds. Use a specific worked example where helpful. Keep its situation and actors consistent; show actual starting material, a decision or action, a tangible output, and how the next step uses it.
6. **Build the approved presentation.** Visualize the difficult or crowded passage itself. For a substantive explanation needing sections, comparisons, or worked states, check the available rendering tools and skills and use an in-conversation renderer when available. Put the whole explanation in the approved light reading interface, not just a small diagram beneath ordinary chat prose. Read and actually apply `assets/explainer.css` as described below; a palette declaration or a generic renderer card does not make the approved layout. Keep clear passages simple within that presentation. Select interaction only when changing a premise, input, or step changes a substantive result and its explanation.
7. **Close with a prominent takeaway and one understanding check.** Finish the requested explanation first. Ask one short question that applies the central idea to a nearby case. Do not require an answer to unlock essential content.

## Completeness and depth

- Use a brief opening plus 3–5 main sections as a default. Use substeps inside a section when the question needs a detailed path; do not force every step into a separate large card.
- Make the first screen useful: show the central claim and begin explaining it. Avoid a long table of contents before the answer starts.
- Give each explanation unit a clear claim, its reason or mechanism, and a concrete consequence or example. A few keywords in an attractive panel do not constitute an explanation.
- Keep one idea per paragraph, usually 1–3 sentences. Split before introducing another actor, condition, or dependent argument. Use relationships, labels, and separators to organize information; do not replace depth with fragments or place an unchanged text wall inside a box.
- Preserve every premise, decision, and inference needed to reproduce the result. Remove repetition and unrelated background before shortening necessary reasoning.
- For workflows and roles, show what someone actually receives, decides, writes, hands off, and checks. “Identify the need → define → test” alone is too abstract.
- Label examples as `假设示例` unless they come from real material. Identify the source for real material. Distinguish facts, deductions, assumptions, proposed behavior, and unknowns wherever the distinction affects the conclusion.
- Use analogies as bridges; explain the actual mechanism and the analogy's important limit. Never simplify until a claim becomes false.
- Verify time-sensitive or source-dependent claims using appropriate available sources. Cite consequential claims nearby without breaking the reading flow. Do not fabricate facts, citations, product capabilities, or test results.

## Choose the subject path

| Subject | Necessary content | Concrete result to show |
| --- | --- | --- |
| AI or another concept | Familiar need; plain definition; parts and relationships; how it works; meaningful boundary | One input, what happens to it, and the resulting output |
| Logic or math | Goal; complete givens; each deduction and its reason; check against all constraints; final answer | Reproducible steps or states, including relevant alternative branches |
| Tool, skill, or procedure | Purpose; when to use; prerequisites; exact input; actions and decisions; output; failure handling | A realistic run with copyable input where useful and a recognizable result |
| Role, workflow, or collaboration | Shared goal; stages; materials; decisions; owners; handoffs; acceptance conditions | What each role gives and receives, plus one concrete joint decision |
| Research or broad judgment | Question; evidence; finding; what it supports; uncertainty; practical implication | A clearly bounded claim, plus plausible alternatives and affected groups |

For a mixed request, combine the relevant paths without repeating the introduction. When asked for multiple dimensions, select genuinely different dimensions and explain why they matter. Do not assume a result is universally good or bad because one metric improves. In collaboration examples, distinguish who recommends, who implements, and who has decision authority; acknowledge that organizational arrangements vary.

## Approved presentation profile

Use the latest user-approved style as the default. The approved deliverable is a light explanatory reading interface, with the main explanation organized inside it; an unstyled prose answer plus a small interactive graphic does not reproduce this interface. Read [references/presentation.md](references/presentation.md) and [assets/explainer.css](assets/explainer.css) before creating it. When the renderer supports a local `<style>` element, embed the stylesheet in the rendered fragment and place the content under `class="zsve"`. Actually use its layout classes for the opening, separated overview rows, white rounded sections, emphasis, and understanding check. Setting `--primary` or other theme variables without these classes is insufficient. Keep the content specific to the question rather than copying the sample topic.

- **White as the main reading surface.** Keep ordinary explanations and tables on white. Use dark, readable text. Use a light presentation consistently, even when the surrounding conversation uses dark mode.
- **Rounded surfaces.** Use gently rounded corners for bounded sections, notes, and interactive results. Keep borders thin and neutral. Do not place every sentence in its own box or stack unnecessary boxes inside boxes.
- **Blue for emphasis, light gray for support.** Highlight the opening claim, important local claims, and the final takeaway. Use pale blue for a small number of major callouts, blue text for key labels, and pale gray for definitions or supporting notes. Avoid a rainbow of peer sections and large dark-gray fills. Pair color with words; never encode meaning through color alone.
- **Compact, legible spacing.** Follow the approved reference density rather than expanding whitespace indiscriminately. Keep nearby explanations close, leave a moderate gap between sections, and retain readable line height. Do not shrink essential text to compensate for too much content.
- **Separate different dimensions with fine lines.** Present overview items and parallel dimensions as aligned label–explanation rows with a subtle light-gray separator between rows. Use row padding instead of a large empty gap. At narrow widths, put each label above its explanation and keep the separator across the row.
- **Show hierarchy without visual noise.** Let the main claim stand out, let section labels guide scanning, and let reasons read as connected prose. Do not bold entire sections. Never show literal Markdown stars or escaped emphasis markers in the reading surface.
- **Choose the useful structure.** Use tables for exact mappings, a compact flow or branch diagram for dependencies, and side-by-side comparison only when it remains readable. Keep the real reasoning in the structure, not only in introductory labels.
- **Reflow instead of overlapping.** Allow content and buttons to wrap, keep text columns shrinkable, and stack columns when narrow. Avoid fixed text heights, absolute positioning for prose, clipped content, and inner scrolling.

Choose support by local difficulty and density, not total length. A short difficult passage may need a substantial visual; a long easy passage need not become many colored cards. Use one level of grouping where possible.

### Rendering and fallback

- Discover and use the available in-conversation rendering capability for white rounded sections and meaningful controls, following its output and accessibility requirements. If a visualization skill is listed, read and apply it before authoring the rendered response. In Work Mode with Visualize available, create an HTML fragment, embed the approved CSS in its `<style>` element, use the `.zsve` structure, and emit the renderer's required visual reference. The defined light appearance takes precedence over a renderer's generic theme suggestions when custom styling is permitted. Do not turn the answer into an unrelated dashboard or treat only a small diagram as the requested presentation. Do not assume rendering is unavailable merely because a table could express the facts. Keep implementation details out of the explanation.
- Before emitting, inspect the actual fragment: it must contain an opening with pale-blue background, distinct white rounded sections with readable paragraph spacing, blue key labels, fine separators for parallel overview rows, and a prominent takeaway. Do not submit plain `<h1>`, paragraphs, generic `.card`/`.viz-row` containers, or CSS color variables alone as a successful visual explanation. Keep the first screen informative without compressing later reasoning into a text wall.
- Use the plain-text fallback only when rendering is actually unavailable, fails, or the user explicitly requests plain text. Preserve the teaching structure with prominent claim lines, compact paragraphs, Markdown tables, subtle horizontal rules, and numbered steps. Use Mermaid when dependencies or branching are clearer that way and rendering is supported.
- Do not claim to display literal rounded cards, exact colors, or clickable controls when the environment only supports text. A colored emoji is not a substitute for a useful visual.
- Render emphasis correctly for the chosen surface: use actual HTML emphasis in HTML, ordinary Markdown emphasis in Markdown. Never expose raw markup to simulate styling.

## Meaningful interaction

- Offer interaction when the reader can change a meaningful condition and immediately see what follows. Use concrete labels, such as `假设抽到：苹果 / 橙子`, `原文明确 / 原文含糊`, or a stage name.
- Start with one informative state already visible. Keep the central path understandable without clicking. Do not hide all key dimensions behind controls; stage-specific detail or alternate cases may be explored interactively.
- Update the input or premise, substantive result, and reason together. Show the next action when it changes. Keep unchanged facts stable.
- Do not add controls solely for decoration, manufacture tradeoffs, or make compatible goals appear mutually exclusive. Label hypothetical constraints and scenarios.
- Use numerical controls only when values have a real basis or an explicitly explained hypothetical calculation. Never invent qualitative scores to fill a dashboard.
- Use labeled native controls, keyboard access, a clear selected state, and accessible dynamic updates. Preserve a readable initial state and visible results without hover.
- Check every supported branch for logical and factual consistency. If an interactive renderer is unavailable, show the meaningful cases in a compact table; never describe a nonfunctional control as clickable.

## Questions and co-creation

- End every substantive teaching answer with one focused understanding check. Prefer a short application, a reason for a step, or a concrete next action. Avoid “懂了吗”, a long test, an unfamiliar term, or immediately revealing the answer.
- When an answer reveals a gap, repair the first unsupported step with a smaller example. Do not repeat the whole explanation unchanged or judge the reader's ability.
- Skip the learning check for casual chat, simple fact retrieval, and project-status replies.
- During co-creation, ask about the most consequential unresolved design issue after showing a concrete draft. Keep preference feedback distinct from a learning check; do not mechanically add both.
- Treat proposed rule changes as sample-only until the user explicitly approves incorporating them into the skill. After approval, integrate them by replacing conflicting rules, rather than appending a growing history of contradictory instructions. Do not seek repeated approval for routine work within an approved change.

## Final quality gate

Before sending, repair any failure below:

1. Can a new reader understand the opening and find the central claim immediately?
2. Is each essential term explained before it becomes a prerequisite for another step?
3. Can the reader reproduce the reasoning or take the first action without guessing a missing rule or input?
4. Does the worked example show concrete material, a decision, an output/handoff, and a check?
5. Are the opening claim, important claims, and final takeaway visually prominent?
6. Is the difficult passage itself unpacked with reasons, rather than reduced to keywords or left dense under a clear overview?
7. Are white, rounded sections and restrained blue/light gray used when the renderer supports them? Do parallel overview rows have subtle separators and compact spacing?
8. Do text, tables, controls, and every dynamic state fit at narrow widths without overlap or clipping? Check an actual rendered preview when possible. If a screenshot or browser preview is unavailable, check the fragment and interaction logic, then distinguish those checks from visual inspection; do not claim visual testing based only on source inspection.
9. Does each interaction change a meaningful result and its reason, with a useful initial state and no invented metric?
10. Are examples, assumptions, evidence, and uncertainty distinguishable? Does the response complete the request and end with the appropriate single question?
