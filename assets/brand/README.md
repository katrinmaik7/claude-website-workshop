# Visual brand input

This folder receives the completed Visual Direction export and the real assets needed to implement it. The workshop creates the approved brand concept inside the active session as `06-brand-concept.md`; do not duplicate it here.

## Required before `/build`

After `/express-copy` or `/copy`, complete all ten blocks in the Visual Direction tool:

1. Visual Foundation
2. Name & Typography
3. Color System
4. Composition
5. Page Architecture
6. Illustration & Materiality
7. Graphic Language
8. Distinctive Visual Codes
9. Visual Restrictions
10. AI Visual Direction

Also keep the export's `Still to define` / `Pendiente de definir` and `Instructions for AI` / `Instrucciones para la IA` sections. Resolve each website-relevant pending item with an explicit answer, a named system default already present in the export, or `Not applicable` with a reason. Never leave the choice silent. Block 10 is already written by the Visual Direction tool; do not rewrite its base or negative prompts.

The question guide is provided inside the tool. Add the completed export to this folder, not the unfilled guide.

Use these three workshop files as context:

- `sessions/<your-session>/06-brand-concept.md`;
- `sessions/<your-session>/07-website-structure.md`;
- `sessions/<your-session>/08-website-copy.md`.

Download the completed export and save it here with the exact name:

`visual-direction.md`

`/build` reads that file automatically.

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

The **Page Architecture** block controls visual section archetypes, focal points, alternation, and composition. It does not replace the page list, section order, belief journey, or CTA path approved in `07-website-structure.md`. Apply its visual rules to the stable section IDs and make sure they accommodate the actual content volume in `08-website-copy.md`.

Treat the completed visual files as read-only. Claude may implement them during `/build` but must not silently redesign the identity.

The Visual Direction export does not define photography direction. If photography is essential to the approved website content, add explicit direction or leave a clearly labelled placeholder. Do not infer a photo style from the illustration and materials block.
