# MODULE 0 — Foundations: How It All Actually Works (Days 1-5)

**Goal:** Before you write much code, understand the machine you're talking to. Most beginners skip this and stay confused for years. You won't. By the end of this module you'll know what happens inside a computer when code runs, how text becomes numbers, the difference between the tools you'll use, what an "environment" is, how to use the terminal, what the internet and web really are, and you'll have Python running on your machine.

> Read actively. After each concept, close the guide and explain it out loud in your own words. If you can't, read it again.

**Free resources (no AI):**
- Crash Course Computer Science (YouTube series): https://www.youtube.com/playlist?list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo
- MDN — "How the web works": https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works
- How DNS works (illustrated): https://howdns.works/
- Python docs: https://docs.python.org/3/

---

## Day 1 — What Happens Inside a Computer When You Write Code

### LEARN
- A computer only truly understands **binary** — 1s and 0s (electricity on/off). These are called **bits**. 8 bits = 1 **byte**.
- The **CPU** is the brain: it executes simple instructions incredibly fast. The **RAM (memory)** is the short-term workspace where data lives while a program runs. **Storage (disk)** is long-term memory that survives shutdown.
- You write **source code** (human-readable text like Python). The computer can't run that directly — it must be turned into instructions the CPU understands. Something has to translate it (you'll learn what on Day 2).
- The flow: **you type code → it's translated → CPU runs the instructions using RAM → output appears.**

### Encoding & Decoding (you asked for this — here it is)
- Computers store **everything** as numbers (which are stored as binary). So how does it store the letter "A"? With a code.
- **Encoding** = turning something (a letter, an emoji, a color) INTO numbers using an agreed system. **Decoding** = turning those numbers back into the thing.
- **ASCII** is an old encoding: "A" = 65, "B" = 66, "a" = 97. **Unicode / UTF-8** is the modern one that covers every language and emoji.
- Example: the text "Hi" is encoded as the numbers 72, 105 → stored as binary → when shown on screen, it's *decoded* back into "Hi".
- This is why a file can look like garbage if opened with the "wrong" decoding — same numbers, wrong translation table.

### DO (in an online Python runner — https://www.python.org/shell/)
```python
ord("A")          # 65  (encoding a letter to its number)
chr(66)           # 'B' (decoding a number back to a letter)
print(ord("H"), ord("i"))   # 72 105
```
Then on paper: write your name and figure out each letter's relationship to numbers. Explain "encoding vs decoding" out loud.

### TRANSITION CONDITION
You can explain, in your own words: bit/byte, what the CPU and RAM do, the difference between source code and machine instructions, and what encoding vs decoding means — with no notes.

---

## Day 2 — Compiler vs Interpreter vs IDE vs Environment

### LEARN
These words confuse every beginner. Here they are, clearly:

- **Programming language** — the set of words/rules you write code in (Python, JavaScript, C++). Made for humans to read.
- **Compiler** — a translator that converts your *entire* source code into machine code *once, ahead of time*, producing a file the computer can run. (Languages like C++ work this way.) Think: translate the whole book, then hand it over.
- **Interpreter** — a translator that reads and runs your code *line by line, as it goes*. Think: a live translator speaking as the person talks.
  - **Python is an interpreted language** — the Python interpreter reads your `.py` file and runs it line by line.
- **Text editor** — a simple program to write code (like Notepad, but for code).
- **IDE (Integrated Development Environment)** — a *supercharged* editor that bundles many tools together: code editor + ways to run code + debugger + error highlighting + extensions. (VS Code is the popular one.) "Integrated" = many tools in one place.
  - **Editor vs IDE in one line:** an editor just edits text; an IDE edits *and* helps you run, debug, and manage your whole project.
- **Runtime / Environment** — *where* and *with what* your code runs.
  - For Python, the **Python interpreter** installed on your machine is the runtime.
  - A **"development environment"** more broadly = all the tools set up to write and run code (your editor, the Python interpreter, the terminal). Later you'll meet **virtual environments** (isolated setups per project) — just know the word for now.

### Compiler vs Interpreter — the key difference
| | Compiler | Interpreter |
|---|---|---|
| When it translates | All at once, before running | Line by line, while running |
| Output | A runnable machine-code file | Runs directly, no separate file |
| Example languages | C, C++, Rust | Python, JavaScript |
| Trade-off | Faster to run, slower to start | Easier to test quickly, slightly slower |

### DO
- Write, in your own words, a one-sentence definition of each term above. No copying — your words.
- Explain out loud: "Python is run by an ______ (compiler/interpreter). An IDE differs from a text editor because ______."

### TRANSITION CONDITION
You can clearly explain the difference between a compiler and an interpreter, between a text editor and an IDE, and what an "environment/runtime" is — from memory.

---

## Day 3 — The Terminal (Your Command Line)

### LEARN
The **terminal** (a.k.a. command line, shell) is a text window where you type commands to control your computer directly — no clicking. Developers live here. It feels scary, then it feels like a superpower.
- You type a **command**, press Enter, the computer does it.
- You're always "in" a folder (the **working directory**). Commands act on that location.

### Core commands (Mac/Linux terminal, or Git Bash on Windows)
```bash
pwd                 # print working directory (where am I?)
ls                  # list files/folders here   (Windows cmd: dir)
cd foldername       # change into a folder
cd ..               # go up one folder
mkdir myproject     # make a new folder
touch notes.txt     # create an empty file (Git Bash/Mac/Linux)
rm notes.txt        # delete a file (careful - no undo!)
clear               # clean the screen
```

### DO
1. Open your terminal (Mac: Terminal; Windows: install/open **Git Bash**; Linux: your terminal).
2. Practice a full sequence:
```bash
pwd
mkdir coding-practice
cd coding-practice
mkdir day3
cd day3
touch hello.txt
ls
cd ..
```
3. Navigate around your real folders using only `cd`, `ls`, `pwd`. Get un-lost using `cd ..`.

### TRANSITION CONDITION
From memory, you can: find where you are (`pwd`), list contents (`ls`), make a folder (`mkdir`), move into and out of it (`cd`, `cd ..`), and create a file — without looking it up.

---

## Day 4 — What Is the Internet?

### LEARN
- The **internet** is a giant network of computers connected by cables (and wireless) all over the world. It's the *physical + addressing system* that lets any computer talk to any other.
- Every device has an **IP address** — like a postal address for computers (e.g. `142.250.190.78`).
- Data doesn't travel as one big lump. It's broken into small **packets**, sent across many routes, and reassembled at the other end. (Like mailing a book one page per envelope.)
- **Client and server:** a **client** is a computer asking for something (your phone/browser). A **server** is a computer that stores things and answers requests (where a website "lives"). Your laptop asks; the server answers.
- **The internet is NOT the web.** The internet is the roads. The web is one kind of traffic on those roads (more on Day 5). Email, video calls, and games also use the internet but aren't "the web."

### DO
- Draw (on paper) a simple diagram: your device (client) → internet → a server, with a request going one way and a response coming back.
- Explain out loud: "An IP address is like ____. Data travels in ____. A client ____ and a server ____."

### TRANSITION CONDITION
You can explain in your own words: what the internet is, what an IP address is, what packets are, and the difference between a client and a server.

---

## Day 5 — What Is the Web? + Set Up Python For Real

### LEARN — the Web
- The **World Wide Web** is the system of **websites and web pages** you view in a browser. It runs *on top of* the internet.
- A **browser** (Chrome, Firefox) is a client program that requests web pages and displays them.
- **URL** = the address of a web page (e.g. `https://example.com/page`).
- **DNS (Domain Name System)** = the internet's phone book. You type a name (`google.com`); DNS looks up the matching IP address, because names are for humans and numbers are for computers.
- **HTTP/HTTPS** = the language/rules browsers and servers use to talk. Browser sends an HTTP **request** ("give me this page"); server sends an HTTP **response** (the page). HTTPS is the secure (encrypted) version.
- **Frontend vs backend:** the **frontend** is what you see and click (runs in your browser). The **backend** is the server-side logic and data (runs on a server). An **API** is how the frontend asks the backend for data.
- Putting it together: you type a URL → DNS finds the server's IP → browser sends an HTTP request → server responds → browser decodes it and shows the page.

### DO — set up your Python environment (Day 5 graduation)
1. **Install Python:** download the latest from https://www.python.org/downloads/ . On Windows, **check the box "Add Python to PATH"** during install.
2. **Install a code editor:** download **VS Code** (https://code.visualstudio.com/) and install the official **Python extension** inside it.
3. Verify in your terminal:
```bash
python3 --version     # (on Windows you may type: python --version)
```
You should see a version like `Python 3.x.x`.
4. Try the **interactive shell** (REPL): type `python3` (or `python`) and press Enter, then:
```python
print("This is my first program. I wrote it. No AI.")
```
Type `exit()` to leave.
5. Now make a real program **file**:
```bash
mkdir hello-python && cd hello-python
touch app.py
```
6. Open the folder in VS Code, put this in `app.py`:
```python
print("This is my first Python file. I wrote it. No AI.")
```
7. Run it from the terminal:
```bash
python3 app.py     # (or: python app.py)
```

### TRANSITION CONDITION
1. You can explain (no notes): what the web is, what a browser/URL/DNS/HTTP do, and frontend vs backend.
2. You have Python + VS Code installed, you ran code in the REPL, and you ran your own `app.py`.

---

## Module 0 Complete When...
- [ ] You can explain how code runs on a computer (source → translate → CPU/RAM → output)
- [ ] You understand encoding/decoding
- [ ] You can explain compiler vs interpreter, editor vs IDE, and environments
- [ ] You can navigate the terminal from memory
- [ ] You can explain the internet AND the web (and how they differ)
- [ ] Python works on your machine and you ran your own program
- [ ] **All Transition Conditions passed → start Module 1**
