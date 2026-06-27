# MODULE 3 — Data Structures & Algorithms (Days 18-24)

**Goal:** Learn the containers that hold data (lists, strings, dictionaries) and the classic ways to process them (searching, sorting), plus a gentle intro to thinking about efficiency (Big-O). This is where your problem-solving really sharpens. In **Python**.

**Resource:** Python data structures (tutorial): https://docs.python.org/3/tutorial/datastructures.html

---

## Day 18 — Lists
### LEARN
A **list** is an ordered collection: `nums = [10, 20, 30]`. Access by **index** (starts at 0): `nums[0]`. `len(nums)` is the count. `nums.append(x)` adds to the end, `nums.pop()` removes the last.
### DO
- Make a list of 5 numbers. Print each with a loop. Print the sum, the max, and the average — by looping yourself (don't use built-in `sum()`/`max()` yet; build the logic).
- Trace your "find the max" logic on paper.
### TRANSITION CONDITION
From memory: loop through a list and compute its sum and maximum with your own loop.

---

## Day 19 — List Operations By Hand
### LEARN
Build the logic yourself before learning shortcuts. Looping + an `if` + an accumulator solves most list problems.
### DO
- Count how many numbers in a list are even.
- Build a NEW list containing only the even numbers (start with `[]`, `append` matches).
- Reverse a list into a new list (loop from the end, or build up front-to-back — figure it out).
### TRANSITION CONDITION
You can filter a list (keep only items matching a condition) into a new list, from memory, with a manual loop.

---

## Day 20 — Strings In Depth
### LEARN
Strings are sequences of characters. `len(s)`, `s[i]`, `s.upper()`, `s.lower()`, `"x" in s`, `s.split()` (into a list of words), `list(s)` (into letters). You can loop over a string: `for ch in s:`.
### DO
- Count the vowels in a sentence.
- Check if a word is a **palindrome** (same forwards and backwards) — plan on paper first. (Hint: `s[::-1]` reverses a string — but try building it with a loop first to understand it.)
- Count how many times one specific letter appears.
### TRANSITION CONDITION
You can check whether a word is a palindrome from a blank file, no help.

---

## Day 21 — Dictionaries (Labeled Data)
### LEARN
A **dictionary** stores key/value pairs: `user = {"name": "Adham", "age": 25}`. Access with `user["name"]`. Great for representing a "thing" with properties, or for counting. A list of dictionaries models lists of things (e.g. a list of students).
### DO
- Make a dictionary for a book (title, author, pages). Print a sentence about it.
- Make a list of 3 student dictionaries (name, score). Loop to print each, and find the highest scorer.
### TRANSITION CONDITION
From memory: create a list of dictionaries and loop through it to find one matching a condition (e.g. highest score).

---

## Day 22 — Searching
### LEARN
**Linear search:** check each item one by one until you find the target. Simple and always works. (You'll meet faster searches later; understand this one deeply first.)
### DO
- Write `find_index(items, target)` that returns the position of a value, or -1 if missing — using a loop, no built-ins.
- Search a list of student dictionaries for one by name.
### TRANSITION CONDITION
You can write a linear search from scratch that returns the index or -1.

---

## Day 23 — Sorting & Big-O Intuition (Gentle)
### LEARN
**Sorting** = arranging items in order. You'll implement a simple one (bubble sort) to FEEL how sorting works, even though real code uses Python's built-in `sorted()`.
**Big-O (intuition only):** a way to describe how slow an algorithm gets as input grows. Looping once over N items = "O(n)". A loop inside a loop over N items = "O(n²)" (much slower for big N). You don't need math — just the intuition: *nested loops over big data = slow.*
### DO
- Implement **bubble sort** on a small list (repeatedly swap neighbors that are out of order). Plan on paper; it's tricky — that's good.
- Identify: is your bubble sort one loop or a loop-in-a-loop? What does that say about its speed?
### TRANSITION CONDITION
You can explain in plain words why a loop-inside-a-loop is slower than a single loop, and you implemented a basic sort yourself.

---

## Day 24 — Module 3 Challenge Day
### DO (no AI, framework + paper first)
- **Word frequency:** given a sentence, build a dictionary counting how many times each word appears.
- **Second largest:** find the second-largest number in a list (no sorting shortcut — reason it out).
- Trace one solution by hand.
### TRANSITION CONDITION
**Big one:** solve "second largest number in a list" from a blank file, no AI, explaining your plan first.

---

## Module 3 Complete When...
- [ ] You're comfortable with lists, strings, and dictionaries
- [ ] You can search and filter data with your own loops
- [ ] You implemented a sort and understand Big-O intuition
- [ ] You solved the challenge problems yourself
- [ ] **All Transition Conditions passed → start Module 4**
