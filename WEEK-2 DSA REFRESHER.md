## ++Day 2 ++

## ++Base case++:

It is defined as the condition in Recursive Function, which tells the function when to stop. If we fail to include this condition it will result in infinite recursions.  
The base case can be included anywhere between the start of the recursive function and the recursive call statement.  
![def printFun(test):](Attachments/11381974-54C4-46FC-A547-975679303BDF.png)

## ++Call stack++:

It is a built-in memory mechanism that manages function execution using the LIFO data structure.  
Working:

- When a function is invoked, the interpreter stops the current execution flow and pushes a new stack frame onto the top of the call stack.
- The interpreter processes the inner function code. If this function calls another function, a new frame is pushed on top of it.
- When the function hits a return statement or finishes running, its frame is instantly popped off the stack.
- Control returns directly to the execution context immediately below it in the stack.  
  ![def first_function ():](Attachments/6F6B6F7B-E0DC-474E-B92D-40A28FCCE973.png)

## ++Recurrence relation++:

It defines a sequence where each term is given as a function of one or more of its preceding terms.  
![an-1, an-2,... an-k](Attachments/2B6154EC-BEEA-4B2D-8155-01CC7CDFD4BA.png)  
++Examples recurrence relations++ -

- **Binary search**: the problem size if halved at each step, and there is a constant time overhead for each division —> ==T(n) = T(n/2) + O(1)==
- **Merge sort**: the problem is divided into 2 halves, each of size n/2, and merging the two halves takes linear time —> ==T(n) = 2T(n/2) + O(n)==

## ++Divide and Conquer++:

It is an effective approach that divides a major problem into smaller, easier subproblems. The solution to the main problem is obtained by combining the final solutions from individually solved subproblems.

### ++Steps++:

1. The first step is to divide the primary problem into smaller sub issues.
2. Each subproblem is tackled separately as soon as it is small enough; recursive use of divide and conquer approach can be utilised to do this.
3. To solve the primary problem, the subproblems’ answers must be merged in the last stage.  
   ++Eg++: merge sort -  
   ![#merge sort](Attachments/27A3C5B0-D57D-414A-A931-4E78A0A38A32.png)

## ++Recursion errors: (‘RecursionError’)++

It occurs when a recursive function makes too many recursive calls without stopping.  
![def endless_recursion():](Attachments/CCD0878C-0890-43AD-8921-C661833E55A3.png)

### ++Causes++:

- Missing base case
- Infinite recursion due to incorrect logic
- Exceeding python’s recursion limit

## ++Factorial++:

![#factorial](Attachments/F2566E17-32A2-4D95-9535-F11D98C7DEC2.png)

## ++Recursive binary search++:

![#binary search using recursion](Attachments/F3A96167-CD7A-4C30-8529-03944C18D80A.png)
