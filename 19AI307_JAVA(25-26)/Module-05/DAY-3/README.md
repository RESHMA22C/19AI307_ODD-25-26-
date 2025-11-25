# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:

<img width="642" height="290" alt="image" src="https://github.com/user-attachments/assets/8de8439b-f2b1-46f9-bc33-0a137236cb92" />


## AIM:

To read multiple lines of input and print only those lines that contain the word "Java".

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Continuously read lines from the user until the word "exit" is entered.
4.	Store the lines that contain the word "Java".
5.	After input ends, print only those lines that contain "Java".




## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

## SOURCE CODE:

```
import java.io.*;

public class PrintJavaLines {
    public static void main(String[] args) {
        try {
            BufferedWriter bw = new BufferedWriter(new FileWriter("input.txt"));
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

            String line;
            while (!(line = br.readLine()).equals("exit")) {
                bw.write(line);
                bw.newLine();
            }
            bw.close();

            BufferedReader fr = new BufferedReader(new FileReader("input.txt"));
            System.out.println("Lines containing the word 'Java':");
            while ((line = fr.readLine()) != null) {
                if (line.contains("Java")) {
                    System.out.println(line);
                }
            }
            fr.close();

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```






## OUTPUT:

<img width="1179" height="451" alt="image" src="https://github.com/user-attachments/assets/0958ae5a-706b-44d4-bb52-3cd4ce4a636c" />


## RESULT:

The program reads lines until "exit" is entered, checks each line for the word "Java", stores the matching lines, and finally prints only those lines that contain the word "Java".
