## Question 28
Which capability exists only in java.io.FileWriter?  
A. Closing an open stream.  
B. Flushing an open stream.  
C. Writing to an open stream.  
D. Writing a line separator to an open stream.   
【Answer】 D  
**Explanation/Reference:**  
A.B.C is for all IO stream. 

## Question 29
Given that the current directory is empty, and that the user has read and write permissions, and the following:  
```java
import java.io.*;
public class DOS {
  public static void main(String[] args) {
    File dir = new File("dir");
    dir.mkdir();
    File f1 = new File(dir, "f1.txt");
    try {
      f1.createNewFile();
    } catch (IOException e) { ; }
    File newDir = new File("newDir"); 
    dir.renameTo(newDir);
  }
}
```
Which statement is true?  
A. Compilation fails.  
B. The file system has a new empty directory named dir.  
C. The file system has a new empty directory named newDir.  
D. The file system has a directory named dir, containing a file f1.txt.  
E. The file system has a directory named newDir, containing a file f1.txt.  
【Answer】 E   
**Explanation/Reference:**  
