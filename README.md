# Study Coach

A study coach that runs inside an AI agent. You put one instructions file in a folder with your course materials, point an agent at the folder, and it does the rest:

- learns about you and your goals
- figures out what your course covers
- tests what you already know
- teaches you the rest
- keeps track of your progress between sessions

It works for any course, and it's built especially for hard STEM classes where you need to actually understand the material, not just memorize it.

## What you need

- An AI agent that can **read and write files in a folder on your computer**, such as the Claude desktop app with a folder attached, or Claude Code.
- Your course materials.

## Setup

**1. Make a folder for one course** (e.g. `Linear Algebra`). Use a separate folder for each class.

**2. Download `coach_instructions.md`** from this repo and put it in the folder.

**3. Add your course materials to the folder.** The more you add, the better the coach gets:
- **Textbook or lecture notes**: what it teaches from
- **Syllabus or course schedule**: what's covered and when the exams are
- **Past tests, quizzes, homework or practice problems**: how your instructor asks questions and grades them
- **Your graded work** (optional): shows exactly where you lose points

PDFs are fine.

**4. Open a new chat with the folder attached and send:**

```
Read coach_instructions.md in this folder and follow it. Start.
```

## What happens the first time

1. **It reads your materials** and builds a `course_brief.md`: what the course covers, the schedule, the exam format and what your instructor emphasizes.
2. **It asks you a few questions:** your goal and deadline, how much time you have, how fast you want to go, how deeply you want to understand the material, and how you like to learn and get feedback.
3. **It gives you a short diagnostic** to find out what you actually know.
4. **It creates your tracking files** and a study plan.

You can speed this up by including details in your first message, for example: *"...Start. My final is Dec 8 and I can study about an hour a day."*

## Every session after that

Start a **new chat** each time with the same message:

```
Read coach_instructions.md in this folder and follow it. Start.
```

It picks up where you left off. All of its memory lives in the folder, so short, fresh chats work best.

## Just ask it things

You don't need special commands. Talk to it normally. For example:

- *"Make flashcards I can use on my phone."* It can export them for apps like Anki or Quizlet and walk you through importing them.
- *"Where am I? Am I on track for the exam?"*
- *"Quiz me on chapter 3."*
- *"I'm stuck. Explain it more simply."*
- *"I only have 20 minutes today."*
- *"My exam moved to Friday."*
- *"Make this harder."* or *"Slow down."*
- *"Give me a practice exam like the real one."*
- *"How does this topic connect to what we did last week?"*

If you're not sure whether it can do something, ask it.

## Files it creates

| File | What it is |
|---|---|
| `course_brief.md` | What the course covers, the schedule, the exam style |
| `learner_profile.md` | Your goals, time and preferences |
| `plan.md` | Your study plan and whether you're on pace |
| `mastery.md` | How well you know each topic, and when you were last tested on it |
| `mistakes.md` | Every mistake you've made and whether it's fixed |
| `concept_map.md` | How all the ideas connect |
| `learning_rate.md` | How quickly you pick things up |
| `session_log.md` | A short record of each session |
| `review_cards.md`, `flashcards/` | Flashcards, if you want them |

You can read any of these. Leave them in the folder, because they're how the coach remembers you.

## Tips

- **Be honest** when it asks how confident you are. That's how it finds what you only think you know.
- **Try every question before asking for help.** The coach is built around making you recall things, which is what makes them stick.
- **Want to share your setup with a classmate?** Give them `coach_instructions.md`, `course_brief.md` and the course materials, but not your personal tracking files. Their coach will start fresh with them.
- **Want to start over?** Tell it *"start over."*
