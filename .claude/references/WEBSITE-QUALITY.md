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

Visual Direction may change how content is presented, but it cannot silently change what the page says, its argument order, or its proof limits. Structure and copy may require a visual solution, but they cannot silently replace the approved identity. If two authorities materially conflict, identify the conflict and ask one decision question.

A later approved stage may resolve a specifically named open item from an earlier stage only when it explicitly records the participant's decision. This is a documented resolution, not permission for silent overrides.

## Pre-build gap scan

Read all ten Visual Direction blocks, `Still to define`, and `Instructions for AI`. Resolve only gaps that materially change the website implementation.

Check these concrete failure modes before proposing a layout:

- two selected archetypes or alternation rules competing for the only permitted centered section;
- figures, comparisons, images, or other archetype inputs missing from the approved structure, copy, proof, or assets;
- placeholder or instructional text exported as a project answer, especially in `Section order`;
- a block 05 section order, section job, proof requirement, or CTA path that conflicts with `07-website-structure.md` or `08-website-copy.md`;
- the same quality appearing in both positive and negative direction, including conflicts between blocks 01, 09, and 10;
- block 08 signature moves that only repeat generic grid, alignment, or material settings and do not create a recognisable project-specific cue;
- block 09 omitting a material visual boundary already approved in `06-brand-concept.md`;
- lighting or photographic instructions when no positive photography direction has been approved;
- signature moves that merely repeat composition rules without defining a recognisable visible treatment;
- named fonts that are unavailable, unlicensed, missing required weights, or incompatible with the approved language;
- no accessible text-color role for one or more approved section surfaces;
- a system default conflicting with an explicit project answer, visual restriction, content requirement, or supplied asset reality.

- Ask exactly one question per turn when a blocking decision is genuinely missing.
- Do not reopen decisions already approved in the session files.
- Ignore non-website applications such as packaging or signage during this build.
- Use an explicit local placeholder for a missing non-blocking asset or integration.
- Do not invent a logo, licensed font, proof, customer result, or photography direction.
- Record implementation decisions and unresolved items in `09-build-notes.md`; do not create separate decision, copy, or prompt logs.

## Intentional design loop

Before coding, state in `09-build-notes.md` the page's purpose, priority visitor, main action, visual concept, and one recognisable quality carried from Visual Direction. Complete and approve the visual assembly checkpoint below before writing website code. Then work through four passes:

1. **Shape:** decide hierarchy, composition, density, rhythm, and the role of each visual element before styling details.
2. **Build:** implement the approved structure and copy with the simplest suitable code.
3. **Audit:** inspect the rendered page for usability, accessibility, responsiveness, source fidelity, and visual defects.
4. **Polish and harden:** fix hierarchy, spacing, wrapping, states, edge cases, and performance problems found in the audit.

Do not use visual novelty as a substitute for the approved concept. Avoid a generic stack of identical cards, default gradients, arbitrary rounded containers, or repeated centered sections unless Visual Direction specifically calls for them.

Content remains primary. `Low density`, `one idea per screen`, generous whitespace, short sentences, or a restrained visual system controls grouping and emphasis; it does not authorize deleting decision-critical content or stretching one generic sentence into an oversized section. Use content-driven section height. A deliberate brand-moment section may be sparse only when the surrounding page already carries the complete buying decision and the moment has a distinct narrative job.

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

Create `archetypes.css` when block 05 defines reusable archetypes; keep section-specific exceptions in `sections.css`. Create only files the website actually uses. Keep strategy and Visual Direction inputs in their existing locations; do not duplicate or edit them inside `site-v1/`.

## Translate Visual Direction into the website

The current Visual Direction export uses these blocks:

1. **Visual Foundation** — translate territory, tension, desired qualities, and prohibited qualities into the overall visual character and final review criteria.
2. **Name & Typography** — implement the approved brand-name casing, primary and secondary type roles, display/body scale, tracking, leading, italics, and typography restrictions. Use supplied licensed font files or an approved system fallback; do not fetch fonts from a CDN. A descriptive typeface direction is not a licensed font asset.
3. **Color System** — use the supplied color values, roles, proportions, allowed pairings, and prohibited combinations. Calculate text contrast from the actual exported values.
4. **Composition** — translate the approved grid, alignment, symmetry, density, margins, rhythm, spacing scale, layering, block treatment, dividers, and image/text ratios into responsive layout rules.
5. **Page Architecture** — supplies an upstream palette of visual archetypes, focal points, alternation, surface changes, alignment rules, and possibly a draft sequence. `/express-copy` or `/structure` reconciles that palette with the business argument and assigns compatible archetypes to stable section IDs. The later `07-website-structure.md` controls which sections exist, their order, their message jobs, proof placement, and the CTA path.
6. **Illustration & Materiality** — implement the approved illustration position and surface, paper, texture, grain, and material cues. Do not infer a positive photography style from this block.
7. **Graphic Language** — implement only the approved patterns, separators, frames, borders, devices, and repeated motifs.
8. **Distinctive Visual Codes** — make the signature moves perceptible early and consistently. Use a coherent combination in the first viewport when it supports clarity; do not force every code into the hero when that weakens comprehension.
9. **Visual Restrictions** — treat every listed style, typography, composition, and photography prohibition as a review check.
10. **AI Visual Direction** — preserve the supplied base prompt, negative prompt, variable-by-piece guidance, fixed rules, and approval checklist without paraphrasing when image slots need a later generation handoff. Record them in `09-build-notes.md`; they are not permission to generate or approve imagery automatically.

If no photography direction exists, solve the site with approved typography, color, layout, graphic elements, illustration, and materials. Ask one question only when photography is essential to the approved content or offer. Otherwise use a clearly labelled local placeholder.

The archetypes in block 05 form a palette. Use only the archetypes supported by the actual content, proof, and assets. The exact section order always comes from the later `07-website-structure.md`; a dashboard draft, placeholder, or instructional text is not final architecture. Review block 09 together with the conceptual and visual boundaries in `06-brand-concept.md`, so a dashboard omission cannot erase an approved restriction.

### Direction precedence inside the export

When two instructions appear to differ, use this order:

1. explicit project answer or named non-negotiable rule;
2. explicit visual restriction;
3. system default, only where the project answer is silent;
4. expressive or derivable guidance, inferred conservatively from stronger decisions.

A system default never overrides an explicit project answer. For example, an answered six-column grid overrides a generic twelve-column desktop default; responsive implementation may derive compatible tablet and mobile behavior without changing the approved desktop character. Record each applied default or derived decision in `09-build-notes.md`.

Resolve every website-relevant item in `Still to define` or `Pendiente de definir` through an explicit answer, a named system default already present in the export, or `Not applicable` with a reason. Do not invent a new choice or treat a silent gap as approval.

### Visual assembly checkpoint

Create a compact implementation map in `09-build-notes.md` before coding:

| Section ID | Content job from `07` | Copy volume from `08` | Visual archetype from block 05 | Focal point | Surface/alignment/columns | Density | Rule checked |
|---|---|---|---|---|---|---|---|

Below the table add two compact low-fidelity wireframes, one near 390 px and one near 1440 px. They may be ASCII outlines. Show section boundaries, column or stacking behavior, focal element, major image slot, background change, and intentional empty space. They must make repeated composition and mobile-order problems visible before styling.

Check every explicit alternation, centering, focal-point, surface, and archetype rule against the map. Also compare the approximate surface allocation with the exported color proportions. Treat proportions as directional unless the export explicitly requires measurement; do not distort content merely to hit a percentage.

Show the participant only the design intent, the map, the two wireframes, material conflicts or defaults, and one confirmation-or-correction question. Wait for approval before writing website code. Keep all detail in `09-build-notes.md`; do not create `LAYOUT.md`, `DECISIONS.md`, `COPY.md`, or `IMAGE-PROMPTS.md`.

Apply every explicit `non-negotiable` rule from block 05 unless it would break accessibility, hide or reorder approved content, falsify the CTA hierarchy, or conflict with a material requirement in blocks 01–04 or 09. When a conflict exists, preserve the business and accessibility requirement, document the exact conflict, and ask one decision question only if the visual resolution materially changes the result.

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
- Record each missing image slot, intended purpose, aspect ratio, applicable AI Visual Direction, and prohibited treatments in `09-build-notes.md`.

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

Compare each rendered viewport with the approved compact wireframe. For a grid-driven layout, provide a review-only grid overlay such as `?grid=1` when it can be implemented without affecting the normal page; use it to inspect columns, margins, and intentional exceptions. The overlay is an implementation aid, not customer-facing UI.

Treat content or controls hidden or overlapping, an unusable primary action, broken navigation or forms, unreadable text, obstructive horizontal overflow, and severe mobile collapse as **Blockers**.

Treat systematic misalignment, inconsistent containers, visibly broken spacing, accidental empty areas, poor line breaks, and repeated composition errors as **Important**, even when the page remains technically usable.

## Build verification

Before finishing `/build`:

1. Recheck block 09, **Visual Restrictions**, against the rendered site.
2. Check that the approved **Distinctive Visual Codes** are recognisable without obscuring the message or action.
3. Check that color dominance and accent use follow the documented proportions. Treat proportions as directional unless the export explicitly requires exact measurement.
4. Check that reusable brand colors, fonts, and size rules come from `tokens.css`.
5. Check every explicit block 05 alternation, focal-point, centering, archetype, surface, and approximate color-allocation rule against both the section attributes and the full rendered page; record each as `Pass`, `Adapted with reason`, or `Blocked`. Use a lightweight DOM check when local browser tooling is available; otherwise record the manual evidence. Do not add a permanent validation script solely to satisfy this step.
6. Compare the 390 px and 1440 px rendered pages with the approved wireframes and explain every material deviation. For grid-driven layouts, inspect the review overlay as well as the normal page.
7. Exercise the primary action and any local form states.
   Verify through the actual destination, stored record, or network response that the conversion was received. A visual success message alone is not evidence.
8. Inspect the complete rendered page at mobile, tablet, desktop, and any material breakpoint using the visual-layout-integrity checklist. Fix clear local defects before completing `/build`.
9. Record the approved wireframes, visual architecture map, rule-status checks, viewport sizes, rendered areas inspected, deviations, defects fixed, unresolved visual issues, derived implementation choices, missing assets, image prompt handoffs, and known limitations in `09-build-notes.md`.

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
