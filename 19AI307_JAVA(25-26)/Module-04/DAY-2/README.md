# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:

At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.

To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.

Your task is to simulate this system using the Singleton pattern.

Key Hint (Hidden in Story):
Only one control tower object should exist.

Every flight contacting it should register its name.

You should log the order of flights that contacted the tower.

Input Format:
First line: Integer n – number of incoming flights

Next n lines: Each line contains the flight name.

Output Format:
For each flight, print:

[FlightName] registered with Radar Control Tower. Total Flights: [count]

For example:

Input	Result
3
AI101
BA202
EK303
AI101 registered with Radar Control Tower. Total Flights: 1
BA202 registered with Radar Control Tower. Total Flights: 2
EK303 registered with Radar Control Tower. Total Flights: 3


## AIM:

To simulate an airport radar communication system where only a single Radar Control Tower object exists, and every incoming flight must register with this single instance using the Singleton Design Pattern.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class named RadarControlTower.
4.	Inside the class, declare a private static object of the same class (this will hold the single instance).
5.	Write a private constructor so no other class can create a new tower object.
6.	Create a public static method getInstance() that:
       Checks if the instance is null.
       If null → create the object.
       Return the same object every time.
7.Add a flight counter variable inside the class.
8.Create a method registerFlight(String flightName) that:
       Increases the counter.
       Prints the message with flight name and total flights.
9.In the main() method:
       Read the number of flights.
       For each flight:
            Call RadarControlTower.getInstance() to get the ONE tower object.
            Call the registerFlight() method with the flight name.

10.Display the output for each flight in the required format.




## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```
```
import java.util.*;

class RadarControlTower {
    private static RadarControlTower instance;
    private int count = 0;

    private RadarControlTower() {}

    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    public int registerFlight(String flightName) {
        count++;
        return count;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();  // consume newline

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}

```






## OUTPUT:

<img width="1228" height="371" alt="image" src="https://github.com/user-attachments/assets/9dd9710d-e637-43af-8289-815d4f8ed479" />


## RESULT:

The program successfully ensures that all flights register with the same Radar Control Tower instance, updates the flight count for each registration, and prints the message showing the flight name and the total number of flights registered.
