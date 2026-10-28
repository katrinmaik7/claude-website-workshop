# Visual brand input

This folder receives the completed Visual Direction export and the real assets needed to implement it. The workshop creates the approved brand concept inside the active session as `06-brand-concept.md`; do not duplicate it here.

## Required before `/express-copy` or `/structure`

After `/brand-concept`, complete the eight blocks in the Brandbook OS Visual Direction tool, then choose the page format on its result screen:

1. Visual Foundation
2. Name & Typography
3. Color System
4. Composition
5. Page Architecture
6. Illustration & Materiality
7. Graphic Language
8. Visual Restrictions

The export adds `09. Page Format & Structure` from the format selector. `.claude/references/BRANDBOOK-OS-MAP.md` describes every block, option, and exported sentence.

Also keep the export's `Still to define`, `Responsive — desktop and phone, non-negotiable`, and `Instructions for AI` sections. Resolve each website-relevant pending item with an explicit answer, a named system default already present in the export, or `Not applicable` with a reason. Never leave the choice silent.

The question guide is provided inside the tool. Add the completed export to this folder, not the unfilled guide.

Use the active session's approved `06-brand-concept.md` and its research and offer files as context. They supply the factual business context, approved positioning, brand character, distinctive-code candidates, boundaries, name state, proof limits, and image restrictions.

The dashboard's **Page Architecture** answer is a visual composition proposal at this point: one section recipe with its hero and alternation rules. Its recipe run is a visual pattern, not the final information architecture. `/express-copy` or `/structure` will reconcile it with the complete research, offer, objections, proof, CTA path, and copy volume.

Download the completed ZIP. Your computer may unzip it automatically. Find the language-specific Markdown file inside, such as `visual-direction-en.md` or `visual-direction-es.md`, move it into this folder, and rename it exactly:

`visual-direction.md`

The final path must be `assets/brand/visual-direction.md`. Keep the Markdown file, not the ZIP, at that path. `/express-copy` or `/structure` reads it before deciding the final architecture, and `/build` reads it again for implementation.

## Implementation assets

The Markdown export describes the system; it does not replace the actual assets. Also add everything the approved direction requires, such as:

- logo files and usage variants;
- licensed font files or web-font sources;
- approved photographs and imagery, when separately defined;
- illustrations and icons;
- ownership and licensing notes;
- relevant Figma, Canva, or design-system links;
- website-specific responsive or motion guidance when available.

You may organize these in subfolders such as `logos/`, `fonts/`, `images/`, `illustrations/`, and `icons/`. Keep `visual-direction.md` at the top of `assets/brand/` so Claude can find it reliably.

The **Page Architecture** block proposes visual section archetypes, focal points, alternation, and composition. The later `07-website-structure.md` becomes the final source for page list, section IDs, section order, belief journey, proof placement, and CTA path. `/express-copy` or `/structure` maps suitable visual rules to stable IDs and records any visual suggestion it changes because the business argument, evidence, assets, accessibility, mobile layout, or content volume requires it.

A section recipe is a visual palette, not a requirement to use every section type. Do not assign a figures band, quote, comparison, image layout, or similar component unless the approved research, structure, copy, proof, and supplied assets contain what it needs. Neither the recipe run nor the fallback order of parts in block 09 overrides the later exact order in `07-website-structure.md`.

Treat the completed visual files as read-only. Claude may implement them during `/build` but must not silently redesign the identity.

The Visual Direction export does not define photography direction. If photography is essential to the approved website content, add explicit direction or leave a clearly labelled placeholder. Do not infer a photo style from the illustration and materials block.
