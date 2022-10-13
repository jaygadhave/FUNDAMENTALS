Java HashSet:
Java HashSet class is used to create a collection that uses a hash table for storage. It inherits the AbstractSet class and implements Set interface.

The important points about Java HashSet class are:
HashSet stores the elements by using a mechanism called hashing.
HashSet contains unique elements only.
HashSet allows null value.
HashSet class is non synchronized.
HashSet doesn't maintain the insertion order. Here, elements are inserted on the basis of their hashcode.
HashSet is the best approach for search operations.
The initial default capacity of HashSet is 16, and the load factor is 0.75.
Difference between List and Set
A list can contain duplicate elements whereas Set contains unique elements only.

Hierarchy of HashSet class
The HashSet class extends AbstractSet class which implements Set interface. The Set interface inherits Collection and Iterable interfaces in hierarchical order.

HashSet class declaration
Let's see the declaration for java.util.HashSet class.

public class HashSet<E> extends AbstractSet<E> implements Set<E>, Cloneable, Serializable  
Constructors of Java HashSet class
SN	Constructor	Description
1)	HashSet()	It is used to construct a default HashSet.
2)	HashSet(int capacity)	It is used to initialize the capacity of the hash set to the given integer value capacity. The capacity grows automatically as elements are added to the HashSet.
3)	HashSet(int capacity, float loadFactor)	It is used to initialize the capacity of the hash set to the given integer value capacity and the specified load factor.
4)	HashSet(Collection<? extends E> c)	It is used to initialize the hash set by using the elements of the collection c.
Methods of Java HashSet class
Various methods of Java HashSet class are as follows:

SN	Modifier & Type	Method	Description
1)	boolean	add(E e)	It is used to add the specified element to this set if it is not already present.
2)	void	clear()	It is used to remove all of the elements from the set.
3)	object	clone()	It is used to return a shallow copy of this HashSet instance: the elements themselves are not cloned.
4)	boolean	contains(Object o)	It is used to return true if this set contains the specified element.
5)	boolean	isEmpty()	It is used to return true if this set contains no elements.
6)	Iterator<E>	iterator()	It is used to return an iterator over the elements in this set.
7)	boolean	remove(Object o)	It is used to remove the specified element from this set if it is present.
8)	int	size()	It is used to return the number of elements in the set.
9)	Spliterator<E>	spliterator()	It is used to create a late-binding and fail-fast Spliterator over the elements in the set.
