# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:

Write a Java program to write characters to a file using FileWriter.

<img width="397" height="150" alt="image" src="https://github.com/user-attachments/assets/32ed9c55-a3fe-4647-a3b2-702206f425e5" />


## AIM:

To write characters to a file in Java using the FileWriter class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the file name and content from the user.
4.	Create a FileWriter object with the given file name.
5.	Write the content to the file using write().
6.	Close the FileWriter.
7.	Print success message if no exception occurs; otherwise, print an error message.
8.	AIMM End the program.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

## SOURCE CODE:

```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class WriteToFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        
        String fileName = sc.nextLine();
        String content = sc.nextLine();

        try {
            
            FileWriter writer = new FileWriter(fileName);

            
            writer.write(content);

            
            writer.close();

            
            System.out.println("File written successfully.");
        } 
        catch (IOException e) {
            System.out.println("An error occurred.");
        }

        sc.close();
    }
}
```





## OUTPUT:

<img width="792" height="297" alt="image" src="https://github.com/user-attachments/assets/4ef36b00-cfb4-433a-8ca1-de4685aa5809" />


## RESULT:

The program successfully writes the user-provided content to the specified file and confirms completion.


