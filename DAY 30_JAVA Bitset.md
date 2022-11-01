The Java BitSet class implements a vector of bits. The BitSet grows automatically as more bits are needed. The BitSet class comes under java.util package. The BitSet class extends the Object class and provides the implementation of Serializable and Cloneable interfaces.

Each component of bit set contains at least one Boolean value. The contents of one BitSet may be changed by other BitSet using logical AND, logical OR and logical exclusive OR operations. The index of bits of BitSet class is represented by positive integers.

Each element of bits contains either true or false value. Initially, all bits of a set have the false value. A BitSet is not safe for multithreaded use without using external synchronization.

Note: Passing a null parameter to any of the methods of BitSet class will throw a NullPointerException.
Java BitSet Methods
Sl No	Modifier & Type	Method	Description

1	void	and(BitSet set)

This method is used to perform a logical AND operation of this target bit set with the specified argument.

2	void	andNot​(BitSet set)

This method is used to clear the entire bit in this BitSet whose corresponding bit is set in the specified BitSet.

3	int	cardinality​()

This method returns the number of bits set to true in this BitSet.

4	void	clear​()

This method set false to all bits in this BitSet.

5	void	clear​(int bitIndex)	

This method set bit to false of a specified index.

6	void	clear​(int fromIndex, int toIndex)	

This method set bits to false from specified fromIndex (inclusive) to toIndex (exclusive).

7	Object	clone​()

This method makes the clone of this BitSet to new BitSet which is equal to it.

8	boolean	equals​(Object obj)

This method is used to compare the current object with the specified object.

9	void	flip​(int bitIndex)

This method sets the bit to its complement at the specified index.

10	void	flip​(int fromIndex, int toIndex)	This method set each bit value to its complement from specified fromIndex (inclusive) to toIndex (exclusive).

11	boolean	get​(int bitIndex)

This method returns the bit value of the specified index.

12	BitSet	get(int fromIndex, int toIndex)	

This method returns a new BitSet of bits from specified fromIndex (inclusive) to toIndex (exclusive).

13	int	hashCode​()

This method returns the hash code value of this BitSet.

14	boolean	intersects​(BitSet set)

This method returns true if the specified BitSet set value is also true in this BitSet set value.

15	boolean	isEmpty​()

This method returns true if the current BitSet does not contain any bit which is set to true.

16	int	length()

This method returns the "logical size" of this BitSet.

17	int	nextClearBit​(int fromIndex)

This method returns the index of first bit which is set to false that occurs on or after the specified index.

18	int	nextSetBit​(int fromIndex)

This method returns the index of first bit which is set to true that occurs on or after the specified index.

19	void	or​(BitSet set)

This method is used to perform a logical OR operation of this target bit set with the specified argument.

20	int	previousClearBit​(int fromIndex)

This method returns the index of the nearest bit which is set to false which occurs on or before the specified index.

21	int	previousSetBit​(int fromIndex)

This method returns the index of the nearest bit which is set to true which occurs on or before the specified index.

22	void	set​(int bitIndex)

This method sets true to bit value at the specified index.

23	void	set​(int bitIndex, boolean value)

This method sets a bit of specified bitIndex to the specified boolean value.

24	void	set​(int fromIndex, int toIndex)	

This method sets the bits from specified fromIndex (inclusive) to toIndex (exclusive) to true.

25	void	set​(int fromIndex, int toIndex, boolean value)	

This method sets the bits from specified fromIndex (inclusive) to toIndex (exclusive) to specified boolean value.

26	int	size​()

This method returns the number of bit space actually in use by this BitSet to represent bit values.

27	IntStream	stream()

This method returns a stream of indices for which this BitSet contains a bit.

28	byte[]	toByteArray()

This method returns a byte array which contains all the bits of this bit set.

29	long[]	toLongArray​()

This method returns a long array which contains all the bits of this bit set.

30	String	toString​()

This method returns a string representation of this bit set.

31	static BitSet	valueOf​(byte[] bytes)

This method returns a new bit set of the given byte array.

32	static BitSet	valueOf​(long[] longs)

This method returns a new bit set of the given long array.

33	static BitSet	valueOf​(ByteBuffer bb)

This method returns a new bit set from the given byte buffer.

34	static BitSet	valueOf​(LongBuffer lb)	

This method returns a new bit set from the given long buffer.

35	void	xor​(BitSet set)

This method is used to perform a logical XOR operation of this bit set with the specified bit set argument.
