# 🛡️ Python Error Handling

## ZERO → HERO SERIES

This guide takes you from **absolute basics** to **professional-level error handling** in Python.
Designed for **GitHub README**, interviews, and real-world coding.

---

## 🟢 LEVEL 0 — What is an Error? (Foundation)

### ❓ What is an error?

An **error** occurs when Python cannot continue execution normally.

```python
print(10 / 0)
```

❌ Program crashes

### 🧠 Truth

```
Errors are normal.
Crashes are optional.
```

---

## 🟢 LEVEL 1 — Types of Errors (Must Know)

### 1️⃣ Syntax Error (❌ Cannot Be Handled)

```python
if x == 10
    print(x)
```

* Code does **not run at all**
* Happens due to wrong Python syntax

---

### 2️⃣ Runtime Errors (✅ Can Be Handled)

| Error Name        | When It Happens         |
| ----------------- | ----------------------- |
| ZeroDivisionError | Division by zero        |
| ValueError        | Wrong value type        |
| TypeError         | Invalid operation       |
| IndexError        | List index out of range |
| KeyError          | Missing dictionary key  |
| FileNotFoundError | File does not exist     |

👉 **Error handling is ONLY for runtime errors**

---

## 🟢 LEVEL 2 — Basic try-except (Beginner)

```python
try:
    print(10 / 0)
except:
    print("Something went wrong")
```

✔ Prevents crash
❌ Bad practice (too generic)

---

## 🟡 LEVEL 3 — Specific Exceptions (Important)

```python
try:
    x = int(input("Enter number: "))
    print(10 / x)
except ValueError:
    print("Please enter a valid number")
except ZeroDivisionError:
    print("Cannot divide by zero")
```

✔ Clean
✔ Safe
✔ Professional

---

## 🟡 LEVEL 4 — Multiple Exceptions Together

```python
try:
    x = int(input("Enter number: "))
    print(10 / x)
except (ValueError, ZeroDivisionError):
    print("Invalid input or division by zero")
```

✔ Use when handling logic is same

---

## 🔵 LEVEL 5 — except Exception as e (Debugging)

```python
try:
    int("abc")
except Exception as e:
    print("Error:", e)
```

✔ Shows exact error message
✔ Used in debugging & logs

---

## 🔵 LEVEL 6 — else Block (Very Important)

```python
try:
    x = int(input("Enter number: "))
    result = 100 / x
except Exception as e:
    print("Error:", e)
else:
    print("Success:", result)
```

🧠 Rule:

> `else` runs **only if no error occurs**

---

## 🟣 LEVEL 7 — finally Block (Resource Safety)

```python
try:
    f = open("data.txt")
    print(f.read())
except FileNotFoundError:
    print("File not found")
finally:
    print("Program ended")
```

✔ Always runs
✔ Used for cleanup

---

## 🟣 LEVEL 8 — Real File Handling (Best Practice)

```python
try:
    with open("data.txt") as f:
        print(f.read())
except FileNotFoundError:
    print("Check file path")
except PermissionError:
    print("Permission denied")
```

---

## 🔴 LEVEL 9 — Raising Errors (Input Control)

```python
age = int(input("Enter age: "))

if age < 18:
    raise ValueError("Age must be 18+")
```

✔ Input validation
✔ Used everywhere

---

## 🔴 LEVEL 10 — Custom Exceptions (Advanced)

```python
class AgeError(Exception):
    pass

age = int(input("Enter age: "))

if age < 18:
    raise AgeError("Underage user")
```

### Used in:

* Frameworks
* APIs
* Libraries

---

## 🔥 LEVEL 11 — Exception Chaining (Pro Level)

```python
try:
    int("abc")
except ValueError as e:
    raise RuntimeError("Conversion failed") from e
```

✔ Keeps original cause
✔ Debug-friendly

---

## 🔥 LEVEL 12 — Best Practices (Memorize)

- ✅ Catch specific exceptions
- ❌ Never use empty `except:`
- ✅ Validate inputs early
- ✅ Use `with` for files
- ✅ Use logging
- ❌ Don’t hide errors silently

---

## 🧠 LEVEL 13 — Think Like a Developer

### ❌ Bad Practice

```python
try:
    do_something()
except:
    pass
```

### ✅ Good Practice

```python
try:
    do_something()
except SpecificError as e:
    print(e)
```

---

## 🧪 LEVEL 14 — Practice Tasks

### Task 1

* Take two numbers
* Divide them
* Handle invalid input & zero division

### Task 2

* Open a file
* If missing → create it

### Task 3

* Dictionary access with safe handling

---

## 🏁 HERO STATUS CHECKLIST ✅

You are an **Error Handling HERO** if you can:

* Predict errors before running code
* Handle them without crashing
* Write user-friendly messages
* Raise meaningful exceptions
* Debug confidently

---

**Author:** Nithin Kumar Y 🚀
