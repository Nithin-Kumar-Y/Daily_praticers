# 🧠 Regex in Python

This repository is a **complete, practical, copy‑paste‑ready guide** to **Regular Expressions (Regex) in Python**.

Designed for:

* ✅ Beginners who want clarity
* ✅ Developers who want a quick reference
* ✅ Interview & real‑world usage

---

## 📌 What is Regex?

**Regex (Regular Expression)** is a sequence of characters that defines a **search pattern**.

Used for:

* Input validation
* Text search & replace
* Data cleaning
* Log analysis
* Web scraping

Python uses the built‑in **`re` module**.

---

## 📦 Import Regex Module

```python
import re
```

---

## 🔹 Basic Regex Functions

| Function       | Description      |
| -------------- | ---------------- |
| `re.search()`  | Find first match |
| `re.match()`   | Match from start |
| `re.findall()` | Find all matches |
| `re.sub()`     | Replace pattern  |
| `re.split()`   | Split string     |
| `re.compile()` | Compile pattern  |

---

## 🔹 Basic Example

```python
text = "My phone number is 9876543210"
match = re.search(r"\d+", text)
print(match.group())
```

---

## 🔤 Regex Metacharacters (A–Z)

### 1️⃣ Dot `.`

Matches any character except newline

```python
re.findall(r"a.b", "acb aab axb")
```

---

### 2️⃣ Caret `^`

Start of string

```python
re.findall(r"^Hello", "Hello World")
```

---

### 3️⃣ Dollar `$`

End of string

```python
re.findall(r"World$", "Hello World")
```

---

### 4️⃣ Asterisk `*`

0 or more occurrences

```python
re.findall(r"ab*", "a ab abb")
```

---

### 5️⃣ Plus `+`

1 or more occurrences

```python
re.findall(r"ab+", "ab abb a")
```

---

### 6️⃣ Question `?`

0 or 1 occurrence

```python
re.findall(r"colou?r", "color colour")
```

---

### 7️⃣ Curly Braces `{}`

Exact or range repetition

```python
re.findall(r"\d{10}", "9876543210")
```

---

### 8️⃣ Square Brackets `[]`

Character sets

```python
re.findall(r"[abc]at", "bat cat rat")
```

---

### 9️⃣ OR `|`

Alternation

```python
re.findall(r"cat|dog", "cat dog cow")
```

---

### 🔟 Backslash `\`

Escape special characters

```python
re.findall(r"\.com", "google.com")
```

---

## 🔠 Predefined Character Classes

| Pattern | Meaning        |
| ------- | -------------- |
| `\d`    | Digit (0–9)    |
| `\D`    | Non‑digit      |
| `\w`    | Word character |
| `\W`    | Non‑word       |
| `\s`    | Whitespace     |
| `\S`    | Non‑space      |

---

## 📍 Anchors

| Pattern | Meaning       |
| ------- | ------------- |
| `^`     | Start         |
| `$`     | End           |
| `\b`    | Word boundary |

```python
re.findall(r"\bcat\b", "cat scatter")
```

---

## 🔗 Grouping & Capturing

```python
text = "Date: 2025-01-15"
match = re.search(r"(\d{4})-(\d{2})-(\d{2})", text)
print(match.groups())
```

---

## 🔁 `findall()`

```python
re.findall(r"\d+", "12 apples and 45 oranges")
```

---

## ✂️ `split()`

```python
re.split(r"[,\s]+", "apple, banana orange")
```

---

## 🔄 `sub()`

```python
re.sub(r"\d", "*", "Phone: 9876")
```

---

## 📌 `re.compile()` (Performance)

```python
pattern = re.compile(r"\d+")
pattern.findall("123 456")
```

---

## ✅ Input Validation Examples

### 📧 Email Validation

```python
pattern = r"^[\w\.-]+@[\w\.-]+\.\w+$"
re.match(pattern, "test@gmail.com")
```

---

### 📱 Phone Number (India)

```python
pattern = r"^[6-9]\d{9}$"
```

---

### 🔐 Password Rule

```python
pattern = r"^(?=.*[A-Z])(?=.*\d).{8,}$"
```

---

## 🧠 Regex Best Practices

✔ Always use raw strings `r""`
✔ Keep patterns readable
✔ Test on small data
✔ Avoid over‑complex regex
✔ Use comments if needed

---

## 🧪 Practice Problems

* Extract emails from text
* Validate phone numbers
* Replace sensitive data
* Parse log files

---

## 📚 Learning Resources

* Python `re` documentation
* regex101.com (practice)

---

## 🏁 Conclusion

Regex is not memorization — it’s **pattern thinking**.

Master basics → practice daily → apply in real problems.

**Happy Coding 🚀**

---

**Author:** NITHIN KUMAR Y
