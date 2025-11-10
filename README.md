# ATM_mini-project
A Mini project of ATM machine for CU report fole

PROJECT REPORT

Title:

ATM Simulation System using C Programming


---

AIM:

To design and implement a simple ATM simulation program in C that allows users to check balance, deposit money, and withdraw money interactively.


---

OBJECTIVES:

1. To understand and apply the concept of decision-making and looping in C.


2. To develop a console-based simulation that performs basic banking operations.


3. To demonstrate the use of variables, conditional statements, and input/output handling.


4. To practice modular programming through switch-case implementation.




---

INTRODUCTION OF THE PROJECT:

The ATM Simulation System is a console-based program designed to replicate the basic functionalities of an Automated Teller Machine. The program enables users to check their account balance, deposit funds, and withdraw money. It demonstrates core programming concepts like conditionals, loops, and user input validation.

In a real-world ATM, multiple security and backend systems are involved; however, this project focuses solely on the logical operations behind balance management.


---

METHODOLOGY:

1. Problem Definition: Identify the core ATM operations—Check Balance, Deposit, Withdraw, and Exit.


2. Design: Use a while loop to keep displaying the menu until the user chooses to exit.


3. Implementation:

Use switch-case statements for menu selection.

Use conditional checks to validate deposit and withdrawal operations.



4. Testing: Run multiple scenarios to ensure correct balance updates and input validation.


5. Execution: Compile and execute the program using any standard C compiler (e.g., GCC or Turbo C).




---

TECHNOLOGY USED IN PROJECT:

Programming Language: C

Compiler: GCC (GNU Compiler Collection) or Turbo C

Operating System: Windows / Linux



---

HARDWARE AND SOFTWARE REQUIREMENTS:

Hardware Requirements:

Processor: Intel Core i3 or higher

RAM: Minimum 2 GB

Storage: 100 MB free space


Software Requirements:

Operating System: Windows/Linux/MacOS

Compiler: Code::Blocks / Turbo C / GCC

Text Editor: VS Code / Notepad++ / Dev-C++



---

CODE (With Screenshot):

#include <stdio.h>

int main() {
    int choice;
    float balance = 1000.00; // Initial balance
    float amount;

    while (1) {
        printf("\n===== ATM Menu =====\n");
        printf("1. Check Balance\n");
        printf("2. Deposit Money\n");
        printf("3. Withdraw Money\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Your current balance is ₹%.2f\n", balance);
                break;
            case 2:
                printf("Enter amount to deposit: ₹");
                scanf("%f", &amount);
                if (amount > 0) {
                    balance += amount;
                    printf("₹%.2f deposited successfully.\n", amount);
                } else {
                    printf("Invalid deposit amount.\n");
                }
                break;
            case 3:
                printf("Enter amount to withdraw: ₹");
                scanf("%f", &amount);
                if (amount > 0 && amount <= balance) {
                    balance -= amount;
                    printf("₹%.2f withdrawn successfully.\n", amount);
                } else {
                    printf("Insufficient balance or invalid amount.\n");
                }
                break;
            case 4:
                printf("Thank you for using the ATM. Goodbye!\n");
                return 0;
            default:
                printf("Invalid choice. Please try again.\n");
        }
    }

    return 0;
}


---

OUTPUT (Screenshot Example):

===== ATM Menu =====
1. Check Balance
2. Deposit Money
3. Withdraw Money
4. Exit
Enter your choice: 1
Your current balance is ₹1000.00

===== ATM Menu =====

Enter your choice: 2
Enter amount to deposit: ₹500

₹500.00 deposited successfully.

===== ATM Menu =====

Enter your choice: 3
Enter amount to withdraw: ₹300

₹300.00 withdrawn successfully.

===== ATM Menu =====

Enter your choice: 4

Thank you for using the ATM. Goodbye!


---

CONCLUSION:

This project successfully demonstrates a basic ATM simulation using C programming. It reinforces understanding of loops, switch-case structures, conditional logic, and user input handling. While the project operates in a simplified environment without security or multi-user features, it effectively models real-world banking operations at a logical level.

Future enhancements could include features like PIN authentication, transaction history, multiple account management, and file storage for persistent data.

