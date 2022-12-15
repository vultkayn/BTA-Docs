Operators can be overloaded.

# Expressions

## Unary arithmetic

## Unary bitwise operations

## Binary arithmetic operations




#  Operator Precedence



From top to bottom, highest precedence to lowest.

|Operator| Description|
| :---: | :---: |
|()| Parenthesing |
|f(...)| function call|
|a\[5], a\[5:], a.attribute |Indexing, slicing, attribute|
|**| Exponentiation|
|+x, -x, ~x| Unary arithmetic and bitwise operations|
|*, /, //| multiplication and division|
|%| Modulo|
|+, - | binary arithmetic operations|
|>>, << | bit shift (maybe same level as binary arithmetic ?)|
|&| bitwise AND|
|^| bitwise XOR|
| \| | bitwise OR|
| in, not in, is, is not, <br> <, >, <=, >=, ==, !=  | Comparison, identity, membership operators |
|not| Boolean (logical) not|
|and| Boolean (logical) and|
|or| Boolean (logical) or|

## Design issue

Should the precedence be identical to Python, since students are possibly used to it ? 

Or is it a false hope to expect that they know its mechanisms, therefore we should steer towards a simpler implementation ?
In such event, should the binary bitwise operations be reviewed to take a higher than or similar precedence to binary arithmetic operators ?


# Operator overloading

