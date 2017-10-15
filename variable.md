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
Answer: B  
**Explanation/Reference:**  
f cannot be resolved  

