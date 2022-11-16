## Abstraction
- Abstraction is the process of hiding certain details and showing only essential information to the user.It is achieved with either abstract classes or interfaces. 

#### Abstract class
- It is a restricted class that cannot be used to create objects (to access it, it must be inherited from another class).
- Any class have atleast have one abstract method, must be declared as abstract class.
- DMD is allowed.
- final keyword is not allowed in abstraction.

#### Abstract method
- It can only be used in an abstract class, and it does not have a body. The body is provided by the subclass (inherited from).
- No abstract constructors are allowed.
- No abstract static methods are allowed(because, abstract methods need to be overriden and static methods can't be overriden).
- Abstract class can have normal static methods.
- Abstract class can have normal instance methods.

#### abstract keyword
- The abstract keyword is a non-access modifier, used to declare abstract classes and methods.

#### interface
- An interface is a completely "abstract class" that is used to group related methods with empty bodies.
- The interface is "implemented" (similar to inherited) by another class with the implements keyword (instead of extends). The body of the interface method is provided by the "implement" class.
- An interface cannot contain a constructor.
- A variable in an interface are by default final and static.
- A class can implements multiple interfaces.
