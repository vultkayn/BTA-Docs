# Static typing (mostly)

BTA's types are 

# Dynamic possibilities


# Built in types




# Type Casting

Casting in C is not always clear, as the precedence of operators can confuse the learner.

Take for instance the following casts
```c
(int *) a[2]; // 1. Array a is first indexed, and that value is then casted
(int *) (a[2]); // 2. equivalent to 1
((int *) a)[2]; // 3. Array is first casted to int*, before taking *(a + 2*sizeof(int))
```

If already mistakes are sprouting from such a simple example, what about a multi-dimensional array ? or a multi-level pointer ?
The syntax of the casts are not that trivial in C, for those who are not naturally inclined to check the operator precedence in the standard.

# Type qualifiers

### Considerations

- **Default object mutability**: Should the constness of an object be expected by default, hence mutability be an explicit request from the user (as in Rust) ? Or should the default behavior be that of C ?

- **Deduction of a dynamic variable implicit type at initialization from an explicitly-typed one**