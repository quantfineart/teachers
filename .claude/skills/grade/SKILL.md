---
name: grade
description: Help with grading, report cards, rubrics, or student assessment
user-invocable: true
---

# /grade — Grade or Assess Students

Follow these steps exactly. Respond in the teacher's language (match whatever language they write in).

1. **Read `teacher-profile.md`** — if the profile has no name filled in, run the Setup Flow from CLAUDE.md first before proceeding. Otherwise, know the grading system, assessment model, mandated weightings (e.g., DepEd: Written 30%, Performance 50%, Quarterly 20%), comment style, and curriculum standards. If the profile is sparse (early sessions), ask what you need as part of step 2.

2. **Ask what they're assessing** — and offer clear options:
   - "One student or a few specific students?"
   - "Your whole class at once?"
   - "A rubric or marking criteria sheet?"
   - "A comment bank you can reuse?"
   Bundle with any other needed questions (max 3 total).

3. **Privacy check**:
   - For templates and practice: use pseudonyms ("Student A", "Child B") by default.
   - For real report cards: confirm — "This will include real names. Is this for your school's internal use?" Then proceed.
   - **Never** save student names, grades, or personal details to the profile.

4. **Always lead with strengths** — never open an assessment with what the student can't do.

5. **Generate using the teacher's system**:
   - Map observations to their curriculum standards (CCSS, National Curriculum, DepEd MELCs, ACARA, etc.)
   - Use their grading format (letter grades, percentages, competency levels, narrative, etc.)
   - Match their voice — formal, warm, direct — based on how they write
   - Include parent-facing recommendations (actionable things parents can do at home)
   - Respect mandated assessment structures stored in profile

6. **For batch mode** (whole class) — offer TWO approaches:
   - **Individual notes approach**: teacher pastes a class list with brief notes per student. Claude generates individual comments.
   - **Comment bank approach**: teacher describes 4-5 performance levels (e.g., "struggling with basic facts," "solid but careless," "exceeding expectations"). Claude generates a bank of 5-8 comments per level. Teacher assigns comments to students themselves. This is faster for 30+ students.
   - Ask which approach they prefer. Default to comment bank for classes over 25.
   - **Multiple classes**: For teachers with several classes, process one class at a time. Ask "Which class should we start with?" Generate one output per class, not one mega-file for all students.

7. **Output format**:
   - Single student or small group: plain text (easy to copy-paste into school systems)
   - Whole class batch: a printable page with all comments, one per student, with a line between each
   - Comment bank: a printable page organized by performance level
   - Rubric: a printable page with criteria grid
   - Always ask if they want it in a specific format for their school system

8. **After delivery**, offer one follow-up: "Want me to create a parent-facing version too?" or "Need a rubric to go with this?"

9. **Update `teacher-profile.md`** with any new preferences discovered (comment style, grading system, mandated weightings, etc.).
