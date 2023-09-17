'''
MIT License

Copyright (c) 2022-2023 Benjamin Priour <priour.be@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
'''

# Standard library modules

## math

### Trigonometry

cos (f64 radians) -> f64;
cos (f32 radians) -> f32;
sin (f64 radians) -> f64;
sin (f32 radians) -> f32;
tan (f64 radians) -> f64;
tan (f32 radians) -> f32;

acos (f64 radians) -> f64;
acos (f32 radians) -> f32;
asin (f64 radians) -> f64;
asin (f32 radians) -> f32;
atan (f64 radians) -> f64;
atan (f32 radians) -> f32;
atan2 (f64 y, f64 x) -> f64;
atan2 (f32 y, f32 x) -> f32;

### Exponential and logarithmic

exp (f64 x) -> f64;
exp (f32 x) -> f32;
log (f64 x) -> f64;
log (f32 x) -> f32;
log10 (f64 x) -> f64;
log10 (f32 x) -> f32;
log2 (f64 x) -> f64;
log2 (f32 x) -> f32;

### Power functions

## gfx

### Primitives

* point ()
* line ()
* lines ()
* polygon ()
* circle ()
* box ()

### Presentation of data

* plot ()
* scatter ()
* bars ()

### Transformations

* transform ();
* translate ();
* rotate ();
* scale ();

### UI

* inputBox ();
* panel ();
* radio ();
* checkbox ();
* form ();
* label ();

### Interaction

* mouse
* keyboard

## io

fopen ();
fclose ();

write (ostream&, T args..., char sep = ' ', char end = ' ') -> ostream&


## algorithm

Look at C++ for basics algorithm

