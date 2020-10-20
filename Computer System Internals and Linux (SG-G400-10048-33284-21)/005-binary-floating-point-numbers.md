### Binary Floating Point Numbers (Norman Murray)

_2020-10-20 10:00:00 - 2020-10-20 10:50:00_

Floating point numbers are used in computer science to represent decimals. These are decimal numbers:

* `0.9`
* `150.0005`
* `7.85`

In scientific notation decimals are often expressed as powers of 10:

* `332 = 3.32 x 10 ^ 2`
* `0.0000000911 = 9.11 x 10 ^ -8`

The scientific notation syntax is:

```
3.32       x 10 ^ 2
9.11       x 10 ^ -8
{mantissa}   {exponent}
```

#### Floating point numbers in binary

The following numbers all use unsigned-8bit binary for the whole numbers and unsigned-3bit binary for the decimal numbers.

On the number line we've been using so far, we can extend it further to the right to represent fractions (negative powers of 2):

* `2 ^ -1 = 0.5`
* `2 ^ -2 = 0.25`, etc

To work out 13.5 we can do:

```
128 64 32 16 8 4 2 1 | .5 .25 .125
0   0  0  0  1 1 0 1   1  0   0
```

This leaves us with: `00001101.100` or: `1101.1`

To work out 22.75 we can do:

```
128 64 32 16 8 4 2 1 | .5 .25 .125
0   0  0  1  0 1 1 0 | 1  1   0
```

This leaves us with `00010110.110` or: `10110.11`

#### IEEE-754

IEEE-754 is the standard we use to decide how binary floating point numbers should work in computer systems. It is used for representing 32 and 64 bit numbers (E.G. The float and double data types in Java.

_Editor's note: This is a complex topic which is hard to simply explain and I don't understand it in the depth needed to convey it in these notes. It will be covered in depth in your next tutorial and I would suggest you learn it there._
