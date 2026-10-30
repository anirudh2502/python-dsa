# WEEK-2 Python Refresher  
  
## ++Day 1 ++  
  
## ++Importing modules++:   
In python, modules allow to import and use functions, classes and variables from other scripts. The “***import***” statement is the most common way to bring external functionality into the python program.   
### ++Importing built-in modules++:   
They can be imported directly using “***import***” keyword without any installation. This allows access to all functions and variables defined in the module.   
![import math](Attachments/3E76C7C3-768F-4FF4-A899-FF77178573A5.png)  
### ++Importing external modules++:   
To use external modules, we need to install them first, which can be done using “**pip**” command in the terminal (***pip install module_name****)*  
![# Create a simple DataFrame](Attachments/197F34ED-873D-4107-987C-A4508298A171.png)  
### ++Importing specific functions++:   
Instead of importing entire module, only the functions and variables needed can be imported using “***from***” keyword.   
![from math](Attachments/BCC0D4BA-1833-4A63-B1BD-5275338D7B60.png)  
  
  
  
## ++Standard library versus third-party packages++:   

| Aspect | Standard library | Third-party packages |
| ------------ | --------------------------------- | ---------------------------------------- |
| Installation | Nothing to install  | Install with “pip” |
| Reliability  | Very stable, rarely breaks  | Can change or stop being maintained |
| Safety  | Trusted built-in | Must trust outside code  |
| Features  | Covers the basics | Covers specialised areas (data, web, AI) |
| Used for | Small scripts, shared libraries,  | Bigger apps, special tasks |
  
  
  
  
## ++Creating and importing modules++:   
A module is a simple python file with ‘**.py**’ extension that can be imported inside another python program. The name of the python file becomes the module name.   
![' GFG.py '''](Attachments/5214DAAD-4E61-4B83-8F13-4F9B5BB88612.png)  
![import GFG](Attachments/F1563CCB-DCD3-4821-9A9D-3E900A174903.png)  
  
  
  
## ++Organising code into packages++:   
Python packages are a way to organise and structure code by grouping related modules into directories.   
**++Components++**:   
- ++Module++: a single python file containing reusable code  
- ++Package++: directory containing modules special “**__init__.py**” file  
- ++Sub-packages++: packages nested within other packages  
### ++Creating and accessing packages++:   
1. Create a directory (folder that acts as a package)  
2. Add modules (python files)  
3. Add ‘***__init__.py***’ to the directory  
4. Create sub-packages (optional)  
5. Import modules   
### ++Uses of packages++:   
- Organised code structure   
- Easy code reuse   
- Simplifies sharing and distribution (pip)  
- Makes large projects manageable  
  
  
  
## ++__name__ == “__main__” :++  
‘***__name__***’ is a special variable set by the interpreter.   
* If a python file is run directly, Python sets _name__ to “__main__”  
* If the same file is imported into another file, __name__ is set to module’s name  
![print("Always executed")](Attachments/C0046331-619A-4C5D-A3A2-96F5455BFC84.png)  
![import script](Attachments/7E99FCAB-F95E-4BFA-9618-20EBF0CED022.png)  
  
  
  
## ++Module search paths and import behaviour++:  
By default, Python only searches the current working directory and standard library paths for modules. If a module stored in another folder is tried to be imported, Python will raise an error.   
### ++Using ‘sys’ path++:  
Folder path can be manually added to Python’s search path using ***sys*** module.   
![add (a,](Attachments/743C1AFC-4453-447A-93E1-037DA1D4A965.png)  
![# main.py](Attachments/E01CD729-6874-4CAE-9239-D6A3BDFEDB64.png)  
### ++Import using packages (for larger projects)++:  
For larger projects, the best way to organise code is by making folders into packages.   
![project/](Attachments/9FDE8DB9-0574-4708-BA4E-108121715740.png)  
  
  
  
## ++Installing packages with “pip”++:  
Python PIP is the package manager used to install, update and manage python packages and libraries. It allows users to easily download packages from Python Package Index (PyPI) directly through the command line.   
- PIP is commonly used to add external libraries that are not included with Python by default.   
PIP provides the install command to download and install python packages.   
![pip install package_name](Attachments/E301F2FA-064C-4137-BCEF-0823823B6DCC.png)  
### ++Install specific package version++:   
It can be done using the ‘**==**‘ operator with the package name.   
![pip install package_namereversion](Attachments/525AEE5D-ED1C-41A1-A52C-81AE58FA92A2.png)  
### ++Listing installed packages++:   
The “***pip list***” command is used here.   
![pip list](Attachments/141A7466-8436-4274-A347-1A1898259F38.png)  
  
  
  
## ++Virtual environments++:   
It is an isolated environment that allows to manage dependencies for projects separately. It prevents conflicts between projects and avoids affecting the system-wide python installation.   
- Tools like “**venv**” or “**virtualenv**” are used to create them.    
### ++Need for virtual environment++:   
- Avoid dependency conflicts   
- Isolate project environments  
- Simplifies project management   
- Prevents system interference   
By default, all python projects share the same location to store packages. This can cause problems if two projects need different versions of the same package. A virtual environment should be used for every python project. It creates a separate space for each project’s packages, so they don’t interfere with each other.   
![Step 1: Installing virtualenv](Attachments/330F5469-C97A-4BB0-B2A6-1A1790B86972.png)  
  
  
  
## ++Dependency management++:  
Managing dependencies ensures smooth development and deployment processes.   
1. Managing dependencies using ‘**pip**’  
2. Managing using ‘**virtualenv**’  
3. Managing using ‘**Pipenv**’  
### ++Best practices for managing dependencies++:  
* Use virtual environments   
* Use ‘requirements.txt’ file  
* Use dependency management tools  
- Pipenv  
- Poetry  
* Using version ranges carefully   
* Regularly update dependencies   
* Use ‘**.gitignore**’ to avoid committing virtual environments  
* Automating dependency management with CI/CD  
* Documenting dependency practices  
  
  
  
## ++Environment variables++:   
They are key-value pairs present in the system’s environment. Python reads some of the variables at the start to determine how to behave, where to look for modules.   
Frequently used environment variables:   
1. **PYTHONPATH**:   
Adds user-defined directories to Python’s module search path** (sys.path). **  
++Use case++ -> help find modules that aren’t installed in standard locations  
![export PYTHONPATH="/home/user/mymodules"](Attachments/E4675734-8C65-485B-A4F3-133CFE4B64C5.png)  
  
2. **PYTHONHOME**:   
Sets the default location for standard libraries.   
++Use-case++ -> useful when embedding python or using a custom python distribution  
![Example:](Attachments/21DF8FF8-C94F-420F-872D-A2EE3308FEB2.png)  
  
3. **PYTHONINSPECT**:   
Forces python to enter interactive mode after running a script. It can also make changes to the code and force it to enter the inspect mode on program termination.   
++Use-case++ -> helpful during debugging or quick testing.   
  
4. **PYTHONVERBOSE**:  
If this variable is set to an empty string, it prints a message every time a module is initialised, showing the location of the file/module form where it has been loaded.  
++Use-case++ -> helpful for debugging import-related issues  
  
### ++Ways to run python code++:   
* Using interactive mode   
* Using command line  
* Using IDE  
  
  
  
## ++Basic project layout++:   
Python project follows a clean structure to organise code, manage dependencies, and make packaging seamless.   
![- my_project/](Attachments/3337D5E6-57CF-4182-85BD-846A56F63CA9.png)  
