## Exceptions in Java
There are three types of exceptions in Java:

1) **Checked Exception**
The classes which directly inherit Throwable class except RuntimeException and Error are known as checked exceptions e.g. IOException, SQLException etc. Checked exceptions are checked at compile-time. You must need to handle it before compiling your code.

2) **Unchecked Exception**
The classes which inherit RuntimeException are known as unchecked exceptions e.g. ArithmeticException, NullPointerException, ArrayIndexOutOfBoundsException etc. Unchecked exceptions are not checked at compile-time, but they are checked at runtime.

3) **Error**
Mostly related to the environment in which the code is running. Error is irrecoverable e.g. OutOfMemoryError, VirtualMachineError, AssertionError etc.

5 keywords of Java Exception handling

**try**: The first step in constructing an exception handler is to enclose the code that might throw an exception within a try block.If an exception occurs within the try block, that exception is handled by an exception handler associated with it. To associate an exception handler with a try block, you must put a catch block after it.

**catch**: you associate exception handlers with a try block by providing one or more catch blocks directly after the try block. No code can be between the end of the try block and the beginning of the first catch block.

**finally**: The finally block always executes when the try block exits. This ensures that the finally block is executed even if an unexpected exception occurs. But finally is useful for more than just exception handling — it allows the programmer to avoid having cleanup code accidentally bypassed by a return, continue, or break. Putting cleanup code in a finally block is always a good practice, even when no exceptions are anticipated.

**throw**: The "throw" keyword is used to throw an exception.

**throws**: The throws keyword is used to declare exceptions that can occur during the execution of a program. For any method that can throw exceptions, it is mandatory to use the throws keyword to list the exceptions that can be thrown, if it is not handling it in try catch block.


### Custom Exception example in Java

```Java
// class representing custom exception  
class InvalidAgeException extends Exception  
{  
    public InvalidAgeException (String str)  
    {   
        super(str);  
    }  
}  
    
// class that uses custom exception InvalidAgeException  
public class TestCustomException1  
{  
    static void validate (int age) throws InvalidAgeException{    
       if(age < 18){   
        throw new InvalidAgeException("age is not valid to vote");    
       }  
       else {   
        System.out.println("welcome to vote");   
        }   
     }    
  
    // main method  
    public static void main(String args[])  
    {  
        try  
        {   
            validate(13);  
        }  
        catch (InvalidAgeException ex)  
        {  
            System.out.println("Caught the exception");  
            System.out.println("Exception occured: " + ex);  
        }  
  
        System.out.println("rest of the code...");    
    }  
}  
```
