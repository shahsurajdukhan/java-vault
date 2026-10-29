## Today's Agenda is :
# Create A File
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

