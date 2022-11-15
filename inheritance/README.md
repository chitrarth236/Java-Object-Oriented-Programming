## Inheritance in Java

Inheritance can be defined as the process where one class acquires the properties (methods and fields) of another. It is also known as IS-A relationship.
### Types of Inheritance in Python
  - Single Inheritance
  - Multi Level Inheritance
  - Hierarchical Inheritance
  - Hybrid Inheritance

### example:
```Java
class Super {
   .....
   .....
}
class Sub extends Super {
   .....
   .....
}
```
### Method Overriding

#### Rules for Overridding Inherited Methods
- The argument list should be exactly the same as that of the overridden method.
- The return type should be the same or a subtype of the return type declared in the original overridden method in the superclass.
- The access level cannot be more restrictive than the overridden method's access level. 
- Private data fields in a superclass are not accessible outside of that class, hence they cannot be used directly by a subclass; they can be accessed &/or mutated by public accessor &/or mutators defined in the superclass.
- An instance method can be overridden only if it is accessible; private methods cannot be overridden if a method defined in a subclass is private in its superclass, the two methods are completely unrelated
- A static method can be inherited, but a static method cannot be overridden remember that static methods are class methods.
- If a static method defined in a superclass is redefined in a subclass, the method defined in the superclass is hidden; the hidden static method can be invoked by using the syntax “SuperClassName.staticMethodName( );”
- A method declared final cannot be overridden.
- Overridding of non-abstract method to an abstract method is possible.


### super() method/keyword

  - The built-in super() method / super keyword is used to call the super class's constructors, variables and methods from the child class.
  - The super keyword in Java is a reference variable which is used to refer immediate parent class object. 
  - Whenever you create the instance of subclass, an instance of parent class is created implicitly which is referred by super reference variable.

  #### Calling the constructor using super():
  ```Java
  super (parameter-list);
  ```
  - parameter-list specifies any parameters needed by the constructor in the superclass.
  - constructors are called in order of derivation, from superclass to subclass.
  - super(…) must be the first statement executed in a subclass’ constructor.
  - If super(…) is not used, the default constructor of each superclass will be executed(Implicitly default form of super ( super() ) will be invoked in each subclass to call default constructor of superclass). 

  #### Calling the methods and variables using super():
  - To call super class'es members super keyword is used liek this: 'super.member'.
  - Here, member can be either a method or an instance variable.
  - It is most applicable to situations in which member names of a subclass hide members by the same name in the superclass.
