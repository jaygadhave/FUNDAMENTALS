A PriorityQueue is used when the objects are supposed to be processed based on the priority. It is known that a Queue follows the First-In-First-Out algorithm, but sometimes the elements of the queue are needed to be processed according to the priority, that’s when the PriorityQueue comes into play.

The PriorityQueue is based on the priority heap. The elements of the priority queue are ordered according to the natural ordering, or by a Comparator provided at queue construction time, depending on which constructor is used.  

In the below priority queue, an element with a maximum ASCII value will have the highest priority.

Working of PriorityQueue

Declaration:

public class PriorityQueue<E> extends AbstractQueue<E> implements Serializable

where E is the type of elements held in this queue
The class implements Serializable, Iterable<E>, Collection<E>, Queue<E> interfaces.

A few important points on Priority Queue are as follows: 

PriorityQueue doesn’t permit null.
We can’t create a PriorityQueue of Objects that are non-comparable
PriorityQueue are unbound queues.
The head of this queue is the least element with respect to the specified ordering. If multiple elements are tied for the least value, the head is one of those elements — ties are broken arbitrarily.
Since PriorityQueue is not thread-safe, java provides PriorityBlockingQueue class that implements the BlockingQueue interface to use in a java multithreading environment.
The queue retrieval operations poll,  remove,  peek, and element access the element at the head of the queue.
It provides O(log(n)) time for add and poll methods.
It inherits methods from AbstractQueue, AbstractCollection, Collection, and Object class.
Constructors:

1. PriorityQueue(): Creates a PriorityQueue with the default initial capacity (11) that orders its elements according to their natural ordering.

PriorityQueue<E> pq = new PriorityQueue<E>();

2. PriorityQueue(Collection<E> c): Creates a PriorityQueue containing the elements in the specified collection.

PriorityQueue<E> pq = new PriorityQueue<E>(Collection<E> c);

3. PriorityQueue(int initialCapacity): Creates a PriorityQueue with the specified initial capacity that orders its elements according to their natural ordering.

PriorityQueue<E> pq = new PriorityQueue<E>(int initialCapacity);

4. PriorityQueue(int initialCapacity, Comparator<E> comparator): Creates a PriorityQueue with the specified initial capacity that orders its elements according to the specified comparator.

PriorityQueue<E> pq = new PriorityQueue(int initialCapacity, Comparator<E> comparator);

5. PriorityQueue(PriorityQueue<E> c): Creates a PriorityQueue containing the elements in the specified priority queue.

PriorityQueue<E> pq = new PriorityQueue(PriorityQueue<E> c);

6. PriorityQueue(SortedSet<E> c): Creates a PriorityQueue containing the elements in the specified sorted set.

PriorityQueue<E> pq = new PriorityQueue<E>(SortedSet<E> c);
