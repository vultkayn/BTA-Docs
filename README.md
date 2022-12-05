# BTA \[beta version]

An enthusiastic attempt to develop a language to teach core programming concepts, without taking people for betas.

### What's currently done 

Learning tools are few and far between, and so often either too narrow-focused (OOP with ), or too shallow (Scratch). Python was often introduced as a learning language, as its syntax is easy to learn, the interpreter is highly permissive and the dynamic typing greatly takes a heavy weight off the beginner.
However, this does not help the programmer in the long term, as the learner won't have the opportunity to meet their first SEGFAULT, neither will they learn anything about the lower-level mecanism, such as memory management.

In multiple curriculum, Python is used as an introduction to procedural programmation and to algorithmic, to later fall back onto a more 'demanding' language, such as C or C++, to introduce memory management.

A language that should not be as laid-back as Python is while not having the syntaxic difficulties of Rust, nor the intricacies of C++.


### What's BTA is aiming for

Not intended to be that great performance-wise (do not use this in production).
Simply a language for learning purposes, packaged with its own interpreter (written in RUST ? =))

BTA is aiming to accompany the student through a whole diversity of concepts, such as:
- memory management (malloc/free)
- pointers and references, no untracked dangling pointers
- types awareness (and casting)
- types common qualifiers, such as constness
- dynamic typing on explicit demand.
- stack frames and scopes
- garbage collection
- debugging
- function overloading
- arrays and vectors
- (maybe oop ?)


## Core functionalities

- Interpreted language with garbage collection
- All cast must be explicit
- Lightweight syntax
- Static typing by default, but a variable can be dynamic if requested.
- Variables, scopes can be tagged as 'not garbage collected', thus manually managed.
- Any memory leak is to be reported to the user, with a helpful explanation as to how and why this happened
- No `undefined` or `null` variables.
- Distinction between parameters `by value` and `by reference`
- Built-in support of smart pointers, with a redesigned syntax.
- Built-in support of `key-associative` and `index-associative` collections
- Built-in visualisation of memory leak tracing, function call graph, and abstraction of the stack and heap.
- Strict 'compiling', all warnings are errors. To the beginner, warnings are just noisy, easy-to-ignore yellow lines that sometimes appear for no apparent reason.
- Enforce the programmer to abide by their coding style. `style: snake_case, camelCase or PascalCase`
- Built-in unitary testing ?