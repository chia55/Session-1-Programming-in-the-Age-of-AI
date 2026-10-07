# Guide 04 · Why learn to code when AI can write code?

AI assistants (Gemini, ChatGPT, Claude, Copilot and others) can now write working code from a plain-English request. So it's fair to ask: *why spend eight sessions learning Python?*

**Short answer:** AI makes a programmer faster, but it doesn't remove the need for one. Someone still has to **understand** what the code does, **check** that it is correct, and **direct** the AI towards the right problem. That someone is you.

## A useful mental model: AI is a very fast junior assistant

Imagine you hired an assistant who:

- types incredibly fast and has read millions of programs ✅
- never gets tired ✅
- sometimes misunderstands what you asked ⚠️
- occasionally invents things that sound right but are wrong ⚠️
- doesn't know your data, your business, or what "correct" means for you ⚠️
- will never be blamed when things go wrong; **you** will ❗

Would you sign off on their work without reading it? A manager who can't read the work can't tell good from bad. That's why the skill is shifting from *typing code* to **understanding, checking and directing code**.

## The three skills: Understand · Check · Direct

### 1. Understand

You need to be able to read code and say what it does. Otherwise you can't tell if the AI solved *your* problem or a slightly different one.

> **Example.** You ask: *"Calculate the average mark of my class."* The AI writes code that quietly **skips students with missing marks**. Is that what you want? Or should a missing mark count as zero? Only someone who reads the code notices the choice it made.

### 2. Check

AI output can look perfect and still be wrong. Common problems:

| Problem | What it looks like |
|---------|--------------------|
| **Wrong logic** | Grade boundaries off by one: a mark of exactly 70 gets a B instead of an A |
| **Out-of-date code** | Uses features that newer library versions removed. You'll see this with pandas in Session 5 |
| **Invented ("hallucinated") functions** | Calls something like `pandas.auto_clean()` that does not exist |
| **Wrong assumptions** | Treats `KSh 1,200` as text, so the total is wrong |
| **Security & privacy issues** | Puts a password in the code, or sends personal data to an outside service |
| **Misleading charts** | An axis that doesn't start at zero, making a small change look huge |

Checking means: run it, test it with examples where *you know the right answer*, and read it.

### 3. Direct

Good results come from good instructions. Compare:

> ❌ *"Analyse my data."*
>
> ✅ *"I have a CSV of 600 student survey responses with columns age, county and monthly_allowance_ksh. Using pandas, calculate the median allowance per county, sorted from highest to lowest. Explain each step."*

To write the second prompt you need to know what a CSV is, what a median is, what pandas is, and what "per county" means in code. **The better you understand programming, the better you can direct AI.**

## What this means for how we learn

In every session you will:

1. **Learn the concept yourself first.** No AI for the very first attempt.
2. **Use AI to explain**: errors, confusing lines, new ideas.
3. **Compare your solution with an AI solution** and spot the differences (Session 3 onwards).
4. **Verify AI claims**, especially about data and charts (Sessions 7 and 8).
5. **Use AI honestly**: say when and how you used it, and protect personal data (Session 8).

## Prompt patterns that help you learn (try these in Colab's Gemini panel)

| Goal | Prompt pattern |
|------|----------------|
| Understand code | *"Explain this code line by line for a beginner: …"* |
| Understand an error | *"Explain what this error means and why it happened. Don't fix it for me yet."* |
| Get a hint, not an answer | *"I'm learning. Give me a hint for the next step, not the full solution."* |
| Check your work | *"Here is my solution. What edge cases might it miss?"* |
| Learn alternatives | *"Show me another way to write this, and compare the two."* |

## Discussion questions (for class)

1. Would you trust an AI-generated M-Pesa payment program that nobody on the team could read? Why or why not?
2. Which jobs do you think will change most because of AI coding tools? Which skills will stay valuable?
3. Have you seen an AI give a confident but wrong answer? What happened?

Next: [05-where-python-is-used.md](05-where-python-is-used.md)
