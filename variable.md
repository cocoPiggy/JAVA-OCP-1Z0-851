## Question 15
```java
public classQ15Test {
    public static void parse(String str) {
        try {
                float f = Float.parseFloat(str);
            } catch (NumberFormatException nfe) {
                f = 0;
              } finally {
                System.out.println(f);
              }
       }
   public static void main(String[] args) {
       parse("invalid");
   }
}
```
What is the result?  
A. 0.0  
B. Compilation fails.  
C. A ParseException is thrown by the parse method at runtime.  
D. A NumberFormatException is thrown by the parse method at runtime.  
【Answer】 B  
**Reference/Explanation**  
f cannot be resolved  

## Question 26
Given:  
```java
11. double input = 314159.26;
12. NumberFormat nf = NumberFormat.getInstance(Locale.ITALIAN);
13. String b;
14. //insert code here
```
Which code, inserted at line 14, sets the value of b to 314.159,26?  
A. b = nf.parse( input );  
B. b = nf.format( input );  
C. b = nf.equals( input );  
D. b = nf.parseObject( input );  
【Answer】 B  
**Reference/Explanation**  
To format a number for the current Locale, use one of the factory class methods:  
```java  
  myString = NumberFormat.getInstance().format(myNumber);  
```
You can also use a NumberFormat to parse numbers:  
```java
  myNumber = nf.parse(myString);
```
## Question 27
Given:  
```java
public class TestString1 {
  public static void main(String[] args) {
    String str = "420";
    str += 42;
    System.out.print(str);
  }
}
```
What is the output?  
A. 42  
B. 420  
C. 462  
D. 42042  
E. Compilation fails.  
F. An exception is thrown at runtime   
【Answer】 D  
**Reference/Explanation**  
The Java language provides special support for the string concatenation operator ( + ), and for conversion of other objects to strings.  

## Question 35
Given:  
```java
22. StringBuilder sb1 = new StringBuilder("123");
23. String s1 = "123";
24. // insert code here
25. System.out.println(sb1 + " " + s1);
```
Which code fragment, inserted at line 24, outputs "123abc 123abc"?  
A. sb1.append("abc"); s1.append("abc");  
B. sb1.append("abc"); s1.concat("abc");  
C. sb1.concat("abc"); s1.append("abc");  
D. sb1.concat("abc"); s1.concat("abc");  
E. sb1.append("abc"); s1 = s1.concat("abc");  
F. sb1.concat("abc"); s1 = s1.concat("abc");  
G. sb1.append("abc"); s1 = s1 + s1.concat("abc");  
H. sb1.concat("abc"); s1 = s1 + s1.concat("abc");  
【Answer】 E  
**Reference/Explanation**  

## Question 37
Given:  
```java
01. public class LineUp {
02.   public static void main(String[] args) {
03.     double d = 12.345;
04.     // insert code here
05.   }
06. }
```
Which code fragment, inserted at line 4, produces the output | 12.345|?  
A. System.out.printf("|%7d| \n", d);  
B. System.out.printf("|%7f| \n", d);  
C. System.out.printf("|%3.7d| \n", d);  
D. System.out.printf("|%3.7f| \n", d);  
E. System.out.printf("|%7.3d| \n", d);  
F. System.out.printf("|%7.3f| \n", d);  
【Answer】 F  
**Reference/Explanation**  

