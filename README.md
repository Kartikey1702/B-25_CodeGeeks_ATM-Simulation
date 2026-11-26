# K.A.P BANK ATM SIMULATOR

**C Programming Mini Hackathon**

## Team Details

**Batch:** B-25  
**Team Name:** CodeGeeks

### Team Members
1. Kartikey Misra
2. Abdul Samad
3. Priyanshi Gupta

---

## Overview

The **K.A.P Bank ATM Simulator** is a terminal-based banking application developed in C. The system requires PIN authentication before granting access to banking services.

After successful login, the user can perform essential banking operations such as cash withdrawal, cash deposit, balance enquiry, and PIN update through an interactive ASCII-based ATM interface.

---

## Problem Statement

Develop a basic ATM simulation that provides essential banking operations for a single demonstration account.

The program should allow users to check their balance, deposit money, withdraw money, update their PIN, and exit the system while performing appropriate input validation.

---

## Key Features

### PIN Authentication
- Default PIN: `1234`
- Maximum of 3 login attempts.
- Account is locked after three consecutive incorrect PIN attempts.

### Cash Withdrawal
- Allows the user to withdraw money.
- Rejects negative or zero amounts.
- Prevents withdrawal when the requested amount exceeds the available balance.

### Cash Deposit
- Allows money to be deposited into the account.
- Accepts only positive deposit amounts.
- Updates the account balance immediately.

### Balance Enquiry
- Displays the current account balance.
- Balance is displayed up to two decimal places.

### PIN Management
- Allows the user to change the existing PIN.
- The old PIN must be verified before a new PIN is accepted.

### ATM Console Interface
- Menu-driven ASCII interface.
- Provides an ATM-like experience through the terminal.

---

## System Flow

```text
Start Program
     |
     v
Enter PIN
     |
     +---- Incorrect ----> Attempts < 3?
     |                         |
     |                    Yes -> Retry PIN
     |                    No  -> Lock Account -> Exit
     |
   Correct
     |
     v
Display ATM Menu
     |
     +---- [1] Withdraw Money
     |
     +---- [2] Deposit Money
     |
     +---- [3] Balance Enquiry
     |
     +---- [4] Change PIN
     |
     +---- [5] Exit
```

---

## ATM Menu

```text
+==============================================================+
|                                                              |
|                        K.A.P BANK                             |
|                   YOUR TRUST, OUR PROMISE                     |
|                                                              |
+==============================================================+
|                         ATM SERVICES                         |
+--------------------------------------------------------------+
|                                                              |
|                 WELCOME TO K.A.P BANK ATM                    |
|                                                              |
|     +------------------------+  +------------------------+    |
|     | [1] WITHDRAW MONEY     |  | [2] DEPOSIT MONEY     |    |
|     +------------------------+  +------------------------+    |
|                                                              |
|     +------------------------+  +------------------------+    |
|     | [3] BALANCE ENQUIRY    |  | [4] CHANGE PIN        |    |
|     +------------------------+  +------------------------+    |
|                                                              |
|                 +------------------------+                   |
|                 | [5] EXIT               |                   |
|                 +------------------------+                   |
|                                                              |
+--------------------------------------------------------------+
|                     ENTER YOUR CHOICE                        |
+==============================================================+
```

---

## C Programming Concepts Used

- Variables and data types
- Arithmetic and relational operators
- `if-else` conditional statements
- `while` loop
- `do-while` loop
- `switch-case`
- Functions
- Global variables
- User input using `scanf()`
- Formatted output using `printf()`

---

## Function Breakdown

### `WITHDRAW()`

Accepts the withdrawal amount, verifies that it is positive and does not exceed the available balance, and deducts the amount from the balance.

### `DEPOSIT()`

Accepts the deposit amount, checks that it is positive, and adds it to the account balance.

### `UPDATEPIN()`

Verifies the user's existing PIN and allows the PIN to be changed after successful verification.

### `main()`

Controls the overall program, including PIN authentication, the three-attempt security system, ATM menu display, `switch-case` selection, and program termination.

---

## Prerequisites

A standard C compiler such as **GCC (GNU Compiler Collection)** is required.

To verify GCC installation:

```bash
gcc --version
```

---

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/Kartikey1702/B-25_CodeGeeks_ATM-Simulation.git
cd B-25_CodeGeeks_ATM-Simulation
```

### Compile on Windows

```bash
gcc B-25_CodeGeeks_ATM_SIMULATION.c -o atm_simulator.exe
```

### Run on Windows

```bash
.\atm_simulator.exe
```

### Compile on Linux/macOS

```bash
gcc B-25_CodeGeeks_ATM_SIMULATION.c -o atm_simulator
```

### Run on Linux/macOS

```bash
./atm_simulator
```

---

## Sample Test Cases

### Test Case 1 — Correct PIN

**Input:**
```text
1234
```

**Expected Output:**
```text
You are logged in
```

**Actual Output:**
```text
You are logged in
```

### Test Case 2 — Incorrect PIN

**Input:**
```text
0000
```

**Expected Output:**
```text
Incorrect PIN. Try again.
```

**Actual Output:**
```text
Incorrect PIN. Try again.
```

### Test Case 3 — Withdrawal

Initial balance: `50000.00`

**Input:**
```text
120
```

**Expected Output:**
```text
Your current balance is 49880.00
```

**Actual Output:**
```text
Your current balance is 49880.00
```

### Test Case 4 — Deposit

Initial balance: `49880.00`

**Input:**
```text
300
```

**Expected Output:**
```text
Your current balance is 50180.00
```

**Actual Output:**
```text
Your current balance is 50180.00
```

### Test Case 5 — Invalid Withdrawal

If the withdrawal amount exceeds the available balance:

**Expected Output:**
```text
Insufficient balance
```

**Actual Output:**
```text
Insufficient balance
```

---

## Security and Validation

1. Login attempts are limited to three.
2. Zero and negative withdrawal amounts are rejected.
3. Withdrawals exceeding the available balance are rejected.
4. Zero and negative deposit amounts are rejected.
5. The existing PIN must be verified before changing the PIN.

---

## Project Structure

```text
B-25_CodeGeeks_ATM-Simulation/
|
|-- B-25_CodeGeeks_ATM_SIMULATION.c
|-- README.md
|-- ATM_Simulation_Presentation.pptx
|-- .gitignore
```

---

## Future Enhancements

- Multiple user accounts using structures.
- Persistent balance and PIN storage using file handling.
- Mini statement and transaction history.
- Masked PIN entry.
- Improved input validation for non-numeric input.

---

## Conclusion

The K.A.P Bank ATM Simulator demonstrates the practical implementation of fundamental C programming concepts through a simple banking application. The project combines conditional statements, loops, functions, user input validation, and a menu-driven interface to simulate basic ATM operations.