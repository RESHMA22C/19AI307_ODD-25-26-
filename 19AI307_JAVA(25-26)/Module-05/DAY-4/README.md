# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

<img width="739" height="263" alt="image" src="https://github.com/user-attachments/assets/f537bdfb-1bb4-4cf2-80f6-a8a066e0c9b9" />


## AIM:

To write a Java program that reads a thread name from the user, assigns it to the current thread, and displays the thread’s name and priority.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the thread name from the user.
4.	Get the current thread using Thread.currentThread().
5.	Set the thread’s name using setName().
6.	Retrieve the thread’s priority using getPriority().
7.	Retrieve the thread’s name using getName().
8.	Print the thread’s priority, thread’s name, and complete thread information.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class ThreadInfoExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String threadName = sc.nextLine();
        Thread t = new Thread(threadName);
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
        
        sc.close();
    }
}

```





## OUTPUT:

<img width="834" height="338" alt="image" src="https://github.com/user-attachments/assets/f73bdbec-72e4-4d44-8b4a-95f128589b86" />


## RESULT:

The program successfully reads the thread name from the user, assigns it to the current thread, and prints the thread's priority, the updated thread name, and the full thread description (including name, priority, and thread group).
