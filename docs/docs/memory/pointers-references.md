---
title: Pointers & References
permalink: /docs/memory/pointers
---

# Pointers & References

## Pointers

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

### BTA's way

* A pointer cannot points to an immutable variable.
* A pointer can be reassigned as long as its type is preserved. Otherwise, an explicit cast is mandatory.
* Syntax `ptr2 ppx to px`, `ptr3 pppx to ppx` is considered as a way to explicitly highlight higher level pointers.
* *Consideration* Should a pointer always be mutable so that `const` holds no meaning either? (in opposition to references)

### Operations on pointers

All pointers are the same size in memory (size of the adressing), hence they only need one keyword, `ptr` (no `int *, void *, char *`).

* Initialize with a mutable variable's address

`ptr px to x` px contains the address of x, dereferencing px will automatically give a value of x's type.

> The right-hand lvalue on a pointer assignment must a mutable

* Initialize by copying another pointer

`ptr p1 := px` p1 is a copy of pointer px, effectively copying its underlying structure. Dereferencing p1 will effectively be as dereferencing px. However, if p1 is later reassigned, then px won't be changed.

* Pointer-declaration is initialization

A pointer must be explicitly attributed a value upon declaration, it cannot be delayed. If you want to attribute it a dummy value, you should assign it `nullptr`.

* Pointer assignment

`p1 := px`. p1 now is a copy of px.
`p1 to y`. p1 now contains the address of y.

* Pointer dereferencement

`ptr p to x`. p holds the memory address of x
`p` is an expression yielding the address of x.
`@p` is an expression yielding the value of x

### Pointer arithmetic

TBD

## References

* A reference cannot be reassigned
* Qualifying a reference as `const` holds no meaning (since it cannot be reassigned).
* A reference can be directly used as the object it aliases.
* A reference cannot references an immutable variable.
* A reference is guaranteed to never outlast the object it aliases.
* No equivalent of `nullptr` for references. A reference **must** alias something.

### Operations on references

* Initialize as an alias for a mutable lvalue

`ref rx as x`. Under the hood, rx holds the address of x. However, such consideration are obfuscated from the user, which uses `rx` exactly as they would use `x`.


* Initializing by copying another reference is not possible

`ref r1 := rx` is not an actual thing. What would be the point ? You already have rx as a reference onto x. Just nails its name right the first time already.

> **However**, a reference can be given to a function taking a reference as a parameter. In this particular context, an implicit copy is performed between two references. What's  really forbidden is an explicit copy from the user, using the assignment operator.
{: .notice--warning}

* Reference aliasing

`ref rx as x`

After initialization, a reference is in all ways a perfect alias for a variable. Every operation `x` could possibly be subjected to is also a valid operation for `rx`, and will yield a perfectly identical result. *With a slight overhead for the actual cost of derefencing x*

For instance, `rx := 5` is semantically perfectly identical to `x := 5`.

## Vues

A Vue (view in French, translated to get a 3 characters word) is a pointer over any resource, but with the guarantee of never violating any part of its contract. 

* A vue cannot be dereferenced
* Any method not qualified as const cannot be called through a vue.
* A vue can be taken over any immutable or mutable resources.

## Alternatives

`const` qualifier could be added to the above objects, such as `ptr px to const x` and `ref rx to const x` behave like a Vue, all the while retaining their particularities (e.g. such `ref` would only allow read-only operations through it).
With the addition of a `const` qualifier, those objects could be initialized over immutable resources, considering they won't violate its invariants through dereferencement. 