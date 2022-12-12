# <p align="center">[Python](https://www.python.org/) secrets</center>
##### <p align="center">Did you know that...</center>

You can add separators in numbers, and it won't affect any behaviour:
```python
a = 1_000_000
print(a) # -> 1000000
```
Or you can use f-strings to create str numbers with separators:
```python
a = 1000000
print(f"{a:,}") # -> "1,000,000"
print(f"{a:_}") # -> "1_000_000"
```
-------------------------------------------
Python has easter eggs: (Try it, yourself.)
```python
import antigravity
import this
import __hello__
```
Braces won't be used as a part of indentation syntax:
```python
from __future__ import braces
```
```python
  File "c:\python-secrets\showcase.py", line 1
    from __future__ import braces
    ^
SyntaxError: not a chance
```
-------------------------------------------
Python has `pprint()` function, which you can use to print complex data structures in a human readable way.

##### `print()` -> Ususal boring print:
```python
{'widget': {'debug': 'on', 'window': {'title': 'Sample Konfabulator Widget', 'name': 'main_window', 'width': 500, 'height': 500}, 'image': {'src': 'Images/Sun.png', 'name': 'sun1', 'hOffset': 250, 'vOffset': 250, 'alignment': 'center'}, 'text': {'data': 'Click Here', 'size': 36, 'style': 'bold', 'name': 'text1', 'hOffset': 250, 'vOffset': 100, 'alignment': 'center', 'onMouseUp': 'sun1.opacity = (sun1.opacity / 100) * 90;'}}}
```

##### `pprint()` -> Pretified print, with indentation:
```python
from pprint import pprint
```
```python
{'widget': {'debug': 'on',
            'image': {'alignment': 'center',
                      'hOffset': 250,
                      'name': 'sun1',
                      'src': 'Images/Sun.png',
                      'vOffset': 250},
            'text': {'alignment': 'center',
                     'data': 'Click Here',
                     'hOffset': 250,
                     'name': 'text1',
                     'onMouseUp': 'sun1.opacity = (sun1.opacity / 100) * 90;',
                     'size': 36,
                     'style': 'bold',
                     'vOffset': 100},
            'window': {'height': 500,
                       'name': 'main_window',
                       'title': 'Sample Konfabulator Widget',
                       'width': 500}}}
```
###### Basically it works for every data structure including lists, tuples, etc.
-------------------------------------------
You can use `;` to put multiple statements in one line, like:
```python
print("The first") ; print("The second") ; print("The third")
a = 5 ; b = 10 ; c = 100
import datetime ; print("Hello, world!")
```
It even works with `for`, and `while loops`:
```python
for i in range(3): print('Check') ; print('This') ; print("Out")
```
```python
while True: print("123") ; print("456")
```
###### [Semicolons are end statements in C](https://www.geeksforgeeks.org/role-of-semicolon-in-various-programming-languages/).
* ###### The Semicolon tells that the current statement has been terminated and other statements following are new statements.
* ###### Usage of Semicolon in C will remove ambiguity and confusion while looking at the code.
* ###### They are not used in between the control flow statements but are used in separating the conditions in looping. 

-------------------------------------------
Python has the ability to use the [dis module](https://docs.python.org/3/library/dis.html) to disassemble bytecode. This allows you to see the low-level instructions that the Python interpreter uses to execute your code, which can be useful for debugging and performance optimization.

To use the dis module, you need to import it and then use the `dis()` function to disassemble a function or code block. For example:
```python
import dis

def add(a, b):
    return a + b

dis.dis(add)
```
```
  2           0 LOAD_FAST                0 (a)
              2 LOAD_FAST                1 (b)
              4 BINARY_ADD
              6 RETURN_VALUE
```
The first instruction, `LOAD_FAST 0`, loads the value of the a argument onto the stack. The second instruction, `LOAD_FAST 1`, loads the value of the b argument onto the stack. The third instruction, `BINARY_ADD`, pops the top two values from the stack, adds them together, and then pushes the result back onto the stack. Finally, the `RETURN_VALUE` instruction pops the top value from the stack and returns it as the result of the add() function.
#####
These low-level instructions show how the Python interpreter executes the `add()` function, but they are not intended to be read or understood by humans. Instead, they are used by the Python interpreter to quickly and efficiently execute the code.

-------------------------------------------
Another rare feature of Python is the ability to use the `gc` module to control the garbage collector.

```py
import gc

# Enable the garbage collector
gc.enable()

# Create a list of objects
objects = [
    [],
    {},
    "Hello, world!",
    123,
    b"\x01\x02\x03",
    set(),
    (1, 2, 3),
]

# Print the number of objects
print(f"Number of objects: {len(gc.get_objects())}")

# Collect unused objects and reclaim memory
gc.collect()

# Print the number of objects again
print(f"Number of objects after garbage collection: {len(gc.get_objects())}")
```

-------------------------------------------

[![Unlicense](https://img.shields.io/badge/License-Unlicense-blue.svg)](https://unlicense.org/) [![Open Source? Yes!](https://badgen.net/badge/Open%20Source%20%3F/Yes%21/blue?icon=github)](https://opensource.org/)
