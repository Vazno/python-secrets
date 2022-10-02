# <center>Python secrets</center>
##### <center>Did you know that...<center>
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