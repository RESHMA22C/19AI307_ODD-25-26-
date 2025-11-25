# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:


<img width="620" height="190" alt="image" src="https://github.com/user-attachments/assets/5326fc28-c50d-44f9-9b95-42f9f70a0331" />


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
Program to implement a Serialization and Deserialization using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class WriteCharactersToFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            String filename = sc.nextLine(); 
            String content = sc.nextLine();   
            FileWriter writer = new FileWriter(filename);
            writer.write(content);
            writer.close();

            System.out.println("File written successfully.");
        } 
        catch (IOException e) {
            System.out.println("An error occurred while writing to the file.");
        }

        sc.close();
    }
}
```






## OUTPUT:

<img width="1016" height="424" alt="image" src="https://github.com/user-attachments/assets/fdbf3157-4ca1-4268-b4db-03784fa745a9" />



## RESULT:

The program successfully writes the user-provided content to the specified file and confirms completion.
