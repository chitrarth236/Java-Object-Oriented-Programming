static keyword is used to define class property/method independent of any object.
no copy of a static variable is made on object creation. Instead, all objects of the class share the same static variable.
can be accessed via dot operator with class name or object.

you can directly initialized the static variables while declaring
Or you can use static block to initialize static variables
static block is called when the class is loaded

static methods have several resctrictions
-it can only access static data.
-this/super cannot be used.
-they can only call other static methods


Static methods are not polymorphic. they are statically linked at the compile time.
static methods can be inheritaned but cannot be overridden.
if you create same method in subclass, the method in superclass will be hidden instead of overriding.

An abstract class can have general static method
But, an abstract class cannot have static abstract method.
	-Because, static methods cannot be overridden by subclass, and abstract keyword indicates that method must be overridden in subclass.


