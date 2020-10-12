### Objects and Classes - Continued (David Newton)

_2020-10-12 09:00:00 - 2020-10-12 09:50:00_

_If you don't understand the concept of classes, please read [003-objects-and-classes.md](003-objects-and-classes.md)_.

_It's recommended to view the lecture recording for this PROG-01 lecture if you missed it as this was an important lesson for new learners of programming - these lecture notes are supplemental, not a replacement for attendance._

#### Object properties

A `Circle` object (an object created from the `Circle` class) has several attributes (or properties):

* diameter
* colour
* position
* etc.

These attributes are called "instance fields". The `Circle` object is an instance (or example) of the `Circle` class.

The values stored in these instance fields are the object's state. It's important to notice that ONLY the values are the `state` for the purposes of the tests going forwards:

```java
int diameter = 4;

int            diameter             =             4;
{type}         {attribute name}     {assignment}  {value, the state}
```

#### Some new concepts

Dr Newton introduced us to several new concepts we will cover in the next chapter:

* `local` variables: values which only exist within the scope of a single function or method. (it is created within the function and can't be used outside of the function)  
* `accessor` functions: Functions (methods) which return some data  
* `mutator` functions: Functions(methods) which change some data
* `scope`: When you define a variable (or a parameter) that variable can only be used within the method (or function) in which it is defined.

#### Constructors

When you see the `new` keyword it means that a new object instance of a class is being created:

```java
machine = new TicketMachine();
```

When the instance is created a special method called a `constructor` is called:

* Constructor methods have the same name as the class
* Constructors are responsible for creating (instantiating or initialising are other terms used) the variables (properties) which the object uses

For example (in the following code, lines which start with two slashes are COMMENTS, not code):

```java
// The definition of the circle class
public class Circle {
    // The definition of the diameter property
    int diameter;

    // The definition of the constructor
    public Circle {
        // The instantiation (creation) of the diameter property
        diameter = 5;
    }
} 
```

#### Overview of classes

Classes are defined by the Java code we write. The class definition contains the following:

* The attributes (or properties) that will exist within the object  
* The methods (or function) that the object will be able to use  

#### Comments

You saw some examples of comments in the code block above. Comments are useful for annotating our code - giving extra information about the code, who wrote it, etc.

Examples of comments:

```java
// This is a single line comment

// You can have multiple but each line must begin with 2 slashes
```

You can also have comments which span across multiple lines of your code. Example of multi-line comments:

```java
/**
 * This is a multi line comment
 * It must begin with a slash and two stars (asterisk)
 * And it must end with a star (asterisk) and a slash
 */
```

#### Arguments

Methods (functions) can take extra values which they can use, these extra values are called arguments:

```java

public void changeDiameter(int newDiamater) {
    diameter = newDiameter;
}
```

`int newDiameter` in the code above is the argument which can be passed to the `changeDiameter` method. Methods can accept multiple arguments, separated by commas, for example:

```java
public int multiply(int numberOne, int numberTwo) {
    /**
     * In java, the asterisk (*) is used instead of the x you are used to in maths:
     * 5 * 5 = 25
     * NOT:
     * 5 x 5 = 25
     */
    return numberOne * numberTwo;
}
```

#### Home work

Dr Newton asked us to do the work on slide 2.19 of `slides 02.ppt` which can be found in the Programming-1 module in Blackboard.
