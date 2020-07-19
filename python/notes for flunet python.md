immutable: *number*, *string*, *tuple*, *bytes* 
mutable: *list*, *dict*, *set*, *byte array*
sequence: list, string

string vs. bytes vs. byte array

In each iteration of `for i in a:`, *i* get a copy of the current element
* modifying *i* doesn't affect *a*, i.e. *i* is not a lvalue reference of *a[]*
* use`a[:]` as a copy of *a* if you need to modify the sequence

default argument is evaluated only once at the point of function definition in the defining scope.

set may contain duplicate elements while dict may not.

Note that the current implementation only supports function attributes on user-defined functions. Function attributes on built-in functions may be supported in the future.
