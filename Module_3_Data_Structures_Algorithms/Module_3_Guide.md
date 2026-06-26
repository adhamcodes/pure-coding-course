# MODULE 3 — Data Structures & Algorithms (Days 18-24)

**Goal:** Learn the containers that hold data (arrays, strings, objects) and the classic ways to process them (searching, sorting), plus a gentle intro to thinking about efficiency (Big-O). This is where your problem-solving really sharpens.

**Resource:** MDN Arrays: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array

---

## Day 18 — Arrays (Lists)
### LEARN
An **array** is an ordered list: `let nums = [10, 20, 30]`. Access by **index** (starts at 0): `nums[0]`. `nums.length` is the count. `push` adds to the end, `pop` removes the end.
### DO
- Make an array of 5 numbers. Print each with a loop. Print the sum, the max, and the average — by looping yourself (don't search for a shortcut).
- Trace your "find the max" logic on paper.
### TRANSITION CONDITION
From memory: loop through an array and compute its sum and maximum.

---

## Day 19 — Array Operations By Hand
### LEARN
Build the logic yourself before learning built-in shortcuts. Looping + an `if` + an accumulator solves most array problems.
### DO
- Count how many numbers in an array are even.
- Build a NEW array containing only the even numbers (make an empty array, push matches).
- Reverse an array into a new array (loop from the end).
### TRANSITION CONDITION
You can filter an array (keep only items matching a condition) into a new array, from memory, with a manual loop.

---

## Day 20 — Strings In Depth
### LEARN
Strings are sequences of characters. `s.length`, `s[i]`, `s.toUpperCase()`, `s.includes()`, `s.split("")` (into an array of letters). You can loop over a string like an array.
### DO
- Count the vowels in a sentence.
- Check if a word is a **palindrome** (same forwards and backwards) — plan on paper first.
- Count how many times each... no — just count occurrences of one letter for now.
### TRANSITION CONDITION
You can check whether a word is a palindrome from a blank file, no help.

---

## Day 21 — Objects (Labeled Data)
### LEARN
An **object** stores labeled values: `let user = { name: "Adham", age: 25 }`. Access with `user.name`. Great for representing a "thing" with properties. Arrays of objects model lists of things (e.g. a list of students).
### DO
- Make an object for a book (title, author, pages). Print a sentence about it.
- Make an array of 3 student objects (name, score). Loop to print each, and find the highest scorer.
### TRANSITION CONDITION
From memory: create an array of objects and loop through it to find one matching a condition (e.g. highest score).

---

## Day 22 — Searching
### LEARN
**Linear search:** check each item one by one until you find the target. Simple and always works. (You'll meet faster searches later; understand this one deeply first.)
### DO
- Write `findIndex(array, target)` that returns the position of a value, or -1 if missing — using a loop, no built-ins.
- Search an array of student objects for one by name.
### TRANSITION CONDITION
You can write a linear search from scratch that returns the index or -1.

---

## Day 23 — Sorting & Big-O Intuition (Gentle)
### LEARN
**Sorting** = arranging items in order. You'll implement a simple one (bubble sort) to FEEL how sorting works, even though real code uses built-ins.
**Big-O (intuition only):** a way to describe how slow an algorithm gets as input grows. Looping once over N items = "O(n)". A loop inside a loop over N items = "O(n²)" (much slower for big N). You don't need math — just the intuition: *nested loops over big data = slow.*
### DO
- Implement **bubble sort** on a small array (repeatedly swap neighbors that are out of order). Plan on paper; it's tricky — that's good.
- Identify: is your bubble sort one loop or a loop-in-a-loop? What does that say about its speed?
### TRANSITION CONDITION
You can explain in plain words why a loop-inside-a-loop is slower than a single loop, and you implemented a basic sort yourself.

---

## Day 24 — Module 3 Challenge Day
### DO (no AI, framework + paper first)
- **Word frequency:** given a sentence, build an object counting how many times each word appears.
- **Second largest:** find the second-largest number in an array (no sorting shortcut — reason it out).
- Trace one solution by hand.
### TRANSITION CONDITION
**Big one:** solve "second largest number in an array" from a blank file, no AI, explaining your plan first.

---

## Module 3 Complete When...
- [ ] You're comfortable with arrays, strings, and objects
- [ ] You can search and filter data with your own loops
- [ ] You implemented a sort and understand Big-O intuition
- [ ] You solved the challenge problems yourself
- [ ] **All Transition Conditions passed → start Module 4**
