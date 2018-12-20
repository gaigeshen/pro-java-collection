The Map Interface:
> The java.util.Map interface does not extend the Collection interface!
> A Map is a collection that maps key objects to value objects.
	a. A Map cannot contain duplicate keys
	b. Each key can map to at most one value.
> The Map interface methods include:
	a. Adding key-value pairs to the collection: put(K, V), putAll(Map)
	b. Retrieving a value by its key: get(K)
	c. Testing size: size(), isEmpty()
	d. Testing membership: containsKey(K), containsValue(V)
	e. Removing members: remove(K), clear()
> The java.util.SortedMap interface extends Map so that elements are automatically ordered by key.
	a. Iterating over a SortedMap iterates over the elements in key order.
	b. A SortedMap also adds the methods firstKey(), lastKey(), headMap(), tailMap(), and subMap()
	

Retrieving Map Views:
> You can also retrieve collections as modifiable views from the Map representing the keys (keySet()), the values (values()), and a Set of key-value pairs (entrySet()).
	a. These collections are used typically to iterate over the Map elements.
	b. These collections are backed by the Map, so changes to the Map are reflected in the collection views and vice-versa.
> Iterating over Map elements is done typically with a Set of objects implementing the java.util.Map.Entry interface.
	a. You retrieve the Set of Map.Entry objects by invoking Map.entrySet().
	b. To iterate over the Map elements using an explicit Iterator:
	

Classes Implementing Map:
1. java.util.HashMap
	A hash table implementation of the Map interface.
	The best all-around implementation of the Map interface, providing fast lookup and updates.
2. java.util.LinkedHashMap
	A hash table and linked list implementation of the Map interface.
	It maintains the insertion order of elements for iteration, and runs nearly as fast as a HashMap.
3. java.util.TreeMap
	A red-black tree implementation of the SortedMap interface,
	maintaining the collection in sorted order, but slower for lookups and updates.