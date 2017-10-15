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
**Explanation/Reference:**  
Variable argument (varargs) must be the last argument.  

## Question 12
Given:
```java
01. public class Mud {
02. //insert code here
03. System.out.println("hi");
04. }
05. }
```
And the following five fragments:
```java
public static void main(String...a) {
public static void main(String.* a) {
public static void main(String... a) {
public static void main(String[]... a) {
public static void main(String...[] a) {
```
How many of the code fragments, insertedindependently at line 2, compile?  
A. 0  
B. 1  
C. 2  
D. 3  
E. 4  
F. 5  
【Answer】 D  
**Explanation/Reference:**  
public static void main(String...a) {  
public static void main(String... a) {  
public static void main(String[]... a) {  

