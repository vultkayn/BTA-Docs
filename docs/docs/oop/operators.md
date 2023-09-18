For built-in operators, the syntax used by the operators on data
can be reused on the types preceded by impl to overload this operator behavior on these
types

# Unary operators

impl ++Type;
impl Type++;
impl -Type;
impl not Type;

# Binary operators

impl Type1 op Type2;

# Dereferencing

impl Type[];

# Cast

impl Type1 as Type2;

Traits can also be specified to target a set of types
having these traits.

