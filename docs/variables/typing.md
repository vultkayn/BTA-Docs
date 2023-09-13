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

- **Qualification syntax**

Qualifiers should not lead to confusion with types whatsoever.
Therefore, a syntaxic distinction might be welcomed to help distinguish between the two semantics.

Thereby is proposed the following construct:

**DECL** $\rightarrow$ **TYPE** **QUALIFIERS_LIST** *name* [ **$:=$** *value* ]
**QUALIFIERS_LIST** $\rightarrow$ **{** **QUALIFIER** **,** **}** | $\epsilon$

**QUALIFIER** $\rightarrow$ **mut** | **volatile**

<u>Example</u>

```
int{mut, volatile} x;
ptr{mut} p to y;
```


### Considerations

- **Constness**

Constness of an object if the default behavior. Mutability should be an explicit property.


- **Deduction of a dynamic variable implicit type at initialization from an explicitly-typed one**