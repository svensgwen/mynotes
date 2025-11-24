# 🐍 ✨ Python Cheat Sheet

![Python Cover](../../Images/python.webp)

## 📦 Variables
We use variables to temporarily store data in memory.

```python
price = 10
rating = 4.9
course_name = 'Python for Beginners'
is_published = True
```

- 🔢 `price` → integer  
- 🌊 `rating` → float  
- 🔤 `course_name` → string  
- 🔘 `is_published` → boolean  

## 📝 Comments
Use comments to explain the *why* behind your code.

```python
# This is a comment.
# Comments can span multiple lines.
```

## 🎤 Receiving Input
```python
birth_year = int(input('Birth year: '))
```

`input()` returns a string → convert it using `int()`.

## 🔡 Strings
Access, slice, and format strings like a pro.

```python
course = 'Python for Beginners'
course[0]
course[-1]
course[1:5]
```

### 🎨 Methods
- `.upper()`  
- `.lower()`  
- `.title()`  
- `.find('p')`  
- `.replace('p', 'q')`  
- `'Python' in course` → boolean  

## ➗ Arithmetic Operations
- ➕ Addition  
- ➖ Subtraction  
- ✖️ Multiplication  
- ➗ Division  
- 🪓 `//` integer division  
- 🎯 `%` modulus  
- ⚡ `**` exponent  

Order of operations: `()`, `**`, `*/`, `+-`

## 🌡️ If Statements
```python
if is_hot:
    print("hot day")
elif is_cold:
    print("cold day")
else:
    print("beautiful day")
```

### 🔗 Logical Ops
- `and`
- `or`
- `not`

## ⚖️ Comparison Operators
`>`, `>=`, `<`, `<=`, `==`, `!=`

## 🔁 While Loops
```python
i = 1
while i < 5:
    print(i)
    i += 1
```

## 🔄 For Loops
```python
for i in range(1, 5):
    print(i)
```

## 📚 Lists
```python
numbers = [1, 2, 3]
numbers.append(6)
numbers.insert(0, 6)
numbers.remove(6)
numbers.pop()
numbers.index(8)
numbers.sort()
numbers.reverse()
numbers.copy()
```

## 🧱 Tuples
Read‑only lists.

```python
coordinates = (1, 2, 3)
x, y, z = coordinates
```

## 🗂️ Dictionaries
```python
customer = {
    "name": "John Smith",
    "age": 30,
    "is_verified": True
}
```

## 🧩 Functions
```python
def greet_user(name):
    print(f"Hi {name}")
```

- Positional args  
- Keyword args  
- `return` values  

## 🚨 Exceptions
```python
try:
    age = int(input('Age: '))
    risk = 20000 / age
except ValueError:
    print("Invalid number")
except ZeroDivisionError:
    print("Age cannot be 0")
```

## 🏗️ Classes
```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y
```

## 🧬 Inheritance
```python
class Mammal:
    def walk(self):
        print("walk")

class Dog(Mammal):
    def bark(self):
        print("bark")
```

## 📁 Modules & Packages
- `import converters`
- `from converters import kg_to_lbs`
- Packages = folders with `__init__.py`

## 🧰 Standard Library (Examples)
```python
import random

random.random()
random.randint(1,6)
random.choice(['John', 'Bob', 'Mary'])
```

## 🌐 PyPI
Install packages:

```
pip install openpyxl
pip uninstall openpyxl
```

---

✨ **Done. Your PDF is now reborn as a clean, icon-rich markdown file.**  
