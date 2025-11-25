# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program where the inner class is declared private and accessed through a method in the outer class. 

Input	Result
3
Data set inside private inner class: 3


## AIM:

To write a Java program where a private inner class is accessed only through a public method in the outer class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an outer class called Outer.
4.Inside it, create a private inner class named Inner with:
       A variable to store the input value.
       A method to display the value.
5.Provide a public method inside the outer class that:
       Creates an object of the private inner class.
       Passes the input value to it.
       Calls the display method.
6.In the main() method:
       Read the input.
       Call the outer class method to access the private inner class.




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```
```
import java.util.Scanner;

public class Main {

    private class Inner {
        private int data;

        Inner(int data) {
            this.data = data;
        }

        void display() {
            System.out.println("Data set inside private inner class: " + data);
        }
    }

    void accessInner(int value) {
        Inner obj = new Inner(value);
        obj.display();
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int value = sc.nextInt();

        Main outer = new Main();
        outer.accessInner(value);

        sc.close();
    }
}
```





## OUTPUT:


<img width="1128" height="378" alt="image" src="https://github.com/user-attachments/assets/7261dc4b-6b6d-4095-afb8-5bb4db1bb066" />


## RESULT:

Thus, the program successfully demonstrates how a private inner class can be accessed indirectly through a method in the outer class.
