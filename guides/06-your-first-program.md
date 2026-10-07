# Guide 06 · Your first Python program

Open Colab (or VS Code) and follow along. Type every example yourself.

## 1. `print()`: making the computer say something

```python
print("Hello, World!")
```

Output:

```
Hello, World!
```

Let's take this line apart:

| Piece | Name | Meaning |
|-------|------|---------|
| `print` | a **function** | a named, ready-made action that Python already knows |
| `( )` | parentheses | "here is what I'm giving the function" |
| `"Hello, World!"` | a **string** | a piece of text. The quotes mark where the text starts and ends |

> A **function** is like a machine: you put something in (the *argument*), it does its job. `print` puts its argument on the screen.

## 2. Strings: text in quotes

Single or double quotes both work. Just be consistent within one string:

```python
print("Karibu!")
print('Karibu!')
print("It's a lovely day in Nakuru")   # double quotes let you use ' inside
```

## 3. Printing several things

Separate them with commas. `print` puts a space between them automatically:

```python
print("My name is", "Achieng")
print("I am", 21, "years old")
```

Output:

```
My name is Achieng
I am 21 years old
```

Notice `21` has **no quotes**. It's a number, not text. You'll learn more about the difference in Session 2.

## 4. Numbers and simple maths

Python is a very good calculator:

```python
print(250 + 180)        # addition       → 430
print(1000 - 345)       # subtraction    → 655
print(65 * 3)           # multiplication → 195
print(1000 / 4)         # division       → 250.0
print("Total:", 210 * 2 + 65)   # → Total: 485
```

## 5. Comments: notes for humans

Anything after a `#` on a line is ignored by Python. Use comments to explain *why* you did something.

```python
# This program introduces me to the class
print("Habari! I'm Kevin.")   # greeting in Kiswahili
```

## 6. Empty lines and special characters

```python
print()                          # prints an empty line
print("Line one\nLine two")      # \n means "new line"
print("Name:\tAmina")            # \t means "tab"
```

## 7. Multi-line text

Triple quotes let a string span several lines:

```python
print("""
*************************
*   WELCOME TO PYTHON   *
*************************
""")
```

## 8. Your first errors (and how to read them)

Errors are normal. Every programmer sees hundreds every week. Python's error messages tell you **what** went wrong and **where**.

### Missing quote

```python
print("Hello)
```

```
  File "<ipython-input-1>", line 1
    print("Hello)
          ^
SyntaxError: unterminated string literal (detected at line 1)
```

How to read it:

1. **Look at the last line first**: `SyntaxError: unterminated string literal`. A string was started but never ended.
2. **Look at the line number and the arrow `^`**: it points to where Python got confused.
3. **Fix:** add the closing quote: `print("Hello")`.

### Misspelt function

```python
pritn("Hello")
```

```
NameError: name 'pritn' is not defined
```

Python doesn't know any function called `pritn`. Fix the spelling.

### Capital letters matter

```python
Print("Hello")
```

```
NameError: name 'Print' is not defined. Did you mean: 'print'?
```

Python is **case-sensitive**: `print` and `Print` are different names. Newer Python versions even suggest the fix.

### Missing bracket

```python
print("Hello"
```

```
SyntaxError: '(' was never closed
```

### The error-reading routine

1. Read the **last line** (the error type and message).
2. Find the **line number** / arrow.
3. Compare that line carefully with a working example.
4. Still stuck? Ask AI: *"Explain this error for a beginner, don't just fix it."*

## 9. Putting it together: a personal introduction

```python
# My personal introduction
print("==============================")
print("   HELLO, I'M WANJIRU 👋")
print("==============================")
print("I live in Nakuru.")
print("I'm studying Business IT, year", 2)
print("Fun fact: I can name all 47 counties!")
print()
print("In this course I want to learn", "data analysis.")
print("Days until my birthday:", 365 - 200)
```

That's exactly what you'll build in the hands-on exercise. Open [../notebooks/02-exercises.ipynb](../notebooks/02-exercises.ipynb).

## Summary

- `print()` shows things on screen.
- Text goes inside quotes ("strings"); numbers don't.
- `#` starts a comment.
- Python is case-sensitive and very strict about brackets and quotes.
- Errors are messages to help you: read the last line first.
