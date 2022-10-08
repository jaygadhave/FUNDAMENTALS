ArrayList is a part of Java collection framework and it is a class of java.util package. 
It provides us with dynamic arrays in Java. Though, it may be slower than standard arrays but can be helpful in programs where lots of manipulation in the array is needed. 
This class is found in java.util package. The main advantages of ArrayList are, if we declare an array then it’s needed to mention the size but in ArrayList it is not needed to mention to the size of ArrayList but if you want to mention the size then you can do it.

Important Features:
ArrayList inherits AbstractList class and implements the List interface.
ArrayList is initialized by the size. However, the size is increased automatically if the collection grows or shrinks if the objects are removed from the collection.
Java ArrayList allows us to randomly access the list.
ArrayList can not be used for primitive types, like int, char, etc. We need a wrapper class for such cases.
ArrayList in Java can be seen as a vector in C++.
ArrayList is not Synchronized. Its equivalent synchronized class in Java is Vector.

A separate functionality is implemented in each of the mentioned classes. They are:
AbstractList: This class is used to implement an unmodifiable list, for which one needs to only extend this AbstractList Class and implement only the get() and the size() methods.
CopyOnWriteArrayList: This class implements the list interface. It is an enhanced version of ArrayList in which all the modifications(add, set, remove, etc.) are implemented by making a fresh copy of the list.
AbstractSequentialList: This class implements the Collection interface and the AbstractCollection class. This class is used to implement an unmodifiable list, for which one needs to only extend this AbstractList Class and implement only the get() and the size() methods.
Constructors in the ArrayList
In order to create an ArrayList, we need to create an object of the ArrayList class. The ArrayList class consists of various constructors which allow the possible creation of the array list. The following are the constructors available in this class:
 
1. ArrayList(): This constructor is used to build an empty array list. If we wish to create an empty ArrayList with the name arr, then, it can be created as:
ArrayList arr = new ArrayList(); 
 
2. ArrayList(Collection c): This constructor is used to build an array list initialized with the elements from the collection c. Suppose, we wish to create an ArrayList arr which contains the elements present in the collection c, then, it can be created as: 
ArrayList arr = new ArrayList(c); 
 
3. ArrayList(int capacity): This constructor is used to build an array list with initial capacity being specified. Suppose we wish to create an ArrayList with the initial size being N, then, it can be created as:
ArrayList arr = new ArrayList(N);  

Let’s see how to perform some basics operations on the ArrayList as listed which we are going to discuss further alongside implementing every operation.
Adding element to List
Changing elements
Removing elements
Iterating elements   
Operation 1: Adding Elements
In order to add an element to an ArrayList, we can use the add() method. This method is overloaded to perform multiple operations based on different parameters. They are as follows:  
add(Object): This method is used to add an element at the end of the ArrayList.
add(int index, Object): This method is used to add an element at a specific index in the ArrayList.
