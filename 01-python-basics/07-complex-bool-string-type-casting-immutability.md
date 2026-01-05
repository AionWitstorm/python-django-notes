# Complex, Boolean, String, Type Casting & Immutability in Python

## Complex Data Type (`complex`)

### What is a Complex Number?
A **complex number** is represented as:

```python
a + bj
```

Where:
- `a` → real part
- `b` → imaginary part
- `j` → imaginary unit  
  (`j² = -1`, so `j = √-1`)

> ⚠️ Python uses **`j`**, not `i`

---

### Valid Complex Numbers
```python
a = 5 + 2j
print(a)

a = 5 + 2J
print(a)
````

✅ Capital `J` is allowed
❌ `i` or `I` is **not allowed**

```python
a = 5 + 2i   # ❌ Invalid
```

---

### Checking Type

```python
a = 5 + 2j
print(type(a))   # <class 'complex'>
```

---

### Real Part with Different Number Systems
```python
a = 0b1101 + 2j
print(a)   # (13+2j)
```

❌ Imaginary part **must be decimal**
```python
a = 0b1101 + 0b101j   # ❌ Error
```

---

### Operations on Complex Numbers
```python
a = 2 + 2j
b = 5 + 3j

print(a + b)
print(a - b)
print(a * b)
print(a / b)
```

---

### Access Real and Imaginary Parts
```python
a = 2 + 2j

print(a.real)   # 2.0
print(a.imag)   # 2.0
```

---

### Magnitude of Complex Number
```python
a = 3 + 4j
print(abs(a))   # 5.0
```

---

## Boolean Data Type (`bool`)
Boolean values can be **only**:

* `True`
* `False`

⚠️ Must start with **capital T / F**

---

### Examples
```python
a = True
print(type(a))   # bool

b = False
print(type(b))   # bool
```

❌ Invalid
```python
a = false   # ❌ Error
```

---

### Boolean from Comparison

```python
a = 10
b = 20

c = a > b
print(c)         # False
print(type(c))   # bool
```

---

### Boolean Arithmetic

Internally:

* `True` → 1
* `False` → 0

```python
a = True
b = False

print(a + b)     # 1
print(a * b)     # 0
print(type(a + b))   # int
```

---

##  String Data Type (`str`)

### What is a String?

Anything enclosed in quotes is a string.

```txt
' '    single quotes
" "    double quotes
''' ''' triple single quotes
""" """ triple double quotes (docstring)
```

> ❌ Python has **no `char` type**
> Single character is also a string

---

### Examples

```python
a = "Apple"
b = "A"
c = 'A'
```

All are `str`.

---

### Quotes Inside Strings

```python
a = 'Learning "python" is fun'
b = "Learning 'python' is fun"
```

---

### Triple Quotes (Multi-line Strings)

```python
a = """Learning
python
is
fun"""
print(a)
```

Works with `'''` also.

---

## String Indexing & Slicing

### Indexing

```text
-10 -9 -8 -7 -6 -5 -4 -3 -2 -1
 a  b  c  d  e  f  g  h  i  j
 0  1  2  3  4  5  6  7  8  9
```

```python
a = "abcdefghij"
print(a[2])     # c
print(a[-8])    # c
```

---

### Slicing Syntax

```python
a[start : end : step]
```

---

### Examples

```python
a = "Learning python is fun"

print(a[9])          # p
print(a[9:15])       # python
print(a[:15])        # Learning python
print(a[:])          # full string
```

---

## String Arithmetic

```python
a = "Learning python is "
b = "fun"

print(a + b)
print(3 * b)
```

### CLI Example

```python
print("#" * 50)
print("Hello")
print("#" * 50)
```

---

### String Length

```python
a = "apple"
print(len(a))
```

---

### Capitalize First Letter

```python
a = "hello"
temp = a[0].upper() + a[1:]
print(temp)
```

---

### Capitalize Last Letter

```python
a = "hello"
temp = a[:-1] + a[-1].upper()
print(temp)
```

---

## Type Casting in Python

### Fundamental Data Types

* int
* float
* complex
* bool
* str

---

### `int()`

```python
print(int(15.2))      # 15
print(int("123"))     # 123
```

❌ Invalid

```python
int("10.5")
int("0b101")
int(2+4j)
```

---

### `float()`

```python
print(float(10))      # 10.0
print(float(True))    # 1.0
```

❌ Invalid

```python
float(10+2j)
float("hello")
```

---

### `complex()`

```python
print(complex(10))
print(complex(10.5))
print(complex(True))
print(complex(False))
print(complex("10.5j"))
print(complex(10, 5))
```

---

### `bool()`

```python
print(bool(0))        # False
print(bool(10))       # True
print(bool(""))       # False
print(bool("False"))  # True
```

---

### `str()`

```python
print(str(10))
print(str(10.5))
print(str(3+6j))
print(str(True))
```

---

##  Immutability of Fundamental Data Types

### What is Immutability?

Once an object is created, it **cannot be changed**.
Any modification creates a **new object**.

---

### Example

```python
b = 10
print(id(b))

b = b + 3
print(id(b))
```

---

### Another Example

```python
a = 10
b = 10

print(id(a))
print(id(b))
print(a is b)   # True
```

---


Next: [Immutability vs Mutability in Python](08-collections-and-mutability.md)