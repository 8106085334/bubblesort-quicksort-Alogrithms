# Sorting Algorithms: Bubble Sort and Quick Sort

This repository contains implementations of two common sorting algorithms: **Bubble Sort** and **Quick Sort**. These algorithms are written in Python and are designed to demonstrate the fundamental principles of sorting.

---

## 1. Bubble Sort

### **Description**
Bubble Sort is a simple comparison-based sorting algorithm. It repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The process is repeated until the list is sorted.

### **How It Works**
1. Start with the first two elements.
2. Compare them:
   - If the first element is greater, swap them.
   - Otherwise, leave them as-is.
3. Move to the next pair of adjacent elements.
4. Repeat until the largest element "bubbles" to the end of the list.
5. Continue the process for the remaining unsorted portion of the list.

### **Code Example**
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr

# Example Usage
array = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(array)
print("Sorted array:", array)



2. Quick Sort
Description
Quick Sort is a highly efficient, divide-and-conquer sorting algorithm. It works by selecting a "pivot" element, then partitioning the array into two sub-arrays:

Elements smaller than or equal to the pivot.
Elements larger than the pivot.
These sub-arrays are then sorted recursively.

How It Works
Choose a pivot (e.g., the last element in the array).
Partition the array:
Place elements smaller than the pivot into one sub-array.
Place elements larger than the pivot into another sub-array.
Recursively apply Quick Sort to the sub-arrays.
Combine the sorted sub-arrays and the pivot.
Code Example
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    else:
        pivot = arr[-1]
        smaller = [x for x in arr[:-1] if x <= pivot]
        larger = [x for x in arr[:-1] if x > pivot]
        return quick_sort(smaller) + [pivot] + quick_sort(larger)

# Example Usage
array = [10, 7, 8, 9, 1, 5]
sorted_array = quick_sort(array)
print("Sorted array:", sorted_array)
