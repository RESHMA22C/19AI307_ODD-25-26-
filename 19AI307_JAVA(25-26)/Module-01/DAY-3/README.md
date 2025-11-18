# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Display Factors of a Number

For example:

Input	Result
12
Factors: 1 2 3 4 6 12
15
Factors: 1 3 5 15


## AIM:
To write a program to display all the factors of a given number.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a number from the user.
4.Use a loop from 1 to the given number.
5.Check if the current value divides the number evenly (num % i == 0).
6.If true, display it as a factor.



## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

## SOURCE CODE:
```
import java.util.*;

public class Factors {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();

        System.out.print("Factors: ");
        for (int i = 1; i <= n; i++) {
            if (n % i == 0) {
                System.out.print(i + " ");
            }
        }

        scan.close();
    }
}

```


## OUTPUT:

<img width="693" height="240" alt="image" src="https://github.com/user-attachments/assets/581f0c6d-4372-4990-9212-562af6065623" />

## RESULT:

Thus, the program to display the factors of a given number was successfully executed.



