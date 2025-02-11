## BASIC DO-WHILE LOOP

## 101.Print numbers from 1 to 10 using do-while loop. 

````java[]
import java.util.*;
public class prg1
{
    public static void main(String args[])
    {
        int i = 1;
        do{
            System.out.print(i + " ");
            i++;
        } while(i<=10);
    }
}

OUTPUT:
1 2 3 4 5 6 7 8 9 10

````
## 102.Sum of all even numbers using do-while loop. 

````java[]
import java.util.*;
public class prg2 {
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the value of n: ");
        int n = sc.nextInt();
        int i = 1;
        System.out.println("The sum of the even numbers: ");
        int sum = 0;
        do {

                if(i%2==0)
                {
                    sum += i;
                }
                i++;
            }while(i<=n);
            System.out.println(sum);

    }
}

OUTPUT:
Enter the value of n: 
20
The sum of the even numbers: 
110
````

## 103.Print all odd numbers in a range using do-while loop. 

````java[]
import java.util.*;
public class prg3 {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the value of n: ");
        int n = sc.nextInt();
        int i = 1;
        System.out.println("The sum of the odd numbers: ");
        int sum = 0;
        do {

            if (i % 2 != 0) {
                sum += i;
            }
            i++;
        } while (i <= n);
        System.out.println(sum);
    }
}

OUTPUT:
Enter the value of n: 
20
The sum of the odd numbers: 
100

````
## 104.Calculate the factorial of a number using do-while loop. 

````java[]
import java.util.*;
public class prg4 {
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the value of n:");

        int n = sc.nextInt();
        int fact = 1;
        int i=1;
        do{
            fact = fact*i;
            i++;
        }while(i<=n);
        System.out.println("Factorial of the number " + n +" is :" + fact );
    }
}

OUTPUT:

Enter the value of n:
5
Factorial of the number 5 is :120

````

## 105.Reverse a number using do-while loop. 

````java[]
import java.util.*;
public class prg5 {
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the value of n: ");
        int n = sc.nextInt();
        int a = 0;
        do {
            int b = n%10;
            a=a*10+b;
            n/=10;
        } while(n!=0);
        System.out.println("Reverse of the digit is " + n + " is: " + a);
    }
}

OUTPUT:

Enter the value of n: 
123546
Reverse of the digit is 0 is: 645321

````
## 106.Count the number of digits in a number using do-while loop.

````java[]

import java.util.*;
public class prg6 {
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the value of n: ");
        int n = sc.nextInt();
        int count = 0;
        do {
            int a = n%10;
            count++;
            n/=10;
        }while(n!=0);
        System.out.println("Count of the number of digits in a number is: " + count);
    }
}

OUTPUT:

Enter the value of n: 
1234
Count of the number of digits in a number is: 4

````
## 107.Check if a number is prime using do-while loop. 

````java[]
import java.util.*;
public class prg7 {
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the value of n: ");
        int n = sc.nextInt();
        int flag=0;
        int i=2;
        do{
            if(n%i==0)
            {
                flag=1;
                break;
            }
            i++;
        }while(i<=n/2);
        if(flag==0){
            System.out.println(n +" is prime number");
        }
        else{
            System.out.println(n+" is not prime number");
        }
    }
}

OUTPUT:

Enter the value of n: 
12
12 is not prime number

````

## 108.Find the GCD of two numbers using do-while loop. 

````java[]

import java.util.*;
public class prg8
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the two values");
        int n1=s.nextInt();
        int n2=s.nextInt();
        do{
            if(n1>n2){
                n1-=n2;
            }
            else{
                n2-=n1;
            }
        }	while(n1!=n2);
        System.out.println("Gcd of numbers "+n1);
    }
}

OUTPUT:

Enter the two values
10
20
Gcd of numbers 10

````

## 109.Print Fibonacci series up to n terms using do-while loop. 

````java[]

import java.util.*;
public class prg9 {
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the value: ");
        int n = sc.nextInt();
        int a = 0;
        int b = 1;
        System.out.println("Fibonacci of the num is: ");
        System.out.print(a+" "+b+" ");
        int i=1;
        do	{
            int c=a+b;
            a=b;
            b=c;

            System.out.print(c+" ");
            i++;
        }while(i<=n);
    }
}

OUTPUT:

Enter the value: 
10
Fibonacci of the num is: 
0 1 1 2 3 5 8 13 21 34 55 89

````
## 110.Check if a string is a palindrome using do-while loop.

````java[]

import java.util.*;
public class prg10
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Ënter the String");
        String str=s.next();
        String rev="";
        int i=str.length()-1;
        do{
            rev+=str.charAt(i);
            i--;
        }while(i>=0);

        if(rev.equals(str)){
            System.out.println("Palindrome");
        }
        else{
            System.out.println("Not Palindrome");
        }
    }
}

OUTPUT:

Ënter the String
daddy
Not Palindrome

````
## 111.Print a pattern of stars using do-while loop. 

````java[]

import java.util.*;
public class prg11
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        int i=1;
        do{
            int j=1;
            do{

                System.out.print("* ");
                j++;
            }while(j<=i);
            System.out.println();
            i++;
        }while(i<=n);
    }
}


OUTPUT:
5
* 
* * 
* * * 
* * * * 
* * * * * 
````

## 112.Sum all the digits of a number using do-while loop. 

````java[]
import java.util.*;
public class prg12
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        int sum=0;
        do{
            int a=n%10;
            sum+=a;
            n/=10;
        }while(n!=0);
        System.out.print("sum of the digit "+n+" is: "+sum);
    }
}

OUTPUT:

Enter the value of n
12245
sum of the digit 0 is: 14

````

## 113.Reverse a string using do-while loop. 

````java[]

public class prg13
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Ënter the String");
        String str=s.next();
        String rev="";
        int i=str.length()-1;
        do{
            rev+=str.charAt(i);
            i--;
        }while(i>=0);

        System.out.println("Reverse of the String " + rev);
    }
}

OUTPUT:

Ënter the String
nanthini
Reverse of the String is: inihtnan

````
## 114.Find the largest prime number in a given range using do-while. 

````java[]
import java.util.*;
public class prg14 {
    public static boolean isprime(int num){
        if(num<2){
            return false;
        }
        int i=2;
        do{
            if(num%i==0){
                return false;
            }
            i++;
        } while(i<=num/2);
        return true;
    }

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the  start value");
        int start=s.nextInt();
        System.out.println("Enter the end value");
        int end=s.nextInt();
        int num=end;
        int last=-1;
        do{
            if(isprime(num)){
                last=num;
                break;
            }
            num--;
        }while(start<=num);
        System.out.println("Largest prime number is  "+last);
    }
}

OUTPUT:

Enter the  start value
1
Enter the end value
20
Largest prime number is  19

````
##  115.Print all numbers divisible by 5 within a range using do-while. 

````java[]
import java.util.*;
public class prg15
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the start value");
        int start=s.nextInt();
        System.out.println("Enter the end value");
        int end=s.nextInt();
        System.out.println(" numbers in divisible by 5 within a range");
        int i=start;
        do{
            if(i%5==0){
                System.out.print(i+" ");
            }
            i++;

        }while(i<=end);

    }
}

OUTPUT:

Enter the start value
5
Enter the end value
60
 numbers in divisible by 5 within a range
5 10 15 20 25 30 35 40 45 50 55 60

````

## 116.Calculate the sum of squares of numbers in a range using do-while. 

````java[]
import java.util.*;
public class prg17
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the start value");
        int start=s.nextInt();
        System.out.println("Enter the end value");
        int end=s.nextInt();
        int sum=0;
        System.out.println("sum of square number");
        int i=start;
        do{
            sum+=(i*i);
            i++;

        }while(i<=end);
        System.out.print(sum);

    }
}

OUTPUT:

Enter the start value
2
Enter the end value
20
sum of square number
2869

````
## 117.Print the Fibonacci sequence up to a given limit using do-while. 
````java[]
import java.util.*;
public class prg16
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        int a=0;
        int b=1;
        System.out.println("fibonacci of "+n+" is :");
        System.out.print(a+" "+b+" ");
        int i=1;
        do	{
            int c=a+b;
            a=b;
            b=c;

            System.out.print(c+" ");
            i++;
        }	while(i<=n);
    }
}
OUTPUT:
Enter the value of n
10
fibonacci of 10 is :
0 1 1 2 3 5 8 13 21 34 55 89

````
## 118.Check if a number is a perfect number using do-while loop. 

````java[]
import java.util.*;
public class prg18 {


    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value");
        int n=s.nextInt();
        int temp=n;
        int sum=0;
        for(int i=1;i<n;i++){
            int rem=n%i;
            if(rem==0){
                sum+=i;
            }

        }
        if(temp==sum){
            System.out.println(n+ " is Perfect number");
        }
        else{
            System.out.println(n+" is not perfect number");
        }

    }

}

OUTPUT:

Enter the value
123
123 is not perfect number

````

## 119.Find the Armstrong number in a range using do-while loop. 
````java[]

import java.util.*;
import java.lang.*;
public class prg19
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the start value");
        int start=s.nextInt();
        System.out.println("Enter the end value");
        int end=s.nextInt();
        int i=start;
        do{
            int temp=i;
            int count=(int)Math.log10(i)+1;
            int a;
            double result=0;
            int num=temp;
            do	{
                a=num%10;
                result+=Math.pow(a,count);
                num/=10;
            }while(num!=0);
            if (result== temp) {
                System.out.println(temp + " is an Armstrong number.");
            }
            i++;

        }while(i<=end);

    }
}

OUTPUT:

500
153 is an Armstrong number.
370 is an Armstrong number.
371 is an Armstrong number.
407 is an Armstrong number.

````
## 120.Create a menu-driven program using a do-while loop. 

````java[]

````



