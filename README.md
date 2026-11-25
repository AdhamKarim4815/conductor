# Conductor

A master Claude for U of T students who don't want to write detailed prompts. You ask in plain words; Conductor recalls what it knows about you and your courses, asks the questions it needs, writes an expert brief, and hands the work to the right helper on the right model and effort. It checks the result, delivers it in the right format, and records lessons so it improves over time.

## First run

Type `/setup` (or "set me up"). Setup:
1. Connects a `Conductor` folder in Documents where your profile, playbook and course packs live.
2. Builds her profile (paste one in if you have it).
3. Opens Quercus in her Chrome (she signs in herself), reads each current course and writes a course pack: people, grading, dates, rubrics, AI policy, topics, formulas.
4. Offers to add deadlines to her calendar and a Sunday-evening "your week" check-in.

Run "refresh my courses" each term or when new assignments go up.

## Shortcuts

`/study`, `/email`, `/apply`, `/research`, `/slides`, `/week`, `/setup`. Plain messages work too.

## Helpers

| Helper | Model | Effort | Job |
|---|---|---|---|
| quick-helper | Haiku | low | small lookups, rewording, formatting |
| researcher | Sonnet | medium | web research and comparisons |
| writer | Sonnet | high | emails, cover letters, essays, edits |
| tutor | Sonnet | high | course explanations, practice, study sheets |
| builder | Sonnet | medium | content for docs, decks, sheets |
| deep-thinker | Opus | high | hard problems, escalations |
| checker | Haiku | medium | quick review of everyday output |
| strict-checker | Sonnet | high | review of graded or important work |

## Notes

- Helpers, the startup hook and folder access work in the Claude desktop app. On web or phone, Conductor still plans and asks well, uses memory instead of the folder, and does the work itself.
- A startup hook reminds Claude to use Conductor in every session.
- Rottly is used only when she mentions it.
- Personal data stays in your folder and memory, never in the plugin, so the plugin can be updated or shared safely.
- To change a helper's model or effort, edit the `model` and `effort` lines in its file in `agents/`.
