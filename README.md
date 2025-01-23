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

