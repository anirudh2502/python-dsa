# Week 2 Day 6 Python   
  
## Day 6   
  
## ++Datetime++:  
This module provides classes and methods for working with dates, times, time intervals and tome zones.   
Useful for tasks such as -  
- scheduling,   
- logging events,   
- calculating date differences,   
- formatting dates,   
- handling time-based data  
++Install++ - ***from datetime import datetime***  
++Syntax++ - ***class datetime.date(year, month, day)***  
![from datetime import date](Attachments/1CC0CDF0-38E9-4827-BBFD-CBBD9CCDAB6A.png)  

| Method  | Description |
| ------------ | ------------------------------------------------------------------------------------------------ |
| today() | Returns the current local date                                   |
| isoformat() | Converts a date into YYYY-MM-DD format                                                           |
| strftime() | Formats a date according to a specific format  |
| isoweekday() | Returns the weekday as an integer from 1-7 |
  
  
  
  
## ++Datetime.timedelta()++:  
This function is used to represent a time difference. It allows to add or subtract days, hours, minutes from a date/datetime object.  
![from datetime import datetime, timedelta](Attachments/1D64437D-19C0-4AE6-87B7-E18969AD7839.png)  
****This code gets the current date and time using datetime.now() and then uses timedelta(days=1) to calculate the date and time one day in the future***  
++Syntax++-  
![datetime.timedelta(days=0, seconds=0, minutes=0, hours=0, weeks=0)](Attachments/D0DD3F62-9255-4AC0-96EE-265543620C63.png)  
  
  
  
## ++Pathlib++:  
This module provides an object-oriented way to work with filesystem paths. It represents paths as objects, making operations like path joining, file reading/writing, etc much cleaner and cross platform.   
‘**Path**’ class in pathlib is the main class used to represent and interact with file and directory paths on the actual filesystem.   
++Need for this module++ -   
- Same code works on Windows, Linux and macOS  
- Avoids manual string concatenation by offering methods and operator overloading (/)  
![from pathlib import Path](Attachments/AC242DED-069B-4A0D-916C-B352ED5F9443.png)  
### ++Methods in path class ++-   
1. **cwd()** —> returns a new path object which represents current working directory  
2. **exists()** —> checks whether specified path exists on the disk. If yes then returns True, otherwise False  
3. **is_dir()** —> used to determine if path points to a directory. Returns true if path is a directory, else false  
  
  
  
## ++Working with JSON data++:  
JSON is a text format used to store data in key-value pairs, similar to dictionaries.   
- The built-in ‘**json**’ **module** helps convert python objects into JSON strings and vice versa   
- ‘**dumps()**’ helps convert dictionary into JSON format.    
![import json](Attachments/5EC9B636-92BF-4E96-A15F-01A8ECA4AA9A.png)  
### ++Encoding++:  
Transforms python data into JSON   
- Also known as ***serialisation***   
### ++Decoding++: Converts JSON data back into usable python objects  
- Also known as ***deserialisation***   
*Built-in ‘json’ module supports both operations.*  

| Python object  | JSON object |
| -------------- | ----------- |
| Dict           | Object      |
| List. Tuple    | Array       |
| Str            | String      |
| Int, float     | Numbers     |
| True           | True        |
| False          | False       |
| None           | null        |
  
  
  
  
## ++Working with CSV files++:  
A CSV (Comma Separated Values) file is a plain text file where each line represents a data record, and fields within each record are separated by commas.   
- Commonly used for spreadsheets and databases   
- Known for its simplicity and readability   
### ++Reading a CSV file++:   
The ‘***csv.reader*’ *class*** reads data in a structured format.  
- The first step is *opening* the CSV file using ‘*open()*’ function in *read mode (‘r’)*  
- Then ‘**csv.reader()**’ function reads the file, returning an iterable reader object  
### ++Writing to a CSV file++:   
The ‘***csv.writer’ class*** allows to write data to a CSV file.   
- It converts user data into delimited strings before writing them to a file  
—> Writing a single row - ***writerow(fields)***  
—> Writing multiple rows - ***writerows(rows)***  
  
  
  
## ++Collections++:  
This module provides specialised containers, which are designed to address specific programming needs efficiently and offer additional functionalities.  
* Provides specialised container data types beyond built-in data types like list, dict and tuple  
* Includes efficient alternatives such as deque, Counter, OrderedDict, defaultdict, and namedtuple  
* Simplifies complex data structurehandling with cleaner and faster implementations  
* Helps in frequency counting, queue operations and structured records with minimal code    
  
  
  
## ++Itertools++:  
It is a module that provides various functions that work on iterators to produce complex iterators.   
++Different types of iterators provided by this module++ -   
1. Infinite iterators   
2. Combinatoric iterators  
3. Terminating iterators   
  
  
  
## ++Functools++:  
This module offers a collection of tools that simplify working with functions and called objects, that includes utilities to modify, extend or optimise functions without rewriting their core logic, helping to write cleaner and more efficient code.   
* Provides higher-order functions and decorators that simplify programming tasks   
* Offers tools like partial() to fix certain arguments of a function  
* Includes decorators to reduce boilerplate when implementing rich comparisons  
* Helps with cleaner, more efficient and reusable code, with minimal redundancy  
### ++Functions in this module++ -   
1. ‘**partial’ class** —> fixes certain arguments of a function and creates a new function with fewer parameters  
2. ‘**partialmethod’ class**  —> works like partial, but for class methods  
3. **cmp_to_key** —> converts a comparison function into a key function   
4. **reduce** —> it applies a function of two arguments repeatedly on the elements of a sequence so as to reduce the sequence to a single value  
5. **update_wrapper** —> updates a wrapper function to copy attributes from the wrapped function  
6. **lru_cache** —> caches recent function results to speed up repeated calls with the same arguments, improving performance at the cost of memory  
  
  
  
## ++Enums++:   
They are used to define a set of named constant values. They make code cleaner, more readable and prevent using invalid values. Each member of Enum has a name and value.   
- Enums can be easily accessed, compared, or used in loops and dictionaries   
- Help in assigning meaningful names to integer values to improve code readability   
- Useful when having a small set of possible values for an item (directions, days of week, etc.)  
—> Enums are created by defining a class that inherits from the ‘**enum**’ class.   
* Each attribute inside the class represents a unique, named constant with a specific value  
* These members can be easily accessed using their name/value   
![import Enum](Attachments/1DDC346A-D527-47FB-87CD-C871B53AAA98.png)  
  
  
  
## ++UUID++:  
It is 128 bits in total, and provides the uniqueness as it generates IDs on the basis of time, computer hardware.   
Advantages of UUID:  
- Can be used as general utility to generate unique random id  
- Can be used in cryptography and hashing applications   
- Useful in generating random documents, addresses, etc  

| Function  | Generation method  | Used for  |
| ------------ | ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| uuid.uuid4() | Completely random values  | General use, primary keys and session tokens where privacy matters                                                        |
| uuid.uuid1() | Current timestamp + computer’s MAC address | Systems needing time-based tracking (exposes hardware MAC address) |
  
  
  
  
## ++Argparse++:  
The **‘argparse’ module** helps create a program in a command-line-environment in a way that appears not only easy to code, but also improves interaction.   
- It also automatically generates help and usage messages   
- Issues errors when users give the program invalid arguments  
### ++Steps for using ‘argparse++’ -   
1. Create a parser  
2. Adding arguments   
3. Parsing arguments   
### ++Applications of argparse module++ -   
* Find the sum of command-line arguments   
* Program to arrange the integer inputs in ascending order   
* To find the average of the entered command line numerical arguments  
  
  
  
## ++Timeit++:  
The ***‘timeit’ module*** accurately measures the execution time of small code snippets, offering more consistent results than ‘time.timer()’ .  
It is ideal for comparing code performance, benchmarking and optimisation and can be used via the command line.   
![import timeit](Attachments/1F0E92B2-5D2F-4958-B757-7B7183C53012.png)  
++Syntax++ -   
![timeit.timeit(stmt, setup, timer, number)](Attachments/E517C879-383C-4729-98B9-DA0B4AA056BA.png)  
—> **stmt**: the code to be timed (as a string)  
—> **setup**: setup code that runs before timing (as a string) —> **timer**: timer function  
—> **number**: no of times to execute stmt  
  
  
  
## ++Thread++:  
It is the smallest unit of execution within a process. It enables a program to perform multiple tasks concurrently while sharing the same memory and resources. They improve app performance and responsiveness in multitasking environments.   
### ++Properties++ -   
* Each thread has its own Thread ID (TID) for identification  
* A thread moves through states such as new, runnable, running, waiting, terminated   
* Threads within the same process share memory and resources, enabling faster communication  
* Context switching can occur between threads to allow multiple tasks to execute efficiently.  
  
  
  
## ++Process++:   
It is the program that is currently in execution within an OS. It operates in an independent environment and is managed by the OS for proper scheduling and execution. They form the basis of program execution in multitasking system.   
### ++Properties++ -   
* Each process has a unique Process ID (PID) for identification  
* Every process moves through different states such as new, ready, running, waiting, terminated   
* Processes communicate with each other using Inter-Process Communication (IPC) methods  
