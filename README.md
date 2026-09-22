# Claude for Non-Techies — Website Workshop

Use this workshop to turn an idea into a research-backed website hypothesis, an approved brand concept, complete website copy, visual direction, and a local website ready for review. The Express path creates a measurable first experiment; it does not claim to validate demand in two hours.

## The command to start the live workshop

Use the **Express path** during the workshop. Start a new Claude Code chat and type:

`/express-start`

Do not start with `/setup`. That command belongs to the optional longer Full path after the workshop. Claude should not ask you to choose a path.

## Before you start

You need:

- a current version of Claude Code;
- an active Claude Code sign-in and internet connection;
- the complete repository folder, including the `.claude/` folder.

For a stronger business result, bring:

- notes from at least three relevant customer conversations, sales calls, support conversations, or observed customer decisions;
- any real objections, exact customer phrases, previous enquiries, purchases, signups, or analytics;
- a rough view of material, labor, delivery, payment, tax, support, and refund costs when the offer is paid;
- known suppliers, capacity, timing, geographic, legal, or quality constraints;
- a working destination for the website action, such as an existing form, booking page, checkout, or other system that records the promised result.

You can still participate without these inputs. Claude will label the result as a test or prototype and will not present missing evidence as validation.

Open the repository root in Claude Code. If the workshop commands do not appear when you type `/`, confirm that `.claude/skills/` is present and restart Claude Code from the repository root.

## Start here

1. Download the complete repository and unzip it, or clone it with Git.
2. Open the complete folder in Claude Code.
3. Optional: add useful existing materials to `assets/`.
4. Start a new Claude Code chat and type `/express-start`.
5. Answer one question at a time and run the next command Claude recommends.

If Claude mentions an older unfinished session while you want a new workshop run, type `/express-start` explicitly. It creates a new Express session and does not continue the older one.

Keep the complete folder together. Claude saves all new work under `sessions/` and does not rewrite the source files you place in `assets/`.

## You cannot skip stages

Each command checks that the previous stage was completed and approved before it starts. If something is missing, Claude stops and tells you which command to return to.

A field may be completed with an approved answer, an explicitly accepted hypothesis or unknown, or a justified “not applicable.” It may not be left blank or silently assumed. Claude creates the next stage only after you confirm the current checkpoint.

Useful source material can include:

- a product, service, or idea description;
- pricing and offer documents;
- customer interviews or anonymized notes;
- survey, sales, support, or analytics summaries;
- objections, approved testimonials, and previous research;
- founder writing samples;
- existing brand materials.

You can begin without these materials. Missing evidence will be identified when it becomes relevant, and it may limit the result to a test hypothesis or prototype.

## Live workshop path and optional deeper path

The live two-hour workshop uses the **Express path**. It keeps the core business decisions while combining stages and limiting questions. The **Full path** remains available for optional deeper work after the workshop in a new session.

| | Express path | Full path |
|---|---|---|
| Best for | One live workshop session; every participant builds a first one-page website experiment | Working at your own pace over several sessions |
| Commands | `/express-start` → `/express-research` → `/express-offer` → `/brand-concept` → `/express-copy` → Visual Direction → `/build` → `/review` | `/setup` → `/vision` → `/research` → `/audience` → `/offer` → `/positioning` → `/brand-concept` → `/structure` → `/copy` → Visual Direction → `/build` → `/review` |
| Questions asked | Six at the start, then at most one or two per stage | Several per stage, one at a time |
| Research | One focused 25–30 minute deep desk-research pass covering market, audience, demand signals, pricing, and commercial reality | Separate market and audience passes |
| Website format | One page by default | One or several pages, decided from the evidence |

During the live workshop, follow only the Express commands below. Do not switch paths inside a session. `/setup` and the Full commands are included only for optional deeper work later.

## Express path

### 1. Start

`/express-start`

Six short questions: the idea and its stage, who might buy, one real situation, what changes for that person, the website action and where first visitors will come from, and what the site must never promise. Claude creates the session and saves `00-setup-and-vision.md`.

### 2. Research

`/express-research`

One focused deep desk-research pass: direct competitors, indirect and status-quo alternatives, real customer language, audience situations, demand signals, counter-evidence, price bands, fulfillment, trust, and commercial risks. It compares several possible audience situations before selecting one test audience and separates what is safe to claim from what still needs testing. Saves `02-research.md`.

### 3. Offer and positioning

`/express-offer`

At most two questions, then one proposal: what the customer receives, how it can be delivered, price and cost status, which alternative the website is positioned against, the difference that matters, the offer's evidence status, and the claims to avoid. Saves `04-offer-and-positioning.md`.

### 4. Brand concept

`/brand-concept`

Same stage as the Full path, limited to two questions. Saves `06-brand-concept.md`.

### 5. Structure and copy

`/express-copy`

One page. Claude proposes the section list, first screen, and exact conversion path, then writes the complete build-ready copy. A lead, signup, booking, reservation, purchase, or research response is treated as real only when a working destination records it. Saves `07-website-structure.md` and `08-website-copy.md`.

### 6. Visual Direction, build, review

Identical to steps 6 and 7 of the Full path below.

## Optional Full path after the workshop

### 1. Define the starting point

`/setup` → `/vision`

Clarify the idea, intended customer change, website action, boundaries, and early success signals.

### 2. Research the market and audience

`/research` → `/audience`

Investigate direct alternatives, indirect alternatives, the status quo, customer situations, motivations, objections, trust needs, and real language.

### 3. Make the commercial decisions

`/offer` → `/positioning`

Define what the customer receives, how it creates value, commitment, fit, proof, differentiation, and claims the website can support.

### 4. Create the brand concept

`/brand-concept`

Claude imports the approved research, offer, and positioning decisions. It asks only for missing founder and identity choices, then creates the complete ten-block `06-brand-concept.md`. You do not complete a second Brand Concept questionnaire.

### 5. Create the website content

`/structure` → `/copy`

Decide the page architecture, visitor journey, proof placement, objections, CTA path, and exact build-ready website copy.

### 6. Complete Visual Direction

Open the Visual Direction tool after `/copy`. Its questions and guidance are provided inside the tool.

Use these three files from your active session:

- `06-brand-concept.md`;
- `07-website-structure.md`;
- `08-website-copy.md`.

Download the completed export and save it as:

`assets/brand/visual-direction.md`

Add any approved logo files, licensed fonts or web-font sources, images, illustrations, and icons required by the visual direction. The Markdown export defines the rules but does not replace the actual assets.

### 7. Build and review

`/build` → `/review`

Claude combines the approved business decisions, copy, and visual direction into a local website. In an Express session it creates a dependency-free one-page site; the approved structure still determines the actual sections and their order. Claude then reviews conversion clarity, evidence, visual fidelity, usability, accessibility, trust, and launch readiness.

The review reports four separate readiness levels: research, commercial offer, conversion instrument, and website implementation. A polished page can pass the website checks while still failing research or commercial readiness. An unconnected primary action always blocks launch when the site promises to collect a lead, signup, booking, reservation, purchase, or response.

## Continue later

Open the same project folder and run the next command shown in the previous stage. Claude continues the unfinished session automatically when the correct session is clear. It asks you to choose only when several sessions are genuinely possible.

To start a separate workshop project instead of continuing, run `/express-start`.

## What Claude creates

Every new run gets its own folder. The files depend on the path.

Express path:

```text
sessions/<project>-<date-time>/
├── SESSION.md
├── 00-setup-and-vision.md
├── 02-research.md
├── 04-offer-and-positioning.md
├── 06-brand-concept.md
├── 07-website-structure.md
├── 08-website-copy.md
├── 09-build-notes.md
├── 10-launch-audit.md
└── site-v1/
```

Full path:

```text
sessions/<project>-<date-time>/
├── SESSION.md
├── 00-setup.md
├── 01-vision.md
├── 02-market-research.md
├── 03-audience-research.md
├── 04-offer.md
├── 05-positioning.md
├── 06-brand-concept.md
├── 07-website-structure.md
├── 08-website-copy.md
├── 09-build-notes.md
├── 10-launch-audit.md
└── site-v1/
```

A stage file appears only after you approve that stage. `site-v1/` appears during `/build`.

The starter repository does not include anyone's generated `sessions/` or completed `assets/brand/visual-direction.md`. Those are created or added locally by each participant and are excluded from Git by `.gitignore`.

## Complete starter kit

```text
claude-website-workshop/
├── README.md
├── CLAUDE.md
├── .gitignore
├── assets/
│   └── brand/
│       └── README.md
└── .claude/
    ├── THIRD-PARTY-NOTICES.md
    ├── references/
    │   ├── AUDIENCE-RESEARCH.md
    │   ├── BRAND-CONCEPT.md
    │   ├── CONVERSION-STRATEGY.md
    │   ├── MARKET-RESEARCH.md
    │   ├── SESSION-AND-EVIDENCE.md
    │   ├── WEBSITE-COPY.md
    │   ├── WEBSITE-QUALITY.md
    │   └── WEBSITE-STRUCTURE.md
    └── skills/
        ├── express-start/SKILL.md
        ├── express-research/SKILL.md
        ├── express-offer/SKILL.md
        ├── express-copy/SKILL.md
        ├── setup/SKILL.md
        ├── vision/SKILL.md
        ├── research/SKILL.md
        ├── audience/SKILL.md
        ├── offer/SKILL.md
        ├── positioning/SKILL.md
        ├── brand-concept/SKILL.md
        ├── structure/SKILL.md
        ├── copy/SKILL.md
        ├── build/SKILL.md
        └── review/SKILL.md
```

`.claude/` starts with a dot because Claude Code requires that exact name. GitHub displays it normally. macOS Finder hides dot folders by default; press **Command + Shift + .** to show or hide them.

You may inspect every file. Keep the `.claude/` names and paths unchanged so Claude Code can find the commands and supporting methods.

## What the starter files do

### Files you work with directly

| File or folder | Purpose |
|---|---|
| `README.md` | Participant instructions and the complete workflow. |
| `assets/` | Your source materials. Claude reads them but does not rewrite them. |
| `assets/brand/README.md` | Instructions for the completed Visual Direction export and implementation assets. |
| `sessions/` | Created automatically for your research, decisions, copy, website, and review. |

`visual-direction.md` is not included in the starter kit. You add the completed export after `/express-copy` or `/copy`, depending on the session path.

### Runtime and privacy files

| File | Purpose |
|---|---|
| `CLAUDE.md` | Shared rules for participant interaction, evidence, file safety, and external actions. |
| `.gitignore` | Prevents generated sessions, private source materials, and local system files from being added to the public repository accidentally. |
| `.claude/THIRD-PARTY-NOTICES.md` | Attribution for the adapted human-copy methodology. |

### Commands in `.claude/skills/`

Express path only:

| Command | Purpose |
|---|---|
| `/express-start` | Creates a clean Express session; six questions covering setup and vision. |
| `/express-research` | One focused deep desk-research pass over market, competitors, alternatives, audience situations, demand signals, pricing, and commercial reality. |
| `/express-offer` | Defines the offer and the positioning decision in one stage. |
| `/express-copy` | Designs a one-page structure and writes the complete website copy. |

Full path only:

| Command | Purpose |
|---|---|
| `/setup` | Creates a clean session and records the minimum project context. |
| `/vision` | Defines intended customer change, purpose, boundaries, and success signals. |
| `/research` | Researches the market, competitors, and status-quo alternatives. |
| `/audience` | Researches customer situations, behavior, needs, objections, and language. |
| `/offer` | Defines the offer, mechanism, commitment, proof, fit, and action. |
| `/positioning` | Selects defensible differentiation against real alternatives. |
| `/structure` | Creates the page architecture, belief journey, proof placement, and CTA path. |
| `/copy` | Produces final website copy and microcopy from approved evidence and decisions. |

Both paths:

| Command | Purpose |
|---|---|
| `/brand-concept` | Creates the approved ten-block brand concept without repeating research. |
| `/build` | Maps approved content to the visual archetypes, pauses for one compact desktop/mobile wireframe approval, then builds and visually checks the local website. |
| `/review` | Audits the complete rendered website against strategy, wireframes, visual rules, conversion behavior, and launch requirements. |

### Methods in `.claude/references/`

| File | Purpose |
|---|---|
| `SESSION-AND-EVIDENCE.md` | Session selection, evidence labels, source records, approvals, and revision rules. |
| `MARKET-RESEARCH.md` | Market, competitor, alternative, and differentiation research method. |
| `AUDIENCE-RESEARCH.md` | Situation-based audience, behavior, language, and content research method. |
| `CONVERSION-STRATEGY.md` | Offer, positioning, proof, objection, CTA, and conversion standards. |
| `BRAND-CONCEPT.md` | Brand Concept schema, decision ownership, no-duplication rules, and Visual Direction handoff. |
| `WEBSITE-STRUCTURE.md` | Conversion architecture, belief sequencing, proof placement, actions, and measurement. |
| `WEBSITE-COPY.md` | Complete website-copy, microcopy, traceability, voice, and integrity method. |
| `WEBSITE-QUALITY.md` | Build and review standards for usability, accessibility, trust, and technical readiness. |

## Important boundaries

Desk research can reveal alternatives, language, patterns, and useful hypotheses. It cannot prove demand or replace conversations and observed behavior from real customers.

Claude can prepare the website locally. Publishing, deploying, buying a domain, sending messages, submitting forms, or changing an external account requires a separate explicit request.
