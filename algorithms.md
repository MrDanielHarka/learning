# Algorithms

## Q & A

Q1: How does linear search work?\
A1: It starts with the first element and iterates over all, until it finds the one we are looking for. Values do not need to be ordered.

Q2: How does binary search work?\
A2: List must be sorted. 1. Determines middle of list. 2. Compares middle to target element. 3. If it doesn't match, compares value with target. 4. Repeats from step two, until target is found.

Q3: Explain 4 sorting algorithms!\
A3: **Bogo sort** (aka stupid sort) randomly changes values, until list is sorted. **Selection sort** goes one by one, finds the smallest value and puts in to the beginning of the list and starts again. **Insertion sort** is similar to selection sort, but when it checks the list and two numbers are in correct order, then those are skipped and the next one is checked. **Bubble sort** repeatedly swaps adjacent elements if they are in a wrong order, until all elements are in order.

Q4: Why is it good to use recursion when sorting elements?\
A4: Because recursion does the same action over and over again, until requirements met. Like until a list is completely sorted.

## Notes

### General

"A set of steps or instructions for completing a task."

- A clear problem statement is needed. Input and output.

- Correctness is the most important, then the efficiency.

- Running time is measured in Time Complexity.

Important to analyze the Worst Case scenario.

### Linear Search

- Starting on the beginning and going one-by-one to the end.
- Values does not need to be sorted.

### Binary Search

- Search method:
    1. Determines the middle of a sorted list.
    2. Compares the middle position to the target element.
    3. If the element does not match, then check if it's smaller/bigger than the target element.
    4. Repeats from step 2 until target is found.
- Values does need to be sorted.

### Sorting Algorithms

- Bogo sort(aka stupid sort):
    - "The function successively generates permutations of its input until it finds one that is sorted."
    - Two types: Deterministic and Randomized.
    - Higly ineffective.
- Selection sort
    - "Finds the minimum value, swaps it with the value in the first position, and repeats these steps for the remainder of the list."
    - Simple and has performance advantages, but inefficient on large lists. Performs worse than similar insertion sort.
- Insertion sort
    - Simple sorting algorithm.
    - Similar to selection sort, but does not sort all the values one by one. If two values that are in the correct order, then those are skipped and the algorithm checks the new one.
- Bubble sort
    - Simplest sorting algorithm.
    - Repeatedly swaps the adjacent elements if they are in the wrong order.
- Quick and Merge sort
    - These sort types are Divide and Conquer algorithms.
    - These divide up the arrays and then sort them, based on their methods.

### Recursion

