## VISIBILITY

```antlr4
VISIB := public | private | protected
```

## Interface

An interface is a set of method declarations
and traits but don't have any concrete implementation.

**Grammar**

```antlr4
interface IDENTIFIER extends IDENTIFIER '{' DECL_LIST '}'
```

An interface is implemented with:

```antlr4
impl INTERFACE_IDENTIFIER for CLS_IDENTIFIER;
```

## Classes

```antlr4
RECORD_DECL := class IDENTIFIER inherit VISIB CLS_IDENTIFIER ('{' RECORD_BODY '}' | ';')

RECORD_BODY := (VISIB ':' DECL_LIST)+
```


## Methods

