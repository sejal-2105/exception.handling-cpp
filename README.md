# exception.handling-cpp

### **Experiment 1: Exception Handling for Division by Zero**

**Aim:** To demonstrate the use of **exception handling** to gracefully manage the runtime error of **division by zero**.

**Theory:** **Exception Handling** is a mechanism in C++ that allows a program to deal with runtime errors, called **exceptions**, in a structured way.
* The code that might cause an error is placed inside a **`try`** block.
* If the condition for the error (the denominator `n2` being zero) is met, an exception is explicitly generated using the **`throw`** keyword. In this case, the value of the divisor (`n2`, a `float`) is thrown.
* The **`catch`** block immediately following the `try` block receives the thrown exception (`float num`), allowing the program to execute an error-handling routine instead of crashing.

**Algorithm:**
1.  **Input:** Declare two `float` variables, `n1` and `n2`, and prompt the user to enter their values.
2.  **`try` Block:** Begin a `try` block to monitor for exceptions.
3.  **Check Condition:** Inside the `try` block, check if the divisor `n2` is equal to $0$.
4.  **`throw`:** If `n2` is $0$, use `throw n2` to generate an exception.
5.  **Normal Execution:** If `n2` is not $0$, perform the division, store the result in `ans`, and print the "Answer".
6.  **`catch` Block:** Define a `catch` block that specifically catches a `float` type exception (i.e., `catch(float num)`).
7.  **Error Output:** If an exception is caught, print an "ERROR" message indicating "division by 0".

***

### **Experiment 2: Exception Handling for Underage Input**

**Aim:** To demonstrate the use of **exception handling** to enforce a custom program constraint, specifically checking if an entered age is below the minimum required age of $18$.

**Theory:** Exception handling isn't limited to built-in runtime errors; it can be used to manage **application-specific exceptions** that violate program rules.
* The **`try`** block contains the code that checks the validity of the input age (`n1`).
* If the input is less than $18$, the program uses **`throw n1`** to signal an exception. In this case, the invalid age (an `int`) is thrown.
* The **`catch`** block receives the thrown `int` exception (`catch(int a)`) and handles the policy violation by printing a user-friendly error message.

**Algorithm:**
1.  **Input:** Declare an integer variable `n1` and prompt the user to "Enter age of person".
2.  **`try` Block:** Begin a `try` block to monitor the input validity.
3.  **Check Constraint:** Inside the `try` block, check if the age `n1` is less than $18$.
4.  **`throw`:** If `n1` is less than $18$, use `throw n1` to generate an exception.
5.  **Normal Execution:** If the age is $18$ or older, print the approved age and the message "APPROVED".
6.  **`catch` Block:** Define a `catch` block that specifically catches an `int` type exception (i.e., `catch(int a)`).
7.  **Error Output:** If an exception is caught, print an "ERROR" message indicating the person is "UNDERAGE" and displaying the invalid age.

***

### **Conclusion**

These experiments effectively demonstrate **exception handling** as a mechanism for managing both mathematical errors (division by zero) and custom, application-specific constraints (age validation). By using the `try-throw-catch` structure, the programs prevent abnormal termination and provide controlled, meaningful feedback to the user when an error or policy violation occurs.
