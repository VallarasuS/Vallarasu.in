---
layout: post
category: Python
---

<style>
    body {
        filter: none !important;
        background: #000000;
        color: white;
    }

    a {
        color: #ffff10;
    }

    code {
        background: #2d2d2d;
        border-radius: 5px;
    }

    pre { 
        line-height: 125%; 
    }

    .highlight {
        background: #000000;
        color: #cccccc;
    }

    .highlight .hll { background-color: #222222; }

    /* Comments */
    .highlight .c, .highlight .ch, .highlight .cm, 
    .highlight .cp, .highlight .cpf, .highlight .c1 { 
        color: #00d600; 
    }

    /* Keywords */
    .highlight .k, .highlight .kc, .highlight .kd, 
    .highlight .kn, .highlight .kp, .highlight .kr, 
    .highlight .kt, .highlight .ow { 
        color: #cdcd00; 
    }

    /* Strings */
    .highlight .s, .highlight .sa, .highlight .sb, .highlight .sc, 
    .highlight .dl, .highlight .sd, .highlight .s2, .highlight .se, 
    .highlight .sh, .highlight .si, .highlight .sx, .highlight .sr, 
    .highlight .s1, .highlight .ss { 
        color: #ed9d13; 
    }

    /* Numbers */
    .highlight .m, .highlight .mb, .highlight .mf, .highlight .mh, 
    .highlight .mi, .highlight .mo, .highlight .il { 
        color: #cd00cd; 
    }

    /* Builtins & Names */
    .highlight .nb, .highlight .bp { 
        color: #cd00cd; 
    }

    .highlight .nc, .highlight .nv, .highlight .vc, .highlight .vg, 
    .highlight .vi, .highlight .vm { 
        color: #00cdcd; 
    }

    /* Operators */
    .highlight .o { 
        color: #3399cc; 
    }

    /* Special */
    .highlight .cs { 
        color: #cd0000; 
        font-weight: bold; 
    }

    .highlight .err { 
        color: #cccccc; 
        border: 1px solid #FF0000; 
    }

    .code {
        font-size: 14px;
    }
</style>

#### Contents

1. [Variables and Data Types](#variables-and-data-types)
1. [Input and Output](#input-and-output)
1. [Arithmetic Operators](#arithmetic-operators)
1. [Comparison Operators](#comparison-operators)
1. [Logical Operators](#logical-operators)
1. [Membership Operators](#membership-operators)
1. [If elif else](#if-elif-else)
1. [String Operations](#string-operations)
1. [Functions](#functions)
1. [While Loop](#while-loop)
1. [For Loop](#for-loop)
1. [List and Operations](#list-and-operations)
    - [List Operations](#list-operations)
    - [List Comprehension](#list-comprehension)
    - [List Slicing](#list-slicing)
1. [Tuples](#tuples)
1. [Set](#set)
1. [Dictionary](#dictionary)
1. [Exception Handling](#exception-handling)
1. [File Handling](#file-handling)
    - [Read Mode](#read-mode)
    - [Write Mode](#write-mode)
    - [Append Mode](#append-mode)
1. [Common Built-in Functions](#common-built-in-functions)



## Variables and Data Types

```python
name = "John"   # string  ->  str
age = 30        # number  ->  int
weight = 63.5   # number  ->  float
married = True  # Boolean ->  bool
```

## Input and Output

```python
# Read Input from terminal window
name = input("Enter Name")  # -> John

# Write name to terminal window
print(name) # -> John
```

## Arithmetic Operators


```python
x = 10
y = 3
z = x + y   # addition          -> 13
z = x - y   # subtraction       -> 7
z = x * y   # multiplication    -> 30
z = x / y   # true division     -> 3.3333
z = x // y  # floor division    -> 3
z = x ** y  # exponent          -> 1000
z = x % y   # modulo division   -> 1
```

## Comparison Operators

```python
x = 10
y = 5

z = (x == y)   # Equal to                  -> False
z = (x != y)   # Not equal to              -> True
z = (x > y)    # Greater than              -> True
z = (x < y)    # Less than                 -> False
z = (x >= y)   # Greater than or equal to  -> True
z = (x <= y)   # Less than or equal to     -> False
```

## Logical Operators

```python
x = 10
y = 5
z = 15

result = (x > y) and (z > y)    # and  -> True (both conditions true)
result = (x > y) or (z < y)     # or   -> True (any one condition true)
result = not (x > y)            # not  -> False (negate condition)
```

## Membership Operators

``` python
fruits = ["apple", "banana", "cherry"]
name = "python"

result = "banana" in fruits          # in       -> True
result = "mango" in fruits           # in       -> False
result = "python" in name            # in       -> True
result = "java" not in name          # not in   -> True
result = "banana" not in fruits      # not in   -> False
```

## If elif else

```python
if number > 0:
    print(f"{number} -> Positive")
elif number == 0:
    print(f"{number} -> Zero")
else:
    print(f"{number} -> Negative")
```

## String Operations

```python
text = "  Hello Python World!  "

print(text.upper())                     #   HELLO PYTHON WORLD!
print(text.lower())                     #   hello python world!

print(text.strip())                     # Hello Python World!
print(text.split())                     # ['Hello', 'Python', 'World!']

fruits = ["apple", "banana", "cherry"]
print(", ".join(fruits))                # apple, banana, cherry

print("Python".find("th"))              # 2
print("Python".find("java"))            # -1

name = "John"
print("Hello, {}".format(name))         # Hello, John
print(f"Hello, {name}!")                # Hello, John!
```

## Functions

```python
def greet():
    print("Hello World!")
    
def hello(name):
    print("Hello", name)        

def add(x, y):
    return x + y

def increment(x, y = 1)
    return x + y

greet()                         # Hello World!
hello("John")                   # Hello John!

total = add(10, 20)
print(total)                    # 30

result = increment(10)
print(result)                   # 11 
```

## While Loop

```python
i = 1                    # Start
while i <= 10:           # Stop when i > 10
    print(i)
    i = i + 1            # Step
```

## For Loop

```python
for i in range(1, 11, 1):     # Start -> 1, Stop -> 11, Step -> 1
    print(i)
```

## List 

- Lists are non-primitive data type to hold multiple items.
- Can contain any types and number of items
- Can have duplicates
- Mutable - Can modify values
- Allows zero based index read and write

### List Operations

```python
numbers = [10, 30, 20, 40]

numbers.append(50)         # [10, 30, 20, 40, 50]
numbers.insert(1, 15)      # [10, 15, 30, 20, 40, 50]
numbers.extend([60, 70])   # [10, 15, 30, 20, 40, 50, 60, 70]

numbers.pop()              # removes 70
numbers.pop(2)             # removes 30

numbers.clear()            # []

nums = [4, 1, 3, 2]
nums.sort()                # [1, 2, 3, 4]
nums.reverse()             # [4, 3, 2, 1]
```

### List Slicing

```python
numbers = [10, 20, 30, 40, 50, 60, 70, 80]

numbers[0]        # 10
numbers[-1]       # 80
numbers[2:5:1]    # [30, 40, 50]
numbers[:4]       # [10, 20, 30, 40]
numbers[3:]       # [40, 50, 60, 70, 80]
numbers[::-1]     # [80, 70, 60, 50, 40, 30, 20, 10]  reverse
```

### List Comprehension

```python
numbers = [1, 2, 3, 4, 5]
print(numbers)                      # [1, 2, 3, 4, 5]

square = [x**2 for x in numbers]
print(square)                       # [1, 4, 9, 16, 25]
```

## Tuples

- Immutable, can not modify after creation
- Faster than list

```python
# Creating a tuple
colors = ("red", "green", "blue", "yellow")

print(colors)          # ('red', 'green', 'blue', 'yellow')
print(type(colors))    # <class 'tuple'>
```

## Set

- Can not have duplicates
- Mutable

```python
nums = {1, 2, 3, 4, 5}

nums.add(6)            # Add single item
nums.update([7, 8, 9]) # Add multiple items

nums.remove(3)         # Remove item (error if not found)
nums.discard(10)       # Remove item (no error if not found)

print(len(nums))       # 8
```

## Dictionary

- Key, Value Pairs
- Commonly used as look-up table

```python
student = {
    "name": "John",
    "age": 20,
    "grade": "A",
    "city": "Chennai"
}

print(student)
print(student["name"])       # John
print(student.get("age"))    # 20

student["age"] = 21          # Update value
student["country"] = "India" # Add new key-value

print(student.keys())      # ['name', 'age', 'grade', 'city', 'country']
print(student.values())    # ['John', 21, 'A', 'Chennai', 'India']
print(student.items())     # [('name', 'John'), ...]

del student["city"]        # Delete a key
student.pop("grade")       # Remove and return value
student.clear()            # Remove all items
```

## Exception Handling

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")

try:
    x = "10"
    y = "ABC"

    result = int(x) / int(y)
except ValueError:
    print("Invalid input, can not convert to int")
finally:
    print("Clean up resources in finally")
```

## File Handling

### Read Mode

- throws error when file not found

```python
file = open("Quotes.txt", "r")      # r - Read
all_string = file.read()
one_line   = file.readline()
all_lines  = file.readlines()
file.close()
```

### Write Mode

- Create file when not present
- Caution overwrites when file already exists

```python
file = open("Quotes.txt", "w")      # w - Write
file.write("Hello from python")
file.writelines(["First Line\n", "Second Line\n"])
file.close()
```

### Append Mode

- Create file when not present
- Appends to existing file.

```python
file = open("Quotes.txt", "a")      # a - append
file.write("Hello from python")
file.writelines(["First Line\n", "Second Line\n"])
file.close()
```

## Common Built-in Functions

len(), sum(), min(), max(), sorted(), type(str), dir(list)


<template id="copy-icon-template">
    <div style="width: 16px; height: 16px; border-radius: 5px; position: absolute; right: 10px; top: 10px; padding: 10px;
        border-radius: 5px;" onmouseenter="this.style.background='#715A5A'"
        onmouseleave="this.style.background='transparent'" onmousedown="this.style.background='black'"
        onmouseup="this.style.background='transparent'" onclick="copy(this)">

        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" fill="white">
            <path
                d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z">
            </path>
            <path
                d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z">
            </path>
        </svg>

    </div>
</template>

<script>

    copy_template = document.getElementById("copy-icon-template")
    codes = document.getElementsByTagName("code")

    for (let code of codes) {
        parent = code.parentNode.parentNode
        parent.style.position = "relative"
        el_copy = copy_template.content.cloneNode(true)
        parent.appendChild(el_copy)
    }

    function copy(e) {
        navigator.clipboard.writeText(e.parentNode.firstElementChild.textContent)
    }

</script>

