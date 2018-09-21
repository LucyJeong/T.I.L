# Insertion Sort
![InsertionSort](https://upload.wikimedia.org/wikipedia/commons/9/9c/Insertion-sort-example.gif)
- build your sorted array in place, shifting elements out of the way if necessary to make room as you go.
- 삽입 정렬은 두 번째 자료부터 시작하여 그 앞(왼쪽)의 자료들과 비교하여 삽입할 위치를 지정한 후 자료를 뒤로 옮기고 지정한 자리에 자료를 삽입하여 정렬하는 알고리즘이다.
- 정렬한 부분과 정렬하지 않은 부분을 나눈 후 정렬할 대상인 대상을 정렬하지 않은 부분에서 차례대로 꺼내 정렬한 부분의 요소들과 차례대로 비교를 하면서 자신이 삽입될 인덱스를 찾는다.
- _in pseudocode_:
  - Call the first element of the array "sorted."
  - Repeat until all elements are sorted:
    - Look at the next unsorted element. Insert into the "sorted" portion by shifting the requisite number of elements.
- Worst-case scenario : The array is in reverse order; we have to shift each of the _n_ elements _n_ positions each time we make an Insertion.
- Best-case scenario : The array is already perfectly sorted, and we simply keep moving the line between "unsorted" and "sorted" as we examine each element.

## Code

```swift
func insertionSort(_ array: [Int]) -> [Int] {
    var arr = array
    for x in 1..<arr.count {
        var y = x
        while y > 0 && arr[y] < arr[y - 1] {
            swap(&arr[y - 1], &arr[y])
            y -= 1
        }
    }
    return arr
}
```

---
refer to
- [CS50](https://youtu.be/O0VbBkUvriI)
- [[알고리즘] 삽입 정렬(insertion sort)이란](https://gmlwjd9405.github.io/2018/05/06/algorithm-insertion-sort.html)
