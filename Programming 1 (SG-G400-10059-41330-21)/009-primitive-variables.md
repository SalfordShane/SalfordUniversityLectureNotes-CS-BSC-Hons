### Primitive variable decleration (David Newton)

_2020-10-27 13:00:00 - 2020-10-27 13:50:00_

#### Declaration

In the following code, two numbers are declared, allocated memory and initialized to the value `zero`.

```java
int number1, number2;
```

In the following code, new values are assigned to each of those variables:

```java
number1 = 234;
number2 = 87;
```

The variables are the same, their memory is still allocated in the same location in the computer, but the values stored at those locations are different.

#### Declaring objects

In the following code, a new object is declared:

```java
Account account1;
```

When an object is declared, a value isn't stored at the location of its memory, but a `pointer` is created. A `pointer` is a new concept - a `pointer` `points` to a different location in memory. When we declared an integer above, it defaulted to the value `zero`, when we declare an object, the default value is a `null` `pointer`.

In the following code, an account object is created and the `pointer` in `account1` is updated to `point` to that `object`:

```java
account1 = new Account(100);
```

#### Garbage collection

We currently have an `Account` orject stored in `account1`, if we run the following code we end up with a new object stored in `account`:

```java
account1 = new Account(250);
```

So now we have two objects, one with a value of `100` which isn't being pointed to by `account1`, and another with a value of `250` which is being pointed to by `account1`.

The `Account(100)` object is orphaned (because nothing points to it) and Java will automatically deleted that object.This process of Java looking for orphaned data and deleting it from memory is called `Garbage collection`.

#### Shared pointers

Two variables can point to the same object, the following code is perfectly fine:

```java
Account account1, account2;
account1 = new Account(100);
account2 = account1;
```

In the code above, both `account1` and `account2` point to the **same** `Account` object.

#### Further reading

Dr Newton asked that students read slides 39-46 in Slides SM01.ppt in Blackboard **before the next lecture**.

Dr Newton also asked that students attempt the `spec test 1` on in Blackboard **before the next lecture**.
