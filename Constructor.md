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

