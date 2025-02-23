## Other Complex Control Flow Statements 

## 141.Print a Fibonacci sequence using a recursive function. 

````java[]
import java.util.*;
public class prg21
{

    public static int fib(int n){
        if(n<=1){
            return n;
        }
        return fib(n-1)+fib(n-2);
    }
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the number");
        int n=s.nextInt();
        System.out.println("Fibnacci of number");
        for(int i=0;i<n;i++){
            System.out.print(fib(i)+" ");
        }
    }
}

OUTPUT:

Enter the number
15
Fibnacci of number
0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 

````

## 142.Implement a switch case that calculates tax based on income. 

````java[]
import java.util.*;
public class prg39{

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the income");
        double income=s.nextDouble();

        int taxBracket;
        if(income <= 10000) {
            taxBracket=0;
        }
        if(income <= 30000) {
            taxBracket=10;
        }
        if(income <= 70000) {
            taxBracket=20;
        }
        else {
            taxBracket=30;
        }

        double  tax;
        switch(taxBracket) {
            case 10:
                tax=income*0.10;
                break;

            case 20:
                tax=income*0.20;
                break;

            case 30:
                tax=income*0.30;
                break;
            default:
                tax=0;
                break;
        }
        System.out.println("your tax amount is: $"+tax);

    }

}

OUTPUT:
Enter the income
5000
your tax amount is: $1000.0

`````

## 143.Use a loop to generate prime numbers in a given range. 

````java[]
import java.util.*;
import java.lang.*;
public class prg22{
    public static boolean isPrime(int n){
        if(n==1){
            return false;
        }
        for(int i=2;i<=n/2;i++){
            if(n%i==0){
                return false;
            }
        }
        return true;
    }
    public static void range(int start,int end){
        System.out.println(" Prime number between "+ start +" to "+end);
        for(int i=start;i<end;i++){
            if(isPrime(i)){
                System.out.print(i+" ");
            }
        }
        System.out.println();

    }
    public static void main(String args[]){
        Scanner s=new Scanner(System.in);
        System.out.println("Ënter the Range");
        int start=s.nextInt();
        int end=s.nextInt();
        range(start,end);


    }
}

OUTPUT:

Ënter the Range
10
30
 Prime number between 10 to 30
11 13 17 19 23 29

````

## 144.Implement an input validation program with a loop. 

````java[]
import java.util.*;
public class prg26
{
    public static void main(String[] args) {

        Scanner s=new Scanner(System.in);
        int number;
        while(true){
            System.out.println("Enter the positive number");
            if(s.hasNextInt()){
                number=s.nextInt();
                if(number>0){
                    break;
                }
                else{
                    System.out.println("Error: Please enter positive number");
                }
            }
            else{
                System.out.println("invalid input: please enter integer");
                s.next();
            }
        }
        System.out.println("valid input received "+ number);

    }
}

OUTPUT:

Enter the positive number: 5
valid input received 5

````
## 145.Check if a number is an Armstrong number recursively.

````java[]
import java.util.Scanner;
public class prg24 {
    static int armstrongsum(int num, int power) {
        if (num == 0)
            return 0;
        int digit = num % 10;
        return (int) Math.pow(digit, power) + armstrongsum(num / 10, power);
    }
    static boolean isArmstrong(int num) {
        int numDigits = Integer.toString(num).length();
        return num == armstrongsum(num, numDigits);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int num = sc.nextInt();
        sc.close();

        if (isArmstrong(num))
            System.out.println(num + " is an Armstrong number.");
        else
            System.out.println(num + " is not an Armstrong number.");
    }
}

OUTPUT:

Enter a number: 60
60 is  annot Armstrong number.

````
## 146.Implement binary search in a sorted array. 

````java[]
import java.util.*;
public class prg25
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the size of the array");
        int n=s.nextInt();
        int[] a=new int[n];
        System.out.println("Enter the element");
        for(int i=0;i<n;i++){
            a[i]=s.nextInt();
        }
        System.out.println("Enter the target");
        int target=s.nextInt();
        int start=0;
        int end=a.length-1;
        int flag=0;
        while(start<=end){
            int mid=(start+end)/2;
            if(a[mid]==target){
                flag=1;
                System.out.println("Element Found: "+mid);
                break;
            }
            else if(a[mid]<target){
                start=mid+1;
            }
            else{
                end=mid-1;
            }
        }
        if(flag==0){
            System.out.println("Element Not found");
        }
    }
}

OUTPUT:

Enter the size of the array
5
Enter the element
2
5
8
6
4
Enter the target
5
Element Found: 1


````
## 147.Implement linear search for a number in an array. 

````java[]
import java.util.*;
public class prg23
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the size of the array");
        int n=s.nextInt();
        int[] a=new int[n];
        System.out.println("Enter the element");
        for(int i=0;i<n;i++){
            a[i]=s.nextInt();
        }
        System.out.println("Enter the target");
        int target=s.nextInt();
        int flag=0;
        for(int i=0;i<n;i++){
            if(a[i]==target){
                flag=1;
            }

        }
        if(flag==1){
            System.out.println("Element is found");
        }
        else{
            System.out.println("Element is not found");
        }

    }
}

OUTPUT:

Enter the size of the array
5
Enter the element
20
45
655
2
15
Enter the target
22
Element is not found

````
## 148.Find the largest number using a method and return the result. 

````java[]
import java.util.*;
public class prg27
{

    public static int largest(int a,int b,int c){
        if(a>b && a>c){
            return a;
        }
        else if(b>a && b>c){
            return b;
        }
        else{
            return c;
        }
    }
    public static void main(String[] args) {
        System.out.println("Enter the value of a and b and c");
        Scanner s=new Scanner(System.in);
        int a=s.nextInt();
        int b=s.nextInt();
        int c=s.nextInt();
        int result=	largest(a,b,c);
        System.out.println("largets element "+result);

    }
}

OUTPUT:

Enter the value of a and b and c
45
65
25
largest element 65.

````
## 149.Count the occurrence of each character in a string. 
````java[]
import java.util.*;
public class prg28
{
    public static void main(String[] args) {
        System.out.println("Enter the String");
        Scanner s=new Scanner(System.in);
        String str=s.nextLine();
        int[] count=new int[256];
        for(char ch:str.toCharArray()){
            count[ch]++;
        }
        for(int i=0;i<256;i++){
            if(count[i]>0){
                System.out.println((char)i +": "+count[i]);
            }
        }

    }
}

OUTPUT:
Enter the String
Jasmine
J: 1
a: 1
e: 1
i: 1
m: 1
n: 1
s: 1

````

## 150.Perform matrix multiplication using nested loops. 

````java[]
import java.util.*;
public class prg29
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the number of rows");
        int row=s.nextInt();
        System.out.println("Enter the number of column");
        int col=s.nextInt();
        int[][] a=new int[row][col];
        int[][] b=new int[row][col];
        int[][] mul=new int[row][col];
        System.out.println("Enter the first matrix element");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                a[i][j]=s.nextInt();
            }
        }
        System.out.println("Enter the  second matrix element");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                b[i][j]=s.nextInt();
            }
        }

        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                for(int k=0;k<col;k++)
                    mul[i][j] +=a[i][k]*b[k][j];
            }
        }


        System.out.println("Multipliction of the matrix");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                System.out.print(mul[i][j]+" ");
            }
            System.out.println();
        }
    }
}

OUTPUT:

Enter the number of rows
2
Enter the number of column
2
Enter the first matrix element
24
25
5
8
Enter the  second matrix element
4
3
8
9
Multipliction of the matrix
296 297 
84 87 

````
## 151.Implement a stack data structure using control flow statements. 

````java[]
import java.util.Scanner;

class Stack {
    private int top;
    private int size;
    private int[] a;


    public Stack(int size) {
        this.size = size;
        this.a = new int[size];
        this.top = -1;
    }

    public void push(int data) {
        if (top == size - 1) {
            System.out.println("Stack is full! Cannot push " + data);
        } else {
            a[++top] = data;
            System.out.println("Pushed: " + data);
        }
    }


    public void pop() {
        if (top == -1) {
            System.out.println("Stack is empty! Nothing to pop.");
        } else {
            System.out.println("Popped: " + a[top--]);
        }
    }


    public void peek() {
        if (top == -1) {
            System.out.println("Stack is empty! No top element.");
        } else {
            System.out.println("Top element: " + a[top]);
        }
    }

    public void display() {
        if (top == -1) {
            System.out.println("Stack is empty.");
        } else {
            System.out.print("Stack elements: ");
            for (int i = top; i >= 0; i--) {
                System.out.print(a[i] + " ");
            }
            System.out.println();
        }
    }
}

public class peg30{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter the size of the stack: ");
        int size = s.nextInt();

        Stack stack = new Stack(size);

        while (true) {
            System.out.println("\n1. Push  2. Pop  3. Peek  4. Display  5. Exit");
            System.out.print("Choose an option: ");
            int choice = s.nextInt();

            if (choice == 1) {
                System.out.print("Enter value to push: ");
                int value = s.nextInt();
                stack.push(value);
            } else if (choice == 2) {
                stack.pop();
            } else if (choice == 3) {
                stack.peek();
            } else if (choice == 4) {
                stack.display();
            } else if (choice == 5) {
                System.out.println("Exiting...");
                break;
            } else {
                System.out.println("Invalid choice! Try again.");
            }
        }
    }
}

OUTPUT:

Enter the size of the stack: 5

1. Push  2. Pop  3. Peek  4. Display  5. Exit
Choose an option: 1
Enter value to push: 30
Pushed: 30

````

## 152.Implement a queue using loops and conditional statements. 

````java[]

import java.util.*;
class Queue{
    int size,front,rear;
    int a[];
    public Queue(int size){
        this.size=size;
        this.a=new int[size];
        this.front=-1;
        this.rear=-1;
    }

    public void enqueue(int data){
        if(rear==size-1){
            System.out.println("Queue full");
        }
        else{
            if(front==-1){
                front=0;
            }
            a[++rear]=data;
            System.out.println("Enqueue " + data);
        }
    }
    public void dequeue(){
        if(front==-1 || front>rear){
            System.out.println("Queue empty");

        }
        else{
            System.out.println("Dequeue " +a[front++]);
        }
    }
    public void display(){
        for(int i=front;i<=rear;i++) {
            System.out.println(" Display the elements "+a[i]);

        }
    }
}

public class prg31{
    public static void main(String args[]){
        Scanner s=new Scanner(System.in);
        System.out.print("Enter the size of the queue: ");
        int size = s.nextInt();

        Queue q = new Queue(size);

        while (true) {
            System.out.println("\n1. Enqueue  2. Dequeue   3. Display  4. Exit");
            System.out.print("Choose an option: ");
            int choice = s.nextInt();

            if (choice == 1) {
                System.out.print("Enter value to enqueue: ");
                int value = s.nextInt();
                q.enqueue(value);
            } else if (choice == 2) {
                q.dequeue();

            } else if (choice == 3) {
                q.display();
            } else if (choice == 4) {
                System.out.println("Exiting...");
                break;
            } else {
                System.out.println("Invalid choice! Try again.");
            }
        }
    }
}

OUTPUT:
Enter the size of the queue: 5

1. Enqueue  2. Dequeue   3. Display  4. Exit
Choose an option: 1
Enter value to enqueue: 30
Enqueue 30

1. Enqueue  2. Dequeue   3. Display  4. Exit
Choose an option: 1
Enter value to enqueue: 20
Enqueue 20

1. Enqueue  2. Dequeue   3. Display  4. Exit
Choose an option: 1
Enter value to enqueue: 50
Enqueue 50

1. Enqueue  2. Dequeue   3. Display  4. Exit
Choose an option: 1
Enter value to enqueue: 40
Enqueue 40

1. Enqueue  2. Dequeue   3. Display  4. Exit
Choose an option: 1
Enter value to enqueue: 60
Enqueue 60

1. Enqueue  2. Dequeue   3. Display  4. Exit
Choose an option: 1
Enter value to enqueue: 30
Queue full

````
## 153.Create a simple bank account with multiple operations. 

````java[]

import java.util.*;
class BankAccoun{
    String AccountHolderName;
    String AccountNumber;
    double balance;

    BankAccoun(String AccountHolderName,String AccountNumber,double balance){
        this.AccountHolderName=AccountHolderName;
        this.AccountNumber=AccountNumber;
        this.balance=balance;
    }

    public void deposit(double amount) {
        if(amount>0) {
            balance+=amount;
            System.out.println("Deposit $ "+amount);
        }
        else {
            System.out.println("invalid amount");
        }
    }

    public void withdraw(double amount) {
        if(amount>0 && amount<=balance) {
            balance-=amount;
            System.out.println("Withdraw $ "+ balance);
        }
        else {
            System.out.println("Invalid amount or insufficient balance");
        }
    }

    public void checkbalance() {
        System.out.println("Balance Amount $ : " + balance);
    }
    public void detail() {
        System.out.println("Account Holder Name: " + AccountHolderName);
        System.out.println("Account Number: " + AccountNumber);
        System.out.println("Balance Amount $ : " + balance);
    }
}
public class prg32{

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the Account Holder Name");
        String AccountHolderName=s.nextLine();
        System.out.println("Enter the Account Number");
        String AccountNumber=s.nextLine();
        System.out.println("Enter the Initial Balance");
        double  balance=s.nextDouble();
        BankAccoun b=new BankAccoun(AccountHolderName,AccountNumber,balance);
        while(true) {
            System.out.println("\nChoose an operation:");
            System.out.println("1. Deposit");
            System.out.println("2. Withdraw");
            System.out.println("3. Check Balance");
            System.out.println("4. Account Details");
            System.out.println("5. Exit");
            System.out.print("Enter choice: ");
            int choice = s.nextInt();

            switch(choice) {
                case 1:
                    System.out.println("Enter the deposit amount");
                    double amount=s.nextDouble();
                    b.deposit(amount);
                    break;

                case 2:
                    System.out.println("Enter the withdraw amount");
                    double withdrawamount=s.nextDouble();
                    b.deposit(withdrawamount);
                    break;

                case 3:
                    b.checkbalance();
                    break;

                case 4:
                    b.detail();
                    break;

                case 5:
                    System.out.println("Thank you");
                    return;
                default:
                    System.out.println("invalid choice, please Enter valid choice");

            }
        }
    }

}

OUTPUT:

Enter the Account Holder Name
Jasmine
Enter the Account Number
125436658
Enter the Initial Balance
2000

Choose an operation:
1. Deposit
2. Withdraw
3. Check Balance
4. Account Details
5. Exit
Enter choice: 3
Balance Amount $ : 2000.0


````

## 154.Implement a simple ticket reservation system. 

````java[]

import java.util.*;
class Ticket{
    String passengername;
    String Trainnumber;
    int seatnumber;
    boolean isReserved;

    Ticket(String passengername,String Trainnumber,int seatnumber){
        this.passengername=passengername;
        this.Trainnumber=Trainnumber;
        this.seatnumber=seatnumber;
        this.isReserved=true;
    }

    public void cancelTicket() {
        if(isReserved) {
            isReserved=false;
            System.out.println("Reservation cancel for this seat "+seatnumber);
        }
        else {
            System.out.println("No Reservation found");
        }
    }

    public void detail() {
        if(isReserved) {
            System.out.println("Passenger Name: " + passengername);
            System.out.println("Train Number: " + Trainnumber);
            System.out.println("Seat number: " + seatnumber);
        }
        else{
            System.out.println("No Reservation found");
        }
    }
}
public class prg33{

    public static void main(String[] args) {
        ArrayList<Ticket> booking=new ArrayList<>();
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the Passenger Name");
        String passengername=s.nextLine();
        System.out.println("Enter the Train Number");
        String Trainnumber=s.nextLine();
        System.out.println("Enter the Seat Number");
        int  seatnumber=s.nextInt();
        Ticket b=new Ticket(passengername,Trainnumber,seatnumber);
        while(true) {
            System.out.println("\nChoose an operation:");
            System.out.println("1. Booking Ticket");
            System.out.println("2. Cancel Ticket");
            System.out.println("3. View Reservation");
            System.out.println("4. Exit");
            System.out.print("Enter choice: ");
            int choice = s.nextInt();

            switch(choice) {
                case 1:
                    booking.add(new Ticket(passengername, Trainnumber,seatnumber));
                    System.out.println("Ticket booked!");
                    break;

                case 2:
                    b.cancelTicket();
                    break;

                case 3:
                    b.detail();
                    break;

                case 4:
                    System.out.println("Thank you");
                    return;
                default:
                    System.out.println("invalid choice, please Enter valid choice");

            }
        }
    }

}

OUTPUT:

Enter the Passenger Name
Jasmine
Enter the Train Number
2
Enter the Seat Number
22

Choose an operation:
1. Booking Ticket
2. Cancel Ticket
3. View Reservation
4. Exit
Enter choice: 1
Ticket booked!

Choose an operation:
1. Booking Ticket
2. Cancel Ticket
3. View Reservation
4. Exit
Enter choice: 3
Passenger Name: Jasmine
Train Number: 2
Seat number: 22

Choose an operation:
1. Booking Ticket
2. Cancel Ticket
3. View Reservation
4. Exit
Enter choice: 4
Thank you


````
## 155.Write a program to calculate power using recursion. 

````java[]

import java.util.*;
public class prg34 {
    public static int power(int base,int exp) {
        if(exp==0) {
            return 1;
        }
        return base*power(base,exp-1);
    }

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the base");
        int base=s.nextInt();
        System.out.println("Enter the exponent");
        int exp=s.nextInt();
        int result=power(base,exp);
        System.out.println(base+" ^ "+ exp +"= "+ result);

    }

}

OUTPUT:


Enter the base
2
Enter the exponent
4
2 ^ 4 = 16

````

## 156.Implement recursive factorial calculation. 
````java[]

import java.util.*;
public class prg35
{
    public static int factorial(int n){
        if(n==0 || n==1){
            return 1;
        }
        return n*factorial(n-1);

    }
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value");
        int n=s.nextInt();
        int result=factorial(n);
        System.out.println(n+ " factorial is "+result);

    }
}

OUTPUT:

Enter the value
6
6 factorial is 720

````
## 157.Implement recursive Fibonacci sequence. 

````java[]

import java.util.*;
public class prg21
{

    public static int fib(int n){
        if(n<=1){
            return n;
        }
        return fib(n-1)+fib(n-2);
    }
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the number");
        int n=s.nextInt();
        System.out.println("Fibnacci of number");
        for(int i=0;i<n;i++){
            System.out.print(fib(i)+" ");
        }
    }
}

OUTPUT:

Enter the number
8
Fibnacci of number
0 1 1 2 3 5 8 13 

````
## 158.Create a number guessing game with loops and conditions. 

````java[]

import java.util.*;
public class prg36 {

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        Random random=new Random();

        int numberToGuess=random.nextInt(100)+1;
        int attempt=0;
        int userinput=0;
        System.out.println("  WELCOME TO NUMBER GUESSING GAME  ");
        System.out.println("  GUESS A NUMBER BETWEEN 1 AND 100 ");
        while(numberToGuess != userinput) {
            System.out.println("Enter the Guess");
            userinput=s.nextInt();
            attempt++;

            if(userinput < numberToGuess)
            {
                System.out.println("To low! Try Again");
            }
            else if(userinput> numberToGuess) {
                System.out.println("To high! Try Again");
            }
            else {
                System.out.println("Congratulations! You guessed the number in " + attempt + " attempts.");
            }
        }

    }

}

OUTPUT:

 WELCOME TO NUMBER GUESSING GAME  
  GUESS A NUMBER BETWEEN 1 AND 100 
Enter the Guess
50
To high! Try Again
Enter the Guess
22
To high! Try Again
Enter the Guess
10
To low! Try Again
Enter the Guess
2
To low! Try Again
````

## 159.Print a checkerboard pattern using nested loops. 

````java[]

import java.util.*;
public class prg37
{
    public static void main(String[] args) {


        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        for(int i=0;i<n;i++) {
            for(int j=0;j<n;j++) {
                if((i+j)%2==0) {
                    System.out.print("* ");
                }
                else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }

    }

}


OUTPUT:

5
*   *   * 
  *   *   
*   *   * 
  *   *   
*   *   *

````

## 160.Implement a vending machine system using switch statements. 

````java[]

import java.util.*;
public class prg38 {

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        System.out.println("  WELCOME TO CAFE  ");

        System.out.println("1. Sandwich");
        System.out.println("2. Coffee");
        System.out.println("3. Tea");
        System.out.println("4. Pastry");
        System.out.println("5. Juice");
        System.out.println("6. Exit");

        System.out.println("Enter your choice");
        int choice = s.nextInt();

        switch (choice) {
            case 1:
                System.out.println("You selected Sandwich!");
                break;
            case 2:
                System.out.println("You selected Coffee!");
                break;
            case 3:
                System.out.println("You selected Tea!");
                break;
            case 4:
                System.out.println("You selected Pastry!");
                break;
            case 5:
                System.out.println("You selected Juice!");
                break;
            case 6:
                System.out.println("** THANK YOU **");
                break;
            default:
                System.out.println("Invalid input! Please select a valid choice");
        }
    }
}


Output:
 WELCOME TO CAFE  
1. Sandwich
2. Coffee
3. Tea
4. Pastry
5. Juice
6. Exit
Enter your choice
5
You selected Juice!
````
