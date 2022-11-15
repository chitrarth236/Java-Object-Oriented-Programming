### Polymorphism

Polymorphism means "many forms."
#### Polymorphism can be implemented in two ways
- Overloading
- Overriding 

#### Overloading
Overloading means same method name, but with different signature.

Overloaded methods
- Must have different argument lists
- May have different return types, if argument lists are also different
- May have different access modifiers
- May throw different exceptions
- Methods from a superclass can be overloaded in a subclass.

#### Overriding
Notes about Overrding are [here](https://github.com/chitrarth236/Java-Object-Oriented-Programming/tree/main/inheritance#method-overriding)

#### Dynamic Method Dispatch
- Dynamic method dispatch is the mechanism by which a call to an overridden method is resolved at run time, rather than compile time.
- When an overridden method is called through a superclass reference, the method to execute will be based upon the type of the object being referred to at the time the call occurs. Not the type of the reference variable. 

A single object can be referred to by reference variables of many different types —as long as they are the same type or a supertype of the object.

Polymorphic method invocations apply only to overridden instance methods
