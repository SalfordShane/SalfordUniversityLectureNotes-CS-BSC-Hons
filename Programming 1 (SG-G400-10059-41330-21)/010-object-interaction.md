### Object interaction (David Newton)

_2020-11-02 09:00:00 - 2020-11-02 09:50:00_

Dr Newton began by telling the students that the automated testing suite for Homework 2 would be available today or tomorrow, with students uploading using the same method as last time.

#### Class diagrams

Class diagrams are a visual (graphed) representation of the relationship between different classes. Multiple classes can defined (like the Canvas and Shape classes in the original House example in BlueJ) and the class diagram displays the relationships between them (which class uses which other classes, etc.)

Class diagrams contain relationships which exist regardless of the state of the program - as long as a class in your code contains code to use another class, it will be included in the diagram.

#### Primitives vs References

We have used a lot of primitive types so far (simple types like Integers, Strings, Booleans), objects created from a class are referred to as Object Types or Reference Types.

Objects can have fields (object variables / properties) which contain other object. Those objects can in turn contain their own objects, in effect any given object can contain an infinite number of children which contain objects which contain objects which contain objects, etc.

#### Object diagrams

An object diagram is similar to a class diagram, except instead of being an abstract representation of the program it contains the program at a particular state. It only shows objects as they would exist (and containing the data which would exist) at a single point in running the program.

Object diagrams can be very useful for debugging what is happening in a program at a certain point, and how the program changes between two points.

Object diagrams are dynamic (they change over time) and class diagrams are static (they do not change.)

#### Private and public

The keywords public and private are used in method and field declarations. Declaring a method or a field public allows it to be used by code outside of the class. For instance, you could make a method public in one class, pass an object of that class in to another class and then use the public method from within the code in the second class.
