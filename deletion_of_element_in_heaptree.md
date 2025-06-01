# Heap Tree Deletion in C
## Aim:
To write a C program that deletes a specified element from a Heap Tree (represented as an array) and maintains the heap property after deletion.

## Problem Description:
Given a Max-Heap or Min-Heap represented as an array, this program removes a specific element, re-structures the heap accordingly, and prints the updated heap.

### How it Works:
Search for the element in the array.

Swap it with the last element in the heap.

Reduce the heap size.

Heapify the array again to maintain the heap property.

### Input Format:
First line: An integer n (number of elements in the heap).

Second line: n integers representing the heap.

Third line: The element to be deleted.

### Output Format:
Prints the heap array after deleting the specified element.

## Program Code:
```
void deleteRoot(int array[], int num)
{
  // type your code here
  
  int i;
  for (i = 0; i < size; i++)
  {
    if (array[i] == num)
      break;
  }

  if (i == size)
  {
    printf("Element not found in heap\n");
    return;
  }

  // Swap with the last element and reduce heap size
  swap(&array[i], &array[size - 1]);
  size--;

  // Re-heapify the array
  for (int i = size / 2 - 1; i >= 0; i--)
  {
    heapify(array, size, i);
  }
}
```

## Output:
![alt text](image-3.png)
## Conclusion:
This program demonstrates how to delete an element from a heap and re-establish the heap structure using the heapify process. It's useful in priority queues, heap sort, and scheduling algorithms.