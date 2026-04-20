# 🐍 Python Basics: Input, Output, Operators, Data Types & Conditions

---

## 📦 1. Data Types (Very Important)

### 🔢 Numeric Types
```python
age = 20        # int (whole number)
price = 99.5    # float (decimal number)
```

### 📝 String (Text)
```python
name = "Ali"
```

### ✅ Boolean
```python
is_student = True
```

### 📋 List (Mutable / Changeable)
```python
fruits = ["apple", "banana", "mango"]
```

### 🔒 Tuple (Immutable / Fixed)
```python
dob = (2005, 8, 15)
```

### 🧾 Dictionary (Key–Value Pairs)
```python
person = {
    "name": "Ali",
    "age": 20
}
```

### ❌ None Type
```python
x = None
```

---

## ⌨️ 2. Input in Python

```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))
```

---

## 🖨️ 3. Output Methods

### ⭐ f-string (Recommended)
```python
print(f"Your name is {name} and your age is {age}")
```

### Other Methods
```python
print("Your name is {} and your age is {}".format(name, age))
print("Your name is " + name + " and your age is " + str(age))
print("Your name is", name, "and your age is", age)
```

---

## ➗ 4. Arithmetic Operators

```python
+   # Addition
-   # Subtraction
*   # Multiplication
/   # Division
%   # Modulus
```

---

## 🔀 5. Conditions (if / elif / else)

```python
age = int(input("Enter your age: "))

if age < 18:
    print("Not eligible")
elif 18 <= age <= 25:
    print("Grade C")
elif 25 < age <= 30:
    print("Grade B")
elif 30 < age <= 40:
    print("Grade A")
else:
    print("Age out of range")
```

---

## ⚙️ 6. Logical Operators

```python
and   # both conditions true
or    # at least one true
not   # reverse condition
```

### Example
```python
if age >= 18 and age <= 30:
    print("Valid age")

if not age < 18:
    print("Adult")
```

---

## 📤 7. Output Formatting

### Multi-line Output
```python
print(f"""
Sum: {10}
Subtraction: {5}
""")
```

### Using \n
```python
print(f"Sum: {10}\nSubtraction: {5}")
```

---

## 🔁 8. Loops (for / while)

### 🔹 for loop
```python
for i in range(5):
    print(i)

fruits = ["apple", "banana", "mango"]
for fruit in fruits:
    print(fruit)
```

---

### 🔹 while loop
```python
i = 0

while i < 5:
    print(i)
    i += 1
```

---

### 🔹 break and continue
```python
for i in range(5):
    if i == 3:
        break
    print(i)

for i in range(5):
    if i == 3:
        continue
    print(i)
```

---

## 📚 9. List, Tuple & Dictionary Practice (LPP)

### 🔹 List Operations
```python
numbers = [1, 2, 3]
numbers.append(4)
numbers.remove(2)
print(numbers)
```

### 🔹 Tuple Basics
```python
coords = (10, 20)
print(coords[0])
```

### 🔹 Dictionary Operations
```python
person = {"name": "Ali", "age": 20}

print(person["name"])
person["city"] = "Karachi"
person.pop("age")

print(person)
```

---

# ⚙️ FUNCTIONS PRACTICE

## 📌 What is a Function?
A function is a reusable block of code that performs a specific task.

### ✅ Benefits:
- Avoid repetition
- Organize code
- Improve readability

---

## 🧪 Function Examples

### 1. Basic Function
```python
def greet():
    return "Hello"
```

### 2. Function with Parameter
```python
def greet_name(name):
    return f"Hello {name}"
```

### 3. Add Two Numbers
```python
def add(a, b):
    return a + b
```

### 4. Square of a Number
```python
def square(n):
    return n * n
```

### 5. Cube of a Number
```python
def cube(n):
    return n * n * n
```

### 6. Check Positive Number
```python
def is_positive(n):
    if n > 0:
        return "Positive"
    return "Not Positive"
```

### 7. Maximum of Two Numbers
```python
def max_two(a, b):
    if a > b:
        return a
    return b
```

---

## 🚀 Mini Calculator Example

```python
n1 = int(input("Enter first number: "))
n2 = int(input("Enter second number: "))

print(f"""
Sum: {n1+n2}
Subtraction: {n1-n2}
Multiplication: {n1*n2}
Division: {n1/n2}
Modulus: {n1%n2}
""")
```

---

# 🧱 OOP (Object-Oriented Programming)

## 🚗 Classes & Inheritance Example

```python
class Car:
    def __init__(self, name, brand):
        self.name = name
        self.brand = brand

    def carInfo(self):
        return f"Car name is {self.name} and brand is {self.brand}"

class ElectricCar(Car):
    def __init__(self, name, brand, battery_size):
        super().__init__(name, brand)
        self.battery_size = battery_size

car1 = ElectricCar("tesla", "mx6", "86mkh")

print(f"""
{car1.battery_size}
{car1.name}
{car1.brand}
{car1.carInfo()}
""")
```

---

# 🧠 Advanced Practice: Lists, Dictionaries & Functions (JS Comparison)

## 🟡 List in Python (like Array in JS)
```python
users = ["Ali", "Ahmed", "Sara"]

users.append("Haroon")
users.remove(users[2])
users[1] = "Islam"

for user in users:
    if user in ["Ali", "Haroon", "Islam"]:
        print(user)
    else:
        print("user not found")
```

---

## 🟡 Dictionary in Python (like Object in JS)
```python
student = {
    "name": "Ali",
    "age": 20
}

student["class"] = "5"
student["age"] = 23
del student["class"]
```

---

## 🧠 Simple Final Rule

| Method | Best Use |
|--------|----------|
| ["key"] | when you are 100% sure |
| .get() | when working with real apps (Django/API) ⭐ |

```python
print(student["name"])
print(student.get("name"))
print(student.get("name", "not found"))
print(student)
```

---

## 🔁 Looping in Dictionaries

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Karachi"
}

print(student.items())

for key, value in student.items():
    if key == "age":
        student[key] = "23"
    print(value)
```

---

## 🧑‍🤝‍🧑 List of Dictionaries

```python
users = [
    {"name": "Ali", "age": 20},
    {"name": "Ahmed", "age": 22}
]

for user in users:
    print(user)
    print(user["name"])
```

---

## ⚙️ Function Returning Dictionary

```python
def create_user(name, age):
    return {
        "name": name,
        "age": age
    }

r = create_user("hammad", "25")
print(r)
```

---

## 🧾 Final Mini System (Students DB)

```python
students = []

def add_std(name, age):
    student = {
        "name": name,
        "age": age
    }
    students.append(student)

add_std("Hammad", 23)

for student in students:
    print(student)
```