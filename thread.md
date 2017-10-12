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
