# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class City with attributes: cityName (String), population (long), area (double). Create an object. Print all details.

import java.util.Scanner;
class City {

    String cityName;
    long population;
    double area;

    void printDetails() {
           // Your Code Here
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
         // Your Code Here
         scanner.close();
    }
}

For example:

Input	Result
New York
8419000
783.8
City Name: New York
Population: 8419000
Area: 783.8
London
8982000
1572
City Name: London
Population: 8982000
Area: 1572.0



## AIM:
To create a class City with attributes cityName, population, and area, then create an object, accept values from the user, and print all the details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class City with data members:
     String cityName
  	  long population
   double area
4.Define a method printDetails() to display the city information.
5.In the main() method:
         Create a Scanner object to accept user input.

         Create an object of the City class.

         Read input values for city name, population, and area.

         Assign these values to the object.

        Call the printDetails() method to print the details.





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```
```
import java.util.Scanner;
class City {
    String cityName;
    long population;
    double area;
    void printDetails() {
           System.out.println("City Name: " + cityName);
           System.out.println("Population: "+population);
           System.out.println("Area: "+area);
        }
    
}
class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String name = scanner.nextLine();
        long pop = scanner.nextLong();
        double ar = scanner.nextDouble();
        City city = new City();
        city.cityName = name ;
        city.population = pop;
        city.area = ar ;
        city.printDetails();
        scanner.close();
        }
    
}
```


## OUTPUT:

<img width="817" height="481" alt="image" src="https://github.com/user-attachments/assets/67207781-30d5-4723-b25d-e8d22377994a" />



## RESULT:

The program successfully creates a City class, accepts user inputs, stores them inside a City object, and prints the city details as shown in the given example.

