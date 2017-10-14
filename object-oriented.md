## Question 6
Given:  
```java
public abstract class Shape {
  private int x;
  private int y;
  public abstract void draw();
  public void setAnchor(int x,int  y) {
    this.x = x;
    this.y = y;
    }
 }
 ```
 Which two classes use the Shape class correctly? (Choose two.)  
 A. public class Circle implements Shape {  
     private int radius;  
    }  
 B. public abstract class Circle extends Shape {  
     private int radius;  
    }  
 C. public class Circle extends Shape {  
     private int radius;  
     public void draw();  
    }  
 D. public abstract class Circle implements Shape {  
     private int radius;  
     public void draw();  
    }  
 E. public class Circle extends Shape {  
     private int radius;  
     public void draw() {/* codehere */}  
    }  
 F. public abstract class Circle implements Shape {  
     private int radius;  
     public void draw() {/* codehere */}  
    }  

【Answer】 BE  
**Explanation/Reference:**  
A. Shape is a class which cannot be implemented.  
B. Circle（extends）Shape but does not implement the abstract method. So cirble must be a abstract class.   
C. Circle does not implement the abstract method.   
D. Shape is a class which cannot be implemented. 
E. Circle（extends）Shape and implement the abstract method.  
F. Shape is a class which cannot be implemented.  

## Question 9
Which statement is true about the classes andinterfaces in the exhibit?  
```java
01. public interface A {
02.   public void doSomething(String thing);
03. }

01. public class AImpl implements A {
02.   public void doSomething(String msg) {}
03. }

01. public class B {
02.   public A doit(){
03.     //more code here
04.   }
05.   public String execute(){
06     //more code here
07   }
08. }

01. public class C extends B {
02.   public AImpl doit(){
03.     //more code here
04.   }
05.
06.   public Object execute() {
07.     //morecode here
08.   }
09. }
```
A. Compilation will succeed for all classes andinterfaces.  
B. Compilation of class C will fail because of anerror in line 2.  
C. Compilation of class C will fail because of anerror in line 6.  
D. Compilation of class AImpl will fail because of anerror in line 2.  
【Answer】 C  
**Explanation/Reference:**  
AImpl is a child of A so override is sucess. Object is a parent of String so override is failed.  


