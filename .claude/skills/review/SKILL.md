---
name: review
description: Audit the local website against approved strategy, conversion clarity, evidence integrity, accessibility, usability, trust, and technical readiness, then prioritize fixes. Use after a website build or before launch.
---

# Launch Review

Read `CLAUDE.md`, all active session stage files, `assets/brand/visual-direction.md`, `.claude/references/SESSION-AND-EVIDENCE.md`, and `.claude/references/WEBSITE-QUALITY.md`. Inspect the complete local website in `site-v1/` and the approved implementation assets in `assets/brand/`.

## Entry gate

Run the mandatory progression gate in `CLAUDE.md`. Require `Next command: /review`, complete approved stage files through `09-build-notes.md`, and a non-empty `site-v1/` containing the built website. If anything is incomplete, stop and direct the participant to `/build` or the earliest unfinished command.

## Review

Evaluate:

- five-second clarity and message match with the expected traffic source;
- fit with priority audience, situation, and desired progress;
- consistency with offer and positioning;
- fidelity to the approved brand concept and visual direction without weakening comprehension;
- compliance with the block 05 visual architecture map, including section archetypes, focal points, alternation, centering, surface changes, and any explicit non-negotiable rules;
- clarity of message hierarchy and primary action;
- claim-to-proof match;
- objections, trust, and transparent limitations;
- form and post-action experience;
- whether the primary action reaches its exact destination and produces the promised stored record or completed action;
- responsive usability and rendered visual integrity across the complete page;
- container and grid alignment, spacing rhythm, section transitions, text wrapping, overlap, clipping, stacking, image cropping, and breakpoint behavior;
- accessibility checks described in the quality reference;
- links, metadata, content completeness, measurement requirements, privacy, and integration gaps.
- whether the visual result expresses the approved concept and one recognisable quality instead of falling back to generic repeated cards, arbitrary gradients, or repeated centered sections.

Inspect the complete rendered page at the viewport sizes required by `WEBSITE-QUALITY.md`, including mobile, tablet, desktop, and any material breakpoint. Scroll through every section rather than checking only the first viewport. Interact with navigation and the primary path. Distinguish manual checks, automated checks, and items not tested. Do not claim WCAG compliance or conversion impact without adequate evidence.

For each block 05 rule, verify the rendered result rather than accepting the build notes. Report `Pass`, `Adapted with reason`, or `Failed`, and explain any conflict with content hierarchy, accessibility, responsiveness, or conversion clarity.

When rendering or visual inspection is unavailable, record `Visual QA not completed` as a launch blocker. Do not infer that the layout is acceptable from source code alone.

Review four readiness layers separately:

1. **Research readiness:** audience and problem evidence, contradictions, and remaining direct validation.
2. **Commercial readiness:** offer status, price basis, costs, fulfillment, capacity, and viability unknowns.
3. **Conversion-instrument readiness:** destination, persistence or completed action, consent/privacy, confirmation, ownership, and measurement.
4. **Website readiness:** copy, usability, accessibility, full-page visual layout integrity, visual fidelity, responsiveness, metadata, links, and technical behavior.

An unconnected primary action is always a `Blocker` when the stated objective is leads, waitlist signups, bookings, reservations, purchases, votes, preferences, or any captured learning. Visual confirmation alone is not evidence of a successful conversion. Launch readiness cannot be `Ready` until the action is connected and verified, or until the objective and all relevant copy are explicitly changed to a non-collecting prototype.

On a public `Prototype only` page, discarded-input forms, fake preference capture, fake validation, fake submission, and fake confirmation are `Important` at minimum and `Blocker` when they could make a visitor believe an action occurred. Replace them with a useful exploration path.

## Findings

Use `Blocker`, `Important`, and `Improve`. For each issue state:

- location;
- evidence;
- consequence;
- specific fix;
- whether it can be fixed locally or needs participant input.

Fix clear local defects that do not change approved strategy. Ask before making a strategic or externally consequential change.

## Save

Write only `10-launch-audit.md`. Include passes as well as failures, the four readiness layers, a viewport-by-viewport visual QA table, offer status, remaining research and economics gaps, evidence from testing the actual conversion path, launch readiness, and the next three actions in priority order. Update `SESSION.md`.

Finish with readiness status, blockers, saved file, and a reminder that publishing requires an explicit request.
