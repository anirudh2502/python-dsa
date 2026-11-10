#   
  
## ++Week 2 Day 3 python++  
  
## ++Reading and writing files:++  
Python provides built-in functions for creating, reading and writing files.   
###   
### ++Opening a text file++:  
Files can be opened using the built-in “**open()**” function.   
![f1 = open ("MyFile1.txt"](Attachments/1DA5E503-89CE-49BC-8736-9E17B0C146A8.png)  
  
### ++Reading a text file++:  
1. ++Using ‘**read()**++’ - Returns the read bytes in form of a string. Reads 'n' bytes, if no 'n' specified, reads the entire file.   
2. ++Using ‘**readline()**++’ - Reads a single line from the file as a string. If n is specified, it reads at most n characters, but never more than one line.   
3. ++Using ‘**readlines()**++’ - Reads all the lines and return them as each line a string element in a list.    
![(i. closet)](Attachments/8B279D69-2753-42BF-9445-FDE934DA6FF4.png)  
  
### ++Writing in a text file++:   
1. ++Using ‘**write()**++’ - Inserts the string in a single line in the text file.   
2. ++Using ‘**writelines()**++’ - Used to insert multiple strings at a single time.  
  
  
  
## ++File modes++:   
The file mode tells python what kind of operation it needs to perform on the file (read, write, etc). The mode is specified as the second argument to ‘open()’ function.   

| Mode  | Description                   |
| ----- | ----------------------------- |
| R     | Read-only                     |
| r+    | Read and write                |
| W     | Write-only                    |
| w+    | Read and write                |
| A     | Append-only                   |
| a+    | Read and append               |
| Rb    | Read in binary mode           |
| rb+   | Read and write in binary mode |
| Wb    | Write in binary               |
| wb+   | Read and write in binary      |
  
  
  
  
## ++Context manager++:   
Python’s context managers provide a neat way to automatically set-up and clean up resources, ensuring they’re properly managed even if errors occur.   
++Need for context managers++:   
- Automatic cleanup  
- Avoid resource leaks   
- Cleaner code   
- Exception safe  
The “**with**” statement provides a built-in context manager that ensures file is automatically closed once done with it, even if error occurs.   
![with open("test. txt") as](Attachments/816FA5C3-5122-4FA0-9B43-4B5154F5E8AE.png)  
This eliminated the need to call ‘close()’ and protects against resource leakage in case of unexpected failures.   
  
  
  
## ++Pathlib++:   
The path class in **pathlib module** is the main class used to represent and interact with file and directory paths on the actual file system.   
![from pathlib import Path](Attachments/50C17BA3-02DD-4127-8FF9-7826BDFA6997.png)  
++Need for pathlib module++:  
- Cross-platform compatibility   
- Safer operations  
### ++Use-cases of pathlib module++ -   
* Listing subdirectories   
* Listing python files in a directory tree   
* Navigating inside a directory tree   
* Reading and writing to a file   
### ++Methods in path class++:   
1. **cwd() **- returns a new path object which represents current working directory.  
2. **exists()** - checks whether specified path exists on the disk. It returns True if the path exists, otherwise False.  
3. **is_dir()** - used to determine if path points to a directory. It returns True if the path is a directory, otherwise False.  
  
  
  
## ++Detect Encoding of a Text file:++  
Using the ‘**chardet**’ library we can automatically detect a file’s encoding. It works by analysing the statistical patterns of byte sequences to estimate the most likely encoding**. **  
++Why detect file encoding++?  
- Different systems and apps save text files in different encodings   
- Reading a file with wrong encoding can lead to errors  
- Detection encoding helps ensure smooth file reading and processing   
++Steps to detect text file encoding++:   
1. Create a virtual environment   
2. Install the ‘*chardet*’ library  
3. Implement the logic   
4. Add the file path   
5. Run the server  
  
  
  
## ++JSON serialisation++:  
It is the process of converting python objects to JSON-compatible data. Python’s built-in **“json” module** provides methods to serialise data into a JSON file/string.   

| Python object  | JSON equivalent |
| -------------- | --------------- |
| Dict           | Object          |
| List, tuple    | Array           |
| Str            | String          |
| Int, float     | Number          |
| True           | True            |
| False          | False           |
| None           | Null            |
  
### ++Methods for serialising JSON data++ -   
1. Using ‘**json.dump()**’ - serialises a Python object and writes the resulting JSON data to a file.  
2. Using ‘**json.dumps()**’ - converts a Python object into a JSON-formatted string without writing it to a file.  
![data ruser: 1](Attachments/539DAA2C-3390-4DA5-AE47-F05CE7B76D5D.png)  
  
  
  
## ++JSON deserialisation++:  
It is the process of decoding the data in JSON format into native data type. Deserialisation decodes JSON data into a dictionary.   
### ++Methods to deserialise JSON data++:  
1. **loads()** - to deserialise a JSON document to a Python object.  
2. **load()** - to deserialise a JSON formatted stream to a Python object.   
![# importing the module](Attachments/3D26EFDD-B70C-4715-9092-C47B8AA30E70.png)  
  
  
  
## ++CSV processing++:   
A **CSV (Comma Separated Values) file** is a plain text file where each line represents a data record, and fields within each record are separated by commas. It's commonly used for spreadsheets and databases due to its simplicity and readability.  
1. **++Reading a CSV file++**:   
Reading from a CSV file is done using the *reader* object.   
![filenane - "aaol cey a file nano](Attachments/DC7E72FD-BB97-44E3-80AA-B7FEC0EEF5E7.png)  
  
2. **++Writing to a CSV file: ++**  
To write to a CSV file, we first open the CSV file in WRITE mode. The file object is converted to ‘***csv.writer***’ object and further operations takes place.  
![2:9.31](Attachments/BF72ACC5-AC41-4CD4-942A-986FA6468AB6.png)  
  
  
  
## ++Working with large CSV files++:   
Directly importing a large amount of data leads to out-of-memory error and reading the entire file at once leads to system crashes due to insufficient RAM.  
++The following are the ways to effectively handle large data files in **.csv **format and read large CSV files++ -   
- Using ‘**pandas.read_csv**’ (chunk size):   
One way is to read the entries in chunks of reasonable size and read large CSV files in Python Pandas, which are read into the memory and processed before reading the next chunk.  
- Using **Dask**:   
Dask is an open-source python library that includes features of parallelism and scalability in Python by using the existing libraries like pandas, NumPy, or sklearn.  
- Using **compression**:   
Compression method in Pandas' `**read_csv**` allows you to read compressed CSV files efficiently.   
  
  
  
## ++Binary files++:   
Reading a binary file involves opening the file in binary mode and accessing its contents as bytes instead of texts. This is commonly used when working with files such as images, audio files, videos, PDFs or other non-text data.   
![open ("sample. bin",](Attachments/81012391-89F8-4CB1-9A79-559F4856CAA2.png)  
++Binary file modes++:   
1. **rb**: opens a file for reading binary data    
2. **wb**: opens a file for writing binary data. If the file already exists, its contents are overwritten.  
3. **ab**: opens a file for appending binary data at the end without removing existing content.   
  
## ++Opening a binary file++:  
To read data from a binary file, the file must be opened in read binary mode ("rb"). In this mode, Python reads the file as raw bytes instead of converting the contents into text.   
- **read()**: reads the entire binary file and returns its contents as a bytes object.  
- **readlines()**: reads the file line by line and returns a list of byte strings. Each element in the list represents one line from the binary file.  
