# Algorithms

## Notes

21.03.27.

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

