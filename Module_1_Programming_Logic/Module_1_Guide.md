# MODULE 1 — Programming Logic (Days 6-12)

**Goal:** Learn the atoms that ALL programs are built from — variables, types, operators, conditionals, and loops. You'll write every exercise yourself and trace it by hand. No AI. In **Python**.

**How to work:** For every exercise, follow the framework in `CHEATSHEET.md`: UNDERSTAND → PLAN (plain words) → CODE → TEST → DEBUG. Always trace at least one solution on paper.

**Resource:** Python tutorial (official): https://docs.python.org/3/tutorial/

> Python tip: indentation matters. Code inside an `if`/`for`/`def` is indented 4 spaces. Lines that start a block end with a colon `:`.

---

## Day 6 — Variables & Values
### LEARN
A **variable** is a labeled box that holds a value. In Python you just write `name = value` — there's no `let`/`const`. To signal "this shouldn't change," use an UPPER_CASE name by convention. Naming clearly (`total_price`, not `x`) is a real skill (Python style uses `snake_case`).
```python
age = 25
city = "Dhaka"
```
### DO (in Exercises/, as .py files)
- Store your name, age, and city in variables and print a sentence using them (try an f-string: `print(f"I am {name}")`).
- Swap the values of two variables (in Python you can do `a, b = b, a` — but first try it WITH a third variable to understand it).
- Predict each line's output ON PAPER before running.
### TRANSITION CONDITION
From a blank file: create variables, change one, and print a sentence built from them — no notes.

---

## Day 7 — Data Types
### LEARN
Core types: **int** (whole numbers), **float** (decimals), **str** (text), **bool** (`True`/`False`), and **None**. Strings join with `+` (both must be strings). `type(x)` tells you a value's type. Convert with `int()`, `str()`, `float()`.
### DO
- Make one variable of each type; print its value and `type()`.
- Predict the output of `"5" + "2"`, `5 + 2`, `int("5") + 2` BEFORE running, then check.
- Try `"5" + 2` — read the error you get and write down what it means.
### TRANSITION CONDITION
You can name the main data types and predict what `type()` returns for a value, from memory.

---

## Day 8 — Operators
### LEARN
Math: `+ - * / // % **` (`//` integer divide, `%` remainder — hugely useful, `**` power). Comparison: `== != > < >= <=`. Logical: `and`, `or`, `not`.
### DO
- Write expressions to check: is a number even? (hint: `% 2`). Is someone a teenager (13-19)?
- Predict results of `7 % 3`, `10 // 4`, `(5 > 3) and (2 > 4)` on paper, then run.
### TRANSITION CONDITION
You can use `%` to test even/odd and combine conditions with `and`/`or`, from memory.

---

## Day 9 — Conditionals (if / elif / else)
### LEARN
```python
if condition:
    ...
elif other_condition:
    ...
else:
    ...
```
Code that makes decisions. Watch the colons and indentation.
### DO
- Write a program: given an age, print "child", "teenager", or "adult".
- Write a grade program: a score → "A/B/C/D/F".
- Trace your grade program by hand with 3 different scores.
### TRANSITION CONDITION
From a blank file, write a multi-branch if/elif/else that picks the right output for different inputs — no notes.

---

## Day 10 — Loops (for)
### LEARN
A **loop** repeats code. `for i in range(n):` runs `n` times (i goes 0 to n-1). You can also loop directly over a list or string. Loops are where beginners' brains stretch — trace them on paper.
```python
for i in range(5):     # 0 1 2 3 4
    print(i)
```
### DO
- Print numbers 1 to 20 (hint: `range(1, 21)`).
- Print only even numbers 1 to 20 (combine with `%`).
- Add up all numbers from 1 to 100 (keep a running total variable).
- Trace a small loop (1 to 5) line-by-line on paper, writing `i` and the total each round.
### TRANSITION CONDITION
From memory, write a `for` loop that sums numbers 1 to N, and explain what `range()` does.

---

## Day 11 — Loops (while) & Nested Logic
### LEARN
`while condition:` repeats until the condition is false — use when you don't know the count in advance. Be careful of infinite loops (always change something inside!). You can put `if` inside loops, and loops inside loops.
### DO
- Use a `while` loop to count down from 10 to 1.
- FizzBuzz (the classic): print 1-30, but "Fizz" for multiples of 3, "Buzz" for multiples of 5, "FizzBuzz" for both. (Do NOT look up the answer — build it with `%` and `if`.)
### TRANSITION CONDITION
You can solve FizzBuzz from a blank file with no help. (This is a real beginner-interview filter — owning it matters.)

---

## Day 12 — Module 1 Challenge Day
### LEARN
Time to combine everything: variables + types + operators + conditionals + loops.
### DO (no AI, use the framework)
- Print the multiplication table for a number (e.g. 7 × 1 to 7 × 10).
- Given a number, decide if it's prime (only divisible by 1 and itself). Plan on paper first!
- Count how many vowels are in a word (loop through the letters: `for letter in word:`).
### TRANSITION CONDITION
**Big one:** solve the "count the vowels" and "is it prime?" problems from blank files, using the UNDERSTAND→PLAN→CODE→TEST framework, no AI.

---

## Module 1 Complete When...
- [ ] Variables, types, operators are second nature
- [ ] You can write if/elif/else confidently
- [ ] You can write for and while loops and trace them by hand
- [ ] You solved FizzBuzz and the challenge problems yourself
- [ ] **All Transition Conditions passed → start Module 2**
