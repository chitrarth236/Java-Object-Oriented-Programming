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
### Thread Priorities

Thread priority constants are as follows:
1. public static final int MIN_PRIORITY = 1;
2. public static final int NORM_PRIORITY = 5;
3. public static final int MAX_PRIORITY = 10;

Thread priority methods:
1. public final int getPriority();
2. public final void setPriority(int priority);

Any int number between min and max priority can also be used to set priority. Thread with high priority will get the chance to run first. If two threads have same priority we cannot expect execution order. 

Default priority for main thread is 5. For all the other threads default priority is inherited from parent to child thread.

However, thread priorities cannot guarantee the order in which threads execute and are very much platform dependent.

### Important methods related to threads

#### yield()
Causes the currently running thread to yield to any other threads of the same priority that are waiting to be scheduled. If there is no waiting thread or all waiting threads have low priority then same thread can continue its execution.

#### join()
java.lang.Thread class provides the join() method which allows one thread to wait until another thread completes its execution. If t is a Thread object whose thread is currently executing, then t.join() will make sure that t is terminated before the next instruction is executed by the program. An overloaded method of join takes miliseconds to specify waiting time. Like sleep, join also throws an InterruptedException. 

#### sleep()
Thread.sleep causes the current thread to suspend execution for a specified period. This is an efficient means of making processor time available to the other threads of an application or other applications that might be running on a computer system.

#### interrupt()
The interrupt() method of thread class is used to interrupt the thread. If any thread is in sleeping or waiting state (i.e. sleep() or wait() is invoked) then using the interrupt() method, we can interrupt the thread execution by throwing InterruptedException.

If the thread is not in the sleeping or waiting state then calling the interrupt() method performs a normal behavior and doesn't interrupt the thread but sets the interrupt flag to true.

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

### Inter-thread communication
- Below three methods are present in Object class(not in Thread class, because a thread can call these method on any java object).
- All three methods can only be called from synchronized area and the thread should acquire the lock of that object first.

### wait
- If a thread calls wait() on any object it immediately releases the lock of that object and enters into waiting state.
- If waiting thread gets notification it will go to another waiting state to get a lock of that object first then after getting lock it will enter ready/runnable state.

### notify
- If thread calls notify() on any object, it releases the lock of that object but not immediately.

### notifyAll
