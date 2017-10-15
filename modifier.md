## Question 19
Given:  
```java
package test;
class Target {
public String name = "hello";
}
```
What can directly access and change the value of the variable name?  
A. any class  
B. only the Target class  
C. any class in the test package  
D. any class that extends Target   
【Answer】 C  
**Explanation/Reference:**  
If a class has no modifier (the default, also known as package-private), it is visible only within its own packag.  
