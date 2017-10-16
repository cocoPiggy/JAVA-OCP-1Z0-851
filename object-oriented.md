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

## Question 14
```java
01. interface TestA { String toString(); }
02.
03. public class Test {
04.   public static void main(String[] args) {
05.     System.out.println(new TestA() {
06.     public String toString() { return "test"; }
07.     });
08.   }
09. }
```
What is the result?  
A. test  
B. null  
C. An exception is thrown at runtime.  
D. Compilation fails because of an error in line 1.  
E. Compilation fails because of an error in line 5.  
F. Compilation fails because of an error in line 6.  
【Answer】 A  
**Explanation/Reference:**  
Every class in java has toString() method in it by default, which is called by System.out.println() if you pass some object of a class to it. When you try to print object of a class, the System.out.println() method will call toString() of the class which returns the className@hashcode of that object.  

## Question 16
```java
01. public class Blip {
02. protected int blipvert(int x) { return 0; }
03. }
04. class Vert extends Blip {
05. // insert code here
06. }
```
Which five methods, inserted independently at line 5, will compile? (Choose five.)  
A. public int blipvert(int x) { return 0; }  
B. private int blipvert(int x) { return 0; }  
C. private int blipvert(long x) { return 0; }  
D. protected long blipvert(int x) { return 0; }  
E. protected int blipvert(long x) { return 0; }  
F. protected long blipvert(long x) { return 0; }  
G. protected long blipvert(int x, int y) { return 0; }  
【Answer】 ACEFG  
**Explanation/Reference:**  
The access specifier for an overriding method can allow more, but not less, access than the overridden method. For example, a protected instance method in the superclass can be made public, but not private, in the subclass. So B is wrong.  
The compiler does not consider return type when differentiating methods, so you cannot declare two methods with the same signature even if they have a different return type. So D is wrong.  

## Question 18
Which Man class properly represents the relationship "Man has a best friend who is a Dog"?  
A. class Man extends Dog { }  
B. class Man implements Dog { }  
C. class Man { private BestFriend dog; }  
D. class Man { private Dog bestFriend; }  
E. class Man { private Dog<bestFriend>; }  
F. class Man { private BestFriend<dog>; }  
【Answer】 D  
**Explanation/Reference:**  
If the Class has entity reference then it is called Aggregation. Aggregation is also known for "HAS - A" relationship.  
In the above question we have "Man has a best friend " which represents container-ship or "HAS-A" relationship. Therefore bestFriend is one of the Member of Man.  
"Who is a Dog".This part may confuses us, but in the question it is very much clear in stating that best friend is of type Dog . So Datatype is Dog and variable name is bestFriend.  
Since we have Dog bestFriend as a data member of Man, therefore Man has to be a Class which has this data member which satisfies "HAS-A" relationship.  

## Question 20
Given:
```java
11. abstract class Vehicle { public int speed() { return 0; }
12. class Car extends Vehicle { public int speed() { return 60; }
13. class RaceCar extends Car { public int speed() { return 150; } ...

21. RaceCar racer = new RaceCar();
22. Car car = new RaceCar();
23 Vehicle vehicle = new RaceCar();
24 System.out.println(racer.speed() + ", " + car.speed() + ", " + vehicle.speed());
```
What is the result?  
A. 0, 0, 0  
B. 150, 60, 0  
C. Compilation fails.  
D. 150, 150, 150  
E. An exception is thrown at runtime.  
【Answer】 D  
**Explanation/Reference:**  
Racecar().speed() override the method in Car and Vehicle.  
## Question 21
Given:
```java
05. class Building { }
06. public class Barn extends Building {
07.   public static void main(String[] args) {
08.     Building build1 = new Building();
09.     Barn barn1 = new Barn();
10.     Barn barn2 = (Barn) build1;
11.     Object obj1 = (Object) build1;
12.     String str1 = (String) build1;
13.     Building build2 = (Building) barn1;
14.   }
15. }
```
Which is true?  
A. If line 10 is removed, the compilation succeeds.  
B. If line 11 is removed, the compilation succeeds.  
C. If line 12 is removed, the compilation succeeds.  
D. If line 13 is removed, the compilation succeeds.  
E. More than one line must be removed for compilation to succeed.  
【Answer】C  
**Explanation/Reference:**  
Cannot cast from Building to String

## Question 23
Given:
```java
21. class Money {
22.   private String country = "Canada";
23.   public String getC() { return country; }
24. }
25. class Yen extends Money {
26.   public String getC() { return super.country; }
27. }
28. public class Euro extends Money {
29.   public String getC(int x) { return super.getC(); }
30.   public static void main(String[] args) {
31.     System.out.print(new Yen().getC() + " " + new Euro().getC());
32.   }
33. }
```
What is the result?  
A. Canada  
B. null Canada  
C. Canada null  
D. Canada Canada  
E. Compilation fails due to an error on line 26.  
F. Compilation fails due to an error on line 29.  
【Answer】E  
**Explanation/Reference:**  
The field Money.country is not visible  
## Question 24
Assuming that the serializeBanana() and the deserializeBanana() methods will correctly use Java serialization and given:  
```java
13. import java.io.*;
14. class Food implements Serializable {int good = 3;}
15. class Fruit extends Food {int juice = 5;}
16. public class Banana extends Fruit {
17.   int yellow = 4;
18.   public static void main(String [] args) {
19.     Banana b = new Banana(); Banana b2 = new Banana();
20.     b.serializeBanana(b); // assume correct serialization
21.     b2 = b.deserializeBanana(); // assume correct
22.     System.out.println("restore "+b2.yellow+ b2.juice+b2.good);
24.   }
25.   // more Banana methods go here
50. }
```
What is the result?  
A. restore 400  
B. restore 403  
C. restore 453  
D. Compilation fails.  
E. An exception is thrown at runtime.  
【Answer】  
**Explanation/Reference:**  
  


