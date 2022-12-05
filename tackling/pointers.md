Pointers are often introduced with the uninstinctive syntax of C.
Many times have I seen my peers struggle on this syntax.

I believe pointers are not conceptually that difficult to understand, but current curriculum lack two things: abstraction and visualization.

```c
// similar syntaxes yet different interpretations in C
int x = 5;
int * p = &x; // p is a pointer on x. Its value is the address where x is stored.
int * const pc = &x; // a constant pointer through which x can be modified
int const * x = // a modifiable pointer through which x cannot be modified
```

Moreover, the pointers while semantically very different to the variables, use nearly the same syntax. To the beginner, a simple star `*` suffices not describe the particularity of pointers, and only seems like a fancy thing some '72 nerds came with.

```c
int x = y;
int x = &y; // warning on gcc, but will compile
int *p = y; // here y is considered a pointer
int *p = &y; // here y is considered an int
```


## Solution

Pointers, references, variables are 3 different entities, each with their respective syntax.

**pointers**

All pointers are the same size in memory (size of the adressing), hence they only need one keyword, `ptr` (no `int *, void *, char *`)

`ptr p to x` p contains the adress of x, dereferencing p will automatically give a value of x's type` 

``