---
name: setup
description: >
  This skill should be used the first time the user uses Conductor, when she says "set me up",
  "run setup", "/setup", "new term", "refresh my courses", "update my course packs", or pastes
  her profile, or when Conductor finds no profile or course packs. It builds her profile,
  connects her Conductor folder, reads her courses on Quercus and writes a course pack for each,
  and offers a weekly check-in.
metadata:
  version: "0.2.0"
---

# Conductor setup

Set the user up so every future request starts with real knowledge of her and her courses. Run it once at the start, and again each term or whenever she asks to refresh. Speak plainly; never mention file paths, skills, hooks or agents unless she asks.

Before starting, tell her what will happen in two sentences and roughly how long it takes (10 to 20 minutes, most of it hands-off). Use a task list so she can see progress.

## Step 1: Her Conductor folder

All of her knowledge lives in one folder on her computer, so it survives across chats and every helper can read it.

1. Ask her to allow access to a folder named `Conductor` inside her Documents folder (create it if it doesn't exist). Request access through the device folder tools; if that isn't possible, ask her to add the folder with "Add folder" in the desktop app.
2. Create this structure if missing:
   ```
   Conductor/
     profile.md          who she is and how she likes things
     playbook.md         lessons learned: what works, what to avoid
     courses/
       <COURSECODE>.md   one course pack per course
       <COURSECODE>/     source files for that course (syllabus, rubrics)
     weekly/             weekly plans
   ```
3. If no folder can be connected (for example she is on her phone), fall back to memory: save the profile and a short version of each course pack as memory notes, and tell her the full setup works best in the desktop app.

## Step 2: Profile

1. Ask whether she already has a profile written up (from the profile prompt). If yes, have her paste it.
2. Fill gaps with a short interview, grouped into one or two rounds of tappable questions: program and goals, how she likes answers, how she learns best, writing voice, what she uses Claude for, apps she has connected.
3. Write `profile.md` using `references/profile-template.md`. Save the most important points to memory as well, so plain chats also know them.
4. Leave out passwords, account numbers, health and money details.

## Step 3: Quercus course packs

Read `references/quercus.md` for exactly how to navigate Quercus. In short:

1. Open Quercus (q.utoronto.ca) in her Chrome with Claude in Chrome (load the browser tools first). If she is not signed in, ask her to sign in with her UTORid and approve Duo herself; never type her password.
2. List her current-term courses and confirm the list with her (drop clubs, sandboxes and old courses).
3. For each course, gather: course name and code, section, professor and TAs with contact and office hours, grading breakdown, every assessment with date and weight, assignment instructions and rubrics, the syllabus policies on late work, collaboration and AI use, the textbook, weekly topics, and notation or formula conventions visible in slides.
4. Read pages and PDFs in the browser wherever possible. If files need to be downloaded into her folder (syllabus, rubrics), list them with names and sizes and get one yes for the whole batch before downloading.
5. Write one course pack per course to `courses/<CODE>.md` using `references/course-pack-template.md`. Use the tutor helper to draft the "Key concepts and formulas" section from the syllabus topics and slides, and the quick-helper to tidy dates into the calendar table. Pay special attention to the course's AI-use policy; record it word for word in a short quote if it is short, otherwise summarize it precisely.
6. Show her a short summary per course (assessments coming up in the next three weeks, AI policy in one line) and ask her to correct anything wrong.

## Step 4: Calendar and check-ins

1. If Google Calendar or another calendar is connected, offer to add her upcoming assessment dates. Ask first and list the events.
2. Offer a weekly check-in: a scheduled task every Sunday evening that reads her course packs and playbook and sends her "your week": deadlines, what to start now, and a suggested study plan (see the `week` skill). Create it only if she says yes, and tell her which approval setting it got.

## Step 5: Wrap up

1. Write the first lines of `playbook.md` from anything she said about what she likes or dislikes.
2. Tell her in a few lines what Conductor now knows, and the shortcuts she can use: `/study`, `/email`, `/apply`, `/research`, `/slides`, `/week`, and that she can always just type normally.
3. Remind her to say "refresh my courses" next term, or whenever a course posts a new syllabus or assignment.

## Refresh mode

When she asks to refresh, reopen Quercus, look only for what changed (new assignments, changed dates, new announcements about assessments), update the course packs, and summarize the changes.
