# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A food delivery application manages and processes food orders made by two categories of users: NormalUser and PrimeUser. Each food order contains basic information such as an order ID, the customer's name, the cost of the ordered items (referred to as the total amount), and the delivery charge applied to that order.

You are required to implement this system using the concept of inheritance in object-oriented programming.

The base class is called Order. It includes the following attributes:

orderId – a string representing the unique identifier for the order

customerName – a string containing the name of the person who placed the order

totalAmount – a double value representing the total cost of the food items

deliveryCharge – a double value representing the delivery fee applied to the order

From the Order class, two derived classes are created:

NormalUser:
This class represents customers who do not have any delivery benefits. For NormalUser, the final amount they need to pay is the total food cost plus the full delivery charge. The formula is:
finalAmount = totalAmount + deliveryCharge

PrimeUser:
Prime users receive a 50% discount on the delivery charge. Their final payable amount is calculated as:
finalAmount = totalAmount + (deliveryCharge × 0.5)

Your task is to develop a program that:

Accepts exactly three food order inputs from the user.

Each input begins with the user type, either "Normal" or "Prime", followed by order ID, customer name, total food amount, and delivery charge.

Depending on the user type, the final amount is calculated using the appropriate formula.

For each order, the program should display the full details including the user type and final payable amount.

import java.util.Scanner;
import java.text.DecimalFormat;

class Order {
    String orderId;
    String customerName;
    double totalAmount;
    double deliveryCharge;

    public Order(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        this.orderId = orderId;
        this.customerName = customerName;
        this.totalAmount = totalAmount;
        this.deliveryCharge = deliveryCharge;
    }

    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }

    void display(String userType) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: " + userType);
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " + df.format(calculateFinalAmount()));
        
    }
}

 

//Continue your code here

## AIM:

To write a Java program that uses inheritance to calculate and display the final payable amount for food orders made by Normal users and Prime users, based on delivery charge rules.


## ALGORITHM :

1.Start the program.

2.Import the required packages: java.util.Scanner and java.text.DecimalFormat.

3.Create a base class named Order with attributes: orderId, customerName, totalAmount, and deliveryCharge.

4.Create a constructor in the Order class to initialize these variables.

5.Create a method calculateFinalAmount() in the Order class to compute the default final amount.

6.Create a display() method to print order details and the final amount.

7.Create a derived class NormalUser that extends Order and overrides calculateFinalAmount() to add full delivery charge.

8.Create a derived class PrimeUser that extends Order and overrides calculateFinalAmount() to add only 50% of the delivery charge.

9.In the main method, use a loop to accept three user inputs.

10.Read user type, order ID, customer name, total amount, and delivery charge.

11.Based on the user type, create either a NormalUser or PrimeUser object.

12.Call the display() method to show all order details and final payable amount.

13.Repeat for three orders.

14.End the program.



## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Reshma C
RegisterNumber:  21223040168
*/
```
```
import java.util.Scanner;
import java.text.DecimalFormat;
class Order{
     String orderId;
     String customerName;
     double totalAmount;
     double deliveryCharge;
     public Order(String orderId, String customerName, double totalAmount, double deliveryCharge){
         this.orderId=orderId;
         this.customerName=customerName;
         this.totalAmount=totalAmount;
         this.deliveryCharge=deliveryCharge;
     }
     double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }
     void display(String userType){
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: " + userType);
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " + df.format(calculateFinalAmount()));
        
    }
}
class NormalUser extends Order{
    public NormalUser(String orderId, String customerName, double totalAmount, double deliveryCharge){
        super(orderId, customerName, totalAmount, deliveryCharge);
    }
    @Override
    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }
}
class PrimeUser extends Order{
    public PrimeUser(String orderId, String customerName, double totalAmount, double deliveryCharge){
        super(orderId, customerName, totalAmount, deliveryCharge);
    }
    @Override
    double calculateFinalAmount(){
        return totalAmount + (deliveryCharge * 0.5);
    }
}
public class Main{
    public static void main( String args[]){
        Scanner scan = new Scanner(System.in);
        for(int i=1;i<3;i++){
            if (!scan.hasNextLine()) break;
            String userType = scan.nextLine().trim();
            if (userType.isEmpty()) break;
            String orderId = scan.nextLine().trim();
            String customerName = scan.nextLine().trim();
            double totalAmount = Double.parseDouble(scan.nextLine().trim());
            double deliveryCharge = Double.parseDouble(scan.nextLine().trim());
            Order order;
            if(userType.equalsIgnoreCase("Normal")){
                order=new NormalUser(orderId, customerName, totalAmount, deliveryCharge);
            }else{
                order=new PrimeUser(orderId, customerName, totalAmount, deliveryCharge);
            }
            order.display(userType);
            
        }
    }
}
```


## OUTPUT:

<img width="788" height="721" alt="image" src="https://github.com/user-attachments/assets/74de65ed-491e-4fba-868e-ea256645acb3" />


## RESULT:

The program successfully reads three food orders, identifies the user type (Normal or Prime), calculates the final payable amount using inheritance, and displays the complete order details with accurate billing.

