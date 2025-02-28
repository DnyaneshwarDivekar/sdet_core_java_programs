# sdet_core_java_programs

# DataTypes

package datatypes;

import java.util.Scanner;

public class DataTypes {

    public static void main(String[] args) {

        // 1. Primitive Data Types

        // 1.1 Boolean
        boolean flag1 = true; // declare and assign value
        boolean flag2; // declaration
        flag2 = false; // value assignment

        System.out.println(flag1);
        System.out.println(flag2);

        // 1.2 Char
        char myChar1 = 'a';
        myChar1 = '1';
        char myChar2 = 'b';

        int myChar3 = myChar1 + myChar2;
        
        System.out.println(myChar1);
        System.out.println(myChar2);
        System.out.println(myChar3);

        // 1.3 Integer Numbers
        int myInt1 = 10;
        int myInt2 = 22;

        System.out.println(myInt1);
        System.out.println(myInt2);

        // 1.4 Decimal Numbers
        float myFloat1 = 2.1234567F;
        double myDouble = 3.4411111111;

        System.out.println(myFloat1);
        System.out.println(myDouble);

        // 2. Non-Primitive Data Types

        // 2.1 String
        String name = "Amit"; // Literal way
        String obj = new String("Dnyaneshwar");

        System.out.println(name);
        System.out.println(obj);

        // 2.2 Array
        System.out.println("Enter your array size:");

        Scanner sc = new Scanner(System.in); // dynamic values from user
        int value = sc.nextInt();
        sc.close();

        String[] arr = new String[value]; // fixed-size array
        arr[0] = "test1";
        arr[1] = "test2";
        arr[2] = "test3";

        System.out.println(arr[0]);

        // Integer Arrays
        int arr2[] = new int[5];
        int[] arr3 = new int[6];

        // 2.3 Class (Example class definition)
        // public class Test {}

        // 2.4 Interface (Example interface definition)
        // public interface Car {}

        // 2.5 Collections Examples
        // ArrayList
        // HashMap
        // HashSet
    }
}


# Variable Types

package day5;

public class Test {

    // Instance variable (non-static)
    int x = 10;

    // Static variable
    static int y = 20;

    public static void main(String[] args) {

        // Local variable
        int z = 30;

        System.out.println("DD");

        // Creating an object to access instance variable
        Test obj1 = new Test();

        System.out.println("Instance Variable : " + obj1.x);
        System.out.println("Static Variable : " + y);
        System.out.println("Local Variable : " + z);

        // Calculating sum of instance, static, and local variables
        int sum = obj1.x + y + z;

        System.out.println("Sum of x, y and z variable is : " + sum);

        // Expected vs Actual result validation
        // Expected: 60, Actual: 60 => Test Passed
        // Expected: 60, Actual: 0  => Test Failed
    }
}


# Default Constructor 

package day5;

public class Test2 {

    // Instance variables
    int x = 10;
    int w = 30;

    // Static variable
    static int y = 20;

    // Default constructor
    Test2() {
        System.out.println("I'm in the default constructor");
    }

    public static void main(String[] args) {

        // Creating an instance of the class
        Test2 obj2 = new Test2();

        // Accessing instance variables
        int z = obj2.x;

        System.out.println(z);
        System.out.println(obj2.w);

        // Accessing static variable directly
        System.out.println(y);
    }
}


# Cosntructor Use

package day6;

public class Student {

    String studentName; // Instance variable for student name

    public static void main(String[] args) {

        // Creating a College object and setting branch name
        College obj1 = new College(); 
        obj1.branchName = "Arts";

        System.out.println(obj1.branchName);

        // Student 1: Amit, Arts
        Student student1 = new Student(); 
        student1.studentName = "Amit";
        System.out.println(student1.studentName);
        student1.attendClass(); 
        System.out.println(College.collegeName);

        System.out.println("++++++++++++++++++++++++++++++++++++++++++++++++++++++");

        // Student 2: Sumit, Commerce
        Student student2 = new Student(); 
        student2.studentName = "Sumit";
        System.out.println(student2.studentName);
        student2.attendClass(); 
        System.out.println(College.collegeName);

        College obj2 = new College(); 
        obj2.branchName = "Commerce";
        System.out.println(obj2.branchName);

        System.out.println("++++++++++++++++++++++++++++++++++++++++++++++++++++++");

        // Student 3: Manit, Science
        Student student3 = new Student(); 
        student3.studentName = "Manit";
        System.out.println(student3.studentName);

        College obj3 = new College(); 
        obj3.branchName = "Science";

        System.out.println(College.collegeName);
    }

    // Instance method for attending class
    public void attendClass() {
        System.out.println("I'm attending my class");
    }
}

package day6;

public class College {

    // Static variable for common college name
    static String collegeName = "Pune College"; 

    // Instance variable for branch name
    String branchName; 

    public static void main(String[] args) {
        // Main method can be used for testing or additional logic if needed
    }
}


# Use of configuration arguments 

package day7;

import java.util.Scanner;

public class ArgumentsClass {

    public static void main(String[] args) {

        // Way 1: From config args (uncomment to use)
        // System.out.println(args[1]);

        // Way 2: Using Scanner Class for user input
        Scanner obj = new Scanner(System.in); 

        System.out.println("Please enter the string/text value: ");
        String userString = obj.nextLine(); // = assign, == compare 

        System.out.println("The user entered the value: " + userString);

        obj.close(); // Closing the scanner to prevent resource leak
    }
}


# Mini Project - Simple Calculator 

package feb10;

import java.util.Scanner;

public class SimpleCalculator {

    /*
     * Functionalities:
     * 1) Addition
     * 2) Subtraction
     * 3) Multiplication
     * 4) Division
     * 5) Modulus
     */

    public static void main(String[] args) {

        System.out.println("*************************************************************************");
        System.out.println("-------------------- Welcome to the Calculator App!! ---------------------");
        System.out.println("*************************************************************************");
        
        System.out.println("This is a Simple Calculator App with functionalities like:");
        System.out.println("1) Addition");
        System.out.println("2) Subtraction");
        System.out.println("3) Multiplication");
        System.out.println("4) Division");
        System.out.println("5) Modulus");
        
        System.out.println("*************************************************************************");
        System.out.println("Please enter your choice (1, 2, 3, 4, 5):");
        System.out.println("*************************************************************************");

        Scanner sc = new Scanner(System.in);
        int choice = sc.nextInt();

        System.out.println("You have entered your choice as: " + choice);

        if (choice > 5 || choice < 1) { 
            System.out.println("Invalid input. Please select a number from 1 to 5.");
            sc.close();
            return;
        }

        System.out.println("*************************************************************************");
        System.out.println("Please enter the first number: ");
        int num1 = sc.nextInt();

        System.out.println("Please enter the second number: ");
        int num2 = sc.nextInt();

        System.out.println("You have entered the numbers as: " + num1 + " and " + num2);
        System.out.println("*************************************************************************");

        // Handling all cases using If-Else-If statement
        if (choice == 1) { 
            int result = num1 + num2;
            System.out.println("The addition of num1 and num2: " + result);

        } else if (choice == 2) { 
            int result = num1 - num2;
            System.out.println("The subtraction of num1 and num2: " + result);

        } else if (choice == 3) { 
            int result = num1 * num2;
            System.out.println("The multiplication of num1 and num2: " + result);

        } else if (choice == 4) { 
            if (num2 != 0) {
                int result = num1 / num2;
                System.out.println("The division of num1 and num2: " + result);
            } else {
                System.out.println("Error: Division by zero is not allowed.");
            }

        } else if (choice == 5) { 
            if (num2 != 0) {
                int result = num1 % num2;
                System.out.println("The remainder of num1 and num2: " + result);
            } else {
                System.out.println("Error: Modulus by zero is not allowed.");
            }
        }

        sc.close();
    }
}


# Mini Project - ATM Card App

package feb12;

import java.util.Scanner;

public class ATMCardProgram {

    static int balance = 100; // Initial account balance
    static int pin = 0; // PIN code (currently unused)

    static String[] statementArray = new String[5]; // Array to store transaction statements (max 5)
    static int transactionCount = 0; // Counter for transactions

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        while (true) {

            System.out.println("+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++");
            System.out.println("This is a program for ATM/Debit Card ");
            System.out.println("1) Balance");
            System.out.println("2) Withdraw");
            System.out.println("3) Deposit");
            System.out.println("4) Mini Statement");
            System.out.println("5) Exit");
            System.out.println("+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++");
            System.out.println("Please select your choice from 1 to 5: ");

            int choice = sc.nextInt();

            switch (choice) {

                case 1: // Balance Inquiry
                    System.out.println("Your current balance is: " + balance);
                    break;

                case 2: // Withdraw
                    System.out.println("Please enter the withdrawal amount: ");
                    int withdrawAmount = sc.nextInt();

                    if (withdrawAmount > balance) {
                        System.out.println("Insufficient funds! Your current balance is: " + balance);
                    } else if (withdrawAmount <= 0) {
                        System.out.println("Invalid withdrawal amount! Please enter a positive value.");
                    } else {
                        balance -= withdrawAmount;
                        String message1 = "You have successfully withdrawn amount: " + withdrawAmount;
                        System.out.println(message1);
                        System.out.println("Now, remaining balance is: " + balance);
                        addToStatement(message1);
                    }
                    break;

                case 3: // Deposit
                    System.out.println("Please enter the deposit amount: ");
                    int depositAmount = sc.nextInt();

                    if (depositAmount <= 0) {
                        System.out.println("Invalid deposit amount! Please enter a positive value.");
                    } else {
                        balance += depositAmount;
                        String message2 = "You have successfully deposited/credited amount: " + depositAmount;
                        System.out.println(message2);
                        System.out.println("Now, current balance is: " + balance);
                        addToStatement(message2);
                    }
                    break;

                case 4: // Mini Statement
                    System.out.println("Your last " + transactionCount + " transactions are: ");
                    for (int i = 0; i < transactionCount; i++) {
                        System.out.println((i + 1) + ") " + statementArray[i]);
                    }
                    break;

                case 5: // Exit
                    System.out.println("You have successfully logged out!!");
                    sc.close();
                    System.exit(0); // Terminate the program

                default:
                    System.out.println("Invalid choice! Please select a number from 1 to 5.");
            }
        }
    }

    /**
     * Adds a transaction message to the statement array, maintaining a maximum of 5 entries.
     * 
     * @param message The transaction message to be added
     */
    private static void addToStatement(String message) {
        if (transactionCount < statementArray.length) {
            statementArray[transactionCount++] = message;
        } else {
            // Shift statements to make room for new entry (FIFO approach)
            for (int i = 1; i < statementArray.length; i++) {
                statementArray[i - 1] = statementArray[i];
            }
            statementArray[statementArray.length - 1] = message;
        }
    }
}

# Mini Project - Simple Calculator with Switch Case

package feb12;

import java.util.Scanner;

public class SimpleCalculatorSwitch {

    /**
     * This is a Simple Calculator App with functionalities:
     * 1) Addition
     * 2) Subtraction
     * 3) Multiplication
     * 4) Division
     * 5) Modulus
     */
    
    public static void main(String[] args) {

        boolean flag = true;
        Scanner sc = new Scanner(System.in);

        do {
            System.out.println("*************************************************************************");
            System.out.println("--------------------Welcome to the Calculator App!!----------------------");
            System.out.println("*************************************************************************");
            System.out.println("This is a Simple Calculator App having functionalities like:");
            System.out.println("1) Addition");
            System.out.println("2) Subtraction");
            System.out.println("3) Multiplication");
            System.out.println("4) Division");
            System.out.println("5) Modulus");
            System.out.println("*************************************************************************");

            System.out.println("Please enter the first number: ");
            int num1 = sc.nextInt();

            System.out.println("Please enter the second number: ");
            int num2 = sc.nextInt();

            System.out.println("You have entered the numbers as: " + num1 + " and " + num2);
            System.out.println("*************************************************************************");

            System.out.println("Please enter your choice between 1, 2, 3, 4, 5:");
            System.out.println("1) Addition 2) Subtraction 3) Multiplication 4) Division 5) Modulus");
            System.out.println("*************************************************************************");

            int choice = sc.nextInt();
            System.out.println("You have entered your choice as: " + choice);

            switch (choice) {

                case 1: // Addition
                    System.out.println("The addition of num1 and num2: " + (num1 + num2));
                    break;

                case 2: // Subtraction
                    System.out.println("The subtraction of num1 and num2: " + (num1 - num2));
                    break;

                case 3: // Multiplication
                    System.out.println("The multiplication of num1 and num2: " + (num1 * num2));
                    break;

                case 4: // Division
                    if (num2 != 0) {
                        System.out.println("The division of num1 and num2: " + (num1 / num2));
                    } else {
                        System.out.println("Error: Division by zero is not allowed.");
                    }
                    break;

                case 5: // Modulus
                    if (num2 != 0) {
                        System.out.println("The modulus of num1 and num2: " + (num1 % num2));
                    } else {
                        System.out.println("Error: Modulus by zero is not allowed.");
                    }
                    break;

                default:
                    System.out.println("Invalid input. Please select a number from 1 to 5.");
            }

            System.out.println("*************************************************************************");
            System.out.println("Do you want to continue? (true/false): ");
            System.out.println("*************************************************************************");

            flag = sc.nextBoolean();

        } while (flag);

        sc.close();
    }
}


# Character Switch Case 

package feb12;

import java.util.Scanner;

/**
 * A program to check if the entered character is a vowel using a switch case.
 */
public class SwitchCase {

    public static void main(String[] args) {

        System.out.println("Character switch case:");
        System.out.println("This is the program to check Vowels: a, e, i, o, u, A, E, I, O, U");

        Scanner sc = new Scanner(System.in);

        System.out.println("Please enter any character: ");

        char choice = sc.next().charAt(0); // Read the input character from the user

        // Switch case to check for vowels
        switch (choice) {

            case 'a':
                System.out.println("This is a vowel: " + choice);
                break;

            case 'e':
                System.out.println("This is a vowel: " + choice);
                break;

            case 'i':
                System.out.println("This is a vowel: " + choice);
                break;

            case 'o':
                System.out.println("This is a vowel: " + choice);
                break;

            case 'u':
                System.out.println("This is a vowel: " + choice);
                break;

            case 'A':
                System.out.println("This is a vowel: " + choice);
                break;

            case 'E':
                System.out.println("This is a vowel: " + choice);
                break;

            case 'I':
                System.out.println("This is a vowel: " + choice);
                break;

            case 'O':
                System.out.println("This is a vowel: " + choice);
                break;

            case 'U':
                System.out.println("This is a vowel: " + choice);
                break;

            default:
                System.out.println("Entered character is not a vowel.");
        }
        
        sc.close(); // Close the scanner object to prevent resource leak
    }
}

package feb12;

import java.util.Scanner;

/**
 * A program to check if the entered character is a vowel using a switch case.
 */
public class SwitchCase2 {

    public static void main(String[] args) {

        System.out.println("Character switch case:");
        System.out.println("This is the program to check Vowels: a, e, i, o, u, A, E, I, O, U");

        Scanner sc = new Scanner(System.in);

        System.out.println("Please enter any character: ");

        char choice = sc.next().charAt(0); // Read the input character from the user

        boolean flag = false;

        // Switch case to check for vowels (grouped cases for efficiency)
        switch (choice) {
            case 'a':
            case 'e':
            case 'i':
            case 'o':
            case 'u':
            case 'A':
            case 'E':
            case 'I':
            case 'O':
            case 'U':
                flag = true;
        }

        // Output the result based on the flag
        if (flag) {
            System.out.println("This is a vowel: " + choice);
        } else {
            System.out.println("Entered character is not a vowel.");
        }
        
        sc.close(); // Close the scanner to avoid resource leaks
    }
}


# Nested For Loops

package feb14;

import java.util.Scanner;

/**
 * This program prints the multiplication tables from a starting index to an ending index.
 * It uses nested for-loops to generate and display the tables.
 */
public class NestedForLoops {

    public static void main(String[] args) {

        System.out.println("Enter the starting table index: ");

        Scanner sc = new Scanner(System.in);
        int start = sc.nextInt();

        System.out.println("Enter the ending table index: ");
        int end = sc.nextInt();

        if (start > end) {
            System.out.println("Invalid start and end index. The start index should be less than or equal to the end index.");
        } else {
            // Outer loop to iterate through each table from 'start' to 'end'
            for (int i = start; i <= end; i++) {
                // Inner loop to generate each multiplication step for the table
                for (int j = 1; j <= 10; j++) {
                    System.out.println(i + " * " + j + " = " + (i * j));
                }
                System.out.println("++++++++++++++++++");
            }
        }

        System.out.println("+++++++++ Out of both loops ++++++++");

        sc.close(); // Close the scanner to avoid resource leaks
    }
}


# Nested If Else 
package feb14;

/**
 * This program compares three numbers and determines the largest among them 
 * using nested if-else statements.
 */
public class NestedIfCode {

    public static void main(String[] args) {

        // Initialization of three numbers to be compared
        int a = 100;
        int b = 500;
        int c = 3000;

        /**
         * Outer if-else block:
         * 1. Checks if 'a' is greater than 'b'.
         * 2. If true, enters the inner if-else to compare 'a' and 'c'.
         * 3. If false, enters the else block to compare 'b' and 'c'.
         */
        if (a > b) { // Case 1: When 'a' is greater than 'b'

            /**
             * Inner if-else block:
             * Compares 'a' with 'c' to determine if 'a' is the largest.
             */
            if (a > c) {
                System.out.println("a is the largest");
            } else {
                System.out.println("c is the largest");
            }

        } else { // Case 2: When 'b' is greater than or equal to 'a'

            /**
             * Inner if-else block:
             * Compares 'b' with 'c' to determine if 'b' is the largest.
             */
            if (b > c) {
                System.out.println("b is the largest");
            } else {
                System.out.println("c is the largest");
            }

        }
    }
}


# Star Pattern 

package feb14;

/**
 * Program to print a pattern of stars in a decreasing order with spaces.
 */
public class StarPrinting {

    public static void main(String[] args) {

        // Outer loop to control the number of rows (from 5 to 1)
        for (int i = 5; i >= 1; i--) {

            // Inner loop to print stars in each row
            for (int j = i; j >= 1; j--) {
                System.out.print("* ");
            }

            // Move to the next line after printing stars
            System.out.println("");

            // Inner loop to print spaces for alignment
            for (int k = i; k <= 5; k++) {
                System.out.print("  ");
            }
        }

        /*
         * Alternative pattern:
         * Prints an increasing triangle of stars
         * 
         * for (int i = 1; i <= 10; i++) {
         *     for (int j = 1; j <= i; j++) {
         *         System.out.print("* ");
         *     }
         *     System.out.println("");
         * }
         */
    }
}

package feb17;

/**
 * Program to print various star patterns using nested loops.
 */
public class StartPrinting {

    public static void main(String[] args) {

        System.out.println("++++++++++++++ Use of 2 for loops ++++++++++++++++++++++");

        // Square pattern of stars
        System.out.println("WAP to print square of stars");
        for (int i = 1; i <= 5; i++) {		
            for (int j = 1; j <= 5; j++) {
                System.out.print("* ");
            }
            System.out.println("");
        }

        // Rectangle pattern of stars (10 rows, 5 columns)
        System.out.println("WAP to print rectangle of stars");
        for (int i = 1; i <= 10; i++) {		
            for (int j = 1; j <= 5; j++) {
                System.out.print("* ");
            }
            System.out.println("");
        }

        // Rectangle pattern of stars (5 rows, 10 columns)
        System.out.println("WAP to print rectangle of stars");
        for (int i = 1; i <= 5; i++) {		
            for (int j = 1; j <= 10; j++) {
                System.out.print("* ");
            }
            System.out.println("");
        }

        // Right-angled triangle of stars (increasing)
        System.out.println("WAP to print right angled triangle of stars");
        for (int i = 1; i <= 5; i++) {		
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println("");
        }

        // Right-angled triangle of stars (decreasing)
        System.out.println("WAP to print right angled triangle of stars");
        for (int i = 1; i <= 5; i++) {		
            for (int j = i; j <= 5; j++) {
                System.out.print("* ");
            }
            System.out.println("");
        }

    }

}

package feb17;

/**
 * Program to print a right-angled triangle of stars with increasing star patterns.
 */
public class TrianglePrint {

    public static void main(String[] args) {

        String str = "";

        System.out.println("WAP to print right angled triangle of stars");

        for (int i = 1; i <= 5; i++) {

            for (int j = i; j <= 5; j++) {

                str = str + "*";
                System.out.print(str + " ");
            }

            System.out.println("");
        }
    }
}


# Prime Number
package feb18;

import java.util.Scanner;

/**
 * Program to print the prime number series up to a given limit.
 */
public class PrimeNumberSeries {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.println("Please enter the series end: ");

        int end = sc.nextInt();

        System.out.println("*******************The prime number series**************************************************");

        for (int num = 2; num <= end; num++) {

            int factorCount = 2;

            for (int i = 2; i < num; i++) {

                if (num % i == 0) {
                    factorCount++;
                }
            }

            if (factorCount <= 2) {
                System.out.print(num + ", ");
            }
        }

        System.out.println("\n**********************************************************************************************");
    }
}

package feb26;

import java.util.Scanner;

/**
 * Program to check if a given number is a prime number.
 */
public class PrimeNumber {

    public static void main(String[] args) {

        System.out.println("This is a program to find out if the given number is a prime number or not.");

        System.out.println("Please enter an integer number: ");

        Scanner scannerObject = new Scanner(System.in);

        int inputNumber = scannerObject.nextInt(); // capturing user input

        int factorCount = 0;

        // Calculate the number of factors
        for (int index = 1; index <= inputNumber; index++) {

            if (inputNumber % index == 0) {
                factorCount++;
            }
        }

        // Check if the input number is a prime number
        if (factorCount == 2) {
            System.out.println("The given number is a prime number: " + inputNumber);
        } else {
            System.out.println("The given number is NOT a prime number: " + inputNumber);
        }
    }
}


package feb26;

import java.util.Scanner;

/**
 * Program to find and print the prime number series up to a given end number.
 */
public class PrimeNumberSeries {

    public static void main(String[] args) {

        System.out.println("This is a program to find the prime number series.");

        Scanner scannerObject = new Scanner(System.in);

        System.out.println("Please enter the end number: ");

        int endNumber = scannerObject.nextInt(); // capturing user input

        // Loop through numbers from 2 to endNumber to find prime numbers
        for (int inputNumber = 2; inputNumber <= endNumber; inputNumber++) {

            int factorCount = 0;

            // Check factors for each number
            for (int index2 = 1; index2 <= inputNumber; index2++) {

                if (inputNumber % index2 == 0) {
                    factorCount++;
                }
            }

            // If the number has only 2 factors, it's a prime number
            if (factorCount == 2) {
                System.out.print(inputNumber + " , ");
            }
        }
    }
}


package feb26;

import java.util.Scanner;

/**
 * Program to find and print the prime number series within a specified start and end range.
 */
public class PrimeNumberSeries2 {

    public static void main(String[] args) {

        System.out.println("This is a program to find the prime number series within a range.");

        Scanner scannerObject = new Scanner(System.in);

        System.out.println("Please enter the start number: ");
        int startNumber = scannerObject.nextInt();

        System.out.println("Please enter the end number: ");
        int endNumber = scannerObject.nextInt(); 

        // Loop through numbers from startNumber to endNumber to find prime numbers
        for (int inputNumber = startNumber; inputNumber <= endNumber; inputNumber++) {

            int factorCount = 0;

            // Check factors for each number
            for (int index2 = 1; index2 <= inputNumber; index2++) {

                if (inputNumber % index2 == 0) {
                    factorCount++;
                }
            }

            // If the number has only 2 factors, it's a prime number
            if (factorCount == 2) {
                System.out.print(inputNumber + " , ");
            }
        }
    }
}


package feb26;

import java.util.Scanner;

/**
 * Program to find the prime number series within a specified start and end range using a boolean flag.
 */
public class PrimeNumberSeries5 {

    public static void main(String[] args) {

        Scanner scannerObject = new Scanner(System.in);

        System.out.println("Please enter the start number: ");
        int startNumber = scannerObject.nextInt();

        System.out.println("Please enter the end number: ");
        int endNumber = scannerObject.nextInt();

        // Edge case validation for start and end numbers
        boolean testFlag = startNumber <= 1 || endNumber <= 1;

        if (testFlag) {
            System.out.println("The entered start and end numbers are incorrect. Please check once.");
            System.exit(0);
        }

        // Loop through numbers from startNumber to endNumber to find prime numbers
        for (int inputNum = startNumber; inputNum <= endNumber; inputNum++) {

            boolean flag = true; // True indicates a prime number, false indicates not a prime number

            // Check for factors starting from 2 to inputNum-1
            for (int index = 2; index < inputNum; index++) {

                if (inputNum % index == 0) {
                    flag = false;
                    break;
                }
            }

            // Print the number if it's a prime number
            if (flag) {
                System.out.print(inputNum + " , ");
            }
        }
    }
}


package feb26;

import java.util.Scanner;

/**
 * Program to check whether a given number is a prime number using a boolean flag.
 */
public class PrimeNumberWithFlag {

    public static void main(String[] args) {

        System.out.println("This is a program to find out if the given number is a prime number.");

        System.out.println("Please enter an integer number: ");

        Scanner scannerObject = new Scanner(System.in);
        int inputNumber = scannerObject.nextInt();

        boolean flag = true; // True indicates a prime number, false indicates not a prime number

        // Check divisibility from 2 to inputNumber-1
        for (int index = 2; index < inputNumber; index++) {

            if (inputNumber % index == 0) {
                flag = false;
                break;
            }
        }

        // Output based on the flag status
        if (flag) {
            System.out.println("The given number is a prime number: " + inputNumber);
        } else {
            System.out.println("The given number is NOT a prime number: " + inputNumber);
        }
    }
}


# Armstrong Number

package feb16;

/**
 * Program to check if a given number is an Armstrong number.
 * An Armstrong number is a number that is equal to the sum of the cubes of its digits.
 * Examples of Armstrong numbers: 0, 1, 153, 370, 371, 407
 * Example: 153 = (1^3) + (5^3) + (3^3) = 1 + 125 + 27 = 153
 */
public class ArmstrongNumber {

    public static void main(String[] args) {

        int num = 153;
        int orgNum = num;
        int sum = 0;

        while (num > 0) {
            int digit = num % 10;
            sum = sum + (digit * digit * digit);
            num = num / 10;
        }

        if (orgNum == sum) {
            System.out.println("The given number " + orgNum + " is an Armstrong number.");
        } else {
            System.out.println("The given number " + orgNum + " is not an Armstrong number.");
        }
    }
}


# Fibonacci Series 

package feb16;

/**
 * Program to print the Fibonacci series and find the nth term using both iterative and recursive approaches.
 * Fibonacci Series Example: 0, 1, 1, 2, 3, 5, 8, 13, 21, ...
 */
public class PrintFibonacci {
	
	static int arr[];

	public static void main(String[] args) {

		int n = 9; // Fibonacci series up to the 9th term

		arr = new int[n];
		
//		printFibonacciSeries(arr, n);
		
		int tn = printFibonacciSeriesWithRecursion(n);
		
		System.out.println("The " + n + "th term of the Fibonacci series: " + tn);
		
		for (int num : arr) {
			System.out.print(num + ", ");
		}
	}
	
	static int count = 2;
	
	public static int printFibonacciSeriesWithRecursion(int n) {

		int t0 = 0;
		int t1 = 1;
		int tn = 0;
		
		arr[0] = t0;
		arr[1] = t1;

		// Base cases
		if (n < 1) {
			return -1;
		}
		if (n == 1) {
			return 0;
		}
		if (n == 2) {
			return 1;
		}

		t0 = printFibonacciSeriesWithRecursion(n - 1);
		t1 = printFibonacciSeriesWithRecursion(n - 2);
			
		tn = t0 + t1;

		return tn;
	}
	
	
	public static void printFibonacciSeries(int arr[], int n) {
		
		int count = 2;
		int t0 = 0;
		int t1 = 1;

		arr[0] = t0;
		arr[1] = t1;
		
		while (n > 2) {

			int tn = t0 + t1;

			t0 = t1;
			t1 = tn;

			arr[count++] = tn;

			n--;
		}

		for (int num : arr) {
			System.out.print(num + " , ");
		}
	}

}

# Reverse a String

package feb16;

public class ReverseString {

    public static void main(String[] args) {

        // Que 1) WAP to reverse the given string

        // Sample input => Mauli
        // Sample output => iluaM

        String input = "Mauli"; 

        System.out.println("Original String : " + input);

        System.out.print("Reversed String : ");

        // Using input.length() - 1 to handle strings of any length dynamically
        for (int i = input.length() - 1; i >= 0; i--) {
            System.out.print(input.charAt(i));
        }

    }
}

# SumOfIntegers
package feb16;

/**
 * This program calculates the sum of the digits of a given integer.
 * Example:
 * Input: 12345
 * Output: 15 (1 + 2 + 3 + 4 + 5)
 */
public class SumOfIntegers {

    public static void main(String[] args) {

        int num = 12345; // Input number
        int sum = 0; // Variable to store the sum of digits

        /**
         * Loop through each digit of the number.
         * Extract the last digit using modulus operator (%).
         * Add the digit to the sum.
         * Remove the last digit by dividing the number by 10.
         */
        while (num > 0) {
            int digit = num % 10; // Extract the last digit
            sum = sum + digit; // Add digit to the sum
            num = num / 10; // Remove the last digit
        }

        System.out.println("The sum of the digits is: " + sum);
    }

}

# Swap2Integers

package feb16;

/**
 * This program demonstrates how to swap two integers using a temporary variable.
 * 
 * Example:
 * Input: num1 = 10, num2 = 20
 * Output: num1 = 20, num2 = 10
 */
public class Swap2Integers {

    public static void main(String[] args) {

        int num1 = 10, num2 = 20; // Initial values of num1 and num2

        System.out.println("Before swapping:");
        System.out.println("num1 = " + num1);
        System.out.println("num2 = " + num2);

        // Swapping logic using a temporary variable
        int temp = num1; // Store num1 in temp
        num1 = num2;      // Assign num2 to num1
        num2 = temp;      // Assign temp (original num1) to num2

        System.out.println("\nAfter swapping:");
        System.out.println("num1 = " + num1);
        System.out.println("num2 = " + num2);
    }

}

# SwapStrings

package feb16;

/**
 * This program demonstrates how to swap two strings using a temporary variable.
 * 
 * Example:
 * Input: str1 = "Test", str2 = "Automation"
 * Output: str1 = "Automation", str2 = "Test"
 */
public class SwapStrings {

    public static void main(String[] args) {

        String str1 = "Test";       // Initial value of str1
        String str2 = "Automation"; // Initial value of str2

        System.out.println("Before swapping:");
        System.out.println("str1 = " + str1);
        System.out.println("str2 = " + str2);

        // Swapping logic using a temporary variable
        String temp = str1; // Store str1 in temp
        str1 = str2;         // Assign str2 to str1
        str2 = temp;         // Assign temp (original str1) to str2

        System.out.println("\nAfter swapping:");
        System.out.println("str1 = " + str1);
        System.out.println("str2 = " + str2);
    }

}


# PalindromeNumber

package feb21;

/**
 * This program checks whether a given number is a palindrome.
 * 
 * A palindrome number is a number that remains the same when its digits are reversed.
 * 
 * Example:
 * Input: 121
 * Output: The given number is a palindrome.
 * 
 * Input: 12345
 * Output: The given number is not a palindrome.
 */
public class PalindromeNumber {

    public static void main(String[] args) {

        int num = 12345; // Input number to check for palindrome
        int orgNum = num; // Store original number for comparison

        System.out.println("The original number is: " + orgNum);

        int revNum = 0; // Variable to store the reversed number

        // Logic to reverse the digits of the input number
        while (num > 0) {

            int digit = num % 10; // Extract the last digit
            revNum = revNum * 10 + digit; // Append digit to the reversed number
            num = num / 10; // Remove the last digit from the original number

        }

        System.out.println("The reversed number is: " + revNum);

        // Check if the original number is equal to the reversed number
        if (orgNum == revNum) {
            System.out.println("*********** The given number is a palindrome **********");
        } else {
            System.out.println("*********** The given number is not a palindrome ***********");
        }

    }

}

# Single Level Inheritance demonstration

package feb28.inheritance.revision;

// Parent class definition
class Parent {

    String name = "Dnyaneshwar"; // Variable to store name

    // Method to display the name
    public void displayName() {
        System.out.println("The method from Parent class : " + name);
    }
}

// Child class extending Parent class (Single Level Inheritance)
class Child extends Parent {

    String role = "Tester"; // Variable to store role

    // Method to display the role
    public void displayRole() {
        System.out.println("The child class method : " + role);
    }
}

// Main class to execute the program
public class Main1 {

    public static void main(String[] args) {

        // Single Level Inheritance demonstration
        Child child = new Child(); // Creating an instance of Child class

        // Accessing Parent class properties through Child class object
        System.out.println(child.name); // Displaying parent class variable
        child.displayName(); // Calling parent class method

        // Accessing Child class properties
        System.out.println(child.role); // Displaying child class variable
        child.displayRole(); // Calling child class method
    }
}

# Multilevel Inheritance - Minimum 3 classes required

package feb28.inheritance.revision;

// GrandParent class (Superclass)
class GrandParent { 

    String gpProperty = "land"; // Property of GrandParent class

    // Method to demonstrate the use of GrandParent's property
    public void useGPProperty() {
        System.out.println("I'm using my grandparent property");
    }
}

// Parent2 class (Derived from GrandParent, Superclass for Child2)
class Parent2 extends GrandParent { 

    String parentProperty = "home"; // Property of Parent2 class

    // Method to demonstrate the use of Parent2's property
    public void useParentProperty() {
        System.out.println("I'm using my parent property");
    }
}

// Child2 class (Derived from Parent2, demonstrating Multilevel Inheritance)
class Child2 extends Parent2 { 

    String childProperty = "iPhone"; // Property of Child2 class

    // Method to demonstrate the use of Child2's property
    public void useChildProperty() {
        System.out.println("I'm using my own iPhone");
    }

    public static void main(String[] args) {

        // Multilevel Inheritance - Minimum 3 classes required
        
        // GrandParent Class Object
        GrandParent gp = new GrandParent();        
        gp.useGPProperty(); // Accessing GrandParent class method
        
        // Parent2 Class Object
        Parent2 parent2 = new Parent2();        
        parent2.useParentProperty(); // Accessing Parent2 class method
        parent2.useGPProperty(); // Accessing GrandParent class method through Parent2
        
        // Child2 Class Object
        Child2 child2 = new Child2();
        
        // Accessing properties from all levels of the hierarchy
        System.out.println(child2.childProperty); // Child2 class property
        System.out.println(child2.parentProperty); // Parent2 class property
        System.out.println(child2.gpProperty); // GrandParent class property

        // Accessing methods from all levels of the hierarchy
        child2.useParentProperty(); // Parent2 class method
        child2.useGPProperty(); // GrandParent class method
        child2.useChildProperty(); // Child2 class method
    }
}

# Hierarchical Inheritance

package feb28.inheritance.revision;

// Parent Class for Hierarchical Inheritance
public class HierachicalClass { 

    String parentProperty = "Car"; // Parent class property

    // Method to demonstrate the use of Parent's property
    public void driveCar() {
        System.out.println("I'm driving Car : " + parentProperty);
    }

    public static void main(String[] args) {

        // Hierarchical Inheritance involves one parent class and multiple child classes
        
        // Boy class object (Child class 1)
        Boy boy = new Boy();
        
        // Accessing Boy class properties and methods
        System.out.println(boy.boyProperty); // Boy class property
        boy.rideBike(); // Boy class method
        
        // Accessing Parent class properties and methods through Boy class
        System.out.println(boy.parentProperty); // Parent class property
        boy.driveCar(); // Parent class method
        
        // Girl class object (Child class 2)
        Girl girl = new Girl();
        
        // Accessing Girl class properties and methods
        System.out.println(girl.girlProperty); // Girl class property
        girl.rideScooty(); // Girl class method
        
        // Accessing Parent class properties and methods through Girl class
        System.out.println(girl.parentProperty); // Parent class property
        girl.driveCar(); // Parent class method
    }
}

// Boy class (Child class inheriting from HierachicalClass)
class Boy extends HierachicalClass { 

    String boyProperty = "Bike"; // Boy class property

    // Method to demonstrate the use of Boy's property
    public void rideBike() {
        System.out.println("I'm riding bike from boy class : " + boyProperty);
    }
}

// Girl class (Another Child class inheriting from HierachicalClass)
class Girl extends HierachicalClass { 

    String girlProperty = "Scooty"; // Girl class property

    // Method to demonstrate the use of Girl's property
    public void rideScooty() {
        System.out.println("I'm riding my scooty from girl class");
    }
}
