### Defining a Thread

A thread is a lightweight sub-process, the smallest unit of processing. Multiprocessing and multithreading, both are used to achieve multitasking. Multithreading is a process of executing multiple threads simultaneously.

There are two ways to create a thread:

1. By extending Thread class
2. By implementing Runnable interface.

Using Runnable interface

```Java
class MyThreadJob implements Runnable{

    @Override
    public void run() {
        //core thread job's logic
    }
}

public class MultiThreading {
    public static void main(String[] args){
        //define thread's job
        MyThreadJob threadJob = new MyThreadJob();
        
        //create thread by passing the thread's job
        Thread t1 = new Thread(threadJob);
        
        //to start the thread
        t1.start();

        System.out.println("main thread");
    }
}
```

### Synchronized keyword

1. Synchronized is the keyword applicable to methods and blocks(not to classes/variables) and used to resolve concurrency issue.

2. If a method or block is synchronized then at a time only one Thread is allow to execute that method or block on the given object.

3. But the main disadvantage of synchronized keyword can slowdown your program because of restricing concurrency and, a synchronized keyword introduce some overhead in method/block.

4. A good rule of thumb is to synchronize only bare minimum that should be synchronized using synchronized block.

5. Internally synchronization concept is implemented by using lock concept. lock concept is implemented based on object but not based on method.

6. Every object in java has a unique lock. If a thread wants to execute any synchronized method on the given object 1st it has to get the lock of that object. Once a thread got the lock of that object then only it's allow to execute any synchronized method on that object. If the synchronized method execution completes then automatically thread releases lock.

8. While a thread executing any synchronized method the remaining threads are not allowed execute any synchronized method on that object simultaneously. But they are allowed to execute any non-synchronized method simultaneously.

9. If a thread want to access synchronized static method, a thread will need to use class level lock. Every class in Java has a unique lock.

10. if one thread is exceuting static synchronized method, the other threads are not allowed to access any other static synchronized method of that class via any object simultaneously. but they can execute any synchronized or non-synchronized method simultaneously.
