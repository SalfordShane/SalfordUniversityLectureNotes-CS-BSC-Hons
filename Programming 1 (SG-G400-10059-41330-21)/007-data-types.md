### Data Types (David Newton)

_2020-10-20 09:00:00 - 2020-10-20 09:50:00_

#### Numerical data types

There are 6 numerical data types in Java:

* byte (ranges from -128 to 127, takes 1 byte (8 bits) of space)
* short (ranges from -32768 to 32767, takes 2 byte (16 bits) of space)
* int (ranges from -2147483648 to 2147483647, takes 4 byte (32 bits) of space)
* long (ranges from -9223372036854775808 to 9223372036854775807, takes 8 byte (64 bits) of space)
* float (ranges from -3.40282347 x 10^-38 to 2.40282347 x 10^38, takes 4 byte (32 bits) of space)
* double (ranges from -1.7 x 10^-308 to 1.7 x 10^308, takes 8 byte (64 bits) of space)  

For anyone unfamiliar with scientific notation it was briefly covered in a CSIL lecture [here](https://github.com/SalfordShane/SalfordUniversityLectureNotes-CS-BSC-Hons/blob/master/Computer%20System%20Internals%20and%20Linux%20(SG-G400-10048-33284-21)/005-binary-floating-point-numbers.md)

#### Implicit type conversion

Type conversion means changing the type of a variable from one data type to another, for instance, from an integer to a float, or from a char to a string.

Some data types are incompatible because the data type isn't big enough to store the necessary data, for instance:

* You can convert an int to a float because a float is an extension of an int (It's just an int with a mantissa)
* You can't automatically convert from a float to an int (because the int can't store the mantissa)

_Editor's note: Mantissa is the bit after the decimal point in a floating point number._

Some data types require explicit type conversion (actually having to write code to convert between the data types) but others can do it automatically, for instance, this is totally fine:

```java
int number = 3;
float floatNumber = number;
```

And the following is also totally fine:

```java
int number1 = 3;
float number2 = 1.1;
number2 = number1 + number2;

System.out.println(number2);
// Prints 4.1
```
