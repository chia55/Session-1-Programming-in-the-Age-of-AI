# Hands-on 1 · Write step-by-step "recipes" (algorithms)

**Time:** 20 minutes · **Work:** in pairs · **No computer needed**

Your goal is to write instructions so precise that a robot with **no common sense** could follow them. Then swap with another pair and "run" each other's algorithm *exactly* as written, no guessing allowed!

## Rules for a good recipe

- Number every step.
- One action per step.
- Be exact: amounts, times, which button.
- Use **IF … OTHERWISE …** for decisions.
- Use **REPEAT … UNTIL …** or **FOR EACH …** for repetition, and make sure it ends.
- State the **input** (what you need) and **output** (what you end up with).

---

## Task A · Warm-up (everyone)

**Brush your teeth.** Write at least 8 steps.

*Think about:* What if the toothpaste tube is empty? How long do you brush? How does it end?

## Task B · Choose two

1. **Send KSh 500 to a friend using M-Pesa** (via the SIM menu or the app).
   *Edge cases:* wrong PIN, not enough balance, wrong number.
2. **Make chai for a group of N people.**
   *Edge cases:* some take sugar, some don't; the sufuria only holds 1 litre.
3. **Find a word in a printed dictionary.**
   *Hint:* do you start at page 1? (This is a famous algorithm called *binary search*.)
4. **Decide what to wear today.**
   *Inputs:* weather, the day of the week, what's clean.
5. **Calculate a student's grade from their mark.**
   Use: 70–100 → A, 60–69 → B, 50–59 → C, 40–49 → D, below 40 → E.
   *Edge cases:* mark of exactly 70? A mark of 105? A negative mark?
   *(You'll code this for real in Session 2.)*

## Task C · Swap and test

1. Give your recipe to another pair.
2. They follow it **literally**, acting it out or talking it through.
3. Each time they find a vague, missing or wrong step, they mark it with ⚠️.
4. Get your recipe back and fix every ⚠️.

## Task D · Turn one recipe into pseudocode

Pick your grading recipe (or any one with decisions) and rewrite it in pseudocode:

```
INPUT mark
IF mark >= 70 THEN
    OUTPUT "A"
ELSE IF ...
```

## Reflection (write 2–3 sentences)

- What was the hardest part of being precise?
- Which edge case surprised you?
- How is this similar to giving instructions to an AI assistant?

---

### Facilitator example: M-Pesa send money (via SIM menu)

> **Input:** recipient phone number, amount, your PIN. **Output:** money sent, or an error message.
>
> 1. Open the SIM Toolkit / M-PESA menu on your phone.
> 2. Select **Send Money**.
> 3. Enter the recipient's phone number. Select OK.
> 4. Enter the amount (e.g. 500). Select OK.
> 5. Enter your M-Pesa PIN. Select OK.
> 6. Check the confirmation screen: name, number, amount.
> 7. IF the details are correct, select OK. OTHERWISE, cancel and go back to step 3.
> 8. Wait for the SMS.
> 9. IF the SMS says "Confirmed", stop: success.
> 10. OTHERWISE IF it says "insufficient funds", top up your account, then repeat from step 1.
> 11. OTHERWISE IF it says "wrong PIN", repeat from step 5 (but after 3 wrong attempts your account will be locked, so stop and contact Safaricom).
