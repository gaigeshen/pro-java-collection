The Set and SortedSet Interfaces:
The java.util.Set Interface extends the Collection interface.
The Set interface declares methods for managing a collection of objects that contain no duplicates.

1. The basic Set interface makes no guarantee of the order of elements.
2. A Set can contain at most one null element.
3. Mutable elements should not be changed while in a Set.
4. The Set interface adds no methods beyond those of the Collection interface.
	The Set interface simply enforces behavior of the collection.

The java.util.SortedSet interface extends Set so that elements are automatically ordered.
1. A SortedSet Iterator traverses the Set in order.
2. A SortedSet also adds the methods first(), last(), headSet(), tailSet(), and subSet()


Classes Implementing Set:
1. java.util.HashSet
	A hash table implementation of the Set interface.
	The best all-around implementation of the Set interface,
	providing fast lookup and updates.
2. java.util.LinkedHashSet
	A hash table and linked list implementation of the Set interface.
	It maintains the insertion order of elements for iteration, and runs nearly as fast as a HashSet.
3. java.util.TreeSet
	A red-black tree implementation of the SortedSet interface,
	maintaining the collection in sorted order, but slower for lookups and updates.
