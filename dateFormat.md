## Question 25
Given a valid DateFormat object named df, and
```java
16. Date d = new Date(0L);
17. String ds = "December 15, 2004";
18. //insert code here
```
What updates d's value with the date represented by ds?  
A. d = df.parse(ds);  
B. d = df.getDate(ds);  
C. try {   
d = df.parse(ds);  
} catch(ParseException e) { };  
D. try {  
d = df.getDate(ds);  
} catch(ParseException e) { };  
【Answer】 C  
**Reference/Explanation**  
A. Cannot complie 'Unhandled exception type ParseException'  
```java
Date d = new Date(0L);
String ds = "December 15, 2004";
DateFormat df = DateFormat.getDateInstance();
try {
  d = df.parse(ds);
} catch(ParseException e) { };
```
