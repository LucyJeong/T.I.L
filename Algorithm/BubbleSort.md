# Bubble Sort
![bubble sort from wiki](https://upload.wikimedia.org/wikipedia/commons/c/c8/Bubble-sort-example-300px.gif)
- **Bubble Sort** 는 인접한 두수를 비교하여 큰 수를 뒤로 보내는 간단한 정렬 알고리즘. 시간복잡도는 *O(n^2)*. 다른 정렬 알고리즘에 비해 속도가 상당히 느린 편이지만, 코드가 단순하기에 자주 사용됨.
- 원소의 이동이 거품🛁이 수면으로 올라오는 듯한 모습을 보이기 때문에 Bubble Sort라는 이름을 가지게 됐음.
- In bubble sort, the idea of algorithm is to move higher valued elements generally towards the right and lower value elements generally towards the left.
- __in pseudocode__:
  - Set swap counter to a non-zero valued
  - Repeat until the swap counter is 0:
    - Reset swap counter to 0
    - Look at each adjacent pair
      - If two adjacent elements are not in order, swap them and add one to the swap counter
- **Worst-case scenario**: The array is in reverse order; we have to "bubble" each of the *n* elements all the way across the array, and since we can only fully bubble on element into position per pass, we must do this *n* times.
- **Best-case scenario**: The array is already perfectly sorted, and we make no swap on the first pass.

## 코드
```swift
func bubbleSort(_ array: [Int]) -> [Int]
{
    var arr = array
    for _ in 0...arr.count
    {
        for value in 1...arr.count - 1
        {
            if arr[value-1] > arr[value]
            {
                let largerValue = arr[value-1]
                arr[value-1] = arr[value]
                arr[value] = largerValue
            }
        }
    }
    return arr
}
```
- swap함수를 이용하는 방법

```swift
var arr = [3,10,9,7,5]
for i in 0..<arr.count
{
    for j in 0..<arr.count-1
    {
        if arr[j]>arr[j+1]
        {
            swap(&arr[i],&arr[j+1])
        }
    }
}
```

---
refer to
- [Bubble Sort : 거품 정렬](http://bowbowbow.tistory.com/10)
- [Bubble Sort of CS50](https://youtu.be/RT-hUXUWQ2I)
- [Swift3 ) Swift로 버블정렬(Bubble Sort)짜보기](https://zeddios.tistory.com/67)
- https://tech.io/playgrounds/506/sorting-in-swift/bubble-sort
