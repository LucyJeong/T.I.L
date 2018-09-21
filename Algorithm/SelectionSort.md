# Selection Sort
![SelectionSort](https://cdn-images-1.medium.com/max/1600/1*to7gYwi5_bkZhx-1kSB0Lg.gif)
- 정렬되지 않은 가장 작은 요소를 찾아내서 정렬된 리스트의 맨 끝에 추가하는 정렬 알고리즘
- find the **smallest** unsorted element and add it to the end of sorted list.
- _in pseudocode_:
  - Repeat until no unsorted elements remain:
    - Search the unsorted part of the data to find the smallest valued
    - Swap the smallest found value with the first element of the unsorted part

## Code

```swift
func selectionSort(_ array: [Int]) -> [Int] {
    guard array.count > 1 else { return array }  

    var arr = array                    

    for x in 0 ..< arr.count - 1 {  
        var lowest = x
        for y in x + 1 ..< arr.count {
            if arr[y] < arr[lowest] {
                lowest = y
            }
        }
        if x != lowest {
            swap(&arr[x], &arr[lowest])
        }
    }
    return arr
}
```
---
refer to
- [CS50](https://youtu.be/3hH8kTHFw2A)
