# 📂 FILE HANDLING IN PYTHON

---

## 🧠 What is File Handling?

File handling means:
- Creating files  
- Reading files  
- Writing data into files  
- Updating files  

👉 Think of it like saving notes on your computer

---

## 🟢 LEVEL 1 — OPENING A FILE

### 📌 Basic Syntax
```python
file = open("data.txt", "r")
```

---

### 📌 File Modes

| Mode | Meaning |
|------|--------|
| r | Read |
| w | Write (overwrite) |
| a | Append |
| x | Create new file |

---

### 🎯 Example
```python
file = open("data.txt", "r")
print(file.read())
file.close()
```

---

### ⚠️ IMPORTANT
```python
file.close()
```

---

## 🟡 LEVEL 2 — WRITE FILE

### 📌 Overwrite File
```python
file = open("data.txt", "w")
file.write("Hello Python")
file.close()
```

---

## 🟠 LEVEL 3 — APPEND FILE

### 📌 Add Data Without Deleting
```python
file = open("data.txt", "a")
file.write("\nNew Line Added")
file.close()
```

---

## 🔵 LEVEL 4 — BEST PRACTICE (WITH STATEMENT)

### 📌 Read File Safely
```python
with open("data.txt", "r") as file:
    content = file.read()
    print(content)
```

---

### 📌 Write File Safely
```python
with open("data.txt", "w") as file:
    file.write("Hello World")
```

---

## 🟣 LEVEL 5 — READ LINE BY LINE

```python
with open("data.txt", "r") as file:
    for line in file:
        print(line)
```

---

## 🔴 LEVEL 6 — ERROR HANDLING WITH FILES

### 📌 File Not Found Handling
```python
try:
    with open("data.txt", "r") as file:
        print(file.read())
except FileNotFoundError:
    print("File not found")
```

---

## 🧪 PRACTICE TASKS

### 🟢 Task 1
Create a file and write your name

---

### 🟡 Task 2
Append your city name to file

---

### 🟠 Task 3
Read file and print content

---

### 🔴 Task 4
Handle error if file does not exist

---

## 🚀 MINI PROJECT — NOTES APP (CLI)

```python
while True:
    choice = input("""
1. Write Note
2. Read Notes
3. Exit
""")

    if choice == "1":
        note = input("Enter note: ")
        with open("notes.txt", "a") as file:
            file.write(note + "\n")

    elif choice == "2":
        try:
            with open("notes.txt", "r") as file:
                print(file.read())
        except FileNotFoundError:
            print("No notes found")

    elif choice == "3":
        break
```

---

## 🎯 WHAT YOU LEARNED

- Open files  
- Read files  
- Write files  
- Append files  
- Safe handling (`with`)  
- Error handling with files  
- Mini project 