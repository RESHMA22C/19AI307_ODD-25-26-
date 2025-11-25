# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to create a base class Animal (Animal Family) with a method called Sound(). Create two subclasses Bird and Cat. Override the Sound() method in each subclass to make a specific sound for each animal.

For example:

Input	Result
bird
Bird chirps



## AIM:

To write a Java program that demonstrates inheritance and method overriding by creating a base class Animal with a Sound() method and two subclasses Bird and Cat that override the method to produce specific sounds.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a base class Animal with a method Sound().

4.Create two subclasses:
      Bird
      Cat

5.In each subclass, override the Sound() method to print:
       “Bird chirps”
       “Cat meows”

6.In the main() method:
      Take user input.
  	   If input is "bird" → create a Bird object.
      If input is "cat" → create a Cat object.

7.Call the Sound() method to display the respective sound.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

```
import java.util.Scanner;

class Animal {
    void Sound() {
        System.out.println("Animal makes a sound");
    }
}

class Bird extends Animal {
    @Override
    void Sound() {
        System.out.println("Bird chirps");
    }
}

class Cat extends Animal {
    @Override
    void Sound() {
        System.out.println("Cat meows");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();

        Animal animal;

        if (input.equalsIgnoreCase("bird")) {
            animal = new Bird();
        } else if (input.equalsIgnoreCase("cat")) {
            animal = new Cat();
        } else {
            animal = new Animal();
        }

        animal.Sound();
    }
}
```





## OUTPUT:

<img width="822" height="371" alt="image" src="https://github.com/user-attachments/assets/03e64283-867c-427c-a117-d9bd5e5ea9e6" />


## RESULT:
Thus, the program successfully demonstrates inheritance and method overriding by producing different sounds for different animals.

