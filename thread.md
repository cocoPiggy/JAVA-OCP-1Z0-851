## Question 1
Given:  
```Java
public class Threads2 implements Runnable {
 public void run() {
     System.out.println("run.");
     throw new RuntimeException("Problem");
   }
 public static void main(String[]args) {
     Thread t = new Thread(newThreads2());
     t.start();
     System.out.println("End ofmethod.");
   }
 }
```
 Which two can be results? (Choose two.)  
 A. java.lang.RuntimeException: Problem  
 
 B. run.  
    java.lang.RuntimeException: Problem  
    
 C. End of method.  
    java.lang.RuntimeException: Problem  
    
 D. End of method.  
    run.  
    java.lang.RuntimeException: Problem  
    
 E. run.  
    java.lang.RuntimeException: Problem  
    End of method.  

【Answer】 DE  
**Explanation/Reference:**  
In case of threads the behavior can not be predicted(as it depends on JVM's policy to pick items from runnable pool), so the order you see might be different in different runs. System.out.println("End of method.") can run before the run() or after the run().  

## Question 2

Which two statements are true? (Choose two.)  

A. It is possible for more than two threads to deadlock at once.  

B. The JVM implementation guarantees that multiple threads cannot enter into a deadlocked state.  

C. Deadlocked threads release once their sleep() method's sleep duration has expired.  

D. Deadlocking can occur only when the wait(),notify(), and notifyAll() methods are used incorrectly.  

E. It is possible for a single-threaded application to deadlock if synchronized blocks are used incorrectly.  

F. If a piece of code is capable of deadlocking, you cannot eliminate the possibility of deadlocking by inserting invocations of Thread.yield().  

【Answer】 AF  
**Explanation/Reference:**  
A. A deadlock is a situation wherein two or more competing actions are each waiting for the other to finish.  
B. JVM cannot guarantees deadlock.  
C. Deadlock and sleep() are unrelated.  
D. Not the only reason.  
E. Two or more thread.
F. Thread.yield() just give up the control to allow a thread to switch. There is no guarantee which thread the scheduler will run after a yield.  

## Question 3
Given:
```java
void waitForSignal(){
     Object obj = new Object();
     synchronized (Thread.currentThread()) {
            obj.wait();
            obj.notify();
         }
     }
```
Which statement is true?  
A. This code can throw an InterruptedException.  

B. This code can throw an IllegalMonitorStateException.  

C. This code can throw a TimeoutException after ten minutes.  

D. Reversing the order of obj.wait() and obj.notify() might cause this method to complete normally.  

E. A call to notify() or notifyAll() from another thread might cause this method to complete normally.  

F. This code does NOT compileunless "obj.wait()" is replaced with "((Thread)obj).wait()".  

【Answer】 B  
**Explanation/Reference:**  
wait() or notify() calls have to be invoked on object once you get monitor on that object.Otherwise, will throw the IllegalMonitorStateException. The solution is to change synchronized (Thread.currentThread()) to synchronized (obj).  


Reference:Java: Concurrency and Practice.


