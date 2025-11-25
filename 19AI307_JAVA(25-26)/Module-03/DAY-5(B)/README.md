# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to convert a string to an integer using a wrapper class and perform addition.

Input	Result
32
32
Sum = 64


## AIM:

To write a Java program that converts a string input into an integer using a wrapper class (Integer) and then performs addition.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a string from the user.
4.	Convert the string to an integer.
5.	Read another string and convert it in the same way.
6.	Add the two integer values.
7.	Print the sum.




## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

```
import java.util.Scanner;
public class StringToIntegerAddition{
    public static void main(String[]args){
        Scanner sc = new Scanner(System.in);
        String str1 = sc.nextLine();
        String str2 = sc.nextLine();
        try{
            Integer num1 = Integer.valueOf(str1);
            Integer num2 = Integer.valueOf(str2);
            int sum = num1+num2;
            System.out.println("Sum = "+sum);
        }catch(NumberFormatException e){
            System.out.println("Invalid input");
            
        }
    }
}
```





## OUTPUT:


<img width="755" height="440" alt="image" src="https://github.com/user-attachments/assets/b7ecbca5-df24-4a26-b907-8bb2b6aff704" />


## RESULT:

Thus, the program successfully demonstrates string-to-integer conversion using a wrapper class and performs addition on the converted values.
