---
layout: post
category: Python
---

#### Contents

1. [Variables and Data Types](#variables-and-data-types)
1. [Input and Output](#input-and-output)
1. [Arithmetic Operators](#arithmetic-operators)
1. [Comparison Operators](#comparison-operators)
1. [Logical Operators](#logical-operators)
1. [Membership Operators](#membership-operators)
1. [If elif else](#if-elif-else)
1. [String Operations](#string-operations)
1. [While Loop](#while-loop)
1. [For Loop](#for-loop)
1. [List and Operations](#list-and-operations)
1. [Tuples](#tuples)
1. [Set](#set)
1. [Dictionary](#dictionary)


## Variables and Data Types

```python
name = "John"   # string  ->  str
age = 30        # number  ->  int
weight = 63.5   # number  ->  float
married = True  # Boolean -> bool
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
z = x + y   # addition -> 13
z = x - y   # subtraction -> 7
z = x * y   # multiplication -> 30
z = x / y   # true division -> 3.3333
z = x // y  # floor division -> 3
z = x ** y  # exponent -> 1000
z = x % y   # modulo division -> 1
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
result = (x > y) or (z < y)     # or   -> True (at least one condition true)
result = not (x > y)            # not  -> False (reverses the condition)
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

print(text.upper())          #   HELLO PYTHON WORLD!
print(text.lower())          #   hello python world!

print(text.strip())          # Hello Python World!
print(text.split())          # ['Hello', 'Python', 'World!']

fruits = ["apple", "banana", "cherry"]
print(", ".join(fruits))     # apple, banana, cherry

print("Python".find("th"))   # 2
print("Python".find("java")) # -1

name = "John"
print("Hello, {}".format(name))   # Hello, John
print(f"Hello, {name}!")          # Hello, John!
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
for i in range(1, 11):     # Start=1, Stop=10, Step=1
    print(i)
```

## List and Operations

```python
numbers = [10, 30, 20, 40]

numbers.append(50)         # [10, 30, 20, 40, 50]
numbers.insert(1, 15)   # [10, 15, 30, 20, 40, 50]
numbers.extend([60, 70])   # [10, 15, 30, 20, 40, 50, 60, 70]

numbers.pop()              # removes 70
numbers.pop(2)             # removes 30

numbers.clear()            # []

nums = [4, 1, 3, 2]
nums.sort()            # [1, 2, 3, 4]
nums.reverse()         # [4, 3, 2, 1]
```

List Slicing

```python
numbers = [10, 20, 30, 40, 50, 60, 70, 80]

numbers[0]        # 10
numbers[-1]       # 80
numbers[2:5:1]    # [30, 40, 50]
numbers[:4]       # [10, 20, 30, 40]
numbers[3:]       # [40, 50, 60, 70, 80]
numbers[::-1]     # [80, 70, 60, 50, 40, 30, 20, 10]  reverse
```

## Tuples

```python
# Creating a tuple
colors = ("red", "green", "blue", "yellow")

print(colors)          # ('red', 'green', 'blue', 'yellow')
print(type(colors))    # <class 'tuple'>
```

## Set

```python
nums = {1, 2, 3, 4, 5}

nums.add(6)            # Add single item
nums.update([7, 8, 9]) # Add multiple items

nums.remove(3)         # Remove item (error if not found)
nums.discard(10)       # Remove item (no error if not found)

print(len(nums))       # 8
```

## Dictionary

```python
student = {
    "name": "John",
    "age": 20,
    "grade": "A",
    "city": "New York"
}

print(student)
print(student["name"])     # John
print(student.get("age"))  # 20

student["age"] = 21        # Update value
student["country"] = "USA" # Add new key-value

print(student.keys())      # dict_keys(['name', 'age', 'grade', 'city', 'country'])
print(student.values())    # dict_values(['John', 21, 'A', 'New York', 'USA'])
print(student.items())     # dict_items([('name', 'John'), ...])

del student["city"]        # Delete a key
student.pop("grade")       # Remove and return value
student.clear()            # Remove all items
```