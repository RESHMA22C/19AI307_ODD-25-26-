# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:

temperature
botType (1 for SunBot, 2 for RainBot)Output:
Prediction as a string.

For example:

Input	Result
35 1
HOT



## AIM:
To create a program where different weather prediction bots implement a common interface and provide temperature-based predictions.
## ALGORITHM :

1.	Start the program.

2.	Import the necessary package 'java.util'

3.	Create an interface WeatherBot with a method predict(int temperature) that returns a string.

4.Create two classes that implement this interface:
    SunBoT
         If temperature > 30 → return "HOT"
         Else → return "MODERATE"
    RainBot
         If temperature < 20 → return "COLD"
         Else → return "WARM"

5.In the main() method:
         Read temperature and bot type.
         If botType = 1 → create SunBot.
         If botType = 2 → create RainBot.

6.Call the predict() method and print the output.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Reshma C 
RegisterNumber:  212223040168
*/
```
```
import java.util.Scanner;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        return (temperature > 30) ? "HOT" : "MODERATE";
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        return (temperature < 20) ? "COLD" : "WARM";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temperature = sc.nextInt();
        int botType = sc.nextInt();
        WeatherBot bot;

        if (botType == 1) {
            bot = new SunBot();
        } else if (botType == 2) {
            bot = new RainBot();
        } else {
            System.out.println("Invalid bot type!");
            sc.close();
            return;
        }

        System.out.println(bot.predict(temperature));
        sc.close();
    }
}
```



## OUTPUT:


<img width="664" height="276" alt="image" src="https://github.com/user-attachments/assets/47be27e8-09b0-4bf0-9682-60c69e8e5ac4" />


## RESULT:

Thus, the program successfully demonstrates how different bots implement a common interface to provide weather predictions.

