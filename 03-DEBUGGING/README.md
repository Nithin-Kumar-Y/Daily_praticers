## 🐞 Python Debugging — Practical Repository Guide

Debugging is not just a feature in Python — it is a CORE developer skill.

**If you know how to debug, you can:**

• Fix bugs faster

• Understand others’ code

• Crack interviews

• Become a real engineer (not just a coder)

So yes — debugging is absolutely a **concept + practical topic** worth learning.

---

### 📌 What is Debugging?

Debugging is the process of:

• Finding bugs

• Understanding why they happen

• Fixing them correctly (not by guesswork)

**Bugs can be:**

• Syntax errors

• Runtime errors

• Logical errors

---

### 🧠 Why Debugging Matters (My Honest Opinion)

Languages can be learned in months.

Debugging skills take years — but give 10× confidence.

👉 Companies hire people who can DEBUG.

👉 Interviews test debugging indirectly.

👉 Real projects survive only with good debugging.

So yes — treat debugging as a **first‑class topic**.

---

### 🔹 Types of Errors in Python

#### 1️⃣ Syntax Error
Code breaks before running

**Example:**
```
print("Hello"
```
---

#### 2️⃣ Runtime Error
Code runs but crashes

**Example:**
```
x = 10 / 0
```
---

#### 3️⃣ Logical Error (Most dangerous)
Code runs, but output is wrong

**Example:**
Calculating average incorrectly

---

### 🔍 Basic Debugging Techniques

#### 1️⃣ print() Debugging (Most used)
```
print("value of x:", x)
```
Use to:

• Track variable values

• Understand program flow

---

#### 2️⃣ Using traceback (Error messages)

Always read:

• Error type

• Line number

• File name

Python tells you exactly where it failed — people ignore it.

-----

#### 🐍 Built‑in Debugger: pdb

pdb = Python Debugger (VERY IMPORTANT)
```
import pdb
pdb.set_trace()
```

**Common pdb commands:**
```
• n → next line
• s → step inside
• p var → print variable
• c → continue
• q → quit
```
---

### 🧰 IDE Debugging (Real‑World)

Most developers debug using:

• VS Code Debugger

• PyCharm Debugger


Features:

• Breakpoints

• Variable watch

• Step execution

• Call stack view


Knowing IDE debugging = industry ready.

---

### 🧪 Debugging with Exceptions

Use try‑except smartly:
```
try:
risky_code()
except ZeroDivisionError as e:
print(e)
```
Never hide errors blindly.

---

#### 📋 Assertions (Hidden Gem)

assert condition, "message"

Example:
```
assert age > 0, "Age cannot be negative"
```
Used heavily in testing & debugging.

---

### 🪵 Logging (Advanced Debugging)

Instead of print(), professionals use logging.

Levels:

• DEBUG

• INFO

• WARNING

• ERROR

• CRITICAL

(logging topic usually comes after debugging)

---

### 🧠 Debugging Mindset (Very Important)

✔ Don’t guess — observe

✔ Reproduce the bug

✔ Reduce code to minimal example

✔ Fix root cause, not symptom

✔ Test after fix

---

### 🧪 Practice Debugging Tasks

• Fix broken loops

• Debug recursive functions

• Trace linked list errors

• Debug DP wrong answers

• Fix edge cases

---

### 🏁 Final Verdict

Debugging is **NOT** optional.

If you master debugging:

• Python becomes easy

• DSA becomes clear

• Confidence skyrockets

Learn syntax → Learn logic → MASTER DEBUGGING 🧠🔥

**AUTHOR:** NITHIN KUMAR Y
