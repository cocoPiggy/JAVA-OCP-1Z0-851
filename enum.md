## Question 8
Given:
```java
class Nav{
  public enum Direction { NORTH, SOUTH, EAST, WEST }
}

public class Sprite{

// insert code here

}
```
Which code, inserted at line 14, allows the Spriteclass to compile?  
A. Direction d = NORTH;  
B. Nav.Direction d = NORTH;  
C. Direction d = Direction.NORTH;  
D. Nav.Direction d = Nav.Direction.NORTH;  
【Answer】D   
**Explanation/Reference:**  
enum is specified inside a class Nav and that can be called from other class that so we use the reference of the class
Nav.It's Encapsulation concept.  

