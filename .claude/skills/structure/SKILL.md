---
name: structure
description: Design website architecture as a separate stage in an active Full-path session after /brand-concept. Express sessions use /express-copy for structure and copy together.
---

# Website structure and belief journey

Read `CLAUDE.md`, active session files through `06-brand-concept.md`, `.claude/references/SESSION-AND-EVIDENCE.md`, `.claude/references/CONVERSION-STRATEGY.md`, `.claude/references/BRAND-CONCEPT.md`, and `.claude/references/WEBSITE-STRUCTURE.md`.

## Entry gate

Run the mandatory progression gate in `CLAUDE.md`. Require `Path: Full`, `Next command: /structure`, and every stage through a complete approved `06-brand-concept.md`. If anything is incomplete, name the earliest unfinished command. Do not reconstruct or approve brand decisions inside `/structure`.

Act as a conversion-focused information architect. Design the route from the visitor's arrival context to the confidence required for one clear action. Do not start with a generic landing-page template.

## Establish missing context

Use approved session evidence first. In Workshop mode, ask only missing questions, exactly one per turn, in this order:

1. Where will the first visitors most likely come from, and what will they already know?
2. Are any pages, languages, or functions mandatory?
3. What exact destination follows the primary CTA, what data is saved there, and who receives or owns it?
4. Are there required legal, contact, scheduling, checkout, or accessibility constraints not yet recorded?

Skip anything already established. Accept `unknown`; record it as an assumption rather than inventing an answer.

Recommend one page or several from the evidence and constraints. Do not make the participant choose an architecture before seeing the reasoning.

## Define the architecture before sections

Determine:

- website objective and measurable conversion event;
- conversion implementation state: `Connected`, `Connection required before launch`, or `Prototype only`;
- priority visitor, entry source, awareness, device, and decision context;
- one primary action and any genuinely supporting secondary action;
- first-screen comprehension requirements;
- visitor's starting beliefs, questions, objections, and proof needs;
- sequence of belief changes needed for action;
- suitable one-page or multi-page architecture;
- required utility, legal, contact, scheduling, checkout, confirmation, and error pages or states.
- the exact CTA destination, stored data or completed action, consent/privacy need, owner, confirmation evidence, and recovery path.
- brand-concept implications for comprehension, trust, narrative rhythm, and expression without letting aesthetics determine the conversion logic.

If more than one architecture is credible, compare no more than three options using visitor fit, business fit, content/proof requirements, complexity, and conversion risk. Recommend one.

## Design every page and section

For each page or section specify:

- page role and intended entry context;
- visitor question or starting belief;
- belief change or decision supported;
- key message;
- approved evidence, proof, or asset;
- claim limitation and what must not be claimed;
- primary or supporting CTA;
- likely next question;
- source stage file;
- mobile priority and missing content.

Keep proof close to the claim it supports. Place objections where they become relevant instead of collecting generic FAQs. Remove sections that repeat a message, lack evidence, or do not advance the visitor's decision.

Map the complete path:

`Traffic source → Entry page/first screen → Relevance → Value → Mechanism → Difference → Proof → Fit/offer → Risk/objections → CTA → Destination → Confirmation → Follow-up`

The actual order must follow the evidence and visitor awareness; do not force every label into a separate section.

Do not defer the conversion mechanism vaguely to `/build`. A waitlist requires contact details to reach a real destination; a preference test requires a persisted structured response; a booking requires a working booking destination; a purchase or reservation requires a real transaction or reservation system. If nothing is persisted or completed, change the website objective to prototype review and use `Prototype only`. Do not call an unrecorded click demand validation.

For `Prototype only`, end the public journey at a useful on-page destination. Use a specific exploration CTA, request no discarded input, and create no fake validation or confirmation state. One concise availability disclosure is enough when needed; do not repeat research caveats or create a dedicated prototype-disclosure section. Omit unsupported experiment pricing when no real price-response test is captured. Treat “just fake it” as a request for a non-collecting concept presentation, never as permission to imitate a successful conversion.

## Synthesis checkpoint

Present at most five bullets:

- recommended format and page map;
- first three sections and why they come first;
- primary CTA path through a real destination; for `Prototype only`, the useful on-page destination instead of a fake confirmation;
- conversion implementation state and any launch blocker;
- the strongest objection and where it is answered;
- the largest conversion risk or missing asset.

The full belief journey, proof plan, exclusions, and assumptions go into the saved file. Ask one confirmation or correction question. Do not save before approval.

## Save

After confirmation, write only `07-website-structure.md` with:

1. participant constraints and decisions;
2. objective, primary conversion, measurement, and conversion implementation state;
3. audience, traffic, awareness, device, and language assumptions;
4. visitor belief journey;
5. recommended architecture and rejected alternatives;
6. page map and page roles;
7. detailed section plan;
8. first-screen requirements;
9. claim-to-proof placement;
10. objection and risk handling;
11. CTA, destination, data or completed action, owner, consent/privacy, confirmation evidence, error, and follow-up path;
12. navigation, internal-link, and orientation requirements;
13. mobile and accessibility priorities;
14. analytics events and learning questions;
15. content, asset, integration, legal, and privacy requirements;
16. exclusions, assumptions, open questions, and next-stage guardrails.

Update `SESSION.md`. Finish with the approved architecture, saved file, largest unresolved risk, and “Next: `/copy`”.

## Quality gate

- A first-time visitor can identify what this is, who it is for, the credible value, and the next action from the first screen or first meaningful viewport.
- Message order matches entry source, awareness, and likely questions.
- Every page and section has a distinct job, evidence source, and next-step logic.
- One primary conversion is used consistently; supporting actions do not compete with it.
- Material claims have adjacent proof or visible qualification.
- The strongest objections and fit boundaries are handled honestly.
- The CTA has an explicit implementation state. `Connected` reaches and verifies the promised destination; `Connection required before launch` is recorded as a blocker; `Prototype only` clearly says no conversion is recorded.
- A public `Prototype only` page contains no discarded-input form, fake submission, fake validation, or fake confirmation.
- Mobile visitors can understand the offer and complete the primary path without unnecessary friction.
- Measurement events reveal both conversion and the largest strategic assumptions.
- No generic section remains without a research-backed reason.
