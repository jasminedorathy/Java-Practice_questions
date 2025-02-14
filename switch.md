## 41-60: Switch Case Statements .

## 41. Implement a simple calculator using switch case. 
````java[]

import java.util.*;
public class prg1
{
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter the values");
        int a=sc.nextInt();
        int b=sc.nextInt();
        System.out.println("Enter the symbol");
        char c=sc.next().charAt(0);
        switch(c){
            case '+':
                System.out.println("Addition: "+ (a+b));
                break;
            case '-':
                System.out.println("Subtraction:"+ (a-b));
                break;

            case '*':
                System.out.println("Multiplication: "+(a*b));
                break;
            case '/':
                System.out.println("Division: "+(a/b));
                break;
            case '%':
                System.out.println("Modulus: "+(a%b));
                break;
            default:
                System.out.println("Invalid Symbol");
        }
    }
}

OUTPUT:
Enter the values
15
22
Enter the symbol
+
Addition: 37

````
## 42. Convert a number to its word equivalent (1 to 10) using switch. 
````java[]

import java.util.*;
public class prg2
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the values between 1 to 10");
        int n=s.nextInt();

        switch(n){
            case 1:
                System.out.println("One");
                break;
            case 2:
                System.out.println("Two");
                break;
            case 3:
                System.out.println("Three");
                break;
            case 4:
                System.out.println("Four");
                break;
            case 5:
                System.out.println("Five");
                break;
            case 6:
                System.out.println("Six");
                break;
            case 7:
                System.out.println("Seven");
                break;
            case 8:
                System.out.println("Eight");
                break;
            case 9:
                System.out.println("Nine");
                break;
            case 10:
                System.out.println("Ten");
                break;

            default:
                System.out.println("Invalid Option.Enter the Correct option");
        }
    }
}

OUTPUT:
Enter the values between 1 to 10
2
Two

````
## 43. Find the day of the week using switch statement. 
````java[]
import java.util.*;
public class prg3
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the day in a week(Sunday - Saturday)");
        int n=s.nextInt();

        switch(n){
            case 1:
                System.out.println("Sunday");
                break;
            case 2:
                System.out.println("Monday");
                break;
            case 3:
                System.out.println("Tuesday");
                break;
            case 4:
                System.out.println("Wednesday");
                break;
            case 5:
                System.out.println("Thursday");
                break;
            case 6:
                System.out.println("Friday");
                break;
            case 7:
                System.out.println("Saturday");
                break;

            default:
                System.out.println("Invalid Option.Enter the Correct option");
        }
    }
}

OUTPUT:
Enter the day present in a week: 
5
Thursday

````
## 44. Convert a number to its Roman numeral equivalent using switch. 
````java[]


import java.util.*;
public class prg4
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the values between 1 to 10");
        int n=s.nextInt();

        switch(n){
            case 1:
                System.out.println("I");
                break;
            case 2:
                System.out.println("II");
                break;
            case 3:
                System.out.println("III");
                break;
            case 4:
                System.out.println("IV");
                break;
            case 5:
                System.out.println("V");
                break;
            case 6:
                System.out.println("VI");
                break;
            case 7:
                System.out.println("VII");
                break;
            case 8:
                System.out.println("VIII");
                break;
            case 9:
                System.out.println("IX");
                break;
            case 10:
                System.out.println("X");
                break;

            default:
                System.out.println("Invalid Option.Enter the Correct option");
        }
    }
}

OUTPUT:

Enter the values between 1 to 10
5
V

````

## 45.Implement a basic menu-driven program using switch-case. 
````java[]

import java.util.*;
public class prg5 {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("*****The Dishes available in our cafe*****");
        System.out.println("1.Pasta");
        System.out.println("2.Pizza");
        System.out.println("3.Burger");
        System.out.println("4.Icecreams");
        System.out.println("5.Cappuccino");
        System.out.println("6.Muffins");

        System.out.println("Enter you choice:");
        int choice=sc.nextInt();
        switch(choice) {
            case 1:
                System.out.println("Pasta is ready");
                break;
            case 2:
                System.out.println("Pizza is ready");
                break;
            case 3:
                System.out.println("Burger is ready");
                break;

                case 4:
                System.out.println("Icecreams is ready");
                break;

            case 5:
                System.out.println("Cappuccino is ready");
                break;
            case 6:
                System.out.println("Muffins is ready");
                break;
            default:
                System.out.println("Invalid choice");

        }
    }
}

OUtPUT:

*****The Dishes available in our cafe*****
1.Pasta
2.Pizza
3.Burger
4.Icecreams
5.Cappuccino
6.Muffins
Enter you choice
5
Cappuccino is ready



````
## 46. Print all numbers from 1 to n in reverse using switch. 
````java[]

import java.util.*;
public class prg6 {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter the value of n");
        int n=sc.nextInt();
        switch(1) {
            case 1:
                while(n>0) {
                    System.out.print(n+" ");
                    n--;
                }
                break;
            default:
                System.out.println("Invalid Input.Provide the correct input");
        }
    }

}

OUTPUT:
Enter the value of n
15
15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 
````
## 47. Grade student marks using a switch-case statement. 
````java[]

import java.util.*;
public class prg7
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the your mark");
        int mark=s.nextInt();
        int n=mark/10;

        switch(n){
            case 10:
            case 9:
                System.out.println("You scored Grade A");
                break;
            case 8:
                System.out.println("You Scored Grade B");
                break;
            case 7:
                System.out.println("You Scored Grade C");
                break;
            case 6:
                System.out.println("You Scored Grade D");
                break;
            case 5:
                System.out.println("You Scored Grade E");
                break;

            default:
                if(mark>=0 && mark<50) {
                    System.out.println("Fail");

                }
                else {
                    System.out.println("Invalid input");
                }
        }
    }
}

OUTPUT:
Enter the your mark
80
You Scored Grade B

````
## 48. Perform simple arithmetic operations using switch.
````java[]



import java.util.*;
public class prg8
{
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter the values");
        int a=sc.nextInt();
        int b=sc.nextInt();
        System.out.println("Enter the symbol");
        char c=sc.next().charAt(0);
        switch(c){
            case '+':
                System.out.println("Addition: "+ (a+b));
                break;
            case '-':
                System.out.println("Subtraction:"+ (a-b));
                break;

            case '*':
                System.out.println("Multiplication: "+(a*b));
                break;
            case '/':
                System.out.println("Division: "+(a/b));
                break;
            case '%':
                System.out.println("Modulus: "+(a%b));
                break;
            default:
                System.out.println("Invalid Symbol");
        }
    }
}



OUTPUT:


Enter the values
15
22
Enter the symbol
*
Multiplication: 330


````
## 49. Convert temperature from Celsius to Fahrenheit or vice versa using switch. 
````java[]
import java.util.*;
public class prg9 {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("*****Conversion of Celisus to Fahrenheit and vice versa*****");
        System.out.println("1. Convert Celsius to Fahrenheit");
        System.out.println("2. Convert Fahrenheit to Celisus");
        System.out.println("3. Exit");


        System.out.println("Enter you choice:");
        int choice=sc.nextInt();
        switch(choice) {
            case 1:
                System.out.print("Enter temperature in Celsius: ");
                double celsius = sc.nextDouble();
                double fahrenheit = (celsius * 9/5) + 32;
                System.out.println("Temperature in Fahrenheit" + fahrenheit);
                break;
            case 2:
                System.out.print("Enter temperature in fahrenheit: ");
                fahrenheit = sc.nextDouble();
                celsius = (fahrenheit - 32) * 5/9;
                System.out.println("Temperature in celsius" + celsius);
                break;
            case 3:
                System.out.println("Exit");
                break;


            default:
                System.out.println("Invalid choice");

        }
    }
}

OUTPUT:
*****Conversion of Celisus to Fahrenheit and vice versa*****
1. Convert Celsius to Fahrenheit
2. Convert Fahrenheit to Celisus
3. Exit
Enter you choice:
2
Enter temperature in fahrenheit: 224
Temperature in celsius106.66666666666667



````
## 50. Find the number of days in a month using switch-case. 
````java[]

import java.util.*;
public class prg10
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the Month of your choice");
        String month=s.nextLine();

        switch(month){
            case "January":
                System.out.println("Num of Days: 31");
                break;
            case "February":
                System.out.println("Num of Days: 28 or 29");
                break;
            case "March":
                System.out.println("Num of Days: 31");
                break;
            case "April":
                System.out.println("Num of Days: 30");
                break;
            case "May":
                System.out.println("Num of Days: 31");
                break;
            case "June":
                System.out.println("Num of Days: 30");
                break;
            case "July":
                System.out.println("Num of Days: 31");
                break;
            case "August":
                System.out.println("Num of Days: 31");
                break;
            case "September":
                System.out.println("Num of Days: 30");
                break;
            case "October":
                System.out.println("Num of Days: 31");
                break;
            case "November":
                System.out.println("Num of Days: 30");
                break;
            case "December":
                System.out.println("Num of Days: 31");
                break;

            default:
                System.out.println("Invalid Option");
        }
    }
}

OUTPUT:
Enter the Month of your choice
October
Num of Days: 31

````
## 51.Implement a simple banking system with switch-case. 
````java[]













````
## 52.Determine the month name based on its number using switch-case. 
````java[]

import java.util.*;
public class prg12
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the Month(1-12)");
        int month=s.nextInt();

        switch(month){
            case 1:
                System.out.println("January");
                break;
            case  2:
                System.out.println("February");
                break;
            case 3:
                System.out.println("March");
                break;
            case 4:
                System.out.println("April");
                break;
            case 5:
                System.out.println("May");
                break;
            case 6:
                System.out.println("June");
                break;
            case 7:
                System.out.println("July");
                break;
            case 8:
                System.out.println("August");
                break;
            case 9:
                System.out.println("September");
                break;
            case 10:
                System.out.println("October");
                break;
            case 11:
                System.out.println("November");
                break;
            case 12:
                System.out.println("December");
                break;

            default:
                System.out.println("Invalid input");
        }
    }
}

OUTPUT:
Enter the Month(1-12)
8
August

````
## 53.Calculate the area of different shapes using switch-case. 
````java[]

import java.util.*;
public class prg13
{
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("THE SHAPES,ENTER THE OPTION");

        System.out.println("1.Rectangle ");
        System.out.println("2.Square ");
        System.out.println("3.Cube ");
        System.out.println("4.Circle");
        System.out.println("5.Exit");
        int  choice=sc.nextInt();
        switch(choice){
            case 1:
                System.out.println("Enter the length of rectangle");
                int l=sc.nextInt();
                System.out.println("Enter the Breadth of rectangle");
                int b=sc.nextInt();
                System.out.println("Area of the Rectangle is: "+(l*b));
                break;
            case 2:
                System.out.println("Enter the value of a");
                int a=sc.nextInt();
                System.out.println("Area of Square is: "+(a*a));
                break;
            case 3:
                System.out.println("Enter the value of a");
                int c=sc.nextInt();
                System.out.println("Area of Cube is: "+(c*c*c));
                break;
            case 4:
                System.out.println("Enter the value of r");
                int r=sc.nextInt();
                double result=Math.PI*r*r;
                System.out.println("Area of Circle is: "+result);
                break;
            case 5:
                System.out.println("Exit");
                break;

            default:
                System.out.println("Invalid Option");
        }
    }
}

OUTPUT:

THE SHAPES,ENTER THE OPTION
1.Rectangle 
2.Square 
3.Cube 
4.Circle
5.Exit
4
Enter the value of r
22
Area of Circle is: 1520.5308443374597


````
## 54.Implement a basic calculator with multiple operations. 
````java[]

import java.util.*;
public class prg1
{
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter the values");
        int a=sc.nextInt();
        int b=sc.nextInt();
        System.out.println("Enter the symbol");
        char c=sc.next().charAt(0);
        switch(c){
            case '+':
                System.out.println("Addition: "+ (a+b));
                break;
            case '-':
                System.out.println("Subtraction:"+ (a-b));
                break;

            case '*':
                System.out.println("Multiplication: "+(a*b));
                break;
            case '/':
                System.out.println("Division: "+(a/b));
                break;
            case '%':
                System.out.println("Modulus: "+(a%b));
                break;
            default:
                System.out.println("Invalid Symbol");
        }
    }
}

OUTPUT:
Enter the values
22
15
Enter the symbol
/
Division: 1


````
## 55.Determine if a given character is a vowel or consonant using switch-case.
````java[]

import java.util.*;
public class prg15{
    public static void main(String args[]) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the character");
        char ch=s.next().toLowerCase().charAt(0);

        switch(ch) {
            case 'a':
            case 'e':
            case 'i':
            case 'o':
            case 'u':
                System.out.println(ch+" is vowel");
                break;
            default:
                if(Character.isLetter(ch)) {
                    System.out.println(ch+" is consonant");
                }
                else {
                    System.out.println("Invalid input");
                }
        }
    }
}


OUTPUT:

Enter the character
u
u is vowel

````

## 56.Implement a simple menu system for shopping. 
````java[]

import java.util.*;
public class prg5 {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("*****The Dishes available in our cafe*****");
        System.out.println("1.Pasta");
        System.out.println("2.Pizza");
        System.out.println("3.Burger");
        System.out.println("4.Icecreams");
        System.out.println("5.Cappuccino");
        System.out.println("6.Muffins");

        System.out.println("Enter you choice:");
        int choice=sc.nextInt();
        switch(choice) {
            case 1:
                System.out.println("Pasta is ready");
                break;
            case 2:
                System.out.println("Pizza is ready");
                break;
            case 3:
                System.out.println("Burger is ready");
                break;

                case 4:
                System.out.println("Icecreams is ready");
                break;

            case 5:
                System.out.println("Cappuccino is ready");
                break;
            case 6:
                System.out.println("Muffins is ready");
                break;
            default:
                System.out.println("Invalid choice");

        }
    }
}

OUTPUT:

*****The Dishes available in our cafe*****
1.Pasta
2.Pizza
3.Burger
4.Icecreams
5.Cappuccino
6.Muffins
Enter you choice
5
Cappuccino is ready


````
## 57.Convert a time duration in minutes to hours and minutes. 
````java[]


import java.util.*;
public class prg17 {
    public static void main(String args[]) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the minutes");
        int min=s.nextInt();
        int hour=min/60;
        int minutes=min%60;

        switch (hour) {
            default:
                System.out.println(min + " minutes = " + hour + " hours and " + minutes + " minutes.");
        }

    }
}

OUTPUT:
Enter the minutes
152
152 minutes = 2 hours and 32 minutes.

````
## 58.Implement a number to word converter (1-10) using switch.
````java[]

import java.util.*;
public class prg2
{
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the values between 1 to 10");
        int n=s.nextInt();

        switch(n){
            case 1:
                System.out.println("One");
                break;
            case 2:
                System.out.println("Two");
                break;
            case 3:
                System.out.println("Three");
                break;
            case 4:
                System.out.println("Four");
                break;
            case 5:
                System.out.println("Five");
                break;
            case 6:
                System.out.println("Six");
                break;
            case 7:
                System.out.println("Seven");
                break;
            case 8:
                System.out.println("Eight");
                break;
            case 9:
                System.out.println("Nine");
                break;
            case 10:
                System.out.println("Ten");
                break;

            default:
                System.out.println("Invalid Option.Enter the Correct option");
        }
    }
}

OUTPUT:
Enter the values between 1 to 10
2
Two

````
## 59.Implement a traffic light system using switch. 
````java[]

import java.util.*;
public class prg19 {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("*****Traffic Light System*****");
        System.out.println("1.RED");
        System.out.println("2.YELLOW");
        System.out.println("3.GREEN");
        System.out.println("4.EXIT");
        System.out.println("Enter you choice");
        int choice=sc.nextInt();
        switch(choice) {
            case 1:
                System.out.println("RED : STOP");
                break;
            case 2:
                System.out.println("YELLOW: WAIT");
                break;
            case 3:
                System.out.println("GREEN : GO");
                break;

            case 4:
                System.out.println("EXIT");
                break;
            default:
                System.out.println("Invalid choice");

        }
    }
}


OUTPUT:
*****Traffic Light System*****
1.RED
2.YELLOW
3.GREEN
4.EXIT
Enter you choice
2
YELLOW: WAIT


````
## 60. Solve a quadratic equation using switch-case for the discriminant. 
````java[]


import java.util.*;
public class prg20 {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("*****Solving the quadratic equation using thr formula*****");
        System.out.print("Enter coefficient a: ");
        double a = sc.nextDouble();
        System.out.print("Enter coefficient b: ");
        double b = sc.nextDouble();
        System.out.print("Enter coefficient c: ");
        double c = sc.nextDouble();

        double d = b * b - 4 * a * c;

        int discase = (d > 0) ? 1 : (d == 0) ? 2 : 3;
        switch(discase) {
            case 1:
                double root1 = (-b + Math.sqrt(d)) / (2 * a);
                double root2 = (-b - Math.sqrt(d)) / (2 * a);
                System.out.println("Two real and distinct roots: " + root1 + " and " + root2);
                break;
            case 2:
                double root = -b / (2 * a);
                System.out.println("One real and equal root: " + root);
                break;
            case 3:
                System.out.println("It is a complex number and the solutiion is not a real root.");
                break;


            default:
                System.out.println("Invalid choice");

        }
    }
}
OUTPUT:

*****Solving the quadratic equation using thr formula*****
Enter coefficient a: 5
Enter coefficient b: 2
Enter coefficient c: 6
It is a complex number and the solutiion is not a real root.









````
