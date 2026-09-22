# Website copy method

## Purpose

`08-website-copy.md` is the content source of truth for the website. It converts approved research, brand concept and website structure into exact language for every page, section, component, form state and action.

The copy stage may clarify expression. It must not revise the approved audience, offer, positioning, architecture, proof, brand boundaries or commercial conditions.

## 1. Build the research-to-copy ledger

Extract only material that changes a message, proof requirement, action or guardrail:

| Research or decision | Customer meaning | Copy implication | Page/section ID | Proof or qualification |
|---|---|---|---|---|

Include:

- priority visitor, situation, trigger and awareness;
- desired progress and decision criteria;
- current workaround or alternative;
- anxieties, objections and trust requirements;
- sourced customer vocabulary and relevant search language;
- offer mechanism, deliverables, price, effort, timing, eligibility and exclusions;
- differentiation and reason to believe;
- proof and its limitations;
- approved brand voice, narrative pillars and boundaries;
- CTA destination and post-action experience.

## 2. Define the copy foundation

Make these decisions explicit:

### Priority reader

- Who is the page for?
- What situation brings them here?
- What do they already understand?
- Which alternative are they comparing?
- What are they trying to decide?

### Message strategy

- What single useful idea should remain after the visit?
- What credible outcome matters most?
- Which mechanism makes it plausible?
- Which difference matters relative to the current alternative?
- What must the visitor believe before acting?

### Claim boundaries

Record:

- supported claims;
- claims requiring context or qualification;
- hypotheses that cannot appear as facts;
- claims prohibited by missing evidence or business boundaries;
- exact quotations;
- facts, terms, prices, conditions and disclosures that must not change.

### Internal evidence versus public copy

Evidence labels guide what the website may claim. They are not automatically customer-facing language.

- Keep `Hypothesis`, `Unknown`, `Test offer`, `evidence limit`, research caveats, and validation notes in the internal ledger unless a visitor genuinely needs the information to make an informed decision.
- Translate uncertainty into claim strength: make a narrower truthful claim, use the known mechanism, describe the relevant situation, or omit the unsupported statement.
- Do not announce missing proof. Remove the unsupported proof claim and use process, specification, fit, provenance, or transparent scope when these are known.
- Do not publish drafting language such as “we are testing,” “working preview,” “still figuring this out,” “real price TBD,” “hypothesis,” or “not validated” as marketing copy.
- When a prototype could otherwise mislead a visitor, use one concise contextual disclosure near the action or in the footer, such as `Concept preview — ordering is not open.` Do not repeat the disclosure through the hero, offer, and every CTA.
- A public disclosure should explain the visitor's actual limitation, not narrate the team's research process.

Unknown commercial information is not a copy opportunity. If price, availability, fulfillment, or terms are structurally required but unresolved, return the decision to the owning stage or omit the element when the approved structure permits it.

### Voice

Turn the approved brand concept into observable rules for directness, sentence rhythm, vocabulary, technical depth, warmth, formality, humor and calls to action. Use adjectives only when they change a writing choice.

## 3. Write by belief job

For every stable page or section ID, use:

```text
ID:
Page and section:
Visitor question or starting belief:
Required belief or decision change:
Evidence and source:
Claim limit:
Exact copy:
CTA or next question:
Required proof or asset:
```

Separate final build copy visually from research notes so a designer or builder can use it immediately.

## 4. First-screen standard

The first meaningful viewport normally needs:

- a clear category, offer or recognizable context;
- relevance to the priority visitor;
- the most important credible value;
- enough mechanism or specificity to avoid a generic promise;
- a primary CTA with an understandable result;
- an optional proof or fit cue when evidence exists.

Do not force every item into the headline. Distribute the work across the eyebrow, headline, subheadline, supporting note, proof cue and CTA according to the approved structure.

Before choosing the first screen, create three materially different message routes when the evidence supports them:

1. **Situation or desired-progress route** — starts with the moment or change the audience recognises.
2. **Mechanism or offer route** — makes the concrete product or way it works immediately clear.
3. **Contrast or category route** — clarifies the meaningful difference from the real alternative.

Each route includes eyebrow, headline, subheadline, CTA, and optional proof or fit cue. Recommend one using relevance, specificity, differentiation, credibility, and action clarity. Do not present three superficial rewrites of the same sentence.

Reject a headline when a direct competitor could paste it onto their own page unchanged. Abstract words such as `ritual`, `experience`, `meaningful`, `elevated`, `thoughtful`, `simple`, or `different` require a concrete product, situation, or mechanism nearby.

## 5. Body-copy roles

### Situation or problem

Describe a recognizable situation without exaggerating pain, diagnosing the visitor or repeating a fear the research did not show.

### Desired progress and value

Connect the intended outcome to a practical consequence. Do not present an intended outcome as a demonstrated result.

### Mechanism

Explain how the offer works sufficiently for the promise to feel plausible. Avoid feature lists with no customer meaning.

### Difference and alternatives

Clarify relevant trade-offs rather than attacking competitors. Compare with the real alternative or status quo documented in research.

### Proof

Introduce what the evidence demonstrates. Do not make a quote, logo, statistic, credential or case carry a stronger claim than it supports.

### Offer and fit

State deliverables, process, price or commitment, timing, eligibility, exclusions, responsibilities and what happens next.

If a price is still an experiment:

- do not write “still figuring out the real price” or similar drafting commentary;
- show the price only when the approved experiment genuinely tests price and captures a response;
- label it with concise truthful language such as `Proposed launch price` only when that framing is approved;
- otherwise omit the price from public copy and preserve the gap in the internal requirements;
- never present an economically unsupported price as an available live offer.

### Risk and objections

Answer genuine doubts with evidence, transparency, policy or a fit boundary. Do not invent objections to fill an FAQ.

### Action

CTA copy should state or strongly imply the next step. Supporting text should clarify effort, timing, destination and follow-up when relevant.

### System-state truth

Copy describing a completed action is a factual claim about the system. Match it to the approved implementation state:

- Use “Join the list” and “You’re on the list” only when the contact is actually persisted.
- Use “Reserve” or “Order confirmed” only when a real system records that commitment.
- Use “Response received” only when the response reaches a working destination.
- For a local prototype with no persistence, do not simulate success. Use navigation or exploration actions such as `See what’s included`, `Explore the concept`, or another specific destination inside the page. Add one concise disclosure only when needed to prevent misunderstanding.

If structure does not name a real destination or an explicit prototype state, stop and return to `/structure` or `/express-copy`. Do not solve an unconnected action with persuasive wording.

## 6. Microcopy and discoverability

Specify exact text where relevant for:

- navigation, buttons and links;
- form labels, instructions and required or optional fields;
- validation errors, consent and privacy notices;
- loading, empty and unavailable states;
- success confirmation and response-time expectations;
- booking, payment, waitlist, account or download follow-up;
- footer, contact and legal navigation;
- page title, meta description and social-preview text;
- descriptive link labels and image-purpose notes for future alt text.

Use approved search language naturally. Do not add filler sections, repeat phrases mechanically or write to an arbitrary word count.

Do not place implementation placeholders, missing-proof notes, research caveats, or instructions to the builder inside final customer-facing copy. Keep them in the section's internal `Required proof or asset` field and the integration requirements.

## 7. Human copy quality pass

This method applies selected writing-quality patterns from [`blader/humanizer`](https://github.com/blader/humanizer) within an independently written process for evidence-led conversion websites.

Humanization improves how approved copy sounds. It does not create strategy, strengthen evidence or make a weak claim acceptable. The editor may leave strong copy unchanged.

### Seven focused conversion sweeps

Review the draft in separate passes. After each pass, recheck that earlier improvements and protected meaning remain intact:

1. **Clarity:** remove ambiguity, insider language, missing context, and sentences carrying too many ideas.
2. **Voice:** keep directness, rhythm, vocabulary, warmth, formality, and humor consistent with approved evidence.
3. **Reader value:** for every feature or claim, answer the reader's practical “so what?” without inventing an outcome.
4. **Proof:** support the claim nearby, narrow it, or remove it. Do not compensate with confidence or decoration.
5. **Specificity:** replace interchangeable claims with concrete audience, situation, mechanism, scope, timing, or example when supported.
6. **Emotion:** make the real situation and desired progress felt through sourced context; avoid manufactured fear, shame, urgency, or aspiration.
7. **Action confidence:** answer the real hesitation near the CTA and make the next step, effort, destination, privacy, and follow-up clear.

The sweeps are a review method, not seven new sections. They must not lengthen a page that is already clear.

### Protected meaning

Before editing, freeze:

- facts, names, numbers, dates, prices, quotations, citations and results;
- research-supported qualifiers and uncertainty;
- offer scope, conditions, exclusions, guarantees and next steps;
- required search terms and sourced audience language;
- consent, privacy, accessibility and specialist wording;
- CTA meaning and destination.

If a useful detail does not exist, flag the gap. Never invent it.

### Voice hierarchy

Use voice evidence in this order:

1. approved active-session `06-brand-concept.md`;
2. founder writing samples in the website language;
3. sourced audience language where appropriate;
4. plain, neutral, concrete prose.

Match stable patterns such as directness, rhythm, vocabulary, warmth, formality and humor. Do not imitate typos, private disclosures or accidental inconsistencies. Do not invent founder experiences.

### Patterns to review

Remove or fix:

- generic run-ups, artificial suspense and unraised objections;
- conclusions that repeat the previous sentence;
- forced groups of three and identical section shapes;
- uniform sentence lengths and habitual dash use;
- vague superlatives, borrowed authority and promotional padding;
- generic “Transform your…” headlines;
- pain exaggeration and benefits without a mechanism;
- manufactured founder vulnerability;
- decorative headings with no decision value;
- identical CTA wording in every context;
- FAQs with no researched objection;
- fake conversation and chatbot residue.

Preserve a real persuasive benefit when evidence supports it.

### Persuasive specificity pass

For each major section ask:

- Does this open with something the priority reader recognises or wants?
- Is the product, mechanism, or next step concrete?
- Does this say something a relevant competitor could not paste unchanged?
- Is there a reason to believe proportionate to the claim?
- Does the next line increase understanding or desire rather than restate the heading?

Rewrite any section that fails two or more checks. Strong copy may be restrained, but it must not sound like an internal brief, generic template, or apology for an unfinished business.

### Clear and accessible language

- Prefer familiar words, concrete verbs and short blocks appropriate to the audience.
- Put useful information first and keep one main idea per paragraph.
- Use descriptive headings, links and button labels.
- Explain necessary jargon and abbreviations once.
- Avoid idioms, sarcasm or wordplay when they obscure meaning, especially for multilingual audiences.
- Preserve complexity when accuracy requires it.

These practices support clear content but do not establish WCAG compliance by themselves.

### Claims and overall impression

Review explicit and implied claims created by combinations of headline, body copy, testimonial, image, guarantee and omission.

- Do not turn an aspiration into an outcome claim.
- Do not imply that one testimonial is a typical result without suitable support.
- Do not hide material conditions in fine print or a later section.
- Keep disclosures close to the relevant claim.
- Flag health, finance, safety, legal, environmental, earnings and performance claims for suitable specialist review.

This workflow checks evidence integrity and does not provide legal clearance.

### Multilingual copy

- Use voice samples written in the target language where possible.
- Do not translate idioms or personality mechanically.
- Preserve diacritics, names, units, currencies and date formats.
- Recheck claims and humor after translation.
- Retain limitations when evidence comes from another market or language.

## 8. Editing and integrity checks

1. Freeze protected facts and terms.
2. Extract a small voice profile from approved sources.
3. Draft from the approved structure.
4. Review artificial patterns at sentence, paragraph and page level.
5. Rewrite around the actual point rather than swapping isolated words.
6. Compare against the protected ledger and structure.
7. Confirm every claim is unchanged or weaker unless new evidence was approved.
8. Confirm search language remains natural.
9. Read the copy aloud for rhythm and repetition.
10. Show a representative sample before finalizing the complete site.

Run two independent checks:

- **Meaning check:** each protected item is `preserved`, `intentionally removed with reason`, or `needs participant decision`.
- **Reader check:** review relevance, comprehension, credibility, scanning, action clarity and voice consistency.

Do not optimize for or promise to pass an AI detector.

For launch copy, add a four-perspective review after the sweeps:

- conversion: relevance, benefit hierarchy, and action clarity;
- UX: scanning, cognitive load, labels, and recovery;
- skeptical target visitor: credibility, missing answers, and reasons to hesitate;
- brand: voice and positioning fidelity.

Each perspective must name a specific fix or pass. Scores without evidence are not useful.

## 9. Edge cases

### Specificity without a stronger promise

When evidence supports a four-week program, weekly sessions and practical exercises but no outcome data, describe the duration, audience, mechanism and intended use. Do not upgrade this to “unprecedented productivity” or guaranteed transformation.

### Exact testimonial

Preserve an approved quotation word for word, including attribution and permission status. If it implies too much, change the surrounding claim rather than the quote.

### Search phrase

Use an approved phrase such as “AI workshop for marketing teams” in a natural title or heading. Use related natural language elsewhere instead of repeating the exact phrase.

### Founder voice

If samples show short sentences and dry humor but no origin story, use the rhythm and humor without inventing personal fear, struggle or transformation.

### Layout-created claim

A general outcome headline placed beside an exceptional result may imply that result is typical. Preserve authentic evidence but add context or weaken the surrounding promise.

### Localization

Preserve directness and rhythm across languages, but replace idioms only with natural expressions appropriate to the approved regional audience.

### No-change decision

Clear, specific, proportionate copy may stay unchanged. A quality pass does not need to produce a visible rewrite in every section.

## 10. Variants, completeness and output

Provide one approved version by default. Add a variant only when it expresses a meaningful, evidence-safe hypothesis and the file says what the test should teach.

The copy is complete when:

- every approved page and stable section ID has exact copy or a named blocker;
- proof and asset placeholders cannot be mistaken for real content;
- the CTA path includes destination, errors, confirmation and follow-up;
- claim limitations and exact quotations are preserved;
- a designer can understand hierarchy and approximate content volume;
- the build can proceed without reopening every research file;
- unresolved visual decisions remain in the visual direction.
- every CTA, loading state, and confirmation describes behavior the approved implementation can actually perform.

## Method sources

- Marketing Skills, “Copywriting” and “Copy Editing”: https://github.com/coreyhaines31/marketingskills
- Humanizer, writing-quality patterns: https://github.com/blader/humanizer

Use this structure:

```text
# Website copy context

## Scope and source files
## Priority reader and arrival context
## Message strategy and hierarchy
## Voice and terminology
## Claims, proof and prohibited language
## CTA and conversion path

## Page: [name]
### [SECTION-ID] [section name]
#### Section job
#### Final copy
#### Proof/assets/qualification

## Forms and interaction microcopy
## SEO and social metadata
## Research-to-copy traceability
## Semantic-integrity report
## Missing inputs and open questions
```
