# Ex.No:2(B) METHODS

## QUESTION:
Create two methods:

Get the input for radius from the user.

double getArea(double r) → calculate the area and return the area(Don't print anything in this method).

void printArea(double area) → pass the calculated area to this method and print the area of a circle.



For example:

Input	Result
2
12.56


## AIM:
To write a Java program that gets the radius of a circle from the user, calculates the area using a separate method, and prints the area using another method.

## ALGORITHM :

1.Start the program.

2.Import the necessary package java.util.Scanner.

3.Create a class named Circle.

4.Define a method getArea(double r) to calculate and return the area of the circle.

5.Define another method printArea(double area) to print the area.

6.In the main method, create a Scanner object to read the radius from the user.

7.Read the radius value.

8.Create an object of the Circle class.

9.Call getArea() with the radius to compute the area.

10.Store the returned area in a variable.

11.Call printArea() and pass the area to print it.

12.End the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```
```
import java.util.Scanner;
public class two{
    static double getArea(double r)  {
        return 3.14*r*r;
    }
    static void printArea(double area){
        System.out.printf("%.2f",area);
    }
    public static void main(String [] args){
        Scanner sc= new Scanner(System.in);
        double radius = sc.nextDouble();
        double area = getArea(radius);
        printArea(area);
        sc.close();
    }
}
```



## OUTPUT:

<img width="747" height="248" alt="image" src="https://github.com/user-attachments/assets/6ac5f0bb-2b98-486b-903f-fe681b86e062" />


## RESULT:
The program successfully accepts the radius from the user, calculates the area using the getArea() method, and prints the area using the printArea() method. The output matches the expected value (e.g., input 2 produces 12.56).
