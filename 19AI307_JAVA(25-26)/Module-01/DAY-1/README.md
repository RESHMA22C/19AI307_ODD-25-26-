# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely finds an ancient vault secured by binary locks. Each lock responds to bitwise operations to determine whether it opens or stays shut.

To unlock the vault, she is given two integers that represent key codes in binary. The vault uses the following bitwise operations to test them:

Lock Test                           Operator
Bitwise AND                           &
Bitwise OR                               |
Bitwise XOR                            ^
Left Shift first key by 1           <<
Right Shift second key by 1   >>

She needs to apply these operations and report the results.

Input Format:
First line: First key (integer)

Second line: Second key (integer)

Output Format:
Bitwise AND: <result>
Bitwise OR: <result>
Bitwise XOR: <result>
First Key << 1: <result>
Second Key >> 1: <result>

For example:

Input	Result
7
2
Bitwise AND: 2
Bitwise OR: 7
Bitwise XOR: 5
First Key << 1: 14
Second Key >> 1: 1



## AIM:
To write a program that takes two integers as input and performs various bitwise operations—AND, OR, XOR, left shift, and right shift—to produce the corresponding results.

## ALGORITHM :
1.	Start the program.
   
2.Read the first integer and the second integer from the user.

3.Perform bitwise AND using a & b.

4.Perform bitwise OR using a | b.

5.Perform bitwise XOR using a ^ b.

6.Left shift the first number by 1 using a << 1.

7.Right shift the second number by 1 using b >> 1.

8.Display all the results in the given format.

9.End the program.




## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

## Sourcecode.java:

```
import java.util.*;
public class java{
    public static void main(String[]args)
    {
        Scanner scan = new Scanner(System.in);
        int a = scan.nextInt();
        int b = scan.nextInt();
        int c= a & b;
        int d = a | b;
        int e = a ^ b;
        int f = a << 1;
        int g = b >> 1;
        System.out.println("Bitwise AND: "+c);
        System.out.println("Bitwise OR: "+d);
        System.out.println("Bitwise XOR: "+e);
        System.out.println("First Key << 1: "+f);
        System.out.print("Second Key >> 1: "+g);
    }
}
```





## OUTPUT:

<img width="711" height="249" alt="image" src="https://github.com/user-attachments/assets/a6034bc5-0ef1-45ab-9879-554fe95bea16" />


## RESULT:

Thus, the Java program demonstrating bitwise operators and shift operations was successfully executed.

