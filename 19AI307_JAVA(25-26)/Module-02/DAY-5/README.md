# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Student with variables name, rollNumber. Create a method setDetails(String name, int rollNumber),and display them.

For example:

Input	Result
Saveetha
205
Name: Saveetha
Roll Number: 205



## AIM:

To create a Student class with variables name and rollNumber, set their values using a method, and display the details.

## ALGORITHM :
1.Start the program.
2.Import the package java.util.Scanner.
3.Create a class named Student.
4.Declare variables name and rollNumber.
5.Create a method setDetails(String name, int rollNumber) to assign values.
6.Create a method display() to print the values.
7.In the main method, read name and roll number from the user.
8.Create an object of Student class.
9.Call setDetails() to store the values.
10.Call display() to print the details.
11.End the program.


## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```
```import java.util.Scanner;

class Student {
    String name;
    int rollNumber;
    void setDetails(String name, int rollNumber){
        this.name = name;
        this.rollNumber = rollNumber;
    }
    void displayDetails(){
        System.out.println("Name: "+name);
        System.out.println("Roll Number: "+rollNumber);
    }
   
}

class prog {
    public static void main(String[]args){
        Scanner sc = new Scanner(System.in);
        String a = sc.nextLine();
        int b = sc.nextInt();
        Student s = new Student();
        s.setDetails(a , b);
        s.displayDetails();
    }
}
```





## OUTPUT:

<img width="730" height="410" alt="image" src="https://github.com/user-attachments/assets/7291919f-0ac8-4d48-99a7-8e93a51567ad" />



## RESULT:

The program successfully reads the student’s name and roll number, stores them using the setDetails() method, and displays the details.
