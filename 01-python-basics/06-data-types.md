# Data Types in Python

## What is a Data Type?
A **data type** defines:
- The **type of value** stored in a variable
- The **operations** that can be performed on it

### Example
```python
a = 10
```
Here:
* `a` → variable
* `10` → integer value
* `int` → data type
---

## Dynamic Typing in Python
Python is a **dynamically typed language**.
This means:
- You do **not** declare data types explicitly
- A variable can be **reassigned to a different type**
### Example
```python
a = 10
print(a)

a = 10.5
print(a)
```

✅ Valid in Python
❌ Not allowed in **statically typed languages** like C or C++

---

## Checking the Data Type
Use the built-in `type()` function.
```python
a = 10
print(type(a))   # <class 'int'>

a = 10.5
print(type(a))   # <class 'float'>
```

---

## Object Identity (Memory Address)
Python stores objects in memory, and variables reference them.

To check the **memory address**, use `id()`.

```python
a = 10
print(id(a))
```

📌 This helps understand **immutability** in Python.

---

## Built-in Data Types in Python
Python has **14 built-in data types**:
1. int
2. float
3. complex
4. bool
5. str
6. bytes
7. bytearray
8. range
9. list
10. tuple
11. set
12. frozenset
13. dict
14. NoneType
---

# 1️⃣ Integer (`int`)
Integers are **whole numbers** (positive, negative, or zero).
```python
a = 10      # ✅ int
a = -100    # ✅ int
a = 10.5    # ❌ not int
```

### Python 2 vs Python 3

* Python 2 had `int` and `long`
* Python 3 has **only `int`**
* Large numbers are handled automatically

```python
a = 1234293864389456348756348745896745879
print(type(a))   # <class 'int'>
```

---

## Integer Number Systems

Python supports integers in **four number systems**:

| System      | Base | Allowed Digits | Prefix    |
| ----------- | ---- | -------------- | --------- |
| Binary      | 2    | 0, 1           | `0b`      |
| Decimal     | 10   | 0–9            | (default) |
| Octal       | 8    | 0–7            | `0o`      |
| Hexadecimal | 16   | 0–9, A–F       | `0x`      |

---

### Binary Example

```python
a = 0b1010
print(a)      # 10
```

---

### Octal Example

```python
a = 0o1010
print(a)      # 520
```

---

### Hexadecimal Example

```python
a = 0xFACE
print(a)      # 64206
```

---

## Base Conversion Functions

| Function | Converts to |
| -------- | ----------- |
| `bin()`  | Binary      |
| `oct()`  | Octal       |
| `hex()`  | Hexadecimal |

### Example

```python
a = 0xFACE

print(bin(a))
print(oct(a))
print(hex(a))
print(a)       # Decimal (default)
```

### Negative Number Example

```python
a = -15
print(bin(a))
```

---

# 2️⃣ Float (`float`)

A **float** is a number with a **decimal point**.

```python
a = 1.45
print(type(a))   # <class 'float'>
```

### Example

```python
a = 14
print(type(a))   # int

b = 34.56
print(type(b))   # float
```

---

## Exponential (Scientific) Notation

Python supports exponential notation using `e` or `E`.

```python
a = 1.2e3
print(a)         # 1200.0
print(type(a))   # float
```

Meaning:

```
1.2e3 = 1.2 × 10³
```

---

## ❌ Invalid Operations with Float

Floats **cannot** be represented in binary, octal, or hexadecimal form.

```python
a = 1.5
bin(a)    # ❌ TypeError
```

❌ Also invalid:

```python
a = 0b1.1
a = 0o1.1
a = 0x1.1
```
[Go to README](../README.md)