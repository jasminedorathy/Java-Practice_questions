
## Miscellaneous Advanced Programs 

## 181.Create a calculator that supports multiple operations (addition, subtraction, etc.). 

````java[]
mport java.util.*;
public class prg40
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
                System.out.println("  Your Using Calculator  ");

                System.out.println("1. Addition");
                System.out.println("2. Subtraction");
                System.out.println("3. Multiplication");
                System.out.println("4. Division");
                System.out.println("5. Modulus");


                System.out.println("Enter your choice");
                int choice=sc.nextInt();
                System.out.println("Enter the first num: ");
                int a = sc.nextInt();
                System.out.println("Enter the second num: ");
                int b = sc.nextInt();

        switch(choice) {
            case 1:
                System.out.println("You selected addition operation: " + (a+b));
                break;
            case 2:
                System.out.println("You selected subtraction operation: " + (a-b));
                break;
            case 3:
                System.out.println("You selected multiplication operation: " + (a*b));
                break;
            case 4:
                System.out.println("You selected division operation: " + (a/b));
                break;

            case 5:
                System.out.println("You selected modulus operation: " + (a%b));
                break;

            default:
                System.out.println("Invalid input! Please select valid choice");
        }
}


OUTPUT:

Your Using Calculator  
1. Addition
2. Subtraction
3. Multiplication
4. Division
5. Modulus
Enter your choice
 2
Enter the first num: 
45
Enter the second num: 
30
You selected subtraction operation: 15

````

## 182.Implement a Fibonacci series generator using memoization. 

````java[]

import java.util.*;
public class prg41
{
    public static int fib(int n){
        if(n<=1){
            return n;
        }
        return fib(n-1)+fib(n-2);
    }
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number");
        int n=sc.nextInt();
        System.out.println("Fibnacci of the numbers are");
        for(int i=0;i<n;i++){
            System.out.print(fib(i)+" ");
        }
    }
}

OUTPUT:
Enter the number
10
Fibnacci of the numbers are
0 1 1 2 3 5 8 13 21 34

````

## 183.Create a random password generator. 

````java[]


package sample;

import java.util.Random;

public class prg42 {
    public static String generatePassword(int length) {
        String characters = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*";
        Random random = new Random();
        StringBuilder password = new StringBuilder();

        for (int i = 0; i < length; i++) {
            int index = random.nextInt(characters.length());
            password.append(characters.charAt(index));
        }

        return password.toString();
    }

    public static void main(String[] args) {
        int length = 8;
        String password = generatePassword(length);
        System.out.println("Generated Password: " + password);
    }
}

OUTPUT:

Generated Password: HiieAd*!

````

## 184.Create a simple command-line chat application. 
````java[]











````
## 185.Implement a quiz program that uses arrays. 
````java[]

import java.util.Scanner;

public class prg43{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String[] questions = {
                "What is the default value of a boolean variable in Java?",
                "Which keyword is used to define a constant in Java?",
                "Which method is called when an object is garbage collected?",
                "Which of the following is not a primitive data type in Java?",
                "Which of the following loops is guaranteed to execute at least once?"
        };

        String[][] options = {
                {"A. true", "B.null", "C.false", "D.0"},
                {"A. constant", "B. static", "C. final", "D.const"},
                {"A. delete()", "B. finalize()", "C. destroy()", "D. clean()"},
                {"A. int", "B. char", "C. String", "D. double"},
                {"A. for loop", "B. while loop", "C. do-while loop", "D. None of the above"}
        };

        char[] answers = {'B', 'B', 'B', 'C', 'C'};
        int score = 0;

        for (int i = 0; i < questions.length; i++) {
            System.out.println((i + 1) + ". " + questions[i]);
            for (String option : options[i]) {
                System.out.println(option);
            }
            System.out.print("Your answer: ");
            char userAnswer = Character.toUpperCase(scanner.next().charAt(0));

            if (userAnswer == answers[i]) {
                System.out.println("Correct!\n");
                score++;
            } else {
                System.out.println("Wrong! The correct answer is " + answers[i] + "\n");
            }
        }

        System.out.println("Quiz Over! Your final score is: " + score + "/" + questions.length);
        sc.close();
    }
}
OUTPUT:
1. What is the default value of a boolean variable in Java?
A. true
B.null
C.false
D.0
Your answer: A
Wrong! The correct answer is B

2. Which keyword is used to define a constant in Java?
A. constant
B. static
C. final
D.const
Your answer: B
Correct!

3. Which method is called when an object is garbage collected?
A. delete()
B. finalize()
C. destroy()
D. clean()
Your answer: B
Correct!

4. Which of the following is not a primitive data type in Java?
A. int
B. char
C. String
D. double
Your answer: 
C
Correct!

5. Which of the following loops is guaranteed to execute at least once?
A. for loop
B. while loop
C. do-while loop
D. None of the above
Your answer: C
Correct!

Quiz Over! Your final score is: 4/5


````
## 186.Create a program to count words in a sentence. 
````java[]


import java.util.*;
public class prg44 {

    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.println("Enter the sentence ");
        String str=sc.nextLine();


        if(str.length()==0) {
            System.out.println("Count of the words= 0");

        }
        int count=1;
        for(int i=0;i<str.length()-1;i++) {
            if(str.charAt(i)==' ' && str.charAt(i+1)!=' ') {
                count++;
            }
        }
        System.out.println("Count of the words in the sentence= "+count);

    }

}

OUTPUT:

Enter the sentence 
Hello all I feel so blessed and honoured to be part of this program
 Count of the words in the sentence= 14

````
## 187.Implement string compression (e.g., "aaabbb" -> "a3b3"). 
````java[]











````
## 188.Create a program to generate the first N prime numbers. 
````java[]
import java.util.*;
public class prg45{
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
        int num=s.nextInt();
        int n=2;
        while(n<=num){
            if(isprime(n)){
                System.out.print(n+" ");
            }
            n++;
        }
    }
}

OUTPUT:
Enter the value
Enter the value
25
2 3 5 7 11 13 17 19 23 

````
## 189.Create an interactive program to show user details. 
````java[]

import java.util.*;
public class prg46 {

    public static void main(String[] args) {
        // TODO Auto-generated method stub
        Scanner sc=new Scanner(System.in);

        System.out.println("Enter your name");
        String name=sc.nextLine();
        System.out.println("Enter your age");
        int age=sc.nextInt();
        System.out.println("Enter your phone number");
        long number=sc.nextLong();
        System.out.println("Enter Your Date of Birth: ");
        int DOB = sc.nextInt();
        System.out.println("Enter your gender");
        String gender=sc.nextLine();
        sc.nextLine();
        System.out.println("Enter you city");
        String city=sc.nextLine();
        System.out.println("Enter you state");
        String state=sc.nextLine();

        System.out.println("Enter you email");
        String email=sc.nextLine();

        System.out.println(" ****USER DETAIL**** ");
        System.out.println("Name: "+ name);
        System.out.println("Age: "+ age);


        System.out.println("Phone Number: "+ number);
        System.out.println("Date Of Birth: "+ DOB);
        System.out.println("Gender: "+ gender);
        System.out.println("City: "+ city);
        System.out.println("State: "+ state);
        System.out.println("Email: "+ email);
}

## OUTPUT:

````ja]va
Enter your name
jasmine
Enter your age
20
Enter your phone number
93423432889
Enter Your Date of Birth: 
15072005
Enter your gender
Female
Enter you city
Oooty
Enter you state
Tamil nadu
Enter you email
hdfshfgv@gmail.com
 ****USER DETAIL**** 
Name: jasmine
Age: 20
Phone Number: 93423432889
Date Of Birth: 15072005
Gender: 
City: Oooty
State: Tamil nadu
Email: hdfshfgv@gmail.com




````
## 190 .Build a basic database system with file operations. 
````java[]



















````
## 191.Implement a voting system using classes and loops. 
````java[]
import java.util.*;
class Vote{
    String[] candidate= {"Candidate A","Candidate B","Candidate C"};
    int[] voting=new int[candidate.length];
    public void votingCandidate(int choice) {
        if(choice>=1 && choice<=candidate.length) {
            voting[choice-1]++;
            System.out.println("Successfully Voted by "+candidate[choice-1]);
        }
        else {
            System.out.println("Not voted");
        }
    }
    public void display() {
        for(int i=0;i<candidate.length;i++) {
            System.out.println(candidate[i]+": "+ voting[i]+" voted");
        }
    }
}
public class prg47 {

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
         Vote v=new Vote();
        int choice;
        do {
            System.out.println("  WELCOME TO THE VOTING SYSTEM  ");
            System.out.println(" 1.Candidate 1");
            System.out.println(" 2.Candidate 2");
            System.out.println(" 3.Candidate 3");
            System.out.println(" 4.Display");
            System.out.println(" 5.Exit");

            System.out.println("Enter your choice");
            choice=s.nextInt();

            if (choice >= 1 && choice <= 3) {
                v.votingCandidate(choice);
            } else if (choice == 4) {
                v.display();
            } else if (choice != 5) {
                System.out.println("Invalid option. Please try again.");
            }
        } while (choice != 5);
        System.out.println("Thank you for voting.");

    }

}

OUTPUT:
 WELCOME TO THE VOTING SYSTEM  
 1.Candidate 1
 2.Candidate 2
 3.Candidate 3
 4.Display
 5.Exit
Enter your choice
2
Successfully Voted by Candidate B
  WELCOME TO THE VOTING SYSTEM  
 1.Candidate 1
 2.Candidate 2
 3.Candidate 3
 4.Display
 5.Exit
Enter your choice
5
Thank you for voting.

````
## 192.Create a program to convert numbers to words. 
````java[]













````
## 193 .Build a simple bank account system with balance checking. 
````java[]












````
## 194.Create a dynamic menu-driven program using loops. 
````java[]







````
## 195.Implement a Tic-Tac-Toe game with a simple AI. 
````java[]








````
## 196. Build a currency converter program. 
````java[]









````
## 197.Create a program to count the frequency of words in a sentence. 
````java[]















````
## 198.Write a program to find the longest word in a string. 
````java[]










````
## 199.Create a simple ATM simulation with deposit/withdraw functions. 
````java[]



















````
## 200.Write a program to manage student records.
````java[]


















````
