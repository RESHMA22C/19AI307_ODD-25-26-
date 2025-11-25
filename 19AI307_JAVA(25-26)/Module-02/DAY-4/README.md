# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Write a java program using class to perform addition of two numbers using parameterised constructor.

Input	Result
5
5
Sum = 10


## AIM:

To write a Java program using a class and a parameterized constructor to perform the addition of two numbers.

## ALGORITHM :

1.Start the program.

2.Import the package java.util.Scanner.

3.Create a class named Addition.

4.Declare two integer variables.

5.Create a parameterized constructor that accepts two numbers and assigns them to the variables.

6.Create a method to calculate and print the sum of the two numbers.

7.In the main method, create a Scanner object to read input from the user.

8.Read two numbers from the user.

9.Create an object of the Addition class by passing the two numbers to the constructor.

10.Call the method to display the sum.

11.End the program.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Reshma C
RegisterNumber: 212223040168
*/
```
```
import java.util.*;
class Addition {
    int a,b;
    Addition (int x,int y){
        a = x;
        b = y;
    }
    void displaySum(){
        int sum = a + b;
        System.out.println("Sum = " +sum);
    }
}
public class Main{
    public static void main(String[]args){
        Scanner sc = new Scanner(System.in);
        int n1 = sc.nextInt();
        int n2=sc.nextInt();
        Addition obj = new Addition(n1, n2);
        obj.displaySum();
    }
}
```



## OUTPUT:

<img width="572" height="395" alt="image" src="https://github.com/user-attachments/assets/08f4202e-6c8b-4a99-b2a6-2c5a5c19d0c9" />


## RESULT:

The program successfully reads two numbers, passes them to a parameterized constructor, and prints their sum.

