
## Common libraries
math, random, re, time, timeit, profile, struct

## Common builtin functions
len, range, sum, map, filter, reduce, zip, sorted, isinstance, type, copy
## 编码
python使用unicode编码, 字符串以unicode储存在内存中. python区分字符串string和字节串bytes.

```bash
>>> b'ABC'.decode('ascii')
'ABC'
>>> b'\xe4\xb8\xad\xe6\x96\x87'.decode('utf-8')
'中文'
```

### Types Classification

* immutable: number, string, tuple
* mutable: list, dict, class-object

Function arguments are passed by values: immutable objects are copied by value, while mutable objects are copied by aliasing.

classes themselves are objects.

### Iterable, Iterator, Generator

* Iterable: implementing iter() to return an iterator.
* Iterator: implementing next() and using StopIteration to indicate the end of iteration.
* Generator: a function returning an iterator.

### Slicing
In s[i:j:k], if `i` or `j` is negative, the index is relative to the end of sequence `s`: `len(s) + i` or `len(s) + j` is substituted. But note that `-0` is still `0`.
```python
>>> s = "ab\\cdefg"
>>> s[::-1] # In s[a:b:c], c must be nonzero
'gfedc\\ba'
>>> s[-10:100]
'ab\\cdefg'
>>> len(s)
8
>>> s[-9:100:2]
'a\\df'
>>> s[1:-0:1]
''
>>> s[1:-1:1]
'b\\cdef'
```

### Functions
```python=
i = 5
def f(a, L=[i]):
    L.append(a)
    return L
i = 6
print(f(1)) #[5, 1]
print(f(2)) #[5, 1, 2]
print(f(3)) #[5, 1, 2, 3]
```
Each call creates a scope object, in which there is a local `L` pointing to the `L` in the function object `f`. So each call of `L.append(a)` change the `L` in `f`. Compare with the following
```python=
i = 5
def f(a, L=[i]):
    L = L + [a]
    return L
i = 6
print(f(1)) #[5 1]
print(f(2)) #[5 2]
print(f(3)) #[5 3]
```

### Dictionary
Tuples can be used as keys if they contain only strings, numbers, or tuples; if a tuple contains any mutable object either directly or indirectly, it cannot be used as a key.

## Module
A program doesn’t run any faster when it is read from a .pyc file than when it is read from a .py file; the only thing that’s faster about .pyc files is the speed with which they are loaded.

## Resources
[python zip](https://realpython.com/python-zip-function/)