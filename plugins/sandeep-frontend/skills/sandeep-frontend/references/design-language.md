# Sandeep Frontend Design Language

Use this as Sandeep's own design language. Do not imitate source material mechanically, copy assets, use proprietary fonts, or keep name-dropping references in the output.

## Core Intent

Make front ends and visual artifacts feel thoughtful, specific, and usable. This includes apps, websites, dashboards, HTML reports, slide decks, data visualizations, diagrams, and one-off interactive tools. The design should have a point of view, but the point of view must come from the audience, medium, and job.

Default to light-first design. Use dark mode only when explicitly requested or clearly required by the existing product or artifact.

## Mode Selection

Choose one visual mode before coding:

- Front-end app: product UI, SaaS, tools, workflows, forms, editors, portals, or interactive surfaces.
- Website/page: landing page, portfolio, product page, internal hub, documentation page, or marketing surface.
- Dashboard/analytics: operational dashboards, executive views, metrics explorers, monitors, and comparison tools.
- HTML report/data story: rendered reports, research briefs, analysis pages, model evaluations, and narrative data documents.
- Visualization: charts, maps, diagrams, simulations, explainers, scenario tools, and interactive labs.
- Slides/presentation: decks, visual narratives, executive summaries, teaching slides, and board-style updates.
- Document-like artifact: PDF/Word-style reports, memos, proposals, handouts, or printable pages.
- Creative/consumer tool: writing, design, media, habit, finance, health, travel, or personal workflow apps.

Let the mode guide the interface. Do not automatically make things editorial, article-like, dashboard-like, or app-like unless the brief benefits from that shape.

## Default Principles

- Light-first, never generic-dark by default.
- Compact hierarchy: headings should be confident, not huge.
- Subject-specific: derive color, structure, and imagery from the real domain.
- Useful pills: filters, modes, tags, reactions, status, and CTAs. No decorative chip confetti.
- Real structure: grids, dividers, tabs, tables, rails, timelines, and panels should encode information.
- Cards are for repeated objects, modals, and framed tools. Do not make every section a card.
- One signature move per screen: a distinctive rail, chart treatment, interaction, typography detail, image treatment, or navigation pattern.
- Copy is interface material. Use concrete nouns, active verbs, and labels that name user-recognizable outcomes.
- Match the medium: websites need responsive flow, reports need reading hierarchy, slides need one clear idea per frame, and visualizations need accurate encodings before ornament.

## Light Tokens

Start here, then adapt to the subject:

```css
:root {
  --paper: #fbfaf7;
  --surface: #ffffff;
  --surface-warm: #f4f1ea;
  --surface-blue: #eefaff;
  --ink: #111111;
  --muted: #5f625f;
  --faint: #8c8d91;
  --rule: #d8d6cf;
  --rule-strong: #bdb9ad;
  --accent: #c0f0fb;
  --accent-ink: #07313a;
}
```

Do not let the palette become only beige, only blue, or only gray. Add one domain-specific secondary accent when the subject calls for it.

## Typography

Preferred approach:

```css
--font-serif: Newsreader, "Iowan Old Style", Charter, Georgia, serif;
--font-sans: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
```

Use commercial fonts such as Signifier or Switzer only if already present and legally available. Do not fetch or bundle proprietary fonts.

Type roles:

- Page title: 32-56px desktop, 28-36px mobile, line-height 1.0-1.12.
- Section title: 16-30px depending on density.
- Card title: 20-28px, line-height near 1.1.
- Body/deck: 17-21px, line-height 1.45-1.65.
- Metadata: 11-13px, medium weight, uppercase with slight positive tracking.
- Controls: 14-16px, medium or semibold.

Do not use viewport-width font scaling. Avoid negative letter spacing. Use big type only when the brief truly needs a hero.

## Artifact Modes

Use these as starting points, not templates.

### Front-End App

Patterns:

- Clear workspace hierarchy: navigation, working surface, context panel, and action rail when useful.
- Controls should be obvious and efficient: tabs, segmented controls, menus, toggles, sliders, icon buttons, and compact forms.
- Use cards for repeated records or tools, not page sections.
- Keep primary actions close to the object they affect.

### HTML Report or Data Story

- Lead with the conclusion, then give the evidence path.
- Use charts, tables, callouts, and short text blocks in a measured rhythm.
- Use serif texture only if it improves reading; a report can also be clean sans-first.
- Keep citations, caveats, and methodology visible without making them the hero.

### Dashboard or Analytics Surface

- Prioritize scan density, comparison, filtering, and status.
- Use tables, sparklines, small multiples, legends, and annotations.
- Color should encode state, category, or magnitude.
- Do not use marketing hero sections inside operational tools.

### Visualization or Interactive Lab

- Choose the visualization type from the data relationship: comparison, distribution, flow, geography, hierarchy, sequence, or uncertainty.
- Label directly when possible; reduce legend-hunting.
- Use interaction to reveal detail, not to hide the core message.
- Verify chart legibility, color contrast, and responsive behavior.

### Slides or Presentation

- One idea per slide.
- Prefer strong visual hierarchy over dense paragraphs.
- Use repeated slide systems: title, evidence, comparison, quote, diagram, appendix.
- Make charts presentation-safe: larger labels, fewer ticks, clear takeaway titles.
- Keep theme continuity without making every slide identical.

Avoid:

- Treating every artifact as an editorial article.
- Treating every artifact as a SaaS landing page.
- Making slides read like webpages or reports read like slide decks.
- Hiding weak structure behind decoration.

## Operational Mode

Use this for dashboards, admin tools, CRMs, analytics consoles, and internal apps.

- Prioritize scan density, tables, tabs, segmented controls, forms, and durable navigation.
- Use sans-serif as the primary type; reserve serif for a report title or empty-state note only if it helps.
- Keep actions close to the data they affect.
- Use color for status and comparison, not decoration.
- Avoid marketing-style hero sections.

## Components

Pills:

- Shape: full pill for filters/status/reactions, 6-8px radius for quieter controls.
- Selected: pale accent fill with ink text.
- Unselected: transparent or white with hairline border.

Cards:

- Radius 6-10px.
- Border or faint rule instead of heavy shadow.
- Use for repeated entities only.
- Hover with underline, tint, or opacity; avoid scale effects.

Forms:

- Quiet, readable inputs.
- Direct error text.
- Buttons use outcome labels: "Save draft", "Publish", "Run analysis", "Export CSV".

Navigation:

- Keep small and useful.
- Prefer clear text links, tabs, segmented controls, and one primary action.

## Anti-Patterns

- Generic AI gradients, orbs, bokeh, glassmorphism, or sparkle decoration.
- Huge centered H1 plus generic CTA as the whole design.
- Dark mode when the user asked for light or did not ask for dark.
- One-note beige, purple, blue, slate, or espresso palettes.
- Cards inside cards.
- Editorializing everything.
- Dashboardifying everything.
- Making every deliverable look like the same website.
- Decorative numbering when order does not matter.
- Text inside big rounded rectangles when an icon, chip, tab, or link would be clearer.
- Empty marketing copy such as "unlock productivity", "seamless experience", "all-in-one platform", or "revolutionize".

## Build Checklist

- Artifact type and visual mode chosen and appropriate to the subject.
- Inspirations declared only when relevant.
- Light-first styling.
- Typography fits on mobile and desktop.
- Pills are useful.
- Cards represent repeated items or tools.
- Layout structure encodes information.
- Charts/diagrams/slides use encodings and hierarchy appropriate to their medium.
- Copy uses concrete user-facing language.
- Screenshot review confirms the result does not look generic.
