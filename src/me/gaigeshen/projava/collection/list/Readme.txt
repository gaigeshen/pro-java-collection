The List Interface:
The java.util.List Interface extends the Collection interface.

The List interface declares methods for managing an ordered collection of object (a sequence). You can:
1. Control where each element is inserted in the list
2. Access elements by their integer index (position in the list)
3. Search for elements in the list
4. Insert duplicate elements and null values, in most List implementations

Some additional methods provided by List include:
1. add(int index, E element) — Insert an element at a specific location (without an index argument, new elements are appended to the end)
2. get(int index) — Return an element at the specified location
3. remove(int index) — Remove an element at the specified location
4. set(int index, E element) — Replace the element at the specified location
5. subList(int fromIndex, int toIndex) — Returns as a List a modifiable view of the specified portion of the list (that is, changes to the view actually affect the underlying list)

Classes Implementing List: Two are used most commonly:
1. java.util.ArrayList
	An ArrayList is usually your best bet for a List if the values remain fairly static once you’ve created the list.
	It’s more efficient than a LinkedList for random access.
2. java.util.LinkedList
	A LinkedList provides better performance than an ArrayList if you’re frequently inserting and deleting elements,
	especially from the middle of the collection. But it’s slower than an ArrayList for random-access.
