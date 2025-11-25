# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

import java.util.Scanner;

class BankAccount {
    // Private instance variables
    private String accountNumber;
    private double balance;

    // Getter and Setter for accountNumber
    public String getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }

    // Getter and Setter for balance
    public double getBalance() {
        return balance;
    }
    public void setBalance(double balance) {
        this.balance = balance;
    }
}

## AIM:
To write a Java program that creates a BankAccount class with private instance variables and uses public getter and setter methods to access and modify them.

## ALGORITHM :

1.Start the program.

2.Import the package java.util.Scanner.

3.Create a class named BankAccount.

4.Declare private variables accountNumber and balance.

5.Create getter and setter methods for both variables.

6.In the main method, create a Scanner object to take input from the user.

7.Create an object of the BankAccount class.

8.Read account number and balance from the user.

9.Use setter methods to store the values in the object.

10.Use getter methods to retrieve and print the values.

11.End the program.




## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```
```
import java.util.Scanner;
class BankAccount {
    private String accountNumber;
    private double balance;
    public String getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
        
    }
    public double getBalance() {
        return balance;
      }
    public void setBalance(double balance) {
        this.balance = balance;
    }
    
} 
public class Main{
    public static void main(String[]args){
        Scanner scan = new Scanner(System.in);
        BankAccount obj = new BankAccount();
        String accountNumber = scan.nextLine();
        obj.setAccountNumber(accountNumber);
        double balance = scan.nextDouble();
        obj.setBalance(balance);
        System.out.println("Account Number: "+obj.getAccountNumber());
        System.out.println("Balance: "+obj.getBalance());
    }
}
```


## OUTPUT:

<img width="934" height="453" alt="image" src="https://github.com/user-attachments/assets/85dffecc-d777-48cf-ae76-15659c88a3ba" />

## RESULT:

The program successfully creates a BankAccount class with private variables and accesses them using public getter and setter methods. It takes account number and balance as input and displays them as output.

