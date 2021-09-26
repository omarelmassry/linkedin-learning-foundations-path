- [Data types and data structures](#data-types-and-data-structures)
  - [Data types:](#data-types)
    - [Primitive types:](#primitive-types)
    - [Referenced types:](#referenced-types)
  - [Data Structure](#data-structure)
    - [Arrays:](#arrays)
    - [Linked lists](#linked-lists)
    - [Stacks and Queues](#stacks-and-queues)
      - [Stacks](#stacks)
      - [Queues](#queues)
      - [Stacks and queues pros and cons](#stacks-and-queues-pros-and-cons)
    - [Hash-Based Data Structures](#hash-based-data-structures)
      - [Associative Arrays](#associative-arrays)
      - [Hashing functions](#hashing-functions)
      - [Hash tables](#hash-tables)
      - [Pros and Cons of hash-based structures](#pros-and-cons-of-hash-based-structures)
    - [Trees and Graphs](#trees-and-graphs)
      - [Sets](#sets)

# Data types and data structures

To store data, data types were created.

> Data type: is an attribute of data that describes the values it can have and how it can be used

<br/>

---

<br/>

## Data types:

### Primitive types:

- **Numbers** : int, float, double, long ...etc
- **Booleans**
- **Characters**
- ...etc

primitive data types are stored in memory as bits (8, 16, 32)bits, this depends on the language used.

### Referenced types:

In **primitive** types we know exactly how much memory is allocated for each value but in **referenced** types we don't know so **pointers** are used.
Some languages handel pointers and other you have to set them yourself

- **String**: a sequence of characters
- **Data structures**

<br/>

---

<br/>

## Data Structure

Data structures are containers that allow us to store a groupe of other data types

> a data structure is a collection with a defined way to access and store items

### Arrays:

> An array is a collection of elements where each item is identified by an index or a key

- Indices are essential part of arrays.
- Arrays provide organization, storage and access to data.

- **Multidimensional Arrays** are type of arrays that have more than one row (array of arrays with same length). It also uses indices with 2 numbers to identify column and row numbers
- **Jagged Arrays** are similar to multidimensional arrays but each row is different length (array of arrays with different length). Jagged arrays are better when the data is not in even shape, it saves memory and better optimized in this case more than 2D arrays (2D arrays size is fixed)
- Some languages allow for resizable arrays and some not (dynamic or mutable)
- Add, push, splice, remove and pop are some methods used with dynamic arrays in different languages
- Adding an item to non-mutable array can happen in tow ways:

  - If the array is big enough: the language will shuffle all of the items down and add the new one.
  - If not, it will copy all the contents into a new basic array into their new places and simply copy the new item over with it.

  This can have major performance repercussions, depending on how many items you are dealing with and the way the language handles its data structures.

- You can search arrays by checking every item in it and if found return the index of it but this a linear algorithm that takes time and impact performance. This can be a lot easier if the array is sorted.
- You can sort arrays in different ways but this is a computationally expensive and should be used only if needed
- insertion in a small array has **O(1)** complexity while a big array might be **O(n)**
- accessing, updating or deleting an item by its index is always **O(1)**

<br/>

---

<br/>

> Big O Notation is used to describe the performance or complexity of an algorithm.

<br/>

---

<br/>

### Linked lists

- Similar to an array, a linked list is a **linear** data structure.
- The elements of a linked list are not stored at contiguous locations.
- Elements in the list are linked together by **pointers**
- Each group of data in the list is called a **node**
- A node contains data and a pointer to the next node.
- The first node in a linked list is called the head of the list. and through we can access every other item in the list by following the pointers.
- you can't access a node in the list without accessing it's previous node.
- last node of the list has a nullish pointer and that's how we know it's the last node.
- we can add, access, delete and search for items in a linked list.
- adding a node is easier when added to first the first or end of the list, We can also insert into any place within the list, but you always have to update the pointer of the added and adjacent nodes.
- accessing , searching , updating and deleting an item is done in similar way by following the pointers of each node until we find the wanted node
- linked list can be singly or doubly, singly list has pointers to the next nodes only and not the previous nodes; doubly lists have pointers to the previous and next nodes.
- time complexity of operation made on the linked list is usually **O(n)**. thats because we have to access all items of the list to perform the action needed. unless the action is performed on the first node its complexity is always **O(1)**

<br/>

---

<br/>

### Stacks and Queues

#### Stacks

- A stack is an ordered series of objects just like a list, but its intended use is slightly different.We push objectives onto the stack and pop objects off of it.
- Stacks follow a last in, first out, or LIFO policy.
- last item on the stack will be the first item removed from the stack. the first item pushed on the stack will be the last item popped off of the stack.
- This makes stack especially useful for keeping track of state or the order of when things have occurred.

#### Queues

- Queues represent a series of ordered objects. it is designed to have elements inserted at the end of the queue and elements removed from the beginning of the queue.
- Queues follow a FIFO or first in, first out policy
- When we add an item to the queue, we say we enqueue the item,
- Enqueue: when item is added to the queue.
- Dequeue: when item is removed from the queue.
- Priority queue: which dequeue items with highest priority first. not as FIFO order
- if tow items has the same priority they dequeue as their FIFO order.
- D-E-Q-U-E-K: (pronounced DEK) is a double ended queue, which is like normal queues but you can add or remove from either ends.
- it's not possible to remove items from eny where else except the end in DEQUEKs

#### Stacks and queues pros and cons

- Stacks are great for programs where you need to reverse things.
- Stacks are also good for keeping track of state as things are pushed on and popped off the stacks.
- Pushing, peeking and popping takes very little time, in fact, constant time because stacks often have a linked list implementation or dynamic array implementation.
- Stacks and queues are cant have indexes for items and they are very bad for searching.
- Stacks really just help you keep state. A stack only shows its advantages when you need to use it in a manner where the last item in is the first item out.
- Queues are similar to stacks in that they only show their advantages when you're using first in, first out or FIFO functionality.
- Enqueuing to the back and dequeuing from the front is also very quick and takes constant time because the queue has a doubly-linked list implementation.
- You can access items from the middle of the queue by using priority queue but that is not their intended use.

<br/>

---

<br/>

### Hash-Based Data Structures

#### Associative Arrays

- an **associative array** is a collection of key-value pairs.
- Each key-value pair always stays **together**, and every key in an associative array must be **unique**.
- Just like indices are unique in regular arrays, keys must be unique in associative arrays.
- We don't use the word index with associative arrays because we often _don't worry about the order_ of the key-value pairs. The key is just the way we access the value in the pair.
- Most associative arrays are implemented using a **hash table**.

#### Hashing functions

- hashing is a way of taking some raw data and mixing it together to form a smaller single piece of data.
- almost without exception hash functions are not reversible.
- When two different inputs map to the same hash value or produce the same hash value when thrown into a hash function, we call it a collision.
- with the hash function, the same input will always produce the same output.

#### Hash tables

- A hash table is a typical way of implementing an associative array. When a hash table's created internally, it's really an array-based data structure where we add extra functionality to get us past the limitations of an array.
- We use the term bucket to describe each entry or place for a key-value pair to go in a hash table.
- We'll never add just a key or just a value. We'll always add a pair.
- hashed keys is not used as indexes, it's used to calculate and index by making a hash value smaller but in a way that's related to the current size of the hash table. Why do this? It helps us evenly distribute the elements across the buckets we have.
- Essentially we take the hash value, divide it by the size of the hash table, or the number of buckets in the table and use the remainder as the index for where we'll store the value for a given key.
- There is no linear search and no traversing through a series of elements. We just go straight to the element with the key.
- sometimes two keys can have the same hash which means the values of those keys could live at a single index. We call this a collision.
- Instead of having a single value in that slot, we can create a linked list that holds both values. We call this separate chaining and it does affect performance.

#### Pros and Cons of hash-based structures

- Data and hash maps is stored in such a way that searching is much faster than many other data structures.
- hash maps do take up more space.
- Insertion and deletion is also quick.
- lookup, insertion and deletion all take **O(1)** or constant time.
- in a situation where you have a lot of key-value pairs or volatile data, these beat arrays hands down.
- There's no real sorting with hash-based data structures.

<br/>

---

<br/>

### Trees and Graphs

#### Sets

- Another way we can structure our data is with a set. Similar to linked lists, hash maps, and other data structures,
- A set is an abstract data type. It's an idea that can be implemented in many different ways.
- A set is a collection of unique items. The order of these items doesn't matter, but none of the elements are duplicated.
- in sets we don't care about the order of the elements, and often, we don't even want to retrieve a piece of data. That's why we don't have an index, or key, or anything specific to look up the value. Here, we care about membership.
- With sets, we are usually testing if a piece of data is a member in that set.
- behind the scenes, sets are actually using the same idea of hash tables most of the time.
- Instead of hashing a key to store a separate value object, when you're using a set, the key is the value.
- a set works by taking an object, hashing it, and then using the generated index to store the object itself.
