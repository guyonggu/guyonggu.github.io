### Numbers
```python=
>>> -3//2
-2
>>> _ ** 2
4
```
### Strings
```python=
>>> s = "ab\\cdefg"
>>> s[::-1] # In s[a:b:c], c must be nonzero
'gfedc\\ba'
>>> print(s[::-1])
gfedc\ba
>>> s[-10:100]
'ab\\cdefg'
>>> len(s)
8
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