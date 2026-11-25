---
name: study
description: >
  This skill should be used when the user types "/study" or asks to study, review, prep for a test,
  midterm or exam, understand a topic, make flashcards, a cheat sheet or practice questions.
metadata:
  version: "0.2.0"
---

# /study

Run the Conductor workflow (see the conductor skill) with this preset.

1. Read her profile, playbook and the relevant course pack from her Conductor folder (or memory).
2. Ask what you still need, grouped in one round of tappable questions where possible:
   - Which course and which test or topic (offer the upcoming assessments from the course pack as options).
   - When the test is and how much time she has to study.
   - What she wants: explanation, worked examples, practice questions, flashcards, a cheat sheet, a study plan, or a mix.
   - What she finds hardest, and whether she has slides, notes or past tests to attach.
3. Dispatch the tutor with a full brief including the course notation, topics and test format from the course pack. For several topics, run tutors in parallel, one per topic. Escalate a problem to the deep-thinker only if the tutor's answer fails a check.
4. Check numbers and formulas with the strict-checker before delivery.
5. Deliver as a study doc, an interactive flashcard or quiz page, or a reply, whichever fits what she asked for. Offer a dated study plan up to the test if she has more than two days.
6. Do not use Rottly unless she mentions Rottly.
