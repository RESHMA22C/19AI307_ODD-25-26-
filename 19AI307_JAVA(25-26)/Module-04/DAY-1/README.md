# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:

To store input strings in a String array and print each string in uppercase while ensuring the program does not throw a NullPointerException.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare a String array to store the input strings.
4.	Read input values and assign them to the array.
5.	Before calling .toUpperCase() on each string:
     Check whether the array element is not null using
6.If the value is not null, convert it to uppercase using .toUpperCase() and print it.
7.If an element is null, skip it to avoid a NullPointerException.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

```
import java.util.*;

public class UpperCaseArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        List<String> list = new ArrayList<>();

        while (sc.hasNextLine()) {
            String input = sc.nextLine().trim();
            if (input.isEmpty()) continue; 
            list.add(input);
        }

        String[] arr = list.toArray(new String[0]);

        for (String str : arr) {
            if (str != null && !str.equalsIgnoreCase("null")) {
                System.out.println(str.toUpperCase());
            } else {
                System.out.println("Null element");
            }
        }

        sc.close();
    }
}

```





## OUTPUT:

<img width="764" height="369" alt="image" src="https://github.com/user-attachments/assets/4e861c2e-f76d-41b3-80fa-ae10f11b86b8" />


## RESULT:

The program successfully stores the input strings in an array and prints each string in uppercase.
By checking that each array element is not null before calling .toUpperCase(), the program avoids a NullPointerException.
Only the valid (non-null) strings are converted to uppercase and displayed, ensuring smooth and error-free execution.

