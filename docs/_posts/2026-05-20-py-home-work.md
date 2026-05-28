---
layout: post
category: Python
---

## Python Practice Problems

### If Else

1. Compute Indian income tax rate for given annual salary
1	a. [4-8 -> 5%, 8-12 -> 10%, 12-16 -> 15%, 16-20 -> 20%, 20-24 -> 25%, above 24 -> 30%]
1. Given a metal name (gold, silver, platinum), print their price
1. Given a number, if odd double it (2x), if even return same. 3 -> 6, 4 -> 4
1. Given two numbers find min
1. Given two number find max
1. Given number, print day of the week 1 -> Monday 7 -> Sunday
1. Given exam scores ex [50, 23, 36, 45, 30] check if user failed or passed an exam. Pass score 36
1. Given an number, print whether given number is positive, negative or zero
1. Given room temperature, print whether it is Normal, Hot or Cold
	1. 21-24 Normal
	1. Above 24 Hot
	1. Below 21 Cold
1. Given age check if user can vote. min age 18
1. Given age check if user can drive min age 18
1. Given mark check if user fail. pass mark 36
1. Given mark check if user scored centum (100)
1. Given body temperature check if user has fever (more than 100)
1. Given user name, password print 'success' if they match 'admin', '1234'
1. Given a number, print 'positive', 'negative' or 'zero'
1. Check if given number is divisible by 3 and 5
1. Check if a candidate is eligible to appear for a role with age limit 21-32
1. Given a day check if it falls on week end (sat/sun) 
1. Given a color name check if it is primary color (Red/Green/Blue)

# String

1. Find file type image.png, file.pdf, file.docx
1. Find position of given word
1. Reverse string
1. Parse csv ""

# Loop

1. Find total of numbers from 1 ... N
1. Print each character in a string
1. Count number of vowels (a,e,i,o,u) from given string
1. Reverse given string using while loop
1. Extract only numbers from given string
	a. ex: "abc122dkjf834"
1. Find total from csv data:
	a. ex: "John,45,23,76,87,98"
1. Print 1, 2, 3 … 10
1. Print 2, 4 ,6 … 20
1. Print  Table given a number 
	a. Ex: 2 -> 1x2, 2x2, 3x2 … 10x2
1. Find all odd numbers until given number
	a. Ex: 10 -> 1, 3, 5, 7, 9
1. Find all numbers divisible by 3 until given number
	a. Ex: 10 -> 3,  6, 9
1. Find all numbers divisible by 3 and 5 until given number
	a. Ex: 50 -> 15, 30, 45
1. Sum of natural numbers until given number
	a. Ex: input:  4  ->  1 + 2 + 3 + 4 ->  10
1. Find factorial of given number
	a. Ex: input 5 ->  5 * 4 * 3 * 2 * 1 -> 120

# Revision:

1. Reverse a string using index:

```python
    data = "hello world"
  
    start = 0
    stop = len(data)
    step = 1

    for i in range(0, len(data), 1):
        print(data[i])
```

1. Sum of square of even numbers upto N
1. Find total, pass / fail, average, rank
```python
	data = "John,30,40,50,60\nDave,10,20,30,45,50\nAdam,40,95,87,67,50"
```
  