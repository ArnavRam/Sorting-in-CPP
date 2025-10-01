# Experiment 21 - To study and implement sorting techniques

---

## Aim
- To study and implement fundamental sorting algorithms in C++, including **Bubble Sort**, **Selection Sort**, and **Quick Sort**.
- To compare their efficiency, time complexity, and respective use cases.

---

## Tools Used
- Visual Studio Code
- MinGW-w64 with g++ Compiler

---

## Theory
**Sorting** is the process of arranging a collection of data into a specific order (e.g., ascending or descending). Efficient sorting is crucial for optimizing searching algorithms and for organizing data for clear presentation.

- **Bubble Sort:** This is a simple comparison-based algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted.
- **Selection Sort:** This algorithm divides the input list into two parts: a sorted sublist and an unsorted sublist. It repeatedly finds the minimum element from the unsorted sublist and moves it to the end of the sorted sublist.
- **Quick Sort:** This is a highly efficient "divide and conquer" algorithm. It works by selecting a 'pivot' element from the array and partitioning the other elements into two sub-arrays, according to whether they are less than or greater than the pivot. The sub-arrays are then sorted recursively.

| Algorithm | Best Case | Worst Case | Average Case | Space Complexity |
| :--- | :---: | :---: | :---: | :---: |
| **Bubble Sort** | O(n) | O(n²) | O(n²) | O(1) |
| **Selection Sort** | O(n²) | O(n²) | O(n²) | O(1) |
| **Quick Sort** | O(n log n) | O(n²) | O(n log n) | O(log n) |

---

## Algorithm / Logic

### Program 1: Bubble Sort
1.  **Start**
2.  Get an unsorted array from the user.
3.  Use an outer loop that iterates from `i = 0` to `n-1`.
4.  Use an inner loop that iterates from `j = 0` to `n-i-2`.
5.  Inside the inner loop, check if `arr[j] > arr[j+1]`.
6.  If true, swap the two elements.
7.  After the loops complete, the array will be sorted. Print the sorted array.
8.  **End**

### Program 2: Selection Sort
1.  **Start**
2.  Get an unsorted array from the user.
3.  Use an outer loop that iterates from `i = 0` to `n-1`.
4.  Assume the first element of the unsorted part is the minimum: `minIndex = i`.
5.  Use an inner loop to scan the rest of the unsorted part (`j = i+1` to `n-1`).
6.  If `arr[j] < arr[minIndex]`, update `minIndex = j`.
7.  After the inner loop, swap `arr[i]` with `arr[minIndex]`.
8.  Print the sorted array.
9.  **End**

### Program 3: Quick Sort
1.  **Start**
2.  Get an unsorted array from the user.
3.  Write a `partition()` function that takes an array, a `low` index, and a `high` index. It selects a pivot, places it at its correct sorted position, and partitions the other elements around it.
4.  Write a recursive `quickSort()` function.
5.  **Base Case:** If `low >= high`, return.
6.  **Recursive Step:** Call `partition()` to get the pivot's index, `pi`. Then recursively call `quickSort()` for the left sub-array (`low` to `pi-1`) and the right sub-array (`pi+1` to `high`).
7.  Call `quickSort()` from `main()` with the initial array bounds.
8.  Print the sorted array.
9.  **End**

---

## Conclusion
This experiment provided a practical implementation of three key sorting algorithms. **Bubble Sort** and **Selection Sort** are simple to understand but are inefficient for large datasets with a time complexity of O(n²). **Quick Sort**, a divide-and-conquer algorithm, is significantly more efficient for general-purpose sorting with an average time complexity of O(n log n). Understanding the trade-offs between these algorithms in terms of performance and implementation complexity is essential for effective data organization and algorithm design.
