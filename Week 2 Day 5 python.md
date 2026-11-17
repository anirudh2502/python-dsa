# Week 2 Day 5 python  
  
## ++Day 5++  
  
## ++Automated testing++:  
It is a technique where tester writes scripts independently and uses suitable software or automation tools to test the software.   
### ++Objectives++ -   
- They are used to automate the testing tasks that are difficult to perform manually   
- It can be run at any time of the day using scripted sequences to examine the software   
- The goal of automation is to reduce test cases to be executed manually, but not eliminating manual testing  
### ++Advantages of automated testing++ -   
* Improves the coverage of testing as automated execution of test cases is faster than manual execution  
* It reduces the dependency of testing on the availability of testing engineers   
* It provides round-the-clock coverage as automated tests can be run at all times  
* Automated testing takes far fewer resources in execution as compared to manual testing  
* It acts as a test data generator and produces maximum test data to cover a large number of inputs and expected outputs for result comparison  
  
  
  
## ++Unit testing++:   
It is a software testing technique used to verify individual units of source code. It ensures that each unit behaves as expected according to its requirements.   
- Focuses on testing small, independent components of an application to verify their functionality   
- Provides quick feedback by identifying errors in individual units during development  
***Example: ****In banking applications, unit testing is used to verify interest calculations, loan eligibility rules, and transaction validation logic.*  
### ++Characteristics++:  
* Tests individual units with minimal dependency on external systems  
* Produces consistent results when executed with the same controlled inputs and conditions  
* Executes quickly, allowing developers to run tests frequently during development   
* Can be executed repeatedly without affecting the results   
* Uses automated testing frameworks to execute tests with minimal effort  
### ++Unit testing workflow++ -   
1. Identify unit  
2. Define expected behaviour   
3. Create test cases   
4. Prepare test setup   
5. Execute tests   
6. Analyse results   
7. Fix defects   
8. Re-test  
9. CI/CD integration  
### ++Components of a unit test++:  
- **Test setup** —> prepares the environment and resources required before executing a unit test  
- **Test input** —> provides the value/condition used to evaluate the behaviour of a unit  
- **Test execution** —> involves running the selected function/method with the prepared inputs   
- **Assertion** —> it verifies whether the actual result matches the expected outcome  
  
  
  
## ++Test cases and assertions++:   
The ‘**unittest**’ framework is built into the standard library for unit testing. This module is used because -   
- No set-up needed as it comes pre-installed in python  
- Supports test cases, assertions, and test suites  
- Reliable for projects of any size, with easy integration into other tools  
‘***Unittest***’ framework allows developers to verify that functions produce the expected results. A test case is created by inheriting from ‘unittest’.   
  
‘***assertln()***’ is a ‘unittest’ library function that is used in unit testing to check whether a string is contained in other or not.  
This function will take three strings parameters as input and return a boolean value depending upon the assert condition. If the key is contained in container string it’ll return true, else false.   
![# test suite](Attachments/44A52D21-F801-4919-9C8D-153CDDF019B8.png)  
  
  
  
## ++Pytest++:  
It is an open-source testing framework. It automatically discovers and runs test functions written in specific format.   
- It is mainly used to write API test cases / API testing  
- Helps write better programs   
![definina a function with parameter >](Attachments/FE1EA243-070E-48C9-8C79-CCE102C2B0C0.png)  
### ++Advantages of Pytest++:   
* It can run multiple test cases in parallel, thus reducing the execution time of test suite  
* It has its own way of detecting test files and functions automatically, if not mentioned explicitly  
* It is free and open-source  
* Allows to skip a subset of tests during execution  
  
  
  
## ++Pytest fixtures++:   
They are a powerful feature that allow to set-up and tear down resources needed for the tests. They help in creating reusable and maintainable test code.  
A fixture is a piece of code that runs and returns output before the execution of each test.   
![Syntax:](Attachments/5708CC9A-953A-4E80-B01A-9C83FE87E88F.png)  
*The fixtures help the user to use certain part of the code just by declaring and reading it once. *  
  
  
  
## ++Edge-case testing++:   
It verifies how code behaves at extreme operating boundaries or unexpected inputs.   
Common edge cases to test -   
- Empty/null inputs  
- Boundary values   
- Invalid data types   
- Domain specific constraints  
  
  
  
## ++Debugging using ‘breakpoint()’ :++  
Debugging using ‘**breakpoint()**’ and **pdb module** requires a set of *commands* that needs to be followed. They are as follows -   
—> **c**: continue execution  
—> **q**: quit execution  
—> **n**: step to next line within same function  
—> **s**: step to next line in called function  
**++Breakpoints++** - it is a designated point in the source code where we instruct a debugging tool/IDE to pause program execution. They are used to stop the execution of the code at a specific line or function call. When the program reaches a breakpoint, it enters a debugging mode, allowing to inspect variables, step through code, and diagnose issues.   
- Developers set breakpoints at critical points in the code where they suspect there may be a problem.  
- They are particularly useful for identifying the cause of bugs and understanding execution flow.   
  
  
  
## ++Logging++:  
It is the process of keeping records of what a program is doing while it runs.   
- Helps developers understand program behaviour and easily find and fix errors  
![import logging](Attachments/3839DBED-F94F-46E1-9AE5-4C0F2A7E53DA.png)  
++Steps++:   
1. Import the logging module   
2. Create and configure logger  
3. Choose the file mode   
4. Set the log level   
5. Create logger object  
### ++Python logging levels++ -   
- **Debug**: detailed info for diagnosing problems   
- **Info**: confirms things are working as expected   
- **Warning**: indicates unexpected issues/potential future problems  
- **Error**: a serious problem that prevents a function from running  
- **Critical**: a severe error that may stop the program from running  
  
  
  
## ++Logging v/s printing:++  

| Logging  | Printing  |
| ------------------------------------------------------------------------- | --------------------------------------------------------------- |
| Records events and errors that occur during the execution of the programs | Displays the info to the console for the debugging purposes |
| Mainly used in production environment | Mainly for debugging |
| Features: log levels, filtering, formatting, etc | There are no good features  |
| Log levels: debug, info, error, warning, critical | Doesn’t have any levels; simply prints whatever is passed to it |
| Can be configured to log to different output destinations | Prints only on the console |
  
  
  
  
## ++Mocking++: it is a powerful technique in software testing that involves the creation of imitated versions of real objects, “test doubles”, to fake their behaviour in a controlled environment.   
- It allows for a condition, using mocks, under which it is being tested to be controlled and makes possible the testing of how a component would react to edge cases and failures without unpredictability of real-world factors  
- Also provides a way for developers to trace interactions between components and making sure they are communicating as expected and handling data correctly  
  
### ++Mocks++ -   
* They are objects pre-programmed with expectations of their usage.   
* They check that certain interactions have taken place during running of the tests.  
* Useful for testing the behaviour of components which interact with external services or other parts a system.  
  
### ++Stubs++ -   
* They are implementations that answer specific calls with fixed responses.  
* Contrary to mocks, they don’t care about interactions; they just ensure continuation of a test with prepared data.   
* Useful when we wanna isolate a component that feeds the unit under test.  
  
### ++Fakes++:  
* More complex varieties of test doubles that have working implementations, but represent simpler versions of components involved.  
* Makes tests run more quickly and avoid external dependency.  
* Used when some component’s behaviour is too complex to be easily mocked/stubbed, but full implementation of test is not needed.  
  
### ++Spies++:  
* They are much like mocks; sharpen focus on logging interactions.   
* After the test, we can inspect the spy to ensure the interactions have happened as expected.  
* Unlike mocks, they don’t fail the test if the interactions are not what was expected; they just let the test continue and provide data to assertions.   
