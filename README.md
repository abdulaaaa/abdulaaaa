
# Collections Framework Design Document

> Goal: Re-create the Java Collections Framework but add my own features to make it more efficient.
> 

How this can be done (Version 2): 

- Make accessing certain elements faster (Faster Hashing Algorithm)
    - For Hashing Collision See if you can implement a faster Method (Using a tree)
- Implementing New Data Structures Like Graphs, and Trees (Heap & RBT)
- Implement new Sorting Algorithms inside the Collections class to allow users with a wide variety of options.

- Collection (Class)
    
    ### Creation of Collections
    
    - **`emptyList()`**: Returns an empty `List` (immutable).
    - **`emptySet()`**: Returns an empty `Set` (immutable).
    - **`emptyMap()`**: Returns an empty `Map` (immutable).
    - **`singletonList(E o)`**: Returns an immutable list containing only the specified object.
    - **`singleton(E o)`**: Returns an immutable set containing only the specified object.
    - **`singletonMap(K key, V value)`**: Returns an immutable map containing a single key-value pair.
    - **`nCopies(int n, T o)`**: Returns an immutable list consisting of `n` copies of the specified object.
    
    ### Utility Methods for Lists
    
    - **`sort(List<T> list)`**: Sorts the specified list into ascending order, according to the natural ordering of its elements.
    - **`sort(List<T> list, Comparator<? super T> c)`**: Sorts the specified list according to the order induced by the specified comparator.
    - **`binarySearch(List<? extends Comparable<? super T>> list, T key)`**: Searches the specified list for the specified object using binary search.
    - **`binarySearch(List<? extends T> list, T key, Comparator<? super T> c)`**: Searches the specified list for the specified object using binary search with a comparator.
    - **`reverse(List<?> list)`**: Reverses the order of the elements in the specified list.
    - **`shuffle(List<?> list)`**: Randomly permutes the elements in the specified list using a default source of randomness.
    - **`shuffle(List<?> list, Random rnd)`**: Randomly permutes the elements in the specified list using the specified source of randomness.
    - **`fill(List<? super T> list, T obj)`**: Replaces all of the elements of the specified list with the specified element.
    - **`copy(List<? super T> dest, List<? extends T> src)`**: Copies all of the elements from one list into another.
    - **`swap(List<?> list, int i, int j)`**: Swaps the elements at the specified positions in the specified list.
    
    ### Utility Methods for Sets
    
    - **`newSetFromMap(Map<E, Boolean> map)`**: Returns a set backed by the specified map.
    
    ### Utility Methods for Maps
    
    - **`frequency(Collection<?> c, Object o)`**: Returns the number of occurrences of the specified element in the specified collection.
    - **`disjoint(Collection<?> c1, Collection<?> c2)`**: Returns `true` if the two specified collections have no elements in common.
    - **`unmodifiableCollection(Collection<? extends T> c)`**: Returns an unmodifiable view of the specified collection.
    - **`unmodifiableList(List<? extends T> list)`**: Returns an unmodifiable view of the specified list.
    - **`unmodifiableSet(Set<? extends T> s)`**: Returns an unmodifiable view of the specified set.
    - **`unmodifiableMap(Map<? extends K, ? extends V> m)`**: Returns an unmodifiable view of the specified map.
    - **`synchronizedCollection(Collection<T> c)`**: Returns a synchronized (thread-safe) collection backed by the specified collection.
    - **`synchronizedList(List<T> list)`**: Returns a synchronized (thread-safe) list backed by the specified list.
    - **`synchronizedSet(Set<T> s)`**: Returns a synchronized (thread-safe) set backed by the specified set.
    - **`synchronizedMap(Map<K, V> m)`**: Returns a synchronized (thread-safe) map backed by the specified map.
    
    ### Specialized Views and Wrappers
    
    - **`checkedCollection(Collection<T> c, Class<T> type)`**: Returns a dynamically type-safe view of the specified collection.
    - **`checkedList(List<T> list, Class<T> type)`**: Returns a dynamically type-safe view of the specified list.
    - **`checkedSet(Set<T> s, Class<T> type)`**: Returns a dynamically type-safe view of the specified set.
    - **`checkedMap(Map<K, V> m, Class<K> keyType, Class<V> valueType)`**: Returns a dynamically type-safe view of the specified map.
    
    ### Other Utility Methods
    
    - **`asLifoQueue(Deque<T> deque)`**: Returns a view of the specified deque as a `Queue` with last-in-first-out (LIFO) semantics.
    - **`enumeration(Collection<T> c)`**: Returns an enumeration over the specified collection.
    - **`list(Enumeration<T> e)`**: Returns a list containing the elements returned by the specified enumeration.
