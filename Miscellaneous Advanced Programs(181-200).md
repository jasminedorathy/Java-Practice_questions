
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

import java.util.*;

class ChatApplication {
    public void startChat() {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Simple Command-Line Chat Application");
        System.out.println("Type 'exit' to end the chat.");

        String message;
        do {
            System.out.print("You: ");
            message = scanner.nextLine().trim();

            if (message.isEmpty()) {
                System.out.println("Bot: Please type something!");
                continue;
            }

            if (!message.equalsIgnoreCase("exit")) {
                System.out.println("Bot: " + generateResponse(message));
            } else {
                System.out.print("Are you sure you want to exit? (yes/no): ");
                String confirmation = scanner.nextLine().trim();
                if (confirmation.equalsIgnoreCase("yes")) {
                    break;
                } else {
                    message = "";
                }
            }
        } while (true);

        System.out.println("Chat ended. Goodbye!");
        scanner.close();
    }

    private String generateResponse(String input) {
        input = input.toLowerCase();

        if (input.contains("hello") || input.contains("hi")) {
            return "Hello! How can I assist you today?";
        } else if (input.contains("how are you")) {
            return "I'm just a bot, but I'm here to help! How about you?";
        } else if (input.contains("thank you") || input.contains("thanks")) {
            return "You're welcome! Is there anything else I can help with?";
        } else if (input.contains("bye")) {
            return "Goodbye! Have a great day!";
        } else if (input.contains("name")) {
            return "I'm just a simple chat bot. I don't have a name, but you can call me Bot!";
        } else if (input.contains("weather")) {
            return "I'm not connected to the internet, but I hope the weather is nice where you are!";
        } else if (input.contains("joke")) {
            return "Why don't scientists trust atoms? Because they make up everything!";
        } else {
            return "That's interesting! Can you tell me more?";
        }
    }
}

public class prgeg2 {
    public static void main(String[] args) {
        ChatApplication chatApp = new ChatApplication();
        chatApp.startChat();
    }
}

OUTPUT:
Simple Command-Line Chat Application
Type 'exit' to end the chat.
You: hello
Bot: Hello! How can I assist you today?
You: how are you
Bot: I'm just a bot, but I'm here to help! How about you?
You: bye
Bot: Goodbye! Have a great day!
You: 
Bot: Please type something!
You:  
Bot: Please type something!
You: exit
Are you sure you want to exit? (yes/no): yes
Chat ended. Goodbye!



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
import java.util.*;
public class prgeg3 {

    public static String compress(String input) {
        if (input == null || input.isEmpty()) {
            return input;
        }

        StringBuilder comp = new StringBuilder();
        int count = 1;

        for (int i = 0; i < input.length(); i++) {
            if (i + 1 < input.length() && input.charAt(i) == input.charAt(i + 1)) {
                count++;
            } else {
                comp.append(input.charAt(i));
                if (count > 1) {
                    comp.append(count);
                }
                count = 1;
            }
        }

        return comp.length() < input.length() ? comp.toString() : input;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a string to compress: ");
        String input = sc.nextLine();
        String compressed = compress(input);

        System.out.println("Original: " + input);
        System.out.println("Compressed: " + compressed);

        sc.close();
    }
}

OUTPUT:
Enter a string to compress: aaabbbccdd
Original: aaabbbccdd
Compressed: a3b3c2d2


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

import java.util.*;
import java.io.*;
public class prgeg7 {

    public static void main(String[] args) {

        String filename="eg.txt";
        String con="heyy all welcome to the java boot camp";

        try(BufferedWriter writer=new BufferedWriter(new FileWriter(filename))){
            writer.write(con);
            System.out.println("File written Successfully");
        }
        catch (IOException e) {
            System.out.println("An error occurred while writing the file.");
            e.printStackTrace();
        }
        try (BufferedReader reader = new BufferedReader(new FileReader(filename))) {
            String line;
            System.out.println("Reading from file:");
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            System.out.println("An error occurred while reading the file.");
            e.printStackTrace();
        }

    }

}


OUTPUT:

File written Successfully
Reading from file:
heyy all welcome to the java boot camp




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

import java.util.*;
public class prgeg4{

    private static final String[] units = {"", "One", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine"};
    private static final String[] teens = {"Ten", "Eleven", "Twelve", "Thirteen", "Fourteen", "Fifteen", "Sixteen", "Seventeen", "Eighteen", "Nineteen"};
    private static final String[] tens = {"", "Ten", "Twenty", "Thirty", "Forty", "Fifty", "Sixty", "Seventy", "Eighty", "Ninety"};

    public static String convertToWords(int number) {
        if (number == 0) {
            return "Zero";
        }
        return convert(number).trim();
    }

    private static String convert(int number) {
        if (number < 10) {
            return units[number];
        } else if (number < 20) {
            return teens[number - 10];
        } else if (number < 100) {
            return tens[number / 10] + " " + convert(number % 10);
        } else if (number < 1000) {
            return units[number / 100] + " Hundred " + convert(number % 100);
        } else if (number < 1_000_000) {
            return convert(number / 1000) + " Thousand " + convert(number % 1000);
        } else if (number < 1_000_000_000) {
            return convert(number / 1_000_000) + " Million " + convert(number % 1_000_000);
        } else {
            return "Number out of range";
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int number = sc.nextInt();
        String words = convertToWords(number);
        System.out.println("In words: " + words);
        sc.close();
    }
}

OUTPUT:
Enter a number: 1522
In words: One Thousand Five Hundred Twenty Two


````
## 193 .Build a simple bank account system with balance checking. 
````java[]

import java.util.*;

public class BankAccount {
    private String accountNumber;
    private String accountHolderName;
    private double balance;

    public BankAccount(String accountNumber, String accountHolderName, double initialBalance) {
        this.accountNumber = accountNumber;
        this.accountHolderName = accountHolderName;
        this.balance = initialBalance;
    }

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposited: " + amount);
        } else {
            System.out.println("Invalid deposit amount.");
        }
    }

    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("Withdrawn: " + amount);
        } else {
            System.out.println("Invalid withdrawal amount or insufficient balance.");
        }
    }

    public double getBalance() {
        return balance;
    }

    public void displayAccountDetails() {
        System.out.println("Account Number: " + accountNumber);
        System.out.println("Account Holder: " + accountHolderName);
        System.out.println("Balance: " + balance);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter account number: ");
        String accountNumber = sc.nextLine();

        System.out.print("Enter account holder name: ");
        String accountHolderName = sc.nextLine();

        System.out.print("Enter initial balance: ");
        double initialBalance = sc.nextDouble();

        BankAccount account = new BankAccount(accountNumber, accountHolderName, initialBalance);

        while (true) {
            System.out.println("\nChoose an option:");
            System.out.println("1. Deposit");
            System.out.println("2. Withdraw");
            System.out.println("3. Check Balance");
            System.out.println("4. Display Account Details");
            System.out.println("5. Exit");
            System.out.print("Enter your choice: ");
            int choice = sc.nextInt();

            switch (choice) {
                case 1:
                    System.out.print("Enter deposit amount: ");
                    double depositAmount = sc.nextDouble();
                    account.deposit(depositAmount);
                    break;
                case 2:
                    System.out.print("Enter withdrawal amount: ");
                    double withdrawAmount = sc.nextDouble();
                    account.withdraw(withdrawAmount);
                    break;
                case 3:
                    System.out.println("Current Balance: " + account.getBalance());
                    break;
                case 4:
                    account.displayAccountDetails();
                    break;
                case 5:
                    System.out.println("Exiting...");
                    sc.close();
                    return;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }
    }
}


OUTPUT:

Enter account number: 12354689
Enter account holder name: jasmine
Enter initial balance: 500

Choose an option:
1. Deposit
2. Withdraw
3. Check Balance
4. Display Account Details
5. Exit
Enter your choice: 1
Enter deposit amount: 200
Deposited: 200.0

Choose an option:
1. Deposit
2. Withdraw
3. Check Balance
4. Display Account Details
5. Exit
Enter your choice: 3
Current Balance: 700.0

Choose an option:
1. Deposit
2. Withdraw
3. Check Balance
4. Display Account Details
5. Exit
Enter your choice: 5
Exiting


````
## 194.Create a dynamic menu-driven program using loops. 
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
## 195.Implement a Tic-Tac-Toe game with a simple AI. 
````java[]
import java.util.Scanner;

public class prg3{
    private static char[][] board = {{' ', ' ', ' '}, {' ', ' ', ' '}, {' ', ' ', ' '}};
    private static char currentPlayer = 'X';

    public static void main(String[] args) {
        Scanner sc= new Scanner(System.in);
        boolean won = false;
        int moves = 0;

        while (!won && moves < 9) {
            printBoard();
            System.out.println("Player " + currentPlayer + ", enter your move (row and column: 0 1 2): ");
            int row = sc.nextInt();
            int col = sc.nextInt();

            if (row >= 0 && row < 3 && col >= 0 && col < 3 && board[row][col] == ' ') {
                board[row][col] = currentPlayer;
                moves++;
                won = checkWin();
                if (!won) {
                    currentPlayer = (currentPlayer == 'X') ? 'O' : 'X';
                }
            } else {
                System.out.println("Invalid move, try again.");
            }
        }

        printBoard();
        if (won) {
            System.out.println("Player " + currentPlayer + " wins!");
        } else {
            System.out.println("It's a draw!");
        }

    }

    private static void printBoard() {
        System.out.println("\n  0 1 2");
        for (int i = 0; i < 3; i++) {
            System.out.print(i + " ");
            for (int j = 0; j < 3; j++) {
                System.out.print(board[i][j] + " ");
            }
            System.out.println();
        }
    }

    private static boolean checkWin() {
        for (int i = 0; i < 3; i++) {
            if (board[i][0] == currentPlayer && board[i][1] == currentPlayer && board[i][2] == currentPlayer) return true;
            if (board[0][i] == currentPlayer && board[1][i] == currentPlayer && board[2][i] == currentPlayer) return true;
        }
        if (board[0][0] == currentPlayer && board[1][1] == currentPlayer && board[2][2] == currentPlayer) return true;
        if (board[0][2] == currentPlayer && board[1][1] == currentPlayer && board[2][0] == currentPlayer) return true;
        return false;
    }
}


OUTPUT:

  0 1 2
0       
1       
2       
Player X, enter your move (row and column: 0 1 2): 
0
1

  0 1 2
0   X   
1       
2       
Player O, enter your move (row and column: 0 1 2): 
0
2

  0 1 2
0   X O 
1       
2       
Player X, enter your move (row and column: 0 1 2): 
0
3
Invalid move, try again.

  0 1 2
0   X O 
1       
2       
Player X, enter your move (row and column: 0 1 2): 
1
1

  0 1 2
0   X O 
1   X   
2       
Player O, enter your move (row and column: 0 1 2): 
0
0

  0 1 2
0 O X O 
1   X   
2       
Player X, enter your move (row and column: 0 1 2): 
1
2

  0 1 2
0 O X O 
1   X X 
2       
Player O, enter your move (row and column: 0 1 2): 
0
1
Invalid move, try again.

  0 1 2
0 O X O 
1   X X 
2       
Player O, enter your move (row and column: 0 1 2): 
1
0

  0 1 2
0 O X O 
1 O X X 
2       
Player X, enter your move (row and column: 0 1 2): 
0
2
Invalid move, try again.

  0 1 2
0 O X O 
1 O X X 
2       
Player X, enter your move (row and column: 0 1 2): 
2
0

  0 1 2
0 O X O 
1 O X X 
2 X     
Player O, enter your move (row and column: 0 1 2): 
2
1

  0 1 2
0 O X O 
1 O X X 
2 X O   
Player X, enter your move (row and column: 0 1 2): 
3
1
Invalid move, try again.

  0 1 2
0 O X O 
1 O X X 
2 X O   
Player X, enter your move (row and column: 0 1 2): 
3
3
Invalid move, try again.

  0 1 2
0 O X O 
1 O X X 
2 X O   
Player X, enter your move (row and column: 0 1 2): 
2
2

  0 1 2
0 O X O 
1 O X X 
2 X O X 
It's a draw!


````
## 196. Build a currency converter program. 
````java[]

import java.util.*;

public class prgeg8 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Currency Converter");

        System.out.print("Enter the exchange rate : ");
        double exchangeRate = scanner.nextDouble();


        System.out.print("Enter the amount in USD: ");
        double amount = scanner.nextDouble();


        double convertedAmount = amount * exchangeRate;


        System.out.println(amount + " USD = " + convertedAmount + " Target Currency");

    }
}

OUTPUT:

Currency Converter
Enter the exchange rate : 100
Enter the amount in USD: 50
50.0 USD = 5000.0 Target Currency


````
## 197.Create a program to count the frequency of words in a sentence. 
````java[]

import java.util.*;

public class prgeg10 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a sentence: ");
        String sentence = sc.nextLine();

        String[] words = sentence.split(" ");
        String[] uniqueWords = new String[words.length];
        int[] frequency = new int[words.length];
        int unique= 0;

        for (int i = 0; i < words.length; i++) {
            boolean found = false;
            for (int j = 0; j < unique; j++) {
                if (uniqueWords[j].equals(words[i])) {
                    frequency[j]++;
                    found = true;
                    break;
                }
            }
            if (!found) {
                uniqueWords[unique] = words[i];
                frequency[unique] = 1;
                unique++;
            }
        }

        System.out.println("Word frequencies:");
        for (int i = 0; i < unique; i++) {
            System.out.println(uniqueWords[i] + ": " + frequency[i]);
        }


    }
}
OUTPUT:
Enter a sentence: hello how are you? Are you having fun learning java?
Word frequencies:
hello: 1
how: 1
are: 1
you?: 1
Are: 1
you: 1
having: 1
fun: 1
learning: 1
java?: 1


````
## 198.Write a program to find the longest word in a string. 
````java[]

import java.util.*;

public class prgeg9 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String input = scanner.nextLine();

        String longestWord = findLongestWord(input);
        System.out.println("Longest word: " + longestWord);

        scanner.close();
    }

    public static String findLongestWord(String input) {
        String[] words = input.split(" ");
        String longestWord = "";

        for (String word : words) {
            if (word.length() > longestWord.length()) {
                longestWord = word;
            }
        }

        return longestWord;
    }
}

OUTPUT:
Enter a string: Hello All today we will be learning about linkedlist in java
Longest word: linkedlist


````
## 199.Create a simple ATM simulation with deposit/withdraw functions. 
````java[]

import java.util.*;

public class prg20 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double balance = 1000.0;
        int choice;

        do {
            
            System.out.println("\nWelcome to Simple ATM");
            System.out.println("1. Check Balance");
            System.out.println("2. Deposit Money");
            System.out.println("3. Withdraw Money");
            System.out.println("4. Exit");
            System.out.print("Enter your choice: ");
            choice = sc.nextInt();

            switch (choice) {
                case 1:

                    System.out.println("Your current balance is: $" + balance);
                    break;

                case 2:

                    System.out.print("Enter the amount to deposit: $");
                    double depositAmount = sc.nextDouble();
                    if (depositAmount > 0) {
                        balance += depositAmount;
                        System.out.println("$" + depositAmount + " deposited successfully.");
                    } else {
                        System.out.println("Invalid amount. Please enter a positive value.");
                    }
                    break;

                case 3:

                    System.out.print("Enter the amount to withdraw: $");
                    double withdrawAmount = sc.nextDouble();
                    if (withdrawAmount > 0 && withdrawAmount <= balance) {
                        balance -= withdrawAmount;
                        System.out.println("$" + withdrawAmount + " withdrawn successfully.");
                    } else if (withdrawAmount > balance) {
                        System.out.println("Insufficient balance.");
                    } else {
                        System.out.println("Invalid amount. Please enter a positive value.");
                    }
                    break;

                case 4:

                    System.out.println("Thank you for using Simple ATM. Goodbye!");
                    break;

                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        } while (choice != 4);

        sc.close();
    }
}

OUTPUT:

Welcome to Simple ATM
1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Enter your choice: 2
Enter the amount to deposit: $100
$100.0 deposited successfully.

Welcome to Simple ATM
1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Enter your choice: 1
Your current balance is: $1100.0

Welcome to Simple ATM
1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Enter your choice: 3
Enter the amount to withdraw: $500
$500.0 withdrawn successfully.

Welcome to Simple ATM
1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Enter your choice: 1
Your current balance is: $600.0

Welcome to Simple ATM
1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Enter your choice: 4
Thank you for using Simple ATM. Goodbye!

````
## 200.Write a program to manage student records.
````java[]

package Nanthu;
import java.util.*;

class Student {
    String name;
    int roll_no;
    String dept;
    int mark;

    public Student(String name, int roll_no, String dept, int mark) {
        this.name = name;
        this.roll_no = roll_no;
        this.dept = dept;
        this.mark = mark;
    }

    public void display() {
        System.out.println("Name: " + name);
        System.out.println("Roll Number: " + roll_no);
        System.out.println("Department: " + dept);
        System.out.println("Mark: " + mark);
    }
}

public class Main16 {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        ArrayList<Student> a = new ArrayList<>();

        while (true) {
            System.out.println("\nStudent Detail");
            System.out.println("1. Add Student");
            System.out.println("2. Display Student Details");
            System.out.println("3. Exit");
            System.out.print("Enter your choice: ");
            int choice = s.nextInt();

            switch (choice) {
                case 1:
                    System.out.print("Enter your name: ");
                    s.nextLine(); // Consume newline
                    String name = s.nextLine();
                    System.out.print("Enter your roll number: ");
                    int roll_no = s.nextInt();
                    System.out.print("Enter your Department: ");
                    s.nextLine(); // Consume newline
                    String dept = s.nextLine();
                    System.out.print("Enter your Mark: ");
                    int mark = s.nextInt();
                    a.add(new Student(name, roll_no, dept, mark));
                    System.out.println("Successfully Added");
                    break;

                case 2:
                    System.out.println("\nStudent Records:");
                    for (Student student : a) {
                        student.display();
                        System.out.println(); // Add a blank line between records
                    }
                    break;

                case 3:
                    System.out.println("Exiting... Goodbye!");
                    s.close();
                    return;

                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }
    }
}

OUTPUT:

Student Detail
1. Add Student
2. Display Student Details
3. Exit
Enter your choice: 1
Enter your name: jass
Enter your roll number: 101
Enter your Department: AI&DS
Enter your Mark: 470
Successfully Added

Student Detail
1. Add Student
2. Display Student Details
3. Exit
Enter your choice: 2

Student Records:
Name: jass
Roll Number: 101
Department: AI&DS
Mark: 470


Student Detail
1. Add Student
2. Display Student Details
3. Exit
Enter your choice: 3
Exiting... Goodbye!






````
