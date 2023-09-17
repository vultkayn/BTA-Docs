---
title: Typing
permalink: /common/typing
---

BTA's type system is mostly static.
A declaration's type can be implicitly declared, and the interpreter
will deduce its types upon a first definition.

However, once a type has been defined for a declaration,
it cannot be changed.

```
stmt: var_decl | VAR_IDENTIFIER BIN_OP '=' expr
```

## Built in types

### Characters

char, string


### Logical

bool, trool

```
boolean: "true" | "false" | "not" boolean
 | boolean ("or" | "and") boolean
```

```
boolean: "true" | "false" | "unk"
```

### Integers

byte, i16, i32, i64, u16, u32, u64, isize, usize

### Floating point

f32, f64

### Complex type

Pairs of the above

### Array

### Union

## Dynamic possibilities


## Type qualifiers

- **Qualification syntax**

Qualifiers should not lead to confusion with types whatsoever.
Therefore, a syntaxic distinction might be welcomed to help distinguish between the two semantics.

Thereby is proposed the following construct:

```
ALPHA: [a-zA-Z_]
NUMBER: [0-9]+[.e]?[0-9]+
VAR_IDENTIFIER: ALPHA (ALPHA | NUMBER)*
var_decl: "let" type qualifiers_list VAR_IDENTIFIER ['=' expr] ';'
qualifiers_list: type_qualifier*

type_qualifier: "mut"
type:
```

<u>Example</u>

```
int{mut, volatile} x;
ptr{mut} p to y;
```

## Type Casting

Casting in C is not always clear, as the precedence of operators can confuse the learner.

Take for instance the following casts

```c
(int *) a[2]; // 1. Array a is first indexed, and that value is then casted
(int *) (a[2]); // 2. equivalent to 1
((int *) a)[2]; // 3. Array is first casted to int*, before taking *(a + 2*sizeof(int))
```

If already mistakes are sprouting from such a simple example, what about a multi-dimensional array ? or a multi-level pointer ?
The syntax of the casts are not that trivial in C, for those who are not naturally inclined to check the operator precedence in the standard.

```
cast_expr: expr "as" TYPE_IDENTIFIER
```

### Considerations

- **Constness**

Constness of an object if the default behavior. Mutability should be an explicit property.


- **Deduction of a dynamic variable implicit type at initialization from an explicitly-typed one**