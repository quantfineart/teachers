---
name: report-generate
description: Generate report comments for a class — reads brief.md and students.md, writes comments.md using the teacher's style, tags, and sample reports
user-invocable: true
---

# /report-generate — Generate Report Comments

This skill generates a full set of report comments for one class. It is conversational but mostly automated — the teacher's work was done in /report-prep. This step is about producing the output.

---

## Step 1 — Read everything

Read all of the following before writing a single comment:

1. `teacher-profile.md` — grading system, comment style rules, word rules, tag taxonomy, comment structure
2. `CHS/samples/report/` — read all sample files including any PDFs. These are the gold standard for voice, structure, and tone.
3. The relevant `brief.md` — topics, assessment tasks, reporting period
4. The relevant `students.md` — marks, grades, tags for every student

If the year group is not clear from context, ask:
> "Which year group's reports should I generate?"

Determine the folder path: `CHS/[year]/Year [X]/reports/[semester-N or term-N]/`

---

## Step 2 — Check tags are complete

Check `students.md`. If any student is missing tags, stop and ask:
> "A few students don't have tags yet — [list names]. What tags apply to them?"

Do not generate comments for any student without tags. Wait for the answer.

---

## Step 3 — Generate all comments

Write every comment using these non-negotiable rules (from teacher-profile.md):

### Structure (mandatory for every comment)
1. **Open** with `[Name] is a [tag(s)] student who has achieved a [result word] result in the [Examination/Task].`
2. **Strength first** — name the topic(s) the student performed well in before mentioning any weakness
3. **Classroom behaviour** — weave in one observation drawn from their tags (e.g. keeps work up to date, participates actively, seeks help at the right moments, works independently)
4. **Advice** — specific and actionable, matched to their grade and tags
5. **Close** — `By continuing to work diligently, [pronoun] should be able to achieve further success in this course.` (vary closing slightly across the class — don't use identical wording for every student)

### Word rules (mandatory)
- **No raw marks or scores** — describe results in words only: outstanding, exceptional, high, sound, satisfactory, basic
- **Result words by grade:** A → outstanding / exceptional | B → high / commendable | C → sound / satisfactory | D → satisfactory (use carefully) | E → basic / limited
- Student name used **max 2–3 times** per comment — use pronouns for the rest
- **Never repeat** the same key word — vary "examination" with "task" or "assessment"
- **No "near-perfect"** or vague superlatives — be specific or omit
- Use **"harder questions"** or **"harder problems"** — not "harder problem types"
- **Never** repeat the course name at the end — always use "this course"
- Max ~600 characters per comment

### Tag-to-language mapping

| Tag | How it appears in the comment |
|-----|-------------------------------|
| committed | "committed student" in opener |
| dedicated | "dedicated" in opener or body |
| diligent | "diligence" in body or advice |
| hardworking | "hardworking" in opener |
| conscientious | "conscientious" in opener |
| industrious | "industrious" in opener |
| cooperative | "cooperative" in opener |
| focused | "focused approach" in body |
| capable | "capable" in opener — pair with gap/advice |
| respectful | "respectful" in body |
| participative | "active participation in class" in body |
| keeps work up to date | "consistently keeps her/his work up to date" in body |
| always asks the right question when stuck | "habit of seeking clarification at the right moments" in body |
| completes work | "ensures all set tasks are completed" in body |
| quiet | "quiet" in opener — follow with encouragement to participate or seek help |
| should participate in class discussions | end advice with encouragement to participate |
| should ask for assistance when stuck | end advice with encouragement to seek help |
| requires support / requires assistance | gentle, supportive tone throughout; close with teacher-support line |
| incomplete work | mention "would benefit from ensuring all set work is completed" in advice |
| inconsistent | use "capable" opener, name the inconsistency, advise structured revision |
| low participation | open with any positive tag first; encourage active engagement in advice |
| always tried | use as opening positive: "has shown a willingness to try throughout the semester" |
| unfocused | handle gently; frame as encouragement toward consistency |

### Variation rules
- **No two comments should open the same way** — vary the character descriptor, the result sentence structure, and the closing
- Students with similar marks and grades must still have clearly different comments if their tags differ
- For students with identical grades AND similar tags, vary the topic emphasis, the advice sentence, and the closing phrasing

---

## Step 4 — Write comments.md

Save to: `CHS/[year]/Year [X]/reports/[semester-N or term-N]/comments.md`

Use this structure:

```
# Year [X] [Course] — [Semester/Term N] [Year] — Report Comments

---

## [Name] — Grade [X] 

[Comment text]

---

## [Name] — Grade [X]

[Comment text]

---
```

Do not include raw marks in the headings or anywhere in the file.

---

## Step 5 — Confirm delivery

Show the teacher a grade breakdown summary, then say:
> "All [N] comments are written. Have a read — let me know which ones need adjusting and I'll fix them."

Do not offer unsolicited rewrites. Wait for feedback.

---

## Step 6 — Handle revisions

If the teacher asks to change a specific comment:
- Read their feedback carefully
- Rewrite only that comment — do not touch others
- Update `comments.md` in place
- Show the revised comment for confirmation

If they say "all comments are too similar" or "too mechanical":
- Re-read the sample reports
- Identify which structural elements are repeating
- Rewrite the full batch with greater variation in openings, body structure, and closings
- Do not ask clarifying questions — just rewrite and present

---

## Step 7 — Mark brief.md complete

When the teacher is satisfied, update `brief.md`:

Change `Status: PENDING` to `Status: COMPLETE — [date]`

---

## Step 8 — Update teacher-profile.md

Add to Session Log: "Generated Year [X] [Semester/Term N] [Year] report comments — [N] students"

If the teacher gave feedback during revision (e.g. "don't reference marks", "add classroom behaviour"), check if the rule is already in the profile. If not, add it to the relevant section.
