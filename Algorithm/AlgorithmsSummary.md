# Algorithms Summary

Algorithm Name | Basic Concept | O | Ω
-------------- | ------------- | - | -
[Selection sort](/Algorithm/InsertionSort.md) | Find the **smallest** unsorted element in an array and swap it with the **first** unsorted element of that array | n^2 | n^2
[Bubble Sort](/Algorithm/BubbleSort.md) | Swap **adjacent pairs** of elements if they are out of order, effectively "bubbling" larger elements to the right and smaller ones to the left | n^2 | n
Insertion Sort | Proceed once through the array form left-to-right, **shifting** elements as necessary to insert each element into its correct place. | n^2 | n
Merge Sort | **Split** the full array into subarrays, then **merge** those subarrays back together in the correct order. | n log n | n logn
Liner Search | **Iterate** across the array from left-to-right, trying to find the target element. | n | 1
Binary Search | Given a _sorted_ array, **divide and conquer** by systematically eliminating half of the remaining elements in the serach for the target element. | log n | 1

## Image
- SelectionSort

![SelectionSort](https://cdn-images-1.medium.com/max/1600/1*to7gYwi5_bkZhx-1kSB0Lg.gif)

- bubbleSort

![bubble sort from wiki](https://upload.wikimedia.org/wikipedia/commons/c/c8/Bubble-sort-example-300px.gif)

- [Sorting Algorithms Animations](https://www.toptal.com/developers/sorting-algorithms)
---
refer to
- [CS50](https://youtu.be/ktWL3nN38ZA)
