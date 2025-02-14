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

Process finished with exit code 0
````
## 164.Implement a simple file I/O program. 
````java[]

import java.io.*;
import java.util.*;
public class prg4{
    public static void main(String[] args) {
        String fileName = "example.txt";
        String content = "Hello, this is a simple File I/O example in Java.";
        try {
            FileWriter writer = new FileWriter(fileName);
            writer.write(content);
            writer.close();
            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred while writing the file: " + e.getMessage());
        }
        try {
            FileReader reader = new FileReader(fileName);
            int ch;
            System.out.println("File content:");
            while ((ch = reader.read()) != -1) {
                System.out.print((char) ch);
            }
            reader.close();
        } catch (IOException e) {
            System.out.println("An error occurred while reading the file: " + e.getMessage());
        }
    }
}

OUTPUT:
File written successfully.
File content:
Hello, this is a simple File I/O example in Java.


````
## 165.Create a phonebook program with search functionality. 
````java[]

import java.util.*;
public class prg5 {

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        Map<String,String> res=new HashMap<>();
        while(true) {
            System.out.println("*****PhoneBook******");
            System.out.println("1. Add Contact ");
            System.out.println("2. Search a existing Contact ");
            System.out.println(" 3.Exit from the phonebook");
            System.out.println("Enter your choice");
            int choice=s.nextInt();
            switch(choice) {
                case 1:
                    System.out.println("Enter the name");
                    String name=s.nextLine();
                    s.nextLine();
                    System.out.println("Enter the phone num");
                    String no=s.nextLine();
                    res.put(name,no);
                    System.out.println("Contact has been added Successfully");
                    break;

                case 2:
                    System.out.println("Enter a name to search in the phonebook: ");
                    String searchName = s.nextLine();
                    s.nextLine();

                    if (res.containsKey(searchName)) {
                        System.out.println("Phone number: " + res.get(searchName));
                    } else {
                        System.out.println("Contact not found in the phonebook.");
                    }
                    break;

                case 3:
                    System.out.println("Thanks for using phonebook ! Good Bye");
                    return;
                default:
                    System.out.println("Invalid Input");
            }

        }

    }

}

OUTPUT:
*****PhoneBook******
1. Add Contact 
2. Search a existing Contact 
 3.Exit from the phonebook
Enter your choice
1
Enter the name
jasmine
Enter the phone num
9342343299
Contact has been added Successfully
*****PhoneBook******
1. Add Contact 
2. Search a existing Contact 
 3.Exit from the phonebook
Enter your choice
1
Enter the name
nanthini
Enter the phone num
963452153
Contact has been added Successfully
*****PhoneBook******
1. Add Contact 
2. Search a existing Contact 
 3.Exit from the phonebook
Enter your choice
3
Thanks for using phonebook ! Good Bye



````
## 166.Implement a ticket booking system with class and objects. 
````java[]














````
## 167.Create a random number generator for a guessing game. 
````java[]
import java.util.*;
public class prg7{

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        Random random=new Random();

        int numberToGuess=random.nextInt(100)+1;
        int attempt=0;
        int userinput=0;
        System.out.println("******NUMBER GUESSING GAME*****");
        System.out.println("GUESS A NUMBER BETWEEN 1 AND 100:");
        while(numberToGuess != userinput) {
            System.out.println("Enter the Guess");
            userinput=s.nextInt();
            attempt++;

            if(userinput < numberToGuess)
            {
                System.out.println("To low!Try Again");
            }
            else if(userinput> numberToGuess) {
                System.out.println("To high!Try Again");
            }
            else {
                System.out.println("Congratulations! You have guessed the number in " + attempt + " attempts.");
            }
        }

    }

}

OUTPUT:
******NUMBER GUESSING GAME*****
GUESS A NUMBER BETWEEN 1 AND 100:
Enter the Guess
50
To low!Try Again
Enter the Guess
100
To high!Try Again
Enter the Guess
10
To low!Try Again
Enter the Guess
23
To low!Try Again
Enter the Guess
21
To low!Try Again
Enter the Guess
65
To low!Try Again
Enter the Guess
70
To high!Try Again
Enter the Guess
66
To low!Try Again
Enter the Guess
67
To low!Try Again
Enter the Guess
69
Congratulations! You have guessed the number in 10 attempts.

````
## 168 .Build a simple calendar program using loops. 
````java[]
import java.util.*;

public class prg8 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter total number of days in the month:");
        int day = sc.nextInt();
        System.out.println("Enter the starting day of the week (1 for Monday, 7 for Sunday):");
        int start = sc.nextInt();
        System.out.println("  Mon  Tue  Wed  Thu  Fri  Sat  Sun ");
        
        int days = 1;
        int current = start - 1;

        // Print initial spaces for the first week
        for (int i = 0; i < current; i++) {
            System.out.print("     ");
        }

        // Print the days of the month
        for (int i = current; days <= day; i++) {
            System.out.printf("%4d ", days);
            if ((i + 1) % 7 == 0) {  // New line after Sunday
                System.out.println();
            }
            days++;
        }
        sc.close();
    }
}


OUTPUT:
Enter the total number of days present in the month:
28
Enter the starting day of the week: 
2
  Mon  Tue  Wed  Thu  Fri  Sat  Sun 
        1    2    3    4    5    6 
   7    8    9   10   11   12   13 
  14   15   16   17   18   19   20 
  21   22   23   24   25   26   27 
  28 

````
## 169.Create a program that checks for valid email addresses. 
````java[]

import java.util.*;
import java.util.regex.*;

public class prg9{
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter an email address: ");
        String email = scanner.nextLine();

        if (isValidEmail(email)) {
            System.out.println("Valid email address.");
        } else {
            System.out.println("Invalid email address.");
        }

        scanner.close();
    }

    public static boolean isValidEmail(String email) {
        String emailRegex = "^[A-Za-z0-9+_.-]+@[A-Za-z0-9.-]+$";
        Pattern pattern = Pattern.compile(emailRegex);
        Matcher matcher = pattern.matcher(email);
        return matcher.matches();
    }
}


OUTPUT:
Enter an email address: jasmine@gmail.com
Valid email address.


````
## 170 .Build a number encryption/decryption program.
````java[]







````
## 171.Create a weather app interface using control statements. 
````java[]

import java.util.*;

public class prg10{
    public static void main(String[] args) {
        Scanner sc= new Scanner(System.in);

        System.out.print("Enter the temperature in Celsius: ");
        int temperature = sc.nextInt();

        System.out.print("Is it raining? (yes/no): ");
        String raining = sc.next().toLowerCase();

        System.out.println("\nWeather Forecast:");

        if (temperature < 0) {
            System.out.println("It's too cold!");
        } else if (temperature < 15) {
            System.out.println("It's cold.");
        } else if (temperature < 25) {
            System.out.println("The weather is good and humid.");
        } else {
            System.out.println("It's warm.");
        }

        if (raining.equals("yes")) {
            System.out.println("Carry your umbrella!");
        }



        sc.close();
    }
}

OUTPUT:

Enter the temperature in Celsius: 69
Is it raining? (yes/no): no

Weather Forecast:
It's warm.


````
## 172.Write a program for bubble sort. 
````java[]


import java.util.*;
public class prg11
{
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int[] arr=new int[n];
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        bubblesort(arr,n);
        for(int i=0;i<n;i++){
            System.out.print(arr[i]+" ");
        }

    }
    public static void bubblesort(int[] arr,int n){
        for(int i=0;i<n;i++){
            for(int j=i;j<n-1-i;j++){
                if(arr[j]>arr[j+1]){
                    int temp=arr[j];
                    arr[j]=arr[j+1];
                    arr[j+1]=temp;
                }
            }
        }

    }
}

OUTPUT:

5

15
22
2
7
63

15 2 7 22 63


````
## 173.Implement insertion sort using loops.
````java[]


import java.util.*;
public class prg12{
    public static void insertionSort(int a[],int n) {
        for(int i=0;i<=n-2;i++) {
            for(int j=i+1;j>0;j--) {
                if(a[j] <a[j-1]) {
                    int temp=a[j];
                    a[j]=a[j-1];
                    a[j-1]=temp;
                }
                else {
                    break;
                }
            }
        }
    }
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the size of the array");
        int n=s.nextInt();
        int a[]=new int[n];
        System.out.println("Enter the element");
        for(int i=0;i<n;i++) {
            a[i]=s.nextInt();
        }
        System.out.println("After sorting");
        insertionSort(a,n);
        for(int i:a) {
            System.out.print(i+" ");
        }

    }

}


OUTPUT:

Enter the size of the array
5
Enter the element
36
22
15
30
28
After sorting
15 22 28 30 36 


````
## 174.Perform quicksort on an array using recursion. 
````java[]
import java.util.*;
public class prg13 {
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the size of the array");
        int n=s.nextInt();
        int array[]=new int[n];
        System.out.println("Enter the element");
        for(int i=0;i<n;i++) {
            array[i]=s.nextInt();
        }
        //System.out.println("Unsorted Array: " + Arrays.toString(array));
        quickSort(array, 0, array.length - 1);
        System.out.println("Sorted Array: " + Arrays.toString(array));

    }
    public static void quickSort(int[] arr, int low, int high) {
        if (low < high) {
            int pi = partition(arr, low, high);
            quickSort(arr, low, pi - 1);
            quickSort(arr, pi + 1, high);
        }
    }

    public static int partition(int[] arr, int low, int high) {
        int pivot = arr[high];
        int i = (low - 1);
        for (int j = low; j < high; j++) {
            if (arr[j] < pivot) {
                i++;
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
        int temp = arr[i + 1];
        arr[i + 1] = arr[high];
        arr[high] = temp;

        return i + 1;
    }
}

OUTPUT:


Enter the size of the array
5
Enter the element
21
66
33
22
15
Sorted Array: [15, 21, 22, 33, 66]

````
## 175.Implement selection sort with a loop. 
````java[]


import java.util.*;
public class prg14{
    public static void selectionSort(int arr[],int n) {
        for(int i=0;i<n-1;i++) {
            int midindex=i;
            for(int j=i+1;j<n;j++) {
                if(arr[j]<arr[midindex]) {
                    midindex=j;
                }
            }
            int temp=arr[midindex];
            arr[midindex]=arr[i];
            arr[i]=temp;
        }
    }

    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        System.out.println("Enter the size of the array");
        int n=s.nextInt();
        int arr[]=new int[n];
        System.out.println("Enter the elements to added in the array");
        for(int i=0;i<n;i++) {
            arr[i]=s.nextInt();
        }
        System.out.println("Elements after sorting");
        selectionSort(arr,n);
        for(int i:arr) {
            System.out.print(i+" ");
        }

    }

}

OUTPUT:

Enter the size of the array
5
Enter the elements to added in the array
23
62
41
15
33
Elements after sorting
15 23 33 41 62


````
## 176.Perform a binary search recursively.
````java[]


import java.util.*;

public class prg15{
    public static int binarySearch(int[] arr, int left, int right, int target) {
        if (left > right) {
            return -1;
        }
        int mid = left + (right - left) / 2;

        if (arr[mid] == target) {
            return mid;
        } else if (arr[mid] > target) {
            return binarySearch(arr, left, mid - 1, target);
        } else {
            return binarySearch(arr, mid + 1, right, target);
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the number of elements: ");
        int n = sc.nextInt();
        int[] arr = new int[n];

        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        System.out.print("Enter the target element");
        int target = sc.nextInt();

        int result = binarySearch(arr, 0, n - 1, target);

        if (result != -1) {
            System.out.println("Element found : " + result);
        } else {
            System.out.println("Element not found in the array.");
        }

        sc.close();
    }
}




OUTPUT:
Enter the number of elements: 
5
Enter the elements of the array:
15
22
33
44
5
Enter the target element22
Element found : 1

````
## 177.Create a class to manage a simple bank account. 
````java[]














````
## 178.Write a program for linear search recursively.
````java[]

import java.util.*;

public class prg16{
    public static int linearSearch(int[] arr, int index, int target) {
        if (index >= arr.length) {
            return -1;
        }
        if (arr[index] == target) {
            return index;
        }
        return linearSearch(arr, index + 1, target);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the number of elements: ");
        int n = sc.nextInt();
        int[] arr = new int[n];

        System.out.println("Enter the elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        System.out.print("Enter the target value: ");
        int target = sc.nextInt();

        int result = linearSearch(arr, 0, target);

        if (result != -1) {
            System.out.println("Element found : " + result);
        } else {
            System.out.println("Element not found in the array.");
        }

        sc.close();
    }
}


OUTPUT:
Enter the number of elements: 5
Enter the elements:
22
23
56
15
21
Enter the target value: 21
Element found : 4


````
## 179.Implement depth-first search using a stack. 
````java[]














````
## 180.Implement breadth-first search using a queue. 
````java[]














````
