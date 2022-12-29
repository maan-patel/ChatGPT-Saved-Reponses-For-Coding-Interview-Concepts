There are many different sorting algorithms that can be used to sort a list of items. Some common sorting algorithms include:

# Bubble sort:
 This is a simple sorting algorithm that repeatedly iterates through the list, compares adjacent elements, and swaps them if they are in the wrong order. It has a time complexity of O(n^2) in the worst case.

```python
def bubble_sort(items):
  n = len(items)
  for i in range(n - 1):
    for j in range(n - 1 - i):
      if items[j] > items[j + 1]:
        items[j], items[j + 1] = items[j + 1], items[j]
  return items

print(bubble_sort([5, 2, 4, 1, 3])) # Output: [1, 2, 3, 4, 5]
```

# Selection sort:
 This algorithm repeatedly selects the minimum element from the unsorted portion of the list and adds it to the sorted portion. It has a time complexity of O(n^2) in the worst case.
```python
def selection_sort(items):
  n = len(items)
  for i in range(n):
    min_index = i
    for j in range(i + 1, n):
      if items[j] < items[min_index]:
        min_index = j
    items[i], items[min_index] = items[min_index], items[i]
  return items

print(selection_sort([5, 2, 4, 1, 3])) # Output: [1, 2, 3, 4, 5]
```

# Insertion sort: 
This algorithm iterates through the list, taking one element at a time and inserting it into the correct position in the sorted portion of the list. It has a time complexity of O(n^2) in the worst case.
```python
def insertion_sort(items):
  n = len(items)
  for i in range(1, n):
    j = i
    while j > 0 and items[j] < items[j - 1]:
      items[j], items[j - 1] = items[j - 1], items[j]
      j -= 1
  return items

print(insertion_sort([5, 2, 4, 1, 3])) # Output: [1, 2, 3, 4, 5]
```

# Merge sort
 is a divide and conquer algorithm that recursively divides the list into smaller sublists until it reaches lists of size 1, and then merges them back together in a sorted manner. It has a time complexity of O(n log n) in the worst case.

Here is how the algorithm works:If the list has a length of 1 or 0, it is already sorted, so it is returned as is.The list is divided into two equal-sized sublists.The sublists are sorted recursively using the merge sort algorithm.The sorted sublists are merged back together in a sorted manner by comparing the first elements of each sublist and adding the smaller element to the result list. This process is repeated until all elements have been added to the result list.

Here is the complete code for the merge sort algorithm in Python:
```python
def merge_sort(items):
  if len(items) &lt;= 1:
    return items

  mid = len(items) // 2
  left = merge_sort(items[:mid])
  right = merge_sort(items[mid:])

  sorted_items = []
  left_index = 0
  right_index = 0
  while left_index &lt; len(left) and right_index &lt; len(right):
    if left[left_index] &lt; right[right_index]:
      sorted_items.append(left[left_index])
      left_index += 1
    else:
      sorted_items.append(right[right_index])
      right_index += 1
  # Add the remaining elements, if any
  sorted_items.extend(left[left_index:])
  sorted_items.extend(right[right_index:])

  return sorted_items

print(merge_sort([5, 2, 4, 1, 3])) # Output: [1, 2, 3, 4, 5]
```

In this example, the ```merge_sort``` function first checks if the list has a length of 1 or 0. If it does, the list is returned as is. Otherwise, the list is divided into two equal-sized sublists using slicing. The ```merge_sort``` function is then called recursively on each sublist. Once the sublists are sorted, they are merged back together in a sorted manner using the ```sorted_items``` list. The elements from each sublist are compared and the smaller element is added to the ```sorted_items``` list. This process is repeated until all elements have been added to the ```sorted_items``` list. The final ```sorted_items``` list is returned as the result.





# Quick sort:
 This is another divide and conquer algorithm that selects a pivot element and partitions the list into two sublists based on whether the elements are less than or greater than the pivot. It then recursively sorts the sublists. It has a time complexity of O(n log n) in the average case and O(n^2) in the worst case.
```python
def quick_sort(items, start, end):
  if start >= end:
    return

  pivot_index = partition(items, start, end)
  quick_sort(items, start, pivot_index - 1)
  quick_sort(items, pivot_index + 1, end)

def partition(items, start, end):
  pivot_index = end
  pivot = items[pivot_index]
  i = start
  for j in range(start, end):
    if items[j] < pivot:
      items[i], items[j] = items[j], items[i]
      i += 1
  items[i], items[pivot_index] = items[pivot_index], items[i]
  return i

items = [5, 2, 4, 1, 3]
quick_sort(items, 0, len(items) - 1)
print(items) # Output: [1, 2, 3, 4, 5]
```