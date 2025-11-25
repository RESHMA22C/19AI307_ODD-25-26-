# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:

Create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

For example:

Input	Result
africa
Lion eats Wildebeest


## AIM:

To implement the Abstract Factory pattern to create animals from two regions (Africa and Asia), where each region produces a Herbivore and a Carnivore, and to print the interaction where the Carnivore eats the Herbivore.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create abstract products Herbivore and Carnivore.
4.	Create concrete African animals (Wildebeest, Lion) and Asian animals (Buffalo, Tiger).
5.	Create an abstract factory with methods to produce a Herbivore and a Carnivore.
6.	Implement AfricaFactory and AsiaFactory to create region-specific animals.
7.	In main, read the region input and choose the correct factory.
8.	Use the factory to create a Herbivore and Carnivore.
9.	Call the carnivore’s eat() method to show the interaction.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Herbivore {}
interface Carnivore {
    void eat(Herbivore h);
}

class Wildebeest implements Herbivore {}
class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}

class Deer implements Herbivore {}
class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}

interface AnimalFactory {
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}

class AfricaFactory implements AnimalFactory {
    public Herbivore createHerbivore() {
        return new Wildebeest();
    }
    public Carnivore createCarnivore() {
        return new Lion();
    }
}

class AsiaFactory implements AnimalFactory {
    public Herbivore createHerbivore() {
        return new Deer();
    }
    public Carnivore createCarnivore() {
        return new Tiger();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();
        AnimalFactory factory;

        if (region.equals("africa")) factory = new AfricaFactory();
        else if (region.equals("asia")) factory = new AsiaFactory();
        else {
            System.out.println("Invalid region");
            return;
        }

        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}
```






## OUTPUT:

<img width="706" height="367" alt="image" src="https://github.com/user-attachments/assets/508a93e7-1208-4075-b522-394d9e0addb3" />


## RESULT:

The program creates region-specific animals using the Abstract Factory and prints the interaction where the carnivore eats the herbivore.
