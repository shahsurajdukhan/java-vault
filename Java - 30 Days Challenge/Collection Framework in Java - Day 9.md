The Java Collection Framework (JCF) is used in real-world application development, Spring Boot backend development.

##### What is Java Collection Framework?
The Java collection framework is a set of interfaces, classes, and algorithms that help us store, organize, access, search, and manipulate group of objects.

imagine you want to store the name of five students - without a collection, you might create an array:
String[] students = {
	"Rahul", "Amit", "Priya", "Neha", "Raj"
};

but if you want to add another student later - an array has a fixed size. 
with an ArrayList, you can do this:

import java.util.ArrayList;

public class Main {
	public static void main(String[] args) {
	ArrayList String students = new ArrayList<>();

students.add("Rahul");
students.add("Amit");
students.add("Priya");

System.out.println(students);
	
	}
}

this list grows automatically as you add elements.


##### Why we need Collection Framework?
- to store multiple objects without manually managing array sizes.
- to add,remove,search,and update elements easily.
- to remove duplicates when needed.
- to store data as key value pairs.
- to sort and process data efficiently.
- to choose different data structures for different requirements.

##### List Interface
a list is a collection that :
- maintains elements in a defined sequence.
- allows duplicate elements. // important
- supports index-based access, starting at index 0.
- usually allows null, depending on the implementation.
  
  add(element) - adds an element
  add(index, element) - inserts at a specific index
  get(index) - retrieves an element
  set(index, element) - replaces an element
  remove(index) - removes an element at an index
  remove(object) - removes a matching element
  contains(element) - checks whether an element exists
  indeOf (element) - returns the first matching index
  size() - returns the number of element
  isEmpty() - checks whether the list is empty
  clear() - removes all elements

##### What is collection vs collections
Collection is an interface which represents a group of elements for ex : List, Set , Queue
whereas Collections is a utility class which provides hepful operations on collections. for ex : sort() , reverse() , shuffle ().

List() is an interface, and Collections.sort() sorts the list.

ArrayList is a resizable array. - we can access an element directly using its index.
LinkedList stores elements in linked nodes. Each node refers to its neighboring nodes.
Stack follows LIFO - Last in, First out. - Push,Peek,Pop,Empty,Search

