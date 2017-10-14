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




