---
name: setup
description: Start the optional longer Full-path workflow for deeper post-workshop work. Use only when the participant explicitly invokes /setup or explicitly requests the Full path; the live workshop defaults to /express-start.
---

# Setup

Create a clean session without strategic analysis.

Before speaking, silently read `CLAUDE.md`, `README.md`, and `.claude/references/SESSION-AND-EVIDENCE.md`. Inspect filenames in `assets/`; read relevant text-based material, but do not modify it.

## Interaction

Begin immediately with this outcome: “We’ll set up the project first. I’ll ask one short question at a time.”

Use **Workshop mode** by default. Do not ask the participant to choose a mode. Use Deep Research only when the participant explicitly requests it.

Ask these four questions in order, one turn at a time:

1. What is the business, offer, or idea in one or two sentences?
2. What stage is it at today: idea, pre-launch, early customers, or established? Invite a correction rather than forcing the options.
3. Who might buy or use it, in which geography and language? Make clear that this is the participant's starting view, not a validated audience.
4. What one action should the website generate first, and where will the first visitors most likely come from?

Do not ask again for information already clearly supplied in the current chat or assets. State the answer you inferred and ask the next missing question.

After question four, show a compact setup proposal:

- project and stage;
- participant's starting audience hypothesis;
- website action and expected first traffic;
- relevant supplied materials only when at least one useful file exists.

Do not mention the default Workshop mode, an empty `assets/` folder, or missing materials in the participant-facing proposal or final summary. Missing materials may be raised later only when a specific stage actually requires them.

Ask one question: “Is this accurate enough to create the session?”

## Save

After confirmation:

1. Create a new timestamped session folder.
2. Create `SESSION.md` with `Path: Full`, following `.claude/references/SESSION-AND-EVIDENCE.md`.
3. Create `00-setup.md` with the confirmed context, mode, asset inventory, explicit hypotheses, constraints, and unresolved questions.
4. Do not create any later stage files.

Finish with three short bullets: what was decided, the saved file path, and “Next: `/vision`”.

## Quality gate

- Exactly one question per turn.
- No recalled memory or past chat context.
- No strategic audience or offer conclusion presented as fact.
- No extra administrative files.
- No participant-facing narration about empty folders or default mode.
