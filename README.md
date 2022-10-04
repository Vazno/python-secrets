# <p align="center">Python secrets</center>
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
---
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
