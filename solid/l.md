# Liskov Sabstitution Principle

> if you have a parent class and a child class, then the base class and child class can be used interchangeably without getting incorrect results.

> Derived classes must be substitutable for their base classes. (Robert Martin)

> All derivatives must conform to the behavior that clients expect of the base classes that they use. (Robert Martin)

## In the context of JavaScript, this means that:

* Methods of a subclass that override methods of a base class must have exactly the same number of arguments.
* Each argument of the overridden method must be the same type as the method of the base class.
* The return type of the overridden method must be the same as the method of the base class.
* The types of exceptions thrown from the overridden method must be the same as the method of the base class.

[Example](https://github.com/vladilenm/SOLID_javascript/blob/master/3_L.js)
