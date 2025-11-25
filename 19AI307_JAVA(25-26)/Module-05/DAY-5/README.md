# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:

Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

Input:

Two lines: a and b values

Output:

a = <swapped_a>

b = <swapped_b>

## AIM:

To read two integer values from the user, use a synchronized block to safely swap them, and display the swapped values.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read input from the user.
4.	Read the first integer value and store it in variable a.
5.	Read the second integer value and store it in variable b.
6.	Create a lock object for synchronization.
7.	Enter a synchronized block using the lock object.
8.	Inside the synchronized block, swap the values of a and b using a temporary variable temp.
9.	Exit the synchronized block.
10.	Print the updated value of a.
11.	Print the updated value of b.
12.	Close the scanner.
13.	End the program.







## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = Integer.parseInt(sc.nextLine().trim());
        int b = Integer.parseInt(sc.nextLine().trim());

        Object lock = new Object();

        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }

        System.out.println("a = " + a);
        System.out.println("b = " + b);

        sc.close();
    }
}
```




## OUTPUT:

<img width="394" height="286" alt="image" src="https://github.com/user-attachments/assets/57c302fc-beb1-440e-84f7-0a6affd2fd61" />



## RESULT:
The program successfully swaps the values of variables a and b using synchronization and prints the updated values.
