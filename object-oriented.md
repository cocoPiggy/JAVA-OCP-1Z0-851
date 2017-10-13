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
**Explanation/Reference**  
A. Shape is a abstract class which cannot be implemented.
B. Circle（extends） Shape，但没有实现Shape的抽象方法draw(),因此仍然是个抽象类  
C. Circle定义为继承了抽象类Shape的普通类，却没有实现Shape的抽象方法draw()，不符合普通类的语法规定  
D. Shape是类，只能 extends不能implements  
E. Circle定义为继承了抽象类Shape的普通类，并且实现Shape的抽象方法draw()，符合普通类的语法规定  
F. Shape是类，只能extends不能implements  


