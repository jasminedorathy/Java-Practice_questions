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
import java.util.*;
public class anagram
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Ënter the String");
        String str1=s.next();
        System.out.println("Ënter the string ");
        String str2=s.next();
        str1=str1.toLowerCase();
        str2=str2.toLowerCase();
        if(str1.length()!=str2.length())
        {
            System.out.println("both String not anagram");

        }
        else{
            char[] String1=str1.toCharArray();
            char[] String2=str2.toCharArray();

            Arrays.sort(String1);
            Arrays.sort(String2);
            if(Arrays.equals(String1,String2)==true){
                System.out.println("both String is Anagram");
            }
            else{
                System.out.println("both String not Anagram");
            }
        }
    }
}

Output:
Ënter the String
jasmine
Ënter the string 
jasmine
both String is Anagram

````
## 21.Check whether a number is a prime number within a range. 

````java[]

import java.util.*;
import java.lang.*;
public class primenumber{
    public static boolean isPrime(int n)
    {
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
        System.out.println("Prime number between "+ start +" to "+end);
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
Enter the Range
1
10
Prime number between 1 to 10
2 3 5 7

````
## 22.Find the largest number among n numbers using a nested if-else. 

````java[]

import java.util.*;
public class largestnumber
{
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=sc.nextInt();
        System.out.println("Enter the element");
        int max=sc.nextInt();
        for(int i=1;i<n;i++){
            int ele=sc.nextInt();
            if(max<ele){
                max=ele;
            }
        }
        System.out.println("Largest Element "+max);
    }
}

OUTPUT:

Enter the value of n
5
Enter the element
80
42
54
96
75
Largest Element 96

````
## 23.Print all prime numbers in a range using nested loops. 

````java[]
import java.util.*;
import java.lang.*;
public class primenumber{
    public static boolean isPrime(int n)
    {
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
        System.out.println("Prime number between "+ start +" to "+end);
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
Enter the Range
1
10
Prime number between 1 to 10
2 3 5 7

````
## 24.Find all the divisors of a number. 

````java[]
import java.util.*;
public class divisors
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=s.nextInt();
        System.out.println("Divisor of a number");
        for(int i=1;i<=n;i++){
            if(n%i==0){
                System.out.print(i+" ");
            }
        }
    }
}

OUTPUT:
Enter the value of n
8
Divisor of a number
1 2 4 8 

````
## 25.Find the GCD and LCM of two numbers. 

````java[]

import java.util.*;
public class LCMandGCD
{
    public static int gcd(int a,int b)
    {
        while(a!=b){
            if(a>b){
                a-=b;
            }
            else{
                b-=a;
            }
        }
        return a;
    }
    public static int lcm(int n1,int n2,int gcdvalue){
        return Math.abs(n1*n2)/gcdvalue;
    }
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the number");
        int a=s.nextInt();
        int b=s.nextInt();
        System.out.println("gcd of " +a+" and "+b);
        int gcdvalue=gcd(a,b);
        System.out.println(gcdvalue);
        System.out.println("lcm of " +a+" and "+b);
        int lcmvalue=lcm(a,b,gcdvalue);
        System.out.println(lcmvalue);

    }
}

Output:
Enter the number
45
54
gcd of 45 and 54
9
lcm of 45 and 54
270

````

## 26.Check if a number is a perfect number within a range.

````java[]

import java.util.*;
import java.lang.*;
public class perfectnumber{
    public static boolean isPerfect(int n){
        int a=(int)Math.sqrt(n);
        if((a*a)==n){
            return true;
        }
        else{
            return false;
        }
    }
    public static void range(int start,int end){
        System.out.println("Perfect number between "+ start +" to " +end);
        for(int i=start;i<end;i++){
            if(isPerfect(i)){
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
Output:
Ënter the Range
1
5
Perfect number between 1 to 5
1 4
````

## 27.Check whether an integer is positive, negative, or zero. 

````java[]
import java.util.*;
public class positivenegative
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value");
        int n=s.nextInt();
        if(n>0){
            System.out.println(n +" is positive");
        }
        else if(n==0)
        {
            System.out.println(n+" is zero");
        }
        else{
            System.out.println(n+" is negative");
        }
    }

}

Enter the value
23
23 is positive

````

## 28.Determine the type of a triangle based on its angles. 

````java[]
import java.util.*;
public class triangle {


    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter the First Angle");
        int n=sc.nextInt();
        System.out.println("Enter the Second Angle");
        int m=sc.nextInt();
        System.out.println("Enter the Third Angle");
        int o=sc.nextInt();
        int sum=n+m+o;
        if(sum==180) {
            if (n < 90 && m < 90 && o < 90) {
                System.out.println(" Acute Triangle ");
            } else if (n == 90 || m == 90 || o == 90) {
                System.out.println(" Right Triangle ");
            } else {
                System.out.println(" Obtuse Triangle ");
            }
        }
        else
        {
                System.out.println("Invalid");
        }

    }

}
Output:
Enter the First Angle
100
Enter the Second Angle
40
Enter the Third Angle
40
 Obtuse Triangle

````

## 29.Find whether a number is a Fibonacci number within a range. 

````java[]
import java.util.*;
import java.lang.*;
public class fibonorange{
    public static boolean fib(int n){
        if(n==0 || n==1){
            return true;
        }
        int a=0,b=1,c=0;
        while(c<n){

            c=a+b;
            a=b;
            b=c;

        }
        return c==n;
    }
    public static void range(int start,int end){
        System.out.println("Fibonacci number between "+ start +" to " +end);
        for(int i=start;i<end;i++){
            if(fib(i)){
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
40
80
Fibonacci number between 40 to 80
55

````

## 30.Print all leap years within a given range. 

````java[]

import java.util.*;
import java.lang.*;
public class leaprange{
    public static boolean leap(int n){
        if(n%4 ==0 || (n%400==0 && (n%100 !=0))){
            return true;
        }
        else{
            return false;
        }
    }
    public static void range(int start,int end){
        System.out.println("Leap Year  between "+ start +" to " +end);
        for(int i=start;i<end;i++){
            if(leap(i)){
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

Output:

Ënter the Range
2005
2060
Leap Year  between 2005 to 2060
2008 2012 2016 2020 2024 2028 2032 2036 2040 2044 2048 2052 2056

````
## 31.Check whether a string is a valid palindrome. 

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
## 32.Check for a specific pattern in a string using if-else. 

````java[]
import java.util.*;
public class pattern{
    public static void main(String args[]){
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the string");
        String str=s.nextLine();
        System.out.println("Enter the pattern");
        String pat=s.nextLine();
        if(str.contains(pat)){
            System.out.println("pattern found");
        }
        else{
            System.out.println("pattern Not found");
        }
    }
}

OUTPUT:

Enter the string
jasmine
Enter the pattern
jas
pattern found

````
## 33..Check if a given day is a weekend or weekday. 

````java[]

import java.util.*;
public class days
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the day");
        String day=s.next().toLowerCase();
        if(day.equals("sunday") || day.equals("saturday")){
            System.out.println("Weekend");
        }
        else{
            System.out.println("Weekday");
        }


    }
}

Output:

Enter the day
Monday
Weekday

````
## 34.Check if a number is divisible by 7 or 11. 

````java[]
import java.util.*;
public class divisible7 {


    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the value");
        int n=s.nextInt();
        if(n%7==0 && n%11==0){
            System.out.println(n +" is Divisible by 7 and 11");
        }
        else{
            System.out.println(n+" is not Divisible by 7 and 11");
        }
    }

}

Output:

Enter the value
75
75 is not Divisible by 7 and 11

````

## 35.Print prime numbers within a range using nested conditions.
````java[]

import java.util.*;
import java.lang.*;
public class primenumber{
    public static boolean isPrime(int n)
    {
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
        System.out.println("Prime number between "+ start +" to "+end);
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
Enter the Range
1
10
Prime number between 1 to 10
2 3 5 7

````
## 36.Identify if an alphabet character is uppercase, lowercase, or non-alphabet.

````java[]
import java.util.*;
public class alpha
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        char ch=s.next().charAt(0);

        if(ch>='A' && ch<='Z'){
            System.out.println("Given character is Upper case");
        }
        else if(ch>='a' && ch<='z'){
            System.out.println("Given character is Lower case");
        }
        else{
            System.out.println("Non alphabet");
        }


    }
}

OUTPUT:

L
Given character is Upper case
````

## 37.Determine if a given number is a valid credit card number. 

````java[]
import java.util.*;
public class creditcard
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the card number");
        long num=s.nextLong();
        long sum=0;
        boolean seconddigit=false;
        while(num>0){
            long digit=num%10;
            num/=10;
            if(seconddigit){
                digit=digit*2;
                if(digit>=10){
                    digit-=9;
                }
                sum+=digit;
                seconddigit=!seconddigit;
            }
        }
        if(sum%10==0){
            System.out.println("valid card number");
        }
        else{
            System.out.println("not valid number");
        }
    }
}

Output:

Enter the card number
12541589554645
valid card number

````

## 38. Check if a given date is valid or invalid.

````java[]

import java.util.*;
import java.time.LocalDate;
public class date
{
    
    public static boolean valid(int date,int month,int year){
        try{
        LocalDate.of(year,month,date);
        return true;
        }
        catch(Exception e){
            return false;
        }
    }
	public static void main(String[] args) {
	 Scanner s=new Scanner(System.in);
	 System.out.println("Enter the year");
	 int year=s.nextInt();
	  System.out.println("Enter the month");
	 int month=s.nextInt();
	  System.out.println("Enter the date");
	 int date=s.nextInt();
	 
	 if(valid(date,month,year)){
	     System.out.println("valid date");
	 }
	 else{
	     System.out.println(" Not valid date");
	 }
	 
	}	
}

Output:
Enter the year
2025
Enter the month
01
Enter the date
15
valid date

````

## 39.Find the day of the week for a given date. 

````java[]

import java.util.*;
import java.time.LocalDate;
import java.time.DayOfWeek;
public class Main
{
    

	public static void main(String[] args) {
	 Scanner s=new Scanner(System.in);
	 System.out.println("Enter the year");
	 int year=s.nextInt();
	  System.out.println("Enter the month");
	 int month=s.nextInt();
	  System.out.println("Enter the date");
	 int day=s.nextInt();
	 
	 try{
	 LocalDate date=LocalDate.of(year,month,day);
	 DayOfWeek week=date.getDayOfWeek();
	 System.out.println("Day of the week "+week);
	 }
	 catch(Exception e){
	     System.out.println("Invalid date");
	 }
	}	
}

Output:
Enter the year
2025
Enter the month
08
Enter the date
30
Day of the week SATURDAY

````
## 40. Print multiplication tables for a given number using nested loops. 

````java[]

import java.util.*;
public class multiplicationtable
{
    public static void main(String args[])
    {
        Scanner s = new Scanner(System.in);

        int n = s.nextInt();
        for(int i=1;i<=10;i++)
        {
            System.out.println(n + "*" + i + "=" + (i*n));
        }

    }
}

Output:
10
10*1=10
10*2=20
10*3=30
10*4=40
10*5=50
10*6=60
10*7=70
10*8=80
10*9=90
10*10=100

````



