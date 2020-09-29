### Introduction to Objects (David Newton)

_2020-09-29 13:00:00 - 2020-09-29 13:50:00_

After this lecture students should be able to:

* Name the basic components of object-oriented programming (OOP)
* Distinguish between classes and objects

By the end of this week students should have practical experience of using BlueJ with Java objects and methods.

#### Shapes example

Shapes can be different types: Circles, Squares, Triangles.

Although they can be different sizes, different colours, etc., they still remain the same shape: a bigger circle is still just a circle.

Each circle is an example, or instance of, a circle. A blue circle is just a different instance of a circle to, say, a red circle.

The "circle" is a class which describes the shared properties of the red and blue circle instances.

Students watched Dr Newton perform the following tasks in BlueJ:

* Create a new Object called "circle1" which was an instance of the class Circle.  
* Analyse the functions and variables which that object has access to
* Make the circle "visible" on the screen and move it around the canvas
* How functions work and how arguments can be passed to functions  
* The difference between variables and hard-coded values

Dr Newton then related the changes he made to actual code. _Editor's notes: I HEAVILY recommend that you watch this lecture via Blackboard if you haven't already, the visual example is worth 100x what these lecture notes are._

#### BlueJ

Students should download and install version 3.1.7 of BlueJ on their personal devices.

BlueJ is a software for visually designing programs in Java. It abstracts over and simplifies the process of creating Java classes.

Students are advised to open BlueJ and experiment with it, become accustomed to the options on the menu at the top (Project, Edit, Tools, View, Help, BlueJ Tutorial under Help).

#### Booleans

A boolean value can be either true or false. This true or false value is a mirror of the binary 1 or 0.

```
0 = false
1 = true
```

Boolean values are very efficient and useful when you need to only store one piece of information: About a thing that either **is** or **isn't**.

#### Integer

An integer is just a whole number. Later on we will learn about how many bits can make up an integer (int) but for now, just think of them as whole numbers.

#### Strings

A string is a type of data which contains letters, words, etc. In Java, strings are encapsulated in double quotes:

#### Boolean, Integer, String examples

In Java these are some example ways to initialise (create) a variable (a named box which can hold a value):

```
String firstName = "David";
String lastName = "Beckham";
Boolean isFootballer = true;
int age = 45;
```
