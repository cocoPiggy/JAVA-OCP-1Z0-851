## Question 7
Given:
```java
public class Barn {
 public static void main(String[]args) {
   new Barn().Go("hi",1);
   new Barn().go("hi","world", 2);
   }
 public void go(String... y,int x) {
      System.out.print(y[y.length - 1] +" ");
   }
 }
 ```
 What is the result?  
 A. hi hi  
 B. hi world  
 C. world world  
 D. Compilation fails.  
 E. An exception is thrown at runtime.  
【Answer】 D
**Reference/Explanation**
Variable argument (varargs) must be the last argument.  
