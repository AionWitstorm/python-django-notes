# Immutability vs Mutability in Python

In Python, **everything is an object**. Objects can be either **immutable** (cannot be changed after creation) or **mutable** (can be changed in place).

---

## Immutability

If two variables refer to the same immutable object, they may share the same memory address. Any modification results in **creation of a new object**.

```python
a = "react"
b = "react"
print(id(a))
print(id(b))
```

**Output (example):**

```
133696360725168
133696360725168
```

Both variables point to the same string object because strings are immutable.

---

## Mutability

Mutable objects can be modified **without changing their memory address**.

```python
a = [12, 13, 14, 15]
print(id(a))
print(a)

a[0] = 50
print(id(a))
print(a)
```

The `id` remains the same because lists are mutable.

---

## Key Difference

| Feature            | Immutable              | Mutable         |
| ------------------ | ---------------------- | --------------- |
| Change allowed     | ❌ No                   | ✅ Yes           |
| New object created | ✅ Yes                  | ❌ No            |
| Examples           | int, float, str, tuple | list, dict, set |

---

# Collection Data Types in Python

Python provides several **collection-related data types**:

* list
* tuple
* set
* frozenset
* dict
* range
* bytes
* bytearray

---

## 1. List

A **list** represents a group of values where:

* Insertion order is preserved
* Duplicates are allowed
* Heterogeneous elements are allowed
* Mutable

```python
a = []
print(type(a))  # list
```

### Example

```python
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
print(bicycles)
```

### Heterogeneous List

```python
a = [10, 20, 30, 10.4, True, "Hello"]
print(a)
```

### Indexing & Slicing

```python
a = [10, 20, 30, 40, 50, 60]
print(a[1])      # 20
print(a[2:4])    # [30, 40]
```

### Common Operations

```python
a.append(90)
a.remove(10)   # removes first occurrence

for x in a:
    print(x)
```

---

## 2. Tuple

A **tuple** is exactly like a list, but **immutable**.

```python
t = (10, 20, 30, 40)
print(type(t))
```

⚠️ Single-value tuple must include a comma:

```python
a = (10,)   # tuple
a = (10)    # int
```

### Tuple Features

* Order preserved
* Duplicates allowed
* Indexing & slicing allowed
* No add, remove, or update

```python
print(t[1])
print(t[1:3])
```

**Real-world example:**

```python
dashboard_roles = ('admin', 'student', 'teacher', 'parent')
```

---

## 3. Set

A **set** represents a group of values where:

* No duplicates
* Order is not preserved
* Mutable
* Heterogeneous allowed

```python
s = {10, 20, 30}
print(type(s))
```

### Important Notes

* `{}` → dict
* `set()` → empty set

### Set Operations

```python
s.add(31)
s.remove(20)
```

⚠️ Indexing & slicing are **not supported**.

---

## 4. Frozenset

A **frozenset** is an immutable version of a set.

```python
s = {10, 20, 30}
fs = frozenset(s)
print(type(fs))
```

* No add or remove
* No indexing

---

## Tuple vs Frozenset

| Feature    | Tuple     | Frozenset     |
| ---------- | --------- | ------------- |
| Order      | Preserved | Not preserved |
| Duplicates | Allowed   | Not allowed   |
| Mutable    | ❌ No      | ❌ No          |
| Indexing   | ✅ Yes     | ❌ No          |

---

## 5. Dictionary (dict)

A **dictionary** stores data in **key–value pairs**.

```python
d = {1: "Apple", 2: "Ball"}
print(type(d))
```

### Operations

```python
d[3] = "Mango"      # add
d[1] = "Elephant"  # update
```

* Keys must be unique
* Mutable
* No indexing or slicing

---

## 6. Range

A **range** represents a sequence of numbers.

```python
r = range(10)
print(type(r))
```

### Examples

```python
range(10)          # 0 to 9
range(10, 20)      # 10 to 19
range(10, 20, 2)   # step = 2
```

```python
r = range(20, 10, -3)
for i in r:
    print(i)
```

* Immutable
* Indexing & slicing allowed
* Item assignment ❌

---

## 7. Bytes

* Collection of integers (0–255)
* Immutable

```python
b = [10, 20, 30, 255]
by = bytes(b)
print(type(by))
```

⚠️ Invalid:

* Values > 255
* Non-integer elements

---

## 8. Bytearray

Same as bytes, but **mutable**.

```python
b = [10, 20, 30, 255]
by = bytearray(b)
by[0] = 200
print(type(by))
```

---

# Summary: Mutability of Data Types

| Data Type | Mutable |
| --------- | ------- |
| int       | ❌       |
| float     | ❌       |
| complex   | ❌       |
| bool      | ❌       |
| str       | ❌       |
| bytes     | ❌       |
| bytearray | ✅       |
| range     | ❌       |
| list      | ✅       |
| tuple     | ❌       |
| set       | ✅       |
| frozenset | ❌       |
| dict      | ✅       |

---

## None Data Type

`None` represents **no value / absence of value**.

```python
a = 10
a = None
```

---

## All 14 Python Data Types

1. int
2. float
3. complex
4. bool
5. str
6. list
7. tuple
8. set
9. frozenset
10. dict
11. range
12. bytes
13. bytearray
14. NoneType

Next: [Go to README](../README.md)