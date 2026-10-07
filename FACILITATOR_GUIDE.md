# Facilitator Guide · Session 1 (FREE taster session)

**Goal of the session:** learners leave confident that *they* can program, understand why it matters in the AI era, and are excited to sign up for Sessions 2–8.

**Audience:** complete beginners. Assume no prior coding and limited familiarity with file systems.

## Before the session

- [ ] Test the room Wi-Fi with Colab. Colab needs a stable connection, but very little bandwidth.
- [ ] Add learners' GitHub usernames to the `Chia-ai` organisation (read access) **or** prepare the notebooks to share as files / a Google Drive folder.
- [ ] Have a backup: download the three `.ipynb` files to a USB stick.
- [ ] Print the recipe worksheet (1 per pair) or share it on screen.
- [ ] Check that Gemini in Colab works on your demo account. Have a backup AI chat open in another tab.
- [ ] Prepare 2–3 sticky notes per learner (green = "I'm done", red = "I need help") if teaching in person.

## Running order and teaching notes

| Time | Segment | Notes |
|------|---------|-------|
| 0:00 | Welcome & icebreaker | Ask: "Name one app you used today. What's its input and output?" Write answers on the board. |
| 0:10 | What is a program | Do the **"make tea" robot** live: a volunteer gives instructions, and you follow them *literally* (pour water on the floor if they forget the cup!). Big laughs, memorable lesson. |
| 0:20 | Thinking like a programmer | Walk through the matatu change example. Emphasise **edge cases** and **dry runs**. |
| 0:50 | Hands-on 1: recipes | Pairs choose tasks; insist on the swap-and-test step. Collect one great example to show. |
| 1:10 | Break | |
| 1:20 | Why code in the AI era | Show a short AI-generated program with a subtle bug (e.g. grade boundary `> 70` instead of `>= 70`) and ask who can spot it. Link back to *Understand · Check · Direct*. |
| 1:40 | Where Python is used | Keep it local: M-Pesa, agritech, county data, research. Mention PyCon Kenya / local communities. |
| 1:55 | Colab tour + first program | Everyone runs `print("Hello, World!")` **before** you move on. Walk the room. Then do the error cells together: read the last line aloud. |
| 2:25 | Hands-on 2: personal introduction | Learners write Exercise 7. Invite 2–3 volunteers to show theirs on the projector. |
| 2:50 | Wrap-up | Recap with the cheat sheet. Preview Session 2: "Next time your programs will *ask questions* and *make decisions*: a KSh tip calculator and a grading program." |

## Common issues

- **Pop-up blocked when authorising GitHub in Colab** → allow pop-ups for colab.research.google.com.
- **Learner edits the shared notebook and loses work** → remind everyone: *File → Save a copy in Drive*.
- **Smart quotes** (“ ”) pasted from Word/WhatsApp cause `SyntaxError: invalid character`. Retype the quotes in Colab.
- **Learners racing ahead with AI** → redirect: "Write yours first, then compare." Exercise 9 is built for this.

## Assessment for learning

Quick checks during the session:
1. Thumbs up/down: "Can you explain what an algorithm is to a friend?"
2. Exit ticket: each learner writes one sentence: *"AI can write code, but I still need to learn Python because…"*

## Conversion tips (free session → paid course)

- Show a teaser of the Session 7 dashboard and the Session 8 AI survey categoriser.
- Emphasise the hands-on, local datasets (county populations, a duka's sales, a student survey).
