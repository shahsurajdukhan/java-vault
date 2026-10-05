Hashset is a class in Java used to store a collection of unique elements.

`import  java.util.HashSet;`

`HashSet<String> names = new HashSet<>();`

`names.add("Suraj");`
`names.add("Rahul");`
`names.add("Amit");`
`names.add("Pratik");`

`System.out.println(names);`

## Important properties of HashSet
- It doesn't allow duplicates
- It doesn't maintains insertion order
- It allows only one null value.

## Why do we use HashSet?
- It mainly used to reduce data redundancy
- suppose you have int [] numbers = {10,20,10,30,20,40}; > you want 10 20 30 40 then a HashSet is perfect for this type of lookup.

## How does HashSet work internally?
- when you do set.add("Suraj"); java calculates the object's hash code "suraj".hashCode() > this hashcode helps java determine where the object should be stored internally.
- and then when you do set.contains("Suraj"); java uses the hashcode to quickly find the appropriate location.
## What is hash Collision?
- when both objects have ended up in the same bucket.
- Object A → Bucket 3   ;   Object B → Bucket 3

## What are the different java methods that exists
- add()  - adds an element to the HashSet.
- remove() - removes an element from the HashSet.
- contains() - checks whether an element exists.
- size() - checks the size of the HashSet
- clear() - removes everything

## Iterating over HashSet
- HashSet doesn't have indexes therefore we can't do > set.get(0); like in case of Array 
- instead we can use a for-each loop.
		`for(String name : set) {`
			`System.out.println(name);`
		`}`
- or an iterator too can work in HashSet

## Why HashSet is used over ArrayList
- suppose you want to check whether a number exists
- Arraylist will take time complexity of O(n) because java may have to scan the list element by element.
- But in HashSet the average time complexity for the lookup will take only 0(1) because it converts the required value into HashCode first then mathches with the available elements inside the HashSet().
- Thus whenever the requirement comes like "have I already seen this element?" then HashSet is the most effective Data Structure to use in Java.

## HashSet vs HashMap
- HashSet -> unique values
	A, B,C,D
- HashMap -> key-value pairs
	A->10; B->20; C->30; D->40


---
