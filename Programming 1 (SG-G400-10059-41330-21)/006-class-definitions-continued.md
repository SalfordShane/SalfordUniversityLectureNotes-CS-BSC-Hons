### Class definitions - Continued (David Newton)

_2020-10-19 09:00:00 - 2020-10-19 09:50:00_

#### Conditional statements

`Conditional statements` is a term which roughly means "if this, do something, else, do something else".

An if statement in Java generally has this form:

```java
if (condition) {
    // A statement
}
```

If the value of condition is true, the statement within the curly brackets will be executed. For instance:

```java

int number = 1;

if (number == 1) {
    // This will execute as number equals 1
}

if (number == 2) {
    // This will not execute as number does not equal 2
}

```

You can also use the following format:

```java
int number = 1;

if (number == 2) {
    // This will not be executed as number does not equal 2
} else {
    // The else statement will be executed instead
}
```

#### Boolean expressions

`Boolean expressions` is a complex term for a simple idea: if conditions which will always equal either true or false. Good examples we should be familiar with are numeric comparisons:

```java
int number = 1;

// if number equals 2
if (number == 2) {
    // this will not execute
}

// if number does not equal 2
if (number != 2) {
    // this will execute
}

// if number is more than 1
if (number > 1) {
    // this will not execute
}

// if number is less than 2
if (number < 2) {
    // this will execute
}

// if number is more than or equal to 1
if (number >= 1) {
    // this will execute
}

// if number is less than or equal to 2
if (number <= 2) {
    this will execute
}
```

#### Local variables

We spoke about local variables in [004-objects-and-classes-continued.md](004-objects-and-classes-continued.md), but for simplicity I'll include the decinition here:

> `local` variables: values which only exist within the scope of a single function or method. (it is created within the function and can't be used outside of the function)

Here is an example of a local variable:

```java
public int functionWithLocalVariable() {
    // number is our local variable
    int number = 0;
    number = number + 1;
    return number;
}
```

The variable `number` in the above method is a local variable, scoped to the method it is defined within. This means that `number` can only be used within that method, trying to access the variable outside of the method will cause the compiler to throw an error.

#### Method signatures

A `signature` just means the `name`, `number of arguments` and `type of arguments` which a method can take. In java you can't have two functions with the same signature:

```java
public void sayHello() {

}

public void sayHello() {
   // throws an error: a method with this signature is already defined
}
```

The above code would throw an error, however if you chance a single part of the signature the code will compile just fine:

```java
public void sayHello() {

}

public void sayHello(string name) {
    // This won't throw an error as the arguments passed to the functions are different
}
```

#### Numerical data types

At this point in the lecture, Dr Newton talked about numerican data types but as he said he would re-cap that next lecture it will be covered in the next set of notes.
