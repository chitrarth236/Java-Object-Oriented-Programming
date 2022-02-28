- A variable/field can be declared as final. Doing so prevents its contents from being modified, making it a constant.
You must initialize a final field when it is declared.

- It is a common coding convention to choose all uppercase identifiers for final fields:
        
	```java
	final int CONN = -1;
	```

- final keyword guarantees immutability only when variable is of primitive type not reference type.

- If a variable of a reference type has the final modifier, it will always refer to the same object—but the values inside of the object itself can change.
 	
	```java
	final Person Abby = new Person("Abby McG");
	Abby.updateName("Dobby"); //this is correct and possible
	
	// referencing other object is not
	Abby = new Person("Papper"); //not valid
	```
	
- final keyword in method definition prevents it from being overridden.
You cannot override final methods

"Methods declared as final can sometimes provide a performance enhancement: The compiler is free to inline calls to them because it “knows” they will not be overridden by a subclass. When a small final method is called, often the Java compiler can copy the bytecode for the subroutine directly inline with the compiled code of the calling method, thus eliminating the costly overhead associated with a method call. Inlining is only an option with final methods. Normally, Java resolves calls to methods dynamically, at run time. This is called late binding. However, since final methods cannot be overridden, a call to one can be resolved at compile time. This is called early binding."

-Important paragraph on final methods from Java The Complete Reference Book

- Making a class final pervents it from being inherited
- Abstract class cannot be declared as final
