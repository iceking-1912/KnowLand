---
tags:
  - Data_Structures_and_Algorithms
parent:
  - "[[SE SEM 1]]"
Purpose:
  - Knowledge
---

# **Unit III: Searching and Sorting**

## Searching Techniques: Linear Search (Variants), Binary Search,
## Sorting Algorithms: Internal vs. External Sorting Methods
## Sorting Concepts: Order, Stability, Efficiency, Number of Passes
## Comparison-Based Sorting: Bubble Sort, Insertion Sort, Selection Sort, Quick Sort, Shell Sort
## Non-Comparison Sorting: Radix Sort, Counting Sort, Bucket Sort
## Sorting Analysis: Comparing Complexity of Different Sorting Algorithms


## Comparison-Based Sorting:
### Bubble Sort, Insertion Sort, Selection Sort, Quick Sort, Shell Sort

Here's a brief overview of each sorting algorithm:

### Bubble Sort

* **Time Complexity:** O(n^2)
* **Space Complexity:** O(1) (in-place)
* **Description:** Bubble sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.
* **Example:**
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n-1):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                # Swap elements
                arr[j], arr[j+1] = arr[j+1], arr[j]

arr1 = [10,621,90,20,210,30,520,40,50,201,60]
bubble_sort(arr1)
print(arr1)
```
### Insertion Sort

* **Time Complexity:** O(n^2)
* **Space Complexity:** O(1) (in-place)
* **Description:** Insertion sort is a simple sorting algorithm that builds the final sorted array one item at a time, inserting each item into its proper position within the already-sorted part of the array.
* **Example:**
```python
def insertion_sort(arr):
    n = len(arr)
    for i in range(1, n):
        key = arr[i]
        j = i-1
        while j >= 0 and arr[j] > key:
            # Shift elements to the right
            arr[j+1] = arr[j]
            j -= 1
        arr[j+1] = key

arr1 = [10,621,90,20,210,30,520,40,50,201,60]
insertion_sort(arr1)
print(arr1)
```
### Selection Sort

* **Time Complexity:** O(n^2)
* **Space Complexity:** O(1) (in-place)
* **Description:** Selection sort is a simple sorting algorithm that repeatedly selects the minimum element from the unsorted part of the array and swaps it with the first unsorted element.
* **Example:**
```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n-1):
        min_idx = i
        for j in range(i+1, n):
            if arr[j] < arr[min_idx]:
                # Swap elements
                min_idx = j
        # Swap minimum element with first unsorted element
        arr[i], arr[min_idx] = arr[min_idx], arr[i]
arr1 = [10,621,90,20,210,30,520,40,50,201,60]
selection_sort(arr1)
print(arr1)
```
### Quick Sort

* **Time Complexity:** O(n log n) on average, O(n^2) in the worst case
* **Space Complexity:** O(log n) for efficiency (uses recursion or a divide-and-conquer approach)
* **Description:** Quick sort is a divide-and-conquer algorithm that selects a pivot element and partitions the array around it.
* **Example:**
```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    # Select pivot element (e.g., median of first, middle, and last elements)
    pivot = sorted([arr[0], arr[len(arr)//2], arr[-1]])[1]
    less_than_pivot = [x for x in arr if x < pivot]
    greater_than_pivot = [x for x in arr if x > pivot]
    return quick_sort(less_than_pivot) + [pivot] + quick_sort(greater_than_pivot)
arr1 = [10,621,90,20,210,30,520,40,50,201,60]
print(quick_sort(arr1))
```
### Shell Sort

* **Time Complexity:** O(n log n) on average, O(n^2) in the worst case
* **Space Complexity:** O(1) (in-place)
* **Description:** Shell sort is a comparison-based sorting algorithm that uses a "shell" or series of smaller steps to move elements towards their final positions.
* **Example:**
```python
def shell_sort(arr):
    n = len(arr)
    gap = n//2
    while gap > 0:
        for i in range(gap, n):
            temp = arr[i]
            j = i
            while j >= gap and arr[j-gap] > temp:
                # Shift elements to the right
                arr[j] = arr[j-gap]
                j -= gap
            arr[j] = temp
        gap //= 2
arr1 = [10,621,90,20,210,30,520,40,50,201,60]
shell_sort(arr1)
print(arr1)
```

## Non-Comparison Sorting:
## Radix Sort, Counting Sort, Bucket Sort

Here's a brief overview of each sorting algorithm:

### Radix Sort

* **Time Complexity:** O(nk)
* **Space Complexity:** O(n + k)
* **Description:** Radix sort is a non-comparison sorting algorithm that sorts integers or strings by considering the digits (or characters) of each number individually.
* **Example:**
```python
def radix_sort(arr):
    RADIX = 10
    placement = 1

    max_digit = max(arr)
    while placement < max_digit:
        buckets = [list() for _ in range(RADIX)]
        for i in arr:
            tmp = int((i / placement) % RADIX)
            buckets[tmp].append(i)
        a = 0
        for b in range(RADIX):
            buck = buckets[b]
            for i in buck:
                arr[a] = i
                a += 1
        placement *= RADIX

arr1 = [10,621,90,20,210,30,520,40,50,201,60]
radix_sort(arr1)
print(arr1)
```
### Counting Sort

* **Time Complexity:** O(n + k)
* **Space Complexity:** O(n + k)
* **Description:** Counting sort is a non-comparison sorting algorithm that sorts integers by counting the number of occurrences of each unique element.
* **Example:**
```python
def counting_sort(arr):
    max_val = max(arr)
    count = [0] * (max_val + 1)
    for num in arr:
        count[num] += 1
    sorted_arr = []
    for i, cnt in enumerate(count):
        sorted_arr.extend([i] * cnt)
    return sorted_arr

arr1 = [10,621,90,20,210,30,520,40,50,201,60]
counting_sort(arr1)
print(arr1)
```
### Bucket Sort

* **Time Complexity:** O(nk log n)
* **Space Complexity:** O(n + k)
* **Description:** Bucket sort is a non-comparison sorting algorithm that sorts elements by distributing them into a number of buckets, and then collecting the elements from the buckets in order.
* **Example:**
```python
def bucket_sort(arr):
    min_val = min(arr)
    max_val = max(arr)
    size = len(arr)

    # Create empty buckets
    bucket_size = 10
    buckets = [[] for _ in range(size)]
    for num in arr:
        index = int((num - min_val) / (max_val - min_val) * bucket_size)
        if index == size:
            index -= 1
        buckets[index].append(num)

    # Sort each bucket individually
    sorted_buckets = [sorted(bucket) for bucket in buckets]

    # Collect elements from the buckets into a single array
    sorted_arr = []
    for bucket in sorted_buckets:
        sorted_arr.extend(bucket)
    return sorted_arr

arr1 = [10,621,90,20,210,30,520,40,50,201,60]
print(bucket_sort(arr1))
```


