# Banking System Project

## Overview
This project is a simple banking system implemented in C++ that allows users to create and manage bank accounts. It provides functionalities such as creating accounts, depositing and withdrawing money, modifying account details, and deleting accounts. Data persistence is handled using binary file storage.

## Features
- Create a new bank account
- Deposit and withdraw money
- Display account details
- Modify account details
- List all account holders
- Delete an account

## Code Structure
The project consists of:
1. **Class `account`**: Encapsulates account details and operations.
   - Attributes: Account number, Name, Deposit amount, Type (Savings/Current)
   - Methods:
     - `create_account()` - Initializes account details.
     - `show_account()` - Displays account details.
     - `modify()` - Allows modification of account details.
     - `dep(int)` - Deposits an amount into the account.
     - `draw(int)` - Withdraws an amount from the account.
     - `report()` - Prints a formatted account summary.
     - Getters for account number, balance, and type.
2. **File Handling Functions**
   - `write_account()` - Stores account data in a binary file.
   - `display_sp(int)` - Retrieves and displays a specific account.
   - `modify_account(int)` - Updates an account's details in the file.
   - `delete_account(int)` - Deletes an account from the file.
   - `display_all()` - Lists all accounts.
   - `deposit_withdraw(int, int)` - Handles deposits and withdrawals.
3. **Main Function (`main()`)**
   - Implements the user interface for account management.
   - Uses a menu-driven approach for user interaction.

## Programming Concepts Used
1. **Object-Oriented Programming (OOP)**
   - **Encapsulation**: The `account` class encapsulates data and methods.
   - **Abstraction**: Users interact with methods without worrying about internal implementation.
   - **Modularity**: The class structure helps in code organization and reusability.

2. **File Handling**
   - **Binary File Operations**: `write_account()`, `display_sp()`, `modify_account()`, etc., use file I/O for data persistence.
   - **Reading and Writing**: Uses `ifstream` and `ofstream` for handling bank account records.

3. **Data Structures**
   - **Class (`account`)**: Serves as a structured data model.
   - **Sequential File Storage**: Accounts are stored as records in a binary file.

4. **Control Structures**
   - **Loops**: Used for menu iteration and account searching.
   - **Conditional Statements**: `if-else` and `switch` statements drive user actions.

5. **Functions & Methods**
   - **Encapsulated Member Functions**: Methods inside the `account` class handle various account operations.
   - **Standalone Functions**: Global functions manage file operations and user interaction.

6. **Basic Algorithmic Concepts**
   - **CRUD Operations**: The system follows Create, Read, Update, and Delete operations for accounts.
   - **Linear Search**: Used for finding accounts in a file.
   - **Transaction Processing**: Handles deposits and withdrawals with file updates.

7. **Complexity Analysis**
   - **Time Complexity Consideration**: Analyzed for each operation in the project.
   - **Space Complexity Consideration**: Efficient storage by using binary files.

## Algorithm
1. **Account Creation**
   - Input account details.
   - Store data in a binary file.
2. **Deposit/Withdraw**
   - Retrieve the account from the file.
   - Modify balance based on transaction type.
   - Update record in the file.
3. **Account Display & Modification**
   - Read account data from file.
   - Modify details if needed and update.
4. **Account Deletion**
   - Copy all records except the target account to a temporary file.
   - Replace the original file with the temporary file.

## Time and Space Complexity
| Operation             | Time Complexity | Space Complexity |
|-----------------------|----------------|-----------------|
| Create Account       | O(1)            | O(1)            |
| Display Account      | O(n)            | O(1)            |
| Modify Account      | O(n)            | O(1)            |
| Deposit/Withdraw     | O(n)            | O(1)            |
| Delete Account       | O(n)            | O(1)            |
| Display All Accounts | O(n)            | O(1)            |

## Future Improvements
- **Relational Database Integration**: Replace file storage with MySQL or PostgreSQL for better scalability and efficiency.
- **User Authentication**: Implement a secure login system.
- **Graphical User Interface (GUI)**: Develop a user-friendly interface using Qt or Tkinter.
- **Multithreading**: Improve performance by handling file operations in parallel.
- **Transaction History**: Maintain a log of all transactions.
- **REST API Integration**: Expose functionalities via a web API for real-world banking applications.

## Real-World Applications
This project serves as a foundation for banking software, financial applications, and account management systems in enterprises. With database integration and security enhancements, it can be scaled into a real-world banking system.

---
**Author: Aditya Pratap Deshmukh**

