JAVA ITERATOR:

A Java Cursor is an Iterator, which is used to iterate or traverse or retrieve a Collection or Stream object’s elements one by one. There are three cursors in Java.

Iterator
Enumeration
ListIterator
Note: SplitIterator can also be considered as a cursor as it is a type of Iterator only.

1. Iterator
Iterators in Java are used in the Collection framework to retrieve elements one by one. It is a universal iterator as we can apply it to any Collection object. By using Iterator, we can perform both read and remove operations. It is an improved version of Enumeration with the additional functionality of removing an element.

Iterator must be used whenever we want to enumerate elements in all Collection framework implemented interfaces like Set, List, Queue, Deque, and all implemented classes of Map interface. Iterator is the only cursor available for the entire collection framework.
Iterator object can be created by calling iterator() method present in Collection interface.

Syntax:

Iterator itr = c.iterator();
Note: Here “c” is any Collection object. itr is of type Iterator interface and refers to “c”.

Methods of Iterator Interface in Java
Iterator interface defines three methods as listed below:

1. hasNext(): Returns true if the iteration has more elements.

public boolean hasNext();
2. next(): Returns the next element in the iteration. It throws NoSuchElementException if no more element is present.

public Object next();
3. remove(): Removes the next element in the iteration. This method can be called only once per call to next().

public void remove();
Note: remove() method can throw two exceptions namely as follows:

UnsupportedOperationException : If the remove operation is not supported by this iterator
IllegalStateException : If the next method has not yet been called, or the remove method has already been called after the last call to the next method.
How does Java Iterator Works Internally?
 In this section, we will try to understand how Java Iterator and its methods work internally. Let us take the following LinkedList object to understand this functionality.


List<String> cities = new LinkedList<>(); 
cities.add("G-1"); 
cities.add("G-2"); 
cities.add("G-3"); 
. 
. 
. 
cities.add("G-n");
Now, let us create an Iterator object on List object as shown below:

Iterator<String> citiesIterator = cities.iterator();
The “citiesIteartor” iterator will look like –

Here Iterator’s Cursor is pointing before the first element of the List.

Now, we will run the following code snippet.

citiesIterator.hasNext();
citiesIterator.next();


When we run the above code snippet, Iterator’s Cursor points to the first element in the list as shown in the above diagram.

Now, we will run the following code snippet.

citiesIterator.hasNext();
citiesIterator.next();


When we run the above code snippet, Iterator’s Cursor points to the second element in the list as shown in the above diagram. Do this process to reach the Iterator’s Cursor to the end element of the List.



After reading the final element, if we run the below code snippet, it returns a “false” value.

citiesIterator.hasNext();


As Iterator’s Cursor points to the after the final element of the List, hasNext() method returns a false value.

Note: After observing all these diagrams, we can say that Java Iterator supports only Forward Direction Iteration as shown in the below diagram. So it is also known as Uni-Directional Cursor.
