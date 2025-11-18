# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the maximum odd number in an array

 
For example:

Input	Result
5
2
3
7
8
6
7
4
2
4
6
8
No odd number found

## AIM:

To write a Java program to find the maximum odd number in an array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the size of the array from the user.
4.	Read all the array elements one by one.
5.Check each element to see if it is odd.
6.Keep track of the largest odd number found.
7.Display the maximum odd number, or show a message if no odd number exists.


## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Reshma C 
RegisterNumber:  212223040168
*/
```

## SOURCE CODE:
```
import java.util.*;
public class max{
    public static void main(String[]args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i = 0;i < n ;i++){
            arr[i]=sc.nextInt();
        }
        int b = Integer.MIN_VALUE;
        boolean found = false;
        for(int i =0; i < n;i++){
            if(arr[i]%2 != 0){
                if(!found || arr[i] > b){
                b = arr[i];
                found = true;
                }
            }
        }
    
    if(found){
        System.out.print(b);
    }else{
        System.out.print("No odd number found");
    }
}
}
```


## OUTPUT:

<img width="751" height="529" alt="image" src="https://github.com/user-attachments/assets/2add35df-a5f8-4d3d-a5c1-103088b3eb90" />


## RESULT:
Thus, the Java program to find the maximum odd number in an array was successfully executed.
