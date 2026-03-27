---
name: lesson
description: Create a lesson plan — single lesson, weekly plan, or full term/year plan
user-invocable: true
---

# /lesson — Create a Lesson Plan

Follow these steps exactly. Respond in the teacher's language (match whatever language they write in).

1. **Read `teacher-profile.md`** — if the profile has no name filled in, run the Setup Flow from CLAUDE.md first before proceeding. Otherwise, know the teacher's system, curriculum, pedagogy, calendar, output format preference, textbook, class size, and resources. If the profile is sparse (early sessions), ask what you need as part of step 2.

2. **Ask only what's missing for THIS plan** — topic, date/time slot, any special requirements. If the profile already has subject, level, and curriculum, don't re-ask. Bundle questions together (max 3).

3. **Confirm output format** if not already saved in the profile. Offer these options in plain language:
   - "A page you can open in your browser and project in class" → create an `.html` file with interactive elements, bright colors, large text
   - "A clean page you can print" → create an `.html` file with print-friendly CSS, page breaks, no dark backgrounds, works offline
   - "Text you can copy and paste into Word or Google Docs" → output directly in the chat as clean formatted text, easy to select and paste
   - "A presentation with slides" → create an `.html` file structured as a slide deck
   - "Plain text you can copy into Google Classroom, Seesaw, etc." → output directly in the chat (no file), easy to copy

   **Never mention file formats (.html, .md, CSS) to the teacher.** Just say "Here's your lesson plan — double-click to open it" or "Here it is — you can copy and paste this."

4. **Generate the plan** using the correct curriculum standards, terminology, and structure for their system. Include:
   - Learning objectives aligned to their curriculum
   - Materials and resources list (only what they actually have access to)
   - Activities with timing
   - Differentiation appropriate to their system
   - Assessment checkpoints
   - Homework (if standard in their system)
   - Values/character integration (if required by their curriculum)
   - Teacher prep time estimate (for week/term plans)

5. **For plans longer than 4 weeks**: produce an overview first for approval. After approval, generate detail in chunks — per week or per quarter. Ask: "Want me to put it all in one file, or separate files per week?"

6. **After delivery**, offer one follow-up: "Want a worksheet to go with this?" or "Need a quiz for the end?" Keep it brief — one suggestion, not a list.

7. **Update `teacher-profile.md`** with any new preferences discovered (output format, plan structure, lesson plan format, etc.).
