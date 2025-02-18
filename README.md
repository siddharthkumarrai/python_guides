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
> ( ) के बिना tuple बन सकता है, लेकिन readability के लिए parentheses इस्तेमाल करना बेहतर होता है। <br> <br>
> Single-element tuple में , लगाना जरूरी है, वरना ये integer या string माना जाएगा।

2️.)  Accessing Elements (Indexing & Slicing)
```python
my_tuple = (10, 20, 30, 40, 50)

print(my_tuple[1])   # Output: 20  (0-based indexing)
print(my_tuple[-1])  # Output: 50  (Last element)

# Slicing (start:end:step)
print(my_tuple[1:4])    # Output: (20, 30, 40)
print(my_tuple[:3])     # Output: (10, 20, 30)
print(my_tuple[::2])    # Output: (10, 30, 50)  (हर दूसरा element)
print(my_tuple[::-1])   # Output: (50, 40, 30, 20, 10)  (Reverse tuple)
```
3.) Tuple Methods
```python
my_tuple = (1, 2, 3, 4, 2, 5, 2)

print(my_tuple.count(2))    # Output: 3 (2 कितनी बार आया)
print(my_tuple.index(3))    # Output: 2 (3 का index)
```
4.) Tuple Packing & Unpacking
```python
# Packing (एक tuple में multiple values रखना)
packed_tuple = ("sidd", 21, "India")

# Unpacking (tuple values को अलग-अलग variables में डालना)
name, age, country = packed_tuple

print(name)     # Output: sidd
print(age)      # Output: 21
print(country)  # Output: India
```
> [!WARNING]
> ⚠ Note: Unpacking करते समय values और variables की count match होनी चाहिए, नहीं तो error आएगा।

5.) Merging Tuples (Concatenation & Repetition)
```python
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)

# Concatenation (जोड़ना)
merged_tuple = tuple1 + tuple2
print(merged_tuple)  # Output: (1, 2, 3, 4, 5, 6)

# Repetition (एक tuple को multiple बार repeat करना)
repeated_tuple = tuple1 * 3
print(repeated_tuple)  # Output: (1, 2, 3, 1, 2, 3, 1, 2, 3)
```
6.) Converting Between List & Tuple
```python
# Tuple to List (Modification के लिए)
tuple1 = (1, 2, 3)
list1 = list(tuple1)  # Convert to list
list1.append(4)       # List को modify किया
tuple1 = tuple(list1)  # फिर से tuple में बदला
print(tuple1)  # Output: (1, 2, 3, 4)

# List to Tuple
list2 = [10, 20, 30]
tuple2 = tuple(list2)
print(tuple2)  # Output: (10, 20, 30)
```
7.) Checking If an Element Exists in a Tuple
```python
my_tuple = ("apple", "banana", "cherry")

print("banana" in my_tuple)  # Output: True
print("grape" in my_tuple)   # Output: False
```
8.)   Looping Over a Tuple
```python
fruits = ("apple", "banana", "cherry")

# For loop
for fruit in fruits:
    print(fruit)

output: apple
        banana
        cherry

# Using enumerate() (index + value)
for index, fruit in enumerate(fruits):
    print(f"Index {index}: {fruit}")

output: Index 0: apple
        Index 1: banana
        Index 2: cherry
```
9.) Finding Maximum, Minimum, and Sum in a Tuple
```python
numbers = (5, 2, 9, 1, 7)

print(max(numbers))  # Output: 9
print(min(numbers))  # Output: 1
print(sum(numbers))  # Output: 24
```
10.) Tuple as Dictionary Key (Immutable होने की वजह से Possible)
```python
# Tuples can be dictionary keys, unlike lists
locations = {
    (28.6139, 77.2090): "Delhi",
    (19.0760, 72.8777): "Mumbai"
}

print(locations[(28.6139, 77.2090)])  # Output: Delhi
```
11.) Checking if an Object is a Tuple
```python
my_tuple = (1, 2, 3)
print(isinstance(my_tuple, tuple))  # Output: True

my_list = [1, 2, 3]
print(isinstance(my_list, tuple))  # Output: False
```
## CONDITIONALS
```python
if age < 13 :
    print("you are chlid")
elif age < 19 :
    print("you are teenager")
elif age < 59 :
    print("you are adlult")
else:
    print("you are senior")
```
```python
price = 12 if age >= 18 else 8
```
```python
if (year % 400 == 0) or  (year % 4 == 0) and (year % 100 != 0):
    print("leap year")
```
## LOOPS
- for loop
```python
for i in range(0,n+1):
    print(i)
```
- while loop
```python
n = 3
fac = 1
while True:
    fac = fac * n
    n = n-1
    if n < 1:
        break
print(fac)
```
## behind the scenes in iterator (loops)
![Alt text](https://res.cloudinary.com/dnknslaku/image/upload/v1738851784/Screenshot_165_r9qhy8.png)
```python
>>> f = open("sidd.py")
>>> f.readline()
'import os\n'
```
```python
>>> f.__next__()
'print("siddharth")\n'
>>> f.__next__()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
StopIteration
>>>
```
```python
>>> for line in open("sidd.py").readlines():
...     print(line)
... 
import os
os.getcwd()
print("siddharth")
>>>
```
```python
>>> for line in open("sidd.py"):
...     print(line)
...
```
```python
>>> f = open("sidd.py")
>>> while True:
...     line = f.readline()
...     if not line: break
...     print(line)
... 
import os
os.getcwd()
print("siddharth")
>>>
```
```python
>>> myList = [1,2,3,4]
>>> L = iter(myList)
>>> L
<list_iterator object at 0x000001F85121BD00>
>>> L.__next__()
1
```
```python
>>> list = [1,2]
>>> i = iter(list)
>>> next(i)
1
```
> [!NOTE]
> IMPORTANT
```python
>>> f = open("sidd.py")
>>> iter(f) is f
True
>>> iter(f) is f.__iter__()
True
>>> list = [1,2]
>>> iter(list) is list     
False
```
## functions
```python
   def square(number){                //  number are parameter  (function defination)
        return number*number
   }

   sq = square(3)                     //  are argument  (function call)
   print(sq)                          //  output: 9
```
- Lambda Function
```python
    cube = lambda x: x**3

    print(cube(3))
```
- Multiple Argument (*args)
```python
    def sum_num(*args):
        print(sum(args))

    sum_num(1,2,3)                      // result: 5
```
- kwargs key,value arguments
```python
def kw_args(**kwargs):
    print(kwargs)                        // output: {'name': 'sidd', 'roll_no': 17}

kw_args(name = "sidd",roll_no = 17)
```
- Function with yield
```python
def print_even(limit):
    for i in range(2,limit+1,2):
        yield i
    
for num in print_even(10):
    print(i)
```
## OOP
- Basic Class and Object
  - Class Method and Self
```python
class Car:
    def __init__(self,brand,model):
        self.brand = brand
        self.model = model

    def full_name(self):
        return f"{self.brand} {self.model}"

car1 = Car("tata","safari")
print(car1.full_name)
```
- Inheritance
  - ElectricCar class that inherits from the Car class and has an additional attribute battery_size.
```python
class Electric_Car(Car):
    def __init__(self,brand,model,battery_size):
        super().__init__(brand,model)
        self.battery_size = battery_size

electric_car_one = Electric_Car("tesla","ev1","18KWH")
print(electric_car_one.battery_size)
```
- Encapsulation
  - Car class to encapsulate the brand attribute, making it private, and provide a getter method for it.
```python
class Car:
    def __init__(self,brand,model):
        self.__brand = brand
        self.model = model
    
    def get_brand(self):
        return self.__brand

electric_car_one = Car("tesla","ev1")
print(electric_car_one.get_brand())
```
-  Polymorphism
    - polymorphism by defining a method fuel_type in both Car and ElectricCar classes, but with different behaviors.
```python
class Car:
    def __init__(self,brand,model):
        self.__brand = brand
        self.model = model
    
    def fuel_type(self):
        return f"car fuel diseal and petrol"



class Electric_Car(Car):
    def __init__(self,brand,model,battery_size):
        super().__init__(brand,model)
        self.battery_size = battery_size
    
    def fuel_type(self):
        return f"car fuel Electric charges"

car_one = Car("tesla","ev1")
electric_car_one = Electric_Car("tesla","ev1","18KWH")

print(car_one.fuel_type())
print(electric_car_one.fuel_type())
```
- Class Variables
   - a class variable to Car that keeps track of the number of cars created.
```python
class Car:
    total_car = 0

    def __init__(self,brand,model):
        self.__brand = brand
        self.model = model
        Car.total_car += 1
    
    

class Electric_Car(Car):
    def __init__(self,brand,model,battery_size):
        super().__init__(brand,model)
        self.battery_size = battery_size


car_one = Car("tata","safari")
car_Two = Car("tata","eicher")
electric_car_one = Electric_Car("tesla","ev1","18KWH")


print(car_one.total_car)    # output:- 3
print(Car.total_car)        # output:- 3
```






