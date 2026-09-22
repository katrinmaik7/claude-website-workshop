---
name: build
description: Build the first local website from the active session's approved strategy, brand concept, structure, copy, and Visual Direction without publishing it. Use after copy and visual inputs are ready.
---

# Build

Read `CLAUDE.md`, the active session's `SESSION.md` and stage files through `08-website-copy.md`, `.claude/references/WEBSITE-QUALITY.md`, and the completed Visual Direction export and implementation assets in `assets/brand/`.

## Source authority

Use the ownership rules in `WEBSITE-QUALITY.md`:

- approved upstream stages own audience, offer, positioning, proof, and claim limits;
- `06-brand-concept.md` owns brand meaning, voice, messaging, and conceptual boundaries;
- `07-website-structure.md` owns pages, section order, section roles, and the CTA path;
- `08-website-copy.md` owns the exact customer-facing wording;
- `assets/brand/visual-direction.md` owns visual execution.

Do not replace the approved structure with a generic landing-page sequence. Do not rewrite approved copy during layout. Do not let visual choices weaken comprehension, proof integrity, accessibility, or the primary action.

## Pre-build check

Run the mandatory progression gate in `CLAUDE.md`. Require every stage file for the recorded path through complete approved `06-brand-concept.md`, `07-website-structure.md`, and `08-website-copy.md`.

Before visual work, run the research-payoff and subtraction tests in `WEBSITE-COPY.md` against the customer-facing copy. Stop and return to `/express-copy` or `/copy` when the page omits an applicable audience situation, alternative friction, differentiated mechanism, complete offer or approved commitment, reason to believe or transparent status, researched objections and fit, or meaningful action without a material evidence or decision blocker. A traceability table does not compensate for generic or missing public content. Also stop if an approved price, difference, or offer detail was removed solely because analytics or a destination is not connected.

Require matching `D1`–`D10` coverage maps in `06`, `07`, and `08`. Verify that every applicable ID reaches exact public copy and that every section passes the decision-density test. Do not begin visual assembly when a section only repeats a slogan or when the site would be substantially unchanged without the research.

If an upstream `Test offer` or measurable objective became `Prototype only`, require an explicit recorded participant decision that names the lost CTA, follow-up, and learning. Otherwise return to the owning structure stage and default to `Connection required before launch`.

Then require `assets/brand/visual-direction.md`. It must contain all ten current blocks from Visual Foundation through AI Visual Direction; each website-relevant item in `Still to define` or `Pendiente de definir` must be resolved by an explicit answer, a named system default already present in the export, or `Not applicable` with a reason. Confirm that the export and supplied assets match the active project's brand concept, structure, and copy rather than an earlier session.

Run a cross-source visual consistency check before approving Visual Direction:

- compare the name state, desired perception, distinctive codes, image policy, and every brand boundary in `06-brand-concept.md` with blocks 01, 02, 08, 09, and 10;
- compare block 05 with the exact section IDs, order, jobs, proof, CTA path, and copy volume in `07-website-structure.md` and `08-website-copy.md`;
- treat the block 05 archetype list as a palette unless the export explicitly maps archetypes to approved section IDs; never force figures, quotes, comparisons, or image layouts when their required content or proof does not exist;
- ignore a placeholder or instructional `Section order` value as a source of architecture and use `07-website-structure.md` instead;
- identify direct internal conflicts such as the same attribute appearing in both positive and negative direction, or explicit separators competing with explicit no-line rules;
- calculate the declared text/background combinations before approval. If a dominant pairing fails WCAG AA for its intended text size, constrain it to a valid use or select an accessible semantic text role from the approved palette; if neither is possible, ask one decision question;
- confirm that named fonts and weights are supplied or that an explicit approved fallback will be used.

A later approved stage may resolve a specifically named open item from an earlier stage only when it records the participant's decision explicitly. Treat that as a resolution. Never infer a silent override. Record every non-blocking reconciliation in `09-build-notes.md`; stop for one decision when a material conflict remains.

Read the conversion implementation state from `07-website-structure.md`. Require an exact destination and persistence/completion rule for `Connected`. If it says `Connection required before launch`, build the interface only when useful but keep the missing connection as a launch blocker and do not show real-success language. If it says `Prototype only`, implement the approved exploration path and never simulate submission, reservation, purchase, booking, preference capture, or list entry.

After this visual gate passes, mark Visual Direction `Approved` and `/build` `In progress` in `SESSION.md`, then continue. Do not mark `/build` approved until the website and `09-build-notes.md` both pass the build checks.

If `visual-direction.md` is missing, inspect `assets/brand/` before responding:

- if there is exactly one language-specific export such as `visual-direction-en.md` or `visual-direction-es.md`, stop with one short instruction to rename that file to `assets/brand/visual-direction.md`, then run `/build` again;
- if there is only a Visual Direction ZIP, stop with one short instruction to unzip it, move the exported Markdown file into `assets/brand/`, rename it `visual-direction.md`, then run `/build` again;
- otherwise stop with one short instruction to complete Visual Direction using the three approved session files, then place the exported Markdown file at `assets/brand/visual-direction.md`.

Do not treat a ZIP, language-specific filename, or incomplete export as an approved Visual Direction file.

Confirm that any `Instructions for AI` or `Instrucciones para la IA` section is preserved. Apply the direction-precedence rule in `WEBSITE-QUALITY.md`; do not let a system default override an explicit project answer. Verify that referenced logo, font, image, illustration, icon, and license files exist or have explicit placeholders. Calculate contrast from exported color values rather than trusting a written ratio.

If an unresolved issue materially changes the code, identify the decision owner and ask exactly one question. Do not reopen approved decisions, ask about non-website applications, or request a batch of setup answers. Apart from the mandatory visual assembly checkpoint below, begin without another permission question when there is no material conflict.

## Visual assembly checkpoint

Before writing website code, initialize `09-build-notes.md` and complete the checkpoint in `WEBSITE-QUALITY.md`:

1. write the short intentional design statement;
2. map every approved content section to one block 05 archetype, focal point, surface, alignment, columns, and density;
3. check the explicit alternation rules and approximate color allocation;
4. draw compact 390 px and 1440 px wireframes;
5. show the participant the proposed composition, material conflicts or defaults, and one confirmation-or-correction question.

Wait for approval. Do not code first and ask the participant to approve the layout afterward. Keep this checkpoint in `09-build-notes.md`; do not create additional planning files.

## Build

- Record the short intentional design statement required by `WEBSITE-QUALITY.md`, then follow its Shape → Build → Audit → Polish and harden loop. Do not create a separate design document.
- Create the website only inside the active session's `site-v1/`.
- For an Express session, build a dependency-free static one-page site with semantic HTML, CSS, and minimal JavaScript. No framework, build step, external code CDN, or font CDN.
- For a Full session, implement the approved architecture with the simplest maintainable approach that supports its actual requirements.
- Centralize reusable visual values in `site-v1/styles/tokens.css` and follow the token, visual translation, asset, responsive, accessibility, and verification rules in `WEBSITE-QUALITY.md`.
- Use stable page and section IDs from `07-website-structure.md` to connect architecture, copy, visual applications, navigation, and review findings.
- Create and follow the visual architecture implementation map from `WEBSITE-QUALITY.md`. Block 05 chooses visual archetypes and alternation for existing section IDs; it cannot add, remove, merge, or reorder the approved content architecture.
- When block 05 defines reusable archetypes, implement them in `site-v1/styles/archetypes.css`; keep `sections.css` for genuine section-specific exceptions.
- Add the applicable inspection attributes from `WEBSITE-QUALITY.md` to every content section and mark exactly one focal element per section.
- Keep essential content and actions functional without JavaScript; use JavaScript only for progressive enhancement.
- Use approved supplied assets or clearly labelled local placeholders. Do not invent photography direction, brand assets, proof, testimonials, customer logos, statistics, scarcity, guarantees, or results.
- Treat block 10 AI prompts as a future asset handoff, not permission to generate or approve imagery automatically.
- Treat every explicit block 05 `non-negotiable` rule as a rendered review requirement, with `Pass`, `Adapted with reason`, or `Blocked` recorded in `09-build-notes.md`.
- Implement the primary action according to its recorded state. For `Connected`, verify the real destination or persisted/completed action and truthful post-action state. For `Prototype only`, use a specific exploration action and a concise availability disclosure when needed. Never display `You're on the list`, `Reserved`, `Order confirmed`, or equivalent unless that result actually occurred.
- For a public `Prototype only` page, do not build discarded-input forms, fake preference capture, fake validation, or fake confirmation. Use the approved exploration CTA and on-page destination. Keep facilitated UX mock interactions separate from the public marketing page.
- Render and inspect the complete page using the visual-layout-integrity checklist in `WEBSITE-QUALITY.md`. Check mobile, tablet, desktop, and any width where the composition changes. Fix clear overlap, clipping, alignment, spacing, wrapping, stacking, and responsive defects before completing the build.
- Reject generic repeated-card or centered-section layouts that ignore the approved Visual Direction. Confirm that the result has one recognisable visual quality from the supplied direction without compromising clarity.
- Treat `low density`, `one idea per screen`, generous space, or concise voice as composition guidance. Do not delete, shrink, or visually trivialize decision-critical copy to satisfy it. Avoid oversized empty sections and arbitrary viewport-height blocks when the content does not warrant them.
- Do not publish or deploy.

## Build notes

Create only `09-build-notes.md` in addition to the website. Include:

- what was built and how to preview it;
- exact strategy, structure, copy, Visual Direction, and asset sources used;
- the approved content-to-archetype map and compact 390 px and 1440 px wireframes;
- derived implementation decisions and their source;
- missing content, proof, assets, licenses, and integrations;
- image slots with purpose, aspect ratio, applicable base and negative prompts, and prohibited treatments when relevant;
- responsive, interaction, accessibility, contrast, and visual checks performed;
- exact viewport sizes inspected, wireframe deviations, visible layout defects found, and fixes applied;
- checks not performed and known limitations.
- conversion implementation state and evidence of destination, network response, stored record, or completed action; if unavailable, the exact launch blocker.

Update `SESSION.md`.

Finish with the local result, preview instructions, saved locations, and “Next: `/review`”.
