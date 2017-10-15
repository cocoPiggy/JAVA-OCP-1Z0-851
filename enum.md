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

## Question 11
Given:  
```java
01. public class Rainbow {
02.   Public enum MyColor {
03.     RED(0xff0000), GREEN(0x00ff00),BLUE(0x0000ff);
04.     private final int rgb;
05.     MyColor(int rgb) { this.rgb = rgb; }
06.     public int getRGB() { return rgb; }
07.   };
08.   publicstatic void main(String[] args) {
09.     //insert code here
10.   }
11. }
```
Which code fragment, inserted at line 9,allows the Rainbow class to compile?  
A. MyColor skyColor = BLUE;  
B. MyColor treeColor = MyColor.GREEN;  
C. if(RED.getRGB() < BLUE.getRGB()) { }  
D. Compilation fails due to other error(s) inthe code.  
E. MyColor purple = new MyColor(0xff00ff);  
F. MyColor purple = MyColor.BLUE + MyColor.RED;  
【Answer】 B  
**Explanation/Reference:**  
A. MyColor skyColor = MyColor.BLUE;  
C. if(MyColor.RED.getRGB() < MyColor.BLUE.getRGB()) { }. 
E. cannot use new to create enum.
F. cannot use operator '+'  

## Question 


