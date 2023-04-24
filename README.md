- a collection is like a container that can have zero, one, or many elements in it
- arrays are not easy or convenient to code against
- arrays can be difficult to debug because they do not have a human readable toString implementation
- you can pass System.out.println(Arrays.toString(products)); just to read it, otherwise it will not be readable
- arrays are not resizable
- collections are a lot more flexible than arrays
- arrays support duplicates, which generally you do not want
- arrays are a low level construct, they are good for basic coding, but can only go so far
- data structures are diverse, can have ordering, pairs, and uniqueness
- lists: collections with iteration order
- maps: collections of pairs
- collections framework top interface is a collection interface
- most used collection is a List, which is a list that has ordering of elements, and each element has a given index
- Set, SortedSet, and NavigableSet interfaces. Set has uniqueness as a key property
- Queue and double ended queue(Deque) interfaces. Can use first in first out, last in last out, etc
- Map and SortedMap extension, map is a collection of pairs
- each collection has at least two different components
- most popular implementations of List is ArrayList and LinkedList
- most popular implementations of sets are HashSets and TreeSets, TreeSet is a SortedSet
- most popular implementations of QUeues are PriorityQueue and LinkedList and ArrayDeque, the latter two are Deque.
- for map, we have HashMap, and for SortedMap, we have TreeMap
- to figure out which one to use, first figure out:
- are your elements keyed or just elements on their own?
- if yes, is order important?
- if yes, use SortedMap. if no, use Map
- if elements are not keyed, do the elements have to be unique?
- if yes, is order important?
- if yes, use SortedSet. if no, use Set
- if the elements do not have to be unique, does insertion order matter?
- if yes, use Deque, if no, use List
- collection interface extends the Iterable interface
- iterable interface allows us to create an object called iterator, which we can use to loop over elements in a collection
- first set of operations that collections have in common are: size(), isEmpty(), add(), and addAll()
- size() gets the number of elements in the collection
- isEmpty() returns true if size() == 0, false otherwise
- add() ensure that an element is in the collection
- addAll() adds all elements of the argument collection to this collection
- remove(element) removes the element from this collection
- removeAll(collection) removes all the elements of the argument collection to this collection
- retainAll(collection) removes all the elements of this collection not in the argument collection
- contains(element) true if the element is in this collection, false otherwise
- containsAll(collection) true if all the elements of the argument collection are in this collection
- clear() remove all elements from this collection
- easiest way to loop through a collection is to use forEach loop
- for each product in the products collection, then specify type
- reads as for(Product product : products)
- when printing use what is right before the :
- for example, this one would be System.out.println(product);
- can remove elements by using what is in the object
- for example: if(product.getWeight() > 20) {products.remove(product)}
- you cannot use add or remove or modify a collection while looping through it with foreach, it must be before or after
- to modify while looping, you can use the .iterator() that every collection has since it extends the iterable interface and has ab iterator associated with it
- example of iterator format: while(iterator.hasNext()) {Product product = iterator.next();
- if(product.getWeight() > 20 )
- {iterator.remove();
-     }
- System.out.println(products.size());
- System.out.println(products.size());
-   }
- }

- 
