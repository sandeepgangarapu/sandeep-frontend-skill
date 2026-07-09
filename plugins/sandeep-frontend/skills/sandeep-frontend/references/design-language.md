# Sandeep Frontend Design Language

Use this as Sandeep's own design language. Do not imitate source material mechanically, copy assets, use proprietary fonts, or keep name-dropping references in the output.

## Core Intent

Make front ends feel thoughtful, specific, and usable. The design should have a point of view, but the point of view must come from the product's audience and job.

Default to light-first design. Use dark mode only when explicitly requested or clearly required by the existing product.

## Mode Selection

Choose one visual mode before coding:

- Editorial analysis: reports, research, essays, data stories, knowledge products.
- Operational product: CRMs, admin tools, internal dashboards, B2B workflows. Use compact utilitarian layout, restrained color, dense scanning, and predictable controls.
- Creative tool: writing, design, media, personal workflow apps. Use light surfaces, tactile controls, and one expressive signature element.
- Consumer utility: habit, finance, health, travel, shopping. Use friendly clarity, strong task flow, and domain-specific visual cues.
- Branded/product page: follow the brand or object first; Sandeep's taste should show in restraint, typography, and interaction polish.

Let the mode guide the interface. Do not automatically use serif-heavy layouts, article grids, or publication-style closing bands unless the subject benefits from them.

## Default Principles

- Light-first, never generic-dark by default.
- Compact hierarchy: headings should be confident, not huge.
- Subject-specific: derive color, structure, and imagery from the real domain.
- Useful pills: filters, modes, tags, reactions, status, and CTAs. No decorative chip confetti.
- Real structure: grids, dividers, tabs, tables, rails, timelines, and panels should encode information.
- Cards are for repeated objects, modals, and framed tools. Do not make every section a card.
- One signature move per screen: a distinctive rail, chart treatment, interaction, typography detail, image treatment, or navigation pattern.
- Copy is interface material. Use concrete nouns, active verbs, and labels that name user-recognizable outcomes.

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

## Editorial Mode

Use this mode for editorial analysis, data reports, essays, research hubs, publication-like collections, knowledge tools, and AI workflow briefs.

Patterns:

- Narrow metadata rail beside the headline.
- Compact title plus serif deck.
- Fine rules, dashed dividers, or ruled adaptive grids.
- Pills for filters, categories, reactions, and CTAs.
- Repeated cards with metadata, title, short serif summary, and small footer/status.
- Light surfaces with pale cyan selected states.
- Constrained article measure plus denser collection grids.

Avoid:

- Overusing split-letter title quirks.
- Making every product look like a publication.
- Dark homepage-inspired sections, unless the user explicitly wants dark.

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
- Decorative numbering when order does not matter.
- Text inside big rounded rectangles when an icon, chip, tab, or link would be clearer.
- Empty marketing copy such as "unlock productivity", "seamless experience", "all-in-one platform", or "revolutionize".

## Build Checklist

- Visual mode chosen and appropriate to the subject.
- Inspirations declared only when relevant.
- Light-first styling.
- Typography fits on mobile and desktop.
- Pills are useful.
- Cards represent repeated items or tools.
- Layout structure encodes information.
- Copy uses concrete user-facing language.
- Screenshot review confirms the result does not look generic.
