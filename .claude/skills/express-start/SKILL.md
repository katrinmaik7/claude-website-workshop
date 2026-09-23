---
name: express-start
description: Start an Express workshop session in one run. Inspect participant assets, collect the minimum project context and founder intent in six short questions, then create the session index and the combined setup-and-vision file. Use at the beginning of a two-hour workshop run instead of /setup and /vision.
---

# Express start (setup + vision)

Create a clean Express session and record the participant's starting view in one stage.

Before speaking, silently read `CLAUDE.md`, `README.md`, and `.claude/references/SESSION-AND-EVIDENCE.md`. Inspect filenames in `assets/`; read relevant text-based material, but do not modify it.

## Interaction

Begin immediately with: “We’ll set up your project first. Six short questions, one at a time.”

Ask these questions in order, one per turn. Skip any question already clearly answered in the chat or in `assets/`; state what you inferred and move on.

1. What is the business, offer, or idea in one or two sentences, and what stage is it at today: idea, pre-launch, early customers, or established?
2. Who do you think will buy or use it, in which place and language?
3. Tell me about one real person or situation that shows why someone would look for this. What happened?
4. If this works, what becomes different for that person in practical terms?
5. What one real action should the website generate first, where should that action lead, and where will the first visitors most likely come from? For a pre-launch idea, the destination can be an existing email address, Instagram profile, WhatsApp link, simple form, booking page, or checkout.
6. What must the website never promise, imply, or pressure people to do?

Accept “I don’t know” for questions 3–4. For question 5, offer the three simplest truthful actions available to this participant and let them choose one; if no usable destination exists, record `Connection required before launch` rather than silently changing the goal to a brochure or scroll-only prototype. Do not ask for an essay.

## Checkpoint

Show at most five bullets:

- project and stage;
- starting audience and the example situation, labelled `Reported — founder`;
- intended customer change;
- website action and expected first traffic;
- boundaries.

Ask one question: “Is this accurate enough to start?”

Do not mention the default mode, an empty `assets/` folder, or missing materials.

## Save

After confirmation:

1. Create `sessions/<project>-<YYYYMMDD-HHMM>/`.
2. Create `SESSION.md` with `Path: Express`, following `.claude/references/SESSION-AND-EVIDENCE.md`.
3. Create `00-setup-and-vision.md` with the confirmed context, asset inventory, the participant's starting audience and example situation, intended customer change, business purpose when stated, website action and traffic assumption, boundaries, and 3–5 research questions for `/express-research`. Label every untested claim `Reported — founder` or `Hypothesis`.
4. Do not create later stage files.

Finish with three short bullets: what was decided, the saved file path, and “Next: `/express-research`”.

## Quality gate

- Exactly one question per turn; six questions at most.
- No recalled memory or past chat context.
- No audience, offer, or market conclusion presented as fact.
- No extra files.
