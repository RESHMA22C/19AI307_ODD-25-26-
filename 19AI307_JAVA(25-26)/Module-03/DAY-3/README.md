# Ex.No:3(C) ABSTRACTION

## QUESTION:
Description:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

Input Format:

First line: 1 or 2
Second line: base, level (or attempts)

Output Format:

Final score (int)

For example:

Input	Result
1 100 3
400
2 4
500

## AIM:

To create an abstract class GameScore with an abstract method finalScore(), and implement two subclasses ArcadeGame and PuzzleGame that compute scores based on given rules.

## ALGORITHM :

1.Start the program.

2.	Import the necessary package 'java.util'

3.	Create an abstract class GameScore with an abstract method finalScore() returning an integer.

4.Create subclass ArcadeGame with:
          Inputs: baseScore, level
          Formula:
          score = baseScore + (level × 100)

5.Create subclass PuzzleGame with:
          Input: attempts
  	       Rule:
             If attempts ≤ 3 → score = 1000 - (attempts × 100)
             Else → score = 500

6.Read user input:
       1 → ArcadeGame
       2 → PuzzleGame

7.Based on the choice, create the appropriate object.

8.Call finalScore() and print the result.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

```
import java.util.*;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    private int baseScore;
    private int level;

    ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }

    int finalScore() {
        return baseScore + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    private int attempts;

    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    int finalScore() {
        if (attempts <= 3)
            return 1000 - (attempts * 100);
        else
            return 500;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        GameScore game;

        if (type == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            game = new ArcadeGame(base, level);
        } else {
            int attempts = sc.nextInt();
            game = new PuzzleGame(attempts);
        }

        System.out.println(game.finalScore());
    }
}

```



## OUTPUT:

<img width="659" height="332" alt="image" src="https://github.com/user-attachments/assets/5eb22a04-457f-4892-8874-179e47dffd76" />


## RESULT:

Thus, the program correctly computes the final score based on the game type and user inputs.

