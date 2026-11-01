## ++Day 2++

## ++Errors and exceptions++:

- Errors are problems in a program that causes the program to stop its execution.
- Exceptions are raised when some internal events change the program’s normal flow.

### ++Types of errors:++

- Syntax error
- Indentation error
- Logical error

| Syntax error                                                   | Exception                                                                   |
| -------------------------------------------------------------- | --------------------------------------------------------------------------- |
| Detected during compile time                                   | Detected during runtime                                                     |
| Caused due to violation of structural/grammatical python rules | Caused when a syntactically correct code encounters an impossible operation |
| Can’t be caught/handles using ‘try-except’ block               | Can be caught using the ‘try-except’ block                                  |
| The program terminates immediately; no code runs               | The normal flow changes, but the program can recover if handled             |
| Eg: missing colons, unmatched parentheses, wrong indentation   | Eg: ZeroDivisionError, ValueError, etc.                                     |

## ++Built-in exceptions++:

Python provides a set of built-in exceptions, each designed to signal a specific type of error and helps to debug more effectively.

| Exception           | Description                                                                                |
| ------------------- | ------------------------------------------------------------------------------------------ |
| TypeError           | Raised when an operation/function is applied to an object of inappropriate type.           |
| ValueError          | Raised when a function receives an argument of the correct type but with an invalid value. |
| ImportError         | Raised when there is a problem with the import statement.                                  |
| ModuleNotFoundError | Raised when a module can’t be found.                                                       |
| FileNotFoundError   | Raised when a file/directory is requested and can’t be found.                              |
| RuntimeError        | Raised when an error occurs that doesn’t fall under other categories.                      |
| SyntaxError         | Raised when there is an error in the syntax.                                               |
| IndentationError    | Raised when the indentation is not right in the code.                                      |

## ++Exception handling++:

It allows a program to handle unexpected errors during execution in a controlled way instead of crashing abruptly. It enables the program to detect errors, manage them properly and continue execution wherever possible.

- It handles runtime errors such as invalid input, file not found, division by zero, etc that occur during execution
- Helps improve program reliability by ensuring the app doesn’t terminate unexpectedly when an error occurs  
  ++Syntax++:  
  ![except SomeException:](Attachments/18C3E9C1-3F9E-4581-8F3A-8E9AA60ED906.png)

* **Try** - runs the risky code that might cause an error
* **Except** - catches and handles the error if one occurs
* **Else** - executes only if no exception occurs in try block
* **Finally** - runs regardless of what happens  
  ![res = 100 / n](Attachments/18364FA0-A8F8-4D26-BB5A-961851550F00.png)

## ++Raising exceptions++:

The “**raise**” keyword raises an exception and immediately stops the normal execution of the program. The control is then transferred to the nearest matching except block, otherwise the program terminates.  
++Syntax++:  
![raise Exception("user text")](Attachments/D9D9C16B-A33E-4EC1-957F-26BCCB647F55.png)  
![a % 2 != 0:](Attachments/A23377EE-F244-43E3-9CF2-1B2E3D3CA876.png)  
++Advantages++:

- Helps in stopping execution when an invalid condition occurs
- Allows custom error messages for better debugging
- Useful for input validation
- Enables manual raising of exceptions when needed

## ++Exception chaining++:

To chain exceptions, use the “**raise-from**” statement instead of just “raise” statement. This gives info about both the errors.  
![def example():](Attachments/6E19CD18-73F3-42CF-838D-8680D3AEDFF8.png)

## ++Assertions++:

They are debugging tools used to test if certain conditions remain true during program execution. “**Assert**” keyword is used to check.  
If the condition evaluated by the ‘assert’ statement is true, the code runs without interruption, else ‘_AssertionError_’ is raised immediately and program is terminated.  
![username = "David"](Attachments/54B5DD06-82E4-4B03-AC64-BCD658BF3135.png)

## ++Defensive programming++:

It is a software development approach that focuses on protecting the integrity of a program by anticipating and handling possible errors and exceptions.  
There are several techniques you can use to implement defensive programming -

- Use “**try-catch**”
- Check function arguments
- Use “**stopifnot**”
- Use “**assert that**”  
  **++Objectives of defensive programming++**:

* To prevent errors and exceptions
* To improve reliability of code
* To save time and effort in debugging
* To improve maintainability of code  
  **++Possible threats++**:
* Syntax errors
* Runtime errors
* Exceptions
* Data integrity issues  
  **++Common errors in defensive programming++**:

- Using wrong error-handling function
- Forgetting to include error-handling code
- Overusing error-handling functions
- Not testing the error-handling code  
  **++Principles of defensive programming++**:

1. Anticipate and handle errors and exceptions
2. Check function arguments
3. Use error-handling functions
4. Test error-handling code
5. Keep the code simple and maintainable

——————————————————————————————————————
