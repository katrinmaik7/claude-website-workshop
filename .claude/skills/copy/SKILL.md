---
name: copy
description: Create complete build-ready website copy as a separate stage in an active Full-path session after /structure. Express sessions use /express-copy instead.
---

# Website copy context

Read `CLAUDE.md`, every approved active-session stage file through `07-website-structure.md`, and these references:

- `.claude/references/SESSION-AND-EVIDENCE.md`
- `.claude/references/CONVERSION-STRATEGY.md`
- `.claude/references/WEBSITE-STRUCTURE.md`
- `.claude/references/BRAND-CONCEPT.md`
- `.claude/references/WEBSITE-COPY.md`

Use the approved `06-brand-concept.md` from the active session. Inspect relevant founder writing samples and customer-language material in `assets/` without modifying them.

This stage owns the content and exact words of the website. It does not define or change visual brand direction.

## Entry gate

Run the mandatory progression gate in `CLAUDE.md`. Require `Path: Full`, `Next command: /copy`, and every stage through a complete approved `07-website-structure.md`, including stable page and section IDs. If anything is incomplete, name the earliest unfinished command. Do not silently create a new architecture or reconstruct brand decisions inside this stage.

Use the website language approved in the session. If it is unresolved, ask one language question before drafting.

Require `07-website-structure.md` to name the conversion implementation state, exact destination, stored data or completed action, owner, confirmation, and launch consequence. If these are missing, stop and return to `/structure`; do not solve the gap with persuasive microcopy.

If a `Prototype only` structure requests discarded visitor input, a fake form, validation, submission, or confirmation, stop and return to `/structure`. Do not write copy that makes a nonexistent action feel real. If it displays an unsupported experiment price without a captured price-response test, omit it only when the approved structure explicitly allows omission; otherwise return to `/structure`.

If there is no suitable founder voice sample, proceed with a clear, natural voice based on the approved brand concept and audience language. Mention the missing sample only when it creates a material voice decision.

Skip questions already answered. Ask exactly one question per turn.

## Synthesize the copy foundation

Create an internal evidence ledger from all previous stages:

- priority visitor, situation, trigger, awareness, and desired progress;
- current alternatives and why they fall short;
- decision criteria, objections, anxieties, and trust needs;
- approved offer, mechanism, deliverables, price or commitment, fit boundaries, and CTA;
- offer status and conversion implementation state;
- positioning, differentiated value, proof, and prohibited claims;
- approved brand essence, personality behavior, voice rules, narrative pillars, expressions, and boundaries;
- sourced customer language and relevant search terms;
- page roles, section IDs, belief changes, proof placement, and CTA path.

Resolve no contradiction silently. Ask one decision question when conflicting approved files would materially change the copy.

Treat the brand concept as expression guidance. It cannot override audience evidence, approved positioning, offer conditions, proof limits, legal requirements, accessibility, or the website's conversion path. Brand narrative pillars are not automatically website claims.

## Direction and sample checkpoint

Before writing the full website, present at most three brief strategy bullets:

- one-sentence message strategy for the priority reader;
- primary promise and its evidence limit;
- voice direction, with the terms to preserve or avoid.

Then draft three materially different first-screen routes using the route method in `WEBSITE-COPY.md`. For each show only the customer-facing eyebrow, headline, subheadline, CTA, and optional proof or fit cue. Recommend one and explain the choice in one sentence. Do not mix evidence annotations, missing-proof notes, or internal strategy language into the displayed copy.

Also draft one polished evidence-heavy section, such as mechanism, proof, offer, or objection handling. Show customer-facing copy first, followed by a separate one-line internal note naming its evidence source and any blocker.

Apply the human-copy method before presenting it. Ask one question about the direction. Do not ask the participant to write the copy for you.

## Write the complete website

After direction approval, write exact, build-ready copy for every approved page and section ID. Include where relevant:

- SEO title, meta description, and social-preview text;
- navigation and utility labels;
- eyebrow, headline, subheadline, and supporting text;
- body copy, benefits, mechanism, comparison, and offer detail;
- proof introductions, exact approved quotations, captions, and qualifications;
- objection handling and genuine FAQ answers;
- primary and supporting CTA labels;
- form labels, instructions, helper text, validation errors, consent, confirmation, and follow-up text;
- footer, contact, trust, and required legal-navigation labels;
- internal placeholder annotations for missing content, proof, or integrations, clearly separated from final customer-facing copy.

System-state copy must be true. Use `Join`, `Reserve`, `Order`, `Book`, `Submitted`, or equivalent success language only when the action reaches a real destination and is stored or completed. For a prototype, use a specific navigation or exploration CTA and one concise disclosure only when needed to prevent misunderstanding. Do not repeat internal labels or research caveats across the page. A missing connection remains a launch blocker rather than a copy problem.

Keep placeholders and implementation notes outside the customer-facing copy. If a required price, term, proof item, or integration is unresolved, either return to its owning stage or omit the element when the approved structure allows it. Never publish “still figuring out,” “TBD,” “hypothesis,” “working preview,” or equivalent drafting language.

Use the stable IDs from `07-website-structure.md`. Do not add a page or section merely to fit unused research. Do not omit a structurally required section because its copy is difficult; flag the missing evidence or decision.

## Copy quality passes

Run the seven focused conversion sweeps in `WEBSITE-COPY.md`, then run these five integrity checks:

1. **Research traceability:** every material message follows from approved evidence or a confirmed decision.
2. **Conversion logic:** copy performs the section's belief job and moves toward the primary action without pressure or repetition.
3. **Human voice:** remove generic, inflated, formulaic, or AI-shaped writing while preserving meaning and useful nuance.
4. **Persuasive specificity:** reject generic headlines, interchangeable value statements, research-report language, weak CTAs, and body copy that merely repeats headings.
5. **Semantic integrity:** preserve facts, numbers, prices, quotations, necessary public qualifications, search terms, conditions, CTA destinations, and disclosures.

For launch copy, review once from the conversion, UX, skeptical target-visitor, and brand perspectives. Require a concrete reason for every requested change; do not use invented persona opinions as evidence.

Review explicit and implied claims created by copy combinations. Flag claims requiring specialist or jurisdictional review. Do not promise legal clearance, conversion uplift, or AI-detector results.

## Final checkpoint and save

Present a compact page-by-page preview: headline and one line per section, full copy for the first screen and the offer section. Add at most three unresolved items: claims needing qualification, missing proof, or placeholders. Ask one final approval question.

After approval, write only `08-website-copy.md` with:

1. source files and scope;
2. copy foundation and reader context;
3. message hierarchy and voice rules;
4. terminology, search language, and claim guardrails;
5. proof, objection, and CTA strategy;
6. complete build-ready copy organized by page and stable section ID;
7. form, error, confirmation, follow-up, and utility microcopy;
8. asset, proof, integration, and specialist-review requirements;
9. research-to-copy traceability table;
10. semantic-integrity report;
11. approved decisions and unresolved questions.

Update `SESSION.md`. Do not edit earlier stage files.

Finish with the approved copy direction, saved file, and unresolved content blockers. Then give this concise handoff using the exact active-session paths:

1. Open the Visual Direction tool.
2. Use `06-brand-concept.md`, `07-website-structure.md`, and `08-website-copy.md` from the active session as inputs.
3. Save the completed export as `assets/brand/visual-direction.md` and add any required visual assets.
4. Run `/build`.

## Quality gate

- Every approved page and section ID has final copy or an explicit evidence gap.
- A visitor can identify relevance, credible value, offer, proof, fit, and action without reading internal research language.
- Headlines are specific to this audience, offer, and situation.
- A relevant competitor could not paste the hero unchanged onto its own website.
- Material claims trace to evidence and retain necessary qualifications.
- Proof is introduced in the context of the claim it supports.
- Objections are answered where they arise rather than hidden in a generic FAQ.
- CTA and form microcopy describe what happens next.
- CTA, loading, validation, confirmation, and follow-up copy match the actual implementation state.
- Copy is clear, natural, scannable, and consistent without invented personality.
- Internal evidence labels, validation notes, drafting commentary, and implementation placeholders do not appear as marketing copy.
- Search language serves the reader and is not repeated mechanically.
- No fact, quote, number, price, condition, disclosure, or destination changed during humanization.
- The file can be handed to a designer or builder without asking Claude to reconstruct the strategy.
