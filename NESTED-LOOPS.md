## NESTED LOOPS PROGRAMS

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
## 129.Print a number pattern with asterisks using nested loops. 

````java[]

import java.util.*;
public class prg9
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        for(int i=1;i<=n;i++){
            for(int j=1;j<=i;j++){
                System.out.print("* ");
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

`````

## 130.Print all possible combinations of two arrays using nested loops. 

````java[]
import java.util.*;
public class prg10
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
                System.out.println("Enter the size of element");
                int n1=sc.nextInt();
                int[] a=new int[n1];
                System.out.println("Enter the element");
                for(int i=0; i<n1; i++)
                {
                    a[i]=sc.nextInt();
                }
                System.out.println("Enter the size of element");
                int n2=sc.nextInt();
                int[] b=new int[n1];
                System.out.println("Enter the element");
                for(int i=0;i<n2;i++)
                {
                    b[i]=sc.nextInt();
                }
                System.out.println("Possible Combination");
                for(int i=0;i<n1;i++)
                {
                    for(int j=0;j<n2;j++)
                    {
                        System.out.println("("+ a[i] +"," + b[j]+")");
                    }
                }

            }
        }

OUTPUT:


Enter the size of element
2
Enter the element
2
3
Enter the size of element
2
Enter the element
4
6
Possible Combination
(2,4)
(2,6)
(3,4)
(3,6)

````

## 131.Create a matrix and perform operations like transpose using nested loops. 

````java[]
import java.util.*;
public class prg11
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the number of rows");
        int row=s.nextInt();
        System.out.println("Enter the number of column");
        int col=s.nextInt();
        int[][] a=new int[row][col];
        int[][] transpose=new int[row][col];

        System.out.println("Enter the first matrix element");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                a[i][j]=s.nextInt();
            }
        }

        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                transpose[i][j]=a[j][i];
            }
        }
        System.out.println("Original matrix");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                System.out.print(a[i][j]+" ");
            }
            System.out.println();
        }


        System.out.println("Transpose of the matrix");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                System.out.print(transpose[i][j]+" ");
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
1
2
3
4
Original matrix
1 2 
3 4 
Transpose of the matrix
1 3 
2 4

````
## 132.Count the number of vowels and consonants in a string using nested loops. 

````java[]

import java.util.*;
public class prg12
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the string");
        String str=s.nextLine();
        int c1=0;
        int c2=0;
        str=str.toLowerCase();
        for(int i=0;i<=str.length()-1;i++){
            char ch=str.charAt(i);
            if(ch=='a' || ch=='e' || ch=='i'|| ch=='o'|| ch=='u'){
                c1++;
            }
            else{
                c2++;
            }
        }
        System.out.println(" number of vowels: "+c1);
        System.out.println(" number of consonant: "+c2);
    }
}

OUTPUT:

Enter the string
jasmine
 number of vowels: 3
 number of consonant: 4

````

## 133.Create a multiplication matrix using nested loops. 

````java[]
import java.util.*;
public class prg13
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of rows");
        int row= sc.nextInt();
        System.out.println("Enter the number of columns");
        int col = sc.nextInt();
        int [][] a = new int[row][col];
        int [][] b = new int[row][col];
        int [][] mul = new int[row][col];

        System.out.println("Enter the first matrix element");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                a[i][j]=sc.nextInt();
            }
        }

        System.out.println("Enter the second matrix element");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                b[i][j]=sc.nextInt();
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
Enter the number of columns
2
Enter the first matrix element
2
4
6
8
Enter the second matrix element
3
6
9
12
Multipliction of the matrix
42 60 
90 132

````
## 134.Print an alphabet pattern using nested loops. 

````java[]

import java.util.*;
public class prg14
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for(int i=1;i<n;i++)
        {
            for(char j='A';j<='A'+i;j++)
            {
                System.out.print(j+" ");
            }
            System.out.println();
        }
    }
}

OUTPUT:

5
A B 
A B C 
A B C D 
A B C D E

````

## 135.Find all prime numbers between two numbers using nested loops. 

````java[]
import java.util.*;
import java.lang.*;
public class prg15{
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
        System.out.println("Prime number between: "+ start +" to "+end);
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
20
Prime number between: 10 to 20
11 13 17 19

````

## 136.Create a 2D array and initialize it with user input using nested loops.

````java[]

import java.util.*;
public class prg16
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of rows ");
        int row = sc.nextInt();
        System.out.println("Enter the number of columns ");
        int col = sc.nextInt();

        int a[][] = new int[row][col];
        System.out.println("Enter the matrix elements");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                a[i][j]=sc.nextInt();
            }
        }
        System.out.println("Values of the matrix");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                System.out.print(a[i][j]+" ");
            }
            System.out.println();
        }

        }
    }

OUTPUT:

Enter the number of rows 
2
Enter the number of columns 
2
Enter the matrix elements
2
4
6
9
Values of the matrix
2 4 
6 9

````

## 137.Find the diagonal elements of a matrix using nested loops. 

````java[]

import java.util.*;
public class prg17
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of rows ");
        int row = sc.nextInt();
        System.out.println("Enter the number of columns ");
        int col = sc.nextInt();

        int a[][] = new int[row][col];
        System.out.println("Enter the matrix elements");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                a[i][j]=sc.nextInt();
            }
        }
        System.out.println("Diagonal Values of the matrix");
        for(int i=0;i<row;i++) {

            System.out.print(a[i][i] + " ");

            System.out.println();
        }
    }

}

OUTPUT:

Enter the number of rows 
2
Enter the number of columns 
2
Enter the matrix elements
2
6
4
8
Diagonal Values of the matrix
2 
8

````

## 138.Create a number grid using nested loops. 

````java[]
import java.util.*;
public class prg18
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
        System.out.println("NUMBER GRID");
        for(int i=1;i<=row;i++){
            for(int j=1;j<=col;j++){
                System.out.print((i*j)+"\t");
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
NUMBER GRID
1	2	
2	4

````

## 139.Create a star pattern like a Christmas tree using nested loops. 

````java[]

import java.util.*;

public class prg19 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();


        for (int i = 1; i <= n; i++) {
            for (int k = 1; k <= n - i; k++) {
                System.out.print("  ");
            }
            for (int j = 1; j <= (2 * i) - 1; j++) {
                System.out.print(" *");
            }
            System.out.println();
        }

        int Height = n / 3;
        for (int i = 0; i < Height; i++) {
            for (int j = 1; j <= (2 * n - 3); j++) {
                System.out.print(" ");
            }
            System.out.println("***");
        }

        sc.close();
    }
}

OUTPUT:

7
             *
           * * *
         * * * * *
       * * * * * * *
     * * * * * * * * *
   * * * * * * * * * * *
 * * * * * * * * * * * * *
           ***
           ***

````
## 140.Perform matrix addition using nested loops. 

````java[]
import java.util.*;
public class prg20
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the number of rows");
        int row=s.nextInt();
        System.out.println("Enter the number of column");
        int col=s.nextInt();
        int[][] a=new int[row][col];
        int[][] b=new int[row][col];
        int[][] sum=new int[row][col];
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
                sum[i][j]=a[i][j]+b[i][j];
            }
        }


        System.out.println("sum of the matrix");
        for(int i=0;i<row;i++){
            for(int j=0;j<col;j++){
                System.out.print(sum[i][j]+" ");
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
2
4
6
8
Enter the  second matrix element
3
6
9
5
sum of the matrix
5 10 
15 13

````


