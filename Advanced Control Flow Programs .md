## 161-180: Advanced Control Flow Programs 


## 161.Create a simple text-based game using if-else and loops. 
````java[]

import java.util.*;

public class prg1{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Welcome to the Adventure Game!");
        System.out.println("You find yourself in a dark forest. Choose your action:");

        boolean gameRunning = true;
        while (gameRunning) {
            System.out.println("\n1. Go left\n2. Go right\n3. Climb a tree\n4. Exit");
            System.out.print("Enter your choice: ");
            int choice = sc.nextInt();

            if (choice == 1) {
                System.out.println("You encounter a wild wolf! You run away safely.");
            } else if (choice == 2) {
                System.out.println("You find a hidden treasure chest! It's full of gold.");
            } else if (choice == 3) {
                System.out.println("You climb a tree and spot a village nearby.");
            } else if (choice == 4) {
                System.out.println("Exiting the game. Thanks for playing!");
                gameRunning = false;
            } else {
                System.out.println("Invalid choice! Try again.");
            }
        }
        sc.close();
    }
}

OUTPUT:

Welcome to the Adventure Game!
You find yourself in a dark forest. Choose your action:

1. Go left
2. Go right
3. Climb a tree
4. Exit
Enter your choice: 2
You find a hidden treasure chest! It's full of gold.

1. Go left
2. Go right
3. Climb a tree
4. Exit
Enter your choice: 4
Exiting the game. Thanks for playing!


````
## 162 .Build a password validation program with loops and conditions. 
````java[]
import java.util.*;

public class prg2 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a password to validate:");
        String password = sc.nextLine();

        if (isValidPassword(password)) {
            System.out.println("Password is valid!");
        } else {
            System.out.println("Password is invalid! It must contain:");
            System.out.println("- At least 8 characters");
            System.out.println("- At least one uppercase letter");
            System.out.println("- At least one lowercase letter");
            System.out.println("- At least one digit");
            System.out.println("- At least one special character (!@#$%^&* etc.)");
        }

        sc.close();
    }

    public static boolean isValidPassword(String password) {
        if (password.length() < 8) return false;
        boolean hasUpper = false, hasLower = false, hasDigit = false, hasSpecial = false;

        for (char ch : password.toCharArray()) {
            if (Character.isUpperCase(ch)) hasUpper = true;
            else if (Character.isLowerCase(ch)) hasLower = true;
            else if (Character.isDigit(ch)) hasDigit = true;
            else if ("!@#$%^&*()-+".indexOf(ch) != -1) hasSpecial = true;
        }

        return hasUpper && hasLower && hasDigit && hasSpecial;
    }
}


OUTPUT:

Enter a password to validate:
Jasmine1522!
Password is valid!

````

## 163.Implement a Tic-Tac-Toe game using loops and conditions. 
````java[]














````
## 164.Implement a simple file I/O program. 
````java[]














````
## 165.Create a phonebook program with search functionality. 
````java[]














````
## 166.Implement a ticket booking system with class and objects. 
````java[]














````
## 167.Create a random number generator for a guessing game. 
````java[]














````
## 168 .Build a simple calendar program using loops. 
````java[]














````
## 169.Create a program that checks for valid email addresses. 
````java[]














````
## 170 .Build a number encryption/decryption program.
````java[]














````
## 171.Create a weather app interface using control statements. 
````java[]














````
## 172.Write a program for bubble sort. 
````java[]














````
## 173.Implement insertion sort using loops.
````java[]














````
## 174.Perform quicksort on an array using recursion. 
````java[]














````
## 175.Implement selection sort with a loop. 
````java[]














````
## 176.Perform a binary search recursively.
````java[]














````
## 177.Create a class to manage a simple bank account. 
````java[]














````
## 178.Write a program for linear search recursively.
````java[]














````
## 179.Implement depth-first search using a stack. 
````java[]














````
## 180.Implement breadth-first search using a queue. 
````java[]














````
