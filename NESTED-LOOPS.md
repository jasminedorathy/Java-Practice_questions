NESTED LOOPS PROGRAMS

## 121.Print a multiplication table using nested loops. 

````java[]
import java.util.*;
public class prg1
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

10
1*10=10
2*10=20
3*10=30
4*10=40
5*10=50
6*10=60
7*10=70
8*10=80
9*10=90
10*10=100

````

## 122.Print an inverted triangle pattern using nested loops.

````java[]
import java.util.*;
public class prg2
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        for(int i=n;i>=1;i--){
            for(int k=1;k<=n-i;k++){
                System.out.print(" ");
            }
            for(int j=1;j<=i;j++){

                System.out.print(" *");
            }
            System.out.println();
        }
    }
}

OUTPUT:

5
 * * * * *
  * * * *
   * * *
    * *
     *

````
## 123.Print a pyramid pattern using nested loops. 

````java[]
import java.util.*;
public class prg3
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
## 124.Print a diamond shape pattern using nested loops. 

````java[]

import java.util.*;
public class prg4
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        for(int i=1;i<=n;i++){
            for(int k=1;k<=n-i;k++){
                System.out.print(" ");
            }
            for(int j=1;j<=i;j++){

                System.out.print(" *");
            }
            System.out.println();
        }
        for(int i=n-1;i>=1;i--){
            for(int k=1;k<=n-i;k++){
                System.out.print(" ");
            }
            for(int j=1;j<=i;j++){

                System.out.print(" *");
            }
            System.out.println();
        }
    }
}


OUTPUT:

5
     *
    * *
   * * *
  * * * *
 * * * * *
  * * * *
   * * *
    * *
     *

````

## 125.Print a hollow square pattern using nested loops. 

````java[]

import java.util.*;
public class prg5
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();

        for(int i=1;i<=n;i++){
            for(int j=1;j<=n;j++){
                if(i==1 || i==n || j==1|| j==n){
                    System.out.print("* ");
                }
                else{
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }
}

OUTPUT:

5
* * * * * 
*       * 
*       * 
*       * 
* * * * *

````

## 126.Print a number triangle using nested loops. 

````java[]
import java.util.*;
public class prg6
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
## 127.Check for prime numbers within a range using nested loops. 

````java[]

import java.util.*;
import java.lang.*;
public class prg7{
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
10
 Prime number between 1 to 10
2 3 5 7

````
## 128.Generate Pascal's Triangle using nested loops. 

````java[]
import java.util.*;
public class prg8{
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

