---
name: build
description: Build the first local website from the active session's approved strategy, brand concept, structure, copy, and Visual Direction without publishing it. Runs start to finish without asking the participant anything. Use after copy and visual inputs are ready.
allowed-tools: Read Write Edit Glob Grep Bash(mkdir *) Bash(cp *) Bash(unzip *) Bash(curl *)
---

# Build

Read `CLAUDE.md`, the active session's `SESSION.md` and stage files through `08-website-copy.md`, `.claude/references/WEBSITE-QUALITY.md`, `.claude/references/BRANDBOOK-OS-MAP.md`, and the completed Visual Direction export and implementation assets in `assets/brand/`.

## Run without questions

`/build` asks the participant nothing. The approved session files and the participant's Visual Direction export are the complete brief. Do not ask for approval, confirmation, preferences, or missing information, and do not pause between steps. Resolve every open item with the rules below, record each resolution in `09-build-notes.md`, and finish the website in the same run. `/review` reports anything that still needs a human decision.

Stop only when a required input does not exist at all: an approved `07-website-structure.md`, an approved `08-website-copy.md`, or any Visual Direction export (see below). Then name the missing file and the exact command or step that creates it in one short message.

When sources disagree, decide in this order and record the decision:

1. keep approved content, proof limits, truthful claims, accessibility, and the primary action intact;
2. follow the source authority below and the direction-precedence rule in `WEBSITE-QUALITY.md`;
3. if still tied, choose the more conservative option: the export's system default, fewer elements, or the option closer to the block 01 keywords.

The export's `Instructions for AI` say to ask when something material is missing. During `/build`, apply this decision order instead.

## Source authority

Use the ownership rules in `WEBSITE-QUALITY.md`:

- approved upstream stages own audience, offer, positioning, proof, and claim limits;
- `06-brand-concept.md` owns brand meaning, voice, messaging, and conceptual boundaries;
- `07-website-structure.md` owns pages, section order, section roles, and the CTA path;
- `08-website-copy.md` owns the exact customer-facing wording;
- `assets/brand/visual-direction.md` owns visual execution.

Do not replace the approved structure with a generic landing-page sequence. Do not rewrite approved copy during layout. Do not let visual choices weaken comprehension, proof integrity, accessibility, or the primary action.

## Visual Direction export

`BRANDBOOK-OS-MAP.md` describes the mold every export comes from: `00. Brand copy and voice` (optional), blocks `01`–`08`, `09. Page Format & Structure`, `Still to define`, `Responsive — desktop and phone, non-negotiable`, and `Instructions for AI`. Use its option tables to tell a catalog option from an *Other* answer, a note, or an unanswered field. Never fill an unanswered field with the dashboard's *Suggest one* option; apply the block's system default when one exists, and otherwise derive conservatively from blocks 01–04.

There are no other blocks. `Distinctive Visual Codes`, `AI Visual Direction`, a `Section order` field, and `Visual Restrictions` numbered as block 09 belong to an earlier export format. Visual restrictions are block 08, and there are no image-generation prompts to hand off.

The map is written for the dashboard on its own. In this workshop the approved session files come first:

- `08-website-copy.md` is the brand copy. Section `00`, when present, is earlier voice input; when it differs from `08` on public wording, `08` wins. Never stop or ask for copy because `00` is missing.
- `07-website-structure.md` owns sections, order, the goal, and the primary action. Do not use `09` point 2 or the fallback order in `09` point 3.
- Honor the `09` point 1 format. For `From your copy`, apply the map's word-count rule to `08`. When `Single screen, chosen by the brand` cannot hold the sections approved in `07`, build a scrolling landing whose first screen is a complete single-screen composition (hero and primary action within `100svh`), and record the adaptation. Never drop approved content to fit one screen.
- Apply `09` point 4 navigation unless `07` defines navigation.
- Block 05 `Section archetypes` is one recipe (`Editorial`, `Alternating`, `Grid`, or `Cinematic`) or an *Other* text. Its hero line defines the hero; its run is the vocabulary for the remaining sections, not their order. The `Alternation rules — non-negotiable` and the accordion pattern always apply.
- The visual assembly plan below is the numbered structure that `09` asks for before building.

### Find the export

Use `assets/brand/visual-direction.md`. If it is missing, use the participant's export where it is, without renaming or moving anything:

- exactly one `visual-direction-*.md`, such as `visual-direction-en.md`, in `assets/brand/`, the active session folder, or the project root → read that file;
- several → the most recently modified one whose block 02 `Brand name` matches the active project, otherwise the most recent;
- only a ZIP containing an export → read the Markdown inside it (for example with `unzip -p`) without extracting into `assets/`.

Record which file was used in `09-build-notes.md`. If no export exists anywhere, stop as described above.

## Pre-build check

Run the mandatory progression gate in `CLAUDE.md`. Require every stage file for the recorded path through complete approved `06-brand-concept.md`, `07-website-structure.md`, and `08-website-copy.md`.

Run the research-payoff and subtraction tests in `WEBSITE-COPY.md` against the customer-facing copy, compare the `D1`–`D10` coverage maps in `06`, `07`, and `08`, and apply the decision-density test to every section. Build with the approved copy as written. Record every gap under `Copy findings for /review` in `09-build-notes.md`: an omitted audience situation, alternative friction, differentiated mechanism, complete offer or approved commitment, reason to believe or transparent status, researched objection, fit, or meaningful action; a section that only repeats a slogan; or an approved price, difference, or offer detail removed because a destination is not connected. A traceability table does not compensate for generic or missing public content, so never mark such a gap resolved.

Never render evidence labels, internal notes, or implementation commentary that leaked into `08`; record each omission. When approved customer-facing text contains internal language such as `concept preview`, `prototype`, `demo only`, `proposed launch price`, or `there is no list to join`, keep the approved wording and record it as a copy finding. When the primary CTA only scrolls to another section on a launch-oriented or conversion-focused page, or the closing section has no action, use the real destination recorded in `07` if one exists; otherwise keep the approved action and record the missing destination as a launch blocker.

If an upstream `Test offer` or measurable objective became `Prototype only` without a recorded participant decision that names the lost CTA, follow-up, and learning, implement `Connection required before launch` instead and record it.

Then run a cross-source visual consistency check:

- compare the name state, desired perception, distinctive codes, image policy, and every brand boundary in `06-brand-concept.md` with blocks 01, 02, 06, and 08; `06` wins on meaning and boundaries, the export on visual execution;
- compare the block 05 recipe and the `09` format with the exact section IDs, order, jobs, proof, CTA path, and copy volume in `07-website-structure.md` and `08-website-copy.md`;
- treat the block 05 recipe as a palette of section types; never force the Grid figures band, the Cinematic display quote, image rows, or a full-bleed image when the required content, proof, or asset does not exist;
- never use the recipe's run or `09` point 3 as a source of architecture; use `07-website-structure.md` instead;
- resolve direct internal conflicts, such as a block 01 keyword or another block answer contradicted by an anti-keyword or block 08, or explicit separators competing with explicit no-line rules, with the decision order above;
- calculate the declared text/background combinations, including the computed `Interface surfaces` and `Buttons and calls to action` in block 03. If a pairing fails WCAG AA for its intended text size, constrain it to a valid use or switch to an accessible text role from the palette; if no palette tone passes, derive a darker or lighter step of the Neutral as a semantic text role, not a new brand color;
- use the exported font families as described in `WEBSITE-QUALITY.md`; when the files cannot be obtained, use the exported stack.

If the export's block 02 `Brand name` does not match the active project, keep its visual decisions, use the name state from `06-brand-concept.md`, and record the mismatch for `/review`.

A later approved stage may resolve a specifically named open item from an earlier stage only when it records the participant's decision explicitly. Treat that as a resolution. Never infer a silent override. Record every reconciliation in `09-build-notes.md`.

Read the conversion implementation state from `07-website-structure.md`. `Connected` needs an exact destination and persistence/completion rule; without them, treat the action as `Connection required before launch` and record it. If it says `Connection required before launch`, build the interface only when useful but keep the missing connection as a launch blocker and do not show real-success language. If it says `Prototype only`, implement the approved exploration path and never simulate submission, reservation, purchase, booking, preference capture, or list entry.

Apply the direction-precedence rule in `WEBSITE-QUALITY.md`; do not let a system default override an explicit project answer. Use referenced logo, font, image, illustration, icon, and license files when they exist and clearly labelled local placeholders when they do not. Calculate contrast from exported color values rather than trusting a written ratio. Do not reopen approved decisions or consider non-website applications.

After this check, mark `/build` `In progress` in `SESSION.md` and continue.

## Visual assembly plan

Before writing website code, initialize `09-build-notes.md` and complete the plan in `WEBSITE-QUALITY.md`:

1. write the short intentional design statement;
2. map every approved content section to one section type from the block 05 recipe, focal point, surface, alignment, columns, and density;
3. check the explicit alternation rules and approximate color allocation, and fix any rule the map breaks;
4. draw compact 390 px and 1440 px wireframes.

Do not show the plan for approval or wait; continue straight to the build. Keep the plan in `09-build-notes.md`; do not create additional planning files.

## Build

- Record the short intentional design statement required by `WEBSITE-QUALITY.md`, then follow its Shape → Build → Audit → Polish and harden loop. Do not create a separate design document.
- Create the website only inside the active session's `site-v1/`.
- For an Express session, build a dependency-free static one-page site with semantic HTML, CSS, and minimal JavaScript. No framework, build step, external code CDN, or font CDN.
- For a Full session, implement the approved architecture with the simplest maintainable approach that supports its actual requirements.
- Centralize reusable visual values in `site-v1/styles/tokens.css` and follow the token, visual translation, asset, responsive, accessibility, and verification rules in `WEBSITE-QUALITY.md`.
- Use stable page and section IDs from `07-website-structure.md` to connect architecture, copy, visual applications, navigation, and review findings.
- Create and follow the visual architecture implementation map from `WEBSITE-QUALITY.md`. The block 05 recipe chooses visual section types and alternation for existing section IDs; it cannot add, remove, merge, or reorder the approved content architecture.
- Implement the recipe's reusable section types and the block 05 accordion pattern in `site-v1/styles/archetypes.css`; keep `sections.css` for genuine section-specific exceptions.
- Add the applicable inspection attributes from `WEBSITE-QUALITY.md` to every content section and mark exactly one focal element per section.
- Keep essential content and actions functional without JavaScript; use JavaScript only for progressive enhancement.
- Use approved supplied assets or clearly labelled local placeholders. Do not invent photography direction, brand assets, proof, testimonials, customer logos, statistics, scarcity, guarantees, or results.
- Use the block 05 accordion pattern wherever the approved copy offers collapsible options such as FAQs, plans, or steps.
- Obey the export's `Responsive — desktop and phone, non-negotiable` section as fixed rules.
- Treat every explicit block 05 `non-negotiable` rule as a rendered review requirement, with `Pass`, `Adapted with reason`, or `Blocked` recorded in `09-build-notes.md`.
- Implement the primary action according to its recorded state. For `Connected`, verify the real destination or persisted/completed action and truthful post-action state. For `Prototype only`, use a specific exploration action and a concise availability disclosure when needed. Never display `You're on the list`, `Reserved`, `Order confirmed`, or equivalent unless that result actually occurred.
- Repeat the exact primary action in the first screen and final conversion section. Explain what the visitor receives and what happens next. Do not substitute a slogan, `Opening soon`, or an internal page anchor for the final action.
- For a public `Prototype only` page, do not build discarded-input forms, fake preference capture, fake validation, or fake confirmation. Use the approved exploration CTA and on-page destination. Keep facilitated UX mock interactions separate from the public marketing page.
- Render language selectors only when each label leads to a complete implemented language version. Do not display decorative `EN`, `ES`, `CA`, or similar placeholders.
- Do not repeat the same image as the main focal asset in multiple large sections unless the approved visual direction gives that repetition a deliberate narrative job. Use an approved alternate asset, a detail crop with a distinct job, a non-image composition, or a labelled placeholder.
- Render and inspect the complete page using the visual-layout-integrity checklist in `WEBSITE-QUALITY.md`. Check mobile, tablet, desktop, and any width where the composition changes. Fix clear overlap, clipping, alignment, spacing, wrapping, stacking, and responsive defects before completing the build.
- Reject generic repeated-card or centered-section layouts that ignore the approved Visual Direction. Confirm that the result has one recognisable visual quality from the supplied direction without compromising clarity.
- Treat `low density`, `one idea per screen`, generous space, or concise voice as composition guidance. Do not delete, shrink, or visually trivialize decision-critical copy to satisfy it. Avoid oversized empty sections and arbitrary viewport-height blocks when the content does not warrant them.
- Give research-critical comparison and reason-to-believe content enough visual weight to affect the decision. Do not reduce them to tiny columns, captions, or footnotes while decorative manifesto copy dominates the page.
- Do not publish or deploy.

## Build notes

Create only `09-build-notes.md` in addition to the website. Begin it with:

```text
Stage: Build
Path: Express | Full
Status: Approved
Approved after checkpoint: Not applicable — /build runs without a participant checkpoint
```

Include:

- what was built and how to preview it;
- exact strategy, structure, copy, Visual Direction file, and asset sources used;
- the content-to-archetype map and compact 390 px and 1440 px wireframes;
- every decision made without the participant, with its source and reason;
- derived implementation decisions and their source;
- `Copy findings for /review`;
- missing content, proof, assets, licenses, and integrations;
- image slots with purpose, aspect ratio, and the prohibited treatments from block 08 and the block 01 anti-keywords;
- responsive, interaction, accessibility, contrast, and visual checks performed;
- exact viewport sizes inspected, wireframe deviations, visible layout defects found, and fixes applied;
- checks not performed and known limitations;
- conversion implementation state and evidence of destination, network response, stored record, or completed action; if unavailable, the exact launch blocker.

Set `Status: Approved` once the website exists, every fixable defect found in the checks has been fixed, and the notes are complete. Record anything the build could not fix or verify, including visual QA that could not be rendered, as a launch blocker or known limitation rather than holding back approval.

Update `SESSION.md`: `/build` `Approved` and `Next command: /review`.

Finish with the local result, preview instructions, saved locations, at most five bullets on the decisions made without the participant, and “Next: `/review`”.
