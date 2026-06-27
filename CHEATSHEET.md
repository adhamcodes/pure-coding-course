# Cheatsheet — Problem-Solving Framework + Python Basics

> Two things here: (1) the THINKING framework that matters more than any syntax, and (2) the Python basics you'll use. When stuck, come here — NOT to AI.

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
- Add `print()` to see what your variables actually are.
- After it works: ask "could this be simpler/clearer?" Then write what you learned.

> **The golden habit:** trace your code BY HAND on paper. Pretend you're the computer. Walk through each line with a real value. This builds the mental model AI can never give you.

---

## 🐍 PART 2: Python Basics

> Python uses **indentation** (spaces) to group code — no curly braces. Be consistent (4 spaces).

### Print to the screen
```python
print("Hello")        # shows text in the console
```

### Variables (no let/const — just a name = a value)
```python
age = 25
name = "Adham"
PI = 3.14159           # convention: UPPER_CASE means "treat as constant"
```

### Data types
```python
num = 42               # int (whole number)
price = 9.99           # float (decimal)
text = "hello"         # str (string)
yes = True             # bool (True / False)
nothing = None         # the "empty" value
type(num)              # <class 'int'>
```

### Operators
```python
+  -  *  /  //  %  **   # //=integer divide, %=remainder, **=power
==  !=                  # equal / not equal
>  <  >=  <=            # comparison
and   or   not          # logical (not &&, ||, !)
```

### Conditionals (note the colon and indentation)
```python
if age >= 18:
    print("adult")
elif age >= 13:
    print("teenager")
else:
    print("child")
```

### Loops
```python
for i in range(5):       # 0 1 2 3 4
    print(i)

for item in [10, 20, 30]:  # loop over a list directly
    print(item)

count = 5
while count > 0:
    print(count)
    count = count - 1
```

### Functions
```python
def add(a, b):
    return a + b

add(2, 3)   # 5

greet = lambda name: "Hi " + name   # small inline function
```

### Lists (ordered collections — like arrays)
```python
nums = [10, 20, 30]
nums[0]            # 10 (first item)
len(nums)          # 3
nums.append(40)    # add to end
for n in nums:
    print(n)
```

### Dictionaries (labeled data — key/value pairs)
```python
person = {"name": "Adham", "age": 25}
person["name"]        # "Adham"
person["age"] = 26    # change a value
```

### Strings
```python
s = "hello"
len(s)            # 5
s.upper()         # "HELLO"
"ell" in s        # True
s[0]              # "h"
list(s)           # ['h','e','l','l','o']
```

### Getting input (for interactive programs)
```python
name = input("What's your name? ")   # reads text the user types
number = int(input("Pick a number: "))  # convert text to a number
```

---

## 🔎 How to read an error
1. Read the **last line** first — it names the error type (e.g. `NameError`, `TypeError`, `IndentationError`).
2. Python shows the **line number** — go there.
3. Read the message literally (`name 'x' is not defined` → you used `x` before creating it).
4. Add `print()` before the error line to see your values.

---

## The rule
When stuck: **Framework first. Docs second. AI never** (in this course).
Docs: https://docs.python.org/3/
