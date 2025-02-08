## BASIC IF ELSE PROGRAMS 

## 1.Check whether a number is positive or negative.


````java[]
import java.util.*;
public class positive
{
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        if (n < 0)
        {
            System.out.println("The number is negative");
        }
        else
        {
            System.out.println("The number is positive");
        }
    }
}

OUTPUT:

2
positive

````

## 2.Check whether a number is even or odd.

````java[]

import java.util.*;
public class even
{
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        if (n % 2 == 0)
        {
            System.out.println("The number is even");
        }
        else
        {
            System.out.println("The number is odd");
        }
    }
}

OUTPUT:
7
The number is odd.

````
## 3.Check whether a number is divisible by 3 and 5.

````java[]
import java.util.*;
public class divisible
{
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        if (n % 3 == 0 && n % 5 == 0)
        {
            System.out.println("The number is divisible by 3 and 5");
        }
        else
        {
            System.out.println("The number is not divisible by 3 and 5");
        }
    }
}

OUTPUT:
15
The number is divisible by 3 and 5.
````

## 4.Find the largest of three numbers.

````java[]
import java.util.*;
public class largest
{
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
        if(a>b && a>c)
        {
            System.out.println(a + "number is the greatest");
        }
        else if(b>a && b>c)
        {
            System.out.println(b + "number is the greatest");
        }
        else
        {
            System.out.println(c + "number is the greatest");
        }

    }
}
OUTPUT:
2 3 56
56 is the greatest.

````
## 5.Check whether a number is a prime number.

````java[]
import java.util.*;
public class prime
{
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();;
        if (num <= 1)
        {
            System.out.println("It is not a prime number");
        }

        for(int i =2;i<num-1;i++)
        {
            if(num % i == 0)
            {
                System.out.println("It is not a prime number");
            }
      
        }
        System.out.println("It is a prime number");
    }
}
Output:
7
It is a prime number.

````
## 6.Check whether a year is a leap year.

````[]java

import java.util.*;
public class year
{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        int year = sc.nextInt();
        if(year % 4 == 0 || (year%400 == 0 && year%100!=0))
        {
            System.out.println("It is a leap year");
        }
        else {
            System.out.println("It is not a leap year");
        }
    }
}

OUTOUT:
2020
It is a leap year.
````

## 7.Find the greatest of four numbers.

````[]java
import java.util.*;
public class greatest4{
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
        int d = sc.nextInt();
        if(a>b && a>c && a>d)
        {
            System.out.println(a + "is the greatest");
        }
        else if(b>a && b>c && b>d)
        {
            System.out.println(b + "is the greatest");
        }
        else if(c>a && c>b && c>d)
        {
            System.out.println(c + "is the greatest");
        }
        else {
            System.out.println(d + "is the greatest");
        }
    }
}

OUTPUT:
455 50 20 30
455 is the greatest.

````

## 8.Check if a number is a palindrome.

````[]java

import java.util.*;
public class palindrome
{
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int a;
        int b = 0;
        int temp = n;
        while(n!=0)
        {
            a = n%10;
            b = b*10+a;
            n = n/10;
        }
        System.out.println(b);

        if(temp == b)
        {
            System.out.println("Palindrome number");
        }
        else {
            System.out.println("Not a Palindrome number");
        }
    }
}

OUTPUT:
123321
It is a palindrome.

````
## 9.Check whether a character is a vowel or consonant.

````[]java

import java.util.*;
public class vowel
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        String ch = sc.next();
        ch.toLowerCase();
        if(ch=="a" || ch=="e" || ch=="i" || ch == "o" || ch == "u")
        {
            System.out.println("It is a vowel");
        }
        else {
            System.out.println("It is a consonant");
        }

    }
}

OUTPUT:
jkhf
It is constant.

````

## 10.Find the smallest of three numbers

````java[]
import java.util.*;
public class smallest
{
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
        if(a<b && a<c)
        {
            System.out.println(a + "number is the smallest");
        }
        else if(b<a && b<c)
        {
            System.out.println(b + "number is the smallest");
        }
        else
        {
            System.out.println(c + "number is the smallest");
        }

    }
}

OUTPUT:
34 5 7
5 is the smallest number.

````
## 11.Check if a number is prime or not using a simple loop.

````java[]
import java.util.*;
public class prime
{
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();;
        if (num <= 1)
        {
            System.out.println("It is not a prime number");
        }

        for(int i =2;i<num-1;i++)
        {
            if(num % i == 0)
            {
                System.out.println("It is not a prime number");
            }
        //System.out.println("It is a prime number");
        }
        System.out.println("It is a prime number");
    }
}

OUTPUT:
7
It is a prime number.

````
## 12.Check if a number is perfect or not.

````java[]
import java.util.*;
public class perfect
{
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        if (n == 1)
        {
            System.out.println("Not a perfect Number");
        }
        int sum =1;
        for(int i=2;i<n;i++)
        {
            if(n%i==0)
            {
                sum += i;
            }
        }
        if (sum==n)
        {
            System.out.println("It is a perfect number");
        }
        else {
            System.out.println("It is not a perfect number");
        }
    }
}
OUTPUT:
5
It is not a perfect number

````
## 13.Find whether a number is Armstrong or not.
````java[]
import java.util.*;
public class armstrong
{
    public static  void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int a;
        int count = 0;
        int temp = n;
        int t = n;
        while(n!=0)
        {
            a=n%10;
            count++;
            n=n/10;
        }
        //System.out.println(count);
        double sum = 0;
        double result = 0;

        while(temp!=0)
        {
            a=temp%10;
            result = Math.pow(a,count);
            temp = temp/10;
            sum = sum + result;
        }
        //System.out.println(sum);
        if(t == sum)
        {
            System.out.println("It is a armstrong");
        }
        else {
            System.out.println("It is not a armstrong");
        }
    }
}

OUTPUT:
4524
It is not a armstrong

````

## 14.Calculate the factorial of a number using recursion.

````java[]

import java.util.*;
public class factorial
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int fact = 1;
        for(int i=1;i<n;i++)
        {
            fact = fact * i;
        }
        System.out.print(fact);
    }
}

OUTPUT:
6
120
````

## 15.Check whether a number is an automorphic number.

````java[]
import java.util.*;
public class automorphic
{
    public static void  main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int a = n*n;
        System.out.println(a);

        while(n>0)
        {
            if(n%10 != a%10)
            {
                System.out.println("Not an automorphic number");
                break;
            }
            n=n/10;
            a=a/10;

        }
        if(n==0)
        {
            System.out.println("It is an automorphic number");
        }

    }
}

Output:
5
25
It is an automorphic number.

````
## 16.Find if a number is a Fibonacci number.

````java[]
import  java.util.*;
public class fibnocci {
    public static  void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int a=0;
        int b=1;
        System.out.print(a+" ");
        System.out.print(b+" ");
        for(int i=0;i<=n;i++)
        {
            int c = a+b;
            a=b;
            b=c;
            System.out.print(c + " ");
        }
    }
}

OUTPUT:

5
0 1 1 2 3 5 8 13

````
## 17.Determine if a number is a perfect square.

````java[]

import java.util.*;
import java.lang.*;
public class perfectsquare {
    public static void main(String [] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int sqrt = (int)Math.sqrt(n);
        int b = sqrt*sqrt;
        if(n == b)
        {
            System.out.println("It is a perfect square");
        }
        else {
            System.out.println("It is not a perfect square");
        }

    }
}

Output:
4
It is a perfect square.

````

## 18.Count the number of digits in a number.

````java[]

import java.util.*;
public class numberofdigits {
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int count = 0;
        while(n>0)
        {
            int a = n%10;
            count++;
            n = n/10;
        }
        System.out.println("The number of digits present is " + count);
    }
}

Output:
12546987
The number of digits present is 8
````

## 19.Check whether a string is a palindrome.

````java[]

import java.util.*;
public class palindromestring {
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        String reversed = " ";
        for(int i=str.length()-1;i>=0;i--)
        {
            reversed += str.charAt(i);
        }
        if(str.equals(reversed))
        {
            System.out.println("It is a palindrome String");
        }
        else {
            System.out.println(("It is not a palindrome String"));
        }
    }
}
OUTPUT:
hello
It is not a palindrome String

````
## 20.Check if a string is an anagram of another string.

````java






