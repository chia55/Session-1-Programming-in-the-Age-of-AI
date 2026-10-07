# Guide 02 · What is a program?

## The short answer

A **program** is a list of precise instructions that a computer follows, one step at a time, to turn some **input** into some **output**.

```
   INPUT  ──►  PROCESS (the instructions)  ──►  OUTPUT
  amount paid      "subtract the price"         change to give back
```

You already use dozens of programs every day:

| You do this… | A program is… |
|--------------|---------------|
| Dial `*334#` and send money with M-Pesa | checking your PIN, checking your balance, moving the money, sending both of you an SMS |
| Ask Google Maps for the fastest route to town | reading live traffic, comparing possible routes, choosing the shortest time |
| Watch a video on TikTok | deciding which video to show you next based on what you watched before |
| Tap your card at the supermarket | adding up items, applying discounts, contacting the bank |

## How a computer follows instructions

A computer is **extremely fast** and **extremely literal**.

- **Fast:** a cheap phone can do billions of simple operations every second.
- **Literal:** it does *exactly* what the instructions say, not what you *meant*. It has no common sense.

### The "make tea" experiment

Imagine giving a robot this instruction: *"Make me a cup of tea."*

A human understands. A robot doesn't know where the kettle is, how much water to use, whether you take sugar, or that you should switch the kettle *off* afterwards. To a computer, you must say something more like:

1. Pick up the kettle.
2. Fill it with 500 ml of water.
3. Put it on the base and switch it on.
4. **Wait until** the water boils.
5. Put one tea bag in a cup.
6. Pour 250 ml of the hot water into the cup.
7. **If** the person wants milk, add 50 ml of milk.
8. **If** the person wants sugar, add one spoon of sugar **for each** spoon requested.
9. Stir for 10 seconds.
10. Hand over the cup.

Notice three special words in bold. Almost every program in the world is built from these three ideas:

| Idea | Example word | Programming name | Session |
|------|--------------|------------------|---------|
| Do things in order | "then" | **sequence** | today |
| Choose between options | "if" | **selection / decisions** | Session 2 |
| Repeat something | "for each", "until" | **iteration / loops** | Session 3 |

## From human language to machine language

Computers only understand **machine code**: patterns of 1s and 0s. Writing that directly is painful, so people invented **programming languages** that look closer to English.

```
You write (Python):        print("Habari!")
         │
         ▼   the Python interpreter translates it
Computer runs:             10110000 01100001 …  (machine instructions)
         │
         ▼
You see:                   Habari!
```

**Python** is a *high-level* language: it reads almost like English and hides the hard details. That's why it is the most popular first language, and why it's used everywhere from schools to NASA.

### Interpreter vs. compiler (just the idea)

- Python is **interpreted**: the interpreter reads your code and runs it line by line. If line 5 has a mistake, lines 1–4 still run first.
- Languages like C are **compiled**: the whole program is translated into machine code before it runs.

You don't need to remember this. Just know that when you press ▶ in Colab, the Python interpreter reads your cell from top to bottom.

## Key vocabulary

| Word | Meaning |
|------|---------|
| **Program / code** | Instructions written for a computer |
| **Programming language** | A language with strict rules for writing those instructions (Python, JavaScript, SQL…) |
| **Syntax** | The grammar rules of a language. Break them and you get a *syntax error* |
| **Run / execute** | Make the computer carry out the instructions |
| **Input** | Data that goes into a program (typed text, a file, a sensor reading) |
| **Output** | What comes out (text on screen, a file, a chart, an SMS) |
| **Bug** | A mistake in a program |
| **Debugging** | Finding and fixing bugs |

## Check your understanding

1. In your own words, what is a program?
2. Pick an app on your phone. What is its input? What is its output?
3. Why is it a problem that computers are "literal"? Give an example.
4. Which of *sequence*, *selection* and *iteration* appear in these instructions: "Keep stirring the ugali until it is firm; if it is too soft, add more flour"?

<details>
<summary>Suggested answers</summary>

1. A precise list of steps a computer follows to turn input into output.
2. e.g. M-Pesa: input = phone number, amount, PIN; output = money moved + confirmation SMS.
3. The computer does exactly what you say, so missing or vague steps cause wrong results. "Add sugar" (how much?).
4. Iteration ("keep stirring until…"), selection ("if it is too soft…") and sequence (the steps happen in order).
</details>

Next: [03-thinking-like-a-programmer.md](03-thinking-like-a-programmer.md)
