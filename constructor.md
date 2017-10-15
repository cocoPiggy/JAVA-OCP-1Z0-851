## Question 10
What is the result?  
```java
11. public class Person {
12.   String name = "No name";
13.   public Person(String nm) { name = nm; }
14. }

15. public class Employee extends Person {
16.   String empID= "0000";
17.   public Employee(String id) { empID = id; }
18. }

19. public class EmployeeTest {
20.   public static void main(String[] args){
21.   Employee e= new Employee("4321");
22.   System.out.println(e.empID);
23.   }
24. }
```
A. 4321  
B. 0000  
C. An exception is thrown at runtime.  
D. Compilation fails because of an error in line 18.  
【Answer】 D  
**Reference/Explanation**  
The constructor of Employee must call its super constructor, the constructor of Person.  
public Employee(String id) { super(id); empID = id; } }  

## Question 13
Given:
```java
class Atom {
  Atom() {System.out.print("atom "); }
}
class Rock extends Atom {
  Rock(Stringtype) { System.out.print(type); }
}
public class Mountain extends Rock {
  Mountain(){
    super("granite");
    new Rock("granite ");
  }
  public static void main(String[] a) { new Mountain(); }
}
```
What is the result?  
A. Compilation fails.  
B. atom granite  
C. granite granite  
D. atom granite granite  
E. An exception is thrown at runtime.  
F. atom granite atom granite  
【Answer】 F  
**Reference/Explanation**  
Java constructor is invoked at the time of object creation.  
Inside Main Method new Mountain object is created which calls its constructor in Line 12. Inside Mountain constructor , super("granite") calls the Rocks constructor by passing granite String argument. Inside Rock constructor, implicitly calls super() Atom constructor passing no argument.  
Therefore atom is printed first from the SOP of Atom Constructor, then comes down to Rock constructor and prints whats is stored in rocks constructor's variable (String Type) which is Granite.  
Comes down and now a new Rock object gets created by calling constructor of Rock passing "granite" String argument and gets accepted in String type= "granite". Inside Rock constructor ,implicitly calls ( super() ) Atom constructor passing no argument.  
Therefore atom is printed again, then comes down to Rock constructor and prints whats is stored in type a String variable which is Granite.  
Comes down to mountain method and comes back to main method and program terminates printing the result Atom Granite Atom Granite.  

## Question 17
Given:
```java
01. class Super {
02.   private int a;
03.   protected Super(int a) { this.a = a; }
04. }

11. class Sub extends Super {
12.   public Sub(int a) { super(a); }
13.   public Sub() { this.a = 5; }
14. }
```
Which two, independently, will allow Sub to compile? (Choose two.)  
A. Change line 2 to: public int a;  
B. Change line 2 to: protected int a;  
C. Change line 13 to: public Sub() { this(5); }  
D. Change line 13 to: public Sub() { super(5); }    
E. Change line 13 to: public Sub() { super(a); }  
【Answer】 CD  
**Reference/Explanation**  
Sub cannot use private a in super.  

## Question 

**Reference/Explanation**  


