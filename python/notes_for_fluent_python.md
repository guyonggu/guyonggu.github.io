One of the best qualities of Python is its consistency.

*dunder method*: `__getitem__`, `__len__`

Unless your are doing a lot of metaprogramming, you should be implementing special methods more often than invoking them directly. The only special method that is frequently called by user code directly is `__init__`, to invoke the initializer of the superclass in your own `__init__` implementation.