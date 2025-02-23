## Basic While loop questions

## 81.Print numbers from 1 to 10 using while loop. 
````java[]

import java.util.*;
public class prg1
{
    public static  void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        //int n = sc.nextInt();
        int n = 1;
        while(n<=10)
        {
            System.out.print(n + " ");
            n++;
        }
    }
}

OUTPUT:
1 2 3 4 5 6 7 8 9 10 .

````

## 82.Print all even numbers up to n using while loop. 

````java[]
import java.util.*;
public class prg3
{
    public static  void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int fact = 1;
        int i=n;
        while(i > 0)
        {
            fact = fact * i;
            i--;

        }

        System.out.println(fact);
    }
}

Output:

5
2 4

````


## 83.Calculate the factorial of a number using while loop.

````java[]

import java.util.*;
public class prg3
{
    public static  void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int fact = 1;
        int i=n;
        while(i > 0)
        {
            fact = fact * i;
            i--;

        }

        System.out.println(fact);
    }
}

Output:

6
720

````

## 84.Reverse a number using while loop. 

````java[]
import java.util.*;
public class prg4
{
    public static  void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int a;
        int b = 0;
        while(n!=0)
        {
            a = n%10;
            b = b*10+a;
            n= n/10;
        }
        System.out.println(b);
    }
}

Output:
65648
84656

````

## 85.Print Fibonacci series up to n terms using while loop. 

````java[]

import java.util.*;
public class prg5
{
    public static  void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int a=0,b=1;
        int count = 0;
        //int c = 0;
        while(count < n)
        {
            System.out.print(a + " ");
            int c = a+b;
            a = b;
            b = c;
            count++;
        }
        //System.out.print(c);

    }
}

OUTPUT:

10
0 1 1 2 3 5 8 13 21 34

````

## 86.Sum of digits of a number using while loop. 

````java[]
import java.util.*;
public class prg6
{
    public static  void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int sum = 0;
        while(n > 0)
        {
            sum += n % 10;
            n = n/10;

        }

        System.out.println(sum);
    }
}

Output:
54
9

````
## 87.Print all odd numbers up to n using while loop. 

````java[]
import java.util.*;
public class prg7
{
    public static  void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int i= 1;
        while(i<=n)
        {
            System.out.print(i + " ");
            i = i+2;
        }
    }
}

Output:

6
1 3 5

````

## 88.Find the sum of natural numbers using while loop.

````java[]
import java.util.*;
public class prg8
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        int sum=0;
        int i=0;

        while(i<=n) {
            sum+=i;
            i++;
        }
        System.out.println("Sum of first " + n + " natural numbers is: " + sum);

    }
}

OUTPUT:

Enter the value of n
9
Sum of first 9 natural numbers is: 45

````

## 89.Count the number of digits in a number using while loop. 

````java[]

import java.util.*;
public class prg9
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        int count=0;
        while(n!=0){
            int a=n%10;
            count++;
            n/=10;
        }
        System.out.print("count of the digit is: "+count);
    }
}

OUTPUT:

Enter the value of n
4568
count of the digit is: 4

````

## 90.Calculate the product of digits of a number using while loop. 

```java[]
import java.util.*;
public class productt
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        //int count=0;
        int a =1;
        int prod = 1;
        while(n!=0){
            a=n%10;
            prod = prod*a;
            n/=10;
        }
        System.out.print("count of the digit is: "+ prod);
    }
}

OUTPUT:

Enter the value of n
56
count of the digit is: 30

````
## 91.Find the largest prime number in a given range. 

````java[]

import java.util.*;
public class prg11 {
    public static boolean isprime(int n){
        if(n<2){
            return false;
        }
        int i=2;
        while(i<=n/2){
            if(n%i==0){
                return false;
            }
            i++;
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the  start value");
        int start=s.nextInt();
        System.out.println("Enter the end value");
        int end=s.nextInt();
        int n=end;
        int last=-1;
        while(start<=n){
            if(isprime(n)){
                last=n;
                break;
            }
            n--;
        }
        System.out.println("Largest prime number "+last);
    }
}

OUTPUT:

Enter the  start value
2
Enter the end value
70
Largest prime number 67

````

## 92.Print all prime numbers up to n using a while loop. 

````java[]

import java.util.*;
public class prg12 {
    public static boolean isprime(int n){
        if(n<2){
            return false;
        }
        int i=2;
        while(i<=n/2){
            if(n%i==0){
                return false;
            }
            i++;
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value");
        int m=s.nextInt();
        int n=2;
        while(n<=m){
            if(isprime(n)){
                System.out.print(n+" ");
            }
            n++;
        }
    }
}

OUTPUT:

Enter the value
45
2 3 5 7 11 13 17 19 23 29 31 37 41 43

````
## 93.Find the greatest common divisor (GCD) using while loop. 

````java[]

import java.util.*;
public class gcdgreatest
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the two value");
        int n1=s.nextInt();
        int n2=s.nextInt();
        while(n1!=n2){
            if(n1>n2){
                n1-=n2;
            }
            else{
                n2-=n1;
            }
        }
        System.out.println("Gcd of numbers "+n1);
    }
}

OUTPUT:
Enter the two value
15
30
Gcd of numbers 15

````
## 94.Implement a simple ATM menu using a while loop. 

````java[]

````

## 95.Reverse a string using while loop. 

````java[]

import java.util.*;
public class prg15
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the String");
        String str=s.nextLine();
        String rev="";
        int n=str.length()-1;
        int i=n;
        while(i>=0){
            rev+=str.charAt(i);
            i--;
        }
        System.out.println(rev);
    }
}

OUTPUT:

Enter the String
jasmine
enimsaj

````
## 96.Sum all odd numbers in a range using while loop. 

````java[]

import java.util.*;
public class prg16
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the start value");
        int start=s.nextInt();
        System.out.println("Enter the end value");
        int end=s.nextInt();
        int sum=0;
        int i=start;
        while(i<=end){
            if(i%2!=0){
                sum+=i;
            }
            i++;
        }
        System.out.println(" Sum all odd numbers in " +start+ " to " +end + " is: " + sum);
    }
}

OUTPUT:
Enter the start value
2
Enter the end value
45
Sum all odd numbers in 2 to 45 is: 528

````

## 97.Check if a number is prime using while loop. 

````java[]

import java.util.*;
public class prg17{


    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value");
        int n=s.nextInt();
        int flag = 0;
        int i=2;
        while(i<=n/2){
            if(n%i==0){
                flag=1;
                break;
            }
            i++;
        }

        if(flag==0){
            System.out.println(n +" is prime number");
        }
        else{
            System.out.println(n+" is not prime number");
        }
    }
}

OUTPUT:
Enter the value
73
73 is prime number

````
## 98.Find the factorial of a number using while loop. 

````java[]

import java.util.*;
public class prg18
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value");
        int n=s.nextInt();
        int i=1;
        int fact=1;
        while(i<=n){
            fact=fact*i;
            i++;
        }
        System.out.println(" Factorial of number "+fact);


    }
}

OUTPUT:

Enter the value
5
Factorial of number 120

````

## 99.Print even numbers from a range using while loop. 

````java[]

import java.util.*;
public class prg19
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the start value");
        int start=s.nextInt();
        System.out.println("Enter the end value");
        int end=s.nextInt();
        int i=start;
        System.out.println("Even number");
        while(i<=end){
            if(i%2==0){
                System.out.print(i+" ");
            }
            i++;
        }
    }
}

OUTPUT:

Enter the start value
2
Enter the end value
22
Even number
2 4 6 8 10 12 14 16 18 20 22

````

## 100.Find the sum of even and odd digits of a number.

````java[]

import java.util.*;
public class prg20
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value");
        int n=s.nextInt();
        int sumodd=0;
        int sumeven=0;
        while(n!=0){
            int a=n%10;
            if(a%2!=0){
                sumodd+=a;
            }
            else{
                sumeven+=a;
            }
            n/=10;
        }
        System.out.println("sum of the even digit "+sumeven);
        System.out.println("sum of the odd digit "+ sumodd);

    }
}

Enter the value
5236489
sum of the even digit 20
sum of the odd digit 17

````


