# Identifiers and Keywords in Python

## What is an Identifier?
An **identifier** is the name used to identify a variable, function, class, or object in Python.

### Examples
```python
a = 10
def hello():
    pass
````
Here:
* `a` → identifier
* `hello` → identifier

---

## Rules for Identifiers

### 1. Allowed characters

Identifiers can contain:

* Lowercase letters: `a–z`
* Uppercase letters: `A–Z`
* Digits: `0–9`
* Underscore: `_`

❌ No special symbols like `@`, `#`, `$`, etc.

---

### 2. Cannot start with a digit

```python
123total = 100   ❌ Invalid (starts with a digit)
total123 = 100   ✅ Valid
cash = 10        ✅ Valid
c@sh = 1         ❌ Invalid (`@` not allowed)
```

---

### 3. Identifiers are case-sensitive

Python treats **uppercase and lowercase letters as different**.

> **Case-sensitive**: uppercase and lowercase letters are treated as different
> **Case-insensitive**: uppercase and lowercase letters are treated as the same

```python
name = 10
Name = 100
NAME = 1000

print(name)
print(Name)
print(NAME)
```

All three variables are **different identifiers**.

---

### 4. Underscore usage

Underscore is allowed in identifiers.

```python
hello_world = 10   ✅ Valid
hello world = 10   ❌ Invalid (space not allowed)
```

---

### 5. Length of identifiers

Python allows **long identifiers** (unlike C/C++), but they are **not recommended**.

```python
hello_world_my_name_is_aaaaaaaaaaaaaaaaaaa = 10
print(hello_world_my_name_is_aaaaaaaaaaaaaaaaaaa)
```

✅ Valid
❌ Poor readability — use meaningful but shorter names.

---

### 6. Keywords cannot be used as identifiers

Reserved words (keywords) **cannot be used as variable or function names**.

```python
if = 100     ❌ Invalid
print(if)    ❌ Invalid
```

---

## Underscore Naming Conventions (Important)

These are **naming conventions**, not strict access control.

```python
_a
```

* Intended as **internal / private by convention**

```python
__a
```

* Name mangling occurs inside classes
* Used to avoid name conflicts (not truly protected)

```python
__a__
```

* Called **magic variables / dunder variables**
* Used internally by Python (e.g., `__init__`, `__str__`)

⚠️ Do not create your own `__something__` names unless you know what you’re doing.

---

## Keywords (Reserved Words) in Python

### What are Keywords?

Keywords are **pre-reserved words** in Python with special meaning.
They **cannot** be used as identifiers.

---

### How to find keywords in Python

```python
import keyword
print(keyword.kwlist)
```

### Output (Python 3.x)

```python
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await',
 'break', 'class', 'continue', 'def', 'del', 'elif', 'else',
 'except', 'finally', 'for', 'from', 'global', 'if', 'import',
 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise',
 'return', 'try', 'while', 'with', 'yield']
```

✅ **Total keywords (currently): 36**

---

## Newer Keywords

* `async`, `await` → introduced in **Python 3.5**
  * Used for asynchronous programming
* `nonlocal` → introduced in **Python 3.0**
  * Used in nested functions (closures)

[Go to README](../README.md)