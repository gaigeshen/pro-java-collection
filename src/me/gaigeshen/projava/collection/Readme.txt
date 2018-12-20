The Collection Interface:
1. It represents a group of Objects.
2. Primitive types (e.g., int) must be boxed (e.g., Integer) for inclusion in a collection.
3. More specific collection interfaces (e.g., List) extend this interface.


Includes a variety of methods:
1. Adding objects to the collection: add(E), addAll(Collection)
2. Testing size and membership: size(), isEmpty(), contains(E), containsAll(Collection)
3. Iterating over members: iterator()
4. Removing members: remove(E), removeAll(Collection), clear(), retainAll(Collection)
5. Generating array representations: toArray(), toArray(T[])

Does not say anything about:
1. the order of elements
2. whether they can be duplicated
3. whether they can be null
4. the types of elements they can contain

This interface is typically used to pass collections around and manipulate them in the most generic way


Iterating Over a Collection:
An iterator is an object that iterates over the objects in a collection.
java.util.Iterator is an interface specifying the capabilities of an iterator.
Invoking the iterator() method on a collection returns an iterator object that implements Iterator and knows how to step through the objects in the underlying collection.

The Collections Class:
The java.util.Collections class (note the final "s" ) consists exclusively of static methods that operate on or return collections. Features include:
1. Taking a collection and returning an unmodifiable view of the collection
2. Taking a collection and returning a synchronized view of the collection for thread-safe use
3. Returning the minimum or maximum element from a collection
4. Sorting, reversing, rotating, and randomly shuffling List elements

Several methods of the Collections class require objects in the collection to be comparable.
1. The object class must implement the java.lang.Comparable interface.
2. The object class must provide an implementation of the compareTo() method



Type Safety in Java Collections:
In Java 1.4 and earlier they used Object as the type for any object added to the collection.



Generics:
1. Java Generics, introduced in Java 5, provide stronger type safety.
2. Generics allow types to be passed as parameters to class, interface, and method declarations.
3. With the type parameter, the compiler ensures that we use the collection with objects of a compatible type only.
4. Another benefit is that we won’t need to cast the objects we get from the collection.
5. Object type errors are now detected at compile time, rather than throwing casting exceptions at runtime.



Generics and Polymorphism:
What can be confusing about generics when you start to use them is that collections of a type are not polymorphic on the type.
That is, you can not assign a List<String> to a reference variable of type List<Object>, it results in a compiler error.
Why? If allowed, we could then add objects of an incompatible type to the collection through the more “generic” typed reference variable.

So if you define a printCollection() to accept a parameter typed List<Person>, you can pass only List<Person> collections as arguments.
a. Even if Employee is a subclass of Person, a List<Employee> can’t be assigned to a List<Person>.
	
	
	
	
Type Wildcards:
The ? type parameter wildcard is interpreted as “type unknown.”
So declaring a variable as List<?> means that you can assign a List of any type of object to the reference variable.
However, once assigned to the variable, you can’t make any assumptions about the type of the objects in the list.

So defining your method as printCollection(List<?> persons) means that it can accept a List of any type.
But when invoked, you can’t make any assumptions as to the type of objects that the list contains.
Remember, ? is “type unknown”.
At best, you know that everything can be treated as an Object.



Qualified Type Wildcards:
Declaring a variable or parameter as List<? extends Person>, says that the list can be of all Person objects, or all objects can be of (the same) subclass of Person.
So you can access any existing object in the List as a Person.
However, you can’t add new objects to the List.
The list might contain all Person objects… or Employee objects, or Customer objects, or objects of some other subclass of Person.
You’d be in trouble if you could add a Customer to a list of Employees.

Another type wildcard qualifier is super.
List<? super Employee> means a List of objects of type Employee or some supertype of Employee.
So the type is “unknown,” but in this case it could be Employee, Person, or Object.
Because you don’t know which, for “read” access the best you can do is use only Object methods.
But you can add new Employee objects to the list, because polymorphism allows the Employee to be treated as a Person or Object as well.

Both extends and super can be combined with the wildcard type.



Generic Methods:
A generic method is one implemented to work with a variety of types.
The method definition contains one or more type parameters whose values are determined when the method is invoked.
Type parameters are listed within <> after any access modifiers and before the method return type.
You can use any identifier for a type parameter, but single letters like <T> are used most often.
	
