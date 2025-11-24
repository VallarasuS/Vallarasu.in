---
layout: post
category: Python
---

#### Contents

1. [Interpreter](#interpreter)
1. [Compiler](#compiler)
1. [Setup](#setup)
1. [Keywords](#keywords)
1. [Variables and Data Types](#variables-and-data-types)
1. [Errors](#errors)
1. [Naming Convention](#naming-convention)
1. [Built-in Function](https://docs.python.org/3/library/functions.html)
1. [Operators](#operators)
1. [Conditional Statements](#conditional-statements)
1. [Python Exercises](./programming-excercises)
1. [References](#references)
1. [Git](#git)


- Created by 'Guido van Rossum' in december of 1989 over christmas holiday.

![Guido van Rossum](https://raw.githubusercontent.com/VallarasuS/Vallarasu.in/master/docs/_screenshots/guido_van_Rossum.webp)

- Python's name was inspired by 'Monty Python's Flying Circus'.
- Python is an interpreted language. Compiled to a byte-code but still interpreted at execution.
- A compiler translates program from one language into another, (byte-code in java).
- This machine code is then executed, with-out the need for the source.
- Byte-code being native to the hardware it runs gives it time/speed advantage.
- But an interpreter like its literal meaning, translates the program line by line at execution.
- Interpreted at executed at run time has it's advantages and dis-advantage.

### Interpreter
<p style="margin-left: 10px; font-style: italic">
    Imagine reding a book written in french without knowing it. 
    You choose someone who knows french to read and translate (interpret) in english for you.
    Every time you read this book, the interpreter helps you translate it for you.
    One down side is this interpreter may not match your reading speed as you do on your own.
</p>

### Compiler
<p style="margin-left: 10px; font-style: italic">
    Now imagine reading it with a compiler. 
    Compiler reads and translates whole book. 
    Writes an english version of the book for you.
    Now the upside of this method is, interpreter don't follow you everywhere. 
    And you can read the book as fast as you can.
</p>

## Setup

- Download & Install latest version from here [Python Release](https://www.python.org/downloads/windows/)
- Add installation dir to PATH environment variable.
- Download & Install VS Code from here [VS Code](https://code.visualstudio.com/download)
- Install Python extension from Marketplace [Python Extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
- Open Command Prompt / Terminal and type 'python' to verify installation.

## Keywords

to display list of keywords in python use the following statement

import keyword
keyword.kwlist

['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']

## Variables and Data Types

- Python Syntax
- Variables
- Data types
    - Numbers: int, float
    - Text: str
    - Boolean: bool
- IO Operations
    - input
    - print
- Type Conversion
    - int, float, str

## Errors
    - Syntax Errors
    - Runtime Errors
    - Semantic Errors

## Naming Convention
- can contain letters and digits,
- can start with a letter or underscore, 
- starting with _ meant for internal use,
- use lower case
- avoid using keywords
- use upper case for const

## Operators
- Arithmetic Operators
    - +, -, *, /, %, //, **
    - PEMDAS 
        - Parenthesis, 
        - Exponent, 
        - Multiplication,
        - Division, 
        - Addition, 
        - Subtraction

- Comparison Operators

    - gt, lt, ge, le, eq, not eq

- Logical Operators

    - and, or

- Membership Operators
- Identity Operators

## Conditional Statements

- if elseif else
- for in range
- while
- match case

## References

- [Docs - The Python Tutorial](https://docs.python.org/3/tutorial/index.html)
- [Book - How to Think Like a Computer Scientist](https://www.openbookproject.net/thinkcs/python/english3e/)
- [Docs - Git Setup](https://git-scm.com/book/ms/v2/Getting-Started-First-Time-Git-Setup)
- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)

## Git

```
    - git clone 'https://github.com/VallarasuS/Vallarasu.in.git'
    - git pull
    - git add *
    - git commit -m "Notes(Python): Day 001 - Data types & Variable"
    - git push origin main

```

![Git Mental Model](https://raw.githubusercontent.com/VallarasuS/Vallarasu.in/master/docs/_screenshots/git-mental-model.webp)