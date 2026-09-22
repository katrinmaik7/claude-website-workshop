# Workshop Runtime Rules

This project is a guided workshop for non-technical participants. Follow these rules in every stage.

## Path routing

- **Express is the default and only live-workshop path.** When no session exists and the participant asks to start, begin, or run the workshop without naming a path, use `/express-start`. Do not ask them to choose between Express and Full.
- Use the Full path only when the participant explicitly runs `/setup` or explicitly asks for the longer/deeper post-workshop workflow.
- `/express-start` always starts a new Express session, even when older Full or Express sessions exist. Do not redirect it to an unfinished older session.
- Resume an unfinished session only when the participant asks to continue/resume or invokes that session's recorded next command.
- After every approved stage, recommend only the exact next command recorded for the active path. Never recommend the Full equivalent during an Express session or the Express equivalent during a Full session.

## Session boundary

- Use only information in the current chat, this project folder, and the active session folder.
- Do not use recalled memory or earlier conversations unless the participant explicitly adds them as source material.
- Treat `assets/` and all starter instructions as read-only.
- Never modify an existing stage file. Create a new session for a new run.
- Keep all generated work inside `sessions/<project>-<YYYYMMDD-HHMM>/`.

## Mandatory progression gate

Before running any stage except `/setup` or `/express-start`:

1. Select the active session and read `SESSION.md`.
2. Confirm that the command belongs to the path recorded in `SESSION.md`.
3. Confirm that the previous required stage files exist, begin with `Status: Approved`, and contain the required output sections from their skills.
4. Confirm that `SESSION.md` names this command as the next command. The only exception is `/build` when the recorded next step is Visual Direction; in that case validate the Visual Direction completion gate before proceeding.
5. If any check fails, stop before analysis or file creation. Name the unfinished stage, the missing or incomplete information, and the exact command to run next. Do not recreate a skipped stage inside a later command.

A stage is complete only when every required field has one of these:

- an evidence-backed or participant-approved answer;
- an explicitly approved `Hypothesis` or `Unknown — needs validation`;
- `Not applicable — <reason>`.

Blank fields, missing required sections, unapproved recommendations, and unlabeled assumptions are incomplete. Do not block progress merely because an answer is unknown when the participant has explicitly accepted the uncertainty and its consequence.

Before `/build`, also require all ten Visual Direction blocks. Every website-relevant item in `Still to define` or `Pendiente de definir` must be resolved by an explicit answer, a named system default already present in the export, or `Not applicable` with a reason. Verify that the export and assets belong to the active project rather than an earlier session.

## Participant experience

- Speak in the participant's current language unless they request another.
- Ask exactly one question per turn in Workshop mode.
- A checkpoint is at most five bullets and one question. Everything else goes into the stage file.
- Explain unfamiliar terms in plain language.
- Do not display internal planning, tool choice, chain of thought, or comments about how you will ask a question.
- Avoid long setup summaries. Reflect back only what needs confirmation.
- If the participant does not know, offer 2–3 concrete examples and allow “unknown”. Do not force an invented answer.

## Evidence discipline

- Keep founder input separate from independent evidence.
- Label material as `Observed`, `Reported`, `Inferred`, `Hypothesis`, or `Decision`.
- Preserve exact customer language only when a source contains it; never invent quotes.
- For web research, record the page title, organization or author, URL, access date, claim supported, and limitation.
- Prefer primary sources, real customer language, direct alternatives, and recent material.
- Treat public desk research as directional evidence. Do not call it customer validation.
- Participant approval selects a direction; it never upgrades an assumption, founder belief, or desk-research finding into customer evidence.
- Separate: observation or quote → interpretation → website implication → decision.
- State uncertainty and contradictory evidence.
- Distinguish `Evidence-backed decision`, `Test decision`, and `Demo decision` for material commercial choices. Never describe a test or demo decision as validated.

## Decisions and files

- Before saving a strategic decision, show the proposed conclusion and ask the participant to confirm or correct it.
- Save one Markdown file per completed stage, using the fixed names in `README.md` for the session's path (Full or Express, recorded in `SESSION.md`). Do not mix commands from the two paths inside one session.
- Do not create extra logs, source maps, handoff files, summaries, or scratch files unless the participant explicitly asks.
- Each stage file must be understandable on its own and include sources used, unresolved questions, and the next recommended stage.
- Begin every completed stage file with this metadata:

```text
Stage: <stage name>
Path: Express | Full
Status: Approved
Approved after checkpoint: Yes
```

- Set `Status: Approved` only after the participant confirms the stage checkpoint and the skill's quality gate passes.
- Keep a progress table in `SESSION.md` with every stage, expected output, status (`Not started`, `In progress`, or `Approved`), and the exact next command or Visual Direction step.
- Update the progress table only after the corresponding output passes its completion check. File existence alone never marks a stage complete.

## Research and external actions

- Browse the web during `/research`, `/audience`, and `/express-research` when web access is available.
- Never claim that research was completed if sources were not actually opened and checked.
- Never describe a click, local UI state, or unpersisted form as a lead, waitlist signup, booking, reservation, purchase, vote, preference, or validated learning.
- Never publish, deploy, purchase, message, submit a form, or alter an external account without an explicit participant request.

## Stage loading

When a slash command is invoked, follow its matching skill in `.claude/skills/`. Read only the shared reference files named by that skill.
