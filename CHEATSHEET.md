# Cheatsheet — Problem-Solving Framework + JavaScript Basics

> Two things here: (1) the THINKING framework that matters more than any syntax, and (2) the JavaScript basics you'll use. When stuck, come here — NOT to AI.

---

## 🧠 PART 1: The Problem-Solving Framework (the real skill)

Memorize these 5 steps. Use them on EVERY problem. This is what separates a coder from a copy-paster.

### 1. UNDERSTAND
- Read the problem twice. Say it back in your own words.
- What are the **inputs**? What is the expected **output**?
- Write one example by hand: input → output.

### 2. PLAN (no code yet!)
- Write the steps in plain language (pseudocode). Example:
  ```
  - make an empty list for results
  - go through each number in the input
  - if the number is even, add it to results
  - return results
  ```
- This is 80% of the work. If your plan is right, code is just translation.

### 3. CODE
- Translate each plan step into code, one line at a time.
- Run it often. Don't write 30 lines then run.

### 4. TEST
- Try your example. Try edge cases: empty input, one item, big input, zero, negative.
- Does it still work? If not, good — now you debug.

### 5. DEBUG & REFLECT
- Read the error message slowly (it usually tells you the line + problem).
- Add `console.log()` to see what your variables actually are.
- After it works: ask "could this be simpler/clearer?" Then write what you learned.

> **The golden habit:** trace your code BY HAND on paper. Pretend you're the computer. Walk through each line with a real value. This builds the mental model AI can never give you.

---

## ⚙️ PART 2: JavaScript Basics

### Print to the screen
```js
console.log("Hello");   // shows text in the console
```

### Variables
```js
let age = 25;        // can change later
const name = "Adham"; // cannot change
```

### Data types
```js
let num = 42;            // number
let text = "hello";      // string
let yes = true;          // boolean (true/false)
let nothing = null;      // intentionally empty
let notSet;              // undefined
```

### Operators
```js
+  -  *  /  %        // math (% is remainder)
=== !==              // equal / not equal (use these)
>  <  >=  <=         // comparison
&&  ||  !            // and / or / not
```

### Conditionals
```js
if (age >= 18) {
  console.log("adult");
} else {
  console.log("minor");
}
```

### Loops
```js
for (let i = 0; i < 5; i++) {
  console.log(i);        // 0 1 2 3 4
}

while (count > 0) {
  count = count - 1;
}
```

### Functions
```js
function add(a, b) {
  return a + b;
}
add(2, 3); // 5

const greet = (name) => "Hi " + name;  // arrow function
```

### Arrays (lists)
```js
let nums = [10, 20, 30];
nums[0];          // 10 (first item)
nums.length;      // 3
nums.push(40);    // add to end
for (let n of nums) { console.log(n); }
```

### Objects (labeled data)
```js
let person = { name: "Adham", age: 25 };
person.name;          // "Adham"
person.age = 26;      // change a value
```

### Strings
```js
let s = "hello";
s.length;             // 5
s.toUpperCase();      // "HELLO"
s.includes("ell");    // true
s[0];                 // "h"
```

---

## 🔎 How to read an error
1. Look at the **error type** (e.g. `ReferenceError`, `TypeError`).
2. Look at the **line number** — go there.
3. Read the message literally (`x is not defined` → you used `x` before creating it).
4. Add `console.log()` before the error line to see your values.

---

## The rule
When stuck: **Framework first. Docs second. AI never** (in this course).
Docs: https://developer.mozilla.org/en-US/docs/Web/JavaScript
