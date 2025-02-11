## FOR LOOP QUESTIONS

## 61.Print numbers from 1 to 10 using for loop. 

````java[]
import java.util.*;
public class prg1 {
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        //int n = sc.nextInt();
        for(int i=1;i<=10;i++)
        {
            System.out.print(i + " ");
        }
    }
}

OUTPUT:
1 2 3 4 5 6 7 8 9 10

````
## 62. Print the multiplication table of a number using for loop. 

````java[]

import java.util.*;
public class prg2
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();

        for(int i=1;i<=10;i++){
            System.out.println(i+"*"+n+"="+(i*n));

        }


    }
}

OUTPUT:
6
1*6=6
2*6=12
3*6=18
4*6=24
5*6=30
6*6=36
7*6=42
8*6=48
9*6=54
10*6=60

````

## 63.Calculate the factorial of a number using a for loop. 

````java[]

import java.util.*;
public class prg3
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        int fact=1;
        for(int i=1;i<=n;i++){
            fact=fact*i;
        }
        System.out.println("factorial of "+n+"is :"+fact);
    }
}

OUPUT:

Enter the value of n
5
factorial of 5 is :120

````
## 64. Print Fibonacci series up to n terms using for loop. 

````java[]

import java.util.*;
public class prg4{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        int a=0;
        int b=1;
        System.out.println("fibonacci of "+n+" is :");
        System.out.print(a+" "+b+" ");
        for(int i=1;i<=n;i++){
            int c=a+b;
            a=b;
            b=c;

            System.out.print(c+" ");
        }
    }
}

OUTPUT:

Enter the value of n
10
fibonacci of 10 is :
0 1 1 2 3 5 8 13 21 34 55 89

````

## 65. Sum of digits of a number using a for loop. 

````java[]

import java.util.*;
public class prg5
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        int sum=0;
        for(int i=n;i>0;i/=10){
            int a=i%10;
            sum+=a;
        }
        System.out.print("sum of the digit "+n+" is: "+sum);
    }
}

OUTPUT:

Enter the value of n
12345
sum of the digit 12345 is: 15

````
## 66. Print prime numbers up to a given number using for loop. 

````java[]
import java.util.*;
import java.lang.*;
public class prg6{
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
1
20
 Prime number between 1 to 20
2 3 5 7 11 13 17 19

````
## 67. Reverse a number using for loop. 

````java[]


import java.util.*;
public class prg7
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        int b=0;
        for(int i=n;i>0;i/=10){
            int a=i%10;
            b=b*10+a;
        }
        System.out.print("Reverse a digit "+n+" is: "+b);
    }
}

OUTPUT:

Enter the value of n
21546
Reverse a digit 21546 is: 64512

````
## 68. Check whether a number is prime or not using a for loop. 

````java[]
import java.util.*;
public class prg8{


    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value");
        int n=s.nextInt();
        int flag=0;
        for(int i=2;i<=n/2;i++){
            if(n%i==0){
                flag=1;
                break;
            }
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
13
13 is prime number

````

## 69.Calculate the sum of even numbers from 1 to n using a for loop. 

````java[]
import java.util.*;
public class prg9
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        int sum=0;
        for(int i=0;i<=n;i++){
            if(i%2==0){
                sum+=i;
            }
        }
        System.out.println("Sum of the even number from 1 to "+n+":"+sum);
    }
}

OUTPUT:

Enter the value of n
10
Sum of the even number from 1 to 10:30

````
## 70.Calculate the sum of odd numbers from 1 to n using a for loop.

````java[]

import java.util.*;
public class prg10
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        int sum=0;
        for(int i=0;i<=n;i++){
            if(i%2!=0){
                sum+=i;
            }
        }
        System.out.println("Sum of the odd number from 1 to "+n+":"+sum);
    }
}

OUTPUT:

Enter the value of n
10
Sum of the odd number from 1 to 10:25

````

## 71. Print a pyramid pattern using for loop. 

````java[]

import java.util.*;
public class prg11
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        for(int i=1;i<=n;i++){
            for(int k=1;k<=n-i;k++){
                System.out.print("  ");
            }
            for(int j=1;j<=(2*i)-1;j++){

                System.out.print(" *");
            }
            System.out.println();
        }
    }
}

OUTPUT:

5
         *
       * * *
     * * * * *
   * * * * * * *
 * * * * * * * * *

````

## 72. Print a reverse triangle pattern using for loop. 

````java[]

import java.util.*;
public class prg12
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        for(int i=n;i>0;i--){
            for(int k=1;k<=n-i;k++){
                System.out.print("  ");
            }
            for(int j=1;j<=(2*i)-1;j++){

                System.out.print(" *");
            }
            System.out.println();
        }
    }
}

OUTPUT:

5
 * * * * * * * * *
   * * * * * * *
     * * * * *
       * * *
         *

````

## 73. Find the largest number in an array using a for loop. 

````java[]
import java.util.*;
public class prg13
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the sizee of the array");
        int n=s.nextInt();
        int a[]=new int[n];
        System.out.println("Enter the Elements");
        for(int i=0;i<n;i++){
            a[i]=s.nextInt();
        }
        int max=a[0];
        for(int i=0;i<n;i++){
            if(max<a[i]){
                max=a[i];
            }
        }
        System.out.println("Maximum of the element "+max);
    }
}

OUTPUT:
Enter the sizee of the array
5
Enter the Elements
22
45
62
10
15
Maximum of the element 62

````
## 74. Print a series of squares (1, 4, 9, ...) using for loop. 

````java[]
import java.util.*;
public class prg14
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the n value");
        int n=s.nextInt();
        System.out.println("square range of 1 to "+ n+" :");
        for(int i=1;i<=n;i++){
            System.out.print((i*i)+" ");

        }
    }
}

OUTPUT:

Enter the n value
10
square range of 1 to 10 :
1 4 9 16 25 36 49 64 81 100

````
## 75. Count the number of even numbers in a range.

````java[]
import java.util.*;
public class prg15
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the start value of range");
        int start=s.nextInt();
        System.out.println("Enter the end value of range");
        int end=s.nextInt();
        int count=0;
        for(int i=start;i<=end;i++){
            if(i%2==0){
                count++;
            }
        }
        System.out.println("count of the even number from "+ start+" to " + end+ " :"+count);
    }
}

OUTPUT:

Enter the start value of range
1
Enter the end value of range
15
count of the even number from 1 to 15 :7

````

## 76. Print all prime numbers between two numbers. 

````java[]
import java.util.*;
import java.lang.*;
public class prg6{
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
1
20
 Prime number between 1 to 20
2 3 5 7 11 13 17 19

````
## 77. Find the sum of all elements in an array using a for loop. 

````java[]
import java.util.*;
public class prg17
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the size of the array");
        int n=s.nextInt();
        int a[]=new int[n];
        System.out.println("Enter the Elements");
        for(int i=0;i<n;i++){
            a[i]=s.nextInt();
        }

        int sum=0;
        for(int i=0;i<n;i++){
            sum+=a[i];
        }
        System.out.println("Sum of the element "+sum);
    }
}

OUTPUT:

Enter the size of the array
5
Enter the Elements
1
2
3
4
5
Sum of the element 15

````
## 78.Calculate the average of an array using a for loop. 

````java[]

import java.util.*;
public class prg18
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the size of the array");
        int n=s.nextInt();
        int a[]=new int[n];
        System.out.println("Enter the Elements");
        for(int i=0;i<n;i++){
            a[i]=s.nextInt();
        }

        int sum=0;
        for(int i=0;i<n;i++){
            sum+=a[i];
        }
        int avg=sum/n;
        System.out.println("Average of the element "+avg);
    }
}

OUTPUT:

Enter the size of the array
5
Enter the Elements
5
10
15
20
25
Average of the element 15

````

## 79. Print a number pattern using for loop. 

````java[]
import java.util.*;
public class prg19
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        for(int i=1;i<=n;i++){
            for(int j=1;j<=i;j++){
                System.out.print(j+" ");
            }
            System.out.println();
        }

    }
}

OUTPUT:

5
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5

````
## 80.Print Pascal’s triangle using nested for loops. 

````java[]
import java.util.*;
public class prg20{
    public static void main(String args[]){
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        for(int i=1;i<=n;i++){
            int val=1;
            for(int j=1;j<=i;j++){
                System.out.print(val+" ");
                val=val*(i-j)/j;
            }
            System.out.println();
        }
    }
}

OUTPUT:
5
1 
1 1 
1 2 1 
1 3 3 1 
1 4 6 4 1

````






