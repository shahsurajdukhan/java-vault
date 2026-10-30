## Complete Guide to File Handling
#### Create A File
we can create a file using multiple ways. 
- Using FileOutputStream() Constructor
- Using File.createNewFile() method
- Using Files.write() method

Creating a file using FileOutputStream() Constructor
FileOutputStream is used to create a file and write data into it. The stream would create a file, if it doesn't already exist, before opening it for output.

1st Syntax : OutputStream f = new FileOutputStream ("C:/java/hello.txt")

2nd Syntax : File f = new File("c:/java/hello.txt");  OutputStream f = new FileOutputStream(f);

Creating File Using File.createNewFile() Method allows to create a file in given location or in current directory as follows - 
File file = new File ()


Java - Writing to File
We can write to a file in java using multiple ways
Using FileOutputStream() Constructor
FileWriter.write() method
Files.write() method 

Write to file using FileOutputStream is used to create a file and write into it.
The stream would create a file, if it doesn't already exists, before opening it for output.

Syntax :
OutputStream f = new FileOutputStream("C:/java/hello.txt")

Other Syntax :
File f = new File ("C:/java/hello.txt");
OutputStream f = new FileOutputStream(f);

for (int x = 0; x < bWrite.length ; x++) {
	os.write( bWrite[x] ); // writes the bytes
}

---
File handling allows our programs to create,read,write,update,append and delete files stored on our comuter.

File handling is the process of storing, retrieving, modifying, and managing data in files using a programming language.
Normally, when we run a java program, the data stored in variables exists in RAM (temporary memory).

For Example : 
`public class Main {`
	`public static void main (String args []) {`
		`String name = "Suraj";`
		`int age = 23;`
		`System.out.println(name);`
		`System.out.println(age);`
	`}`
`}`

The problem is that when your program terminates, the values stored in these variables are lost.
What if we want to store this information permanently?
That's where file handling comes in.
%%You can store the data in a file:
student.text
Name : Suraj
Age : 23%%

Even after closing your java application or restarting your computer, the data remains stored.

#### Why do we use File Handling in Java?
there are several reasons :
1. Permanent Storage - Save information even after the program terminates.
2. Data Retrieval - Read Previously stored information.
3. Data Modification - Update existing information.
4. Data Sharing - Share information between different applications.
5. Logging - Store application activities and errors.
6. Backup - Maintain copies of important information.
7. Configuration - Store application settings.

Real world-examples : 
1. Banking application : store transaction records.
2. Student management system : save student details.
3. E-commerce application : maintain order records.
4. Attendance system : store daily attendance.
5. Chat application : save conversation history.
6. Software application : maintain error logs.
All these applications need some form of persistent storage.

NOTE : large production applications generally use databases such as MYSQL or POSTGRESQL instead of relying entirely on files.

#### Types of File Handling Operations
Java supports several common file operations.
1. Create - Create a new file
2. Read - Retrieve file data
3. Write - Store data in a file
4. Append - Add data at the end
5. Update - Modify existing data
6. Delete - Remove a file

Java provides the File class through the java.io package
`import java.io.File;`

`public class Main {`
`public static void main (String[] args) {`

	`try {`
		`File file = new File(""student.txt);`
		
		`if (file.createNewFile()) {`
		`System.out.println("File created successfully!");`
		`} else {`
			`System.out.println("File already exists.")`
		`}`
	`} catch (IOException e) {`
			`System.out.println("An occur occurred.")`
	`}`
`}`
`}`

---
For creating a file we will use createNewFile() method.
For Writing Data into file we will use FileWriter() method.
For Appending data to an existing file FileWriter() method.
For reading data from a file use FileReader() method.

read() - reads one character
readLine() - reads one complete line
close() - closes the reader

We can also read file contents using the scanner class.
Scanner is especially useful when we want to read and parse different types of data, such as integers, doubles, and strings.

#### Types of File Handling in Java
Java provides different file-handling approaches depending on the type of data you want to store.

Text file (Human Readable characters) - Binary file (Raw bytes)

Type 1 : Text File Handling - text files store information in a human-readable format.
EX : 
.txt
.csv
.json
.xml

Java uses character streams to handle text data.

FileReader - reads characters
FileWriter - writes characters
BufferedReader - Reads text efficiently using buffering
BufferedWriter - Writes text efficiently using buffering
PrintWriter - Writes formatted text

Type 2 : Binary File handling - Binary files store data in the form of bytes rather than directly readable text.
EX:
Images (.jpg , .png)
Audio (.mp3)
Videos (.mp4)
PDF Files
Executable files

Java uses byte streams to handle binary data.

Important classes :
FileInputStream - Reads bytes from a file
FileOutputStream - Writes bytes into a file
BufferedInputStream - Reads bytes efficiently using buffering
BufferedOutputStream - Writes bytes efficiently using buffering
DataInputStream - Reads primitive java data types
DataOutputStream - Writes primitive java data types
ObjectInputStream - Reads serialized objects
ObjectOutputStream - writes serialized objects

---
Difference between Byte Streams and Character Streams

Size of byte streams is 8-bit units and for character streams it's 16-bit java characters
Byte streams is used for images,audio,PDFs and character streams for text files.
Base Classes for Byte Stream is InputStream, OutputStream wahereas for character stream it is Reader,Writer.

---
what is BufferedReader and BufferedWriter?
they increase the performance and efficiency.
consider reading a file containing 10,000 lines 
Using FileReader directly, you might read one character at a time.
BufferedReader uses an internal buffer to reduce expensive underlying read operations.

---
### What is Exception Handling in File Handling?\
File operations can fail for several reasons:
- File does not exist
- File permission is denied
- Storage device has an issue.
- File Cannot be accessed.
- An I/O operation fails.
Java provides exception handling to manage these situations.
Most important exception is : IOException

try {
FileReader reader = new FileReader ("data.txt");
} catch (IOException e) {
System.out.println("File Operation Failed");
}

---
What is try-with-resource?
This is a better approach for managing file resources.
Because Java automatically closes the resource when the try block finishes, even if an exception occurs.