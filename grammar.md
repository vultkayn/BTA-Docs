# Variable initialization

```antlr4
VAR_DECL := let IDENTIFIER ':' TYPE_QUALIFIERS TYPE_IDENTIFIER '=' EXPR ';'
TYPE_QUALIFIERS := [mut]
TYPE_IDENTIFIER := BUILTIN_TYPE | any | IDENTIFIER
```

# Variable assignment

`x = 5`

# Macros


```antlr4
MACRO_IDENTIFIER := '$' IDENTIFIER
```

**Examples**

- `$unreachable ()`: If control flow ever reach this point, then throw  
- $print
