# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.

<img width="604" height="399" alt="image" src="https://github.com/user-attachments/assets/b81f55e1-fbe1-44b8-904a-c6a889b23ca3" />

## AIM:

To implement a Mediator design pattern where an Air Traffic Control (ATC) system coordinates landing requests from multiple airplanes.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of airplanes and whether the runway should be released after landing.
4.	Create an AirTrafficControl mediator.
5.	For each airplane:

  =>Create an Airplane object linked to the ATC.

  =>Request landing through the mediator.
6.If landing is allowed and release flag is true, release the runway.

7.Display landing status messages for each airplane.

8.End the program.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

## SOURCE CODE:
```
import java.util.*;

class AirTrafficControl {
    private boolean runwayFree = true;

    public boolean requestLanding(Airplane airplane) {
        if (runwayFree) {
            runwayFree = false;
            System.out.println(airplane.getName() + " granted landing.");
            return true;
        } else {
            System.out.println(airplane.getName() + " denied landing. Runway busy.");
            return false;
        }
    }

    public void releaseRunway() {
        runwayFree = true;
    }
}

class Airplane {
    private String name;
    private AirTrafficControl control;

    public Airplane(String name, AirTrafficControl control) {
        this.name = name;
        this.control = control;
    }

    public String getName() {
        return name;
    }

    public void requestLanding(boolean releaseAfterLanding) {
        boolean allowed = control.requestLanding(this);
        if (allowed) {
            System.out.println(name + " landed successfully.");
            if (releaseAfterLanding) {
                control.releaseRunway();
            }
        }
    }
}

public class AirTrafficSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        AirTrafficControl control = new AirTrafficControl();

        int n = Integer.parseInt(sc.nextLine()); // number of airplanes
        boolean release = sc.nextLine().equalsIgnoreCase("true"); // release after landing?

        List<Airplane> airplanes = new ArrayList<>();
        for (int i = 0; i < n; i++) {
            String name = sc.nextLine();
            airplanes.add(new Airplane(name, control));
        }

        for (Airplane plane : airplanes) {
            plane.requestLanding(release);
        }

        sc.close();
    }
}
```






## OUTPUT:

<img width="1010" height="521" alt="image" src="https://github.com/user-attachments/assets/5255ff87-df56-472f-b21e-a06efa8dfcae" />


## RESULT:

Airplanes communicate through the ATC mediator, which manages landing permissions, demonstrating centralized control without direct airplane-to-airplane communication.
