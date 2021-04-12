# Data Structures

## Q & A

Q1: What's the Big(O) notation used for?\
A1: It is used for measuring efficiency. Four data gives us the "score" of the efficinecy. The speed of accessing, searching, inserting and deleting elements.

Q2: Why are there different data structures?\
A2: Different data structures are suitable for different use cases.

Q3: What's an array?\
A3: Random Access Data Structure. An array is a list, contains elements, which may or may not be of different types, depending on the programming language. Usually has a fixed length, but this also depends on the language. Elements can be accessed individually.

Q4: What's an arrayList?\
A4: Random Access Data Structure. Similar to arrays, but these have dynamic size and does not have a fixed length. Elements can be accessed individually.

Q5: What's the difference between an array and an arrayList?\
A5: An array usually has a fixed size, while the arrayList is a growing array, which has a dynamic size.

Q6: What's a stack?\
A6: Sequential Access Data Structure. LIFO Principle. Elements are dependent on eachother and can only be accessed through other elements. Top elements need to be removed, before we can access the lower ones.

Q7: What's a queue?\
A7: Sequential Access Data Structure. FIFO Principle. Elements are dependent on eachother and can only be accessed through other elements. We add to the back (Tail) and remove from the front (Head).

Q8: What's the difference between a stack and a queue?\
A8: With a stack we add elements on eachother and each can be only accessed after the ones over are removed, while with queue we can only add new items to the tail and remove/access at head.

Q9: What's the difference between a linked list and a doubly-linked list?\
A9: Linked list items are only referencing/linked to one other node (list item) and go in one direction, while doubly-linked list items have reference points to two other **nodes**, the one before and one after.

Q10: Why is it good to use maps?\
Q11: 

## Notes

### General

"It is a data organization, management, and storage format that enables efficient access and modification. A data structure is a collection of data values, the relationships among them, and the functions or operations that can be applied to the data."

Different data structures are good for different types of applications, use cases and tasks.

### Big(O) notation

- The industry standard for **Measuring Efficiency**.

- Most common functions from a data scructure
	- Accessing elements
	- Searching for an element
	- Inserting an element
	- Deleting an element

- Used to "score" a data scructure based on 4 criteria. **Accessing**, **searching**, **inserting** and **deleting**.

- The report card tells us these measurements. Tells us what the data structure is good and bad at.

- Time Complexity Equations helps representing the efficiency amongst different data structures.
	- Always uses the **worst-case scenario** when judging data structures.

- Syntax for the TCE includes BigO then a set of parantheses for the function.

- "Modeled by an equation which takes in size of data-set **(n)** and returns **number of operations** needed to be performed by the computer to complete that task."

- 6 most common TCEs
	- O(1)
		- Fastest completion time.
		- No matter the size of data set, task will be completed in a single instruction.
	- O(log n)
		- Fast completion time.
		- Gets more efficient as the size of data set increases.
	- O(n)
		- Decent completion time.
		- By every element added to data set the amount of instruction needed to complete that function will increase by the same amount.
	- O(n log n)
		- Relatively bad efficiency.
		- Gets less efficient as the size of data set increases.
	- O(n<sup>2</sup>) and O(2<sup>n</sup>)
		- Very bad efficiency.
		- Exponentially less efficient as the size of data set increases. The larger the data set, the less efficient it gets.
	- These TCEs are **NOT** the only ones to use when deciding which data structure to use. Some provide **other functionality** that makes them super  useful.

### Array

- List of elements (values and/or variables).
- Arrays may contain different type of elements, depends on the language.
- Random Access Data Structure: Can be accessed independently, no matter the other elements.
- Usually has 3 attributes: name, type and size.
- The type tells us what type of information is stored **within** the array. Can only store that type.
- The size is an integer, which represents the **total amount of elements** stored in the array. **Size can not be changed!**

- **Parallel arrays** are two or more arrays that:
	- Contain the **same number of elements**.
	- Have **corresponding values** in the same position.
- Contents can be defined upon creation or can be added later.
- Array items have numerical indexes. Referencing by **array's name** and **index #**.
- Indexes are also used for **replacing items**.
- Big(O) - Accessing O(1), Searching: O(n), Inserting: O(n), Deleting: O(n).

### ArrayList

- It's like a **growing array**. Similar to arrays, but size can change. Has **Dynamic Size**.
- ArrayLists does not support element declaration upon creation.
- Methods:
	- Add: Add(Object) or Add(Object, Index)
	- Remove: Remove(Object) or Remove(Index)
	- Get: Get(Index) Same as referencing an index.
	- Set: Set(Index, Object) Replaces object at index.
	- Clear: Clear() Deletes the entire ArrayList.
	- toArray: toAray() Converts arrayList to Array.
- Big(O) - Accessing: O(1), Searching: O(n), Inserting: O(n), Deleting: O(n).

### Stack

- Sequential Access Data Structure: Can only be accessed in a particular order.
	- Each element is **dependent** on the others.
	- May only be obtainable **throught** those other elements.
- LIFO Principle: Last In First Out.
- Methods:
	- Push: Push(Object) Pushes an object on the top.
	- Pop: Pop() Removes an object from the top.
	- Peek: Peek() Shows the very top object.
	- Contains: Contains(Object) Shows if "Object" is in the stack.
- Stacks are used in **Recursion**.
- Big(O) - Accessing: O(n), Searching: O(n), Inserting: O(1), Deleting: O(1).

### Queue

- Sequential Access Data Structure: Can only be accessed in a particular order.
	- Each element is **dependent** on the others.
	- May only be obtainable **throught** those other elements.
- FIFO Principle: First In First Out
- We add to the back (Tail) and remove from the front (Head).
- Methods:
	- Enqueue: Enqueue(Object) Adds element to the **tail** of Queue. This way the size of the queue also increases.
	- Dequeue: Dequeue(Object) Removes element from **head**.
	- Peek: Peek() Shows the very front object (in head).
	- Contains: Contains(Object) Shows if "Object" is in the queue.
- Big(O) - Accessing: O(n), Searching: O(n), Inserting: O(1), Deleting: O(1).

### Linked List

- Sequential Access Linear Data Structure: Every element is a separate object called a **Node**, which has 2 parts:
	- The **data**
	- The **reference** (or pointer) which points to the next **Node** in the list.
- Node:
	- Data: **Strings**, **Integers** and **Booleans**.
	- Reference/pointer: The next Node in the Linked List.
- Visualization:
	- Head Node: Data + Ref. to 2nd Node.
	- 2nd Node: Data + Ref. to 3rd Node.
	- 3rd Node: Data + Ref. to n-th Node.
	- N-th Node: Data + Ref. to Tail Node.
	- Tail Node: Data + Ref. "null".
- Adding and removing Nodes.
	- Head:
		- Adding: We can just add a new Node to the start and link it to the 2nd one. Then it will be the first one.
		- Removing: When we take the first Node and point it to "null", then it will be cut off from the others and will be exiled from the Linked List. 2nd will now be the Head(1st).
	- Middle:
		- Adding: New Node's pointer will point to the next one, and the one before should point to the new Node.
		- Removing: Point the Node which is before to the Node which is after the Node, that we would like to remove. The actual Node should be pointed to "null".
	- Tail:
		- Adding: We make a new Node, point it to "null" and point the former tail Node, to the new one.
		- Removing: We point the previous Node and the one we would like to remove to "null".
- Big(O) - Accessing: O(n), Searching: O(n), Inserting: O(n) or O(1), Deleting: O(n) or O(1).

### Doubly-Linked List

- Similar to Linked Lists, but able to traverse both **forwards** and **backwards** using pointers.
- It has 3 parts:
	- The **data**
	- The **reference** (or pointer) which points to the next **Node** in the list.
	- The **reference** (or pointer) which points to the previous **Node** in the list.
- Big(O) - Accessing: O(n), Searching: O(n), Inserting: O(n) or O(1), Deleting: O(n) or O(1).

### Map

Also called an associative array. It's an array that allows indexing using any data type. It associates a **key** with a **value**, where each key has no more than one value associated with it.

Example: A dictionary is a map that associates words with definitions. If we look in the dictionary for the word (**key**), we can find the definition (**value**). Sometimes maps are called **dictionaries** for this reason.

Two main variants:
- Ordered Maps (red-black tree) - easily iterated in meaningful order (alphabetical, etc.). Better for listing records by name.
- Unordered Maps (hash table) - better average-case performance for random access. Performs better for finding a user profile by username.

### Set

Used to indentify membership. Similar to map, but just a single element (rather than a key/value pair). Can be ordered or unordered.

- Can only contain a value once.
- Can be ordered or unordered.

### Mutlimaps and Multisets

- Multimap: Maps a single key to multiple values.
- Multiset: Keeps a count of how many of a particular element have been added.

Infrequently used, because unwieldy and complex nature.