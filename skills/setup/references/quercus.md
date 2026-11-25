# Navigating Quercus

Quercus is U of T's Canvas site at https://q.utoronto.ca. Use Claude in Chrome so you work in her signed-in session.

## Sign-in

- If a U of T login page (weblogin) or Duo prompt appears, stop and ask her to sign in and approve Duo herself. Never enter her UTORid password or approve Duo for her.
- Once she is signed in, continue in the same tab.

## Fastest path: Canvas JSON pages

While signed in, these addresses return readable JSON in the browser. Read them with the page-text tool. They are read-only and much faster than clicking through the interface.

| What | Address |
|---|---|
| Current courses | `https://q.utoronto.ca/api/v1/courses?enrollment_state=active&include[]=term&per_page=50` |
| Assignments with dates | `https://q.utoronto.ca/api/v1/courses/<id>/assignments?per_page=100&order_by=due_at` |
| Course syllabus body | `https://q.utoronto.ca/api/v1/courses/<id>?include[]=syllabus_body` |
| Front page | `https://q.utoronto.ca/api/v1/courses/<id>/front_page` |
| Modules and items | `https://q.utoronto.ca/api/v1/courses/<id>/modules?include[]=items&per_page=100` |
| Files list | `https://q.utoronto.ca/api/v1/courses/<id>/files?per_page=100&sort=updated_at` |
| Recent announcements | `https://q.utoronto.ca/api/v1/announcements?context_codes[]=course_<id>&per_page=20` |
| Teachers and TAs | `https://q.utoronto.ca/api/v1/courses/<id>/users?enrollment_type[]=teacher&enrollment_type[]=ta` |

Rules:
- Only read (GET). Never submit, post, or change anything on Quercus.
- Course ids come from the first address. Filter to the current term.
- If a JSON page errors or is blocked, fall back to the interface below.

## Interface fallback

- Dashboard: `https://q.utoronto.ca/` lists course cards.
- In a course: Syllabus, Modules, Assignments and Files are in the left menu. Many U of T courses put the syllabus PDF in Modules or Files rather than the Syllabus page.
- Rubrics appear on each assignment page under the instructions.
- PDFs open in the browser viewer; read them there with the page-text tool when possible.

## Where things usually are

- Grading breakdown and policies (late work, missed tests, academic integrity, AI use): the syllabus PDF.
- Test and exam dates: the syllabus and announcements; final exams are often "TBA" until the exam schedule is out, so note them as TBA.
- Rotman courses (RSM) often keep case readings and slides in Modules by week.

## Privacy

- Do not collect grades, other students' names, or discussion posts.
- Save only what helps her study and plan.
