# Week 2  
  
## ++Day 4++  
  
## ++Type hints++:   
They are features that allow developers to annotate their code with expected types for variables and function arguments.   
- Helps to improve code readability   
- Provides opportunity to catch errors before runtime  
![age: int = 25](Attachments/6C95E412-B410-4FB7-9243-28C2A4BF9F91.png)  
  
  
  
## ++Parameters++:  
They are values passed to a function/method to provide input. They allow the method to use different data each time it is called.  
* **Self-parameter** - it is a reference to the current instance of the class. It is used to access the object’s attributes and other methods from within instance methods.   
![class Person:](Attachments/D559C3DE-2405-4766-BF89-444DCA4D745C.png)  
  
  
  
## ++list, dict, set, and tuple annotations++:  
Type annotations allows to declare the data type that should live inside the collection.   
1. **List(type) **- Annotates a list where every element is of the specified type  
++Example++ —> names: list[str] = ["Alice", "Bob"]  
  
2. **dict[key_type, value_type]** - Annotates key-value pairs  
++Example++ —> ages: dict[str, int] = {"Alice": 25}  
  
3. **set[type]** - Annotates a set of unique elements  
++Example++ —> unique_ids: set[int] = {101, 102}  
  
4. **Tuple** - Can be strict/fixed-size  
++Example++ —> person: tuple[str, int] = ("Alice", 25)  
  
  
  
## ++union():++  
This method returns a new set containing all unique elements from two or more sets. It combines the given sets and automatically removes duplicate values.   
(The original sets remain unchanged.)  
![= {1, 2, 3}](Attachments/7B26C817-3B77-4B02-8E3A-AF217D980747.png)  
![print(a](Attachments/30E2C592-FBA5-4BB1-ABEB-21C833B1B825.png)  
  
  
  
## ++Type aliases++:  
It allows us to create reusable names for existing types, making complex data type definitions easier to read and maintain.   
- Create reusable names for existing types  
- Improve code readability and maintainability  
![type Value = number | string | boolean;](Attachments/26953421-3CE1-4770-B4FA-B13C557309AD.png)  
  
  
  
## ++TypedDict++:  
It enables developers to specify the structure of dictionaries, enforcing both the keys and their associated types.   
- It helps in ensuring that dictionary-like data structures conform to expected types.   
- These also help to specify whether  certain fields in a TypedDict are mandatory or optional.  
![from typing_extensions import NotRequired](Attachments/D2ADB772-32D7-4A1C-BCA2-0AF4C26811DD.png)  
  
  
  
## ++Protocol and structural sub-typing++:  
Protocols allows for structural sub-typing , which means that a class can be considered a subtype of a protocol if it implements the required methods, regardless of whether it explicitly inherits from the protocol.   
![from typing_extensions import Protocol](Attachments/4FB88FB9-06AF-4EB8-BD34-95917F4981BE.png)  
  
  
  
## ++Dataclasses++:  
This module helps define classes that mainly store data.   
It can automatically generate methods such as __init__(), __repr__(), __eq__(), thus reducing the code required for data-oriented classes.    
- Without a data class we may need to manually define the constructor, representation method, and equality method  
- With data classes, these methods are automatically generated.    
### ++Creating a dataclass++:  
![*suatya 2s, etn](Attachments/288B0F60-FC20-4DBE-925B-407C2DB27486.png)  
The **data classes** are implemented by using **decorators** with classes. Attributes are declared using ***type hints*** , essentially specifying data type for variables.   
  
  
  
Naming conventions:  
It refers to rules and guidelines for naming variables, functions, classes and other entities in the code.   
- Ensures consistency   
- Readability   
  
* **Modules** - when naming a module, use lowercase letters and underscores, making it descriptive.  
  
* **Variables** -   
- ++Global variables++: should be in uppercase with underscores separating words  
- ++Local variables++: same convention as functions  
  
* **Classes** - names should follow the ‘CapWords’ or ‘CamelCase’ convention, meaning first letter of each word in the classname should be capitalised and there are no underscores between words.  
  
### ++Importance of naming conventions++:  
- Clear names make code easier to understand  
- A consistent style makes code easier to update, debug and extend  
- A shared naming style keeps a team’s codebase cohesive  
- Descriptive names reduce misunderstandings and misuse  
  
  
  
## ++PEP-8 - python coding style++:  
It is the official *python style guide* that promotes readable and consistent coding.  
—>It ensures code is easy to understand and maintain  
* **Indentation**: it organises code into blocks and defines program structure  
* **Docstrings**: use it to describe functions/modules.  
* **Comments**: use it to explain code for better readability  
* **Trailing commas**: use them in data structures like tuples, lists, etc to improve readability and simplify adding new elements   
* **Encodings**: use standard encodings like UTF-8/ASCII for python files to ensure compatibility  
* **Spaces around operators**: use space around operators and after commas for readability  
* **Naming conventions**: follow consistent naming conventions (CamelCase)   
  
  
  
## ++Static analysis++:   
It involves a set of methods used to analyse software source code, to determine how the software functions and establish criteria to check its correctness.   
- Static analysis studies the source code without executing it and reveals a wide variety of info such as the model structure, data and control flow, syntax accuracy, etc.    
### ++Types of methods++:   
1. **Control analysis**: examines how control flows through the program; calling structure, order of control transfers and state changes.  
2. **Data analysis**: checks that data is defined and used correctly   
3. **Fault/failure analysis**: finds the conditions that cause incorrect components (faults) or incorrect behaviour (failures).  
4. **Interface analysis**: verifies that sub-model and user interfaces are accurate, error-resistant and well integrated.   
