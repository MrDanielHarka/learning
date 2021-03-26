# Data Structures

## Q & A

Q1: ?\
A1: 

Q2: ?\
A2: 

Q3: ?\
A3: 

Q4: ?\
A4: 

Q5: ?\
A5: 

Q6: ?\
A6: 

Q7: ?\
A7: 

Q8: ?\
A8: 

## Notes

21.03.26.

### General

"It is a data organization, management, and storage format that enables efficient access and modification. A data structure is a collection of data values, the relationships among them, and the functions or operations that can be applied to the data."

Different data structures are good for different types of applications, for different use cases and tasks.

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

### Arrays

- List of elements (values and/or variables).

- Arrays may contain different type of elements, depends on the language.

- **Parallel arrays** are two or more arrays that:
	- Contain the **same number of elements**.
	- Have **corresponding values** in the same position.
- Usually has 3 attributes: name, type and size.
- The type tells us what type of information is stored **within** the array. Can only store that type.
- The size is an integer, which represents the **total amount of elements** stored in the array.