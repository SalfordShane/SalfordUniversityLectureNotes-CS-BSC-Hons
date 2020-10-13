### Class definitions (David Newton)

_2020-10-13 13:00:00 - 2020-10-13 13:50:00_

#### Scope

##### Method parameter scope

Parameters (function arguments) can only be accessed (used) from within the function in which it is declared.

This means that once a function ends, all the variables defined _within_ the function are no longer accessible.

##### Field scope

Fields are variables which belong to the class object. These variables can be used within any function inside of the class object, but similar to how method variables (parameters) can't be used outside the method in which they are defined, fields (object variables) can not be used outside of the class in which they are defined.

##### Lifetimes

A new concept is `lifetime`. The `lifetime` of a variable in a method can be simply defined as:

> A lifetime is how long a variable lives during a call to a method

Once the method call ends (the function returns a value), the variables within it are no longer alive.

The `lifetime` of a field (object variable) can be simple defined as:

> How long variables defined within a class live is the same as how long the class object lives

#### Accessors and Mutators

At this point, Dr Newton talked about accessors and mutators, we covered those in the previous lecture which you can [find here](004-objects-and-classes-continued.md).

#### Shorthand assignment

You should be used to seeing the following code by now:

```java
// Assigning the value 50 to the variable named sum
int sum = 50;

// Increasing the value of sum to 100
sum = sum + 50;
```

You can also do shorthand maths, the following code executes EXACTLY the same as the code above:

```java
// Assinging the value 50 to the variable named sum
int sum = 50;

// increasing the value of sum to 100
sum += 50;
```

#### Concatenation

You're going to hear a lot about concatenation. The word concatenate is a very complex word for a very simple idea:

> Concatenate just means to join together multiple words

The following code is exactly the same:

```java

string helloWorld = "hello world";

// Is the same as:

string helloWorld = "hello " + "world";

// Is the same as

string helloWorld = "hello" + " " + "world";
```

You can also concatenate words and numbers (strings and integers) and the numbers will automatically be converted to a string:

```java
string helloNumber = "hello world " + 1001;

System.out.println(helloNumber);

// Outputs: "hello world 1001"
```

#### if statements

At this point, Dr Newton gave a short introduction to `if` statements. If statements only execute the statement within the brackets if the `if statement`'s value is `TRUE`;

We will get in to these deeper in future lectures and tutorials, but for completeness' sake I've included an example:

```java

int amount = 0;

if (amount < 1) {
    System.out.println("This is outputted because amount is less than 1");
} else {
    System.out.println("This is not outputted because amount is not less than 1");
}
```
