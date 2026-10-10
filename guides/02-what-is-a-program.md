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

## From binary to Python: the levels of programming language

Computers only understand **machine code**: patterns of 1s and 0s. Writing that directly is painful, so over 80 years people invented languages that sit at higher and higher **levels**, each one closer to human language than the one below it.

| Level | Looks like | Who uses it today |
|-------|-----------|-------------------|
| **Machine code** (binary) | `10111000 11010010 …` | The CPU: the only thing it can actually run |
| **Assembly** | `mov eax, 210` | Chip makers, device drivers, microcontrollers |
| **Low-level / systems** (C, Rust) | `int total = 210 + 65;` | Operating systems, game engines, embedded devices |
| **High-level** (Python, JavaScript) | `total = 210 + 65` | Data, web, AI, automation: this course |
| **Natural language** (AI prompts) | "Add 210 and 65" | AI turns it into code, and you check it |

To compare them, we'll write **the same tiny program at every level**: a duka bill of KSh 210 + KSh 65 = KSh 275.

### Level 0: bits and binary

A computer chip is billions of tiny switches (transistors). Each one is either **off (0)** or **on (1)**. One 0-or-1 is a **bit**; 8 bits make a **byte**. Numbers, letters, photos and sound are all stored as bits.

In binary each place is worth double the one to its right:

| Place value | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|-------------|-----|----|----|----|---|---|---|---|
| `01000001`  | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 1 |

So `01000001` = 64 + 1 = **65**. Text is stored with a code table (ASCII, now Unicode) where 65 means the letter **A**, 66 is B, and so on.

| Binary | Place values used | Decimal |
|--------|-------------------|---------|
| `00000101` | 4 + 1 | 5 |
| `01000001` | 64 + 1 | 65 (the letter A) |
| `01001011` | 64 + 8 + 2 + 1 | 75 (the letter K) |
| `11010010` | 128 + 64 + 16 + 2 | 210 (our first price) |
| `11111111` | 128 + 64 + … + 1 | 255, the biggest number one byte can hold |

You can check all of this in Python (try it in Colab after the tour):

```python
print(bin(65))              # 0b1000001
print(int("01000001", 2))   # 65
print(ord("A"), chr(65))    # 65 A
print(format(275, "b"))     # 100010011  (275 needs 9 bits)
```

### Level 1: machine code (1st generation, 1940s)

These are the real bytes an Intel/AMD (x86-64) processor runs to add our two prices. They are written in **hexadecimal** (base 16), a shorter way to write bytes: two hex digits = 8 bits, `D2` = 210 and `41` = 65.

```
B8 D2 00 00 00     10111000 11010010 00000000 00000000 00000000   put 210 in a register
83 C0 41           10000011 11000000 01000001                     add 65 to it
C3                 11000011                                       return the answer (275)
```

The first programmers entered patterns like these with switches and punched cards. It is fast, but almost impossible to read, and it only works on **one family of chips**: this code will not run on the ARM chip in your phone.

### Level 2: assembly language (2nd generation, 1950s)

Assembly replaces each number pattern with a short word (a **mnemonic**). One line of assembly = one machine instruction. A program called an **assembler** turns it back into the bytes above.

```nasm
; the same program in x86-64 assembly
add_prices:
    mov eax, 210    ; put 210 in register eax (a tiny storage slot inside the CPU)
    add eax, 65     ; add 65 to it
    ret             ; hand back eax (275)
```

Notice there is no "print" here. Showing text on screen in assembly takes many more lines and a call to the operating system. That pain is why higher-level languages were invented. Assembly is still used for device drivers, microcontrollers and code that must be as fast as possible.

### Level 3: systems languages like C (3rd generation, 1970s)

C introduced named **variables** instead of registers, and it works on any chip, as long as you re-translate it for that chip. A **compiler** translates the whole file into machine code before it runs.

```c
#include <stdio.h>

int main(void) {
    int total = 210 + 65;
    printf("Total: KSh %d\n", total);
    return 0;
}
```

```
$ gcc add.c -o add
$ ./add
Total: KSh 275
```

C is "high-level" compared with assembly but "low-level" compared with Python: you must declare types (`int`), end lines with `;`, and manage memory yourself. Linux, Windows, the core of Android, and Python's own interpreter are written in C.

### Level 4: high-level languages like Python

```python
total = 210 + 65
print("Total: KSh", total)
```

```
Total: KSh 275
```

Two lines. No `main`, no types to declare, no semicolons. You think about the **problem**, not the chip. Underneath, the Python interpreter (itself written in C) still turns this into machine code for the CPU.

**Python** is a *high-level* language: it reads almost like English and hides the hard details. That's why it is the most popular first language, and why it's used everywhere from schools to NASA.

### Level 5: natural language and AI

The newest "level" is plain English (or Kiswahili): you describe what you want, and an AI assistant writes the code. But the AI produces code at one of the levels above, usually Python, and **you** are still responsible for reading and checking it. That's what this course prepares you to do.

### The same task at four levels

| Level | Lines | Readable? | Runs on |
|-------|-------|-----------|---------|
| Machine code | 3 instructions (9 bytes) | no | one chip family only |
| Assembly | 3 + a label | barely | one chip family only |
| C | 7 | with practice | any chip, after re-compiling |
| Python | **2** | **yes** | anywhere Python is installed |

Lower levels give more control and speed, but take more work and leave more room for mistakes. Higher levels need less code and are easier to read and share. For data and AI work, Python's readability wins, and the heavy maths inside libraries like pandas and NumPy is already written in fast C.

### Try it: decode the binary message

Use the place values 128 64 32 16 8 4 2 1. Each byte is one capital letter (A = 65, B = 66 … Z = 90).

1. Decode `01001000 01001001`.
2. Write the letters **K E** in binary.

<details>
<summary>Answers</summary>

1. `01001000` = 64 + 8 = 72 = **H**; `01001001` = 64 + 8 + 1 = 73 = **I**. The message is **HI**.
2. K = 75 = `01001011`, E = 69 = `01000101`.

Check in Python: `chr(int("01001000", 2))` gives `'H'`.
</details>

### Interpreter vs. compiler (just the idea)

- Python is **interpreted**: the interpreter reads your code and runs it line by line. If line 5 has a mistake, lines 1–4 still run first.
- Languages like C are **compiled**: the whole program is translated into machine code before it runs.

You don't need to remember this. Just know that when you press ▶ in Colab, the Python interpreter reads your cell from top to bottom.

## Key vocabulary

| Word | Meaning |
|------|---------|
| **Program / code** | Instructions written for a computer |
| **Programming language** | A language with strict rules for writing those instructions (Python, JavaScript, SQL…) |
| **Bit / byte** | One 0-or-1 / a group of 8 bits |
| **Machine code** | The binary instructions a CPU actually runs |
| **Assembly** | Machine instructions written as short words (`mov`, `add`); turned into machine code by an **assembler** |
| **High-level language** | A language close to human language (Python); turned into machine code by a **compiler** or **interpreter** |
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
