So as we know different types of errors can occur while running a program - such as coding mistakes, invalid input or unexpected situations.

so when this condition arises, which means when an error occurs, java will normally stop and generate an error, this thing in technical term we call as : java will throw an exception.

so basically, exception handling lets you catch and handle errors during runtime - so your program doesn't crash.


## What is try and catch?
- try statement allows us to define a block of code to be tested for errors while it is being executed.
- catch statement allows us to define a block of code to be executed, if an error occurs in the try block.
- try and catch keywords always come in pairs.

for ex:

public class Main {
public static void main (String [ ] args) {
	int myNumbers = {1,2,3};
	System.out.println(myNumbers[10]);   // error!
}
}

for this the output will be error : arrayindexoutofboundsexception.

to handle this error beforehand we can code like this :

public class Main {
public static void main(String[ ] args) {
try {
	int[] myNumbers = {1,2,3};
	System.out.println(myNumbers[10]);
} catch (Exception e) {
System.out.println("Something went wrong");
}
}
}

## this way we can handle the exception well.


# why finally term is used ?
- Basically used to run by default regardless of which block is being executed try or block
- finally statement let's us execute code after try....catch , regardless of the result: if the try block runs then also finally block will run
- and if the catch block will run then also the finally block will run.


# Why the throw keyword is used?
- throw statement allows us to create a custom error.
- throw keyword is used together with many exception types available in java like ArithmeticException, FileNotFoundException, ArrayIndexOutOfBoundException, SecurityException , etc
  
  Ex:
	public class Main {
		static void checkAge(int age) {
		if (age < 18) {
		throw new ArithmeticException("Access Denied - you must be atleast 18 years old")}
		else {System.out.println("Access granted - you are old enough);}
		
		}}
	public static void main (String [] args) {
	checkAge(15); // set age to 15}
}
}



# Exception Types
1. Arithmetic Error - occurs when a numeric calculation goes wrong
2. ArrayIndexOutOfBoundsException - occurs when trying to access an index number that does not exist in an array
3. ClassNotFoundException - occurs when trying to access a class that does not exist
4. FileNotFoundException - occurs when a file cannot be accessed
5. InputMatchException - occurs when entering wrong input
6. IO exception - occurs when an input or output operation fails
7. NullPointerException - occurs when trying to access an object refernce that is null
8. NumberFormatException - occurs when it is not  possible to convert a specified string to a numberic type
9. StringIndexOutOfBoundException - occurs when trying to access a character in a string that does no exist.

there are many more exceptions list but these are some of the important ones....

---
that's it for today, if you have any queries reach out to me at suraj.adi@outlook.com