---
## 리스트(List)
리스트는 동적 배열로, 크기가 고정되지 않고 필요에 따라 자동으로 크기가 조정되는 자료구조입니다.

### 특징
1. 동적 크기 : 리스트는 크기가 고정되지 않고, 요소가 추가되거나 제거될 때 크기가 조정됩니다.

2. 순차적인 접근 : 리스트는 요소들이 순차적으로 저장되어 있으며, 인덱스를 통해 각 요소에 접근할 수 있습니다.

3. 다양한 데이터 타입 : 리스트는 임의의 데이터 타입을 저장할 수 있습니다. 이는 배열과 비슷하지만, 리스트는 동적으로 크기가 조정되는 특징을 가지고 있습니다.

### 장점
1. 동적 크기 : 요소가 추가되거나 제거될 때마다 리스트의 크기가 동적으로 조정되므로, 공간의 효율적인 사용이 가능합니다.

2. 유연성 : 리스트는 임의의 위치에 요소를 추가하거나 제거하는 것이 가능합니다.

### 단점
1. 접근 속도 : 리스트는 인덱스를 통해 요소에 접근할 수 있지만, 배열에 비해 접근 속도가 느릴 수 있습니다.

2. 메모리 오버헤드 : 리스트는 동적으로 크기가 조정되는 과정에서 추가적인 메모리를 요구할 수 있습니다.

### 사용 예시
리스트는 데이터의 동적인 추가와 삭제가 필요한 경우에 사용됩니다. 예를 들어, 사용자의 입력을 받아 저장하거나, 데이터를 동적으로 로드해야 하는 경우에 리스트는 매우 유용한 자료구조입니다.

---

```
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // 리스트 생성
        List<int> list = new List<int>();

        // 리스트에 값 추가
        list.Add(10);
        list.Add(20);
        list.Add(30);

        // 리스트의 값 출력
        for(int i=0; i< list.Count; i++)
        {
            Console.WriteLine($"Element at index {i} : {list[i]}");
        }
        Console.WriteLine();

        // 리스트에서 값 제거
        list.Remove(20);

        // 리스트의 값 출력
        for(int i=0; i< list.Count; i++)
        {
            Console.WriteLine($"Element at index {i} : {list[i]}");
        }
	}
}
```

<br>
출력 결과
<br>
<img src="https://velog.velcdn.com/images/dbsdbds4532/post/7b8563a3-68f6-4260-afc6-257e131027c7/image.png" width="240px" align="left">
