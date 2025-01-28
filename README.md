# python_guides

### Installation
- https://www.python.org/
### Verify
- python --version

> [!NOTE]
> It explains the process of compiling Python code into bytecode and how the Python Virtual Machine (PVM) executes it.

![Alt text](https://res.cloudinary.com/dnknslaku/image/upload/v1737625833/1_c70hbo.png)

### Python Shall
> open terminal
```python
PS C:\Users\siddh\Downloads\python> PYTHON
>>> import os
>>> os.getcwd()
  'C:\\Users\\siddh\\Downloads\\python'
```
### Python Memory
![Alt text](https://res.cloudinary.com/dnknslaku/image/upload/w_500/v1737627260/Screenshot_105_ectjl7.png)

### Mutable and Immutable in Python
![Alt text](https://res.cloudinary.com/dnknslaku/image/upload/v1737628228/mutable-and-immutable-in-python_rzz8jy.png)
```python
PS C:\Users\siddh\Downloads\python> python
Python 3.12.3
>>> l1 = [1,2,3]
>>> l2 = l1
>>> l1
[1, 2, 3]
>>> l2
[1, 2, 3]
>>> l2[0] = 55
>>> l1
[55, 2, 3]
>>> l2
[55, 2, 3]

>>> p1 = [4,5,6]
>>> p2 = p1
>>> p1
[4, 5, 6]
>>> p2
[4, 5, 6]
>>> p1 = [4,5,6]
>>> p1[0] = 99
>>> p1
[99, 5, 6]
>>> p2
[4, 5, 6]
```
## NUMBERS IN PYTHON
```python
>>> 55 + 2.53
57.53
>>> "sidd" + 3
TypeError: can only concatenate str (not "int") to str
>>>
>>> int(2.53)
2
>>> float(55)
55.0
>>>
```
```python
>>> x = 1
>>> y = 2
>>> z = 3
>>> x,y,z
(1, 2, 3)
>>> x<y<z
True
>>> x < y and y < z
True
>>> 1 == 2 < 3
False
>>> 1 == 2 and 2 < 3
False
```
```python
>>> import math
>>> math.floor(3.7)  # closest bottom value
3
>>> math.trunc(2.8)  # towards zero 
2
```
```python
>>> (2+1j)*3
(6+3j)
```
```python
>>> 0o20    # octal   oct(16)
16
>>> 0xFF    # hexal   hex(255)
255
>>> 0b1000  # binary  bin(8)
8
>>> int("64",8) # convert in octal
52
```
```python
>>> import random
>>> random.random()
0.6036513999382547
>>> random.randint(1,100)
6
>>> random.choice(list)
>>> random.shuffle(list)
```
```python
>>> 0.1+0.1+0.1-0.3
5.551115123125783e-17
>>> (0.1+0.1+0.1)-0.3
5.551115123125783e-17

>>> from decimal import Decimal        # decimal context manager
>>> Decimal('0.1')+Decimal('0.1')+Decimal('0.1')
Decimal('0.3')

>>> from fractions import Fraction
```
```python
>>> setone = {1,2,3,4}
>>> & -> intersection
>>> | -> union
>>> setone - {1,2,3,4}
set()
```
## STRINGS IN PYTHON
1.) String Declaration
```python
name = "Siddharth"
repo_count = 50
print(f"Hello, my name is {name} and my repo count is {repo_count}") 

# Template Literals
- ✅ Using f-string (f"{} syntax) – Recommended          print(f"My name is {name} and I am {age} years old.")  
- ❌ Using .format() Method (Older Method)               print("My name is {} and I am {} years old.".format(name, age))
- ❌ Using % Formatting (Outdated in Modern Python)      print("My name is %s and I am %d years old." % (name, age))



You can directly perform calculations inside {} in an f-string:
a = 5
b = 10
print(f"Sum of {a} and {b} is {a + b}")
```



