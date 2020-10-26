### Identifiers, arithmetic and Booleans (David Newton)

_2020-10-26 09:00:00 - 2020-10-26 09:50:00_

#### Overloading

Different operators can act differently based on the data types the operator it is used with, for instance:

##### Addition

When the addition operator `+` is used with integers, the end result is an integer, when it is used with floats it will give you a float:

```java
int num1 = 1;
int num2 = 2;
System.out.println(num1 + num2);
// Prints int: 3

float num3 = 1.5;
System.out.println(num1 + num3);
// Prints float: 2.5
```

When the addition operation is used with strings, it will concatenate the strings (join them together), for instance:

```java
String str1 = "Hello";
String str2 = "World";

System.out.println(str1 + " " + str2);
// Prints String: Hello World
```

##### Overloaded division

When using the division operand `/`, the result type will be the input type with the fewest decimal points (precision):

```
int num1 = 5;
int num2 = 2;
float num3 = 10.0;

System.out.println(num1 / num2);
// Prints int: 2
// The remainder is NOT rounded for integer division, it is DISCARDED

System.out.println(num1 / num3);
// Prints float: 0.5
```

When data types are mixed (such as `4.0 / 3` (a float and an int)) the data type with the lowest precision (the int in this case) will be automatically converted to the data type with the highest precision: to simplify, the int becomes a float.

#### Precedence rules

In general the order in which the parts of an expression are calculated follows BODMAS (Google this if you don't know it). If you don't want your expression to be executed according to BODMAS you can force the order of operation by using brackets. In Java Brackets are executed before the content outside of the brackets:

```java

System.out.println(1 + 2 * 3);
// Prints int: 7

System.out.println((1 + 2) * 3);
// Prints int: 9
```

#### Modulo

The Modulo operator `%` gives you the `remainder` after performing division, for instance:

```
System.out.println(8 % 5);
// Prints int: 3

System.out.println(10 % 5);
// Prints int: 0

System.out.println(11 % 5);
// Prints int: 1
```

To simplify the above example of `8 % 5`:

* Divide 8 by 5
* You are left with 1.6
* This means that 5 goes in to 8: 1 and a "bit" times
* Do 8 - (5 * 1)
* You are left with 3

The remainder when finding out how many times 5 goes in to 8 is 3

#### Explicit type conversion

Consider the following program:

```java

double num1 = 10.5;
double num2 = 15.7;

int num3 = num1 * num2;
```

The above program will not compile because you are trying to store a double in an integer.

Sometimes, we want to do this anyway to simplify our program or get a value we can nicely output. We can explicity tell the program to `cast` one data type to another data type:

```java
double num1 = 10.5;
double num2 = 15.7;

int num3 = (int) (num1 * num2);
System.out.println(num3);
// Prints int: 164
```

#### Boolean logical operators

In the past we've seen boolean expressions in if statements:

```java

int num = 5;

if (num > 0) {
    // This expression executes
} else {
    // This expression does not execute
}
```

We can also combine multiple boolean expressions by using and `&&` and or `||`:

```java

int num = 5;

// if num is more than 0 AND num does not equal 10
if (num > 0 && num != 10) {
    // This expression executes
}

// if num is more than 10 OR num equals 5
if (num > 10 || num == 5) {
    // This expression executes
}
```
