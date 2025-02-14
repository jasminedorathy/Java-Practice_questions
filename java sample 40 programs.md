## 1. Perfect,Abudant, Deficient Number
````java[]
import java.util.*;
public class prg1
{
    public static void main(String args[])
    {
            Scanner sc = new Scanner(System.in);
            int n = sc.nextInt();
            int sum = 0;
            for(int i=1;i<n;i++)
            {
                if(n%i==0)
                {
                    sum += i;
                }

            }
            if ( sum == n)
            {
                System.out.println("Perfect Number");
            }
            else if(sum > n)
            {
                System.out.println("Abudant number");
            }

            else {
                System.out.println("Deficient number");
            }
    }

}




 ````
  
## 2. LCM ,  GCD

````java[]

import java.util.*;
public class prg2
{
  public static void main(String args[])
  {
      Scanner sc = new Scanner(System.in);
      int n1 = sc.nextInt();
      int n2 = sc.nextInt();
      int a=n1;
      int b=n2;

      while(n1!=n2)
      {
          if(n1>n2)
          {
              n1-=n2;
          }
          else
          {
              n2-=n1;
          }
      }
      int gcd = n1;
      int lcm = (a*b)/gcd;

      System.out.println("LCM: " + lcm);
      System.out.println("GCD: " + gcd);
  }
}
OUTPUT:
12
18
LCM: 36
GCD: 6

````
## 3. Ampicable Pair
````java[]
import java.util.*;
public class prg3
{
    public static int sumofdivisors(int num)
    {
        int sum = 0;
        for(int i=1;i<num;i++)
        {
            if(num%i == 0)
            {
                sum += i;
            }
        }
        return sum;
    }
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();

        int sum1 = sumofdivisors(num1);
        int sum2 = sumofdivisors(num2);

        if(sum1 == num2 && sum2 == num1)
        {
            System.out.println("Amicable Pair");
        }
        else
        {
            System.out.println("Not an Amicable Pair");
        }
    }

}
OUTPUT:
10
20
Not an Amicable Pair

````


## 4. Betrothed Pair
````java[]
import java.util.*;
public class prg4
{
    public static int sumofdivisors(int num)
    {
        int sum = 0;
        for(int i=1;i<num;i++)
        {
            if(num%i == 0)
            {
                sum += i;
            }
        }
        return sum;
    }
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();

        int sum1 = sumofdivisors(num1);
        int sum2 = sumofdivisors(num2);

        if(sum1 == num2+1 && sum2 == num1+1)
        {
            System.out.println("Bethored Number");
        }
        else
        {
            System.out.println("Not a Bethored Number");
        }
    }

}
OUTPUT:
48
75
Bethored Number

````

## 5. Sqaure Free Numbers

````java[]
import java.util.*;
public class prg5 {
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();


        boolean isSquareFree = true;

        for (int i = 2; i <= n; i++) {
            if (n % (i * i) == 0) {
                isSquareFree = false;
                break;

            }
        }
        if (isSquareFree) {
            System.out.println("Square free number");
        } else {
            System.out.println("Not a square free number");
        }
    }
}


OUTPUT:



## 6. Ugly Number


## 7. Kaperakar Number
## 8. Armstrong NUmber
## 9. Adam Number
## 10. Digit Odd even Segregate
 11. Palindrome or Not(Digit)
 12.  Happy Number
 13. Pyramid Pattern
 14. Double Right Arrow(Butterfly Pattern)
 15.Hollow Square Pattern
 16.  Second Largest Element in the Array
 17. Majority Element
 18. Sum of Right side elements
 19. Left Rotation
 20. Swap those position values in the array
 21. Remove Duplicates
 22.Kth Largest element in the array
 23. Monotonic Array
 24. Array Odd Even Seggregation
 25. SLL reverse()
 26. DLL Search_Delete()
 27. SLL sort_unsorted()
 28. DLL Palindrome
 29. DLL SortedInsert()
 30. SLL reverse()
 31.Stock Buy and Sell – Max one Transaction Allowed
 32.Remove All Occurrences of an Element in an Array
 33.Remove duplicates from Sorted Array
 34.Minimum Swaps required to group all 1’s together
 35.Implement two Stacks in an Array                                                                                                                                                   36. How to efficiently implement k stacks in a single array?
 37.Implement Stack using Queues
 38.Inverted Right-Angle Triangle Pattern
 39.Pyramid Pattern
 40.Array Right Rotation
