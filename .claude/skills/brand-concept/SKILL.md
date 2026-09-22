---
name: brand-concept
description: Synthesize approved vision, market, audience, offer, positioning, and founder inputs into one evidence-traceable ten-block brand concept. Use after /positioning (Full path) or /express-offer (Express path) to import existing decisions, ask only missing identity questions, and create the canonical 06-brand-concept.md without defining the visual identity.
---

# Brand concept

Read `CLAUDE.md`, every approved stage file in the active session, `.claude/references/SESSION-AND-EVIDENCE.md`, and `.claude/references/BRAND-CONCEPT.md`. Inspect relevant founder, history, writing, customer-language, proof, and existing brand materials in `assets/` without modifying them.

## Entry gate

Run the mandatory progression gate in `CLAUDE.md` and require `Next command: /brand-concept`. On the Full path, require every stage through an approved `05-positioning.md`. On the Express path, require every stage through an approved `04-offer-and-positioning.md`. If anything is incomplete, name the earliest missing stage and recommend its command. Do not recreate positioning here.

This stage creates the final verbal and conceptual brand system used by Visual Direction, `/structure`, and `/copy`. It does not choose colors, typography, logos, page composition, illustration or materials, graphic elements, visual applications, or AI visual direction.

## Build the prefill before asking questions

Create an internal field ledger for all ten Brand Concept blocks in `.claude/references/BRAND-CONCEPT.md`. For every field record:

- proposed content;
- evidence label from `SESSION-AND-EVIDENCE.md`: `Decision`, `Observed`, `Reported`, `Inferred`, or `Hypothesis`;
- source pointer: the stage file and section it was imported from, or `founder, this stage` for a choice made here;
- confidence or unresolved conflict when useful;
- whether a human decision is still required.

Import approved market, audience, offer, and positioning decisions instead of asking the participant to repeat them. Use research to assess relevance, credibility, language, and risk. Do not infer founder values, purpose, history, or identity boundaries from customer preferences.

## Ask only for material gaps

Ask exactly one missing decision per turn. Skip any question already answered by approved sources or explicit founder input. Prioritize gaps in this order when they materially affect the result:

1. purpose or belief that the business chooses to protect;
2. desired perception and a perception to avoid;
3. values expressed through behavior and trade-offs;
4. personality traits and a productive tension;
5. conceptual territory, metaphors, or references;
6. voice behavior and situation-specific tone;
7. existing or candidate distinctive codes;
8. communication boundaries and creative principles.

Ask for a decision, not an essay or an entire block. When helpful, offer no more than three evidence-grounded options with their trade-offs. Accept `unknown` and retain it as a hypothesis.

On the Express path, ask at most two questions: take the first two unresolved items in the order above and recommend or mark `Hypothesis` for everything else.

Do not ask a low-impact question merely to fill a field. Prefer a concise evidence-grounded recommendation or an explicit unresolved hypothesis when the answer would not materially change structure, copy, or Visual Direction.

## Synthesize the concept

Complete all ten blocks:

1. Brand Essence
2. Positioning
3. Brand Personality
4. Brand Values
5. Conceptual Territory
6. Voice & Tone
7. Messaging
8. Distinctive Codes
9. Boundaries
10. Creative Principles

Preserve the ownership rules and quality criteria in the reference. Do not repeat detailed research. Include concise source pointers so downstream work can trace a decision without reopening every source.

Treat distinctive codes created in the workshop as candidates. Treat messaging as an approved message system rather than finished website copy. Ensure promises and claims remain within the evidence limits of the approved offer file (`04-offer.md` or `04-offer-and-positioning.md`).

Finish the synthesis with a **Website message handoff** containing the canonical `D1`–`D9` business spine imported without loss and `D10` for core message, observable voice behavior, distinctive cues, and brand boundaries. Brand language may sharpen expression but must not replace a concrete audience situation, offer, price or commitment, difference, proof state, objection, or action with a generic purpose statement.

Concise voice means economical sentences and low repetition. It never means removing decision-critical information or producing a sparse website.

## Checkpoint

Present exactly five compact groups so the participant can approve every material part of the concept without reading the full file:

- essence and positioning;
- personality, desired perception, and values;
- conceptual territory and distinctive codes;
- voice, core message, and claim limits;
- boundaries, creative principles, and the largest credibility risk.

Mark any recommendation or unresolved hypothesis in these groups. Detailed evidence and source pointers go into the saved file.

Ask one question, for example “Does this sound like your business?” Do not save before approval.

## Save

After confirmation, write only `06-brand-concept.md` using the required output standard in `.claude/references/BRAND-CONCEPT.md`. Update `SESSION.md`. Do not edit earlier stage files and do not create a duplicate in `assets/brand/`.

Finish with the approved essence, saved file, unresolved hypotheses, and this handoff:

1. Open the Visual Direction tool using the approved `06-brand-concept.md` and the active session's research and offer files as factual context.
2. Treat the dashboard's Page Architecture answer as a visual composition proposal. It may suggest archetypes, focal points, rhythm, and a draft sequence; it does not finalize the information architecture.
3. Download and unzip the export. Move its language-specific Markdown file into `assets/brand/`, rename it `visual-direction.md`, and add any required visual assets.
4. Run `/structure` on the Full path or `/express-copy` on the Express path. That stage reconciles the dashboard with the research and makes the final section-order decision.

Update `SESSION.md` to `Next command: Complete Visual Direction`.

## Quality gate

- Every field in the ten-block schema is present or explicitly marked unresolved.
- Approved upstream decisions are imported unchanged and cited.
- Every material decision carries an evidence label and a source pointer, so imported decisions, founder choices, recommendations, and hypotheses remain distinguishable.
- Purpose and values were chosen by the founder rather than invented from audience research.
- Personality traits and values translate into observable behavior and anti-behavior.
- Conceptual territory is strategically grounded without predesigning the visual identity.
- Voice rules and tone shifts can guide actual copy in the website language.
- Every material claim has proof, qualification, or a clear prohibition.
- Workshop-created distinctive codes are labeled as candidates.
- Structure, copy, and the Visual Direction tool can use the file without requiring a second Brand Concept questionnaire.
- The Website message handoff contains `D1`–`D10`, preserves every approved business decision, and is specific enough to map directly into public content.
