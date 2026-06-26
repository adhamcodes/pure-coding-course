# MODULE 2 — Functions & Decomposition (Days 13-17)

**Goal:** Learn to break big problems into small, named, reusable pieces (functions). Decomposition is THE core skill of a developer — it's how you turn "I have no idea where to start" into "I have ten tiny steps I can do."

**Resource:** MDN Functions: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions

---

## Day 13 — What Is a Function?
### LEARN
A **function** is a named recipe: it takes **inputs** (parameters), does work, and gives back an **output** (`return`). Functions let you reuse logic and name your steps. `return` sends a value back; without it you get `undefined`.
```js
function double(n) {
  return n * 2;
}
double(5); // 10
```
### DO
- Write `double`, `square`, and `greet(name)`.
- Write `isEven(n)` that returns true/false.
- Note the difference between `console.log` (shows something) and `return` (hands a value back) — test both.
### TRANSITION CONDITION
From memory: write a function with a parameter that returns a computed value, and call it.

---

## Day 14 — Parameters, Arguments & Return
### LEARN
**Parameters** are the named inputs in the definition; **arguments** are the actual values you pass. Functions can take several parameters. A function should ideally do ONE clear thing.
### DO
- `add(a, b)`, `max(a, b)` (return the bigger), `clamp(n, low, high)`.
- `rectangleArea(width, height)`.
- For each, write the example (input → output) BEFORE coding.
### TRANSITION CONDITION
You can write a multi-parameter function that returns the correct result and explain parameters vs arguments.

---

## Day 15 — Decomposition: Breaking Problems Down
### LEARN
Big problems feel impossible because you try to solve them all at once. **Decomposition** = splitting one big problem into small functions you CAN solve. Example: "validate a password" → `isLongEnough()`, `hasNumber()`, `hasUppercase()`, then combine.
### DO
- Build a password checker by writing 3 small helper functions, then one `isValidPassword()` that uses them.
- On paper FIRST: list the small pieces before writing any code.
### TRANSITION CONDITION
Given a medium problem, you can break it into 2-4 smaller functions on paper before coding.

---

## Day 16 — Functions Calling Functions
### LEARN
Real programs are small functions calling each other. This keeps each piece simple and testable. Build bottom-up: make and test the small pieces, then combine.
### DO
- Write `isVowel(letter)`, then use it inside `countVowels(word)`.
- Write `celsiusToFahrenheit(c)` and a function that prints a small conversion table using it.
### TRANSITION CONDITION
You can write a function that uses your OWN smaller function inside it, from memory.

---

## Day 17 — Module 2 Challenge Day
### DO (no AI, decompose first on paper)
- **Temperature reporter:** a function that takes a Celsius value and returns a sentence like "25°C is warm" using helper functions for conversion and for the description.
- **Initials maker:** `getInitials("Adham Codes Here")` → `"ACH"` (decompose: split the idea into steps).
- Trace one solution by hand.
### TRANSITION CONDITION
**Big one:** solve `getInitials` from a blank file by decomposing it into clear steps first, no AI.

---

## Module 2 Complete When...
- [ ] You understand parameters, arguments, and return
- [ ] You can decompose a problem into small functions ON PAPER first
- [ ] You can compose functions (one calling another)
- [ ] You solved the challenge problems yourself
- [ ] **All Transition Conditions passed → start Module 3**
