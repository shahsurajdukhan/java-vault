
## Java File Class
Java provides several methods for file handling like creating, updating, and deleting the files.

The File class is used to represent the path of a file or a directory in file system. This class is used for creation of files and directories, file searching, file deletion,etc. We need to import java.io.package before using the file class.

Imagine your computer has a folder called Documents containing a file named notes.txt
The file class lets java refer to that file or folder and perform certain operations on it.

### Create File Object
To work with a file in java, you first create a file object by passing the file name or path as a string. The file object represents the actual/directory on the disk.

`import java.io.File;  // imports the File class`
`File myObj = new File ("filename.txt");`

### Important Methods of the File Class
1. getName() - Returns the file or directory name
2. getPath() - Returns the path used to create the object
3. exists() - checks whether the path exists
4. createNewFIle() - Creates a new empty file
5. delete() - attempts to delete a file or an empty directory
6. isFile() - checks whether the path represents a file
7. isDirectory() - checks whether the path represents a directory
8. length() - returns the file size in bytes
9. mkdir() - creates a single directory
10. list() - Returns the names of the entries in a directory.

### File Class Constructors
following is the list of constructors to create a file object
1.  File (File Parent, String child) - This constructor creates a new file instance from a parent abstract pathname and a child pathname string.
2. File (String pathname) - This constructor creates a new file instance by converting the given pathname string into an abstract pathname
3. File (String parent, String child) - This constructor creates a new file instance from a parent pathname string and a child pathname string.
4. File (URI uri)