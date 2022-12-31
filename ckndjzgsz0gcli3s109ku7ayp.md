# Bad programmers worry about the code. Good programmers worry about data structures and their relationships: Data Structures

I have a CS background but understood very little of data structures and algorithms while in school. Maybe I wasn't paying attention or the lecturer didn't do a good job teaching it or its a problem with multidimensional factors, that doesn't matter now. 
I have taken time to take courses to study and understand data structures and I'll explain using code samples in python.

**Data Structure** is a way of collecting and organising data in such a way that we can perform operations on these data in an effective way. Data Structures is about rendering data elements in terms of some relationship, for better organization and storage.
To really optimize a code, an understanding of data sctructures is needed. And this is what separates code monkeys and effective problem solvers. 
Coding is more than just tapping on your keyboard based on some unclear requirements, it is the abstraction of the conceptualization of a solution to a problem and to do that effectively, the nitty gritty of how the data should be stored is needed.

### Array
Array is a container which can hold a fix number of items and these items should be of the same type. An *element* refers to each item contained in an array, an *index* refers to the location of an element.

![array.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1618141914356/A-cHlcXf_.gif)

#### Operations time complexities

Insert at the end: constant O(1)

Insert at the begining: linear O(n)

Insert generally: linear O(n)

Remove from end: constant O(1)

Remove from begining: linear O(n)

Remove generally: linear O(n)

Find value: linear O(n)

Access value: constant O(1)

%[https://gist.github.com/LPMatrix/62a9c2f38dd26225e24098992bd43584]


### Linked List
A linked list is a linear data structure, in which the elements are not stored at contiguous memory locations. The elements in a linked list are linked using pointers. The difference between this and an array is that an array stores elements in contigous memory while linked list doesn't. This means that elements in an array can be accessed faster using the index, but for a linked list, an element also contains information on the next element. There are 3 types of linked list: singly linked list, doubly linked list, circular linked list but in this article we will be dealing with singly linked list only.

![linkedlist.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1618143448421/5i3Z-QHGJ.png)

#### Operations time complexities

Insert at the end: constant (if you have a reference to the next node)

Insert at the begining: constant

Insert generally: linear (if you don't have a reference to the next node)

remove generally: linear

Find value: linear

Access value: linear

%[https://gist.github.com/LPMatrix/ec3cfc327486219891b64cca911526ed]


### HashTable
In a hash table, data is stored like a table, a key and an element the key is pointing to. The difference between this and an array is that in an array, the indexes are integers and ordered but in a hash table, the key could be of any type and there's no order to it.

![hash_function.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1618143611614/3i-j9uoG8.jpeg)

#### Operations time complexities

Insertion: linear O(n)

Remove: linear O(n)

Find value: linear O(n)

%[https://gist.github.com/LPMatrix/aaa0f47cf4b05d8f70e8c2e6f259e76d]


### Stack
 A stack is a LIFO (Last In, First Out) data structure. Elements are added or removed at the top of the stack with the last item to the pushed (added) to the stack to be first to be popped (removed)

![stack.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1618143689893/pgog9j1XZ.png)

#### Operations time complexities

Insert at the end: constant 

Insert at the begining: not available

Insert generally: constant 

Remove from end: constant

Remove from begining: not available

Find value: linear

Access value: linear(if the underlying structure is a linked list) constant (if the underlying structure is a array)


%[https://gist.github.com/LPMatrix/c8aa70bda69c862f775433b3457ed793]



### Queue

![queue.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1618143734475/OdTLIE_2G.png)

#### Operations time complexities

Insert at the end: not available 

Insert at the begining: linear (array)

Insert generally: constant (linked list)

Remove from end: not available

Remove from begining: linear (array) constant (linked list)

Fnd value: linear

Access value: linear(linked list) constant (array)


%[https://gist.github.com/LPMatrix/87c3db11de7172f77f321e540fbebfd9]


### Graph
A graph G consists of two types of elements: vertices and edges. Each edge has two endpoints, which belong to the vertex set. We say that the edge connects (or joins) these two vertices.

![graph.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1618143872585/1hPgEG7yE.png)


### Tree
A tree is a collection of entities called nodes. Nodes are connected by edges. Each node contains a value or data, and it may or may not have a child node .

![tree.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1618143805814/XEdOZ0GHj.png)

#### Operations time complexities
Search: linear

Insertion: linear

Deletion: linear


%[https://gist.github.com/LPMatrix/6c02437ef086dafe2a8ff0e4aca71a70]


