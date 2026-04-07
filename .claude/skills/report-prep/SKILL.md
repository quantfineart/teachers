---
name: report-prep
description: Set up a new report writing task — conversational flow, creates brief.md and students.md automatically, then collects student tags
user-invocable: true
---

# /report-prep — Set Up a Report Writing Task

This is a conversational skill. Ask questions one step at a time. Never show the teacher a file or ask them to edit anything directly. Fill in all files yourself from their answers.

---

## Step 1 — Read context

Read `teacher-profile.md`. Know the school, year groups, folder structure, grading system, grade boundaries, and tag taxonomy before asking anything.

---

## Step 2 — Ask Question 1

Ask only this (friendly, one question):

> "Which year group is this for, and is it a semester or term report — which one?"

Wait for the answer before continuing.

---

## Step 3 — Check for existing files

Determine the folder path: `CHS/[year]/Year [X]/reports/[semester-N or term-N]/`

Check if `brief.md` or `students.md` already exist there.

- If they exist and have content, say:
  > "There's already a report set up for [Year X] [Semester/Term N]. Do you want to start fresh, or continue with what's there?"
  - If start fresh: delete existing files and continue
  - If continue: skip to Step 8 (tag collection)

- If they don't exist: continue to Step 4

---

## Step 4 — Ask Question 2

> "What topics did you cover this [semester/term]? And what were the assessment tasks — just the name, what it covered, and how many marks each."

Wait for the answer. Accept any format — bullet points, a sentence, a rough list. Don't require precision.

If they mention a due date, note it. If not, don't ask — it can be filled in later.

---

## Step 5 — Create brief.md

Create the folder if needed. Write `brief.md` from their answers. Use this structure:

```
# Year [X] [Course] — [Semester/Term N] Report [Year]

Status: PENDING

---

## Report Details

Due date: [if mentioned, otherwise leave blank]
Reporting period: [Semester/Term N], [Year]
Year group: Year [X]
Course: [course name from profile]

---

## Topics Covered This [Semester/Term]

[list topics from their answer]

---

## Assessment Tasks

| Task | Topic | Max Marks |
|------|-------|-----------|
[one row per task]
| **Total** | | **[sum]** |

---

## Class Notes

[leave blank — filled later if needed]
```

Confirm back in plain language:
> "Got it — I've noted [topics] with [tasks]. Now for your students — you can paste your mark sheet, type names and marks directly, or add them later. What works best for you?"

---

## Step 6 — Collect student data

Accept any of these formats — map them to the right columns yourself:

**Option A — paste from Excel/Google Sheets** (tab or comma separated):
```
James    M    10    24
Priya    F    8     19
```

**Option B — typed list**:
```
James M 10 24
Priya F 8 19
```

**Option C — conversational** ("James is a boy, got 10 and 24"):
Extract name, gender, marks from whatever they say.

**Option D — later**:
If they say "I'll add students later", create `students.md` with just the header and column structure, no rows. Skip tag collection for now. Tell them: "Come back when your marks are ready and we'll add the tags then."

For gender: M = he/him, F = she/her, B = they/them. If not mentioned, don't ask — leave blank.

---

## Step 7 — Create students.md

Build the Marks Key table from brief.md tasks. Calculate grade boundary mark ranges from the profile's percentage boundaries and this assessment's total marks.

Write `students.md` with this structure:

```
# Class List — Year [X] [Course], [Semester/Term N] [Year]

## Marks Key

| Task | Topic | Max Marks |
|------|-------|-----------|
[one row per task]
| **Total** | | **[sum]** |

## Grade Boundaries

| Grade | Percentage | Mark /[total] |
|-------|------------|---------------|
| A | 85–100% | [calculated] |
| B | 70–84%  | [calculated] |
| C | 50–69%  | [calculated] |
| D | 30–49%  | [calculated] |
| E | 0–29%   | [calculated] |

---

## Students

| Name | Gender | T1 /[max] | T2 /[max] | ... | Total /[total] | Grade | Tags |
|------|--------|-----------|-----------|-----|----------------|-------|------|
[one row per student — Tags column left blank until Step 8]
```

Show the teacher a brief summary:
> "All [N] students are in. Here's how they're sitting: [grade breakdown table]"

Then move immediately to Step 8.

---

## Step 8 — Collect student tags

This step is mandatory — do not skip it, do not offer to skip it.

Say:
> "Now I need one thing from you for each student — their tags. These shape the whole tone of the comment. Each student can have as many as apply.
>
> Here are the options:"

Show the tag list in a clean, readable format:

**Character:**
committed · dedicated · diligent · hardworking · conscientious · industrious · cooperative · focused · capable · respectful · quiet and industrious

**Classroom behaviours (positive):**
participative · keeps work up to date · always asks the right question when stuck · completes work

**Areas for growth (used constructively):**
quiet · should participate in class discussions · should ask for assistance when stuck · requires support · requires assistance · incomplete work · inconsistent · low participation · always tried · unfocused

> "You can use your own words too — I'll map them. Just go down the list."

Show the student list as a simple table with a blank Tags column:

| # | Student | Grade | Tags |
|---|---------|-------|------|
| 1 | [Name]  | [A/B/C/D/E] | |
...

Wait for the teacher to fill in all tags. Accept any format — one per line, all at once, shorthand. Do not generate comments until tags are received for all students.

---

## Step 9 — Update students.md with tags

Add the tags to each student's row in `students.md`.

Confirm:
> "Tags saved for all [N] students. Just say 'generate Year [X] reports' when you're ready and I'll write all the comments."

---

## Step 10 — Update teacher-profile.md

Add to Session Log: "Set up report task: Year [X] [Semester/Term N] [Year] — [N] students, tags collected"
