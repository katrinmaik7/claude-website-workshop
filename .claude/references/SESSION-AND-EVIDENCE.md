# Session and Evidence Method

## Session creation

Create `sessions/<short-project-slug>-<YYYYMMDD-HHMM>/` only after the participant has answered the opening questions of the chosen path (`/setup` or `/express-start`) and confirmed the summary.

Create `SESSION.md` with:

- project name and timestamp;
- path: Full or Express;
- active mode: Workshop or Deep Research;
- current stage;
- supplied assets;
- stage files created;
- next stage.
- a progress table listing every stage on the selected path, its expected output, and its status.

Update `SESSION.md` as a small index after each stage. It is the only cross-stage administrative file.

Use the exact label `Next command:`. Initialize the matching progress table when the session is created.

Express session:

```text
## Progress

| Stage | Output | Status |
|---|---|---|
| Start and vision | 00-setup-and-vision.md | Approved |
| Research | 02-research.md | Not started |
| Offer and positioning | 04-offer-and-positioning.md | Not started |
| Brand concept | 06-brand-concept.md | Not started |
| Structure and copy | 07-website-structure.md; 08-website-copy.md | Not started |
| Visual Direction | assets/brand/visual-direction.md | Not started |
| Build | 09-build-notes.md; site-v1/ | Not started |
| Review | 10-launch-audit.md | Not started |

Next command: /express-research
```

Full session:

```text
## Progress

| Stage | Output | Status |
|---|---|---|
| Setup | 00-setup.md | Approved |
| Vision | 01-vision.md | Not started |
| Market research | 02-market-research.md | Not started |
| Audience research | 03-audience-research.md | Not started |
| Offer | 04-offer.md | Not started |
| Positioning | 05-positioning.md | Not started |
| Brand concept | 06-brand-concept.md | Not started |
| Structure | 07-website-structure.md | Not started |
| Copy | 08-website-copy.md | Not started |
| Visual Direction | assets/brand/visual-direction.md | Not started |
| Build | 09-build-notes.md; site-v1/ | Not started |
| Review | 10-launch-audit.md | Not started |

Next command: /vision
```

After each approval, change only the completed row and `Next command:`. While a stage is being worked on, use `In progress`. After `/express-copy` or `/copy`, set `Next command: Complete Visual Direction`, then allow `/build` only through the special Visual Direction gate in `CLAUDE.md`. After `/review`, set `Next command: Complete`.

## Paths and stage files

A session follows one path from start to finish. Do not mix commands from the two paths inside one session.

| Full path | Express path |
|---|---|
| `/setup` → `00-setup.md` | `/express-start` → `00-setup-and-vision.md` |
| `/vision` → `01-vision.md` | |
| `/research` → `02-market-research.md` | `/express-research` → `02-research.md` |
| `/audience` → `03-audience-research.md` | |
| `/offer` → `04-offer.md` | `/express-offer` → `04-offer-and-positioning.md` |
| `/positioning` → `05-positioning.md` | |
| `/brand-concept` → `06-brand-concept.md` | `/brand-concept` → `06-brand-concept.md` |
| `/structure` → `07-website-structure.md` | `/express-copy` → `07-website-structure.md` and `08-website-copy.md` |
| `/copy` → `08-website-copy.md` | |
| Visual Direction → `assets/brand/visual-direction.md` | Visual Direction → `assets/brand/visual-direction.md` |
| `/build` → `09-build-notes.md`, `site-v1/` | `/build` → `09-build-notes.md`, `site-v1/` |
| `/review` → `10-launch-audit.md` | `/review` → `10-launch-audit.md` |

Shared stages (`/brand-concept`, `/build`, `/review`) read whichever earlier files the session's path produced.

## Required progression

Use this order as a gate, not merely as a recommendation.

| Path | Required order |
|---|---|
| Express | `/express-start` → `/express-research` → `/express-offer` → `/brand-concept` → `/express-copy` → Visual Direction → `/build` → `/review` |
| Full | `/setup` → `/vision` → `/research` → `/audience` → `/offer` → `/positioning` → `/brand-concept` → `/structure` → `/copy` → Visual Direction → `/build` → `/review` |

Before entering a stage, run the mandatory progression gate in `CLAUDE.md`. Never use a later skill to manufacture or infer a missing earlier approval.

## Stage completion contract

Every completed stage file begins with:

```text
Stage: <stage name>
Path: Express | Full
Status: Approved
Approved after checkpoint: Yes
```

Approval means all of the following are true:

1. the participant saw the stage checkpoint and confirmed or corrected it;
2. every required output section named by the skill exists;
3. every required field contains an answer, an explicitly accepted hypothesis or unknown, or a justified `Not applicable`;
4. the skill's quality gate passes;
5. `SESSION.md` is updated with the stage as `Approved` and the exact next command or Visual Direction step.

Approval records the participant's decision to use an output in this website version. It does not upgrade a founder belief, desk-research finding, or unknown into customer evidence. Preserve the original evidence label and confidence after approval.

An output file without this metadata, with blank required sections, or with unresolved unapproved recommendations is incomplete even if its filename is correct.

Visual Direction is complete only when all ten current blocks are present, website-relevant `Still to define` or `Pendiente de definir` items are resolved by an explicit answer, a named system default, or a justified `Not applicable`, and the export matches the active project's brand concept, structure, and copy. `/build` performs this check before marking the visual step approved.

When `/build` validates Visual Direction, update its progress row to `Approved`, set the `/build` row to `In progress`, and continue in the same command. Mark `/build` approved only after both `site-v1/` and the approved `09-build-notes.md` exist and pass the build quality gate.

## Active session

- If the participant invokes `/express-start`, create a new Express session regardless of older sessions.
- Select an unfinished session when the participant asks to continue or resume, or invokes a command that must operate on an existing session.
- If several sessions fit that request, use the most recently updated unfinished session when the project name and current chat make the choice clear.
- Ask one short selection question only when more than one existing session is genuinely plausible.
- A request to start or begin the live workshop is a new Express run, not a request to resume an older Full session.
- State the selected session briefly; do not narrate directory inspection.
- Never combine evidence or decisions across sessions unless the participant explicitly requests it.

## Evidence labels

Use exactly these labels:

- **Observed** — directly visible behavior, analytics, document content, or a checked public fact.
- **Reported** — a sourced statement by a customer, participant, organization, or publication.
- **Inferred** — a reasoned interpretation derived from observations or reports.
- **Hypothesis** — plausible but unverified; requires testing.
- **Decision** — a choice confirmed by the participant for this website version.

Do not use `Observed` for a founder's general impression. Record it as `Reported — founder` or `Hypothesis` depending on wording.

## Confidence

Use `high`, `medium`, or `low` only when it helps a decision. Explain the reason in one sentence.

- **High:** multiple relevant sources agree, including direct or behavioral evidence.
- **Medium:** several directional sources agree, with material limits.
- **Low:** one indirect source, a founder belief, or an unresolved contradiction.

Confidence is not mathematical probability.

## Source record

For every external source used in a conclusion, record:

```text
Title:
Author or organization:
URL or local file:
Accessed or supplied:
Supports:
Limitations:
```

Do not list sources that were not opened or did not influence the output.

## Analysis chain

Use this structure for important findings:

```text
Observation or quote:
Interpretation:
Alternative interpretation:
Website implication:
Evidence label and confidence:
```

Only turn the implication into a `Decision` after confirmation.

A `Decision` is not evidence that the decision is correct. For every material commercial decision, retain both the decision and the evidence strength behind it. Use one of these decision states when helpful:

- **Evidence-backed decision** — supported by relevant direct, behavioral, commercial, or convergent independent evidence.
- **Test decision** — deliberately selected for a measurable experiment while material uncertainty remains.
- **Demo decision** — selected only to complete a prototype; it must not be described as validated or used to simulate a real conversion.

## Approval checkpoint

Before writing a stage file:

1. Present at most five bullets: the proposed decisions or conclusions, one of which is the strongest uncertainty or contradiction.
2. Ask one confirmation question.
3. Incorporate the correction.
4. Write the stage file and update `SESSION.md`.

Detail that the participant does not need in order to approve belongs in the stage file, not in the checkpoint.

## Revisions

Inside an unfinished stage, update the draft conclusion in chat until approved. Once a stage file exists, never edit it. If the participant wants a materially different version, create a new session and cite the earlier session as participant-provided context only when they explicitly ask.
