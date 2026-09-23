---
name: express-copy
description: Design a one-page website structure and write complete build-ready copy in a single stage from the approved research, brand concept, and Visual Direction. Use after Visual Direction in an Express session instead of /structure and /copy; produces 07-website-structure.md and 08-website-copy.md.
---

# Express copy (structure + copy)

Read `CLAUDE.md`, all active session stage files through `06-brand-concept.md`, `assets/brand/visual-direction.md`, and these references: `.claude/references/SESSION-AND-EVIDENCE.md`, `.claude/references/CONVERSION-STRATEGY.md`, `.claude/references/WEBSITE-STRUCTURE.md`, and `.claude/references/WEBSITE-COPY.md`. Inspect founder writing samples, customer-language material, and approved visual assets in `assets/` without modifying them.

## Entry gate

Run the mandatory progression gate in `CLAUDE.md`. Require `Path: Express`, `Next command: Complete Visual Direction`, every Express stage through a complete approved `06-brand-concept.md`, and a complete active-project `assets/brand/visual-direction.md`. If anything is incomplete, name the earliest unfinished step. Do not recreate the missing stage here. When the visual gate passes, mark Visual Direction `Approved`, mark Structure and copy `In progress`, and continue.

## Visual input contract

Use Visual Direction before finalizing the information architecture. Block 05 Page Architecture supplies possible section archetypes, focal rules, alternation, density, surface, alignment, and draft visual sequence. It does not own the final page list, section IDs, argument order, proof placement, CTA path, or the amount of decision-critical content.

Reconcile the block 05 proposal with the research-backed belief journey. Preserve useful visual intent, but change, omit, or reassign an archetype when it lacks the required proof or asset, cannot hold the real copy volume, harms mobile comprehension, or conflicts with the conversion path. Never ask the participant to decide the section order a second time unless two materially different research-supported routes remain; present the routes and one recommendation when that happens.

## Defaults

- One page. Add a separate page only for a legal or privacy requirement, and only as a stub.
- Website language: the one approved in the session; ask once if unresolved.
- Ask at most one further question, only if unknown: “What exactly should happen after the main button: where does the person go, what is recorded or completed, who owns it, and what happens next?” Recommend the smallest mechanism appropriate to the approved business goal; do not default to a communication channel. If no real mechanism is supplied, set `Connection required before launch` and keep it as a blocker. Use `Prototype only` only when the participant explicitly asks for a presentation-only page after seeing the lost CTA, follow-up, and learning.

## Context coverage

Before designing the structure, build the upstream-context ledger from `WEBSITE-COPY.md`. Reverse-scan every approved Express input:

- `00-setup-and-vision.md`: founder intent, starting situation, desired change, traffic assumption, language, action, and boundaries;
- `02-research.md`: alternatives, customer language, audience situations, objections, trust signals, contradictions, safe claims, and unknowns;
- `04-offer-and-positioning.md`: offer status, mechanism, deliverables, price or commitment, fit, exclusions, proof, differentiation, and claim limits;
- `06-brand-concept.md`: essence, personality behavior, voice, messaging, distinctive-code candidates, and boundaries;
- `assets/brand/visual-direction.md`: visual archetypes, composition constraints, assets, and restrictions to reconcile with the final content architecture;
- relevant participant materials in `assets/`: founder voice, customer language, proof, constraints, and exact facts.

Mark each material item `Used`, `Guardrail`, `Intentionally excluded`, or `Blocked`, with a source pointer and destination section when used. Do not put every answer on the website; require a reason when relevant context is omitted. Resolve no contradiction silently.

Import the `D1`–`D10` Website message handoff from `06-brand-concept.md`. Create a content-coverage map that assigns every applicable ID to at least one public section, interaction, or justified guardrail. The map must name the exact customer-facing consequence; a source citation or internal note alone is not coverage.

## Structure

Design the belief journey for the priority visitor arriving from the expected traffic source: arrival → relevance → value → mechanism → difference → proof → offer and fit → risk → action → confirmation. Give every section a stable ID (`S01-hero`, `S02-situation`, …), a visitor question, a belief change, an evidence source, a claim limit, and a CTA or next question. Remove any section without a research-backed job. Place proof next to the claim it supports and objections where they arise.

The first screen must state the concrete offer or mechanism, not only an emotional promise. When the meaningful difference depends on an alternative, give the comparison enough space to help the visitor decide rather than hiding it in a small note. Give `D7` a visible reason-to-believe treatment through actual proof, specification, provenance, process, or transparent operating standard. End with a closing section that repeats the real primary action and explains what happens next.

Record the conversion implementation state as `Connected`, `Connection required before launch`, or `Prototype only`. Specify the exact destination, stored data or completed action, owner, consent/privacy need, success evidence, error state, and follow-up. Do not describe an unrecorded click as demand validation.

Do not silently downgrade an approved `Test offer` or measurable website objective to prototype review merely because the destination is not connected yet. Show the participant the concrete consequence in the checkpoint: what CTA, learning, follow-up, and launch capability will be lost. Preserve the intended conversion and use `Connection required before launch` unless the participant explicitly changes the website objective after seeing that consequence.

For an explicitly requested `Prototype only` page, use a useful on-page destination and request no discarded input. Do not create a fake form, preference picker, validation, submission, or confirmation. State availability naturally once. Keep the complete approved proposition visible. A participant-approved experiment price may use one approved customer-facing qualifier such as `Expected price: €12` or `Around €12`; keep the evidence status internal. Lack of tracking is never by itself a reason to remove the offer, price, meaningful difference, fit, or objections from the page.

## Research-payoff gate

Before the structure checkpoint, prove that the research changes the public website. Map visible content to all applicable categories:

1. the priority audience's concrete situation or trigger;
2. the real alternative or status-quo friction;
3. the differentiated mechanism and why it matters;
4. the complete offer, including deliverables and approved price or commitment;
5. a reason to believe, process evidence, specification, provenance, or transparent current status;
6. researched objections, fit boundaries, and trade-offs;
7. one meaningful next action and what happens after it.

Do not satisfy this gate with internal annotations or a traceability table alone. The relevant insight must materially affect customer-facing wording, content, or interaction. If removing `02-research.md` and `04-offer-and-positioning.md` would leave substantially the same page, the structure and copy are too weak to approve.

## Checkpoint 1 — structure and first screen

Show at most five bullets: the section list with IDs and one-line jobs, the CTA path with conversion implementation state, the strongest research-derived difference, the strongest objection and its honest answer, and the biggest missing proof, asset, or launch blocker. If the proposed state removes a previously approved test, name exactly what would disappear and what business learning would be lost. Then show three materially different customer-facing first-screen routes from `WEBSITE-COPY.md`, recommend one, and ask one confirmation or correction question. Keep evidence annotations and internal research language outside the displayed copy.

After confirmation, retain the approved structure for this stage but do not save it yet. This allows the final copy review to correct a section job, order, or CTA path without leaving the structure file inconsistent.

## Write the copy

Write exact, build-ready copy for every section ID: navigation labels, eyebrow, headline, subheadline, body, proof introductions and exact approved quotations, offer details, objection answers, CTA labels, form labels, validation, consent, confirmation, footer and legal labels, SEO title, meta description, and social preview. Keep missing proof, integration notes, and implementation placeholders in internal requirements rather than customer-facing copy.

Use `Join`, `Reserve`, `Order`, `Book`, `You're on the list`, or equivalent success language only when the action is genuinely connected and persisted or completed. For an explicitly requested presentation-only prototype, use a specific exploration CTA and natural availability wording. Never publish `concept preview`, `prototype`, `demo only`, `proposed launch price`, `there is no list to join`, “we are testing,” “working preview,” `TBD`, evidence labels, or similar internal commentary. For `Connection required before launch`, treat the missing connection as a launch blocker.

If price is experimental, follow `WEBSITE-COPY.md`: use one natural approved qualifier and never present it as a validated live price. Do not combine `proposed`, `about`, and `expected`. Capturing a response determines whether the page tests price; it does not determine whether the approved price can be communicated.

Use FAQs only for genuine remaining questions that were not answered more effectively in the mechanism, offer, comparison, proof, or action sections. Do not turn every internal uncertainty into a public FAQ.

Run the seven focused conversion sweeps and the five integrity checks from `WEBSITE-COPY.md`. Freeze facts, prices, quotations, necessary public qualifications, and CTA destinations before editing. For launch copy, add the conversion, UX, skeptical target-visitor, and brand perspectives; every requested change needs a concrete reason.

## Checkpoint 2 — copy

Show the complete customer-facing one-page copy in reading order: every heading, body paragraph, list, offer detail, proof or transparent-status line, objection answer, CTA, form field, disclosure, and footer text. Hide internal tables and annotations from this preview. Then add at most three unresolved items: missing proof, placeholders, or claims needing qualification. Ask one final approval question. Do not ask the participant to approve a summary when the full copy is what will be built.

## Save

After approval, write both files:

1. `07-website-structure.md` in compact form: objective and conversion event; conversion implementation state; destination, stored data or completed action, owner, consent/privacy, confirmation and error path; audience, traffic, and device assumptions; belief journey; section plan with IDs; first-screen requirements; claim-to-proof placement; objections; mobile priorities; analytics events; assumptions and exclusions.
2. `08-website-copy.md` using the output structure in `WEBSITE-COPY.md`, including the upstream-context coverage table, research-to-copy traceability table, and semantic-integrity report.

Include the final `D1`–`D10` content-coverage map in both files: `07` maps IDs to section jobs and interactions; `08` maps IDs to exact public wording.

Ensure the final section IDs, order, and CTA path match across both files. Update `SESSION.md` once after both files are saved.

Finish with the saved files, the largest remaining blocker, and “Next: `/build`”.

## Quality gate

- A first-time visitor can identify what this is, who it is for, the credible value, and the next action from the first screen.
- Every section ID has final copy or a named evidence gap.
- Every material upstream item has a source pointer and a coverage status; nothing material was dropped silently.
- The public page passes the research-payoff gate; the traceability table is evidence of use, not a substitute for visible value.
- No approved offer detail, price, difference, or fit information was removed solely because analytics, a form, or another destination is not connected.
- A `Test offer` remains a measurable test or an explicit `Connection required before launch`; any move to `Prototype only` records the participant's informed objective change and its lost learning.
- Every public section adds new decision value. A large section may not merely restate its heading, hero promise, or another section in different words.
- Concise brand voice changes sentence form, not the amount of decision-critical content.
- Material claims trace to `02-research.md` or `04-offer-and-positioning.md` and keep their qualifications.
- A relevant competitor could not paste the hero unchanged onto its own website.
- One primary CTA; its implementation state, destination, persistence, confirmation, and launch consequence are explicit.
- The primary CTA leads beyond an internal scroll, appears in the first screen and closing section, and states what the visitor receives next.
- A visible comparison carries the researched alternative when differentiation depends on it, and a visible reason to believe supports the main promise.
- No customer-facing sentence exposes internal prototype, research, price-status, evidence, or missing-integration language.
- No prototype interaction simulates a successful real-world conversion.
- Internal research labels, drafting commentary, and implementation placeholders do not appear as marketing copy.
- No fact, quote, number, price, condition, or destination changed during the human-voice pass.
- The final section order follows the research-backed belief journey; every block 05 archetype used has compatible content, proof, assets, and mobile behavior.
