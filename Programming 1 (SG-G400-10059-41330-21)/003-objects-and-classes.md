### Objects and Classes (David Newton)

_2020-10-05 09:00:00 - 2020-10-05 09:50:00_

Dr Newton began the lecture by highlighting the importance of taking notes. Dr Newton recommends that students take snips (screenshots) of important learning materials for later study.

#### Considering objects

Computer programs often have to represent (or model) real world information.

Dr Newton gave an example of an application which models bank account information:

* We need some mechanism for holding information about thw bank  
* In programming we call this mechanism an object  

Some example object we could use are:

* Information about the bank itself
* A customer
* Their bank accounts (because they could have multiple, a savings and a checking account for example)
* Transactions
* Direct debits
* Information about the staff and their permissions

Think of objects like a template (or mould) which can be used over and over again to store similar information.

We call these templates `classes`. A single template is called a `class`. When we create a customer or a bank account from this template, we callt he resulting data structure and `object`.

A computer program (written using this object-oriented programming style) will consist of many interacting objects.

#### Classes

Each class (or template) has a set of attributes (AKA properties, or more simply values).

For example, the properties of a circle are:

* A diameter (stored as an integer - meaning whole-number)  
* An x and y position  (each stored as integers)  
* A colour  (stored as a String - meaning a collection of characters)  
* Whether it is visible (stored as a boolean - meaning yes or no)  

In programming in general these properties are a type of variable, meaning a type of data which can be changed - it is literally vary-able.

Creating an object (or instance) of the circle class is done using the following code in Java:

```
new Circle();
```

#### Compiling

Compiling is a way that the java machine tells you that it understand what you have written. It takes the code (or in the case of BlueJ, the classes you've visually designed) and turns it in to a computer program which your computer can run.


