# Website structure and conversion architecture method

## Core principle

A website structure is a sequence of decisions and belief changes, not a list of fashionable sections. It connects the visitor's entry context to a real action through relevant information, credible evidence, understandable choices, and low-friction interaction.

Structure must come from approved audience, market, offer, and positioning evidence. Competitor pages can reveal conventions and expectations, but they are not templates.

## 1. Begin with arrival context

Architecture changes with the source and awareness of traffic:

| Entry context | Likely need on arrival | Structural implication |
|---|---|---|
| Warm referral or existing community | Confirm fit and understand the offer | Reach offer, proof, commitment, and action quickly |
| Problem-aware search | Confirm relevance and compare approaches | Lead with the situation and desired progress; explain mechanism and difference |
| Solution-aware search | Compare providers, scope, proof, and price | Make differentiation, fit, evidence, and terms easy to find |
| Campaign or event | Continue the promise that generated the visit | Maintain message continuity and remove unrelated navigation |
| Returning visitor | Resolve remaining risk or complete action | Make proof, pricing, FAQ, and CTA easy to revisit |

Record uncertainty when traffic sources are not yet known. Do not design simultaneously for every awareness level unless the business genuinely expects a mixed audience and can support clear routes.

## 2. Define the first-screen contract

The first meaningful viewport should help the intended visitor understand:

- what the offer or organization is;
- whether it may be relevant to their situation;
- the most important credible value;
- what action is available;
- enough context to continue rather than bounce from confusion.

It does not need to contain every argument, price, feature, and proof item. Avoid vague slogans, unsupported outcomes, premature forms, and competing CTAs.

## 3. Build the belief journey

Use these as decision states, not mandatory section headings:

| State | Visitor question | Evidence or content often needed |
|---|---|---|
| Arrival | Am I in the right place? | Clear category, audience situation, message continuity |
| Relevance | Is this for someone like me, now? | Trigger, context, recognizable problem or goal |
| Value | What useful progress could this create? | Credible outcome and practical consequence |
| Mechanism | How does it work? | Process, product behavior, curriculum, service model |
| Difference | Why choose this over my current alternative? | Meaningful comparison and distinctive capability |
| Credibility | Why should I believe it? | Proof matched to claim strength |
| Fit | What exactly do I get and what is required? | Scope, deliverables, price or commitment, exclusions |
| Risk | What could go wrong or make this unsuitable? | Honest limitations, objection handling, policies, support |
| Action | What happens if I proceed? | Specific CTA, destination, effort, confirmation, next step |

Some audiences need credibility before mechanism; others need price before proof. Use research and arrival context to choose the order.

## 4. Choose one page or several

Prefer one focused page when:

- there is one audience, one offer, and one primary action;
- traffic arrives with similar intent;
- the necessary explanation and proof remain manageable;
- separate pages would create thin or repetitive content.

Prefer multiple pages when:

- distinct visitor groups have materially different needs or actions;
- products, services, locations, languages, or buying journeys require separate routes;
- substantial proof, documentation, resources, or search intent deserves independent pages;
- legal, privacy, contact, checkout, account, or support functions require them;
- navigation helps visitors orient rather than distracts them.

Do not choose multiple pages merely to make the business look established. Do not force complex decisions into one long page solely because landing pages are fashionable.

## 5. Give every page and section a job

For every unit define:

```text
Entry context:
Visitor question or belief:
Required change:
Key message:
Evidence or asset:
Claim limitation:
CTA or next question:
Source:
Mobile priority:
```

Remove or merge a section when:

- it repeats an earlier point;
- no visitor question or decision depends on it;
- it contains claims without proof;
- it exists only because competitors have it;
- it delays the primary action without reducing uncertainty;
- it presents company history before establishing visitor relevance.

## 6. Map evidence to claims

Proof should appear near the claim it supports. Use the evidence type appropriate to the claim:

| Claim | Suitable evidence |
|---|---|
| The process or feature exists | Demo, screenshots, specification, curriculum, workflow |
| The founder or team has relevant expertise | Verifiable work, credentials, publications, track record |
| Customers value an experience | Attributed feedback with context and permission |
| A measurable outcome occurs | Relevant results with sample, conditions, timeframe, and limitations |
| The offer fits a specific use case | Case example showing starting situation, mechanism, and outcome |

Do not place logos, statistics, ratings, or testimonials decoratively. Explain what each proves. Preserve limitations and avoid implying that an exceptional result is typical.

## 7. Handle objections at the point of doubt

Map each important objection:

| Objection or anxiety | When it appears | Honest answer | Proof or policy | Page/section |
|---|---|---|---|---|

Use FAQs only for real remaining questions that do not fit naturally elsewhere. Do not manufacture objections to fill a standard FAQ block.

## 8. Design the complete action path

Structure includes what happens after the button:

```text
Entry → CTA → Destination → Input or commitment → Validation → Success confirmation → Follow-up
```

Specify:

- exact destination or integration;
- information requested and why;
- price or commitment visibility;
- error and recovery states;
- confirmation message;
- expected response time or next event;
- privacy and consent needs;
- what happens when the integration is not connected yet.

Never represent an unconnected form, checkout, calendar, or waitlist as functional.

Before approving the structure, assign the conversion implementation one state:

- **Connected:** a real destination or integration is identified and can record the intended action.
- **Connection required before launch:** the exact integration and required data are specified, but it is not yet connected.
- **Prototype only:** no data will be recorded. A public concept page uses a navigational or exploration CTA and does not imitate a form submission, preference capture, booking, order, or confirmation.

For a conversion-focused project, `Connection required before launch` is the default when the intended destination is missing. Before accepting that state, offer the simplest truthful existing routes: email, Instagram, WhatsApp, a simple form, booking, or checkout. `Prototype only` is an explicit request for a presentation-only page, not the default live-workshop outcome. Before accepting it, show the participant which CTA, follow-up, measurement, and business learning will disappear.

A decision to collect no contact data is compatible with an anonymous preference test only when the selected response is actually persisted through a suitable structured event or form endpoint. If nothing is persisted, change the website objective from demand validation to prototype review.

For `Prototype only`:

- do not ask the visitor to enter, choose, or “submit” information that is discarded;
- do not create validation or success states for an action that does not occur;
- use an on-page destination such as offer details, mechanism, examples, or `See what’s included`;
- use at most one natural availability statement when needed, such as `Opening soon` or `Orders open in October`; never publish `Concept preview`, `Prototype`, `Demo only`, `there is no list to join`, or other internal workflow language;
- do not create a dedicated disclosure section as a substitute for customer value or proof;
- keep the complete approved proposition visible; an approved experiment price uses one natural qualifier such as `Expected price: €12` or `Around €12`, while the evidence status stays internal;
- if the actual goal is a facilitated UX prototype, keep that mock interaction clearly separate from the public marketing page and do not treat it as business evidence.

A request to “fake it,” “mock it,” or “make the button look real” defaults to a non-collecting concept presentation with an exploration CTA. It is not permission to build a fake conversion flow.

A scroll-to-details action can support exploration but cannot be the only primary action for a converting or launch-oriented website. The first screen and closing section must offer the same useful next step to a real destination. The closing section must state what the visitor gets and what happens next.

Do not defer the measurement mechanism to `/build` without specifying what will be recorded, where it will go, and what success means. Build may implement an approved mechanism; it must not invent the conversion model.

## Research-payoff test

Before structure approval, confirm that the public journey has a visible role for every applicable decision category:

1. concrete audience situation or trigger;
2. real alternative or status-quo friction;
3. differentiated mechanism and practical value;
4. complete offer, approved price or commitment, and fit;
5. reason to believe, process evidence, specification, provenance, or transparent current status;
6. researched objections and trade-offs;
7. meaningful next action and post-action expectation.

These do not require seven sections. They do require visible customer value. A traceability table, internal evidence label, or `Intentionally excluded` status is not a substitute. Apply a subtraction test: if removing market and audience research would leave substantially the same architecture, the research has not been converted into the website.

## 9. Navigation and orientation

- Use labels that visitors understand rather than internal business terminology.
- Make the current location and available next step clear.
- Keep campaign pages focused when global navigation would distract.
- Provide routes to information needed for trust, access, support, privacy, and legal obligations.
- Use descriptive internal links; do not rely on repeated “learn more”.

## 10. Mobile and accessibility priorities

- Prioritize message, proof, offer, and CTA for a narrow viewport.
- Avoid making essential meaning depend on hover, animation, or a wide comparison table.
- Preserve logical reading and focus order.
- Keep headings descriptive and hierarchical.
- Ensure CTA and navigation labels remain meaningful out of context.
- Plan form labels, instructions, errors, and confirmation states.
- Avoid sticky elements that obscure content or the primary action.

Structure planning supports accessibility but does not establish WCAG compliance.

## 11. Measurement and learning

Define events that answer business questions, not only clicks:

- meaningful page or section reached;
- proof, pricing, or comparison viewed where technically appropriate;
- primary CTA initiated;
- form or checkout completed;
- validation error or abandonment;
- confirmation reached;
- qualified follow-up or downstream outcome when available.

Use the smallest useful event set. Avoid collecting personal data without a valid need and suitable consent. Do not invent conversion benchmarks.

## 12. Structure approval standard

Before approval, show:

- recommended architecture and rationale;
- first three sections and their sequence;
- proof and objection plan;
- complete CTA path;
- mobile priorities;
- missing assets and integrations;
- largest unsupported assumption;
- what was deliberately excluded.
- conversion implementation state, destination, data recorded, and launch blocker if unconnected.

The participant approves the decision logic before brand styling or final copy begins.

## Sources informing this method

- [GOV.UK: Identify user needs](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/plan-manage-content/identify-user-needs/)
- [GOV.UK: Structuring forms](https://www.gov.uk/service-manual/design/form-structure)
- [W3C: Page structure](https://www.w3.org/WAI/tutorials/page-structure/)
- [W3C: Forms](https://www.w3.org/WAI/tutorials/forms/)
- [Google Search Essentials](https://developers.google.com/search/docs/essentials)
- [Google: Helpful, people-first content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)
