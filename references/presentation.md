# Approved presentation reference

Use this profile when a rendered explanation is available. Present the substantive explanation in the approved reading interface, including its opening claim, organized reasons, worked steps, and takeaway. A generic theme-colored graphic below an otherwise plain answer is not equivalent to this presentation. Keep an ordinary text fallback available. Read the renderer's own UI/interface instructions for emission and accessibility; treat the light palette and rounded compact layout as the requested interface design. Do not assume the reusable CSS alone creates a rendering capability.

## Visual hierarchy

- Keep the primary surface white (`#ffffff`), body text dark (`#263344`), key labels blue (`#2364b5`), the major callout pale blue (`#edf4ff`), and supporting notes pale gray (`#f4f6f8`). Use neutral separators (`#e1e7ef`). This presentation uses a light style.
- Use the opening claim and final takeaway as the strongest emphasis. Give important local claims a blue label or short emphasized sentence; keep the reasons in normal text.
- Use rounded sections around 16–20 px and a gently rounded outer reading surface. Do not create a box for every sentence or nest filled boxes unnecessarily.
- Keep body text at the approved 16 px with about 1.65 line height. Keep secondary notes readable at 14 px. Use heading scale for hierarchy, not large gaps.
- Use roughly 14 px between ordinary paragraphs, 16–18 px padding inside typical sections, and 24–27 px between main sections. Do not add blank spacer elements. A one-line row needs only about 9 px top/bottom padding.
- Keep buttons at least 44 px high with about 8 px between them; allow wrapping. Use a clearly selected blue control and white text.

These are stable defaults from the approved sample. Adapt to accessibility settings or a new explicit user preference; do not silently revert to large dark panels or excessive spacing.

## Reusable styles

Read `assets/explainer.css` and include its actual content in a local `<style>` element when the chosen renderer supports custom CSS. Place the entire explanation under a unique root ID with class `zsve`. Scope JavaScript queries to that root. Do not link a local CSS path into a sandbox that cannot access it. The CSS file is an asset for the generated response, not a theme that gets applied automatically.

In Visualize, use this minimum structure as a starting point. Replace the words with the topic's real explanation and add substeps where necessary. Do not merely declare theme variables or substitute generic host `.card` and `.viz-row` classes for these components:

```html
<style>/* insert the contents of assets/explainer.css here */</style>
<div id="unique-explainer-id" class="zsve">
  <h2>Question-specific title</h2>
  <div class="opening">
    <div class="blue">先看结论</div>
    <p class="label">The central claim in ordinary language.</p>
    <p>One or two sentences of orientation.</p>
  </div>
  <div class="roadmap" role="list">
    <div class="map-row" role="listitem"><span class="blue">Dimension</span><span>Why it matters.</span></div>
  </div>
  <section class="section"><h3>First real question</h3><p>Claim, reason, consequence.</p></section>
  <div class="quote"><span class="blue">最后记住</span>Takeaway.</div>
  <div class="check"><span class="label">理解检查</span>One application question.</div>
</div>
```

Use 3–5 substantive sections when the topic needs them. The skeleton is a layout guide, not a license to replace explanation with headings and short labels. Pale blue belongs mainly in the opening and occasional takeaway; white remains the dominant reading surface.

Use only the classes needed for this answer:

| Class | Purpose |
| --- | --- |
| `opening` | Prominent starting claim and brief orientation |
| `blue`, `label` | Key label and short emphasis |
| `scope`, `small-note` | Clearly bounded context or supporting qualification |
| `roadmap` with `map-row` children | Aligned parallel dimensions with fine row separators |
| `section` | Main rounded white section with a neutral border |
| `flow-table` | Exact mappings, with labeled stacked rows on narrow screens |
| `caption`, `doc` | Occasional supporting note or concrete artifact fragment |
| `quote` | Major takeaway; use sparingly |
| `ex-controls`, `ex-button` | Wrapping, rounded native controls; set `aria-pressed` |
| `ex-interactive`, `explorer-fields` | A selected result with labeled reasons and actions |
| `check` | One focused comprehension question |

Do not instantiate every class by default. Preserve full reasoning while grouping related ideas. Main section count is guidance, not a demand for empty sections.

### Parallel dimension rows

Use a real wrapper per label–explanation pair so each separator spans one whole dimension. Do not use independently spaced label and value columns that lose their row association.

```html
<div class="roadmap" role="list">
  <div class="map-row" role="listitem">
    <span class="blue">输入是什么</span>
    <span class="detail">解释用户实际提供的材料，以及材料为何足够或不足。</span>
  </div>
  <div class="map-row" role="listitem">
    <span class="blue">结果怎么看</span>
    <span class="detail">说明得到什么，并用明确条件判断是否达到目标。</span>
  </div>
</div>
```

Use the same row structure for other parallel dimensions when useful. Preserve connected prose for reasoning that depends on the preceding sentence.

### Interactive result

Use native buttons inside `ex-controls`. Put the initial meaningful result in `ex-interactive`; a heading plus `explorer-fields` can show the changed input, output, reason, and next action. Set one initial `aria-pressed="true"`, update it after a choice, and update all dependent text together. Use `aria-live="polite"` on the result. Add the renderer's interaction cursor class when provided; do not assume it exists everywhere.

Keep one main interaction per explanation where practical. A stage explorer and an input comparison may coexist in a detailed workflow answer when they teach distinct relationships, but avoid competing controls or repetitive result panels.

## Layout checks

- Support the normal conversation width around 736 px and narrow screens down to 320 px.
- Use `minmax(0,1fr)` for shrinking text columns, `min-width:0` for children, and wrapping buttons. Stack labels and explanations on narrow screens.
- Keep all prose in normal document flow. Do not use fixed content heights, absolute positioning, negative margins, clipping, or inner scrolling to fit text.
- Use table headers and `data-label` on cells for the bundled narrow-screen table layout. Add labels that match the actual column meaning.
- Do not collapse all relevant dimensions into an interaction merely to shorten the initial view. Keep the map and core explanation present; use controls for detailed cases or changing states.
- When a browser renderer is available, inspect both normal and narrow widths, including the longest dynamic state. Otherwise distinguish source/interaction checks from visual rendering verification.
- Confirm that the stylesheet is embedded and that the rendered fragment uses `zsve`, `opening`, `section`, blue emphasis, and a takeaway. A visual with only color variables, plain paragraphs, and generic host rows is the specific failure this rule prevents.
- Treat long output by removing repeated explanation, shortening labels, or using meaningful stage detail. Do not create artificial length with large gaps; do not compress essential reasoning to isolated keywords.

## Fallback

If exact styling or interaction cannot render, use a prominent opening claim, compact paragraphs, aligned Markdown tables for mappings, and horizontal rules between major dimensions. Preserve all essential reasons and show alternate cases as actual content. Do not display HTML source, escaped Markdown emphasis, pretend buttons, or promise a fixed color/shape in a text-only surface.
