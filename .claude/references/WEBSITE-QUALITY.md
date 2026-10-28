# Website Build and Review Standard

Use this reference during `/build` and `/review`. It translates approved strategy, copy, and Visual Direction into a usable local website without creating a second strategy or design process.

## Source authority

| Decision | Authority |
|---|---|
| Audience, offer, positioning, proof, and claim limits | Approved upstream session files |
| Brand meaning, personality, voice, messaging, and conceptual boundaries | `06-brand-concept.md` |
| Page list, section order, section purpose, proof placement, and CTA path | `07-website-structure.md` |
| Exact customer-facing wording and microcopy | `08-website-copy.md` |
| Color, typography, composition, graphic language, imagery treatment, and visual restrictions | `assets/brand/visual-direction.md` |

Visual Direction may change how content is presented, but it cannot silently change what the page says, its argument order, or its proof limits. Structure and copy may require a visual solution, but they cannot silently replace the approved identity. If two authorities materially conflict, `/build` resolves the conflict with the decision order in its skill and records it in `09-build-notes.md`; `/review` reports it.

A later approved stage may resolve a specifically named open item from an earlier stage only when it explicitly records the participant's decision. This is a documented resolution, not permission for silent overrides.

## Pre-build gap scan

Read every section of the Visual Direction export as described in `BRANDBOOK-OS-MAP.md`: `00` when present, blocks `01`–`08`, `09. Page Format & Structure`, `Still to define`, `Responsive — desktop and phone, non-negotiable`, and `Instructions for AI`. Blocks 01, 06, and 08 disappear from the export when unanswered and are then named only in `Still to define`; blocks 02, 03, 04, 05, and 07 always appear, and their system defaults apply in full when unanswered. Resolve only gaps that materially change the website implementation.

Check these concrete failure modes before proposing a layout:

- the recipe's hero, a centred alignment answer, or another section competing for the only permitted centred section;
- figures, quotes, images, or other inputs of a recipe section type missing from the approved structure, copy, proof, or assets;
- placeholder or instructional text exported as a project answer;
- a block 05 recipe run or a `09` format, goal, or order of parts that conflicts with `07-website-structure.md` or `08-website-copy.md`;
- `Single screen, chosen by the brand` when `07` approves more content than one screen can hold;
- the same quality appearing in both positive and negative direction, including conflicts between block 01 keywords, other block answers, block 01 anti-keywords, and block 08;
- block 08 missing, or omitting a material visual boundary already approved in `06-brand-concept.md`;
- lighting or photographic instructions when no positive photography direction has been approved;
- named fonts that are unavailable, unlicensed, missing required weights, or incompatible with the approved language;
- no accessible text-color role for one or more approved section surfaces;
- a system default conflicting with an explicit project answer, visual restriction, content requirement, or supplied asset reality.

- Do not ask the participant during `/build`; resolve a missing decision with the build's decision order and record it.
- Do not reopen decisions already approved in the session files.
- Ignore non-website applications such as packaging or signage during this build.
- Use an explicit local placeholder for a missing non-blocking asset or integration.
- Do not invent a logo, licensed font, proof, customer result, or photography direction.
- Record implementation decisions and unresolved items in `09-build-notes.md`; do not create separate decision, copy, or prompt logs.

## Intentional design loop

Before coding, state in `09-build-notes.md` the page's purpose, priority visitor, main action, visual concept, and one recognisable quality carried from Visual Direction. Complete the visual assembly plan below before writing website code. Then work through four passes:

1. **Shape:** decide hierarchy, composition, density, rhythm, and the role of each visual element before styling details.
2. **Build:** implement the approved structure and copy with the simplest suitable code.
3. **Audit:** inspect the rendered page for usability, accessibility, responsiveness, source fidelity, and visual defects.
4. **Polish and harden:** fix hierarchy, spacing, wrapping, states, edge cases, and performance problems found in the audit.

Do not use visual novelty as a substitute for the approved concept. Avoid a generic stack of identical cards, default gradients, arbitrary rounded containers, or repeated centered sections unless Visual Direction specifically calls for them.

Content remains primary. `Low density`, `one idea per screen`, generous whitespace, short sentences, or a restrained visual system controls grouping and emphasis; it does not authorize deleting decision-critical content or stretching one generic sentence into an oversized section. Use content-driven section height. A deliberate brand-moment section may be sparse only when the surrounding page already carries the complete buying decision and the moment has a distinct narrative job.

Allocate visual emphasis according to decision value. A researched comparison, offer, proof, or primary action must not be rendered as tiny secondary text while an unsupported manifesto or decorative statement receives the dominant section. Reusing the same hero image in another major section requires a distinct narrative or product-detail purpose; otherwise use a different approved asset or a non-image composition.

## Implementation profile

For the Express path, build a dependency-free static one-page site with semantic HTML, CSS, and minimal JavaScript. It must work locally without a build step or external code and font CDNs.

For the Full path, follow the approved page architecture. Prefer the same static approach unless the approved requirements genuinely need another implementation. Do not reduce a required multi-page journey or integration merely to fit a preferred stack.

Place all implementation files inside the active session's `site-v1/`. A typical Express build is:

```text
site-v1/
├── index.html
├── styles/
│   ├── tokens.css
│   ├── base.css
│   ├── layout.css
│   ├── archetypes.css
│   └── sections.css
├── scripts/
│   └── main.js
└── assets/
```

Create `archetypes.css` for the reusable section types of the block 05 recipe and the accordion pattern; keep section-specific exceptions in `sections.css`. Create only files the website actually uses. Keep strategy and Visual Direction inputs in their existing locations; do not duplicate or edit them inside `site-v1/`.

## Translate Visual Direction into the website

The Visual Direction export comes from the Brandbook OS dashboard. `BRANDBOOK-OS-MAP.md` lists every question, option, and exact exported sentence; use it to tell a catalog option from an *Other* answer, a note, or an unanswered field. The export uses these sections:

0. **Brand copy and voice** (optional) — brand text pasted into the dashboard. In this workshop `08-website-copy.md` owns the exact public wording; use `00` only as voice evidence, and never stop because it is missing.
1. **Visual Foundation** — translate territory, tension, keywords, and anti-keywords into the overall visual character and final review criteria. The first quality of the tension usually lives in material (texture, image, stroke) and the second in structure (grid, type, margins).
2. **Name & Typography** — implement the brand name exactly as written, the primary and secondary families with their exported stacks and weights, the case, weight, and hierarchy settings, and the system-default type scale. The catalog families (Libre Caslon Text, Inter, Nunito, JetBrains Mono) use the SIL Open Font License: bundle the required weights in `site-v1/assets/fonts/` rather than loading them from Google Fonts or another CDN; if the files cannot be obtained, use the exported stack and record it. A family typed through *Other* is not a licensed font asset until it is supplied.
3. **Color System** — use the five exported tones, function and proportion, color rules, and the computed `Interface surfaces` and `Buttons and calls to action` blocks as tokens. Verify every stated contrast ratio from the actual exported values. Proportions refer to visible surface, not element count. A dark Neutral, as in the `Night` palette, means a dark page background.
4. **Composition** — translate grid, alignment, symmetry, density, and white space, plus the defaults for columns, measure, margins, rhythm, spacing, breakpoints, layers, dividers, and image/text splits, into responsive layout rules.
5. **Page Architecture** — one section recipe (`Editorial`, `Alternating`, `Grid`, `Cinematic`, or an *Other* text), the `Alternation rules — non-negotiable`, the accordion pattern, and defaults for header, hero, hero on mobile, calls to action, and section heads. `/express-copy` or `/structure` reconciles the recipe with the business argument and assigns compatible section types to stable section IDs. The later `07-website-structure.md` controls which sections exist, their order, their message jobs, proof placement, and the CTA path.
6. **Illustration & Materiality** — implement the illustration style, line quality, and level of detail, and the paper and texture finish. `None` means no illustrative SVG. On the web, `Matte` means flat surfaces without shine, `Gloss` smooth surfaces with a subtle reflection, and `Textured` subtle CSS or SVG grain, never stock paper images. Do not infer a positive photography style from this block.
7. **Graphic Language** — implement only the approved shapes, patterns, icons, and separators plus the frame, border, device, and motif defaults. `Shapes` sets the border radius for the whole page, buttons included.
8. **Visual Restrictions** — treat every `What to avoid` row and every block 01 anti-keyword as a review check.
9. **Page Format & Structure** — honor the format in point 1; `From your copy` applies the map's word-count rule to `08`. Points 2 and 3 are fallbacks for a page with no structure stage; here `07` owns the goal, primary action, and order. Apply point 4 navigation unless `07` defines navigation.

Every export also ends with `Responsive — desktop and phone, non-negotiable` and `Instructions for AI`. Obey both as fixed rules, except that `/build` never asks the participant: where `Instructions for AI` would ask, apply the build's decision order.

There is no Distinctive Visual Codes block and no AI Visual Direction block. Carry the recognisable visual quality from blocks 01, 06, and 07 and the distinctive codes approved in `06-brand-concept.md`. Do not write image-generation prompts.

If no photography direction exists, solve the site with approved typography, color, layout, graphic elements, illustration, and materials. Use a clearly labelled local placeholder for any image slot; when photography is essential to the approved content or offer, also record the missing photography direction as a launch blocker.

The block 05 recipe forms a palette. Use only the section types supported by the actual content, proof, and assets. The exact section order always comes from the later `07-website-structure.md`; the recipe's run, `09` point 3, a placeholder, or instructional text is not final architecture. Review block 08 together with the conceptual and visual boundaries in `06-brand-concept.md`, so a dashboard omission cannot erase an approved restriction.

### Direction precedence inside the export

When two instructions appear to differ, use this order:

1. explicit project answer or named non-negotiable rule;
2. explicit visual restriction;
3. system default, only where the project answer is silent;
4. expressive or derivable guidance, inferred conservatively from stronger decisions.

An *Other* answer carries the same weight as a catalog option; interpret it rather than snapping it to the nearest option. A note (` — <note>` or `_Note: <note>_`) refines the option it follows and wins when the two contradict. A system default never overrides an explicit project answer. For example, an answered six-column grid overrides a generic twelve-column desktop default; responsive implementation may derive compatible tablet and mobile behavior without changing the approved desktop character. Record each applied default or derived decision in `09-build-notes.md`.

Resolve every website-relevant item in `Still to define` or `Pendiente de definir` through an explicit answer, a named system default already present in the export, or `Not applicable` with a reason. Do not invent a new choice or treat a silent gap as approval.

### Visual assembly plan

Create a compact implementation map in `09-build-notes.md` before coding. Head it with the page format from block 09 and the goal and primary action from `07`, so the map also serves as the numbered structure that block 09 asks for:

| Section ID | Content job from `07` | First words and copy volume from `08` | Section type from the block 05 recipe | Focal point | Surface/alignment/columns | Density | Rule checked |
|---|---|---|---|---|---|---|---|

Below the table add two compact low-fidelity wireframes, one near 390 px and one near 1440 px. They may be ASCII outlines. Show section boundaries, column or stacking behavior, focal element, major image slot, background change, and intentional empty space. They must make repeated composition and mobile-order problems visible before styling.

Check every explicit alternation, centering, focal-point, surface, and archetype rule against the map. Also compare the approximate surface allocation with the exported color proportions. Treat proportions as directional unless the export explicitly requires measurement; do not distort content merely to hit a percentage.

Do not show the plan for approval or wait for confirmation: fix any rule the map breaks, then continue to code. Keep all detail in `09-build-notes.md`; do not create `LAYOUT.md`, `DECISIONS.md`, `COPY.md`, or `IMAGE-PROMPTS.md`.

Apply every explicit `non-negotiable` rule from block 05 unless it would break accessibility, hide or reorder approved content, falsify the CTA hierarchy, or conflict with a material requirement in blocks 01–04 or 08. When a conflict exists, preserve the business and accessibility requirement, choose the closest visual resolution, and document the exact conflict.

Do not interpret `Page Architecture` as permission to invent, remove, merge, or reorder sections. Do not force an archetype when the real copy volume cannot fit it at mobile and desktop widths.

In the HTML, give every content section stable inspection attributes for the decisions that actually apply, such as `data-section`, `data-arch`, `data-theme`, `data-align`, `data-cols`, and `data-density`. Mark exactly one focal element per section with `data-focal`. Do not add meaningless attributes merely to satisfy a schema.

## Token system

Keep reusable brand values in `styles/tokens.css` and use semantic variables throughout the remaining CSS:

- source and semantic color tokens;
- display and body font stacks, weights, and approved heading levels;
- spacing rhythm, content measure, container width, and gutters;
- corner, border, shadow, surface, and material rules;
- motion durations and easing when motion is approved;
- documented responsive breakpoints.

Comment each token group with its Visual Direction block and whether the value is an explicit answer, system default, or derived implementation choice. Record the reasoning for derived values in `09-build-notes.md`.

Use exact supplied brand colors. Derive accessible semantic roles from them without presenting a derived value as a new brand color. Do not scatter brand HEX values, font families, or reusable brand sizes through component files. One-off layout calculations and browser-safe technical values do not need artificial tokens.

CSS custom properties cannot be used directly in standard media-query conditions in all target browsers. Document breakpoint values in `tokens.css`, then use the matching literal conditions in media queries.

## Structure and copy implementation

- Implement the exact approved pages, section order, stable IDs, section purposes, and CTA path from `07-website-structure.md`.
- Implement the approved wording from `08-website-copy.md` in the HTML. Do not rewrite it to fit a component.
- Use semantic landmarks, one clear `h1` per page, and heading levels that reflect content hierarchy.
- Keep important content and actions available without JavaScript. JavaScript may add progressive enhancement such as navigation state or motion.
- Vary section composition according to Visual Direction and content purpose rather than repeating one generic card layout.
- Preserve the `D1`–`D10` customer-facing consequences and the decision contribution of every section. Do not reduce body copy to fit an archetype; adapt the archetype to the approved content volume.
- Use honest placeholders for missing proof or assets. A placeholder must not resemble a real testimonial, client logo, statistic, or result.
- Implement the primary action according to the approved conversion implementation state. A missing connection is a launch blocker, not a successful local substitute.
- Do not simulate a successful waitlist entry, reservation, order, booking, saved response, or other conversion when no real destination persisted it. Build an explicitly labelled prototype state instead.
- Avoid generic agency language, invented scarcity, unsupported guarantees, and invented business details.

## Visual assets

- Use approved supplied assets whenever available and preserve their usage restrictions.
- If illustration is approved, simple local SVG or CSS implementation may express the documented system. Do not present an improvised illustration as a final approved brand asset.
- Do not use stock images, external placeholder services, or unapproved remote assets.
- Give informative images useful alternative text. Give decorative images empty alternative text.
- Provide intrinsic `width` and `height` for raster images and lazy-load below-the-fold images.
- Record each missing image slot, intended purpose, aspect ratio, and the prohibited treatments from block 08 and the block 01 anti-keywords in `09-build-notes.md`.

## Responsive behavior, access, and trust

Check at minimum:

- meaningful layouts at approximately 360, 768, 1280, and 1600 pixels, with no horizontal scrolling;
- readable text, suitable line length, and adequate touch targets;
- semantic landmarks and heading order;
- keyboard navigation and visible `:focus-visible` states;
- WCAG AA contrast for ordinary text and interactive states;
- meaningful link and button labels;
- labels, instructions, validation, and status feedback for forms;
- reduced-motion behavior when animation exists;
- understandable errors and recovery;
- working links and actions;
- accurate metadata and social preview;
- privacy and consent appropriate to any data collected;
- clear contact or business information where relevant;
- a clear post-submission state.
- mobile controls with a practical hit target of at least 44 × 44 CSS pixels;
- form text at least 16 CSS pixels on mobile to prevent unwanted browser zoom;
- no disabled browser zoom and no sticky element covering focused content;
- error messages that explain how to recover rather than only naming the error;
- layout, wrapping, and alignment handled with CSS flow, flexbox, or grid rather than JavaScript measurements when possible;
- safe-area insets respected where fixed mobile controls touch screen edges.

Use WCAG 2.2 as the normative accessibility reference. Do not claim full compliance from an automated or visual check alone. Add dark mode only when Visual Direction supports it.

## Visual layout integrity

Do not infer visual quality from valid HTML, CSS, or the absence of horizontal scrolling. Inspect the rendered page itself.

At minimum, review the complete page at approximately:

- 390 × 844 for a common mobile viewport;
- 768 × 1024 for tablet or narrow layout behavior;
- 1440 × 900 for desktop;
- one additional width near a layout breakpoint when the composition changes materially.

At every width check:

- shared container edges, grid alignment, and intentional exceptions;
- accidental overlap, clipping, overflow, off-screen content, and incorrect stacking order;
- navigation, buttons, forms, cards, badges, and decorative elements after wrapping;
- heading line breaks, orphaned words, unreadably narrow columns, and text colliding with artwork;
- consistent spacing rhythm inside components and between sections;
- section transitions, background boundaries, and unintended gaps;
- visual hierarchy, content density, and whether the primary action remains easy to find;
- whether large areas of whitespace express intentional hierarchy or merely expose missing content;
- whether every section visibly delivers the distinct decision value approved in `07` and `08`;
- image aspect ratio, focal-point cropping, distortion, and placeholder behavior;
- footer completeness and alignment;
- browser font fallback and layout shift when approved fonts are unavailable;
- keyboard focus and 200% browser zoom without loss of content or action.
- deliberate alignment: every visible element aligns to a grid, edge, baseline, or intentional optical center;
- complete interaction states for controls: default, hover where relevant, focus, active, disabled, loading, error, and success only when the flow uses them.

Compare the rendered result with the approved Visual Direction and intended composition, not only with the source code. Decorative shapes must never obscure copy, controls, or focus indicators.

Compare each rendered viewport with the planned compact wireframe. For a grid-driven layout, provide a review-only grid overlay such as `?grid=1` when it can be implemented without affecting the normal page; use it to inspect columns, margins, and intentional exceptions. The overlay is an implementation aid, not customer-facing UI.

Treat content or controls hidden or overlapping, an unusable primary action, broken navigation or forms, unreadable text, obstructive horizontal overflow, and severe mobile collapse as **Blockers**.

Treat systematic misalignment, inconsistent containers, visibly broken spacing, accidental empty areas, poor line breaks, and repeated composition errors as **Important**, even when the page remains technically usable.

## Build verification

Before finishing `/build`:

1. Recheck block 08, **Visual Restrictions**, and the block 01 anti-keywords against the rendered site.
2. Check that the recognisable visual quality named in the design statement is visible without obscuring the message or action.
3. Check that color dominance and accent use follow the documented proportions. Treat proportions as directional unless the export explicitly requires exact measurement.
4. Check that reusable brand colors, fonts, and size rules come from `tokens.css`.
5. Check every explicit block 05 alternation, focal-point, centering, archetype, surface, and approximate color-allocation rule against both the section attributes and the full rendered page; record each as `Pass`, `Adapted with reason`, or `Blocked`. Use a lightweight DOM check when local browser tooling is available; otherwise record the manual evidence. Do not add a permanent validation script solely to satisfy this step.
6. Compare the 390 px and 1440 px rendered pages with the planned wireframes and explain every material deviation. For grid-driven layouts, inspect the review overlay as well as the normal page.
7. Exercise the primary action and any local form states.
   Verify through the actual destination, stored record, or network response that the conversion was received. A visual success message alone is not evidence.
8. Inspect the complete rendered page at mobile, tablet, desktop, and any material breakpoint using the visual-layout-integrity checklist. Fix clear local defects before completing `/build`.
9. Record the planned wireframes, visual architecture map, rule-status checks, viewport sizes, rendered areas inspected, deviations, defects fixed, unresolved visual issues, derived implementation choices, missing assets, and known limitations in `09-build-notes.md`.

## Review outcome

Use these priorities during `/review`:

- **Blocker:** prevents the primary action, creates serious accessibility or privacy risk, materially contradicts an approved source, or makes a key claim misleading.
- **Important:** likely harms understanding, trust, brand fidelity, or use.
- **Improve:** useful refinement with lower expected impact.

For every issue include evidence, location, consequence, and a specific fix. Distinguish manual checks, automated checks, and items not tested. Do not invent a conversion percentage.

For a website whose stated purpose is demand capture, lead generation, booking, reservation, purchase, or data collection, an unconnected primary action is always a **Blocker**. The site is `Not ready to publish` until the action persists the promised result or the public-facing objective and language are changed to an explicit demo.

The site cannot be rated `Ready` unless the complete rendered page and primary path were visually inspected at both mobile and desktop widths. If rendering was unavailable, report `Visual QA not completed` and use `Not ready to publish` until that check is performed.

## Method sources

- Vercel Labs, “Web Interface Guidelines”: https://github.com/vercel-labs/web-interface-guidelines
- Impeccable, design review and refinement methodology: https://github.com/pbakaus/impeccable
