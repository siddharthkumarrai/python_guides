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
```python
game_name = "pubg"
print(game_name[0])  # Output: 'p'
print(dir(game_name))  # Shows available methods in Python
```
2.) String Properties and Methods 
```python
str1 = "Hello World"
print(len(str1))  # Output: 11

print(str1[1])               # Output: 'e'
print(str1.index('l'))        # Output: 2
print(str1[1:4])              # Output: 'ell' (Slicing)
print(str1.upper())           # Output: 'HELLO WORLD'
print(str1.lower())           # Output: 'hello world'
print(str1.replace('H', 'J')) # Output: 'Jello World'
print(str1.split(' '))        # Output: ['Hello', 'World']
print(str1.strip())           # Removes leading/trailing spaces
```
- String are Immutable:
```python
str1[0] = "J"  # Error (Strings in Python are immutable)
print(str1)     # Output: 'Hello World'
```

## LISTS IN PYTHON
- Creating Lists
```python
my_list = [0, 1, 23, True, "sidd", None]  
my_list2 = list((0, 1, 2, 3, 4, 5))  
print(my_list2)  # Output: [0, 1, 2, 3, 4, 5]
```
- Adding/Removing Elements (Mutation Method)
```python
my_list2.append(6)       # [0, 1, 2, 3, 4, 5, 6]
my_list2.pop()           # [0, 1, 2, 3, 4, 5]
my_list2.insert(0, 9)    # [9, 0, 1, 2, 3, 4, 5]
my_list2.pop(0)          # [0, 1, 2, 3, 4, 5]
```
- Accessing Elements
```python
my_list = ["sidd","raj","sagar","sidd"]

print(my_list.index("raj"))      # Output: 1 (not found -> raises ValueError)
print(my_list.count("sidd"))     # Output: 2
print("sagar" in my_list)        # Output: True        
```
- Manipulating Elements
```python
my_list2 = [0, 1, 2, 3, 4, 5]
print(my_list2)  # [0, 1, 2, 3, 4, 5]

# Splicing (Removing & Adding Elements)
my_list2[1:3] = [4]   
print(my_list2)  # Output: [0, 4, 3, 4, 5]

# Other Operations
print(list(reversed([1, 2, 3])))        # Output: [3, 2, 1]
print(sorted([3, 2, 1]))                # Output: [1, 2, 3]
print([1, 2, 3] * 2)                    # Output: [1, 2, 3, 1, 2, 3]
print([1, 2, 3, 4, 5].copy())           # Output: [1, 2, 3, 4, 5]
```
- String Conversion
```python
print("-".join(map(str, my_list2)))  # Output: "0-4-3-4-5"
```
- Iteration
```python
my_list2 = [0, 1, 2, 3, 4, 5]
print(my_list2)  # [0, 1, 2, 3, 4, 5]

for element in my_list2:
    print(element)  # Output: 0 1 2 3 4 5

print([element * 2 for element in my_list2])  # Output: [0, 2, 4, 6, 8, 10]
print([element for element in my_list2 if element > 1])  # Output: [2, 3, 4, 5]

from functools import reduce
print(reduce(lambda acc, x: acc + x, my_list2))  # Output: 15
```
- Merge List in Python
```python
marvel_heros = ["thor", "ironman", "spider"]
dc_heros = ["super", "flash", "batman"]

# Method 1: Using + operator
all_heros = marvel_heros + dc_heros
print(all_heros)  
# Output: ['thor', 'ironman', 'spider', 'super', 'flash', 'batman']

# Method 2: Using extend() (Modifies the original list)
marvel_heros.extend(dc_heros)
print(marvel_heros)  
# Output: ['thor', 'ironman', 'spider', 'super', 'flash', 'batman']

# Method 3: Using unpacking (Recommended for better readability)
all_new_heros = [*marvel_heros, *dc_heros]
print(all_new_heros)  
# Output: ['thor', 'ironman', 'spider', 'super', 'flash', 'batman']
```
- List Comprehension
```python
squares = [x**2 for x in range(1, 6)]
print(squares)  # Output: [1, 4, 9, 16, 25]

even_numbers = [x for x in range(10) if x % 2 == 0]
print(even_numbers)  # Output: [0, 2, 4, 6, 8]
```
## Dictionary
1.)  Creating Objects (Dictionaries)
   - Using  { }  (Dictionary Literal)
```python
user = {
    "name": "Siddharth",
    "age": 19,
    "location": "Delhi",
    "email": "sidd@gmail.com",
    "is_logged_in": False,
    "last_login_days": ["Monday", "Saturday"],
    "full Name": "Siddharth Kumar Rai"
}
```
  - Using dict ( )  Constructor
```python
user = dict(name="Siddharth", age=19, location="Delhi")
```
2.)  Accessing Values
```python
print(user["email"])          # sidd@gmail.com
print(user.get("email"))      # sidd@gmail.com
print(user["full Name"])      # Siddharth Kumar Rai
print(user.get("username", "Not Found"))  # Default value if key is missing
```
3.)  Adding & Modifying Values
```python
user["profession"] = "Developer"
user["age"] = 20
```
4.)  Checking if a Key Exists
```python
print("email" in user)  # True
print(user.keys())      # dict_keys(['name', 'age', 'location', 'email', 'is_logged_in', 'last_login_days', 'full Name'])
print(user.values())    # dict_values(['Siddharth', 19, 'Delhi', 'sidd@gmail.com', False, ['Monday', 'Saturday'], 'Siddharth Kumar Rai'])
print(user.items())     # [('name', 'Siddharth'), ('age', 19), ...]
```
5.)  Deleting a Key
```python
del user["email"]
user.pop("location")
```
6.)  Merging Dictionaries
```python
obj1 = {1: "a", 2: "b"}
obj2 = {3: "c", 4: "d"}

obj3 = {**obj1, **obj2}  # {1: 'a', 2: 'b', 3: 'c', 4: 'd'}
obj4 = obj1 | obj2       # Python 3.9+ syntax for merging
```
7.)  Dictionary Comprehension
```python
squared = {x: x**2 for x in range(5)}  # {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```
8.)  Looping Through Dictionary
```python
user = {
    "name": "Siddharth",
    "age": 19,
    "location": "Delhi",
    "email": "sidd@gmail.com"
}

# Loop through keys
for key in user:
    print(key, ":", user[key])

# Loop through values
for value in user.values():
    print(value)

# Loop through key-value pairs
for key, value in user.items():
    print(f"{key}: {value}")
```
##  TUPLE
1.) Tuple Creation
```python
# Empty tuple
empty_tuple = ()

# Tuple with values
my_tuple = (1, 2, 3, "sidd", True, None)

# Tuple without parentheses (valid but not recommended)
my_tuple2 = 1, 2, 3  

# Single element tuple (comma जरूरी है)
single_element_tuple = (5,)  
print(type(single_element_tuple))  # Output: <class 'tuple'>

# Using tuple() constructor
my_tuple3 = tuple([1, 2, 3, 4])  
print(my_tuple3)  # Output: (1, 2, 3, 4)
```
> [!WARNING]
> () के बिना tuple बन सकता है, लेकिन readability के लिए parentheses इस्तेमाल करना बेहतर होता है।

> Single-element tuple में , लगाना जरूरी है, वरना ये integer या string माना जाएगा।




