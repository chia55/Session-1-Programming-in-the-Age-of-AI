# Session 1 Cheat Sheet: Programming in the Age of AI

## Big ideas
- **Program** = precise instructions a computer follows: **input → process → output**.
- Computers are **fast** but **literal**: no common sense, so be exact.
- **Algorithm** = finite, ordered, unambiguous steps that solve a problem.
- Three building blocks: **sequence** (in order), **selection** (if/otherwise), **iteration** (repeat).
- With AI: you must **Understand · Check · Direct** the code it writes.

## Computational thinking
| Habit | One-liner |
|-------|-----------|
| Decomposition | Break it into smaller problems |
| Pattern recognition | Spot what you've solved before |
| Abstraction | Keep what matters, drop the rest |
| Algorithm design | Write the steps, then test them by hand |

## Python so far
```python
print("Hello, Kenya!")              # show text
print("Age:", 21)                   # text + number, separated by a space
print(2 * 210 + 65)                 # maths: + - * / ** (power)
print("Line 1\nLine 2")             # \n new line, \t tab
# a comment: ignored by Python
print("""multi
line text""")
```

## Colab shortcuts
| Keys | Action |
|------|--------|
| Shift + Enter | Run cell, move on |
| Ctrl + Enter | Run cell, stay |
| Ctrl + M, B | New code cell below |
| Ctrl + M, M | Make text cell |
| Ctrl + / | Comment / uncomment |
| File → Save a copy in Drive | **Do this first with any shared notebook** |

## Reading errors
1. Read the **last line** (error type + message).
2. Go to the **line number / arrow**.
3. Compare with a working example.
4. Ask AI to **explain**, not just fix.

| Error | Usually means |
|-------|---------------|
| `SyntaxError: unterminated string literal` | A quote is missing |
| `SyntaxError: '(' was never closed` | A bracket is missing |
| `NameError: name 'pritn' is not defined` | Typo, or wrong capital letters |

## Good AI prompts for learners
- "Explain this code line by line for a beginner."
- "Explain this error, don't fix it yet."
- "Give me a hint, not the full answer."
- "What edge cases might my solution miss?"
